# Task 1

### 1. What would you do in your first few days of work? Where would you start?

* Get acquainted with the team and working place.

* Talk to the manager about forthcoming milestones and future plans; ask for any urgent work to do.

* Talk to the team/manager about what are they want to gain from automation, what are most crucial parts to test/automate first.

* Get to know product that team is making. Test and taste product manually.

* Get to know processes and tools team is using.

* Prepare roadmap for automation. E.g.:

   1. first sprint: create smoke test to cover base functionality

   1. second sprint: integrate it to CI/CD to run it automatically

   1. third sprint: create integration test to cover simple business case, etc.

### 2. Which process would you establish around testing new functionality?

Rule of thumb: all new functionality should be tested before pushing to production. Practically that means testing all implemented features, user stories, bugs etc. before merging them into "master". If something is wrong return tickets back to developers.

Use bug tracker to handle tickets "cycle" between team members.

Perform test reviews (for both automation and manual tests).

As I understood your company has microservices architecture.
In this case I would prefer having **functional** tests for every microservice and **integration** tests to test interaction between services. Also, it is important to have **regression** tests with all functionality covered, but it is a lot work to do so it is a long term plans.
Additionally, it would be nice to have **monitoring** tests for getting healthcheck in production. 

No flaky tests. No false negatives. Keep tests actualized and relevant.

### 3. Which techniques or best practices in terms of code architecture and test design would you use in your automated tests?

* Use test framework to organize and run tests, e.g. [pytest](https://docs.pytest.org/en/latest/).

* Use tearup/teardown (in terms of pytest it is called [fixtures](https://docs.pytest.org/en/latest/fixture.html)) for test data preparation/deletion and for reusing components in other tests.

* Use [parametrization](https://docs.pytest.org/en/latest/parametrize.html) in order to avoid duplication of code.

* Create test independend from each other.

* Use steps-expected result structure in test.

* Use reporting tool, e.g. [Yandex Allure](https://docs.qameta.io/allure/) for convenient results representation.

* Use [Page Object](https://selenium-python.readthedocs.io/page-objects.html) pattern for UI automation.

# Task 2: API test

https://github.com/alderven/ogavirt

# Task 2: UI test

https://github.com/alderven/pizzade
