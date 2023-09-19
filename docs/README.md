# Joe User Guide

## Usage

### `todo` - Creates a new todo task

Describe the action and its outcome.
#### Usage:
`todo <task_name>`

#### Example of usage: 

`todo sleep`
`todo cook dinner`

#### Expected outcome:

Joe will add the task to your todo list.

```
Got it, I've added this task:
[T][ ] sleep
Now you have 1 task in the list.
```

### `deadline` - Creates a new deadline task

Describe the action and its outcome.
#### Usage:
`deadline <task_name> /by <dd/m/yyyy HHmm>`

#### Example of usage:

`deadline CS2103t ip /by 22/09/2023 1600`

#### Expected outcome:

Joe will add the task to your list.

```
Got it, I've added this task:
[D][ ] CS2103t ip (by: 22 Sep 2023 16:00)
Now you have 1 task in the list.
```

### `event` - Creates a new event task

Describe the action and its outcome.
#### Usage:
`event <task_name> /from <dd/m/yyyy HHmm> /to <dd/m/yyyy HHmm>`

> **Note**: `/to` should be equals to or after `/from`

#### Example of usage:

`event CS2103t finals /from 01/12/2023 0900 /to 01/12/2023 1100`

#### Expected outcome:

Joe will add the task to your list.

```
Got it, I've added this task:
[E][ ] CS2103t finals (from: 01 Dec 2023 09:00 to: 01 Dec 2023 11:00)
Now you have 1 task in the list.
```

### `list` - Shows the list of tasks

#### Usage:
`list`

#### Expected outcome:

Joe will show you the current list of tasks.

```
Here are your tasks:
1. [T][ ] sleep
2. [D][ ] CS2103t ip (by: 22 Sep 2023 16:00)
3. [E][ ] CS2103t finals (from: 01 Dec 2023 09:00 to: 01 Dec 2023 11:00)
```

### `mark` - Marks a task as completed

> **Note**: <task_number> refers to the numbering shown in `list`

#### Usage:
`mark <task_number>`
#### Example of usage:

`mark 1`

#### Expected outcome:

Joe will mark tasks #1 as completed.

```
Nice! I've marked this task as done:
[T][X] sleep
```

### `unmark` - Unmarks a task as completed

> **Note**: <task_number> refers to the numbering shown in `list`

#### Usage:
`unmark <task_number>`
#### Example of usage:

`unmark 1`

#### Expected outcome:

Joe will unmark tasks #1 as completed.

```
Ok! I've marked this task as not done:
[T][ ] sleep
```

### `find` - Searches for tasks whose `<task_name>` contains the keyword

> **Note**: `find` is **NOT** case-sensitive

#### Usage:
`find <key_words>`
#### Example of usage:

`find CS2103T FINALS`

#### Expected outcome:

Joe will find all tasks whose `<task_name>` contain the `<key_words>`.

```
Here are the find results:
1. [E][ ] CS2103t finals (from: 01 Dec 2023 09:00 to: 01 Dec 2023 11:00)
```

### `findmatch` - Searches for tasks whose `<task_name>` contains the keyword with matching case

> **Note**: `findmatch` **IS** case-sensitive

#### Usage:
`find <key_words>`
#### Example of usage:

`findmatch FINALS`

#### Expected outcome:

Joe will find all tasks whose `<task_name>` contain the `<key_words>` with matching case.

```
Here are the find results:
No tasks available
```

### `findall` - Searches for tasks that contains the keyword in any part of the tasks

> **Note**: `findall` is **NOT** case-sensitive

#### Usage:
`find <key_words>`
#### Example of usage:

`findall sep`

#### Expected outcome:

Joe will find all tasks that contain the `<key_words>`.

```
Here are the find results:
1. [D][ ] CS2103t ip (by: 22 Sep 2023 16:00)
```

### `delete` - Removes a task from the list

#### Usage:
`delete <task_number>`

> **Note**: <task_number> refers to the numbering shown in `list`

#### Example of usage:

`delete 1`

#### Expected outcome:

Joe will delete task #1 from the list.

```
Noted! I've removed this task:
[T][ ] sleep
Now you have 2 tasks in the list.
```

### `bye` - Stops the chatbot and saves tasks to file

#### Usage:
`bye`

#### Expected outcome:

Joe will say goodbye and disable the chat box.

```
Bye. Hope to see you again soon!
```

### Saving the data
Tasks are automatically saved to the disk after any commands that changes the data.

### Editing the data file
Task data are saved as a txt file in `joe.txt` in the same directory as the JAR file.