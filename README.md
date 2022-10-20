# Overview
First I would like to investigate current situation of the projects and teams, through questions. The answers of those will give some insight into what to do next.

## Questions
* What is the % coverage of unit tests for each of those mentioned projects?
* How the current SDLC process look like from the idea to production release?
* What is the definition of done for the user story?
* Are we able to estimate what % of the functionalitires the manual test cases are covering? 
* How often is the manual regression performed?
* How long it takes to run full manual regression?
* Are manual test cases assessed/marked by priority and severity?
* What is the % coverage of the e2e automation?
* What is the compile and build time/How long devs need to wait for new build?
* What level/quality and how many bugs goes to production?

## Improvements/QA process
0. Put some(or analyze) metrics in place:
    - agile ones like lead time, cycle time or velocity of the team
    - code coverage by unit tests
    - Mean Time to Detect by the right people or systems
    - Mean Time to Repair is the average time it takes to repair a system
    - etc..
1. Story/Ideas/Features reviews - clear and defined checklist of things that should be done/included within ticket/story before it goes to team board backlog e.g.:
    - title which sums up the intent
    - clear description of the features and desiried behaviour of the software, cannot be to generic and opened for wide interpretation
    - defined and listed Acceptance Criteria
    - if need it listed tech tasks that are need it to complete the story
    - assumed unit tests coverage (e.g. 80-90%)
2. Unit tests should be always written for stories
3. All unit tests and integration tests should be run at least once during nightly build process.
4. On every commit to repo(or every period of time e.g. 30min, 1h etc) there should be CI/CD process to compile the source and deploy to test envrionment and run unit tests and subset of integraton tests e.g. happy/main paths. To speed up the feedback about source code quality.
5. Integration tests should be also always written for the user stories with some assumed coverage of at least e.g. 70%
6. % coverage of the e2e automation should be raised also at the beginnig without QA Automation Engineers each newly developed user story should had at least happy path scenario automated for the developed feature/change
7. Consider if we should also put to Acceptance Criteria task to add documentation or wider/more detailed description for potential users. With documentation it depends what would be the gain to have it and maintain it versus the effort and cost.
8. If possible speed up the CI/CD pipelines so the new builds can be delivered faster, less waiting means faster feedback about the build quality.
9. Analyze current bottlenecks within the teams, when and where the stories had tendency to stuck/pile up within the board/process.

And probably many more ideas.. but all depends what is the current situation and what actions should be taken.
