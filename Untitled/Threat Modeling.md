This page documents the process driven by the security team when working on Threat Modeling campaigns. Outlining the steps, processes, and overall workflow of the service, it can be taken as a step-by-step guide. It is important to note that not all campaigns are driven equally, requirements may vary and adaptations may be required. Our processes are not set in stone, and updates may be required as our services evolve. 

---

## **Introduction**

A Threat Modeling is a type of security assessment we provide to customers in a few different formats. Perhaps the most flexible service we have, and the most comprehensive, as it must adapt to the context where it is applied. Still, as with any security assessment, a Threat Modeling is never definitive.

The effort invested in a Threat Modeling varies based on its purpose. There are thee situations where we typically do Threat Modeling:

- A full Threat Modeling of an application, as a standalone delivery, requested by a customer.
- Threat Modeling a single feature either in the design or implementation phase.
- Threat Modeling an application as support for a Penetration Test.

All instances follow the same principles and structure, but the depth to which we may go and the deliverables format may differ. Our Threat Modeling engagements follows the procedure described in the [Threat Modeling Manifesto](https://www.threatmodelingmanifesto.org/). Following the four-questions framework:

1. What are we working on?
2. What can go wrong?  
3. What are we going to do about it?
4. Did we do a good enough job?

We start by **understanding the application**. What problem is it solving? What is its audience? What type of data it handles? Who may be interested in breaking it? These are all common questions to get things started, we go deeper and start asking more specific things as the process advances. It usually helps if the customer shares his screen, showing the application's features from a user perspective.

Data Flow Diagrams (DFDs) are a great tool to help us visualize the interactions and critical areas of the application, ideally we should draw a DFD interactively, with the customer, using any drawing tool of preference (draw.io, excalidraw, miro). Not only does this help visualize the problem, the trust boundaries and the components of the application, it also help us come up with more questions for our model. This visualization enables using frameworks like STRIDE on each trust boundary and process, ensuring a more thorough analysis.

By the end of each session, we should always review our notes as soon as possible, checking if we missed any questions and documenting with as much detail as possible all the Threats identified so far. Threat modeling sessions should also be recorded so we can reference back to them in the future.

### **Process Overview**

![](https://docs.defensepoint.com/uploads/images/drawio/2025-01/YFdUBhctYVLKIKMu-drawing-14-1736506662.png)

The Threat Modeling process is simple, we kick things off with a scoping meeting, where we'll review the application at a high level and estimate how much time should we invest in each component. At this first step we're trying to understand which problem the application solves, what are the main features and components, what are the types of users and how they interact with it. In this scoping session, we should try to cover everything, we'll dive into details in follow-up meetings, so we don't need to worry about asking too many questions at first, the only goal is understanding the limits of our engagement and deciding how we'll analyze each component. If the engagement is fully online, we should try to avoid meetings that are longer than 2 hours, fatigue hits much faster online, so it is better to have multiple "short" Threat Modeling sessions than only a few long sessions with not so much productivity.

After scoping, we plan, schedule and host the follow-up Threat Modeling sessions, the amount of follow-ups required varies a lot, depending on the size of the application and the scope defined in the beginning. All sessions must be recorded, attendees should take notes and ask any questions that may come up. We should always have at least 2 team members from DefensePoint on a session, one would be driving the meeting while the other will be taking notes, as it may be difficult to take notes and host the session at the same time. 

Note-taking is a bit o a personal experience, all attendees should take notes during the Threat Modeling sessions, we should record implementation details like which hashing and encryption algorithms are being used, platform details like what operating system runs the application, is it cloud-based? Is it a serverless microservice? Are the database keys exposed? Are they incremental integers? Does the application have different access levels? how is that maintained? Basically, any detail that can impact the security posture of the product is of interest. We have a [Threat Modeling Checklist] to guide us, but we should always expand on those questions, go into as much detail as our time and scope allows for.

An important thing to keep in mind when attending Threat Modeling sessions is **that there are no stupid questions**. Any question about the application, business logic, infrastructure, audience, application data, _et cetera_, is relevant. Regardless of how basic it may sound, it can always lead to more complex questions or bring a different perspective to the problem, improving the overall understanding of the application. It also adds to the flow of a session. The more people interact, the more dynamic a Threat Modeling session is, and the results tend to be much better. When attending a session, always try to interact, it adds to the flow and makes it feel less like an interrogatory.

After each Threat Modeling session, each attendee should take some time to process their notes, upgrade them from rough field notes to actual findings or reference documentation, this needs to be done as early as possible, as unprocessed notes run stale pretty fast. If there are still more sessions to be hosted, it is crucial to process your notes before the next session. The output of processing notes should be Threat Modeling Findings, a processed documentation with impact analysis, attack scenarios and recommended actions.

Once we've gone through all planned Threat Modeling sessions, we can start writing a report. The format can vary a lot, some customers prefer actual documents, while others prefer that we add our findings as tickets in Jira or pages in their internal library. Regardless of the format, we should include the following parameters when writing up our findings:

- Affected asset
- Threat Category
- Threat Title
- Threat Scenario
- Impact, considering affected users and reputational and financial  damage
- Likelihood of exploitation, considering reproducibility, exploitability and discoverability of the issue
- Risk Level
- Recommended Actions

An example of a Threat Modeling document we've delivered can be found in [this spreadhseet]. This was performed on the Payslip application in 2024, after about 8 sessions with their development team. The items in this spreadsheet ended up being reported as Jira tickets in their board, but the tickets contain the same information found in the document.

 

[](https://docs.defensepoint.com/books/security-processes-documentation/page/threat-modeling/edit?content-id=bkmrk-upon-delivering-the-&content-text=Upon%20delivering%20the%20report%2C%20we%20should%20expect%20some%20 "Jump to section in editor")

Upon delivering the report, we should expect some customer feedback. There's usually some discussion about the Threats we've reported with the customer, and some adjustments from our side may be required. After validating our findings, we can add any changes to the report and deliver an Executive Summary, outlining our approach and the results found.