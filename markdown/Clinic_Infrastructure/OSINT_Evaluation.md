
# Security Evaluation Framework for OSINT Tools

Research Process, Prototype, and Justifications

Citizen Clinic, Spring 2020

Rachael Cornejo and Thyne Bookmark

____________________________________________________________________________

Skip to [current prototype.]("https://www.citizenclinic.io/Clinic_Infrastructure/OSINT_Evaluation/#prototype")

Want to get involved? Fill out this form: https://forms.gle/8pKCoVpkKKEzrjU6A

__________

## Motivation

Public-interest investigative research using online open source intelligence (OSINT) methods involves utilizing various online tools and searching through various online platforms to find sensitive information.[^1] During this process, public-interest OSINT researchers such as journalists, lawyers, and human rights defenders open themselves up to online risks: use of digital tools creates points of weakness which can reveal researchers’ locations, activities, contacts, and other data.[^2][^3][^4][^5][^6] Protecting oneself online is thus an essential part of OSINT investigations, but unfortunately doing so can be a difficult process. For many investigators, conducting a comprehensive risk assessment and choosing appropriate mitigations is too time consuming and difficult a task to incorporate into their workflow. Our team’s work attempts to make this process easier. We provide a framework to help investigators understand their security needs before beginning a project, and then decide which tools are appropriate for this project based on these security needs.


## Target Audience

To envision our target audience and design our framework accordingly, we crafted user personas.[^7] Our personas were public-interest investigators with different levels of experience and technical knowledge. The process of creating user personas revealed multiple insights about how our target audience could utilize our framework: first, our framework could help researchers new to OSINT reflect on their security needs before an investigation and point them in the direction of tools that would suit these needs. Second, our framework could help more experienced investigators educate others as part of a security training curriculum. Third, our framework could be particularly useful for investigators working on particularly sensitive projects with greater security needs than normal projects.



1. Our first user persona, Fátima, is an experienced investigator who is being paid by an advocacy-oriented nonprofit within the United States to investigate local white supremacist groups: her bosses want to understand who these groups’ leaders are, what types of news and multimedia group members share, whether this news is accurate, and how these groups organize protests and other events. Although she has investigated problematic leaders in other countries, Fátima feels trepidation about carrying out such a project in the U.S., where she thinks those she is researching could easily do harm to her if they found out she was investigating them. She wants to learn how to protect her identity, but is not sure where to look.
2. Our second user persona, Javier, lives in Mexico and spends his time training professionals around the world – mostly journalists and lawyers – on the benefits of utilizing OSINT both in the newsroom and the courtroom. Javier trains professionals in OSINT because he believes OSINT techniques open up new opportunities for them for more impactful pieces of journalism and more impactful legal cases. However, he knows the professionals he works with deal with sensitive issues and wants them to be safe while they use these techniques – he does not want to teach these professionals skills which leave them in more danger than they were before. At the same time, teaching professionals these skills takes a long time and it can be hard to find time to teach security – plus, he does not want to scare professionals away from using these tools.
3. Our third user persona, Aiko, is an U.S.-based investigative journalist who just learned some basic OSINT techniques at a training. She thinks these new skills could make for a cool, unique story. She has also been turning over the idea of breaking a story on surveillance of Islamic Americans who are suspects of terrorism. After the OSINT training, she decides to see whether she can use OSINT to find out more about occasions in which Islamic-Americans have been victims of police surveillance. Aiko has read info about Snowden’s leak and knows American government surveillance of these types of issues is high after 9/11, thus leading to potential risk for herself if she investigates further. However, she thinks this is an important under-reported story and wants to work on it, both to bring much-needed attention to this issue and to advance her career.


## Methodology


### Background Research

To inform our design and prototyping, we conducted research on approaches for helping users to understand their digital security and on previous attempts to create frameworks for evaluating digital tools.

#### ** Helping Users Understand Digital Security **


1. The paper “Obstacles to the Adoption of Secure Communication Tools”[^8] explores how different users understand the security of communication tools, and explains what motivates their messaging app choices.The researchers found that many participants have misconceptions about different communication tools’ security, and are mistaken in their reasoning behind which tools to use.The paper’s findings showed us that average users are not familiar with security concepts and thus need more detailed guidance on risks associated with using certain applications.


2. The paper “Why Johnny Can’t Encrypt”[^9] explains that security mechanisms are only effective when used correctly, and that more than 90% of all computer security failures occur because users have not configured their technologies properly. This paper showed us that in order to help keep investigators secure, we should not only help them choose tools which are appropriately secure for their purposes, but also help them understand how to configure any tool they choose to use in the most secure way possible.

#### **Previous Frameworks for Evaluating Digital Tools**

1. The primary case study we considered was Version 1 of the Electronic Frontier Foundation (EFF’s) Secure Messaging Scorecard. While outdated and considered by the EFF to be insufficient as a recommendation tool, the secure messaging scorecard provided a good starting point for creating a tool evaluation system. The scorecard is presented as a graph with checkmarks notating whether or not a variety of messaging platforms satisfy certain security considerations, such as providing encryption in transit and keeping past communications secure if one’s encryption keys are stolen. Although it has been left online for historical reasons, EFF’s website states that this scorecard does not reflect the most recent developments for all of these messaging platforms.[^10] As an alternative, EFF offers _Surveillance Self-Defense_, a more complex set of tools and how-tos for safer online communications which includes “how-to” guides for certain security tools but does not offer an overarching security matrix of tools in the field for easy comparison.[^11] In a separate article entitled “Why We Can’t Give You a Recommendation,”[^12] EFF explains why the org has steered away from making recommendations on which messaging tool users should implement to be most secure. Tool developers can make sudden changes to their tools which change the tools’ pros and cons with regard to security, security features are only one of multiple variables that matter when choosing a secure messenger (including usability, cost, countries a tool is used in, whether it works on iPHone or Android), and the specific threats someone is worried about influence which messenger is right for their purposes. Another EFF article called “What Is a Good Secure Messaging Tool?” points out that by including checkboxes, Version 1 of EFF’s scorecard can accidentally suggest that there is a single standard for security and that a tool can be 100% “secure” if it checks all the boxes, when in reality security is context-specific and never guaranteed.[^13] These observations from EFF suggested to our team that if we were to create an effective framework to evaluate the security of OSINT tools, we should do three things: include categories beyond traditional “security” features, avoid the checkbox format, and create a clear process for the continued maintenance of our tool.


2. In addition to the EFF scorecard, we researched two other websites which are designed to help users to improve their online safety: Citizen Lab’s security planner and the Digital Defenders Partnership’s digital safety manual for human rights defenders.[^14][^15] Both resources suggest a variety of tools (such as browser extensions) and practices (such as updating your apps) which can help users become more secure. However, these publications primarily propose more secure solutions rather than evaluating the security of existing tools which those in the field already use. In addition, neither website caters this information specifically to the tools which public-interest investigators use in order to accomplish their work: more popular tools like web browsers and secure messaging tools are covered, but not investigator-specific tools like Hunch.ly and SunCalc. Thus, although these tools provide helpful potential models for structuring our tool, their content differs greatly from our project content, showing us that our framework occupies a unique niche.


3. The closest comparison we found to a security framework for OSINT is Michael Bazzell’s Buscador OSINT Virtual Machine, a collection of instructions for users to create a secure “investigative operating system.”[^16] Although Buscador is now out-of-date and Bazzell now recommends a DIY Custom OSINT VM, Buscador provides an example of a secure OSINT setup. However, rather than providing his readers with understanding of why he has housed his system in a VM and why each of the tools he has suggested are necessary, Bazzell lists them and provides instructions for installation. Based on our research into helping users understand digital security, we decided that our tool should focus more on providing explanations and offering options for tools than does Bazzell’s.

### Interviews

To supplement our desk research, we judged that user testing through interviews would provide us with the best sense of how to structure our framework. We focused on individuals who have experience within the public-interest OSINT community either as investigators, trainers of OSINT investigators, and investigative tool developers. 

We first interviewed investigators to gain an understanding of what they do to perform investigations securely and if there are any ways to improve this process. These initial interviews showed us that OSINT investigators lack a quick and efficient method of evaluating security tools, and that many investigators forgo the tool evaluation process as they do not have time to do it.

Once we had a prototype for our framework, we conducted interviews with members of the OSINT community to get feedback on its design, usefulness, and ways to incorporate it into their investigative workflows. Some of these individuals also train investigators, and we asked for their feedback on ways to improve our framework’s usefulness as a training tool. While our framework’s target audience is mainly investigators, we wanted to ensure that our framework formed an accurate depiction of various OSINT tools’ security. We thus also spoke with application developers who had experience as online investigators.


#### Interview Takeaways

** Use Cases: ** The investigators we spoke with believed that our framework would be valuable early on in the investigative process. Interviewees stated that the framework could encourage investigators to better think through security considerations when deciding what tools to use in an investigation, perhaps as part of an initial risk assessment and/or threat modeling process. However, we also learned of some limitations of our work. Because of our framework’s length, interviewees believed that the framework would mainly be useful when planning for longer term investigations into high risk areas. They emphasized that if an investigator has a shorter timeline, they are more likely to stick to whatever tools they are more familiar with and not spend the extra time assessing and choosing new tools. We also found a use case we had not previously considered: tool developers we spoke with found that our framework would be helpful for informing clients and consumers of the features and limitations of their product. This is because the questions included in our framework align with those law enforcement and larger companies ask before deciding to use an investigative tool.

** Compatibility with Existing OSINT Workflows & Training Programs: ** We asked our interviewees about their existing workflows and their thoughts as to where our framework could fit. Multiple interviewees said they would like to see our tool integrated with the Berkeley Protocol on Open-Source Investigations, a forthcoming resource which will set common guidelines for the use of OSINT in international legal and human rights investigations.[^17] The Protocol outlines steps for OSINT researchers to build an online investigation plan & strategy, and although the Protocol is not yet public, some interviewees stated that OSINT trainings for journalists and lawyers already take place with the Protocol in mind. Overall, our interview responses emphasized our framework’s potential usefulness as a tool for training OSINT researchers and investigative journalists, and highlighted the need for further research into how we can align future versions of the tool with these established OSINT workflows and training programs. One interviewee even suggested linking our tool to existing security resources, such as the EFF Security Scorecard and Citizen Lab security planner.

** Tool Format: ** When speaking to investigators, we found that many would find a “security scorecard” rating system very useful. Interviewees said having a concrete score of some kind would make the tool evaluation process much more convenient. One investigator also stated that he would like to see a rating of whether a tool is “low risk” or a “high risk” plotted against a y-axis of how often breaches happen. However, although we noticed demand for a true rating system and for quantification of the risks inherent to a tool, our initial research led us to reject such a system due to the way that security is context-specific – a tool which is secure or low-risk for one investigation could be completely insecure or high-risk for another. This topic is discussed further in our Attributes and Justifications section.

In addition, our interviewees suggested two different ways to organize the information provided about each tool. One suggestion was to show a list of pros and cons for each tool. The other was to separate different attributes based on which tool type they were applicable to. For example, interviewees mentioned that they would like to choose a specific type of tool to examine, messaging tools for instance, and then be shown all the tools specific to that type of application, in order to compare and contrast across tools. Also, our interviewees stated that they would appreciate guidance on how to configure settings to optimize each tool’s security, so that once they decide on a particular tool they can make sure it is configured as securely as possible. Finally, one investigator suggested that he would like to see an “endorsements” section of our tool – similar to the one which can be found on Hunch.ly’s website – in order to lend the tool legitimacy. 

** Tool Categories: ** In our interviews, investigators said they would like to see our framework applied to the following categories of investigative tools: social media platforms, satellite tools, data organizing tools, browsers, VPNs, email services, and collaboration applications. Tool categories could also take into account existing well-known lists and categorizations of OSINT tools, such as Bellingcat’s Online Investigations Toolkit[^18] and First Draft News’s Verification Workstation.[^19] Interviewees also said they would like our framework to include case studies to help them understand the real world implications of certain features. Case studies could also show how specific features were useful to past investigators, which would help cement their practical application to our framework’s users. 

** Visual Design: ** Our interviewees, particularly the non-developer interviewees, emphasized that an appealing visual design would be necessary in order to convince them to use the tool. Because they have limited time for each investigation, interviewees said they would not use our framework if it was hard to navigate, too detailed, and not visually intuitive. One interviewee suggested the idea of having a few key security considerations outlined at the top of the framework webpage, with a dropdown menu which highlights other categories of interest. Similarly, multiple interviewees said they would love to see a compact number of boxes or attributes which expand to reveal more text once the user clicks on it. Our team sees pros and cons to this idea – such a design could perhaps obscure important information about a particular tool, but could also increase the overall usability, and therefore likelihood of use, of our framework. 


## Security Assessment Design

To organize our framework, we created five overarching categories which our research suggested investigators should be aware of: provider & geography, provider transparency, personal identifiers, security features, and tool usability & maintenance.

We created these categories based upon feedback from our initial conversations with OSINT investigators. Initial interviewees highlighted the need for some sort of overarching categorization which would help investigators understand the different types of security considerations they should keep in mind. Because one of our project goals is to make security approachable for those unfamiliar, we thus decided to adopt a categorization system.

Although we renamed and slightly reshuffled these categories throughout the design process, the same five general concepts held firm throughout. In contrast to the EFF secure messaging scorecard which primarily addressed technical security of tools, we reasoned that although these technical security features are very important, technical security should be one of multiple categories that investigators consider when evaluating security. Thus, technical security features make up one category of five, and are not the first category listed in our prototype. Instead, we reasoned that the identity of the tool's provider – as well as location of that provider – would be important initial information for investigators to know, since where a tool’s provider is based can impact which governments have most potential access to any information stored by their systems. Similarly, we decided that tool provider transparency regarding legal threats and security vulnerabilities within a tool was an important category to then consider. Third, we reasoned that if a tool requires certain personal identifiers to use, this may necessitate the use of burner profiles and affect how investigators interact with the tool – thus, we listed personal identifiers third. Only after considering provider and geography, transparency, and potential necessity or personal identifiers did we judge it necessary for investigators to need information about a tool’s particular security features, making security features our fourth category. Finally, we reasoned that an investigator happy with a tool’s security features would have questions about its usability and maintenance, making this question the farthest down of our five categories. In particular tool usability and maintenance (as well as creator transparency) can be vital if investigators are considering using a tool long term.

Since we want our tool to be usable by investigators with little to no technical background, with each security attribute we have included a high level description and a justification for its inclusion in our framework – in other words, an appeal to why investigators should consider it important. This additional explanation and information should help define security concepts in concrete terms relevant to OSINT investigators and help them reflect on their security needs before an investigation.


## Attributes and Justifications by Category

** Not Including a Tool Rating: ** While a numeric score representing tools’ security was requested by multiple investigators, our team avoided implementing such a system because it leaves little room for nuance and would not teach investigators how to evaluate their own context-specific security needs. Looking at the EFF’s previous endeavors in security scorecards, we learned that we cannot label tools as completely “secure.” The importance of certain security factors heavily depends on the context in which the tool will be used, and lots of information needs to be understood about an investigator’s context before making this decision.[^20] Our team thus wanted to outline what considerations investigators should think about and to teach investigators to think critically about these considerations, rather than making a decision for them. 


### Provider & Geography

The “Provider & Geography” category of our framework contains information about the tool provider’s access and retention of information and motives for developing the tool, as well as the country where the provider is located and any countries in which use of the tool is restricted. The “Provider – Goal” attribute was initially called “Provider – Entity” and, along with the ““Provider – Country” attribute, was listed before all other categories in this section. We initially placed these two categories highest on the list because they seemed intuitively important. However, based on feedback from one of our project advisors, we realized that in order to make effective decisions as to whether to use a tool from a specific provider, an investigator first needs to understand what types of data the tool can access, as well as whether, and how, the tool stores this information. If investigators do not know what data is being accessed temporarily by a tool and whether this data is stored more permanently even temporarily, they cannot accurately make other key security decisions. Once investigators understand these two key considerations, they can then evaluate whether they are willing to input their data for a specific investigation into a tool whose provider has specific potential goals and is from a specific country. 

** “Provider” vs “Developer” vs “Owner” ** – Our team initially labeled this category “Owner & Geography” and also included the phrase “developer” in our prototype – however, we realized that owner and developer were two different categories, and that using the two terms interchangeably was confusing. In addition, one project advisor pointed out to us that the developer or a tool may not be its owner. Thus, we settled on the phrase “provider” to describe the entity which owns, and/or develops, and/or maintains the tool.

** “Provider – Entity” → “Provider – Goal” ** – Initially we included an attribute called “Provider – Entity” which listed the name of the tool provider, but after speaking with one of our project mentors. we decided the name of the provider was not as important as the goals this provider has for the tool. Thus, the new category, “Provider – Goal,” includes both the provider name and their goal. In addition, although we reason that funding can sometimes give clues as to the goal of a project, funding never came up in our interviews or discussions with project mentors, and thus we do not currently include an attribute for funding, although one could be created or included as part of a reworked “Provider – Goal” attribute.

** Location-Based Bans ** – Although this attribute does not fit into the roadmap outlined above which connects the rest of the attributes in the “Provider & Geography” category, we included it in this category because it involves geography. We determined that access by country is important to include because some governments block the use of certain tools, rendering these tools unsuitable for certain investigations – one investigator confirmed that this attribute was important.


### Provider Transparency

The “Provider Transparency” section of our framework contains information regarding whether the provider is transparent about potential weaknesses within their platform which could make it insecure: this includes both technical vulnerabilities, and requests from governments and law enforcement to turn over data. One interviewee suggested that we combine this section with the country of origin section because creator transparency is dictated by jurisdiction in a lot of cases. Our research team felt that provider transparency was different enough from geography that it deserves its own category, but decided to order this section immediately after the “Provider and Geography” in the hopes that investigators will keep provider location in mind when evaluating provider transparency.

** Vulnerability Transparency – ** At first, this attribute was amorphous: “vulnerabilities” were not clearly defined. We included touting code as open source in this category, as an example of vulnerability transparency. However, one of our research mentors suggested that this section include information about bug bounty programs, as bug bounty programs suggest that a tool’s provider values security, as well as encourages tool providers to continually improve the security of their tools. One interviewee suggested that this category could also include information about how tool providers respond to known security issues, although our research team has debated creating a separate category for this attribute. 

** Government / Law Enforcement Interaction Transparency ** – Our interviewees agreed that this category was important. One interviewee suggested multiple metrics by which to evaluate tool providers’ transparency with regard to government and law enforcement interaction, including transparency reports and warrant canaries. Our team has observed that there is no universal way to quantify this attribute, and recommends further exploration. 

** Legal Obligations ** – This category initially included a section titled “legal obligations” which, like all other categories in the spreadsheet, contained a description, as well as a space to provide tool-specific information. However, multiple interviewees, including a lawyer who gave us feedback, emphasized that providers in any location can be obligated to turn content over to law enforcement when legally requested. Thus, we decided to take out space for tool-specific information in favor of notating that legal obligations are applicable to all tools. However, one interviewee suggested that our description should explain that these legal obligations are driven by jurisdiction – for example, US and Canada privacy/security laws are different – and that we could perhaps make it apparent in our chart which jurisdiction particular tools fall under.


### Personal Identifiers

The “Personal Identifiers” section provides a variety of information which relates to users’ personal identities – although these attributes do not build upon each other in a linear fashion, they share this common theme. Interviewees appeared to find this grouping of criteria intuitive. 

** Aliases ** – Developer interviewees found that this is a very important category that can make or break a product for users. Law enforcement groups in particular have a great need for aliases in certain tools.

** Data Required to Use ** – Interviewees found this to be important. Depending on the data required to use a tool (name, phone number, etc), investigators might have to set up a burner profile which is an important consideration to think about before starting a project. Although this category overlaps with the information collected in the “Provider access” and “Provider retention” areas of the scorecard, interviewees did not appear to notice this redundancy – no interviewees mentioned it. However, this overlap may still perhaps be an area for further refinement.

** Data Collected ** – Interviewees found this important and most relevant if they were working in sensitive scenarios. Developer interviewees also found that many investigators they worked with in the past cared about this, especially in terms of data portability (could users access and download data associated with them?). As with “data required to use,” thus section overlaps with the information collected in the “Provider access” and “Provider retention” areas of the scorecard, interviewees did not appear to notice this redundancy, although it could use more fine-tuning.

** Login and Contact Authentication ** – Forms of login authentication such as MFA and contact authentication like safety numbers were very important to our interviewees. It was suggested to us that other investigators with less familiarity of common security practices could use examples that demonstrate the importance of MFA and safety numbers. Threats associated with not having authentication may not be immediately clear to some potential users of our framework.


### Security Features

Our prior research and interviews demonstrated that before a researcher decides whether to incorporate a tool into an investigative workflow, this researcher must understand the security features the tool supports[^21] – although we contend that  “security features” is an amorphous term which may require more precise definition. However, we reasoned that since not all investigators have a technical background in regards to security there is a need to explain certain features in terms of their impact rather than their technical specifications, an attitude which was confirmed in our interviews with non-technical investigators. Our team’s goal in this section was thus not just to tell investigators what features a tool has, but to get them to understand what these features help protect against and if they would be necessary in the investigators’ context. 

** Retention of Metadata ** – Feedback from developers was that this is very important for investigators to consider, because metadata can be as powerful as actual data in terms of identifying individuals or groups.
 
** Cloud Storage ** – Feedback was mixed. Our project mentor noted that it is hard to define whether data is stored in the Cloud “securely,” and wonders how investigators will assess this. Further consideration of whether to include this category, and how to quantify it, is needed.

** Transport and End-to-End Encryption ** – Interviewees found these categories to be very important. However, they mentioned that for investigators with no familiarity with encryption or cybersecurity these category labels would not properly convey their importance. One interviewee thus suggested linking to supplementary materials that explain the technical details of these attributes more thoroughly for investigators who are curious, while others emphasized that we should use case studies and clear examples to convey the importance of encryption to our audience. In addition, one interviewee suggested combining these two categories together, although we ultimately decided to leave them separate transport encryption and end-to-end encryption provide very different levels of security. 

** Access Controls ** – Interviewees thought this category is important to keep in mind if a tool is going to have multiple collaborators.

** Open Source Code ** – From our developer interviews, this category appears to be important in certain cases. Some tools that are open sourced can be made more secure for users if they host these tools on their own servers. However, just because a tool is open source does not mean it is free of vulnerabilities – a third party audit can help determine this. Thus, the fact that an application has open source code may not be the best metric by which investigators should judge their security. However, our team left this metric in the scorecard for further development because our tool could perhaps serve as an opportunity to write a description for investigators as to why open source code is not an appropriate security metric.

** Independently Audited ** – Mixed response from interviewees. They stated that although public independent audits exist for some tools, such as Signal, the public often has no way to evaluate whether these audits have exposed vulnerabilities in the tools or not. In addition, tool developer interviewees suggested that law enforcement or government agencies perform many independent audits of applications, yet the results of these audits are kept private even from the tool developers. Thus, while potentially informative when available, audits may not be the best metric by which to judge the security of a tool.

** App vs Browser ** – We wanted to distinguish the difference between using a tool through its downloaded application versus using it through a web browser. Downloading an application can give it more permissions/access to certain aspects of a user’s device while using the browser version does not. From our interviews we found that investigators were interested in how security differs across app-based and web-based versions of a tool, and in the question of whether one version gives users more security than another. Further research and clarification is needed. In addition one interviewee brought up the question of whether tools operate using HTTPS vs HTTP, a consideration which we did not include but could be incorporated in the future.

** Ephemeral Messages ** – We added this category when we were testing our framework for the Signal messaging app, but eventually deleted it due to unfavorable reactions from interviewees. Investigators were not immediately sure of the term “ephemeral messages” and when clarified, it appeared to be low on their priorities in terms of security considerations. Developers could see how this could be important, but it seems to be more of a niche category that is not as much of a primary concern. We eventually concluded that the availability of ephemeral messaging as a feature could perhaps be subsumed under “data collected” or “provider retention.”


### Tool Usability and Maintenance

** Cost ** – Very important for our interviewees. For investigative teams, certain costs may be prohibitive and make a tool unfeasible to use. Developer feedback also told us that specific pricing models of tools could also be important for users (one-time payment, renewing license, etc). In addition, one interviewee mentioned security considerations related to the method of billing. He noted that a user in a particular country may not be able to purchase a certain because purchase by international credit cards is blocked. In addition, this interviewee mentioned that payments could potentially be tracked. Additional research into exact methods for quantifying this category is needed.

** Ease of Use ** – Feedback suggested that this category was too broad. One investigator mentioned that he would like us to expand upon the category and that he would want to know whether the tool provided a “good user experience,” although he admitted this terminology was vague. Developer interviewees suggested adding specificity around whether a tool requires a large amount of training. They found that if a tool is complicated enough to require training before it can be used properly, users might be turned away from the tool as it would take too long to incorporate into their work. More research into how to quantify this category is needed.

** Cross-user Collaboration ** –  Interviewees found this to be very important. If an investigator is working in a team on a project, tools that enable them to collaborate in one space become very valuable.

** User Support Capability ** – Interviewees found this to be important for tools. If they run into an issue while using an application, they want some form of support/troubleshooting available to them.

** Consistent Maintenance & Updates ** – Mixed response from interviewees. We originally had an “update frequency” category that was meant to gauge how well a developer was handling the security of their tool. However, the developers we interviewed mentioned how update frequency alone is not a great measure of a tool’s security: simply being updated a lot does mean a tool’s security is improving, because these updates may not relate to security. In addition, one interviewee brought up the consideration of how updates are delivered – whether they are delivered online vs deployed by the provider. Further refinement is needed.

** Compatibility with Other Systems ** – Our initial draft of our prototype contained this category, but we removed it because we thought it was vague and was not sure how to quantify it. However, one interviewee mentioned this category of his own accord. He explained that outlining a tool’s compatibility with other commonly used OSINT tools could be useful because he has observed that many users do not often buy tools in isolation This interviewee explained that private investigators and journalists may buy tools in isolation; but users running firms, law enforcement agencies, and research organizations buy stacks of compatible tool chains. However, because the primary audience of our scorecard is investigators who work alone or in small teams, we decided not to add this attribute back into our framework.


## Next Steps

** Testing and Community Feedback **

We conducted research with a small sample size of participants and believe that further input from a wide variety of OSINT researchers will be key to developing a tool which works for as many researchers as possible. We need to test our prototype to see whether what we have built actually solves the problems we initially thought it could solve, and whether it fits nicely into existing OSINT workflows. Thus, we recommend sending our prototypes out to a large group of international public-interest OSINT researchers from a variety of fields, including journalism, law, and advocacy. This “call to action” could include sending our prototype out via Google Docs or GitHub and asking for comments, and scheduling interviews with those interested in providing more in-depth feedback. It could also include presenting our prototype at conferences and working groups composed of relevant stakeholders.

** Refining Categories: ** To make using our framework easier for investigators, our current  should be grouped hierarchically based on tool type and importance of an attribute. Not every attribute in our framework is relevant for every tool, and it would be useful to clarify which tool types (messaging, preservation, geo-locating, etc) each attribute is meant for. For example, it would be useful for all criteria relevant to messaging apps to be grouped together, all criteria relevant to preservation tools grouped together, etc. Interviewees also mentioned that they would like to view highly impactful application features first – such as cost, end-to-end encryption in messaging apps, etc – and then be able to optionally view “nice to have” features. Thus, future research could identify what information is necessary to show at the top of the framework, and how to order all other features.

** Developing UI system **

From our interviews we found that the current table format of our framework can take a long time to read through. Once we have further refined our tool evaluation attributes and grouped them into categories, it would be helpful to integrate them into some interactive system so users could choose to look at the features most relevant to them rather than the entire list. The investigators we spoke to suggested that the tool would be easier to use if it was interactive and let users select certain attributes based on tool types. Creating such a system would require more design work, web interface work, as well as thorough usability testing with members of the OSINT community.

** Increasing Accessibility **

In order to not alienate the users whom our tool is meant for, future work on this prototype should include simplifying its technical language, as well as providing more tangible examples, case studies, and explanations which help users learn about security and change the way they think about security, rather than simply informing them of tool attributes. 

** Expanding Framework to More Tools **

Our current framework has primarily tested messaging and preservation tools, but in the future we would like to expand it to be applicable to other types of tools, such as social media platforms, satellite tools, data organizing tools, browsers, VPNs, email services, and collaboration applications. The four tools we have tested so far include Signal, Whatsapp, Hunch.ly, and Check – thus, the current iteration of our work is mostly geared to describe the security of these types of messaging and preservation tools. However, expanding the types of tools our framework can evaluate would make our framework more comprehensive, and make it more useful to investigators who may require a wider array of tools. Testing other types of investigative applications would help uncover features specific to them, which in turn could help clarify what security considerations investigators should think about when choosing these tools. 


## Conclusion

Our research team has completed the first steps towards creating a framework which can be used to evaluate the security of tools which public-interest OSINT researchers commonly use. We have identified that many OSINT researchers input sensitive information into a variety of digital tools, yet lack effective methods for evaluating the security of these tools and deciding which tools are appropriate for a particular investigation. We explore a potential solution to this problem by proposing a framework which OSINT researchers can use during the initial planning stages of their investigation to decide which tools will be most secure for the project. In the future, we recommend continued testing of our framework to discover whether it actually helps address the problem it purports to solve. We also recommend the exploration and creation of an intuitive UI system which ensures that our framework can be easily implemented by our intended audience. Finally, we recommend additional research into ways in which this tool could be designed and presented to fit into investigators’ existing workflows.

We learned that rather than subjectively evaluating whether a certain tool is “safe,” we should teach investigators to evaluate tools based upon the investigators’ specific project and situation. Our framework should bring investigators attention to security features that are important, but which these investigators may never have considered. Thus, our tool should provide a learning experience to investigators as to which security considerations should be taken into account and why. Our team is still grappling with the best way to encourage such learning in a usable, simple format, but further testing and refinement should help achieve this goal.


### Acknowledgments

We extend our utmost thanks to the following people for providing invaluable input and advice on this project: Steve Trush, Citizen Clinic; Kristin Berdan, Citizen Clinic; Bill Marczak, Citizen Clinic & Citizen Lab; Justin Seitz, Hunch.ly; Michael Elsanadi, Syrian Archive; John Ortilla, Human Rights Investigations Lab at UC Berkeley Law.

<<div id="prototype"></div>

## Current Prototype

<table>
  <tr>
   <td colspan="4" ><strong>Security Framework for OSINT Tools</strong>
   </td>
  </tr>
  <tr>
   <td><strong>Category</strong>
   </td>
   <td><strong>Attribute</strong>
   </td>
   <td><strong>Description</strong>
   </td>
   <td><strong>Why choose this attribute?</strong>
   </td>
  </tr>
  <tr>
   <td colspan="2" >Basic Functionality
   </td>
   <td colspan="2" >How can the tool be useful for an investigation?
   </td>
  </tr>
  <tr>
   <td rowspan="5" >Provider & Geography
   </td>
   <td>Provider Access
   </td>
   <td>What information does the tool gain from the user, even temporarily?
   </td>
   <td>Outlines the information companies/government(s)/cyber criminals could potentially have access to – how sensitive is this information?
   </td>
  </tr>
  <tr>
   <td>Provider Retention
   </td>
   <td>Does the tool retain this info more permanently and if so, how/where is it stored?
   </td>
   <td>Outlines the information companies/government(s)/cyber criminals could potentially have access to
   </td>
  </tr>
  <tr>
   <td>Provider Goal
   </td>
   <td>Who owns and/or developed the tool and what are their plans for the data?
   </td>
   <td>Gives a tentative idea of what the owner may do with the information stored in the tool. (Targeted advertising, used to improve the service, etc.)
   </td>
  </tr>
  <tr>
   <td>Provider Location
   </td>
   <td>Where is the provider located or headquartered? 
   </td>
   <td>Gives an idea of which government(s) could potentially gain access to above information which goes through a tool.
   </td>
  </tr>
  <tr>
   <td>Location-
<p>
Based
<p>
Bans
   </td>
   <td>Banned in any locations? Attempts to block?
   </td>
   <td>Ex. if investigating China, using Facebook will not be useful because Facebook is disabled in China.
   </td>
  </tr>
  <tr>
   <td rowspan="3" >Provider Transparency
   </td>
   <td>Vulnerability Transparency
   </td>
   <td>Does the provider have a robust bug bounty program? Do they publish public bug reports? How does the provider handle known security issues?
   </td>
   <td>Publishing bug reports and having a bug bounty program can encourage third party researchers to uncover potential flaws in a tool. This then helps developers strengthen the security of their product. 
<p>
Notification of security issues helps users understand when a product’s security has been compromised. 
   </td>
  </tr>
  <tr>
   <td>Government / Law Enforcement Interaction Transparency
   </td>
   <td>Do developers have a realistic and transparent attitude toward government and law enforcement?
   </td>
   <td>Organizations which care about notifying their consumers of possible legal requests may publish transparency reports and/or utilize warrant canaries to alert the public to both the existence and the fulfillment of such requests.
   </td>
  </tr>
  <tr>
   <td>Legal Obligations
   </td>
   <td colspan="2" >All providers can be obligated to turn content over to law enforcement when legally requested. 
   </td>
  </tr>
  <tr>
   <td rowspan="5" >Personal Identifiers
   </td>
   <td>Aliases
   </td>
   <td>Do you have to use a personal identifier (phone number, real name, etc) as a public-facing username?
   </td>
   <td>Having an alias can safeguard against leaking personal identifiers (such as phone numbers) to onlookers. 
   </td>
  </tr>
  <tr>
   <td>Data required to use
   </td>
   <td>How much information do you have to hand over to the provider in order to sign up?
   </td>
   <td>While performing research on certain online communities, investigators should take care to protect their anonymity and reduce the amount of information that may point to their true identity, else open themselves to greater risks.For example, if a tool user is forced to enter their personal phone number as their username and police track their phone number, police could arrest them. Accounts and services that require personal identifiers to sign up (such as phone number, full name, etc) may then necessitate the use of burner profiles/devices by an investigator. Some information, such as a linked phone number, are more resource intensive to set up and should be taken into account before an investigation. 
   </td>
  </tr>
  <tr>
   <td>Data collected
   </td>
   <td>What type of information does the company collect?
   </td>
   <td>If an investigator is performing sensitive work on a platform or service, it is important to know if any of this will be stored by the host. If so, this information could be requested and accessed by other entities such as law enforcement.
   </td>
  </tr>
  <tr>
   <td>Login Authentication
   </td>
   <td>If login required, offers multi-factor authentication?
   </td>
   <td>Multi-factor authentication (use of a second method of verifying your identity when you  log into an account, in addition to a password) adds an extra layer of protection. If an attacker got their hands on your login credentials and you use MFA, they will have much more trouble accessing the user’s account without access to the user’s secondary authentication method than if you do not use MFA.
   </td>
  </tr>
  <tr>
   <td>Contact Authentication
   </td>
   <td>Can you be certain that the person being contacted is the intended recipient?
   </td>
   <td>Apps that let you verify the identity of your contacts helps protect against man in the middle attacks. Verifying who you are communicating with can help prevent you from sending information to an unintended audience – for example, an enemy pretending to be someone you trust.
   </td>
  </tr>
  <tr>
   <td rowspan="8" >Tool Security features
   </td>
   <td>Retention of Metadata
   </td>
   <td>Does the company retain data surrounding the content you create/upload?
   </td>
   <td>Metadata relation to an individual’s use or interactions with a tool/platform could possibly reveal personally identifying information. For example, if an investigator is working on a collaborative platform with individuals of a vulnerable population, metadata related to who accessed/made changes on the platform could linke the individuals to the investigator.
   </td>
  </tr>
  <tr>
   <td>Cloud Storage
   </td>
   <td>Does the company retain data in the cloud? If so, is it stored securely?
   </td>
   <td>If a company keeps users’ data in the cloud and proper protections are not implemented, there is increased risk of personal data being exposed or leaked to the public. 
<p>
Failure of a cloud service may also lead to irreversible loss of users’ data.
<p>
If data is kept unencrypted in the cloud, the data may be shared if the company is compelled by  law enforcement or other government entities.
   </td>
  </tr>
  <tr>
   <td>Transport encryption
   </td>
   <td>Does the tool protect messages from being listened in on by outsiders?
   </td>
   <td>Transport encryption protects data when it is being transported between two communicating parties. This helps protect against adversaries trying to spy on the data. However, transport encryption does not hide data from the company hosting the communication.
   </td>
  </tr>
  <tr>
   <td>End-to-end encryption
   </td>
   <td>Does the tool protect messages from being listened in on by outsiders AND the company hosting the tool?
   </td>
   <td>E2E encryption, like transport encryption, protects data while it is being transported. In addition, E2E also protects data from anyone besides the communicating parties. This means that the company behind the communication would not be able to access the data or share it with other entities. One might use end-to-end encryption so that instead of $5 to get your conversations, attackers have to pay $1 million to get these conversations – these attackers often practice “targeted interception” where they only attempt to compromise their top 1000 targets.
   </td>
  </tr>
  <tr>
   <td>App vs browser
   </td>
   <td>Do you have to download an app, or can you use this tool in your browser?
   </td>
   <td>Downloading a tool’s application may give it greater access to your device compared to using the tool as a browser extension or web-page.
   </td>
  </tr>
  <tr>
   <td>Access Controls
   </td>
   <td>Can you control who can access shared information?
   </td>
   <td>If an investigator is planning on sharing private documents or performing sensitive work through a tool, it is important that they be able to control who can access this information. If a tool defaults to making documents/information public, it is important that an investigator adjust settings.
   </td>
  </tr>
  <tr>
   <td>Open-Source Code
   </td>
   <td>Is the code publicly available for audits?
   </td>
   <td><strong>If you are an activist, what is actionable about this for you?</strong>
   </td>
  </tr>
  <tr>
   <td>Independently audited
   </td>
   <td>Have independent auditors checked the tool for security vulnerabilities? What have they found?
   </td>
   <td>If a tool has been independently audited by a third party and has a security report available, this could provide valuable information regarding the security of the application. If an audit has not found any significant security/privacy issues, then the tool may be less open to attacks from more technical adversaries and hackers.
   </td>
  </tr>
  <tr>
   <td rowspan="5" >Tool Usability & Maintenance
   </td>
   <td>Cost
   </td>
   <td>Free to use? If not, how expensive?
   </td>
   <td>Free to use tools are more accessible, especially to non-profit or resource constrained organizations.
   </td>
  </tr>
  <tr>
   <td>Ease of use
   </td>
   <td>Easy to set up? Does it require training to know how to use it?
   </td>
   <td>A good tool should be straightforward and easy to use. If the tool is unintuitive, users may accidentally misuse the tool and introduce new risk into their workflow.
<p>
If the tool is complicated enough to require training to use it properly, it would be more difficult to initially incorporate it into investigations.
   </td>
  </tr>
  <tr>
   <td>Cross-user collaboration
   </td>
   <td>Does this tool allow for multiple collaborators/contributors in real time?
   </td>
   <td>If multiple investigators will be working together on a project, cross-user support may facilitate easier and more convenient collaboration.
   </td>
  </tr>
  <tr>
   <td>User support capacity
   </td>
   <td>If you run into issues using the tool, can you get support? How much support can you get
   </td>
   <td>Running into issues while using an application should be expected, and in these cases company support can be helpful and make the experience using a tool smoother. 
<p>
Support FAQs and training guides provide by a company can also be helpful in making the most out of a tool.
   </td>
  </tr>
  <tr>
   <td>Consistent Maintenance & Updates
   </td>
   <td>Are developers frequently maintaining and updating their application? If a security issue is found, do the developers quickly address the problem? 
   </td>
   <td>If an application is not currently being maintained, then any security flaws already existing in the tool will not be addressed. For long-term investigations, investigators may want to avoid out-dated tools in favor of tools that will continue to be updated to reduce the risk of technical vulnerabilities.
<p>
Frequency of updates can be helpful in determining how well a tool is maintained, but may not always be a good indicator of a tool’s security. 
   </td>
  </tr>
</table>



<!-- Footnotes themselves at the bottom. -->
## Notes

[^1]:
    [https://www1.essex.ac.uk/hrc/documents/Introductory_Guide_to_Open_Source_Inteligence_and_Digitial%20Verification.pdf](https://www1.essex.ac.uk/hrc/documents/Introductory_Guide_to_Open_Source_Inteligence_and_Digitial%20Verification.pdf)

[^2]:
     [https://academic.oup.com/jhrp/article-abstract/5/3/535/2188773](https://academic.oup.com/jhrp/article-abstract/5/3/535/2188773)

[^3]:
     [https://www.varonis.com/blog/what-is-osint/](https://www.varonis.com/blog/what-is-osint/)

[^4]:
    [https://www.researchgate.net/publication/312251766_A_New_Age_of_Open_Source_Investigation_International_Examples](https://www.researchgate.net/publication/312251766_A_New_Age_of_Open_Source_Investigation_International_Examples)

[^5]:
    [https://securityboulevard.com/2019/08/how-to-conduct-social-media-investigations-and-remain-anonymous/](https://securityboulevard.com/2019/08/how-to-conduct-social-media-investigations-and-remain-anonymous/)

[^6]:
     [https://opil.ouplaw.com/view/10.1093/law/9780198836063.001.0001/law-9780198836063](https://opil.ouplaw.com/view/10.1093/law/9780198836063.001.0001/law-9780198836063)

[^7]:
      [https://www.sciencedirect.com/science/article/abs/pii/S0142694X11000275](https://www.sciencedirect.com/science/article/abs/pii/S0142694X11000275)

[^8]:

     [Abu-Salma et al., 2017 IEEE Symposium on Security and Privacy. doi:10.1109/SP.2017.65](https://ieeexplore.ieee.org/document/7958575)

[^9]:

     [Whitten & Tygar, SSYM ‘99. doi:10.5555/1251421.1251435](https://dl.acm.org/doi/10.5555/1251421.1251435)

[^10]:

     [https://www.eff.org/pages/secure-messaging-scorecard](https://www.eff.org/pages/secure-messaging-scorecard) 

[^11]:
     [https://ssd.eff.org/](https://ssd.eff.org/) 

[^12]:
     [https://www.eff.org/deeplinks/2018/03/why-we-cant-give-you-recommendation](https://www.eff.org/deeplinks/2018/03/why-we-cant-give-you-recommendation)

[^13]:
     [Musiani, F. and Ermoshina, K. (2017). What is a Good Secure Messaging 
    Tool? The EFF Secure Messaging Scorecard and the Shaping of Digital
    (Usable) Security. Westminster Papers in Communication and Culture,
    12(3), 51–71.  doi:10.16997/wpcc.265](https://www.westminsterpapers.org/articles/10.16997/wpcc.265/)

[^14]:

     [https://securityplanner.org/#/all-recommendations](https://securityplanner.org/#/all-recommendations) 

[^15]:
     [https://digitalsafetymanual.org/](https://digitalsafetymanual.org/) 

[^16]:

     [https://inteltechniques.com/buscador/](https://inteltechniques.com/buscador/) 

[^17]:
    [https://humanrights.berkeley.edu/programs-projects/tech-human-rights-program/open-source-investigations-protocol](https://humanrights.berkeley.edu/programs-projects/tech-human-rights-program/open-source-investigations-protocol) 

[^18]:
     [https://docs.google.com/document/d/1BfLPJpRtyq4RFtHJoNpvWQjmGnyVkfE2HYoICKOGguA/edit](https://docs.google.com/document/d/1BfLPJpRtyq4RFtHJoNpvWQjmGnyVkfE2HYoICKOGguA/edit) 

[^19]:
     [https://firstdraftnews.org/latest/verification-workstation/](https://firstdraftnews.org/latest/verification-workstation/)

[^20]:
     [https://www.eff.org/deeplinks/2018/03/why-we-cant-give-you-recommendation](https://www.eff.org/deeplinks/2018/03/why-we-cant-give-you-recommendation) 

[^21]:
     [https://www.eff.org/deeplinks/2018/03/why-we-cant-give-you-recommendation](https://www.eff.org/deeplinks/2018/03/why-we-cant-give-you-recommendation)
