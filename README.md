# sample
sample
Yes, for all three. Each agent reaches its tools only through AgentCore Gateway, every tool is read-only, and none of them can write to GitHub or anywhere else.

**Agent 1: Sizing Agent**
Yes. It uses the models on Amazon Bedrock and two read-only tools through AgentCore Gateway: reading the run's copy of the reference application, and searching BMO coding standards in the Bedrock knowledge base. It cannot write to GitHub or any other system.

**Agent 2: Generation Agent**
Yes. It uses the models on Amazon Bedrock and three read-only tools through AgentCore Gateway: reading the target GitHub repository, reading the run's copy of the reference application, and searching BMO coding standards in the Bedrock knowledge base. It cannot write to GitHub or any other system; the code reaches GitHub only as a pull request opened by the application, not by the agent.

**Agent 3: Grading Agent**
Yes. It uses the models on Amazon Bedrock and two read-only tools through AgentCore Gateway: reading the run's copy of the reference application, and searching BMO coding standards in the Bedrock knowledge base. For the end-to-end review, it reads the run's generated files from its own task input. It cannot write to GitHub or any other system.
