# Learning Practice 7: Test Planning

## Project: North Vacation Booking Application

### 1. Test Context

#### Test Objectives
1. Verify that users can select a rental, enter valid check-in and checkout dates and a guest count, and successfully create a booking.
2. Verify that users can view their bookings and that the application handles invalid inputs and booking actions appropriately.

#### In Scope
- Viewing available rentals.
- Selecting a rental.
- Entering check-in and checkout dates.
- Entering the number of guests.
- Creating a booking.
- Viewing the booking list.
- Checking input validation and error handling.
- Checking applicable increase, decrease, and reset controls.

#### Out of Scope
- Real payment processing.
- External travel-provider integrations.
- Production performance testing at large scale.
- Security penetration testing.
- Features not described in the provided requirements.

#### Test Basis
- North Vacation Booking application requirements provided in Learning Practice 7.
- Application user interface and available behavior.
- Relevant source code, where available.

#### Assumptions and Constraints
- The application and its test environment will be available during the planned test period.
- Rental data and sample booking data will be available.
- Testing will be completed within five working days.
- The exact expected behavior for requirements that are unclear must be confirmed with the product owner.

### 2. Roles and Responsibilities

| Role | Responsibilities | When Involved | Communication |
|---|---|---|---|
| Tester / QA | Review requirements, design test cases, execute tests, record results, and report defects. | Throughout planning and testing. | Shares test results and defects with developers and the product owner. |
| Developer | Prepare testable code, investigate defects, fix issues, and support regression testing. | Before testing and whenever defects are found. | Discusses defects and fixes with the tester. |
| Product Owner | Clarify requirements, confirm expected behavior, prioritize features, and review release readiness. | During planning and when requirements or defects need clarification. | Communicates priorities and acceptance expectations to the tester and developer. |

### 3. Test Approach

| Test Area | Test Level or Type | Technique | Manual or Automated | Deliverable |
|---|---|---|---|---|
| Booking form | Component testing | Equivalence partitioning and boundary value analysis | Manual and automated where supported | Booking form test cases and results |
| Date validation | Functional testing | Valid and invalid input testing | Manual | Date validation results |
| Guest count | Functional testing | Boundary value analysis, including minimum and invalid values | Manual and automated where supported | Guest-count test results |
| Create booking | Integration testing | End-to-end workflow testing | Manual | Booking creation test results |
| Booking list | System testing | Positive and negative testing | Manual | Booking list test results |
| Existing booking behavior | Regression testing | Re-run previously passed tests after changes | Manual and automated where supported | Regression test results |

#### Test Levels
- Component testing of individual controls or components.
- Integration testing of the booking form and booking data flow.
- System testing of complete booking workflows.
- Acceptance testing against the user's booking goals.

#### Test Types
- Functional testing.
- Validation and negative testing.
- Regression testing.
- Usability checks.

#### Test Deliverables
- Test plan.
- Test cases and checklist.
- Test execution results.
- Defect reports.
- Automated test files, where supported.
- Test completion summary.

### 4. Test Requirements

#### Environment
- A computer with the North Vacation Booking application installed or accessible.
- A test instance of the application and any required backend or mock data service.
- A stable local or test network connection.

#### Browsers and Devices
- Google Chrome on a desktop computer.
- Safari or another supported browser for compatibility checks, if available.
- Responsive layout checks at desktop and mobile-sized viewport widths.

#### Tools
- Browser developer tools.
- A text editor or Visual Studio Code.
- Git and GitHub.
- Jest and React Testing Library if the application supports automated component tests.
- A spreadsheet or Markdown file for recording test cases and results.

#### Test Data
- At least three available rental listings.
- A valid check-in date and checkout date.
- A checkout date earlier than check-in to test invalid date handling.
- A missing rental selection.
- A valid guest count and invalid values such as zero or a negative number.
- Sample existing bookings and a new booking.

#### Access and People
- Access to the application and its test data service.
- Permission to view source code and submit changes to the designated test repository.
- Developer assistance if the environment fails or a defect needs investigation.
- Product owner availability to clarify ambiguous requirements.

### 5. Risk Register

| Risk | Type | Likelihood | Impact | Mitigation |
|---|---|---|---|---|
| The application accepts invalid dates or guest counts. | Product risk | Medium | High | Prioritize validation and boundary tests for dates and guest counts. |
| The rental data service is unavailable, preventing booking tests. | Project risk | Medium | High | Verify the service before testing and prepare known test data or an approved fallback. |
| Requirements do not define all expected validation behavior. | Project risk | Medium | Medium | Record assumptions and ask the product owner for clarification before final acceptance. |
| A code change breaks previously working booking behavior. | Product risk | Medium | High | Re-run the regression suite after fixes. |
| Testing is delayed by environment or dependency setup problems. | Project risk | Medium | Medium | Install and verify tools before execution and reserve time for troubleshooting. |

### 6. Entry Criteria

Testing may begin when all of the following are met:

1. The application starts successfully in the agreed test environment.
2. The rental data service is available, or an approved test-data alternative is ready.
3. The requirements and expected behavior for high-priority booking workflows have been reviewed.
4. Test cases for creating and viewing bookings have been prepared and reviewed.
5. Required tools and test data are available.

### 7. Exit Criteria

Testing is complete when all of the following measurable conditions are met:

1. At least 95% of planned test cases have been executed, and every unexecuted test is documented with a reason.
2. All high-priority test cases for selecting rentals, entering booking details, creating bookings, and viewing bookings have been executed.
3. No unresolved critical or high-severity defects remain. Any accepted exceptions must be documented and approved by the product owner.
4. All failed tests have a recorded result and an associated defect or documented explanation.
5. Regression testing has been completed for the affected booking workflows after fixes.
6. A test completion summary has been prepared and shared with the team.

### 8. Test Schedule

The following schedule assumes a five-working-day test period.

| Activity | Responsible Role | Time | Dependency |
|---|---|---|---|
| Review requirements and confirm scope | Tester and Product Owner | Day 1 | Requirements are available |
| Prepare test environment and data | Developer and Tester | Day 1 | Environment access is available |
| Design and review test cases | Tester, with Product Owner input | Day 2 | Requirements have been reviewed |
| Execute booking form and validation tests | Tester | Day 3 | Environment, data, and test cases are ready |
| Execute booking creation and booking list tests | Tester | Day 4 | Core form tests have started and required services are available |
| Report defects and retest fixes | Tester and Developer | Day 4–5 | Defects have been recorded and fixes are available |
| Perform regression testing and summarize results | Tester | Day 5 | Relevant fixes have been retested |
| Review release readiness | Product Owner, Developer, and Tester | Day 5 | Exit criteria and test results are available |

### 9. Communication Plan

| Information | Audience | Method | Frequency |
|---|---|---|---|
| Test progress, completed tests, and blockers | Developer and Product Owner | Daily message or team stand-up | Daily during testing |
| Defect description, reproduction steps, expected result, and actual result | Developer and Product Owner | GitHub issue or agreed defect tracker | Whenever a defect is found |
| Clarification of requirements and acceptance expectations | Product Owner and Tester | Team message or meeting | Whenever clarification is needed |
| Fix status and retest results | Developer and Tester | GitHub issue or team message | Whenever a fix is ready |
| Final test summary, coverage of planned tests, open defects, and release risks | Developer and Product Owner | Written test completion report | At the end of testing |

## Conclusion

This test plan defines the scope, objectives, approach, resources, risks, entry and exit criteria, schedule, and communication process for testing the North Vacation Booking application. Testing will prioritize the complete booking workflow, validation of user input, and reliable display of saved bookings. Release readiness will be assessed using the measurable exit criteria above.

## AI Transparency

AI assistance was used to help organize and draft portions of this test plan. The plan should be reviewed against the application's actual behavior and any clarifications provided by the project team.
