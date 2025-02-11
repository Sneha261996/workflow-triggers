# workflow-triggers

Branch Protection Rule:

Branch protection rules are policies on specific branches in a repository to prevent accidental or unauthorized changes. 

It prevents direct pushes to main branch, require pull request review

created → Triggers when a branch protection rule is added.
deleted → Triggers when a branch protection rule is removed.
edited  → Triggers when a branch protection rule is modified.

🔹 Create a Branch Protection Rule
Go to: Settings → Branches → Add Rule.
Set a rule for main branch.
Click Save changes.
The workflow will trigger automatically (check Actions tab).

Check-run:

Whenever you push code to GitHub or open a pull request, automated checks run to verify:
✅ Did the code compile successfully?
✅ Did all tests pass?
✅ Is the code formatted correctly?

Each of these checks (e.g., running tests, checking for errors) is a Check Run.

Check status:
Action (created, completed)
Check Run Name (e.g., “Lint Check” or “Unit Tests”)
Status (in_progress, completed)
Conclusion (success, failure, neutral)
Who triggered the event (github.actor)


check_suite:

A Check Suite is a group of Check Runs that GitHub runs on a commit to verify code quality.
✅ Linting Check → Ensures code follows style guidelines
✅ Unit Tests Check → Runs automated tests
✅ Security Scan Check → Detects vulnerabilities

Create a reusable workflow that runs when called (workflow_call).

The workflow_run event allows a workflow to run after another workflow completes.

