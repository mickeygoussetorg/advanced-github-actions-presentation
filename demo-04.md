# Demo 04 Notes

Estimated Time: 10 minutes

Topics Covered:
- IssueOps
- Real-world example of using workflows and issues to get stuff done
- Caching

Repos:

Workflows:
- demo04-sonarcloud - disabled

Before Demo
  - Enable demo-04-sonarcloud
  - remove sonar_token secret

Demo Steps
  - On slide, overview
    - Real world example
    - explain scenario
    - Developers need to use sonarcloud scanning, but don't have ability to create a key
    - Ops (who has that ability), wants to provide a way to review and automate key creation for a developer
    - Caching

  - Open Demo04 sonarcloud scanner and review workflow
    - Explain what the caching does for us
    - Show how we need a sonar token to make this work
  - Go to the request sonar token repo and request a token
  - Show how workflow runs and creates the secret
  - Runthe workflow, view the results. If caching didn't work, because you haven't run in a while, then rerun and you will see caching work, which shows conditional expressions as well
