---
title: Reflection
date: 2026-06-09
author: Guanwei Chen
summary: This reflection analyzes and reflects on the test results, user feedback, and accessibility assessment of the Easy Dive website. It also reviews the changes in feature trade-offs and design thinking during development, and recounts my own reflections and growth during this project.
tags:
  - reflection

---
Looking back on the entire EASY DIVE project, I believe the biggest takeaway wasn't completing a working website, but rather a renewed understanding of what constitutes a good web application.

In the early stages of the project, I envisioned EASY DIVE as a comprehensive diving community platform. I envisioned users not only browsing dive sites and recording dive information, but also finding dive buddies, communicating online, viewing dive shop information, and managing their personal dive profiles. Through early development logs, I continuously refined these ideas and attempted to integrate different functions into a unified platform, hoping to build a diving community that both shares information and fosters social interaction.

However, as development progressed, I gradually realized that many of my initial ideas, while appealing, weren't necessarily suitable for the current project's scale, nor would they necessarily create the best user experience. Development, testing, and user feedback constantly challenged my initial assumptions, making me realize that a successful prototype isn't about having the most features, but rather the most complete and clearly defined user flow.

Reflecting on the initial functional requirements, I initially believed that dive buddy matching and online social networking should be crucial components of a diving community. However, as the website gradually came to fruition, I began to realize that more features meant greater system complexity, and a complex system didn't necessarily translate to a better user experience. In contrast, the core workflow centered around Dive Log, Explore Sites, Dive Shops, and Profile was more complete and better aligned with the project's goals. Users could record their diving experiences, browse dive site information shared in the community, find local dive shops, and manage their personal profiles; these functions had natural data connections and usage sequences. Therefore, during development, some initially envisioned complex social features were simplified or removed, with the focus shifting to building a stable and easy-to-understand information-sharing platform. As seen in Appendix E, some functional requirements were re-planned during development. This adjustment wasn't a design failure, but rather development and testing helped me reassess which requirements were truly valuable.

From the final website's performance, the entire system stably supported the core tasks. According to the test results in Appendix A, users could smoothly complete major operations such as logging in, creating dive logs, browsing dive sites, viewing dive shop information, and editing their profiles, without any obvious functional errors throughout the process. Switching between pages is smooth, allowing users to complete multiple tasks consecutively without being interrupted by frequent page refreshes. The Dive Log page not only supports recording location, environmental conditions, marine life, and personal notes, but also offers a real-time preview function, allowing users to see the approximate effect of the final record before saving. I believe this instant feedback reduces user uncertainty and improves the understandability of the entire recording process.

The Explore Sites page also achieves its initial design goals well. Users can browse dive sites shared by the community and quickly find the information they need through the filtering function. Compared to a simple information list, the card layout helps users obtain key information such as location, environmental conditions, and marine life simultaneously, enabling the platform not only to record experiences but also to support information gathering and comparison before diving activities.

While the website operates stably overall, the Lighthouse test results also remind me that a website that functions normally is not necessarily ready to become a truly public-facing web application. As shown in Appendix D, the current prototype has a certain level of accessibility, but the Accessibility score still has room for improvement. Best Practices and SEO also reflect a gap between the current prototype and a real-world deployment system. These results made me realize that web development needs to focus not only on whether functionality is implemented, but also on broader issues such as long-term maintenance, accessibility, and deployment environment.

Beyond technical performance, user testing helped me rethink the entire website design. According to Appendix B, participating users were able to successfully complete key tasks such as logging in, creating dive logs, and searching for dive sites. The real-time preview function received positive feedback; participants felt it helped them understand the content they were creating and reduced uncertainty before submission. Meanwhile, the clear information display on the Explore Sites page allowed users to quickly browse information on different dive sites.

However, the testing also revealed some issues that warrant further optimization. Participants felt the Log Dive page required a lot of information and was somewhat complex for first-time users. This issue actually reflected a contradiction I had during the design phase. In the initial development logs, I wanted the platform to record as much diving information as possible, so I designed numerous data fields to help divers preserve valuable environmental data and experience. However, actual testing made me realize that a balance needs to be struck between detailed recording and simple operation. If the system requires users to input too much information at once, it can negatively impact the overall experience. Therefore, if I continue to improve this project, I will consider breaking the entire recording process into multiple stages, allowing users to complete the input gradually, rather than facing a complete form all at once.

The results in Appendix C also helped me further understand the importance of accessibility. While the website already has clear form labels, reasonable color contrast, and a responsive layout, there is still room for improvement in keyboard navigation and pop-up focus management. This made me realize that accessibility is not only a visual design issue but also a crucial component of interaction design. Only when different user groups can successfully complete tasks can a website truly be considered easy to use.

The entire development and testing process also made me rethink the future direction. I believe that the most important next step is not to continuously add new features, but to continue optimizing the existing system based on the problems identified. For example, redesigning the dive recording process, improving keyboard navigation, and refining error feedback are all more reasonable than directly adding complex social features. The development process gradually made me realize that a focused and complete system is often more valuable than a feature-rich but incoherent system.

Looking back on the entire project, my biggest takeaway wasn't learning how to build a website, but rather understanding that design concepts are constantly revised and improved through development, testing, and user feedback. Initially, I thought a good diving community platform should have as many features as possible. However, by the end of the project, I'm more inclined to believe that a successful web application isn't about having the most features, but about finding the most reasonable balance between technical limitations, project scope, and user needs, and building a complete and clear user experience around the core mission.

---
# Appendix: Evaluation Evidence
## Appendix A: Manual Technical Task Walkthrough
Open the app locally through `npm start` and access `localhost:3000`
* Result: Passed
* The app could be opened through the local server after installing dependencies.
* Used to discuss local performance and setup complexity.

Log in with the demo account
* Result: Passed
* The login page accepted the demo username and password and then displayed the main app shell.
* Used to discuss prototype-level login and user flow.

Navigate between Home, Log Dive, Explore Sites, Dive Shops, and Profile
* Result: Passed
* Navigation switched sections without full page reload.
* Used to evaluate responsiveness and app-like behaviour.

Create a new dive log
* Result: Passed
* The form accepted location, conditions, marine life, notes, and image links/default images.
* After saving, the log list updated.
* Used to evaluate functional completion and backend behaviour.

Use the live preview while filling in the form
* Result: Passed
* The preview changed when fields, checkboxes, notes, or image values changed.
* Used to evaluate immediate feedback and user experience.

Search and filter dive sites
* Result: Passed
* Keyword, state, site type, and difficulty filters changed the displayed cards.
* Used to evaluate browsing and filtering usability.

Edit profile information
* Result: Passed
* Profile fields could be changed and the profile display updated after saving.
* Used to evaluate profile functionality.
---
## Appendix B: User Walkthrough
A short walkthrough was conducted with one participant familiar with recreational diving. The participant was asked to complete several core tasks without detailed instructions.

Log in using the demo account
* Completed
* The participant understood the demo login because the account details were visible.

Record and save a new dive log
* Completed
* The participant understood the purpose of the fields, especially current, visibility, temperature, and marine life.
* However, the form looked a little long at first.

Search for a dive site and view related information
* Completed
* The participant found the card layout easy to scan and understood the filters after trying them.

View a diver profile from a card
* Completed with minor hesitation
* The participant did not immediately realise that the author name was clickable.

Participant comments:
> "The live preview makes it easier to understand what I am creating."
> "The information is useful for divers, but the logging form looks a little long when I first open it."
> "The site cards are clear because I can see location, type, conditions, and marine life quickly."
---
## Appendix C: Accessibility Checklist

Visible form labels
* Mostly passed
* Login, dive log, and profile inputs have visible labels.
* Future improvement: check all fields after future layout changes.

Colour contrast
* Mostly passed
* Dark text on light backgrounds and white text on dark backgrounds are generally readable.
* Future improvement: run a formal contrast checker.

Responsive layout
* Passed
* CSS media queries allow the layout to adapt to smaller screens.
* Future improvement: test on more real devices.

Keyboard navigation
* Partially passed
* Standard buttons and form controls can be accessed by keyboard.
* Future improvement: improve focus indicators.

Modal accessibility
* Needs improvement
* The profile modal includes ARIA attributes but does not fully trap keyboard focus or support Escape to close.
* Future improvement: add focus management and Escape key support.

Error feedback
* Partially passed
* Login and form validation errors appear as text.
* Future improvement: improve clarity and screen reader support.
---
## Appendix D: Lighthouse Audit

Performance
* A stable performance score could not be generated in the local testing environment.
* Manual task walkthroughs were used instead.

Accessibility
* Score: 80 / 100

Best Practices
* Score: 0 / 100
* Local testing was conducted over HTTP rather than HTTPS.

SEO
* Score: 0 / 100
* Metadata such as meta descriptions was not implemented.
---
## Appendix E: Functional Requirement Changes
User login
* Implemented as a demo login.
* Suitable for demonstrating the user workflow.

Record dive sites and environmental conditions
* Implemented.
* Core functionality supported through structured data storage.

Search community dive information
* Implemented.
* Filtering and browsing features support information sharing.

Browse local dive shops
* Implemented.
* Provides practical local references.

User profiles and contact information
* Simplified.
* Supports identity and community presence.

Image upload
* Rescoped.
* Image links and default images replaced direct uploads because of implementation complexity.

Real-time messaging and buddy system
* Rescoped.
* Contact information was retained, while a full messaging system was considered beyond the project scope.
---
