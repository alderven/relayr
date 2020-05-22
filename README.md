## Task 1

> 1. What would you do in your first few days of work? Where would you start?

Get acquainted with the team and working place.

Talk to the manager about forthcoming milestones and future plans; ask for any urgent work to do.

Talk to the team/manager about what are they want to gain from automation, what are most crucial parts to test/automate first.

Get to know product that team is making. Test and taste product manually.

Get to know processes and tools team is using.

Prepare roadmap for automation. E.g.: first sprint: create smoke test to cover base functionality, second sprint: integrate it to CI/CD to run it automatically, third sprint: create integration test to cover simple business case, etc.

> 2. Which process would you establish around testing new functionality?

Rule of thumb: all new functionality should be tested before pushing to production. Practically that means testing all implemented features, user stories, bugs etc. before merging them to "master". Return "rejected" tickets back to developers.

Use bug tracker to handle tickets "cycle" and interact with other team members.


> 3. Which techniques or best practices in terms of code architecture and test design would you use in your automated tests?

As I understood your company has microservices architecture.
In this case I would prefer having **functional** tests for every microservice and **integration** tests to test interaction between services. Also **regression** tests with all functionality covered, but it is a lot work to do so it is in a long term plans.
Additionally it would be nice to have **monitoring** tests for getting healthcheck in production.

General rule is that all tests should be well documented. That's why I love [Yandex Allure](https://docs.qameta.io/allure/): this tools allows to have self-documented way of writing tests.

No flaky tests. No false negatives. My job as a QA is to keep tests actualized and relevant.

Integrate tests into CI/CD tool and run tests on every developers commit.

Perform tests review.

## Task 2: API test

https://github.com/alderven/ogavirt

## Task 2: UI test

https://github.com/alderven/pizzade
