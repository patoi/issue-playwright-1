# Reproduction Playwright test runner issue with ES module on Ubuntu

Playwright runner doesn't execute test and give a "no tests found." message, if the path contains a hidden directory reference (.hidden-jenkins-directory).

This issue blocks test running on Jenkins server with default workspace dir path.

Reproduction: same test, and package.json in different directories, one of them is hidden

- Successful running: `cd an-ordinary-directory && npm i && npm test && cd ..`
- "no tests found" message: `cd .hidden-jenkins-directory && npm i && npm test`
