### ** Summary **

Module 4, Digital Surveillance of Politically Vulnerable Organizations: The Threat Landscape, immerses students in most salient threats to vulnerable civil society organizations and their use of both encrypted and unencrypted systems. This module explores common surveillance threats such as intercepting communication, deanonymizing targets, accessing targets’ online accounts, malware, and zero day exploits. Credit to Bill Marczak for developing the majority of this module and our specific implementation for Citizen Clinic.

### ** Learning Objectives **

*   Be able to define and identify common threats
*   Compare surveillance threats across encrypted and unencrypted systems
*   Understand the fiscal incentives involved in the likelihood of attacks

### ** Pre-Readings **

See readings for [Digital Surveillance of Politically Vulnerable Organizations: The Threat Landscape](../../../Consolidated_Bibliography/#threats)


### ** Activity **

Using a recent breach or cyberattack in recent news or current events, have students discuss how they believe the attack happened, how the attack might have been worse, and what other techniques the adversary could have tried. 

*   The goal of this activity is to start building the foundations of applying theory from the literature to current scenarios in advance of breaking down individual steps in the attack.
*   Students should begin highlighting where and when the attack could have been prevented, according to the scenarios that they suggest (it’s ok if they do not have the facts on how the event actually happened). Introduce concepts such as ‘cyber kill chain’ if you feel it is appropriate. 


### ** Discussion **

1. Are we concerned about a similar situation happening to us? Why or why not?
2. What activities, tools, or other measures do we individually take that could prevent a similar situation from happening to us? What about the measures we take as a Clinic?
3. Which of those things should be done regardless of the likelihood of the same attack happening to us? Which things might be burdensome for us to keep doing?


### ** Input **

*   (_Reference to the Le Blond reading_) Define “targeted attacks” and “APTs” or “advanced persistent threats.”
*   Reminder of ethical use of the discussed information
*   Risks of unencrypted communications
    *   Phone calls and SMS are really bad for confidentiality!
    *   Weaknesses in SS7 protocol: See Circles and Hacking Team [https://www.adaptivemobile.com/blog/can-they-hear-you-now-hacking-team-ss7](https://www.adaptivemobile.com/blog/can-they-hear-you-now-hacking-team-ss7) 
    *   Telecommunication provider cooperation with governments: See case of Nokia Siemens
    *   Also, call detail records, tower dumps, and cell site simulators
*   Risks of Encrypted communications
    *   Deanonymizing targets
        *   Identifying IP address via IP loggers sites, server logs, and tracking images 
        *   Governments take IP address to ISP via court order 
    *   Accessing targets’ online accounts and communications
        *   Frontdoor: Social engineering
            *   Phishing
            *   Account Recovery Process
            *   Asking recovery code sent to their own phone
        *   Backdoor: Government requests to platforms
            *   See Transparency Reports to get an idea of which countries are more likely to get responses from platforms
    *   Malware and zero-day exploits
        *   Malicious attachments & macros: See Finfisher and Project Raven 
        *   MITM & Deep Packet Inspection to replacing (unencrypted) downloads with spyware: See PacketLogic and spyware injection in Turkey
        *   NSO Group: Pegasus and 1-click / 0-click deployment on phones

### ** Deepening **

How should we think of these threats?
    *   Wiretapping
    *   Phone tracking
    *   Targeted deanonymization
    *   Intel gathering
    *   Phishing
    *   Targeted malware
    *   Zero-day
    *   Packet injection
    *   Non-targeted surveillance
    *   Accidental ransomware download
    *   Bitcoin scam

In small groups, have students categorize those attacks into 4 to 5 groups according to... 
    *   the relative cost for adversaries to deploy them against an individual NGO.
    *   the relative frequency that adversaries deploy them against an individual NGO.

As groups share their suggested categories & rankings, discuss how fiscal incentives may or may not have a bearing on how common an attack is likely to occur. Ask and discuss how controls from the communications setup in Module 3 might help protect the Clinic from the described attacks. 


### ** Synthesis **

Given all of these threats, how can an organization raise the bar and the resources an adversary needs to dedicate against the targeted NGO?
*   Securing accounts is something we’ve discussed but now we see the need to understand these attacks, think critically, and rely upon others in an organization.
   	*   Use an alternative communication channel to contact the sender of a suspicious message
    *   Don’t click immediately or at all (eg, expand shortened URLs, go to website directly)
    *   Ask yourself: would the government actually call me if there was a problem with my taxes?
    *   See something, say something: others in an organization are likely to be targeted as well.

Social engineering is an important component of targeted attacks. Why? 

We see the need for not just technical controls, but organizations require awareness, training, policies, cohesion, and well-being in its staff. Why?

