# Your First CycleCode Project

[Overview](README.md) · [Install CycleCode](INSTALL.md) · [Data and backups](DATA-AND-PRIVACY.md)

Start with one small idea and one AI connection. Your first milestone is a useful product draft you can review. A checked implementation comes later, after the relevant product decisions and approvals. This is a walkthrough of the preview workflow, not a timed demo or a claim of installed-app qualification.

## 1. Connect One Agent

After accepting the terms, use the setup wizard:

1. **AI connections:** add a provider you already have access to. For a CLI connection, install the tool and complete authentication using the provider's instructions.
2. **Check connections:** run the connection check and address any reported problem. Checks may contact the provider and incur API charges.
3. **Roles:** choose a checked connection and use **Assign to unconfigured roles**. Existing assignments and permissions are preserved. Use advanced settings when you need a different provider or model for a role.
4. **Tools:** external MCP servers and advanced tool settings can wait. Project execution will need Git and the development tools required by the selected stack.
5. **Ready to start:** review missing settings, then finish setup. A successful connection check is separate from a successful agent task or project build.

You can use **Finish later** and reopen the wizard from Settings. Saved configuration remains available there.

## 2. Start With A Small Idea

On Home, choose **Create project**. Enter a project name, select a new managed folder, and add a short description. For example:

> A shared checklist for a small team. Members can add items, mark them done, and see what remains. Start with a React web app. Keep the first version small; leave notifications and external integrations for later.

Creation opens Discovery with the description captured when provided. Continue the conversation to clarify users, the main scenario and explicit constraints. Ask for a saved product draft, read it, and correct assumptions before approving anything. Creating the project or saving a draft does not approve it.

If you already have code, choose its folder instead and review the repository understanding and proposed backlog before authorizing changes. Existing requirements can use the stories-first planning path; Architecture approval is still required for criteria and Work Item planning.

## 3. Agree On What To Build

Develop the idea through Vision, PRD, a clickable prototype where applicable, and Architecture. Review the applicable approval gates, including PRD and Architecture. For the checklist example, keep the first scope to adding, completing and listing items.

In **Plan**, review **Stories → Acceptance Criteria → Work Items**. Use coverage gaps to find requirements that have no criteria or tasks. Choose one bounded Work Item to implement first.

## 4. Prepare Project Commands

Ask Architect:

> Inspect the project and propose Run Profiles for installing dependencies, building, testing and running it. Explain the required host tools, commands and working directories. Save a proposal for my review.

Review the proposal in chat or **Project Settings → Run profiles** before approving it. You can also edit profiles there. Install the host tools the project actually requires. Do not approve guessed commands solely to clear a setup warning.

Use the app-bar Run/Test controls when appropriate to inspect workspace behavior and output. Approved project test profiles are mandatory checks for newly prepared development and repair candidates. A successful manual workspace run does not replace candidate-bound Work Item validation.

## 5. Review One Implementation

Prepare the selected Work Item using its agreed inputs, scope and acceptance criteria. Review the proposed execution scope and permissions before authorizing implementation in an isolated Git worktree.

When execution finishes, inspect the diff, recorded validation results and acceptance criteria. Address failures or uncovered behavior before accepting the candidate. Keep approval before merge/deploy explicit. Acceptance, local Git integration and external delivery are separate steps.

Preview.7 reads GitHub/Jira tasks but does not update remote issues. You can choose Manual or Semi-auto per Work Item; Semi-auto prepares stages up to development and stops at approval gates. Auto is unavailable, and the one-button project build is planned. Follow your repository's normal push, PR and delivery process for external publication. See the [release notes](release-notes/0.1.0-preview.7.md) for boundaries, including guided repair qualification.

## If You Get Stuck

| Symptom | Next action |
| --- | --- |
| CLI executable missing or sign-in fails | Follow the provider's installation/authentication instructions, correct the connection, and check it again. Finding an executable does not establish authentication. |
| A role has no usable connection | Return to Roles, assign a checked connection, and review any compatibility error. Setup completion allows visible gaps. |
| Git or a build tool is missing | Install the required host tool. The desktop Java runtime runs CycleCode; it does not supply the project's build environment. |
| Run Profiles are empty | Ask Architect for a proposal or add profiles in Project Settings. Approve agent proposals before execution. |
| An older task reports outdated test checks | Use **Update task** to refresh the prepared package. |
| An application run fails | Read the output. Use **Repair** if offered for that failure; review its proposed commands and scope. |
| You need a backup before experimenting or upgrading | Create and verify one in **Settings → Storage And Backup**, and back up the source repository separately. |

For a reproducible problem, [report an issue](https://github.com/cyclecode-labs/releases/issues) with version, OS, steps, expected behavior and actual behavior. Remove private content and credentials first.
