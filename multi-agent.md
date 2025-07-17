# Multi-Agent

You are given the following context:
$ARGUMENTS

## Task

You are tasked with initializing a multi-agent system.

Follow the steps below.

## Glossary

### Structure

- task/: The task folder.
  - context.md: The context of the task.
  - plan.md: The plan for the task.
  - channel.md: The team chat channel for the task.
  - agents/: The agents for the task.
    - agent\_<agent_number>.md: An agent file.

### Components

- Task: The task to be completed.
- Agent: A single agent that is part of the team.

## Steps

### Step 1: Initialize the task folder

In .claude/tasks create a new folder for the current task.

In the task folder:

- create a new file called context.md
- create a new file called plan.md
- create a new file called channel.md
- create a new folder called agents/

### Step 2: Create the context file

Use ultrathink to deeply research the codebase until you have a complete understanding of how it works, how it is organized, and how the current task relates to it.

The goal is to gain a comprehensive understanding of the codebase needed to complete the task that can be passed to each of the agents on the team.

Record your research in the context.md file. It should be considerably in-depth. Provide so much context that it almost feels like overkill.

Context is the #1 driver of performance, and without it the team will not be able to complete the task.

### Step 3: Create the plan file

Use ultrathink to create a detailed plan for the task based on your research in the plan.md file.

As you create the plan, you may find that you need to research more about the codebase. If you do so, use ultrathink and keep the context.md file updated.

### Step 4: Wait for plan approval

Before continuing, ask me to approve the plan.

We may iterate on the plan until it is approved.

As we iterate, continue to update both the plan.md and context.md files.

### Step 5: Modify the plan for multi-agent collaboration

Use ultrathink to turn the plan.md file into a multi-agent collaboration plan.

Divide the plan up amongst a team of 2-4 agents. Determine the number of agents based on the complexity of the task. Do not create more agents than necessary. The goal is to mimic a real-world team of developers working on a project. A multi-agent team allows us to parallelize, specialize, and optimize the work of the team. An added agent must serve a purpose. No fluff.

The updated plan will be given to each agent so that they can begin working on the task and collaborating with each other.

### Step 6: Create the agent files

For each agent, create a new file in the agents folder called agent\_<agent_number>.md.

As each agent works, they will update their notepad with their thoughts and progress as they go. All agents can see each other's notepads, but only the agents themselves can edit their own notepad.

Each agent will also update the plan.md file with their progress as tasks are completed and sign off on each task with @agent_number.

The agent file should be formatted as follows:

```md
# Agent <agent_number>

## Role

<role_here>

## Responsibilities

<responsibilities_here>

## Notepad

<leave_empty>
```

Example:

```md
# Agent 1

## Role

Backend Developer

## Responsibilities

- [ ] Implement the backend of the application
- [ ] Create the API endpoints
- [ ] Create the database schema
- [ ] Create the authentication system
- [ ] Create the authorization system
- [ ] Create the logging system
- [ ] Create the error handling system

## Notepad
```

### Step 7: Create the channel file

Each agent will have access to the channel.md file.

This file mimics a real-world Slack channel for the team to communicate with each other while working on the task.

Anytime an agent needs to communicate with the team, they will update the channel.md file with their message.

Agents can tag individual agents with @agent_number, multiple agents with @agent_number1, @agent_number2, etc., or the entire team with @all.

Agents can create threads by replying under a message as a new sub-message. Agents are encouraged to use threads to keep the conversation organized and easy to follow, just like a real team would in Slack.

All agents should frequently check the channel.md file and update it as needed. Team collaboration is key to success.

You only need to add the core structure of the file and add the team members. Leave the messages empty to start.

The file should be formatted as follows:

```md
# Team Chat Channel

## Team Members

- <agent_number>: <agent_role>
- ...

## Messages
```

Here's an example of a working channel file:

```md
# Team Chat Channel

## Team Members

- agent_1: Backend Developer
- agent_2: Frontend Developer
- agent_3: UI/UX Developer

## Messages

...

- agent_2: I've begun working on ...

- agent_1: I've completed ...

- agent_3: @agent_1, Can you create the API endpoints for ...

  - agent_1: No problem, I'll get started on ...

  - agent_3: @agent_1, That's now done. Let me know if ...

- agent_3: @all, Does anyone know if ...

  - agent_2: Yeah, you can use ...

- agent_2: Just finished the UI for ...

...
```
