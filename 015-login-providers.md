# Title <!-- What do you want to call your `awesome_feature`? -->

- Implementation Owner: (your github @username)
- Start Date: (today's date, dd-mm-yyyy)
- Target Date: (expected date of completion, dd-mm-yyyy)
- Appwrite Issue:
  [Is this RFC inspired by an issue in appwrite](https://github.com/appwrite/appwrite/issues/)

## Summary

[summary]: #summary

<!-- Brief explanation of the proposed contribution. Write your answer below. -->

This RFC will plan on how to adapt our current authentication and make it more extendable and configurable, by allowing the developers to configure all authentication methods and having a base for Appwrite contributors to add new authentication methods.

## Problem Statement (Step 1)

[problem-statement]: #problem-statement

**What problem are you trying to solve?**

<!-- Write your answer below. -->

Developers can't configure if E-Mail registration and authentication in their projects at all. Meaning they can't disable or enable it easily.

**What is the context or background in which this problem exists?**

<!-- Write your answer below. -->

For private or internal applications that only allow creating user account by hand in the console.

**Once the proposal is implemented, how will the system change?**

<!-- Write your answer below. -->

Users will be able to configure authentication methods like E-Mail, Anonymous Login and any other upcoming provider the same we, for what we offer with OAth2 providers now.

## Design proposal (Step 2)

[design-proposal]: #design-proposal

<!--
This is the technical portion of the RFC. Explain the design in sufficient detail keeping in mind the following:

- Its interaction with other parts of the system is clear
- It is reasonably clear how the contribution would be implemented
- Dependencies on libraries, tools, projects or work that isn't yet complete
- New API routes that need to be created or modifications to the existing routes (if needed)
- Any breaking changes and ways in which we can ensure backward compatibility.
- Use Cases
- Goals
- Deliverables
- Changes to documentation
- Ways to scale the solution

Ensure that you include examples, code-snippets etc. to allow the community to understand the proposed solution. **It would be best if the examples use naming conventions that you intend to use during the actual implementation so that changes can be suggested early on during the development.**

Write your answer below.

-->

We would adapt how OAuth2 providers are build right now and adapt them to other common login methods. Meaning, that we would build a class to extend which can be used to create any kind of authentication. These are gonna be registered within in our codebase, user can enable/disable and if needed configure them.

Right now, E-Mail Authentication is heavily integrated into Appwrite - which would make decoupling them a big undertaking. Instead we give the user the option to disable and enable it for now and build this system around different methods like SMS or OTP.

### Prior art

[prior-art]: #prior-art

<!--

Discuss prior art, both the good and the bad, in relation to this proposal. A
few examples of what this can include are:

- Does this functionality exist in other software and what experience has their
  community had?
- For other teams: What lessons can we learn from what other communities have
  done here?
- Papers: Are there any published papers or great posts that discuss this? If
  you have some relevant papers to refer to, this can serve as a more detailed
  theoretical background.

This section is intended to encourage you as an author to think about the
lessons from other software, provide readers of your RFC with a fuller picture.
If there is no prior art, that is fine - your ideas are interesting to us
whether they are brand new or if it is an adaptation from other software.

Write your answer below.
-->

### Unresolved questions

[unresolved-questions]: #unresolved-questions

<!-- What parts of the design do you expect to resolve through the RFC process before this gets merged? -->

<!-- Write your answer below. -->

### Future possibilities

[future-possibilities]: #future-possibilities

<!-- This is also a good place to "dump ideas", if they are out of scope for the RFC you are writing but otherwise related. -->

<!-- Write your answer below. -->