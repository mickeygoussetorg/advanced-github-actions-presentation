# Demo 03 Notes

Estimated Time: 20 minutes

Topics Covered:
- Composite Actions
- Container Actions
- Javascript Actions

Repos:
- https://github.com/mickeygoussetorg/get-a-dad-joke
- https://github.com/mickeygoussetorg/my-custom-csharp-container-action
- https://github.com/mickeygoussetorg/my-custom-javascript-action

Workflows:
- demo03-add-dad-joke-to-issue-using-slash-command - disabled

Before Demo
  - Enable the tell a dad joke workflow

Demo Steps
  - On slide, three types of custom actions
    - Composite
    - Container
    - Javascript
    - Good/Bad/Why to use for each
  - Open Get A Dad Joke Composite Action
    - explain how it works
    - Run test workflow
    - Go back to the advanced-github-actions-presentation and create an issue and put /joke in it.
    - Show how this is a fun example, btu does show that, just as we saw before, we can trigger off non ci/cd events to get stuff done.
  - Open Container version of Action
    - explain how it works
    - Run sample workflow
    - Show how you are using teh samepl workflow to call the action like you would if it were in a non-public repo
    - also it runs slower, and requires  linux container with docker
  - Open the Javascript version of Action
    -  explain how it works
    - Run sample workflow
    - Show how you are using teh samepl workflow to call the action like you would if it were in a non-public repo
  - Demo 3 Wrap Up Slide
    - Three types of containers
