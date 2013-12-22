


## Github issue template


### TITLE

Express an action with your title, make it stand out.

As a developer, my goal for title is that I want to grasp in a sentence what's going to happen.

*Bad Example*: Monitoring and transparent statistics for DynamoDB (not actionable, too generic)

*Good Example*: Enable Scroll on Modal Windows

### NEED

The client problem we are trying to solve. For example:
```gherkin
As an uberVU user
I want to be able to print my reports
So that I can share social data with my team, clients and superiors
```

This is factual and might require help from Customer Services or other departments to get right (it’s a common practice, especially when defining the need for a project). It is expressed in the [Gherkin](http://docs.behat.org/guides/1.gherkin.html) language which can serve as a structured expression understood throughout the company, that is also executable by automated test runners such as [Lettuce](https://pypi.python.org/pypi/lettuce).

The need is our alignment mechanism: we are all here to solve the client’s problem and *everybody* will contribute to it. Our goal is not to write code, but to solve the problem in the most creative and pleasing way possible. Writing code that does not meet the need is considered worthless and is completely discouraged. This forces everyone to empathize with the client (a well known weakness of engineers in general) and to center the discussion around clients instead of code.
The need serves also as a high-level justification of effort stripped of technical details. Every developer seeing the issue should be able to quickly know *why we are working on this* and *why it is a good use of our time to work on that*. 
As a perk, since Gherkin is easy to understand, most of the time the purpose of the issue will be easily understood by all technical and non-technical stakeholders throughout the company.

### DELIVERABLES

This is a list of clear and concise bullet points that we chose to do in order to solve the client need. Most of the time, the bullet points imply programming / technical effort, but not always. For example, we could decide to migrate by hand some client data for which an automated script is too complicated to write. Each deliverable should be expressed as an affirmation that should hold true after the issue has been correctly solved.

*Good example*: a DynamoDB database named “author_reactions” with write throughput 70 and read throughput 20 exists (notice the present tense)

*Bad example*: create a table to store the reactions of the authors in AWS (not specific enough, cannot be easily verified)

After you think you finished the issue, remember to double-check whether all the deliverables are met.

The main purpose of the list of deliverables is to provide a checklist of important items that we think will lead to solving the client need. Forcing it to be factual and concise puts the developer writing them into the state of mind of identifying the key steps of the technical plan and presenting them in a manner that can be vetoed at any point by anyone in the team.

### PREREQUISITES

List of bullet-points that are important nuggets of information needed for someone to be able to solve this issue. It does not need to be an extensive list of all programming knowledge since the 1950s, but rather a list of key things to skim before diving into this issue. The assumption will be that your colleagues already have an overview of the important areas of the system, and you just need to remind them some details they might be overlooking. Even if you are the one who will be working on this issue as well, it will make it a whole easier for your colleagues to follow your work and stay up-to-date with what you are doing.

The philosophy behind this type of writing Github issues is that you as a developer are put into teaching mode. You are pitching your work to your colleagues, expecting them to stay up to date with it, and making yourself helpable (i.e. what if you have to go out of town for 2 days? They should be able to finish up your fork for you. Or, what if we need to finish your work faster? How will they know what you are doing and how you can be helped without you having to invest too much time to explain it by word of mouth).
This makes for a very nice way to onboard people on a new technology as well. They can start working on simpler issues and become accustomed to it by reading the correct prerequisites.

### TODO'S

**The plan**. One should never embark on any endeavor without **taking every important aspect of it into consideration beforehand**. This does not mean obtaining a complete bulletproof implementation in pseudocode. In order to properly spec an issue, you will most likely need to dig into the code and understand it. This will take some serious time at first, but once you get used to most of the subsystems and learn how to read code fast, it will get into your bloodstream. Remember that you can always use `git blame` on the relevant piece of code to ask for help from your knowledgeable colleagues in order to build a sane checklist of steps toward the solution. We don’t expect this checklist to be perfect, but rather touch on all important aspects, and demonstrate that you can ship it efficiently during the maximal allotted timeframe for an issue (2p = less than a day). If you feel the issue is larger, then you should break it up into multiple smaller ones.

Example:
* Create Mozaic channel for the social profiles endpoint
* Allow filtering by search expression in posts Tastypie resource

This is especially useful for less experienced developers. The more experienced ones should be able to generate their own checklist starting from the need and deliverables.

### SCREENSHOTS

Including a single screenshot with everything for that feature works really well to better understand the project.

### NOTES

Personal insights from previous experience can be real time-savers. Take a note of peculiar aspects relevant to the implementation of this issue. Here is a good occasion to give some pieces of historical information like approaches we previously tried and failed. We also use it in order to give some sense of the broader vision. For example: we are implementing so many tests for this part of the code, because it used to break very often, and we are now going towards 80% code coverage on this particular section of the codebase.
