# Demo repo for testing dipatch events for ChatOps development

The following GitHub Actions [automation commands](.github/workflows) are supported in the comments for this repository's issues:

| Command                         | Action                                                                                                                       |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| /help                           | Posting the help message with the list of possible commands.                                                                 |
| /start                          | Assignee → commenter<br/>DRI → commenter<br/>Status → `In Progress`                                                          |
| /assign @username               | Assignee → @username<br/>DRI → @username<br/>Status → `Ready`                                                                |
| /review @username               | Assignee → @username<br/>Code Reviewer → @username<br/>Status → `In Review`                                                  |

The following GitHub Actions [automation commands](.github/workflows) are supported in the comments for this repository's PRs:

| Command                         | Action                                                                                                                       |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| /help                           | Posting the help message with the list of possible commands.                                                                 |
| /ci                             | Run the basic CI for the PR and publish test results as comment                                                              |

(commenter = a person who left a PR comment with a command)

You can do any of the operations above manually in case you want to bypass the automation.

The comment parser works if there’s additional text in the comment after the command so that one can send a comment like this:

> /start
>
> Off we go! 🚀
