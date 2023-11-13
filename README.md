[![CI/CD Workflow](https://github.com/cassiekang/IDS706-template/actions/workflows/cicd.yml/badge.svg)](https://github.com/cassiekang/IDS706-template/actions/workflows/cicd.yml)


## Template for Python projects
The goal of this repository is to provide a template for future projects. It includes the following components:

1.`Makefile`: a makefile is a configuration file used in Unix-based systems for autmating tasks and building software. It contains instructions and dependencies for compiling code, running tests, and other development tasks.
I also used commands "make lint", "make test", "make format" to check format and errors, and my repo has passed all the test.
<img width="1144" alt="Screen Shot 2023-09-06 at 19 40 55" src="https://github.com/cassiekang/IDS706-template/assets/143849077/3b39149b-4d8b-4480-bae4-1286ec4eee68">

<img width="1153" alt="Screen Shot 2023-09-06 at 19 41 15" src="https://github.com/cassiekang/IDS706-template/assets/143849077/e9a1ba7c-f2aa-4a26-ba76-9aa0df0297e2">

2. `requirments.txt`: this file is to specify the dependencies (libraries and packages) required to run the project.  

3. `.devcontainer` including a `Dockerfile`: the 'Dockerfile' within this folder specifies how the container should be built, and other settings in this directory may control development environment configurations.

4. `.gitignore`: this file is used to specify which files or directories should be excluded from vrsion control when using Git.

5. `GitHubActions`: (.github/workflows) which contain configuration files for setting up automated build, test and deployment pipelines for the project.

6. `main.py`: This is the main Python script for the project. Modify it to implement the project's functionality.

7. 'test_main.py': This is the unit testing script for the project. Write test cases to ensure the correctness of the code.







