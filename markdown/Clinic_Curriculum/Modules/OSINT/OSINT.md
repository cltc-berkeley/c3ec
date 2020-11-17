### ** Summary **

This module describes how open source intelligence (or open source investigative techniques or OSINT) can be used for research. While OSINT uses publicly available sources of information to learn about an organization, an individual, or their contexts, there are risks that students and partners may face by gathering the information. This module will discuss safety precautions and tools to effectively organize collected information.

### ** Learning Objectives **

*   Learn how open source information can be used to protect civil society from cyberattacks.
*   Understand common OSINT techniques & sources for security researchers.
*   Determine when and how to begin collecting open source information.

### ** Pre-Readings **

* See Course Readings for ["Open Source Research Methods, Safety, and Tools"](../../../Consolidated_Bibliography#osint)

### ** Resources **

* [Citizen Clinic Virtual Identities guide](../../../Clinic_Infrastructure/Virtual_Identities.md)
* [Citizen Clinic Virtual Private Network guide](../../../Clinic_Infrastructure/VPN.md)

### ** Activities **

OSINT, open source intelligence (or open source investigative techniques), is using publicly available sources of information to learn about an organization, an individual, or their contexts.

Pop quiz! True or False?

1. OSINT-gathering activities cannot be attributed to the collector or collecting organization. 
2. Sources of OSINT information or methods of collection do not need to be protected.
3. OSINT is easily accessible.
4. OSINT can require a degree of technical expertise.

### ** Discussion **

Discuss the answers to the previous activity as a class.

Why might open source information be useful in our work with civil society organizations?


### ** Input **

Major categories of open source information:

*   Public media sources: news reports, printed magazines, and newspapers
*   Internet (Web 2.0) sources: archives, social media, blogs, discussion groups
*   Public government data: hearings, budgets, directories, and other public records.
*   Professional and academic publications: papers, theses, dissertations, and journals.
*   Commercial data: corporate databases, financial, and industrial assessments.
*   Grey data: Public but hard to get… conference promotional material, business documents, unpublished works, technical reports...

Starting points:

*   Direct from target websites
*   Nihad Hassan’s OSINT.Link: https://osint.link  
*   OSINT Framework: https://osintframework.com/
*   Bellingcat Online Investigation Toolkit: https://docs.google.com/document/d/1BfLPJpRtyq4RFtHJoNpvWQjmGnyVkfE2HYoICKOGguA/edit 

OSINT is an iterative process of methodically collecting, archiving, analyzing, and re-examining available data. Provide examples of taking a piece of information (such as domain name) and uncovering additional pieces of information (such as the real name of a website owner).

Key questions for this work:

*   How to organize collected information?
*   How to keep track of where you’ve been?
*   How to stay safe?

Tools for organization and archiving:

*   CherryTree
*   Maltego
*   Hunch.ly

How and where can your OSINT activities be tracked ?

*  Browser History
*  Router / Access Point
*  Internet Service Provider
*  Sites you directly visit (HTTP vs HTTPS)
*  3rd Party Sites (Lightbeam extension on Firefox)
*  What else?

How can we protect our open source investigations?

*   Virtual Private Networks
*   The Onion Router aka TOR (or Orbot)
*   Using a common browser (https://panopticlick.eff.org/)
*   Using Incognito / Private Mode
*   Using browser extensions:
    *   HTTPSeverywhere
    *   PrivacyBadger
    *   Brave “Shields Up”
*   “Burner” devices / virtual machines
*   Virtual identities, profiles & user accounts
*   Maintain separation between searches / sessions
*   Smart defaults (Ex: DuckDuckGo vs Google for searches)
*   Critical Thinking (avoid inadvertent connections)

Google Dorking (Advanced Search Queries): https://exposingtheinvisible.org/guides/google-dorking/

	Search: 

	* site:[target website] filetype:[pdf, docx, doc, xls or xlsx]

	* [target name] filetype:pdf 

	Write a script: 

	* site:[target website] + https://gist.github.com/heiswayi/641201f3bac04168108a 

Automated: 

recon-ng (in Kali) - you still need to enter API keys for most searches

### ** Deepening **

Each student team should create an OSINT research plan to gather information about their client’s context or potential threats.

The plan should contain the following:

1. What information are you seeking?
2. Where are you going to look?
3. What tools / resources do you need? (including burner accounts)
4. What precautions will you take to…
    1. Protect yourself?
    2. Protect your partner(s)?
    3. Protect your investigation?
5. What is your documentation system?
    1. Document your searches performed / sites visited / tools used
        1. Date, URL, & search terms at minimum
    2. Investigation type can dictate archive needs (do you need to capture the entire site? Screenshot?)

Each team will share elements of their plan with the class.

### ** Synthesis **

OSINT is not just an exercise in collecting all available information about an individual or organizations. When a practitioner reports their findings, they should succinctly describe:

1. What is the information?
2. Why does it matter? How could it be used?
3. Where (and when) did the information come from?
4. If defensive (ie, about a partner), is there a way to mitigate or prevent the information from being used in an attack?
5. If offensive (ie, about a threat), what are the next steps? Are there immediate actions that should take place?

