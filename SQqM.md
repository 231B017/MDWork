### I. Requirements Met but User Needs Not Satisfied

This shows the difference between **Verification and Validation**.

* **Verification:** Checks whether the software is built according to specified requirements — *“Are we building the product right?”*
* **Validation:** Checks whether the software actually satisfies user needs — *“Are we building the right product?”*
* In this case, verification may have passed because all documented requirements were correctly implemented.
* However, validation failed because the requirements did not properly represent the users’ real expectations.
* **SQA** should prevent this by involving users, reviewing requirements, conducting prototypes/usability testing, and performing acceptance testing.

**Conclusion:** Meeting documented requirements does not guarantee software quality if the requirements themselves are incomplete or incorrect.

---

### II. Can Automated Static Analysis Replace Manual Reviews?

**No.** Automated static code analysis and manual reviews complement each other.

* **Static analysis** automatically detects issues such as syntax errors, security vulnerabilities, code smells, unused variables, and possible bugs.
* It is fast, consistent, and useful for checking large amounts of code.
* However, it cannot fully understand **business logic, user requirements, design decisions, or whether the code is easy for humans to maintain**.
* **Manual reviews and formal inspections** allow developers to examine logic, design, requirements, and coding decisions using human judgment.
* For example, a static analyzer may detect an SQL-injection risk but may not identify that a checkout process implements the wrong business rule.

**Conclusion:** Automated analysis should be used with manual reviews, not as a complete replacement.

---

### III. Unit Tests Pass but Failures Occur After Integration

Passing unit tests only proves that individual modules work correctly in isolation.

* **Integration Testing:** Checks interactions between modules. It could identify problems such as incorrect API communication, data-format mismatches, database connection issues, or incorrect interfaces.
* **System Testing:** Tests the complete integrated e-commerce system. It could identify problems involving the complete checkout, payment, login, inventory, and order-processing workflows.
* **Acceptance Testing:** Checks whether the complete system satisfies actual business and user requirements. It could identify issues such as an inconvenient checkout process or incorrect order/payment behavior.
* Therefore, testing only individual modules is insufficient because failures can occur when correctly working modules interact.

**Conclusion:** Testing should progress from **Unit → Integration → System → Acceptance Testing** before deployment.

---

### IV. Automated, Regression and Continuous Testing Strategy

The company should create an automated testing pipeline that runs tests whenever new code is committed.

**Strategy:**

1. **Automated Testing:** Automate unit, integration, API, and important system tests.
2. **Regression Testing:** Maintain a regression test suite containing previously detected and critical existing functionality.
3. **Continuous Testing:** Integrate tests into the **CI/CD pipeline** so tests automatically run after code changes and before deployment.
4. **Risk-based Testing:** Give higher priority to critical areas such as login, payments, orders, and security.
5. **Failure Handling:** Block deployment when critical automated tests fail and investigate the failures.
6. **Regular Test Maintenance:** Update the regression suite whenever new features or defects are discovered.

**Conclusion:** Combining automation, regression testing, and continuous testing ensures that new changes are checked without losing previously working functionality.
