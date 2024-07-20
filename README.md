# Github Actions Events - Action Types and Event Filters

For example, we may only need to trigger the workflow when you push to the main branch

We would need to configure the behavior of event triggers to control when the workflow runs

So for this, we need to use event related features live events filters and activity types

Activity types allows you to specify which exact version or variation of event should trigger a workflow

For example, pull_request event has multiple variations like opened, edited, closed, etc.

Event filters allows you to specify the conditions that must be met for the workflow to run

For example, we can specify the branch name in the event filter to trigger the workflow only when the push is made to the main branch

Activity Types -> https://docs.github.com/en/actions/reference/events-that-trigger-workflows

Event Filters -> https://docs.github.com/en/actions/using-workflows/workflow-syntax-for-github-actions
