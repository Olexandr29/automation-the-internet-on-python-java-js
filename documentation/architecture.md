# Architecture
<details><summary><b>Overview</b></summary>
This project is a multi-language UI test automation ecosystem built around the same application under test(AUT): [The Internet](https://the-internet.herokuapp.com/).

The project consists of a central General repositoryand three independent automation framework repositories:
- [Python](https://github.com/Olexandr29/automation-the-internet-python)
- [JavaScript](https://github.com/Olexandr29/automation-the-internet-js)
- [Java](https://github.com/Olexandr29/automation-the-internet-java)

The General repository serves as the central place for project-level documentation, test design, sprint reporting, and project management.

Each language-specific repository contains an independent UI automation framework responsible for test implementation and execution against the same AUT.

</details>


<details><summary><b>Repository Structure</b></summary>
The project is organized as a central repository with three independent automation framework repositories.

```
Automation Testing Project
│
├── General Repository
│   ├── documentation/
│   │   ├── architecture.md
│   │   ├── test-cases.md
│   │   └── sprint-reports.md
│   └── README.md
│
├── Python Automation Framework
│   ├── pages/
│   ├── test_data/
│   ├── tests/
│   ├── utils/
│   └── .github/workflows/
│
├── JavaScript Automation Framework
│   ├── pages/
│   ├── testData/
│   ├── tests/
│   ├── utils/
│   └── .github/workflows/
│
└── Java Automation Framework
    ├── src/
    │    ├── main/
    │    └── test/
    ├── testng/
    └── .github/workflows/
```
The General repository contains project-level documentation and coordination, while automation implementation is maintained in th language-specific  repositories.

For detailed framewokr structure and implementation, see the corresponding repository documantation.

</details>


<details><summary><b>Automation Frameworks</b></summary>
All three frameworks share the same core technologies and architecture approach: 

- Selenium WebDriver;
- GitHub Actions;
- Allure Report;
- Page Object Model.

The main differences are the programming language, test framework, package/project structure, and execution tools.

|Framework|Language|Test Framework|Build / Package Tool|
|---|---|---|---|
|Python|Python|Pytest|—|
|JavaScript|JavaScript|Mocha|npm|
|Java|Java|TestNG|Maven|

For implementation details, see:

- Python Architecture
- JavaScript Architecture
- Java Architecture

</details>


<details><summary><b>Test Automation Architecture</b></summary>
Although the three frameworks use different programming languages, they follow the same high-level test automation architecture.

```
Test Layer 
│ 
▼ 
Page Object Layer 
│
▼ 
Utility / WebDriver Layer 
│ 
▼ 
Browser 
│ 
▼ 
Application Under Test
```

The common architecture separates test scenarios from UI interaction, reusable framework functionality, and test execution infrastructure.

The implementation details of these layers are specific to each framework and are documented in their respective repositories.

</details>


<details><summary><b>Component Interaction
</b></summary>

```
Test
  │
  ▼
Page Object
  │
  ▼
Utility / WebDriver
  │
  ▼
Browser
  │
  ▼
Application Under Test
  │
  ▼
Test Result
  │
  ▼
Allure Report
```

Tests define scenarios and assertions,
Page Objects encapsulate UI interactions, anduUtilities provide reusable framework functionality.

The test framework executes the tests and produces results that are used to generate Allure reports.
</details>

<details><summary><b>Architecture Diagram
</b></summary>
The overall project architecture can be represented as follows:

```
                              ┌──────────────────────────┐
                              │    General Repository    │
                              │                          │
                              │ Documentation            │
                              │ Test Cases               │
                              │ Architecture             │
                              │ Sprint Reports           │
                              │ Project Management       │
                              └────────────┬─────────────┘
                                           │
                                           │ Coordination
                                           │
             ┌─────────────────────────────┼─────────────────────────────┐
             │                             │                             │
             ▼                             ▼                             ▼
     ┌─────────────────┐          ┌─────────────────┐          ┌─────────────────┐
     │ Python Framework│          │ JavaScript      │          │ Java Framework  │
     │                 │          │ Framework       │          │                 │
     │ Tests           │          │ Tests           │          │ Tests           │
     │ Pages           │          │ Pages           │          │ src/main        │
     │ Utils           │          │ Utils           │          │ src/test        │
     │ Test Data       │          │ Test Data       │          │ TestNG          │
     └────────┬────────┘          └────────┬────────┘          └────────┬────────┘
              │                            │                            │
              └────────────────────────────┼────────────────────────────┘
                                           │
                                           ▼
                                  ┌─────────────────┐
                                  │ Selenium        │
                                  │ WebDriver       │
                                  └────────┬────────┘
                                           │
                                           ▼
                                  ┌─────────────────┐
                                  │     Browser     │
                                  └────────┬────────┘
                                           │
                                           ▼
                                  ┌─────────────────┐
                                  │       AUT       │
                                  │  The Internet   │
                                  └────────┬────────┘
                                           │
                                           ▼
                                  ┌─────────────────┐
                                  │  Test Results   │
                                  └────────┬────────┘
                                           │
                                           ▼
                                  ┌─────────────────┐
                                  │  Allure Report  │
                                  └─────────────────┘
```
The General repository provides the project-level documentation and coordination layer, while the three language-specific repositories independently implement and and execute the automation.

</details> 