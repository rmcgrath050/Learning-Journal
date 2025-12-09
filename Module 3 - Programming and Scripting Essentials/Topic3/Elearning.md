# Lession 3 : Python

## Introduction to the Software Development Lifecycle

The SDLC is a structured methodology that guides us through the process of designing, developing, testing, and deploying software applications. 


#### Planning
Definition: This initial phase involves defining the scope and purpose of the project, identifying stakeholders, and setting objectives.
Examples: Gathering requirements from clients, defining project timelines, and resource allocation.
Role of Data Engineering: Data engineers may be involved in assessing data needs, understanding data sources, and planning for data integration and storage solutions.


#### Analysis
Definition: During the analysis phase, detailed requirements are gathered and analysed to create a comprehensive project specification.
Examples: Conducting feasibility studies, defining functional and non-functional requirements.
Role of Data Engineering: Data engineers analyse data requirements, ensure data quality, and design data models that meet the project needs.

#### Design
Definition: The design phase focuses on creating the architecture and detailed design of the software based on the requirements gathered.
Examples: System architecture design, user interface design, database schema design.
Role of Data Engineering: Data engineers design the data architecture, including database schemas, ETL (Extract, Transform, Load) processes, and data pipelines.

#### Development
Definition: In this phase, actual coding takes place. Developers write the code to implement the designed functionalities.
Examples: Writing code, developing algorithms, creating user interfaces.
Role of Data Engineering: Data engineers develop the data infrastructure, implement ETL processes, and create data pipelines to ensure data flows smoothly across the system

#### Deployment
Definition: Once testing is complete, the software is deployed to a production environment where it becomes available to users.
Examples: Installing the software, configuring environments, user training.
Role of Data Engineering: Data engineers ensure that data systems are correctly deployed, migrate data if necessary, and verify that data systems are operational in the production environment.
Step 5 - Deployment: The new system was deployed with minimal downtime, thanks to careful planning and execution.


#### Testing
Definition: The testing phase involves verifying that the software works as intended and identifying any defects.
Examples: Unit testing, integration testing, system testing, user acceptance testing.
Role of Data Engineering: Data engineers test data flows, validate data accuracy and integrity, and ensure that data processing meets performance requirements.


#### Maintenance
Definition: After deployment, the software enters the maintenance phase, where it is monitored and updated as needed.
Examples: Bug fixes, software updates, performance enhancements.
Role of Data Engineering: Data engineers maintain data pipelines, update ETL processes, and ensure ongoing data quality and system performance. Data engineers fix bugs to ensure that the systems remain fully operational in production.
Step 6 - Maintenance: Data engineers continued to monitor and update the data processes, ensuring the system remained efficient and effective


## Lession 2: Introduction to Phyton

<br>
<img width="718" height="632" alt="image" src="https://github.com/user-attachments/assets/f62be2a5-bdf9-42eb-ae13-434d77a5c6c6" />

<br>
Python uses indentation to define code blocks rather than braces or keywords, which enhances readability.

Control flow refers to the order in which individual statements, instructions, or function calls are executed or evaluated in a Python program. Control flow structures include conditional statements and loops, which allow for decision-making and the repetitive execution of code. Conditional statements like if, elif, and else are used to execute code based on specific conditions.

#### Recursion + Reserved Words

Recursion is a technique where a function calls itself to solve a problem. Each recursive call reduces the problem size, bringing it closer to a base case, which stops the recursion. Recursion can simplify the solution of complex problems by breaking them down into simpler sub-problems. For example, calculating the factorial of a number can be elegantly solved using recursion


Reserved keywords: The team used reserved keywords to create functions (def), manage loops (for), and implement conditionals (if) effectively. In Python, functions are defined using the ‘def’ keyword, not ‘function’ or ‘define’!!!


## Lession 3: Introduction to test-driven development

Test-driven development (TDD) is a software development approach where tests are written before the actual code. This method involves writing a test for a specific function or feature, running the test to see it fails (since the feature isn't implemented yet), writing the minimum amount of code to pass the test, and then refactoring the code while keeping the tests green (passing). This cycle is often referred to as the Red-Green-Refactor cycle, as follows:

- Red: Write a test that fails because the feature is not yet implemented
- Green: Write just enough code to make the test pass
- Refactor: Improve the code while ensuring that all tests still pass


#### Improved code quality
Definition: TDD encourages writing code that is clean, efficient, and free of defects.
Examples: By writing tests first, developers are forced to consider edge cases and potential issues early on. This leads to more robust and reliable code.
Details: Tests serve as a form of documentation, making it easier for other developers to understand the code. Additionally, the need to write tests often leads to simpler, more modular code that is easier to maintain and extend


#### Enhanced productivity
Definition: TDD can streamline the development process, allowing for faster and more confident coding.
Examples: Developers can focus on one small piece of functionality at a time, leading to steady progress and reducing the likelihood of getting stuck on complex problems.
Details: Automated tests provide immediate feedback, helping developers quickly identify and fix bugs. This reduces the time spent on debugging and allows for more efficient use of development time.


#### Better test coverage
Definition: TDD ensures that all features of the code are tested, leading to comprehensive test coverage.
Examples: By writing tests for every new feature before implementation, developers ensure that each part of the codebase is covered by tests.
Details: TDD mandates tests before coding, enhancing coverage, reducing bugs, and aiding refactoring by detecting regressions. 



#### Facilitates refactoring
Definition: With a suite of tests in place, developers can refactor code with confidence, knowing that any errors introduced will be quickly detected.
Examples: Refactoring can improve code readability, reduce complexity, and enhance performance without altering the code's functionality.
Details: Tests safeguard functionality, promote continuous code improvement, and enhance software scalability and maintainability.


#### Clear documentation
Definition: Tests serve as live documentation that describes how the code is supposed to behave.
Examples: Instead of sifting through outdated or incomplete documentation, developers can look at the tests to understand the intended behaviour of the code.
Details: This documentation, always synced with the code, simplifies onboarding for new developers and code review for existing ones.


#### Improved code quality
Definition: TDD encourages writing code that is clean, efficient, and free of defects.
Examples: By writing tests first, developers are forced to consider edge cases and potential issues early on. This leads to more robust and reliable code.
Details: Tests serve as a form of documentation, making it easier for other developers to understand the code. Additionally, the need to write tests often leads to simpler, more modular code that is easier to maintain and extend.


#### Enhanced productivity
Definition: TDD can streamline the development process, allowing for faster and more confident coding.
Examples: Developers can focus on one small piece of functionality at a time, leading to steady progress and reducing the likelihood of getting stuck on complex problems.
Details: Automated tests provide immediate feedback, helping developers quickly identify and fix bugs. This reduces the time spent on debugging and allows for more efficient use of development time.


#### Better test coverage
Definition: TDD ensures that all features of the code are tested, leading to comprehensive test coverage.
Examples: By writing tests for every new feature before implementation, developers ensure that each part of the codebase is covered by tests.
Details: TDD mandates tests before coding, enhancing coverage, reducing bugs, and aiding refactoring by detecting regressions. 


#### Facilitates refactoring
Definition: With a suite of tests in place, developers can refactor code with confidence, knowing that any errors introduced will be quickly detected.
Examples: Refactoring can improve code readability, reduce complexity, and enhance performance without altering the code's functionality.
Details: Tests safeguard functionality, promote continuous code improvement, and enhance software scalability and maintainability. 


#### Clear documentation
Definition: Tests serve as live documentation that describes how the code is supposed to behave.
Examples: Instead of sifting through outdated or incomplete documentation, developers can look at the tests to understand the intended behaviour of the code.
Details: This documentation, always synced with the code, simplifies onboarding for new developers and code review for existing ones.


#### So, what were the benefits of this approach?
- Improved code quality :  This led to fewer bugs and a more reliable system.
- Enhanced productivity : Automated tests provided quick feedback, enabling faster bug fixes.
- Better test coverage : Every feature had associated tests, ensuring comprehensive test coverage and catching potential issues early.
- Facilitates refactoring : refactor the code to improve performance and readability without fearing regressions.
- Clear Docs : Tests provided clear documentation of the system's functionality, making it easier for new team members to understand and contribute to the project.



## Summary 

- Python syntax is the set of rules that dictate how programs written in Python language should be written. Coding conventions are
  suggestions for style and formatting to ensure that code is easy to understand and maintain.

- TDD is a software development approach in which tests are written before the code. It helps to ensure the accuracy of the code, makes the
  code more maintainable, and can lead to better design.

#### Phyton Basics

- Reserved Keywords: These are words that have a special meaning in Python and cannot be used for other purposes.
- Control Flow: This refers to the order in which the program’s code executes. Key control flow structures include if, for, and while statements.
- Recursion: A method where the solution to a problem depends on solutions to smaller instances of the same problem.
- Functions: Functions are reusable pieces of code that perform a specific task.

