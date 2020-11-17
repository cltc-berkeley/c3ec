### ** Summary **

In this module, students will learn how and why social engineering is a common threat to civil society organizations. Attacks like phishing are simple and inexpensive to construct and execute and are a common vector for additional escalating threats. By understanding how these attacks are constructed, security practitioners are able to implement mitigations, deliver training, and evaluate resilience via phishing simulations. 

### ** Learning Objectives **

* Understand common social engineering attacks or attack vectors.
* Identify how the principles of persuasion are used for successful social engineering attacks,
* Describe the elements of a phishing simulation for training and evaluation.

### ** Pre-Readings **

* See Course Readings for ["Social Engineering and Phishing"](../../../Consolidated_Bibliography#phishing)

### ** Resources **

* [Citizen Clinic Phishing Simulation Resources](../../../Clinic_Infrastructure/Phishing_Simulation.md)

### ** Activities **

Break into small groups and use [https://phishingquiz.withgoogle.com/](https://phishingquiz.withgoogle.com/).

Have each group reflect on their experience. 

* Considering past module "Changing Security Behaviors," how might a quiz like this be useful to you or your client?

### ** Discussion **

* What is phishing and why do we care about it?

### ** Input **

Define social engineering.

Define the following social engineering attack vectors:

*   Phishing
*   Spear Phishing
*   Whaling
*   Smishing (SMS Phishing)
*   Vishing (Voice Phishing)

Source: https://www.social-engineer.org/framework/attack-vectors/

Examples: https://security.berkeley.edu/resources/phishing/phishing-examples-archive 

How do these attacks actually work?


*   Reciprocity:
    *   What could be offered to your partner that creates a desire for them to return the favor?
    *   The Golden Rule
*   Scarcity (“Urgency”)
    *   What does your partner need more of?
    *   What services does your partner rely upon?
*   Authority
    *   What sources of authority exist over your partner?
    *   Where does your partner lack expertise?
    *   Who would your partner let “overrule” their own judgement?
*   Consistency
    *   What activities, questions, or requests would be similar to what your partner already handles?
    *   What language, manners, and perspectives match an expected sender?
*   Liking
    *   What appeals to your partner?
    *   What characteristics are desirable in your partner’s context?
*   Consensus (“Social Proof”)
    *   How would you introduce a new collaborator to your partner?
    *   What bona fides does your partner look for from outsiders?
    *   Who are the other organizations that your partner works with?
    *   What statistical evidence might your partner care about? 

Provide examples of successful phishing attacks (eg, John Podesta DNC attack) and discuss how the principles of persuasion were leveraged.

How do we deal with phishing? How can your partner reduce the likelihood or impact of phishing?


*   Training
*   Technical Measures
*   Multi-factor authentication
*   Unique passwords
*   Information sharing and reporting across organizations 
*   Critical thinking

Creating a phishing campaign simulation for evaluation and training:

*   Target Research
    *   Context(s)
    *   Contact(s)
    *   Devices / OS
    *   Who and which platforms might your adversary target?
    *   Which approaches (Six Principles of Persuasion) might best “convince” your partner?
*   Sending Profile
    *   False persona, name, email address and domain (does the domain have DMARC or other spoof protection? Check www.dmarcian.com)
    *   Name
    *   Email Address + Domain / Phone Number 
    *   Persona
*   Sending Infrastructure
    *   Email Account (inside access?)
    *   SMTP Server (Simple Mail Transfer Protocol)
    *   Websites for sending spoof email / texts
    *   Twilio / ClockworkSMS
    *   Automated Software (GoPhish)
*   Email/Message Template
    *   To Line
    *   Subject
    *   Body
    *   Links
    *   Signature (2 types - signature block and PGP signature)
    *   Attachments
*   Landing Page (see https://data.phishtank.com/ )
    *   Web server
    *   Form Submission
    *   Describe what happens when a link is clicked. Are you presenting them with a web form to collect credentials? Are you attempting to install malware? 
    *   What tracking or other data collection do you want? Do you want to learn how many employees opened the email, clicked the link, and/or entered their passwords?
    *   What URL / Domain will you use? Is it available?
    *   Will the landing page forward them to a benign final destination page?
*   Other
    *   Think about what timing considerations for when the training emails should reach your partner.
    *   What amount of repetition or variation between training messages would be appropriate? Would you likely need to generate similar messages?

    Test your infrastructure (website, email address, etc), however phish filters may be alerted by future deployments of the same infrastructure.

    Avoid spam filters or suspicious email labeling. The goal posts are always moving - creativity is necessary.

    Create a phishing simulation plan with training objectives & consent agreement for your partner. Your phishing simulation and data collection must support your training goals. There should be various recommendations based upon an organization’s performance

### ** Deepening **

As a team, design a concept for a phishing campaign simulation to support improving your partner’s resilience against phishing.

*   Identify training objectives, data collection, and elements of the phishing attack.
*   Describe how the phishing simulation will support those training objectives. Again, the organization’s performance should have some impact on any subsequent recommendations.

Share each concept with the class. Discuss which principles of persuasion are used for each simulation.

### ** Synthesis **

Reiterate the importance of a phishing simulation plan and agreement with your partner before conducting any phishing simulation.

