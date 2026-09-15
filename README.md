# Awesome Agentic AI [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0--1.0-lightgrey.svg)](LICENSE)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](CONTRIBUTING.md)

A curated collection of **Agentic AI resources** for developers, researchers, and learners, including AI agent frameworks, tutorials, courses, hands-on projects, MCP tools, multi-agent systems, research papers, benchmarks, evaluation tools, security practices, observability resources, and production guides.

Agentic AI moves beyond single-turn generation toward systems that can reason across multiple steps, use tools, retrieve knowledge, maintain state, collaborate with other agents, and take controlled actions on behalf of users. This repository is designed to help you **learn Agentic AI, build AI agents, evaluate them, secure them, and operate them reliably in production**.

> **Curation over collection:** inclusion is based on technical relevance, documentation quality, maintenance, practical usefulness, and value to the Agentic AI community. This repository is not intended to list every AI agent project.

## Contents

- [What Is Agentic AI?](#what-is-agentic-ai)
- [Start Here](#start-here)
- [Titan Codes Agentic AI Developer Roadmap](#titan-codes-agentic-ai-developer-roadmap)
- [Agentic AI Learning Resources](#agentic-ai-learning-resources)
  - [Beginner Guides and Tutorials](#beginner-guides-and-tutorials)
  - [Agentic AI Courses](#agentic-ai-courses)
  - [Agentic AI Projects and Hands-On Tutorials](#agentic-ai-projects-and-hands-on-tutorials)
  - [Roadmaps and Reference Guides](#roadmaps-and-reference-guides)
  - [Books](#books)
  - [Selected Videos](#selected-videos)
- [Core Agentic AI Concepts and Patterns](#core-agentic-ai-concepts-and-patterns)
- [Agentic AI Frameworks and SDKs](#agentic-ai-frameworks-and-sdks)
- [How to Choose an Agentic AI Framework](#how-to-choose-an-agentic-ai-framework)
- [Protocols and Interoperability](#protocols-and-interoperability)
- [Tool Use and MCP](#tool-use-and-mcp)
- [Retrieval, RAG, and Memory](#retrieval-rag-and-memory)
- [Agent Evaluation and Testing](#agent-evaluation-and-testing)
- [Observability and Tracing](#observability-and-tracing)
- [Guardrails, Security, and Human Oversight](#guardrails-security-and-human-oversight)
- [Sandboxes and Computer Use](#sandboxes-and-computer-use)
- [Research Papers](#research-papers)
- [Agent Benchmarks](#agent-benchmarks)
- [Production Readiness Checklist](#production-readiness-checklist)
- [Contributing](#contributing)
- [Maintainers](#maintainers)

## What Is Agentic AI?

**Agentic AI** refers to AI systems that can pursue goals through multiple steps instead of only generating a single response. An agent typically combines a model with instructions, tools, external knowledge, state or memory, and a control loop that determines what to do next.

A useful mental model is:

**Model + Instructions + Context + Tools + State + Control Loop + Evaluation + Guardrails**

Not every AI application needs an autonomous agent. Deterministic workflows are often easier to test and safer to operate. Agentic approaches are most useful when a task involves ambiguity, changing information, tool use, iterative reasoning, dynamic planning, or decisions that cannot be fully encoded in advance.

Common Agentic AI capabilities include:

- Tool and function calling.
- Retrieval-augmented generation (RAG).
- Short-term and long-term memory.
- Planning and task decomposition.
- Reflection and iterative improvement.
- Routing and delegation.
- Multi-agent collaboration.
- Model Context Protocol (MCP) integrations.
- Agent-to-agent interoperability.
- Human approval and escalation.
- Evaluation, tracing, and observability.
- Sandboxed code or computer use.

## Start Here

If you are new to Agentic AI, use this sequence:

1. **LLM fundamentals** - Understand prompts, context windows, structured outputs, model limitations, and API usage.
2. **Tool calling** - Learn how models select and invoke functions, APIs, search, databases, and external systems.
3. **Single-agent loops** - Build an agent that can decide, act, observe results, and continue until a task is complete.
4. **RAG and retrieval** - Give agents access to relevant external knowledge instead of relying only on model memory.
5. **State and memory** - Preserve useful information across steps, conversations, or sessions.
6. **Agentic patterns** - Learn routing, sequential workflows, parallelization, planner-executor, reflection, and evaluator-optimizer patterns.
7. **Multi-agent systems** - Introduce specialist agents only when decomposition or separation of responsibilities is useful.
8. **MCP and interoperability** - Connect agents to tools and external systems through standardized protocols.
9. **Evaluation** - Measure outcomes, tool use, trajectories, groundedness, reliability, latency, and cost.
10. **Guardrails and human approval** - Add permissions, validation, escalation, and review before granting consequential autonomy.
11. **Observability** - Trace model calls, tool calls, state changes, handoffs, errors, token usage, and latency.
12. **Production engineering** - Design for retries, idempotency, timeouts, fallbacks, security, monitoring, and controlled failure.

## Titan Codes Agentic AI Developer Roadmap

This roadmap provides a practical progression from learning the fundamentals to building production-ready AI agents.

| Stage | Learn | Build |
| --- | --- | --- |
| **1. Foundations** | Python, APIs, JSON, LLM basics, prompting, structured outputs | Simple LLM-powered application |
| **2. Tool Calling** | Functions, schemas, API tools, error handling | Agent with two or three reliable tools |
| **3. Agent Loops** | Thought/action/observation loops, stopping conditions | Single task-completing agent |
| **4. Retrieval** | Embeddings, vector search, RAG, hybrid retrieval | Knowledge or research agent |
| **5. State & Memory** | Session state, short-term memory, persistent memory | Agent that remembers useful context |
| **6. Agentic Patterns** | Routing, parallelization, reflection, planner-executor, evaluator-optimizer | Multi-step workflow with explicit control |
| **7. Multi-Agent Systems** | Supervisors, specialists, handoffs, agents-as-tools | Coordinated specialist-agent system |
| **8. MCP & Interoperability** | MCP servers/clients, tool discovery, A2A concepts | Agent connected to external systems through MCP |
| **9. Evaluation** | Task success, trajectory evaluation, tool accuracy, regression testing | Repeatable agent evaluation suite |
| **10. Security & Guardrails** | Prompt injection, permissions, sandboxing, approvals, PII controls | Agent with constrained tool access and approval gates |
| **11. Observability** | Tracing, logs, latency, token usage, cost, failure analysis | Debuggable and measurable agent service |
| **12. Production** | Retries, idempotency, queues, timeouts, fallbacks, deployment | Production-ready agent with monitoring and safe failure modes |

---

# Agentic AI Learning Resources

## Beginner Guides and Tutorials

These resources are suitable for learning core Agentic AI concepts, architecture, tools, evaluation, MCP, and implementation patterns.

| Resource | Provider | Why it is useful |
| --- | --- | --- |
| [A Practical Guide to Building Agents](https://openai.com/business/guides-and-resources/a-practical-guide-to-building-ai-agents/) | OpenAI | Framework-agnostic introduction to agent use cases, tools, instructions, orchestration, multi-agent patterns, and guardrails. |
| [Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents) | Anthropic | Strong conceptual guide to workflows versus agents and simple, composable agentic patterns. |
| [Effective Context Engineering for AI Agents](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents) | Anthropic | Explains how to manage instructions, tools, memory, history, and external context across long-running agent interactions. |
| [Writing Effective Tools for AI Agents](https://www.anthropic.com/engineering/writing-tools-for-agents) | Anthropic | Practical guidance for designing, testing, and improving tools that agents can reliably select and use. |
| [Demystifying Evals for AI Agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents) | Anthropic | Current guide to evaluating multi-turn, tool-using agents and building useful evaluation suites. |
| [OpenAI Agents SDK Quickstart](https://openai.github.io/openai-agents-python/quickstart/) | OpenAI | Hands-on path from a first agent to tools, multiple agents, handoffs, and tracing. |
| [OpenAI Agents SDK Examples](https://openai.github.io/openai-agents-python/examples/) | OpenAI | Official examples covering routing, agents-as-tools, parallelization, guardrails, MCP, memory, and more. |
| [Human-in-the-Loop with the OpenAI Agents SDK](https://openai.github.io/openai-agents-python/human_in_the_loop/) | OpenAI | Approval and rejection patterns for sensitive tool actions, including pause and resume. |
| [Tools in the OpenAI Agents SDK](https://openai.github.io/openai-agents-python/tools/) | OpenAI | Reference for function tools, hosted tools, agents as tools, shell execution, computer use, and MCP integrations. |
| [Introduction to Agents](https://huggingface.co/learn/agents-course/en/unit1/introduction) | Hugging Face | Beginner-friendly explanation of agents, tools, messages, reasoning loops, actions, and observations. |
| [Build Your First Agent with smolagents](https://huggingface.co/learn/agents-course/unit1/tutorial) | Hugging Face | Step-by-step first agent tutorial using tools and the smolagents framework. |
| [smolagents Documentation](https://huggingface.co/docs/smolagents/index) | Hugging Face | Official documentation for tool-calling agents, code agents, multi-agent systems, monitoring, and secure execution. |
| [Google ADK Python Quickstart](https://adk.dev/get-started/python/) | Google | Official quickstart for creating, running, and inspecting an ADK agent. |
| [Building AI Agents with ADK: The Foundation](https://codelabs.developers.google.com/devsite/codelabs/build-agents-with-adk-foundation) | Google | Foundational hands-on codelab for building an agent with Google's Agent Development Kit. |
| [Building AI Agents with ADK: Empowering with Tools](https://codelabs.developers.google.com/devsite/codelabs/build-agents-with-adk-empowering-with-tools) | Google | Hands-on codelab covering custom tools, search, framework integrations, and subagents. |
| [Tools Make an Agent](https://codelabs.developers.google.com/codelabs/cloud-run/tools-make-an-agent) | Google | Build an assistant and progressively add functions, search, third-party tools, subagents, and MCP capabilities. |
| [Microsoft Agent Framework Development Journey](https://learn.microsoft.com/en-us/agent-framework/journey/) | Microsoft | Progressive learning path from model calls to tools, context, memory, skills, middleware, and composition. |
| [Microsoft Agent Framework Get Started](https://learn.microsoft.com/en-us/agent-framework/get-started/) | Microsoft | Build an agent from scratch, then add tools, sessions, memory, workflows, an agent harness, and hosting. |
| [Introduction to AI Agents and Agent Use Cases](https://github.com/microsoft/ai-agents-for-beginners/blob/main/01-intro-to-ai-agents/README.md) | Microsoft | Beginner lesson explaining agent anatomy, use cases, and when agentic solutions make sense. |
| [Thinking in LangGraph](https://docs.langchain.com/oss/python/langgraph/thinking-in-langgraph) | LangChain | Guide to translating a real workflow into state, nodes, decisions, transitions, retries, and human review. |
| [Build a SQL Agent](https://docs.langchain.com/oss/python/langchain/sql-agent) | LangChain | Practical database agent with schema discovery, SQL generation, error recovery, and human review. |
| [Build a Custom Agentic RAG System](https://docs.langchain.com/oss/python/langgraph/agentic-rag) | LangChain | Build an agent that decides when to retrieve, evaluates retrieved information, and rewrites queries. |
| [Build Your First MCP Server](https://modelcontextprotocol.io/docs/develop/build-server) | Model Context Protocol | Official tutorial for exposing tools and capabilities through an MCP server. |
| [Build an MCP Client](https://modelcontextprotocol.io/docs/develop/build-client) | Model Context Protocol | Official walkthrough for discovering MCP tools and invoking them from an AI application. |
| [CrewAI Documentation and Quickstart](https://docs.crewai.com/) | CrewAI | Official guides for agents, crews, tasks, tools, flows, memory, guardrails, and human-in-the-loop workflows. |

## Agentic AI Courses

These courses provide structured learning paths for Agentic AI, AI agent development, multi-agent systems, Agentic RAG, memory, MCP, and production engineering.

| Course | Provider | Coverage |
| --- | --- | --- |
| [Agentic AI](https://www.deeplearning.ai/courses/agentic-ai) | DeepLearning.AI | Intermediate course by Andrew Ng covering reflection, tool use, planning, multi-agent workflows, evaluation, and production deployment. |
| [Agents Course](https://huggingface.co/learn/agents-course/unit0/introduction) | Hugging Face | Structured course covering agent fundamentals, smolagents, LlamaIndex, LangGraph, use cases, evaluation, and a final assignment. |
| [5-Day AI Agents Intensive](https://www.kaggle.com/learn-guide/5-day-agents) | Google + Kaggle | Agent architectures, tools, memory, evaluation, multi-agent systems, and moving prototypes toward production. |
| [5-Day AI Agents: Intensive Vibe Coding](https://www.kaggle.com/learn-guide/5-day-agents-vibecoding) | Google + Kaggle | 2026 course materials covering ADK, MCP, agent skills, security, interoperability, evaluation, and production agent development. |
| [AI Agents for Beginners](https://github.com/microsoft/ai-agents-for-beginners) | Microsoft | Open GitHub curriculum with written lessons, videos, code samples, design patterns, framework concepts, production deployment, and agent security. |
| [Introduction to LangChain: Build AI Agents with Python](https://academy.langchain.com/courses/foundation-introduction-to-langchain-python) | LangChain Academy | Agent fundamentals, tools, short-term memory, MCP, context, multi-agent systems, human-in-the-loop, middleware, and hands-on projects. |
| [Introduction to LangGraph - Python](https://academy.langchain.com/courses/intro-to-langgraph) | LangChain Academy | Free structured course covering graphs, state, memory, routing, human-in-the-loop, long-term memory, research assistants, and deployment. |
| [AI Agents in LangGraph](https://www.deeplearning.ai/courses/ai-agents-in-langgraph) | DeepLearning.AI | Build an agent from scratch and with LangGraph, then add persistence, search, and human-in-the-loop control. |
| [Multi AI Agent Systems with crewAI](https://www.deeplearning.ai/courses/multi-ai-agent-systems-with-crewai) | DeepLearning.AI | Hands-on introduction to role-based agents, tools, memory, guardrails, cooperation, and multi-agent business workflows. |
| [Building Agentic RAG with LlamaIndex](https://www.deeplearning.ai/courses/building-agentic-rag-with-llamaindex) | DeepLearning.AI | Router agents, tool calling, reasoning loops, research assistants, and multi-document agentic retrieval. |
| [MCP: Build Rich-Context AI Apps with Anthropic](https://www.deeplearning.ai/courses/mcp-build-rich-context-ai-apps-with-anthropic) | DeepLearning.AI + Anthropic | MCP architecture, servers, clients, tools, resources, prompts, remote deployment, and integrations. |
| [Agent Memory: Building Memory-Aware Agents](https://www.deeplearning.ai/courses/agent-memory-building-memory-aware-agents) | DeepLearning.AI + Oracle | Persistent memory architecture, memory managers, semantic tool retrieval, extraction, consolidation, and self-updating memory. |
| [Event-Driven Agentic Document Workflows](https://www.deeplearning.ai/courses/event-driven-agentic-document-workflows) | DeepLearning.AI + LlamaIndex | Event-driven workflows, branching, concurrency, RAG, structured outputs, and human feedback. |
| [AI Agentic Design Patterns with AutoGen](https://www.deeplearning.ai/courses/ai-agentic-design-patterns-with-autogen) | DeepLearning.AI | Useful for learning reflection, tool use, planning, and multi-agent design patterns through AutoGen; treat it as framework-specific rather than the current Microsoft production path. |
| [Agentic AI Course](https://www.mygreatlearning.com/iit-bombay-certificate-in-agentic-ai) | IIT Bombay, in collaboration with Great Learning | Five-month online certificate covering Agentic AI concepts and hands-on topics including RAG, MCP, LangGraph, CrewAI, multi-agent systems, evaluation, security, and deployment. |

## Agentic AI Projects and Hands-On Tutorials

Use these resources when you want to build rather than only read.

| Project / Tutorial | What you build or learn |
| --- | --- |
| [Build Your First Agent with smolagents](https://huggingface.co/learn/agents-course/unit1/tutorial) | Build and run a tool-using agent, then understand how its reasoning/action loop works. |
| [OpenAI Agents SDK Quickstart](https://openai.github.io/openai-agents-python/quickstart/) | Create a first agent, add tools, introduce handoffs, and inspect traces. |
| [OpenAI Human Approval Flow](https://openai.github.io/openai-agents-python/human_in_the_loop/) | Pause an agent before a sensitive action, approve or reject the action, and resume the run. |
| [OpenAI Multi-Agent Examples](https://openai.github.io/openai-agents-python/examples/) | Explore routing, manager-style orchestration, agents-as-tools, parallel agents, and other official patterns. |
| [Google ADK Python Quickstart](https://adk.dev/get-started/python/) | Create an ADK project, define an agent, run it locally, and inspect its behavior. |
| [Google ADK Foundation Codelab](https://codelabs.developers.google.com/devsite/codelabs/build-agents-with-adk-foundation) | Build a complete starter agent through a guided codelab. |
| [Google Tools Make an Agent Codelab](https://codelabs.developers.google.com/codelabs/cloud-run/tools-make-an-agent) | Build an assistant and add function tools, search, external tools, subagents, and MCP. |
| [LangChain SQL Agent](https://docs.langchain.com/oss/python/langchain/sql-agent) | Build a database agent that discovers schemas, generates SQL, handles failures, and supports human review. |
| [LangGraph Agentic RAG](https://docs.langchain.com/oss/python/langgraph/agentic-rag) | Build retrieval logic that can decide whether to retrieve, grade results, rewrite queries, and continue. |
| [Thinking in LangGraph: Customer Support Email Agent](https://docs.langchain.com/oss/python/langgraph/thinking-in-langgraph) | Model a real email-support workflow with classification, retrieval, drafting, retries, and escalation. |
| [Build an MCP Server](https://modelcontextprotocol.io/docs/develop/build-server) | Expose structured tools through a standards-based MCP server. |
| [Build an MCP Client](https://modelcontextprotocol.io/docs/develop/build-client) | Build an AI application that connects to MCP servers, discovers tools, and executes them. |
| [Microsoft Agent Framework Get Started](https://learn.microsoft.com/en-us/agent-framework/get-started/) | Build progressively from a first agent through tools, sessions, memory, workflows, and hosting. |
| [CrewAI Quickstart](https://docs.crewai.com/en/quickstart) | Create agents, tasks, and a crew, then execute a coordinated multi-agent workflow. |

## Roadmaps and Reference Guides

| Roadmap / Reference | Why use it |
| --- | --- |
| [Titan Codes Agentic AI Developer Roadmap](#titan-codes-agentic-ai-developer-roadmap) | Original progression in this repository from LLM fundamentals through tools, RAG, memory, MCP/A2A, evaluation, security, observability, and production. |
| [Titan Codes Production-Ready AI Agent Checklist](#production-readiness-checklist) | Original checklist covering scope, tools, security, human oversight, reliability, evaluation, and observability. |
| [Microsoft Agent Framework Development Journey](https://learn.microsoft.com/en-us/agent-framework/journey/) | Progressive guide from model fundamentals to tools, context, memory, middleware, skills, and agent composition. |
| [Microsoft AI Agents for Beginners Study Guide](https://github.com/microsoft/ai-agents-for-beginners/blob/main/STUDY_GUIDE.md) | Concise reference for agent fundamentals, components, patterns, and implementation concepts. |
| [LangChain Learn](https://docs.langchain.com/oss/python/learn) | Structured entry point for agents, RAG, SQL, multi-agent systems, Deep Agents, and production patterns. |
| [Hugging Face Agents Course Syllabus](https://huggingface.co/agents-course) | Learning sequence from agent fundamentals through frameworks, use cases, evaluation, and a final agent project. |
| [Anthropic Building Effective Agents](https://www.anthropic.com/engineering/building-effective-agents) | Architecture reference for choosing simple workflows, composable patterns, or autonomous agents. |
| [OpenAI Practical Guide to Building Agents](https://openai.com/business/guides-and-resources/a-practical-guide-to-building-ai-agents/) | Reference for identifying agent use cases and designing models, tools, instructions, orchestration, and guardrails. |

## Books

| Book | Author(s) | Why include it |
| --- | --- | --- |
| [AI Agents in Action, Second Edition](https://www.manning.com/books/ai-agents-in-action-second-edition) | Micheal Lanham | Practical 2026 guide covering agent design, MCP, A2A, tools, memory, reasoning, multi-agent systems, evaluation, observability, and deployment. |
| [AI Engineering: Building Applications with Foundation Models](https://www.oreilly.com/library/view/ai-engineering/9781098166298/) | Chip Huyen | Broader production AI engineering reference covering models, evaluation, RAG, agents, latency, cost, and application design. |
| [Building AI Agents with LLMs, RAG, and Knowledge Graphs](https://www.oreilly.com/library/view/building-ai-agents/9781835087060/) | Salvatore Raieli and Gabriele Iuculano | Technical guide combining LLMs, RAG, knowledge graphs, reasoning, and practical agent development. |
| [Generative AI with LangChain, Second Edition](https://www.packtpub.com/en-us/product/generative-ai-with-langchain-9781837022014) | Ben Auffarth | Updated treatment of LangGraph workflows, multi-agent systems, RAG, evaluation, testing, observability, and production practices. |

## Selected Videos

| Video / Session | Publisher | Focus |
| --- | --- | --- |
| [Build Hour: Agents SDK](https://www.youtube.com/watch?v=tK32trvj_b4) | OpenAI | 2026 walkthrough of long-running agents, tools, memory, MCP, skills, shell execution, and sandboxing. |
| [Getting Started with Agent Development Kit](https://www.youtube.com/watch?v=44C8u0CDtSo) | Google for Developers | Introduction to agent definitions, runners, services, loop agents, local debugging, and ADK execution. |
| [Python + Agents: Building Your First Agent in Python](https://www.youtube.com/watch?v=I4vCp9cpsiI) | Microsoft Reactor | Agent anatomy, tool calling, MCP server integration, middleware, and supervisor-agent patterns. |
| [Orchestrate Your Agents with Microsoft Agent Framework](https://learn.microsoft.com/en-us/shows/azure-friday/orchestrate-your-agents-with-microsoft-agent-framework) | Microsoft Azure Friday | Practical multi-agent orchestration demonstration with checkpointing and human-in-the-loop capabilities. |
| [Building More Effective AI Agents](https://www.youtube.com/watch?v=uhJJgc-0iTQ) | Anthropic | Discussion of simple architectures, multi-agent patterns, tools, MCP, context engineering, failure modes, and practical advice. |

---

# Core Agentic AI Concepts and Patterns

## Augmented LLM

An LLM becomes more useful for real-world tasks when it is connected to capabilities such as retrieval, tools, memory, code execution, and external systems.

## Routing

A routing step classifies a request and directs it to the most appropriate model, tool, workflow, or specialist agent.

## Sequential Workflows

A task is broken into ordered stages where the output of one stage becomes the input to the next.

## Parallelization

Independent subtasks are executed concurrently and their results are combined. This is useful for research, verification, comparison, and multi-perspective analysis.

## Planner-Executor

A planner decomposes an objective into steps while one or more executors carry out those steps. The plan can be revised as new information becomes available.

## ReAct

Reasoning and acting are interleaved so an agent can select an action, observe the result, and use that observation to determine the next step.

## Reflection

The system critiques or reviews an intermediate result and uses that feedback to improve a later attempt.

## Evaluator-Optimizer

One component generates a result while another evaluates it against explicit criteria. The cycle continues until an acceptable result is produced or a stopping condition is reached.

## Supervisor and Specialist Agents

A coordinating agent delegates work to specialized agents and combines their results while retaining control of the overall task.

## Agents as Tools

A coordinating agent can call specialist agents through tool-like interfaces. This often preserves clearer control than unrestricted peer-to-peer agent conversation.

## Handoffs

Responsibility moves from one agent to another when the second agent is better suited to continue the task.

## Human in the Loop

A human reviews, approves, modifies, or rejects actions at important control points, especially before irreversible, sensitive, expensive, or high-impact operations.

---

# Agentic AI Frameworks and SDKs

- [AutoGen](https://github.com/microsoft/autogen) - Microsoft's open-source framework for conversational and multi-agent applications. Useful for studying established multi-agent patterns; for new Microsoft production projects, also review Microsoft Agent Framework.
- [CrewAI](https://github.com/crewAIInc/crewAI) - Framework for orchestrating role-based AI agents, crews, tools, tasks, and multi-agent workflows.
- [Google Agent Development Kit (ADK)](https://github.com/google/adk-python) - Google's code-first toolkit for building modular agents, tools, workflows, sessions, evaluation flows, and multi-agent systems.
- [Haystack](https://github.com/deepset-ai/haystack) - Open-source AI orchestration framework for agents, retrieval-augmented generation, pipelines, and production AI applications.
- [LangGraph](https://github.com/langchain-ai/langgraph) - Low-level orchestration framework for stateful, controllable, and long-running agent workflows with durable execution and human-in-the-loop patterns.
- [LlamaIndex](https://github.com/run-llama/llama_index) - Data and workflow framework with agents, retrieval, tools, structured workflows, and multi-agent capabilities.
- [Microsoft Agent Framework](https://github.com/microsoft/agent-framework) - Microsoft framework for building, orchestrating, and deploying production-grade agents and multi-agent workflows.
- [OpenAI Agents SDK](https://github.com/openai/openai-agents-python) - Lightweight SDK for agents, tools, handoffs, guardrails, sessions, tracing, human approval, and multi-agent orchestration.
- [Pydantic AI](https://github.com/pydantic/pydantic-ai) - Typed Python framework for building agents with structured data, tools, model flexibility, evaluation, and production integrations.
- [smolagents](https://github.com/huggingface/smolagents) - Hugging Face library for lightweight tool-calling and code-based agents with support for multiple model providers.

# How to Choose an Agentic AI Framework

There is no single best framework for every agentic application. Start with the control model and operational requirements of your use case.

| Framework | Consider it when you need |
| --- | --- |
| **OpenAI Agents SDK** | Lightweight primitives, tools, handoffs, guardrails, sessions, tracing, human approval, and OpenAI-native agent development |
| **Google ADK** | Code-first Google ecosystem development, tool integrations, sessions, evaluation, deployment, and multi-agent composition |
| **Microsoft Agent Framework** | Microsoft ecosystem integration, Python/.NET development, workflows, checkpointing, orchestration, and enterprise deployment |
| **LangGraph** | Fine-grained state machines, durable execution, explicit workflow control, long-running agents, and human-in-the-loop |
| **CrewAI** | Role-oriented agents, crews, task delegation, and business-process-style multi-agent workflows |
| **Pydantic AI** | Strong typing, structured data, validation, model flexibility, and Python-first development |
| **LlamaIndex** | Data-centric agents, RAG, knowledge workflows, document retrieval, and agentic data applications |
| **Haystack** | Production-oriented AI pipelines, agents, retrieval, and modular orchestration |
| **smolagents** | Lightweight experimentation, tool-calling agents, code agents, and Hugging Face ecosystem integration |
| **AutoGen** | Studying and implementing established conversational multi-agent patterns, especially in existing AutoGen projects |

Before adopting a framework, evaluate:

- Control over agent state and execution.
- Model-provider flexibility.
- Tool and MCP support.
- Memory and persistence.
- Multi-agent orchestration.
- Human-in-the-loop capabilities.
- Evaluation support.
- Tracing and observability.
- Deployment model.
- Security boundaries.
- Community activity and maintenance.
- Ease of testing and debugging.
### Further Reading

- [Best AI Agent Frameworks in 2026: Production Comparison, Costs, and How to Choose](https://titancodes.com/blog/best-ai-agent-frameworks/) - A detailed comparison of leading AI agent frameworks based on workflow control, state management, human-in-the-loop support, observability, MCP integration, model flexibility, and production fit.
---

# Protocols and Interoperability

- [Agent2Agent Protocol (A2A)](https://github.com/a2aproject/A2A) - Open protocol for communication and interoperability between independent agentic applications.
- [Model Context Protocol (MCP)](https://modelcontextprotocol.io/) - Open protocol for connecting AI applications to tools, data sources, prompts, and external capabilities.

## MCP Ecosystem

- [Model Context Protocol](https://modelcontextprotocol.io/) - Open protocol for connecting AI applications to tools, data sources, prompts, and external capabilities.
- [MCP Specification](https://modelcontextprotocol.io/specification/) - Official protocol specification and versioned technical documentation.
- [MCP Inspector](https://github.com/modelcontextprotocol/inspector) - Developer tool for testing and inspecting MCP servers.
- [MCP Reference Servers](https://github.com/modelcontextprotocol/servers) - Reference implementations and examples for MCP integrations.
- [GitHub MCP Server](https://github.com/github/github-mcp-server) - Official GitHub MCP server for connecting agents to repositories, issues, pull requests, and GitHub workflows.
- [Playwright MCP](https://github.com/microsoft/playwright-mcp) - MCP server that exposes browser automation capabilities through Playwright.

# Tool Use and MCP

Good agent tools should have narrow responsibilities, clear schemas, predictable error behavior, useful descriptions, and outputs that give the model enough information without unnecessary context.

When designing tools, consider:

- Clear tool names and descriptions.
- Strong input validation.
- Structured outputs where practical.
- Authentication and authorization outside the model.
- Least-privilege access.
- Timeouts and bounded retries.
- Idempotency for actions that may be retried.
- Explicit and useful error responses.
- Rate limits, quotas, and spend controls.
- Human approval for consequential actions.
- Audit logs for tool execution.
- Protection against untrusted tool output and prompt injection.

Recommended guides:

- [Anthropic: Writing Effective Tools for AI Agents](https://www.anthropic.com/engineering/writing-tools-for-agents)
- [OpenAI Agents SDK: Tools](https://openai.github.io/openai-agents-python/tools/)
- [Build Your First MCP Server](https://modelcontextprotocol.io/docs/develop/build-server)
- [Build an MCP Client](https://modelcontextprotocol.io/docs/develop/build-client)

---

# Retrieval, RAG, and Memory

Retrieval and memory solve different problems. **Retrieval** supplies relevant external knowledge for the current task, while **memory** preserves useful state or information across steps or sessions.

## Memory and Retrieval Infrastructure

- [Mem0](https://github.com/mem0ai/mem0) - Memory layer for AI applications and agents with support for persistent user and application context.
- [Chroma](https://github.com/chroma-core/chroma) - Open-source embedding database commonly used for retrieval and AI applications.
- [Milvus](https://github.com/milvus-io/milvus) - Distributed vector database for large-scale similarity search.
- [pgvector](https://github.com/pgvector/pgvector) - Vector similarity search extension for PostgreSQL.
- [Qdrant](https://github.com/qdrant/qdrant) - Vector database and similarity search engine for retrieval systems.
- [Weaviate](https://github.com/weaviate/weaviate) - Open-source vector database for semantic search and AI applications.

## Agentic Retrieval Patterns

Common Agentic RAG patterns include:

- Query rewriting.
- Multi-query retrieval.
- Tool-selected retrieval.
- Retrieval planning.
- Corrective retrieval.
- Iterative search.
- Source verification.
- Retrieval followed by critique.
- Knowledge-graph-assisted retrieval.
- Hybrid lexical and semantic retrieval.

Useful tutorials:

- [LangGraph: Build a Custom Agentic RAG System](https://docs.langchain.com/oss/python/langgraph/agentic-rag)
- [DeepLearning.AI: Building Agentic RAG with LlamaIndex](https://www.deeplearning.ai/courses/building-agentic-rag-with-llamaindex)
- [DeepLearning.AI: Agent Memory - Building Memory-Aware Agents](https://www.deeplearning.ai/courses/agent-memory-building-memory-aware-agents)

---

# Agent Evaluation and Testing

Agent evaluation should go beyond checking the final response. Mature evaluation also examines **what the agent did**, **which tools it used**, **whether the environment actually changed as intended**, and **whether the behavior remains reliable across updates**.

Useful dimensions include:

- Task completion.
- Final outcome correctness.
- Tool selection.
- Tool argument quality.
- Tool response handling.
- Trajectory quality.
- Number of steps.
- Groundedness.
- Hallucination.
- Safety and policy compliance.
- Recovery from tool failures.
- Human intervention rate.
- Latency.
- Token usage.
- Cost.

## Evaluation Frameworks

- [Arize Phoenix](https://github.com/Arize-ai/phoenix) - Open-source platform for tracing, datasets, experiments, evaluation, and debugging AI applications.
- [DeepEval](https://github.com/confident-ai/deepeval) - Open-source evaluation framework for LLM applications and agents with task, hallucination, relevance, safety, and custom metrics.
- [Pydantic Evals](https://ai.pydantic.dev/evals/) - Evaluation tooling integrated with the Pydantic AI ecosystem.
- [promptfoo](https://github.com/promptfoo/promptfoo) - Testing and red-teaming framework for prompts, models, RAG systems, and AI agents.
- [Ragas](https://github.com/explodinggradients/ragas) - Evaluation framework for retrieval-augmented generation and AI application quality.

## Evaluation Guidance

- [Anthropic: Demystifying Evals for AI Agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents)
- [OpenAI Agents SDK Examples](https://openai.github.io/openai-agents-python/examples/)
- [Microsoft AI Agents for Beginners](https://github.com/microsoft/ai-agents-for-beginners)

A useful starting evaluation suite should include:

1. Representative normal tasks.
2. Known historical failure cases.
3. Tool-error scenarios.
4. Ambiguous instructions.
5. Adversarial or prompt-injection attempts.
6. Tasks requiring safe refusal or escalation.
7. Long-running tasks that stress memory and state.
8. Regression tests for every serious production incident.

---

# Observability and Tracing

An agent trace should make it possible to answer:

- Which model was called?
- Which instructions and context were supplied?
- Which tools were available?
- Which tool was selected?
- What arguments were generated?
- What did the tool return?
- Which agent or workflow step ran next?
- Which handoffs occurred?
- How long did each step take?
- How many tokens were used?
- What did the run cost?
- Where did the run fail?
- What changed between successful and failed runs?

## Observability Tools

- [Arize Phoenix](https://github.com/Arize-ai/phoenix) - Open-source tracing and evaluation platform for AI application observability.
- [Langfuse](https://github.com/langfuse/langfuse) - Open-source platform for LLM tracing, prompt management, evaluation, cost analysis, and production monitoring.
- [OpenInference](https://github.com/Arize-ai/openinference) - OpenTelemetry-based semantic conventions and instrumentation for AI application tracing.
- [OpenTelemetry](https://opentelemetry.io/) - Vendor-neutral observability framework for traces, metrics, and logs.
- [Opik](https://github.com/comet-ml/opik) - Open-source evaluation and observability platform for LLM and agent applications.

---

# Guardrails, Security, and Human Oversight

Agentic applications expand the attack surface because models can interact with untrusted content and may be able to take actions through tools.

Important controls include:

- Input validation.
- Output validation.
- Prompt-injection defenses.
- Data access controls.
- Tool allowlists.
- Least-privilege permissions.
- Scoped credentials.
- Secrets isolation.
- Sandboxed execution.
- Network restrictions.
- Human approval gates.
- Spend and rate limits.
- Action previews.
- Audit trails.
- PII detection and redaction.
- Safe retry behavior.
- Kill switches and cancellation.
- Clear boundaries for irreversible operations.

## Security Resources

- [garak](https://github.com/NVIDIA/garak) - LLM vulnerability scanner for probing weaknesses and undesirable model behavior.
- [Guardrails AI](https://github.com/guardrails-ai/guardrails) - Framework for validating and controlling model inputs and outputs.
- [Microsoft Presidio](https://github.com/microsoft/presidio) - Open-source tools for detecting and anonymizing sensitive information.
- [NeMo Guardrails](https://github.com/NVIDIA-NeMo/Guardrails) - NVIDIA framework for programmable safety and control rails around generative AI applications.
- [OWASP GenAI Security Project](https://genai.owasp.org/) - Community security guidance and risk resources for generative AI and agentic systems.
- [PyRIT](https://github.com/Azure/PyRIT) - Microsoft's open-source framework for identifying and assessing risks in generative AI systems.
- [promptfoo Red Teaming](https://github.com/promptfoo/promptfoo) - Automated testing and red-teaming workflows for AI applications.

## Human Approval

Human approval is especially important before:

- Sending messages or emails.
- Publishing content.
- Deleting or overwriting data.
- Spending money.
- Executing financial transactions.
- Changing permissions.
- Deploying code.
- Running destructive database operations.
- Accessing highly sensitive information.
- Taking actions that cannot be reliably reversed.

---

# Sandboxes and Computer Use

Agents that execute code, manipulate files, use shells, or control browsers should run inside constrained environments whenever practical.

- [browser-use](https://github.com/browser-use/browser-use) - Open-source tooling for browser-based agent workflows.
- [Docker](https://docs.docker.com/) - Container platform commonly used to isolate agent execution environments.
- [E2B](https://github.com/e2b-dev/E2B) - Isolated cloud sandboxes designed for AI-generated code and agent workloads.
- [Playwright](https://github.com/microsoft/playwright) - Browser automation framework useful for controlled web interaction and testing.
- [Playwright MCP](https://github.com/microsoft/playwright-mcp) - MCP integration that exposes browser automation capabilities to agents.

Recommended controls include:

- Ephemeral environments.
- Restricted filesystem access.
- Network allowlists.
- CPU, memory, and execution limits.
- Secret isolation.
- Non-root execution.
- Timeouts.
- Process cleanup.
- Logging.
- Human approval before sensitive external actions.

---

# Research Papers

- [ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/abs/2210.03629) - Introduces the ReAct pattern that interleaves reasoning, actions, and observations.
- [Toolformer: Language Models Can Teach Themselves to Use Tools](https://arxiv.org/abs/2302.04761) - Explores self-supervised learning of external tool use.
- [Gorilla: Large Language Model Connected with Massive APIs](https://arxiv.org/abs/2305.15334) - Studies API selection and reliable tool use by language models.
- [Reflexion: Language Agents with Verbal Reinforcement Learning](https://arxiv.org/abs/2303.11366) - Uses linguistic feedback and memory to improve later attempts.
- [CAMEL: Communicative Agents for Mind Exploration of Large Scale Language Model Society](https://arxiv.org/abs/2303.17760) - Explores role-playing and communication between language-model agents.
- [AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation](https://arxiv.org/abs/2308.08155) - Presents patterns for conversational multi-agent applications.
- [MetaGPT: Meta Programming for Multi-Agent Collaborative Framework](https://arxiv.org/abs/2308.00352) - Applies structured roles and workflows to collaborative software-engineering agents.
- [Generative Agents: Interactive Simulacra of Human Behavior](https://arxiv.org/abs/2304.03442) - Introduces memory, reflection, and planning mechanisms for interactive agents.
- [Voyager: An Open-Ended Embodied Agent with Large Language Models](https://arxiv.org/abs/2305.16291) - Demonstrates long-horizon learning with an automatic curriculum and reusable skills.
- [WebArena: A Realistic Web Environment for Building Autonomous Agents](https://arxiv.org/abs/2307.13854) - Introduces realistic web environments for evaluating autonomous agents.

---

# Agent Benchmarks

- [AgentBench](https://github.com/THUDM/AgentBench) - Benchmark suite for evaluating language models as agents across multiple interactive environments.
- [GAIA](https://huggingface.co/gaia-benchmark) - General AI assistant benchmark designed around real-world questions that require reasoning, tools, and multiple steps.
- [OSWorld](https://github.com/xlang-ai/OSWorld) - Benchmark environment for multimodal agents that operate real computer applications and operating-system interfaces.
- [SWE-bench](https://github.com/SWE-bench/SWE-bench) - Benchmark for evaluating systems on real software-engineering issues from GitHub repositories.
- [τ-bench](https://github.com/sierra-research/tau-bench) - Benchmark for evaluating tool-using agents in realistic user-facing scenarios.
- [WebArena](https://github.com/web-arena-x/webarena) - Web environment and benchmark for testing autonomous agents on realistic websites.

Benchmarks are useful reference points, but a production agent should also be evaluated against **your own representative tasks, failure modes, policies, tools, and operating environment**.

---

# Production Readiness Checklist

Before giving an agent access to real users, sensitive data, or consequential actions, review the following.

## Scope and Behavior

- [ ] The agent has a clearly defined objective and operating boundary.
- [ ] Expected success criteria are measurable.
- [ ] The system knows when to stop, ask for clarification, or escalate.
- [ ] The agent is not being used where a deterministic workflow would be safer and sufficient.
- [ ] High-risk or irreversible capabilities are explicitly identified.

## Tools

- [ ] Tool descriptions are clear and tested with the target models.
- [ ] Tool inputs are validated.
- [ ] Tool outputs are structured and bounded.
- [ ] Tools use least-privilege credentials.
- [ ] Destructive actions have additional controls.
- [ ] Retries cannot accidentally duplicate irreversible actions.
- [ ] Tool failures return useful errors to the agent.
- [ ] Rate limits and quotas are defined.

## Security

- [ ] Secrets are never placed directly in prompts.
- [ ] Untrusted retrieved content is treated as untrusted data.
- [ ] Prompt-injection scenarios have been tested.
- [ ] Sensitive data is detected and protected.
- [ ] Code or shell execution is sandboxed.
- [ ] Network and filesystem access are restricted where possible.
- [ ] Authentication and authorization are enforced outside the model.
- [ ] Tool permissions are scoped to the minimum required access.
- [ ] External links and third-party integrations have been reviewed.

## Human Oversight

- [ ] High-impact actions have explicit approval points.
- [ ] Users can preview consequential actions.
- [ ] Users can cancel or stop long-running operations.
- [ ] Escalation paths exist for ambiguous or failed tasks.
- [ ] Approval decisions are logged.

## Evaluation

- [ ] A representative evaluation dataset exists.
- [ ] The agent is tested for task success, not only response quality.
- [ ] Tool selection and tool arguments are evaluated.
- [ ] Regression evaluations run after meaningful changes.
- [ ] Known failure cases are preserved as tests.
- [ ] Safety and adversarial tests are included.
- [ ] Evaluation results are tracked across model or prompt changes.

## Reliability

- [ ] Timeouts are defined.
- [ ] Retry behavior is bounded.
- [ ] Long-running tasks can recover from partial failure.
- [ ] State transitions are understandable and auditable.
- [ ] External service failures have fallbacks or safe failure modes.
- [ ] Repeated tool calls cannot create accidental duplicate side effects.
- [ ] Cancellation and cleanup behavior have been tested.

## Observability

- [ ] Model calls are traced.
- [ ] Tool calls are traced.
- [ ] Agent handoffs and workflow transitions are visible.
- [ ] Token usage and cost are monitored.
- [ ] Latency is monitored by step.
- [ ] Errors can be tied back to a specific run.
- [ ] Sensitive information is redacted from telemetry where required.

---

# Contributing

Contributions are welcome. Please read [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.

All contributions are reviewed before they are merged. If you find a broken link, outdated resource, or project that no longer meets the inclusion criteria, please open an issue using the repository templates.

For security vulnerabilities, follow [SECURITY.md](SECURITY.md) instead of opening a public issue.

# Maintainers

This resource is maintained by [Titan Codes](https://titancodes.com/).

The goal is to keep this repository technically useful, vendor-neutral, and community-driven. Inclusion does not imply endorsement, partnership, sponsorship, or a commercial relationship unless explicitly stated.
