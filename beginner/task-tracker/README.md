# Task Tracker

Build a CLI app to track tasks and manage your top-down list.

## Requirements
The CLI application must:
- Run from the command line using positional arguments
- Store tasks in a JSON file (created automatically if missing)
- Support these actions:
  - Add/Update/Delete tasks
  - Mark tasks as: `todo`, `in-progress`, or `done`
  - List tasks (all tasks/filtered by status)
  
**Constraints**:
- Use native filesystem modules (no external libraries)
- Handle errors gracefully
- Task properties must include:
  - Unique ID
  - Description
  - Status
  - Creation timestamp (`creatable`)
  - Update timestamp (`updatedable`)

## Example Usage
```bash
# Add task
task-cli add "Buy groceries"  # Output: Task added successfully (ID: 1)

# Update task
task-cli update 1 "Buy groceries and cook dinner"

# Mark status
task-cli mark-in-progress 1
task-cli mark-done 1

# List tasks
task-cli list
task-cli list done
task-cli list todo
task-cli list in-progress