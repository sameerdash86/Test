Explanation of Configuration:

Schedule (on.schedule): The workflow is scheduled to run daily at midnight UTC. Adjust the cron expression to modify the frequency (e.g., '0 0 * * 0' for weekly runs on Sundays).​

Permissions (permissions): The workflow requires write permissions for contents, issues, and pull requests to perform actions like labeling, commenting, and closing PRs.​
GitHub

Action Settings (with):

days-before-pr-stale: Sets the number of days of inactivity before a PR is marked as stale.​
GitHub

days-before-pr-close: Sets the number of days after being marked stale before a PR is closed. Setting this to 0 closes the PR immediately after marking it stale.​

stale-pr-message: Comment added when a PR is marked as stale.​

close-pr-message: Comment added when a PR is closed due to inactivity.​

stale-pr-label: Label applied to stale PRs.​

exempt-pr-labels: PRs with this label will not be marked as stale or closed.​
GitHub

delete-branch: If set to true, deletes the branch after closing the stale PR.​
GitHub

Additional Considerations:

Manual Triggering (workflow_dispatch): This allows you to manually trigger the workflow from the Actions tab in your repository.​
GitHub

Exemptions: Use the exempt-pr-labels option to prevent certain PRs from being marked as stale or closed. For example, adding a do-not-stale label to a PR will exempt it from this workflow.​
GitHub

Branch Deletion: The delete-branch option ensures that the branch associated with the closed PR is also deleted, helping to keep your repository clean.