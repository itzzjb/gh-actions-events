# Github Actions Events - Action Types and Event Filters

For example, we may only need to trigger the workflow when you push to the main branch

We would need to configure the behavior of event triggers to control when the workflow runs

So for this, we need to use event related features live events filters and activity types

Activity types allows you to specify which exact version or variation of event should trigger a workflow

For example, pull_request event has multiple variations like opened, edited, closed, etc.

Event filters allows you to specify the conditions that must be met for the workflow to run (branches, paths, branches-ignore, paths-ignore)

For example, we can specify the branch name in the event filter to trigger the workflow only when the push is made to the main branch

Activity Types -> https://docs.github.com/en/actions/reference/events-that-trigger-workflows

Event Filters -> https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions

## Workflow runs for pull requests of Forked Users

When a user who is a first time contributor (never opened a pull request before) forks the repository and opens a pull request to tha main repository, even if the event filters and action types are fulfilled, the workflow won't start.

This is because anyone can fork the repository and make workflows run in a malicious way, or spam the main repository by pull request that starts workflow runs. A github paid user this could even cause money.

The owner of the repository must manually approve the workflow run. After the first approval the following pull requests will automatically run the workflow without the permission of the owner.

> [!NOTE]
> Collaborates don't need to wait for the approval like forked users, they are considered as trusted users by the owner. So, the workflows will run for them automatically.
