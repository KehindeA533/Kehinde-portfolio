# Continuous Integration with GitHub Actions - Deployment Project

## Overview

This deployment project demonstrates the integration of Continuous Integration (CI) using GitHub Actions, aimed at automating manual and repetitive tasks in a software development process. CI significantly increases productivity by ensuring that code changes are continuously tested and validated before being merged. This project is set up to run tests automatically whenever there is a pull request to the master branch, ensuring that only stable and tested code is integrated.

The rationale behind this project was to automate the testing and build process for my projects, reducing the risk of bugs and integration issues by catching them early in the development cycle.

Manual testing and code reviews can be error-prone and time-consuming. The goal was to implement a system that would automatically validate code through testing and build processes before merging it into the main branch.

## Tech Stack:

- **CI/CD Tool:** GitHub Actions
- **Scripting Language:** YAML (for defining workflows)
- **Environment:** Node.js, Ubuntu (for virtual machine setup)

GitHub Actions was chosen because it integrates seamlessly with GitHub repositories, making it easier to automate workflows directly within the platform. Node.js was used because the project was built with JavaScript, and Ubuntu was selected for the virtual machine environment due to its widespread use in CI/CD pipelines.

## Design and Architecture:

The project structure includes a `.github/workflows` directory containing a YAML file named `integrate.yml`. This file defines the CI workflow:

- **Event Trigger:** The workflow is triggered by pull requests to the master branch.
- **Jobs:** A job named "test pull request" runs on an Ubuntu virtual machine.
- **Steps:**
  - **Checkout Code:** The workflow checks out the code from the repository into the virtual machine.
  - **Set Up Node.js:** Node.js is set up with the specified version using the node setup action.
  - **Install Dependencies:** All dependencies are installed using the CI command, similar to `npm install`.
  - **Run Tests:** The test suite is executed to ensure that the code passes all tests.
  - **Build Code:** The code is built to confirm that it compiles correctly.

## Challenges:

One challenge I faced was not realizing that I didn’t have the `.github/workflows` directory inside my repository folder. I was working outside of it, so whenever I triggered the workflow, nothing happened. I realized this after about 45 minutes of debugging.

## Overview of Completed Integration:

The CI pipeline is fully operational, running tests and builds automatically on every pull request to the master branch. The system uses real-time logging to display the status of each step, providing immediate feedback on the success or failure of the tests.

This project reinforced the importance of automation in the software development process. I learned how to leverage GitHub Actions to streamline CI workflows, and the experience underscored the value of integrating automated testing into the development pipeline.

---

## Competencies

### JF 4.5: Can explain relevant and up-to-date software testing frameworks and methodologies.

**Situation:**  
As part of setting up Continuous Integration (CI) for my project using GitHub Actions, I needed to implement up-to-date software testing frameworks to ensure code quality.

**Actions:**
- Integrated a testing framework that automatically runs a suite of unit tests whenever code changes are pushed or a pull request is made.
- Configured the CI pipeline to run on specific triggers and built it to test the code thoroughly using modern testing methodologies such as Test-Driven Development (TDD).

**Results:**  
The CI pipeline now continuously runs tests and builds the project, ensuring code stability and catching errors before they are merged into the master branch. This setup keeps the project aligned with current software testing practices.

---

### JF 5.2: Understands how to test code and analyze results to correct errors found using unit testing.

**Situation:**  
Ensuring that code changes didn't introduce bugs or break the application required a robust testing process within the CI pipeline.

**Actions:**
- Configured the CI workflow to include unit testing as part of the automated checks.
- Wrote unit tests for critical components of the project and set up the pipeline to analyze results from each test suite run.
- When a test failed, I examined the logs, identified the error, and corrected the code before re-running the pipeline.

**Results:**  
By integrating unit testing into the CI pipeline, I was able to catch bugs early in the development process, improve code reliability, and ensure that new features did not disrupt existing functionality. This iterative process improved the stability and correctness of the project.

---

### JF 6.4: Works independently and takes responsibility. For example, has a disciplined and responsible approach to risk, and stays motivated and committed when facing challenges.

**Situation:**  
Setting up a CI/CD pipeline and managing its various aspects, including ensuring that tests run properly and builds are successful, required disciplined and independent work.

**Actions:**
- Independently set up GitHub Actions for CI, configuring YAML files to define the pipeline's flow, specifying triggers, and ensuring that all dependencies were handled correctly.
- When faced with challenges, such as failed builds or test errors, I analyzed the issues, took responsibility for resolving them, and adjusted the pipeline or code as necessary to ensure successful builds.

**Results:**  
Through disciplined and independent work, I successfully established a reliable CI workflow that automated testing and deployment, maintaining project stability. My commitment to resolving issues helped ensure that the system operated smoothly, reducing the risk of bugs entering the production environment.
