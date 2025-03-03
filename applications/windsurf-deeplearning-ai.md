# Build Apps with Windsurf’s AI Coding Agents

- [Course Link](https://www.deeplearning.ai/short-courses/build-apps-with-windsurfs-ai-coding-agents/)

- The course is divided into 2 parts:
    - Part 1: Is around the architecture of Windsurf and what a coding IDE needs to be as good as a pair programmer.
    - Part 2: Is a sample project showing Windsurf's capabilities.

- Windsurf's Cursor Composer equivalent is called "Cascade (Writer mode)".

- Part 1:
    - Windsurf is explicitly designed to work with a human-in-the-loop
        - What this means is that the IDE is aware of your changes and actions as you type and can immediately pull them to fulfil the next task.
        - The human can accept, reject, revert to last state of each agent action.
        - Controlling the IDE helps control this entire pair programming experience vs just a VS code extension.
    - A coding IDE needs 3 things to be efficient
        - Context - What data is relevant to the user's task? (RAG, Web Search)
        - Tools - grep, ls, sed etc. to achieve the user's task.
        - Reasoning models - Take in context to generate code and decide what tools to call.
        - Reasoning model is the same across most coding IDEs, so context and tools will help differentiate them.
    - Context
        - Plain RAG retrieval is not that effective.
        - Most embedding models have a needle in the haystack metric.
        - However, what matters is not just finding the needle in the haystack but getting top-K results and user continuously using the pulled context in the task i.e. subsequent hits as well.
            - Hence, existing embedding model benchmarks don't work.
        - Pulling immediate files is counterintuively better than adding other context from the web (libraries) and simple RAG.
            - Context is polluted.
        - Windsurf innovation
            - Instead Windsurf looked at Github PRS, took the commit message and the individuals diff in the PRs to train a new model that goes from task to the diffs generated. This represents real world usage.
            - They also don't use simple RAG for retrieval.
                - Send all files to an LLM and ask "how relevant is this file to the user's query?"

- Part 2:
    - This just shows how to use Windsurf, not to different from Cursor's composer, chat and in-line chat mode.
