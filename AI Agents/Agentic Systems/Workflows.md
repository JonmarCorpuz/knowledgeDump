# Workflow Overview

Workflows are systems where LLMs and tools are orchestrated through predefined code path

<br>

# Workflow Design Patterns

## Prompt Chaining

* Tasks can be decomposed into fixed sub-tasks

<br>

## Routing

* Directs an input into a specialized sub-task 
* Ensures separation of concerns

<br>

## Parallelization

* Runs multiple subtasks concurrently (The tasks don't have to be different)
* Code is doing the orchestration

<br>

## Orchestrator Worker

* Complex tasks are broken down dynamically and recombined
* LLM is doing the orchestration (We're using a LLM model to break down a complex task into smaller steps and then using a LLM model to combine the results)

<br>

## Evaluator-Optimizer

* LLM output is validated by another LLM

<br>