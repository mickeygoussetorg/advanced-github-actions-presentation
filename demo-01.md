# Demo 01 Notes

Estimated Time: 20 minutes

Topics Covered:
- Issue Verification as a branch protection rule (should be preset on the repo, will turn it off later)
- Lightbulb build status
- Concurrency
- GH CLI
- CodeQL

Workflows
- demo-01-pr
  - Can keep fail commented out but point it out as to how you do it. Using Verify issue to cause failure
  - Workflow disabled at start
- demo-01-push-to-main
  - Set initial candel in progress to false for start of demo
  - workflow disabled at start
  
- pr-verify-linked-issue
  - branch protection rul for this initially
- codeql-analysis
  - turned on for PR

Before Demo
  - Make sure lightbulb is connected to wifi and set to White
  - make sure all workflows listed above are disabled
  - make sure verify linked issue is set as a branch protection rule

Demo Steps
  - On slide, give an overview of what we are doing
    - MVC App. .net core
    - On PR, we want to verify several things
      - Linked to issue
      - code builds/tests/upload artifacs
      - CodeQL scanning
      - Set color of lightbulb to green/red
    - On Push to Main
      - We will use new keyword concurrency to ensure we don't run multiple deploys at the same time, and to ensure we are deploying the latest
      - Build/Test/Upload Artifacts
      - set color of light bulb to green/red
      - Deploy to DEV/QA/PROD using environments
    - GH CLI and how it interacts with actions
      - gh workflow list/view/enable/disable/run
      - gh run list/view/watch

  - GH CLI
    - Show list of workflows in repo
    - enable the two demo01 workflows that are currently disabled
  - Create a change to the layout, create a PR
    - Notice how PR has checks, some required, some not
    - PR will fail because it isn't associated with issue
  - Update the PR with an issue tag, that check should restart and pass correctly
  - Review demo-01-pr, verify workflow, codeql workflow and explain what is happening
  - view final results of workflows.  PR should be ready to push to main
  - Review CodeQL alerts
  - Merge the PR to main. Go to Action tab and you can see it running
  - GH CLI
    - Watch the workflow run from the command line
  - Open push workflow and review what it does.  Point out the keyword concurrency. We will come back to that.
  - Show environments and how you created them
  - Concurrency keyword
    - by default, I can start multiple versions of the workflow that run at the same time
    - Concurrency allows me to control that better, to ensure I don't have multiple worflows trying to deploy at the same time
    - Right now, they way this is configured is if I start a new workflow run that has the same concurrency keyword, it goes into a wait state.
    - Start one and show it
    - Start another and show how it becomes the latest pending.
    - Or, I can make it where it kills the one currently running and starts the new one.
  - Approve the deployment to prod, show the deployment happened
  - Show PR and Push workflows again, and show how long they are
  - GH CLI
    - Show results of the watch
    - Disable the demo01 workflows, and codeql workflows, and the verify workflows
  - Demo 1 summary slide of what we covered, including
    - CI/CD
    - GH CLI
    - Concurrncy
    - CodeQL and GHAS
