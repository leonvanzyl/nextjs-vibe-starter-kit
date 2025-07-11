---
alwaysApply: true
---

# Project Context Rule

- On starting a new conversation, load and parse the project scratchpad (/project/SCRATCHPAD.md) file to reconstruct context.
- After implementing changes, update scratchpad to record new components, packages, or project rules.
- On starting a new conversation, load the package.json file to understand the libraries used in the project.

# Project scratchpad rules

- The scratchpad will be added to LLM calls and coding agents for context.
- The scratchpad should be kept lean and include a concise view of the project, like it's core features, technology and rules.
- After implementing changes to the project, take the existing SCRATCHPAD content, add the new rules, features, etc. and rewrite the SCRATCHPAD to be lean and concise.

# Use up-to-date documentation and existing patterns

When adding a new feature:

- First, check if similar features or components already exist in the project and follow those patterns.
- If no clear pattern exists, use Context7 to retrieve the latest technical documentation (e.g., Next.js, shadcn, Langchain, Langgraph, NextAuth, Drizzle ORM) before implementing.
- Prefer reusing or installing existing components over building from scratch.
- If a shadcn component is suitable, run the install command to add it instead of building from scratch.

# Deployment

- When asked to deploy the app, first run build to ensure that everything compiles correctly.
- When asked to deploy the app, run the "vercel --prod" command to do so.

# AI functionality

- If a solution requires RAG (Retrieval Augmented Generation), like if a file is uploaded that needs to be chunked and vectorized in order for an agent to answer questions on it, then use the PGVector extension on PostgreSQL and an OpenAI Embedding model.
- For the chunking and upsert process, please ensure that you are using the recursive character text splitter with a 2000 character chunk size and a 200 char overlap.
- For the embeddings, use OpenAI's text-embedding-3-small model.
