---
title: Reflection
date: 2026-06-09
author: Guanwei Chen
summary: Short description
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

### Open the app locally through npm start and access localhost:3000

* Result: Passed
* Evidence / observation:
  The app could be opened through the local server after installing dependencies.
* Used in reflection:
  Used to discuss local performance and setup complexity.

### Log in with the demo account

* Result: Passed
* Evidence / observation:
  The login page accepted the demo username and password and then displayed the main app shell.
* Used in reflection:
  Used to discuss prototype-level login and user flow.

### Navigate between Home, Log Dive, Explore Sites, Dive Shops, and Profile

* Result: Passed
* Evidence / observation:
  Navigation switched sections without full page reload.
* Used in reflection:
  Used to evaluate responsiveness and app-like behaviour.

### Create a new dive log

* Result: Passed
* Evidence / observation:
  The form accepted location, conditions, marine life, notes, and image link/default image. After saving, the log list updated.
* Used in reflection:
  Used to evaluate functional completion and backend/API behaviour.

### Use the live preview while filling in the form

* Result: Passed
* Evidence / observation:
  The preview changed when fields, checkboxes, notes, or image values changed.
* Used in reflection:
  Used to evaluate immediate feedback and user experience.

### Search and filter dive sites

* Result: Passed
* Evidence / observation:
  Keyword, state, site type, and difficulty filters changed the displayed cards.
* Used in reflection:
  Used to evaluate client-side filtering and browsing usability.

### Edit profile information

* Result: Passed
* Evidence / observation:
  Profile fields could be changed and the profile display updated after saving.
* Used in reflection:
  Used to evaluate profile functionality.

---

## Appendix B: User Walkthrough with a Participant Familiar with Recreational Diving

A short walkthrough was conducted with one participant familiar with recreational diving. The participant was asked to complete three core tasks without step-by-step instruction.

### Log in using the demo account

* Result: Completed
* Observation:
  The participant understood the demo login because the account details were visible on the login page.

### Record and save a new dive log

* Result: Completed
* Observation:
  The participant understood the purpose of the fields, especially current, visibility, temperature, and marine life. However, the form looked long at first.

### Search for a dive site and view related information

* Result: Completed
* Observation:
  The participant found the card layout easy to scan and understood the filter options after trying them.

### View a diver profile from a card

* Result: Completed with minor hesitation
* Observation:
  The participant did not immediately realise that the author name was clickable.

### Short feedback notes

> "The live preview makes it easier to understand what I am creating."

> "The information is useful for divers, but the logging form looks a little long when I first open it."

> "The site cards are clear because I can see location, type, conditions, and marine life quickly."

---

## Appendix C: Accessibility Checklist

### Visible form labels

* Result: Mostly passed
* Evidence from prototype:
  Login, dive log, and profile inputs have visible labels.
* Improvement needed:
  Check every field after future layout changes.

### Colour contrast

* Result: Mostly passed
* Evidence from prototype:
  Dark navy text on light backgrounds and white text on dark blue areas are generally readable.
* Improvement needed:
  Run a formal contrast checker for all buttons and labels.

### Responsive layout

* Result: Passed
* Evidence from prototype:
  CSS media queries allow layouts to collapse into a single column on smaller screens.
* Improvement needed:
  Test on additional real devices instead of browser resizing only.

### Keyboard navigation

* Result: Partially passed
* Evidence from prototype:
  Standard buttons and form controls can be accessed by keyboard.
* Improvement needed:
  Provide stronger visible focus indicators.

### Modal accessibility

* Result: Needs improvement
* Evidence from prototype:
  The profile modal includes ARIA attributes but does not fully trap focus or support Escape to close.
* Improvement needed:
  Add focus management and Escape key support.

### Error feedback

* Result: Partially passed
* Evidence from prototype:
  Login and form validation errors appear as text.
* Improvement needed:
  Improve clarity and support for screen readers.

---

## Appendix D: Lighthouse Audit Results

### Performance

* Score: Not reliably available
* Main issue:
  The local environment could not consistently generate a performance score.
* Used in reflection:
  Manual technical walkthroughs were used instead.

### Accessibility

* Score: 80 / 100
* Main issue:
  The application provides a reasonable accessibility foundation but still requires improvements.

### Best Practices

* Score: 0 / 100
* Main issue:
  The prototype was tested locally over HTTP rather than HTTPS.

### SEO

* Score: 0 / 100
* Main issue:
  Metadata such as meta descriptions was not implemented.

*(Insert Lighthouse screenshot here if needed.)*

---

## Appendix E: Rescoped Functional Requirements

### User login

* Final implementation:
  Demo login
* Reflection:
  Suitable for demonstrating workflow but not for production authentication.

### Record dive sites and environmental conditions

* Final implementation:
  Implemented
* Reflection:
  Core functionality supported through structured data storage.

### Search community dive information

* Final implementation:
  Implemented
* Reflection:
  Filtering and browsing features support information sharing.

### Browse local dive shops

* Final implementation:
  Implemented
* Reflection:
  Provides practical local references.

### User profiles and contact information

* Final implementation:
  Simplified
* Reflection:
  Supports identity and community presence without a full social network.

### Image upload

* Final implementation:
  Rescoped
* Reflection:
  Image links and default images replaced direct uploads because of implementation complexity.

### Real-time messaging or buddy system

* Final implementation:
  Rescoped
* Reflection:
  Contact information was retained, while a full messaging system was considered beyond the project scope.

---

End of Appendix

