### ** Summary **

This module will describe the concepts of threat modeling and bounding risk assessments. These concepts are important for practitioners since we will never have enough time to conduct as thorough a risk assessment as we would like. Having some practical bounds when analyzing risk is even more important for organizations attempting to adopt risk-informed practices and proactive security given the resource constraints commonly facing our clients. 

### ** Learning Objectives **

*   Understand how to prioritize security measures based on risk and other organizational pressures.
*   Identify the cybersecurity maturity and path of growth for an organization.
*   Develop threat models bounded by given resource constraints.

### ** Pre-Readings **

* See Course Readings for ["Threat Modeling and Bounding Risk Assessments"](../../../Consolidated_Bibliography#modeling)

### ** Resources **

* [EFF, Threat Modeling Activity Handout For Learners](https://sec.eff.org/materials/threat-modeling-activity-handout-for-learners)

### ** Activities **

Play the following newscast from CyberWire:

[https://youtu.be/MyY6hjABkk4?t=115](https://youtu.be/MyY6hjABkk4?t=115)

As small groups, discuss the targeting of Citizen Lab and then share answers to the class:

*   What are the threats?
*   What are the adversaries seeking?
*   What damage could this cause? How might this situation played out differently?

### ** Discussion **

Discuss the following questions:

*   How concerned should Citizen Clinic be about a similar approach?
*   What is the probability of this happening?
*   What is the potential impact?


### ** Input **

NIST Cybersecurity Framework allows us to define the *things an organizations should do, and where to find commonly-accepted definitions of those things*

One of the better things to come out of the Cybersecurity Framework is the implementation tier maturity model: describe what cybersecurity growth looks like -- where is an organization at now, where do they want to *get* to, and where do they want to be set up to go long-term? 

(See explainer: [https://www.cybersaint.io/blog/the-nist-cybersecurity-framework-implementation-tiers-explained](https://www.cybersaint.io/blog/the-nist-cybersecurity-framework-implementation-tiers-explained))

*   Tier 1 - Partial: Risk management is typically performed in an ad-hoc/reactive manner. Security activities are typically performed with little to no prioritization based on risk.
*   Tier 2 - Risk-Informed: Risk management practices are typically not established as organizational-wide policies but, along with the organizational objectives, the threat environment, and business requirements, directly inform the prioritization of security activities.
*   Tier 3 - Repeatable: Formally approved and regularly updated risk management practices that are expressed as policy. 
*   Tier 4 - Adaptive: Organizations adapt their security practices, including lessons learned and predictive factors, implementing a process of continuous improvement.

Our clients are almost exclusively at Tier 1. To reach Tier 2, our clients need risk-informed security activities, but what does it mean to be risk-informed?


**Threat modeling allows us to prioritize by risk and resources: Probability x Impact = Risk (see EFF’s https://ssd.eff.org/).**

1. What do I want to protect? (Assets)
2. Who do I want to protect it from? (Threats / Adversaries)
3. How bad are the consequences if I fail? (Impact)
4. How likely is it that I will need to protect it? (Probability)
5. How much trouble am I willing to go through to try to prevent potential consequences? (Mitigations)

Risk (impact and likelihood) is one pressure for prioritization but an organization must also consider urgency (availability, dependencies), requirements (legal, contractual) and incentives (funding, opportunities).

We still need to scope the bounds of risk assessments since analyzing all risk can be unwieldy for even less complex systems. Also, people (including the security practitioner) only have so much time and attention. Bounding assessments is about finding specific areas of focus: where do we need more time, attention, details?


### ** Deepening **

Share the following scenarios with students to discuss in small groups.

Part 1. You’re conducting a broad organizational security assessment for a partner. You discover a few critical pieces of information:

*   You suspect many of their devices may be out of date or running illegitimate copies of software
*   A system they are deeply dependent runs on a service that is out of the support lifecycle 
*   A member of their staff recently had the webcam on their laptop turn on and off mysteriously 

All of these things will take time to assess. Where do you start? How would you figure out what to focus on?

Part 2. Your partner wants to use Skype as the primary way to communicate. Everyone in their organization has a Skype account and it is currently the primary way they hold conference calls and send messages between staff and partners.

Discuss in assigned teams:

*   Initial reactions: Is it secure? Is it reliable?
*   What are the risks? What adversaries might present greater concerns?
*   What is the your risk *tolerance*? Why should you tolerate any risk for this partner to use their preferred communications method?

### ** Synthesis **

Review the concepts of threat modeling and risk assessment by discussing the threat model for your own Clinic program and how various activities were prioritized. Discuss resource constraints or other business requirements that were considered in implementing risk mitigations.

### ** Assignments **

Develop your initial client threat model.

1. What do they want to protect? (Assets)
2. Who do they want to protect it from? (Threats / Adversaries)
3. How bad are the consequences if they fail? (Impact)
4. How likely is it that they will need to protect it? (Probability)
5. How much trouble are they willing to go through to try to prevent potential consequences? (Mitigations)
