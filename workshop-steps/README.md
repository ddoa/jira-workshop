# Jira Workshops: On your way

## Learning Objectives
* Create Jira Agile Scrum projects.
* Perform basic administration of a planning board (workflows, columns and time tracking).
* Create tasks and subtasks
* Create and manage a product backlog based on tasks (e.g. features, user stories, use cases)
* Create and manage a sprint backlog
* View reporting like burndowns

## Steps

1. Create a new project of projecy type "Agile Scrum" with the name "Workshop" and the key "WOR".
2. Normally a Jira Agile Scrum project has a standardized workflow with the swimlanes To Do, In Progress and Done. We're going to add at least an extra swimlane but that requires a _simplified workflow_.

  Navigate to Board->Configure and click on "Columns". Click on the button "Simplify Workflow", then click "Next" and "Simplify" and finally "Acknowledge". Now click on the "Add Column" and name it "To Review". Go back to your board and click on "Work" and check to see if the "To Review"-column appears.

  > To simplify a workflow you need global administrator permissions. You might need to contact an administrator in a "live" environment to simplify your workflow.

  > Jira has to types of administrators: global administrators and board administrators. When working in a team it's easy to let all your team members manage the board: Navigate to Board->Configure and click on the pencil behind "Administrators". Add your group name (e.g. grp-Verkeersplein6) here and every member of this group can manage the board.

3. Before we can use Jira for our product backlog and sprint backlog we have to perform some last configuration to be able to see some nice reporting (e.g. the burndown). Navigate to Board->Configure and click on "Estimation". Click on "Estimation Statistic" and and select "Original Time Estimate". Set "Time Tracking" to "Remaining Estimate and Time Spent".

4. Let's create the product backlog. Go back to "Plan"-mode. The product backlog will be created using issues of type "Task".

  > A task relates to a feature expressed in the language of the customer (product owner), e.g. a user story, feature of use case. In this workshop we are going to use a use case diagram to build our product backlog.

  Click on the Blue(-ish) "Create"-button.  
