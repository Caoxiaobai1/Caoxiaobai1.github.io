title: Claude Code官网教程
date: 2025-01-24 17:49:32
cover: covers\fll.jpg
tags: Claude
categories: 编程
mermaid: true

---

# Claude Code官网教程

# Claude Code 概述

了解 Claude Code，Anthropic 的智能编程工具，它在您的终端中运行，帮助您比以往任何时候都更快地将想法转化为代码。

## 30 秒快速开始

前提条件：[**Node.js 18 或更新版本**](https://nodejs.org/en/download/)

```shell
# 安装 Claude Code
npm install -g @anthropic-ai/claude-code

# 导航到您的项目
cd your-awesome-project

# 开始使用 Claude 编程
claude
```

## Claude Code 为您做什么

*   从描述构建功能：用简单的英语告诉 Claude 您想要构建什么。它会制定计划、编写代码并确保其正常工作。
    
*   调试和修复问题：描述一个错误或粘贴错误消息。Claude Code 将分析您的代码库，识别问题并实施修复。
    
*   导航任何代码库：询问有关您团队代码库的任何问题，并获得深思熟虑的答案。Claude Code 保持对您整个项目结构的感知，可以从网络上找到最新信息，并且通过 MCP 可以从 Google Drive、Figma 和 Slack 等外部数据源获取信息。
    
*   自动化繁琐任务：修复复杂的 lint 问题、解决合并冲突并编写发布说明。在您的开发机器上通过单个命令完成所有这些，或在 CI 中自动完成。
    

## 为什么开发者喜爱 Claude Code

*   在您的终端中工作：不是另一个聊天窗口。不是另一个 IDE。Claude Code 在您已经工作的地方与您相遇，使用您已经喜爱的工具。
    
*   采取行动：Claude Code 可以直接编辑文件、运行命令并创建提交。需要更多功能？MCP 让 Claude 读取您在 Google Drive 中的设计文档、更新您在 Jira 中的工单，或使用\_您的\_自定义开发工具。
    
*   Unix 哲学：Claude Code 是可组合和可脚本化的。tail -f app.log | claude -p "如果您在此日志流中看到任何异常，请通过 Slack 通知我" 有效。您的 CI 可以运行 claude -p "如果有新的文本字符串，将它们翻译成法语并为 @lang-fr-team 提出 PR 进行审查"。
    
*   企业就绪：使用 Anthropic 的 API，或在 AWS 或 GCP 上托管。企业级安全性、隐私和合规性是内置的。
    

# 快速开始

欢迎使用 Claude Code！

这个快速开始指南将让您在几分钟内使用AI驱动的编程辅助。完成后，您将了解如何使用 Claude Code 进行常见的开发任务。

## 开始之前

确保您已经：

*   [**安装了 Claude Code**](https://docs.anthropic.com/zh-CN/docs/claude-code/setup)
    
*   打开了终端或命令提示符
    
*   有一个代码项目可以使用
    

## 步骤 1：开始您的第一个会话

在任何项目目录中打开终端并启动 Claude Code：

```bash
cd /path/to/your/project
claude

```

您将在新的交互式会话中看到 Claude Code 提示符：

```plaintext
✻ Welcome to Claude Code!

...

> Try "create a util logging.py that..." 

```

## 步骤 2：提出您的第一个问题

让我们从了解您的代码库开始。尝试以下命令之一：

```plaintext
> what does this project do?

```

Claude 将分析您的文件并提供摘要。您也可以提出更具体的问题：

```plaintext
> what technologies does this project use?

```
```plaintext
> where is the main entry point?

```
```plaintext
> explain the folder structure

```

Claude Code 会根据需要读取您的文件 - 您不必手动添加上下文。

## 步骤 3：进行您的第一次代码更改

现在让我们让 Claude Code 做一些实际的编程工作。尝试一个简单的任务：

```plaintext
> add a hello world function to the main file

```

Claude Code 将：

1.  找到合适的文件
    
2.  向您展示建议的更改
    
3.  请求您的批准
    
4.  进行编辑
    

Claude Code 在修改文件之前总是请求许可。您可以批准单个更改或为会话启用”全部接受”模式。

## 步骤 4：将 Git 与 Claude Code 一起使用

Claude Code 使 Git 操作变得对话化：

```plaintext
> what files have I changed?

```
```plaintext
> commit my changes with a descriptive message

```

您也可以提示更复杂的 Git 操作：

```plaintext
> create a new branch called feature/quickstart

```
```plaintext
> show me the last 5 commits

```
```plaintext
> help me resolve merge conflicts

```

## 步骤 5：修复错误或添加功能

Claude 擅长调试和功能实现。

用自然语言描述您想要的：

```plaintext
> add input validation to the user registration form

```

或修复现有问题：

```plaintext
> there's a bug where users can submit empty forms - fix it

```

Claude Code 将：

*   定位相关代码
    
*   理解上下文
    
*   实现解决方案
    
*   如果可用，运行测试
    

## 步骤 6：测试其他常见工作流程

有多种方式与 Claude 协作：

**重构代码**

```plaintext
> refactor the authentication module to use async/await instead of callbacks

```

**编写测试**

```plaintext
> write unit tests for the calculator functions

```

**更新文档**

```plaintext
> update the README with installation instructions

```

**代码审查**

```plaintext
> review my changes and suggest improvements

```

**记住**：Claude Code 是您的AI结对编程伙伴。像与有用的同事交谈一样与它交谈 - 描述您想要实现的目标，它将帮助您达到目标。

## 基本命令

以下是日常使用最重要的命令：

| **命令** | **功能** | **示例** |
| --- | --- | --- |
| `claude` | 启动交互模式 | `claude` |
| `claude "task"` | 运行一次性任务 | `claude "fix the build error"` |
| `claude -p "query"` | 运行一次性查询，然后退出 | `claude -p "explain this function"` |
| `claude -c` | 继续最近的对话 | `claude -c` |
| `claude -r` | 恢复之前的对话 | `claude -r` |
| `claude commit` | 创建 Git 提交 | `claude commit` |
| `/clear` | 清除对话历史 | `> /clear` |
| `/help` | 显示可用命令 | `> /help` |
| `exit` 或 Ctrl+C | 退出 Claude Code | `> exit` |

# 使用 CLAUDE CODE 构建

# Claude Code SDK

了解如何使用 Claude Code SDK 以编程方式将 Claude Code 集成到您的应用程序中。

Claude Code SDK 支持将 Claude Code 作为子进程运行，提供了一种构建 AI 驱动的编码助手和工具的方法，利用 Claude 的能力。

SDK 可用于命令行、TypeScript 和 Python 使用。

## 身份验证

要使用 Claude Code SDK，我们建议创建一个专用的 API 密钥：

1.  在 [**Anthropic Console**](https://console.anthropic.com/) 中创建一个 Anthropic API 密钥
    
2.  然后，设置 `ANTHROPIC_API_KEY` 环境变量。我们建议安全地存储此密钥（例如，使用 Github [**secret**](https://docs.github.com/en/actions/security-for-github-actions/security-guides/using-secrets-in-github-actions)）
    

## 基本 SDK 使用

Claude Code SDK 允许您在应用程序中以非交互模式使用 Claude Code。

### 命令行

以下是命令行 SDK 的一些基本示例：

```bash
# 运行单个提示并退出（打印模式）
$ claude -p "Write a function to calculate Fibonacci numbers"

# 使用管道提供 stdin
$ echo "Explain this code" | claude -p

# 以 JSON 格式输出并包含元数据
$ claude -p "Generate a hello world function" --output-format json

# 在到达时流式传输 JSON 输出
$ claude -p "Build a React component" --output-format stream-json

```

### TypeScript

TypeScript SDK 包含在 NPM 上的主要 [`**@anthropic-ai/claude-code**`](https://www.npmjs.com/package/@anthropic-ai/claude-code) 包中：

```ts
import { query, type SDKMessage } from "@anthropic-ai/claude-code";

const messages: SDKMessage[] = [];

for await (const message of query({
  prompt: "Write a haiku about foo.py",
  abortController: new AbortController(),
  options: {
    maxTurns: 3,
  },
})) {
  messages.push(message);
}

console.log(messages);

```

TypeScript SDK 接受命令行 SDK 支持的所有参数，以及：

| **参数** | **描述** | **默认值** |
| --- | --- | --- |
| `abortController` | 中止控制器 | `new AbortController()` |
| `cwd` | 当前工作目录 | `process.cwd()` |
| `executable` | 要使用的 JavaScript 运行时 | 在 Node.js 中运行时为 `node`，在 Bun 中运行时为 `bun` |
| `executableArgs` | 传递给可执行文件的参数 | `[]` |
| `pathToClaudeCodeExecutable` | Claude Code 可执行文件的路径 | 与 `@anthropic-ai/claude-code` 一起提供的可执行文件 |

### Python

Python SDK 在 PyPI 上作为 [`**claude-code-sdk**`](https://github.com/anthropics/claude-code-sdk-python) 提供：

```bash
pip install claude-code-sdk

```

**先决条件：**

*   Python 3.10+
    
*   Node.js
    
*   Claude Code CLI：`npm install -g @anthropic-ai/claude-code`
    

基本使用：

```python
import anyio
from claude_code_sdk import query, ClaudeCodeOptions, Message

async def main():
    messages: list[Message] = []
    
    async for message in query(
        prompt="Write a haiku about foo.py",
        options=ClaudeCodeOptions(max_turns=3)
    ):
        messages.append(message)
    
    print(messages)

anyio.run(main)

```

Python SDK 通过 `ClaudeCodeOptions` 类接受命令行 SDK 支持的所有参数：

```python
from claude_code_sdk import query, ClaudeCodeOptions
from pathlib import Path

options = ClaudeCodeOptions(
    max_turns=3,
    system_prompt="You are a helpful assistant",
    cwd=Path("/path/to/project"),  # 可以是字符串或 Path
    allowed_tools=["Read", "Write", "Bash"],
    permission_mode="acceptEdits"
)

async for message in query(prompt="Hello", options=options):
    print(message)

```

## 高级使用

下面的文档使用命令行 SDK 作为示例，但也可以与 TypeScript 和 Python SDK 一起使用。

### 多轮对话

对于多轮对话，您可以恢复对话或从最近的会话继续：

```bash
# 继续最近的对话
$ claude --continue

# 继续并提供新的提示
$ claude --continue "Now refactor this for better performance"

# 通过会话 ID 恢复特定对话
$ claude --resume 550e8400-e29b-41d4-a716-446655440000

# 在打印模式下恢复（非交互式）
$ claude -p --resume 550e8400-e29b-41d4-a716-446655440000 "Update the tests"

# 在打印模式下继续（非交互式）
$ claude -p --continue "Add error handling"

```

### 自定义系统提示

您可以提供自定义系统提示来指导 Claude 的行为：

```bash
# 覆盖系统提示（仅适用于 --print）
$ claude -p "Build a REST API" --system-prompt "You are a senior backend engineer. Focus on security, performance, and maintainability."

# 具有特定要求的系统提示
$ claude -p "Create a database schema" --system-prompt "You are a database architect. Use PostgreSQL best practices and include proper indexing."

```

您还可以将指令附加到默认系统提示：

```bash
# 附加系统提示（仅适用于 --print）
$ claude -p "Build a REST API" --append-system-prompt "After writing code, be sure to code review yourself."

```

### MCP 配置

模型上下文协议（MCP）允许您使用来自外部服务器的附加工具和资源扩展 Claude Code。使用 `--mcp-config` 标志，您可以加载提供专门功能的 MCP 服务器，如数据库访问、API 集成或自定义工具。

创建一个包含您的 MCP 服务器的 JSON 配置文件：

```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-filesystem",
        "/path/to/allowed/files"
      ]
    },
    "github": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-github"],
      "env": {
        "GITHUB_TOKEN": "your-github-token"
      }
    }
  }
}

```

然后与 Claude Code 一起使用：

```bash
# 从配置加载 MCP 服务器
$ claude -p "List all files in the project" --mcp-config mcp-servers.json

# 重要：必须使用 --allowedTools 明确允许 MCP 工具
# MCP 工具遵循格式：mcp__$serverName__$toolName
$ claude -p "Search for TODO comments" \
  --mcp-config mcp-servers.json \
  --allowedTools "mcp__filesystem__read_file,mcp__filesystem__list_directory"

# 使用 MCP 工具在非交互模式下处理权限提示
$ claude -p "Deploy the application" \
  --mcp-config mcp-servers.json \
  --allowedTools "mcp__permissions__approve" \
  --permission-prompt-tool mcp__permissions__approve

```

使用 MCP 工具时，您必须使用 `--allowedTools` 标志明确允许它们。MCP 工具名称遵循模式 `mcp__<serverName>__<toolName>`，其中：

*   `serverName` 是您的 MCP 配置文件中的键
    
*   `toolName` 是该服务器提供的特定工具
    

这种安全措施确保 MCP 工具仅在明确允许时使用。

如果您只指定服务器名称（即 `mcp__<serverName>`），则该服务器的所有工具都将被允许。

不支持通配符模式（例如 `mcp__go*`）。

### 自定义权限提示工具

可选地，使用 `--permission-prompt-tool` 传入一个 MCP 工具，我们将使用它来检查用户是否授予模型调用给定工具的权限。当模型调用工具时，会发生以下情况：

1.  我们首先检查权限设置：所有 [**settings.json 文件**](https://docs.anthropic.com/zh-CN/docs/claude-code/settings)，以及传递给 SDK 的 `--allowedTools` 和 `--disallowedTools`；如果其中之一允许或拒绝工具调用，我们继续进行工具调用
    
2.  否则，我们调用您在 `--permission-prompt-tool` 中提供的 MCP 工具
    

`--permission-prompt-tool` MCP 工具会传递工具名称和输入，并且必须返回一个带有结果的 JSON 字符串化载荷。载荷必须是以下之一：

```ts
// 工具调用被允许
{
  "behavior": "allow",
  "updatedInput": {...}, // 更新的输入，或者只是返回原始输入
}

// 工具调用被拒绝
{
  "behavior": "deny",
  "message": "..." // 解释为什么权限被拒绝的人类可读字符串
}zai1

```

例如，TypeScript MCP 权限提示工具实现可能如下所示：

```ts
const server = new McpServer({
  name: "Test permission prompt MCP Server",
  version: "0.0.1",
});

server.tool(
  "approval_prompt",
  'Simulate a permission check - approve if the input contains "allow", otherwise deny',
  {
    tool_name: z.string().describe("The tool requesting permission"),
    input: z.object({}).passthrough().describe("The input for the tool"),
  },
  async ({ tool_name, input }) => {
    return {
      content: [
        {
          type: "text",
          text: JSON.stringify(
            JSON.stringify(input).includes("allow")
              ? {
                  behavior: "allow",
                  updatedInput: input,
                }
              : {
                  behavior: "deny",
                  message: "Permission denied by test approval_prompt tool",
                }
          ),
        },
      ],
    };
  }
);

```

要使用此工具，添加您的 MCP 服务器（例如使用 `--mcp-config`），然后像这样调用 SDK：

```sh
claude -p "..." \
  --permission-prompt-tool mcp__test-server__approval_prompt \
  --mcp-config my-config.json

```

使用说明：

*   使用 `updatedInput` 告诉模型权限提示改变了其输入；否则，将 `updatedInput` 设置为原始输入，如上面的示例所示。例如，如果工具向用户显示文件编辑差异并让他们手动编辑差异，权限提示工具应该返回该更新的编辑。
    
*   载荷必须是 JSON 字符串化的
    

## 可用的 CLI 选项

SDK 利用 Claude Code 中可用的所有 CLI 选项。以下是 SDK 使用的关键选项：

| **标志** | **描述** | **示例** |
| --- | --- | --- |
| `--print`, `-p` | 在非交互模式下运行 | `claude -p "query"` |
| `--output-format` | 指定输出格式（`text`、`json`、`stream-json`） | `claude -p --output-format json` |
| `--resume`, `-r` | 通过会话 ID 恢复对话 | `claude --resume abc123` |
| `--continue`, `-c` | 继续最近的对话 | `claude --continue` |
| `--verbose` | 启用详细日志记录 | `claude --verbose` |
| `--max-turns` | 在非交互模式下限制代理轮次 | `claude --max-turns 3` |
| `--system-prompt` | 覆盖系统提示（仅适用于 `--print`） | `claude --system-prompt "Custom instruction"` |
| `--append-system-prompt` | 附加到系统提示（仅适用于 `--print`） | `claude --append-system-prompt "Custom instruction"` |
| `--allowedTools` | 允许的工具的空格分隔列表，或<br>允许的工具的逗号分隔列表字符串 | `claude --allowedTools mcp__slack mcp__filesystem`<br>`claude --allowedTools "Bash(npm install),mcp__filesystem"` |
| `--disallowedTools` | 拒绝的工具的空格分隔列表，或<br>拒绝的工具的逗号分隔列表字符串 | `claude --disallowedTools mcp__splunk mcp__github`<br>`claude --disallowedTools "Bash(git commit),mcp__github"` |
| `--mcp-config` | 从 JSON 文件加载 MCP 服务器 | `claude --mcp-config servers.json` |
| `--permission-prompt-tool` | 用于处理权限提示的 MCP 工具（仅适用于 `--print`） | `claude --permission-prompt-tool mcp__auth__prompt` |

有关 CLI 选项和功能的完整列表，请参阅 [**CLI 参考**](https://docs.anthropic.com/zh-CN/docs/claude-code/cli-reference) 文档。

## 输出格式

SDK 支持多种输出格式：

### 文本输出（默认）

仅返回响应文本：

```bash
$ claude -p "Explain file src/components/Header.tsx"
# 输出：This is a React component showing...

```

### JSON 输出

返回包括元数据的结构化数据：

```bash
$ claude -p "How does the data layer work?" --output-format json

```

响应格式：

```json
{
  "type": "result",
  "subtype": "success",
  "total_cost_usd": 0.003,
  "is_error": false,
  "duration_ms": 1234,
  "duration_api_ms": 800,
  "num_turns": 6,
  "result": "The response text here...",
  "session_id": "abc123"
}

```

### 流式 JSON 输出

在接收到每条消息时流式传输：

```bash
$ claude -p "Build an application" --output-format stream-json

```

每个对话都以初始的 `init` 系统消息开始，然后是用户和助手消息列表，最后是带有统计信息的最终 `result` 系统消息。每条消息都作为单独的 JSON 对象发出。

## 消息模式

从 JSON API 返回的消息根据以下模式严格类型化：

```ts
type SDKMessage =
  // 助手消息
  | {
      type: "assistant";
      message: Message; // 来自 Anthropic SDK
      session_id: string;
    }

  // 用户消息
  | {
      type: "user";
      message: MessageParam; // 来自 Anthropic SDK
      session_id: string;
    }

  // 作为最后一条消息发出
  | {
      type: "result";
      subtype: "success";
      duration_ms: float;
      duration_api_ms: float;
      is_error: boolean;
      num_turns: int;
      result: string;
      session_id: string;
      total_cost_usd: float;
    }

  // 作为最后一条消息发出，当我们达到最大轮次时
  | {
      type: "result";
      subtype: "error_max_turns" | "error_during_execution";
      duration_ms: float;
      duration_api_ms: float;
      is_error: boolean;
      num_turns: int;
      session_id: string;
      total_cost_usd: float;
    }

  // 在对话开始时作为第一条消息发出
  | {
      type: "system";
      subtype: "init";
      apiKeySource: string;
      cwd: string;
      session_id: string;
      tools: string[];
      mcp_servers: {
        name: string;
        status: string;
      }[];
      model: string;
      permissionMode: "default" | "acceptEdits" | "bypassPermissions" | "plan";
    };

```

我们将很快以 JSONSchema 兼容格式发布这些类型。我们对主要的 Claude Code 包使用语义版本控制来传达此格式的重大更改。

`Message` 和 `MessageParam` 类型在 Anthropic SDK 中可用。例如，请参阅 Anthropic [**TypeScript**](https://github.com/anthropics/anthropic-sdk-typescript) 和 [**Python**](https://github.com/anthropics/anthropic-sdk-python/) SDK。

## 输入格式

SDK 支持多种输入格式：

### 文本输入（默认）

输入文本可以作为参数提供：

```bash
$ claude -p "Explain this code"

```

或者输入文本可以通过 stdin 管道传输：

```bash
$ echo "Explain this code" | claude -p

```

### 流式 JSON 输入

通过 `stdin` 提供的消息流，其中每条消息代表一个用户轮次。这允许对话的多个轮次而无需重新启动 `claude` 二进制文件，并允许在模型处理请求时向模型提供指导。

每条消息都是一个 JSON ‘用户消息’ 对象，遵循与输出消息模式相同的格式。消息使用 [**jsonl**](https://jsonlines.org/) 格式格式化，其中输入的每一行都是一个完整的 JSON 对象。流式 JSON 输入需要 `-p` 和 `--output-format stream-json`。

目前这仅限于纯文本用户消息。

```bash
$ echo '{"type":"user","message":{"role":"user","content":[{"type":"text","text":"Explain this code"}]}}' | claude -p --output-format=stream-json --input-format=stream-json --verbose

```

## 示例

### 简单脚本集成

```bash
#!/bin/bash

# 运行 Claude 并检查退出代码的简单函数
run_claude() {
    local prompt="$1"
    local output_format="${2:-text}"

    if claude -p "$prompt" --output-format "$output_format"; then
        echo "Success!"
    else
        echo "Error: Claude failed with exit code $?" >&2
        return 1
    fi
}

# 使用示例
run_claude "Write a Python function to read CSV files"
run_claude "Optimize this database query" "json"

```

### 使用 Claude 处理文件

```bash
# 通过 Claude 处理文件
$ cat mycode.py | claude -p "Review this code for bugs"

# 处理多个文件
$ for file in *.js; do
    echo "Processing $file..."
    claude -p "Add JSDoc comments to this file:" < "$file" > "${file}.documented"
done

# 在管道中使用 Claude
$ grep -l "TODO" *.py | while read file; do
    claude -p "Fix all TODO items in this file" < "$file"
done

```

### 会话管理

```bash
# 启动会话并捕获会话 ID
$ claude -p "Initialize a new project" --output-format json | jq -r '.session_id' > session.txt

# 使用相同会话继续
$ claude -p --resume "$(cat session.txt)" "Add unit tests"

```

## 最佳实践

1.  **使用 JSON 输出格式** 进行响应的程序化解析：
    

```bash
# 使用 jq 解析 JSON 响应
result=$(claude -p "Generate code" --output-format json)
code=$(echo "$result" | jq -r '.result')
cost=$(echo "$result" | jq -r '.cost_usd')

```

2.  **优雅地处理错误** - 检查退出代码和 stderr：
    

```bash
if ! claude -p "$prompt" 2>error.log; then
    echo "Error occurred:" >&2
    cat error.log >&2
    exit 1
fi

```

3.  **使用会话管理** 在多轮对话中维护上下文
    
4.  **考虑超时** 对于长时间运行的操作：
    

```bash
timeout 300 claude -p "$complex_prompt" || echo "Timed out after 5 minutes"

```

5.  **尊重速率限制** 在进行多个请求时通过在调用之间添加延迟
    

## 实际应用

Claude Code SDK 能够与您的开发工作流程进行强大的集成。一个值得注意的例子是 [**Claude Code GitHub Actions**](https://docs.anthropic.com/zh-CN/docs/claude-code/github-actions)，它使用 SDK 直接在您的 GitHub 工作流程中提供自动化代码审查、PR 创建和问题分类功能。

## 相关资源

*   [**CLI 使用和控制**](https://docs.anthropic.com/zh-CN/docs/claude-code/cli-reference) - 完整的 CLI 文档
    
*   [**GitHub Actions 集成**](https://docs.anthropic.com/zh-CN/docs/claude-code/github-actions) - 使用 Claude 自动化您的 GitHub 工作流程
    
*   [**常见工作流程**](https://docs.anthropic.com/zh-CN/docs/claude-code/common-workflows) - 常见用例的分步指南
    

# 开始使用 Claude Code hooks

学习如何通过注册 shell 命令来自定义和扩展 Claude Code 的行为

Claude Code hooks 是用户定义的 shell 命令，在 Claude Code 生命周期的各个点执行。Hooks 提供对 Claude Code 行为的确定性控制，确保某些操作总是发生，而不是依赖 LLM 选择运行它们。

有关 hooks 的参考文档，请参阅 [**Hooks 参考**](https://docs.anthropic.com/zh-CN/docs/claude-code/hooks)。

hooks 的示例用例包括：

*   **通知**：自定义当 Claude Code 等待您的输入或运行权限时如何获得通知。
    
*   **自动格式化**：在每次文件编辑后对 .ts 文件运行 `prettier`，对 .go 文件运行 `gofmt` 等。
    
*   **日志记录**：跟踪和计算所有执行的命令以用于合规性或调试。
    
*   **反馈**：当 Claude Code 产生不遵循您的代码库约定的代码时提供自动反馈。
    
*   **自定义权限**：阻止对生产文件或敏感目录的修改。
    

通过将这些规则编码为 hooks 而不是提示指令，您将建议转换为应用程序级代码，每次预期运行时都会执行。

您必须考虑添加 hooks 时的安全影响，因为 hooks 在代理循环期间使用您当前环境的凭据自动运行。 例如，恶意 hooks 代码可以泄露您的数据。在注册之前始终检查您的 hooks 实现。

有关完整的安全最佳实践，请参阅 hooks 参考文档中的[**安全考虑**](https://docs.anthropic.com/zh-CN/docs/claude-code/hooks#security-considerations)。

## Hook 事件概述

Claude Code 提供了几个在工作流程不同点运行的 hook 事件：

*   **PreToolUse**：在工具调用之前运行（可以阻止它们）
    
*   **PostToolUse**：在工具调用完成后运行
    
*   **Notification**：当 Claude Code 发送通知时运行
    
*   **Stop**：当 Claude Code 完成响应时运行
    
*   **SubagentStop**：当子代理任务完成时运行
    

每个事件接收不同的数据，并可以以不同的方式控制 Claude 的行为。

## 快速开始

在这个快速开始中，您将添加一个记录 Claude Code 运行的 shell 命令的 hook。

### 先决条件

安装 `jq` 用于命令行中的 JSON 处理。

### 步骤 1：打开 hooks 配置

运行 `/hooks` [**斜杠命令**](https://docs.anthropic.com/zh-CN/docs/claude-code/slash-commands) 并选择 `PreToolUse` hook 事件。

`PreToolUse` hooks 在工具调用之前运行，可以阻止它们，同时为 Claude 提供关于如何做不同事情的反馈。

### 步骤 2：添加匹配器

选择 `+ Add new matcher…` 以仅在 Bash 工具调用上运行您的 hook。

为匹配器输入 `Bash`。

您可以使用 `*` 来匹配所有工具。

### 步骤 3：添加 hook

选择 `+ Add new hook…` 并输入此命令：

```bash
jq -r '"\(.tool_input.command) - \(.tool_input.description // "No description")"' >> ~/.claude/bash-command-log.txt

```

### 步骤 4：保存您的配置

对于存储位置，选择 `User settings`，因为您正在记录到您的主目录。然后此 hook 将应用于所有项目，而不仅仅是您当前的项目。

然后按 Esc 直到您返回到 REPL。您的 hook 现在已注册！

### 步骤 5：验证您的 hook

再次运行 `/hooks` 或检查 `~/.claude/settings.json` 以查看您的配置：

```json
{
  "hooks": {
    "PreToolUse": [
      {
        "matcher": "Bash",
        "hooks": [
          {
            "type": "command",
            "command": "jq -r '\"\(.tool_input.command) - \(.tool_input.description // \"No description\")\"' >> ~/.claude/bash-command-log.txt"
          }
        ]
      }
    ]
  }
}

```

### 步骤 6：测试您的 hook

要求 Claude 运行一个简单的命令，如 `ls` 并检查您的日志文件：

```bash
cat ~/.claude/bash-command-log.txt

```

您应该看到类似以下的条目：

```plaintext
ls - Lists files and directories

```

## 更多示例

有关完整的示例实现，请参阅我们公共代码库中的 [**bash 命令验证器示例**](https://github.com/anthropics/claude-code/blob/main/examples/hooks/bash_command_validator_example.py)。

### 代码格式化 Hook

编辑后自动格式化 TypeScript 文件：

```json
{
  "hooks": {
    "PostToolUse": [
      {
        "matcher": "Edit|MultiEdit|Write",
        "hooks": [
          {
            "type": "command",
            "command": "jq -r '.tool_input.file_path' | { read file_path; if echo \"$file_path\" | grep -q '\.ts$'; then npx prettier --write \"$file_path\"; fi; }"
          }
        ]
      }
    ]
  }
}

```

### 自定义通知 Hook

当 Claude 需要输入时获得桌面通知：

```json
{
  "hooks": {
    "Notification": [
      {
        "matcher": "",
        "hooks": [
          {
            "type": "command",
            "command": "notify-send 'Claude Code' 'Awaiting your input'"
          }
        ]
      }
    ]
  }
}

```

### 文件保护 Hook

阻止对敏感文件的编辑：

```json
{
  "hooks": {
    "PreToolUse": [
      {
        "matcher": "Edit|MultiEdit|Write",
        "hooks": [
          {
            "type": "command",
            "command": "python3 -c \"import json, sys; data=json.load(sys.stdin); path=data.get('tool_input',{}).get('file_path',''); sys.exit(2 if any(p in path for p in ['.env', 'package-lock.json', '.git/']) else 0)\""
          }
        ]
      }
    ]
  }
}
```

# 故障排除

发现Claude Code安装和使用中常见问题的解决方案。

## 常见安装问题

### Linux权限问题

使用npm安装Claude Code时，如果您的npm全局前缀不可用户写入（例如`/usr`或`/usr/local`），您可能会遇到权限错误。

#### 推荐解决方案：创建用户可写的npm前缀

最安全的方法是配置npm使用您主目录内的目录：

```shell
# 首先，保存现有全局包的列表以便后续迁移
npm list -g --depth=0 > ~/npm-global-packages.txt

# 为您的全局包创建目录
mkdir -p ~/.npm-global

# 配置npm使用新的目录路径
npm config set prefix ~/.npm-global

# 注意：根据您的shell，将~/.bashrc替换为~/.zshrc、~/.profile或其他适当的文件
echo 'export PATH=~/.npm-global/bin:$PATH' >> ~/.bashrc

# 应用新的PATH设置
source ~/.bashrc

# 现在在新位置重新安装Claude Code
npm install -g @anthropic-ai/claude-code

# 可选：在新位置重新安装您之前的全局包
# 查看~/npm-global-packages.txt并安装您想要保留的包
```

推荐此解决方案是因为它：

*   避免修改系统目录权限
    
*   为您的全局npm包创建一个干净、专用的位置
    
*   遵循安全最佳实践
    

#### 系统恢复：如果您已运行更改系统文件所有权和权限或类似的命令

如果您已经运行了更改系统目录权限的命令（例如`sudo chown -R $USER:$(id -gn) /usr && sudo chmod -R u+w /usr`）并且您的系统现在损坏（例如，如果您看到`sudo: /usr/bin/sudo must be owned by uid 0 and have the setuid bit set`），您需要执行恢复步骤。

##### Ubuntu/Debian恢复方法：

1.  重启时，按住**SHIFT**键访问GRUB菜单
    
2.  选择”Advanced options for Ubuntu/Debian”
    
3.  选择恢复模式选项
    
4.  选择”Drop to root shell prompt”
    
5.  将文件系统重新挂载为可写：
    

```bash
mount -o remount,rw /

```

6.  修复权限：
    

```bash
# 恢复root所有权
chown -R root:root /usr
chmod -R 755 /usr

# 确保/usr/local由您的用户拥有以用于npm包
chown -R YOUR_USERNAME:YOUR_USERNAME /usr/local

# 为关键二进制文件设置setuid位
chmod u+s /usr/bin/sudo
chmod 4755 /usr/bin/sudo
chmod u+s /usr/bin/su
chmod u+s /usr/bin/passwd
chmod u+s /usr/bin/newgrp
chmod u+s /usr/bin/gpasswd
chmod u+s /usr/bin/chsh
chmod u+s /usr/bin/chfn

# 修复sudo配置
chown root:root /usr/libexec/sudo/sudoers.so
chmod 4755 /usr/libexec/sudo/sudoers.so
chown root:root /etc/sudo.conf
chmod 644 /etc/sudo.conf
```

7.  重新安装受影响的包（可选但推荐）：
    

```shell
# 保存已安装包的列表
dpkg --get-selections > /tmp/installed_packages.txt

# 重新安装它们
awk '{print $1}' /tmp/installed_packages.txt | xargs -r apt-get install --reinstall -y
```

8.  重启：
    

```bash
reboot

```

##### 替代Live USB恢复方法：

如果恢复模式不起作用，您可以使用live USB：

1.  从live USB启动（Ubuntu、Debian或任何Linux发行版）
    
2.  找到您的系统分区：
    

```bash
lsblk

```

3.  挂载您的系统分区：
    

```bash
sudo mount /dev/sdXY /mnt  # 将sdXY替换为您的实际系统分区

```

4.  如果您有单独的启动分区，也要挂载它：
    

```bash
sudo mount /dev/sdXZ /mnt/boot  # 如果需要

```

5.  Chroot到您的系统：
    

```shell
# 对于Ubuntu/Debian：
sudo chroot /mnt

# 对于基于Arch的系统：
sudo arch-chroot /mnt
```

6.  按照上面Ubuntu/Debian恢复方法的步骤6-8执行
    

恢复系统后，按照上面的推荐解决方案设置用户可写的npm前缀。

## 自动更新器问题

如果Claude Code无法自动更新，可能是由于您的npm全局前缀目录的权限问题。按照上面的[**推荐解决方案**](https://docs.anthropic.com/zh-CN/docs/claude-code/troubleshooting#%E6%8E%A8%E8%8D%90%E8%A7%A3%E5%86%B3%E6%96%B9%E6%A1%88%E5%88%9B%E5%BB%BA%E7%94%A8%E6%88%B7%E5%8F%AF%E5%86%99%E7%9A%84npm%E5%89%8D%E7%BC%80)来修复此问题。

如果您更愿意禁用自动更新器，您可以将`DISABLE_AUTOUPDATER`[**环境变量**](https://docs.anthropic.com/zh-CN/docs/claude-code/settings#environment-variables)设置为`1`

## 权限和身份验证

### 重复的权限提示

如果您发现自己重复批准相同的命令，您可以使用`/permissions`命令允许特定工具在无需批准的情况下运行。请参阅[**权限文档**](https://docs.anthropic.com/zh-CN/docs/claude-code/iam#configuring-permissions)。

### 身份验证问题

如果您遇到身份验证问题：

1.  运行`/logout`完全退出登录
    
2.  关闭Claude Code
    
3.  使用`claude`重启并重新完成身份验证过程
    

如果问题持续存在，请尝试：

```bash
rm -rf ~/.config/claude-code/auth.json
claude

```

这会删除您存储的身份验证信息并强制进行干净的登录。

## 性能和稳定性

### 高CPU或内存使用率

Claude Code设计用于与大多数开发环境配合使用，但在处理大型代码库时可能会消耗大量资源。如果您遇到性能问题：

1.  定期使用`/compact`来减少上下文大小
    
2.  在主要任务之间关闭并重启Claude Code
    
3.  考虑将大型构建目录添加到您的`.gitignore`文件中
    

### 命令挂起或冻结

如果Claude Code似乎无响应：

1.  按Ctrl+C尝试取消当前操作
    
2.  如果无响应，您可能需要关闭终端并重启
    

### ESC键在JetBrains（IntelliJ、PyCharm等）终端中不工作

如果您在JetBrains终端中使用Claude Code，ESC键无法按预期中断代理，这可能是由于与JetBrains默认快捷键的键绑定冲突。

要修复此问题：

1.  转到设置 → 工具 → 终端
    
2.  点击”覆盖IDE快捷键”旁边的”配置终端键绑定”超链接
    
3.  在终端键绑定中，向下滚动到”切换焦点到编辑器”并删除该快捷键
    

这将允许ESC键正确用于取消Claude Code操作，而不是被PyCharm的”切换焦点到编辑器”操作捕获。

## 获取更多帮助

如果您遇到此处未涵盖的问题：

1.  在Claude Code中使用`/bug`命令直接向Anthropic报告问题
    
2.  检查[**GitHub存储库**](https://github.com/anthropics/claude-code)了解已知问题
    
3.  运行`/doctor`检查您的Claude Code安装的健康状况
    

# 设置 Claude Code

在您的开发机器上安装、认证并开始使用 Claude Code。

## 系统要求

*   **操作系统**: macOS 10.15+、Ubuntu 20.04+/Debian 10+ 或通过 WSL 的 Windows
    
*   **硬件**: 最少 4GB RAM
    
*   **软件**:
    
    *   Node.js 18+
        
    *   [**git**](https://git-scm.com/downloads) 2.23+（可选）
        
    *   [**GitHub**](https://cli.github.com/) 或 [**GitLab**](https://gitlab.com/gitlab-org/cli) CLI 用于 PR 工作流（可选）
    
*   **网络**: 需要互联网连接进行认证和 AI 处理
    
*   **地区**: 仅在[**支持的国家**](https://www.anthropic.com/supported-countries)可用
    

## 安装和认证

**1**

**安装 Claude Code**

To install Claude Code, run the following command:

```sh
npm install -g @anthropic-ai/claude-code

```

**2**

**导航到您的项目**

```bash
cd your-project-directory 

```

**3**

**启动 Claude Code**

```bash
claude

```

**4**

**完成认证**

Claude Code 提供多种认证选项：

1.  **Anthropic Console**: 默认选项。通过 Anthropic Console 连接并 完成 OAuth 流程。需要在 [**console.anthropic.com**](https://console.anthropic.com/) 激活计费。
    
2.  **Claude App（Pro 或 Max 计划）**: 订阅 Claude 的 [**Pro 或 Max 计划**](https://www.anthropic.com/pricing)，获得包含 Claude Code 和网页界面的统一订阅。以相同价格获得更多价值，同时在一个地方管理您的账户。使用您的 Claude.ai 账户登录。在启动期间，选择与您的订阅类型匹配的选项。
    
3.  **企业平台**: 配置 Claude Code 使用 [**Amazon Bedrock 或 Google Vertex AI**](https://docs.anthropic.com/zh-CN/docs/claude-code/bedrock-vertex-proxies) 进行企业部署，使用您现有的云基础设施。
    

## 故障排除

### WSL 安装故障排除

目前，Claude Code 不能直接在 Windows 中运行，而是需要 WSL。

您可能在 WSL 中遇到以下问题：

**操作系统/平台检测问题**: 如果您在安装过程中收到错误，WSL 可能正在使用 Windows `npm`。尝试：

*   在安装前运行 `npm config set os linux`
    
*   使用 `npm install -g @anthropic-ai/claude-code --force --no-os-check` 安装（不要使用 `sudo`）
    

**找不到 Node 错误**: 如果您在运行 `claude` 时看到 `exec: node: not found`，您的 WSL 环境可能正在使用 Windows 安装的 Node.js。您可以通过 `which npm` 和 `which node` 确认这一点，它们应该指向以 `/usr/` 开头的 Linux 路径，而不是 `/mnt/c/`。要解决这个问题，请尝试通过您的 Linux 发行版的包管理器或通过 [`**nvm**`](https://github.com/nvm-sh/nvm) 安装 Node。

## 优化您的终端设置

Claude Code 在您的终端正确配置时效果最佳。遵循这些指南来优化您的体验。

**支持的 shell**:

*   Bash
    
*   Zsh
    
*   Fish
    

### 主题和外观

Claude 无法控制您终端的主题。这由您的终端应用程序处理。您可以在入门时或通过 `/config` 命令随时将 Claude Code 的主题与您的终端匹配

### 换行

您有几个选项可以在 Claude Code 中输入换行：

*   **快速转义**: 输入 `\` 然后按 Enter 创建新行
    
*   **键盘快捷键**: 通过适当配置按 Option+Enter（Meta+Enter）
    

在您的终端中设置 Option+Enter：

**对于 Mac Terminal.app:**

1.  打开设置 → 配置文件 → 键盘
    
2.  勾选”使用 Option 作为 Meta 键”
    

**对于 iTerm2 和 VSCode 终端:**

1.  打开设置 → 配置文件 → 键
    
2.  在常规下，将左/右 Option 键设置为”Esc+”
    

**iTerm2 和 VSCode 用户提示**: 在 Claude Code 中运行 `/terminal-setup` 以自动配置 Shift+Enter 作为更直观的替代方案。

### 通知设置

通过适当的通知配置，永远不会错过 Claude 完成任务的时机：

#### 终端铃声通知

在任务完成时启用声音警报：

```sh
claude config set --global preferredNotifChannel terminal_bell

```

**对于 macOS 用户**: 不要忘记在系统设置 → 通知 → \[您的终端应用\] 中启用通知权限。

#### iTerm 2 系统通知

对于任务完成时的 iTerm 2 警报：

1.  打开 iTerm 2 偏好设置
    
2.  导航到配置文件 → 终端
    
3.  启用”静音铃声”和过滤器警报 → “发送转义序列生成的警报”
    
4.  设置您首选的通知延迟
    

请注意，这些通知特定于 iTerm 2，在默认的 macOS 终端中不可用。

### 处理大型输入

在处理大量代码或长指令时：

*   **避免直接粘贴**: Claude Code 可能难以处理非常长的粘贴内容
    
*   **使用基于文件的工作流**: 将内容写入文件并要求 Claude 读取它
    
*   **注意 VS Code 限制**: VS Code 终端特别容易截断长粘贴
    

### Vim 模式

Claude Code 支持 Vim 键绑定的子集，可以通过 `/vim` 启用或通过 `/config` 配置。

支持的子集包括：

*   模式切换: `Esc`（到 NORMAL）、`i`/`I`、`a`/`A`、`o`/`O`（到 INSERT）
    
*   导航: `h`/`j`/`k`/`l`、`w`/`e`/`b`、`0`/`$`/`^`、`gg`/`G`
    
*   编辑: `x`、`dw`/`de`/`db`/`dd`/`D`、`cw`/`ce`/`cb`/`cc`/`C`、`.`（重复）
    

# 身份和访问管理

了解如何为您的组织配置Claude Code的用户身份验证、授权和访问控制。

## 身份验证方法

设置Claude Code需要访问Anthropic模型。对于团队，您可以通过以下三种方式之一设置Claude Code访问：

*   通过Anthropic控制台使用Anthropic API
    
*   Amazon Bedrock
    
*   Google Vertex AI
    

### Anthropic API身份验证

**通过Anthropic API为您的团队设置Claude Code访问：**

1.  使用您现有的Anthropic控制台账户或创建新的Anthropic控制台账户
    
2.  您可以通过以下任一方法添加用户：
    
    *   从控制台内批量邀请用户（控制台 -> 设置 -> 成员 -> 邀请）
        
    *   [**设置SSO**](https://support.anthropic.com/en/articles/10280258-setting-up-single-sign-on-on-the-api-console)
    
3.  邀请用户时，他们需要以下角色之一：
    
    *   “Claude Code”角色意味着用户只能创建Claude Code API密钥
        
    *   “开发者”角色意味着用户可以创建任何类型的API密钥
    
4.  每个受邀用户需要完成以下步骤：
    
    *   接受控制台邀请
        
    *   [**检查系统要求**](https://docs.anthropic.com/zh-CN/docs/claude-code/setup#system-requirements)
        
    *   [**安装Claude Code**](https://docs.anthropic.com/zh-CN/docs/claude-code/setup#installation)
        
    *   使用控制台账户凭据登录
        

### 云提供商身份验证

**通过Bedrock或Vertex为您的团队设置Claude Code访问：**

1.  遵循[**Bedrock文档**](https://docs.anthropic.com/zh-CN/docs/claude-code/amazon-bedrock)或[**Vertex文档**](https://docs.anthropic.com/zh-CN/docs/claude-code/google-vertex-ai)
    
2.  向您的用户分发环境变量和生成云凭据的说明。了解更多关于如何[**在此处管理配置**](https://docs.anthropic.com/zh-CN/docs/claude-code/settings)。
    
3.  用户可以[**安装Claude Code**](https://docs.anthropic.com/zh-CN/docs/claude-code/setup#installation)
    

## 访问控制和权限

我们支持细粒度权限，以便您能够准确指定代理被允许做什么（例如运行测试、运行linter）以及不被允许做什么（例如更新云基础设施）。这些权限设置可以检入版本控制并分发给您组织中的所有开发者，也可以由个别开发者自定义。

### 权限系统

Claude Code使用分层权限系统来平衡功能和安全性：

| **工具类型** | **示例** | **需要批准** | **”是的，不要再问”行为** |
| --- | --- | --- | --- |
| 只读 | 文件读取、LS、Grep | 否 | 不适用 |
| Bash命令 | Shell执行 | 是 | 每个项目目录和命令永久生效 |
| 文件修改 | 编辑/写入文件 | 是 | 直到会话结束 |

### 配置权限

您可以使用`/permissions`查看和管理Claude Code的工具权限。此UI列出所有权限规则及其来源的settings.json文件。

*   **允许**规则将允许Claude Code使用指定工具而无需进一步手动批准。
    
*   **拒绝**规则将阻止Claude Code使用指定工具。拒绝规则优先于允许规则。
    
*   **其他目录**将Claude的文件访问扩展到初始工作目录之外的目录。
    
*   **默认模式**控制Claude在遇到新请求时的权限行为。
    

权限规则使用格式：`Tool(optional-specifier)`

仅为工具名称的规则匹配该工具的任何使用。例如，将`Bash`添加到允许规则列表中将允许Claude Code使用Bash工具而无需用户批准。

#### 权限模式

Claude Code支持几种权限模式，可以在[**设置文件**](https://docs.anthropic.com/zh-CN/docs/claude-code/settings#settings-files)中设置为`defaultMode`：

| **模式** | **描述** |
| --- | --- |
| `default` | 标准行为 - 在首次使用每个工具时提示权限 |
| `acceptEdits` | 自动接受会话的文件编辑权限 |
| `plan` | 计划模式 - Claude可以分析但不能修改文件或执行命令 |
| `bypassPermissions` | 跳过所有权限提示（需要安全环境 - 请参见下面的警告） |

#### 工作目录

默认情况下，Claude可以访问启动它的目录中的文件。您可以扩展此访问权限：

*   **启动期间**：使用`--add-dir <path>` CLI参数
    
*   **会话期间**：使用`/add-dir`斜杠命令
    
*   **持久配置**：添加到[**设置文件**](https://docs.anthropic.com/zh-CN/docs/claude-code/settings#settings-files)中的`additionalDirectories`
    

其他目录中的文件遵循与原始工作目录相同的权限规则 - 它们变得可读而无需提示，文件编辑权限遵循当前权限模式。

#### 工具特定权限规则

一些工具使用可选说明符进行更细粒度的权限控制。例如，带有`Bash(git diff:*)`的允许规则将允许以`git diff`开头的Bash命令。以下工具支持带有说明符的权限规则：

**Bash**

*   `Bash(npm run build)` 匹配确切的Bash命令`npm run build`
    
*   `Bash(npm run test:*)` 匹配以`npm run test`开头的Bash命令。
    

Claude Code了解shell操作符（如`&&`），因此像`Bash(safe-cmd:*)`这样的前缀匹配规则不会给它运行命令`safe-cmd && other-cmd`的权限

**Read & Edit**

`Edit`规则适用于所有编辑文件的内置工具。Claude将尽力将`Read`规则应用于所有读取文件的内置工具，如Grep、Glob和LS。

Read和Edit规则都遵循[**gitignore**](https://git-scm.com/docs/gitignore)规范。模式相对于包含`.claude/settings.json`的目录解析。要引用绝对路径，请使用`//`。对于相对于您主目录的路径，请使用`~/`。

*   `Edit(docs/**)` 匹配对项目`docs`目录中文件的编辑
    
*   `Read(~/.zshrc)` 匹配对您的`~/.zshrc`文件的读取
    
*   `Edit(//tmp/scratch.txt)` 匹配对`/tmp/scratch.txt`的编辑
    

**WebFetch**

*   `WebFetch(domain:example.com)` 匹配对example.com的获取请求
    

**MCP**

*   `mcp__puppeteer` 匹配由`puppeteer`服务器提供的任何工具（在Claude Code中配置的名称）
    
*   `mcp__puppeteer__puppeteer_navigate` 匹配由`puppeteer`服务器提供的`puppeteer_navigate`工具
    

### 企业管理策略设置

对于Claude Code的企业部署，我们支持企业管理策略设置，这些设置优先于用户和项目设置。这允许系统管理员强制执行用户无法覆盖的安全策略。

系统管理员可以将策略部署到：

*   **macOS**：`/Library/Application Support/ClaudeCode/managed-settings.json`
    
*   **Linux和Windows（通过WSL）**：`/etc/claude-code/managed-settings.json`
    

这些策略文件遵循与常规[**设置文件**](https://docs.anthropic.com/zh-CN/docs/claude-code/settings#settings-files)相同的格式，但不能被用户或项目设置覆盖。这确保了整个组织的一致安全策略。

### 设置优先级

当存在多个设置源时，它们按以下顺序应用（从最高到最低优先级）：

1.  企业策略
    
2.  命令行参数
    
3.  本地项目设置（`.claude/settings.local.json`）
    
4.  共享项目设置（`.claude/settings.json`）
    
5.  用户设置（`~/.claude/settings.json`）
    

此层次结构确保始终执行组织策略，同时在适当的情况下仍允许在项目和用户级别的灵活性。

### 使用钩子进行额外权限控制

[**Claude Code钩子**](https://docs.anthropic.com/zh-CN/docs/claude-code/hooks)提供了一种注册自定义shell命令以在运行时执行权限评估的方法。当Claude Code进行工具调用时，PreToolUse钩子在权限系统运行之前运行，钩子输出可以确定是否批准或拒绝工具调用以代替权限系统。

## 凭据管理

Claude Code支持通过Claude.ai凭据、Anthropic API凭据、Bedrock Auth和Vertex Auth进行身份验证。在macOS上，API密钥、OAuth令牌和其他凭据存储在加密的macOS钥匙串中。或者，设置[**apiKeyHelper**](https://docs.anthropic.com/zh-CN/docs/claude-code/settings#available-settings)可以设置为返回API密钥的shell脚本。默认情况下，此助手在5分钟后或在HTTP 401响应时被调用；指定环境变量`CLAUDE_CODE_API_KEY_HELPER_TTL_MS`定义自定义刷新间隔。

# 有效管理成本

了解如何在使用 Claude Code 时跟踪和优化令牌使用量和成本。

Claude Code 每次交互都会消耗令牌。平均成本为每个开发者每天 6 美元，90% 的用户每日成本保持在 12 美元以下。

对于团队使用，Claude Code 按 API 令牌消耗量收费。平均而言，使用 Sonnet 4 的 Claude Code 每个开发者每月成本约为 100-200 美元，但根据用户运行的实例数量以及是否在自动化中使用，存在很大差异。

## 跟踪您的成本

*   使用 `/cost` 查看当前会话使用量
    
*   **Anthropic Console 用户**：
    
    *   在 Anthropic Console 中检查[**历史使用量**](https://support.anthropic.com/en/articles/9534590-cost-and-usage-reporting-in-console)（需要管理员或计费角色）
        
    *   为 Claude Code 工作区设置[**工作区支出限制**](https://support.anthropic.com/en/articles/9796807-creating-and-managing-workspaces)（需要管理员角色）
    
*   **Pro 和 Max 计划用户**：使用量包含在您的订阅中
    

## 为团队管理成本

使用 Anthropic API 时，您可以限制 Claude Code 工作区的总支出。要配置，请[**按照这些说明操作**](https://support.anthropic.com/en/articles/9796807-creating-and-managing-workspaces)。管理员可以通过[**按照这些说明操作**](https://support.anthropic.com/en/articles/9534590-cost-and-usage-reporting-in-console)查看成本和使用量报告。

在 Bedrock 和 Vertex 上，Claude Code 不会从您的云端发送指标。为了获取成本指标，几家大型企业报告使用了 [**LiteLLM**](https://docs.anthropic.com/zh-CN/docs/claude-code/bedrock-vertex-proxies#litellm)，这是一个开源工具，帮助公司[**按密钥跟踪支出**](https://docs.litellm.ai/docs/proxy/virtual_keys#tracking-spend)。该项目与 Anthropic 无关，我们也未审核其安全性。

## 减少令牌使用量

*   **紧凑对话：**
    
    *   Claude 默认在上下文超过 95% 容量时使用自动紧凑
        
    *   切换自动紧凑：运行 `/config` 并导航到”Auto-compact enabled”
        
    *   当上下文变大时手动使用 `/compact`
        
    *   添加自定义指令：`/compact Focus on code samples and API usage`
        
    *   通过添加到 CLAUDE.md 来自定义紧凑：
        

```shell
# Summary instructions

When you are using compact, please focus on test output and code changes
```

*   **编写具体查询：** 避免触发不必要扫描的模糊请求
    
*   **分解复杂任务：** 将大型任务拆分为专注的交互
    
*   **在任务之间清除历史：** 使用 `/clear` 重置上下文
    

成本可能因以下因素而显著变化：

*   被分析代码库的大小
    
*   查询的复杂性
    
*   被搜索或修改的文件数量
    
*   对话历史的长度
    
*   紧凑对话的频率
    
*   后台进程（俳句生成、对话摘要）
    

## 后台令牌使用量

Claude Code 即使在空闲时也会为某些后台功能使用令牌：

*   **俳句生成**：您输入时出现的小型创意消息（大约每天 1 分钱）
    
*   **对话摘要**：为 `claude --resume` 功能摘要之前对话的后台作业
    
*   **命令处理**：某些命令如 `/cost` 可能生成请求来检查状态
    

这些后台进程即使没有主动交互也会消耗少量令牌（通常每个会话低于 0.04 美元）。

# 分析

查看您组织的Claude Code部署的详细使用洞察和生产力指标。

Claude Code提供了一个分析仪表板，帮助组织了解开发者使用模式，跟踪生产力指标，并优化他们的Claude Code采用情况。

分析功能目前仅适用于通过Anthropic控制台使用Anthropic API的Claude Code组织。

## 访问分析

导航到分析仪表板：[**console.anthropic.com/claude\_code**](https://console.anthropic.com/claude_code)。

### 所需角色

*   **主要所有者**
    
*   **所有者**
    
*   **计费**
    
*   **管理员**
    
*   **开发者**
    

具有**用户**、**Claude Code用户**或**成员管理员**角色的用户无法访问分析。

## 可用指标

### 接受的代码行数

用户在会话中接受的由Claude Code编写的代码总行数。

*   排除被拒绝的代码建议
    
*   不跟踪后续删除
    

### 建议接受率

用户接受代码编辑工具使用的百分比，包括：

*   编辑
    
*   多重编辑
    
*   写入
    
*   笔记本编辑
    

### 活动

**用户**：给定日期的活跃用户数量（左侧Y轴上的数字）

**会话**：给定日期的活跃会话数量（右侧Y轴上的数字）

### 支出

**用户**：给定日期的活跃用户数量（左侧Y轴上的数字）

**支出**：给定日期的总支出美元（右侧Y轴上的数字）

# Claude Code 设置

使用全局和项目级设置以及环境变量配置 Claude Code。

Claude Code 提供多种设置来配置其行为以满足您的需求。您可以通过在使用交互式 REPL 时运行 `/config` 命令来配置 Claude Code。

## 设置文件

`settings.json` 文件是我们通过分层设置配置 Claude Code 的官方机制：

*   **用户设置** 在 `~/.claude/settings.json` 中定义，适用于所有项目。
    
*   **项目设置** 保存在您的项目目录中：
    
    *   `.claude/settings.json` 用于检入源代码控制并与团队共享的设置
        
    *   `.claude/settings.local.json` 用于不检入的设置，适用于个人偏好和实验。Claude Code 会在创建时配置 git 忽略 `.claude/settings.local.json`。
    
*   对于 Claude Code 的企业部署，我们还支持**企业管理策略设置**。这些设置优先于用户和项目设置。系统管理员可以在 macOS 上将策略部署到 `/Library/Application Support/ClaudeCode/managed-settings.json`，在 Linux 和通过 WSL 的 Windows 上部署到 `/etc/claude-code/managed-settings.json`。
    

Example settings.json

```json
{
  "permissions": {
    "allow": [
      "Bash(npm run lint)",
      "Bash(npm run test:*)",
      "Read(~/.zshrc)"
    ],
    "deny": [
      "Bash(curl:*)"
    ]
  },
  "env": {
    "CLAUDE_CODE_ENABLE_TELEMETRY": "1",
    "OTEL_METRICS_EXPORTER": "otlp"
  }
}

```

### 可用设置

`settings.json` 支持多个选项：

| **键** | **描述** | **示例** |
| --- | --- | --- |
| `apiKeyHelper` | 自定义脚本，在 `/bin/sh` 中执行，用于生成认证值。此值通常作为模型请求的 `X-Api-Key`、`Authorization: Bearer` 和 `Proxy-Authorization: Bearer` 头发送 | `/bin/generate_temp_api_key.sh` |
| `cleanupPeriodDays` | 本地保留聊天记录的时间长度（默认：30 天） | `20` |
| `env` | 将应用于每个会话的环境变量 | `{"FOO": "bar"}` |
| `includeCoAuthoredBy` | 是否在 git 提交和拉取请求中包含 `co-authored-by Claude` 署名（默认：`true`） | `false` |
| `permissions` | 权限结构见下表。 |  |

### 权限设置

| **键** | **描述** | **示例** |
| --- | --- | --- |
| `allow` | 允许工具使用的[**权限规则**](https://docs.anthropic.com/zh-CN/docs/claude-code/iam#configuring-permissions)数组 | `[ "Bash(git diff:*)" ]` |
| `deny` | 拒绝工具使用的[**权限规则**](https://docs.anthropic.com/zh-CN/docs/claude-code/iam#configuring-permissions)数组 | `[ "WebFetch", "Bash(curl:*)" ]` |
| `additionalDirectories` | Claude 可以访问的额外[**工作目录**](https://docs.anthropic.com/zh-CN/docs/claude-code/iam#working-directories) | `[ "../docs/" ]` |
| `defaultMode` | 打开 Claude Code 时的默认[**权限模式**](https://docs.anthropic.com/zh-CN/docs/claude-code/iam#permission-modes) | `"allowEdits"` |
| `disableBypassPermissionsMode` | 设置为 `"disable"` 以防止激活 `bypassPermissions` 模式。参见[**管理策略设置**](https://docs.anthropic.com/zh-CN/docs/claude-code/iam#enterprise-managed-policy-settings) | `"disable"` |

### 设置优先级

设置按优先级顺序应用：

1.  企业策略（参见 [**IAM 文档**](https://docs.anthropic.com/zh-CN/docs/claude-code/iam#enterprise-managed-policy-settings)）
    
2.  命令行参数
    
3.  本地项目设置
    
4.  共享项目设置
    
5.  用户设置
    

## 环境变量

Claude Code 支持以下环境变量来控制其行为：

所有环境变量也可以在 [`**settings.json**`](https://docs.anthropic.com/zh-CN/docs/claude-code/settings#available-settings) 中配置。这作为为每个会话自动设置环境变量的方式很有用，或者为整个团队或组织推出一组环境变量。

| **变量** | **目的** |
| --- | --- |
| `ANTHROPIC_API_KEY` | 作为 `X-Api-Key` 头发送的 API 密钥，通常用于 Claude SDK（对于交互式使用，运行 `/login`） |
| `ANTHROPIC_AUTH_TOKEN` | `Authorization` 和 `Proxy-Authorization` 头的自定义值（您在此处设置的值将以 `Bearer` 为前缀） |
| `ANTHROPIC_CUSTOM_HEADERS` | 您想要添加到请求中的自定义头（以 `Name: Value` 格式） |
| `ANTHROPIC_MODEL` | 要使用的自定义模型名称（参见[**模型配置**](https://docs.anthropic.com/zh-CN/docs/claude-code/bedrock-vertex-proxies#model-configuration)） |
| `ANTHROPIC_SMALL_FAST_MODEL` | 用于后台任务的 [**Haiku 类模型**](https://docs.anthropic.com/zh-CN/docs/claude-code/costs)名称 |
| `BASH_DEFAULT_TIMEOUT_MS` | 长时间运行的 bash 命令的默认超时时间 |
| `BASH_MAX_TIMEOUT_MS` | 模型可以为长时间运行的 bash 命令设置的最大超时时间 |
| `BASH_MAX_OUTPUT_LENGTH` | bash 输出在中间截断之前的最大字符数 |
| `CLAUDE_BASH_MAINTAIN_PROJECT_WORKING_DIR` | 在每个 Bash 命令后返回到原始工作目录 |
| `CLAUDE_CODE_API_KEY_HELPER_TTL_MS` | 凭据应刷新的间隔时间（以毫秒为单位）（使用 `apiKeyHelper` 时） |
| `CLAUDE_CODE_MAX_OUTPUT_TOKENS` | 为大多数请求设置最大输出令牌数 |
| `CLAUDE_CODE_USE_BEDROCK` | 使用 Bedrock（参见 [**Bedrock & Vertex**](https://docs.anthropic.com/zh-CN/docs/claude-code/bedrock-vertex-proxies)） |
| `CLAUDE_CODE_USE_VERTEX` | 使用 Vertex（参见 [**Bedrock & Vertex**](https://docs.anthropic.com/zh-CN/docs/claude-code/bedrock-vertex-proxies)） |
| `CLAUDE_CODE_SKIP_BEDROCK_AUTH` | 跳过 Bedrock 的 AWS 认证（例如使用 LLM 网关时） |
| `CLAUDE_CODE_SKIP_VERTEX_AUTH` | 跳过 Vertex 的 Google 认证（例如使用 LLM 网关时） |
| `CLAUDE_CODE_DISABLE_NONESSENTIAL_TRAFFIC` | 等同于设置 `DISABLE_AUTOUPDATER`、`DISABLE_BUG_COMMAND`、`DISABLE_ERROR_REPORTING` 和 `DISABLE_TELEMETRY` |
| `DISABLE_AUTOUPDATER` | 设置为 `1` 以禁用自动更新器 |
| `DISABLE_BUG_COMMAND` | 设置为 `1` 以禁用 `/bug` 命令 |
| `DISABLE_COST_WARNINGS` | 设置为 `1` 以禁用成本警告消息 |
| `DISABLE_ERROR_REPORTING` | 设置为 `1` 以选择退出 Sentry 错误报告 |
| `DISABLE_NON_ESSENTIAL_MODEL_CALLS` | 设置为 `1` 以禁用非关键路径的模型调用，如风味文本 |
| `DISABLE_TELEMETRY` | 设置为 `1` 以选择退出 Statsig 遥测（注意 Statsig 事件不包括用户数据，如代码、文件路径或 bash 命令） |
| `HTTP_PROXY` | 为网络连接指定 HTTP 代理服务器 |
| `HTTPS_PROXY` | 为网络连接指定 HTTPS 代理服务器 |
| `MAX_THINKING_TOKENS` | 为模型预算强制思考 |
| `MCP_TIMEOUT` | MCP 服务器启动的超时时间（以毫秒为单位） |
| `MCP_TOOL_TIMEOUT` | MCP 工具执行的超时时间（以毫秒为单位） |
| `MAX_MCP_OUTPUT_TOKENS` | MCP 工具响应中允许的最大令牌数（默认：25000） |

## 配置选项

我们正在将全局配置迁移到 `settings.json`。

`claude config` 将被弃用，取而代之的是 [**settings.json**](https://docs.anthropic.com/zh-CN/docs/claude-code/settings#settings-files)

要管理您的配置，请使用以下命令：

*   列出设置：`claude config list`
    
*   查看设置：`claude config get <key>`
    
*   更改设置：`claude config set <key> <value>`
    
*   推送到设置（对于列表）：`claude config add <key> <value>`
    
*   从设置中移除（对于列表）：`claude config remove <key> <value>`
    

默认情况下，`config` 更改您的项目配置。要管理您的全局配置，请使用 `--global`（或 `-g`）标志。

### 全局配置

要设置全局配置，请使用 `claude config set -g <key> <value>`：

| **键** | **描述** | **示例** |
| --- | --- | --- |
| `autoUpdates` | 是否启用自动更新（默认：`true`） | `false` |
| `preferredNotifChannel` | 您希望接收通知的位置（默认：`iterm2`） | `iterm2`、`iterm2_with_bell`、`terminal_bell` 或 `notifications_disabled` |
| `theme` | 颜色主题 | `dark`、`light`、`light-daltonized` 或 `dark-daltonized` |
| `verbose` | 是否显示完整的 bash 和命令输出（默认：`false`） | `true` |

## Claude 可用的工具

Claude Code 可以访问一组强大的工具，帮助它理解和修改您的代码库：

| **工具** | **描述** | **需要权限** |
| --- | --- | --- |
| **Agent** | 运行子代理来处理复杂的多步骤任务 | 否 |
| **Bash** | 在您的环境中执行 shell 命令 | 是 |
| **Edit** | 对特定文件进行有针对性的编辑 | 是 |
| **Glob** | 基于模式匹配查找文件 | 否 |
| **Grep** | 在文件内容中搜索模式 | 否 |
| **LS** | 列出文件和目录 | 否 |
| **MultiEdit** | 对单个文件原子性地执行多个编辑 | 是 |
| **NotebookEdit** | 修改 Jupyter notebook 单元格 | 是 |
| **NotebookRead** | 读取和显示 Jupyter notebook 内容 | 否 |
| **Read** | 读取文件内容 | 否 |
| **TodoRead** | 读取当前会话的任务列表 | 否 |
| **TodoWrite** | 创建和管理结构化任务列表 | 否 |
| **WebFetch** | 从指定 URL 获取内容 | 是 |
| **WebSearch** | 执行带域名过滤的网络搜索 | 是 |
| **Write** | 创建或覆盖文件 | 是 |

权限规则可以使用 `/allowed-tools` 或在[**权限设置**](https://docs.anthropic.com/zh-CN/docs/claude-code/settings#available-settings)中配置。

### 使用钩子扩展工具

您可以使用 [**Claude Code 钩子**](https://docs.anthropic.com/zh-CN/docs/claude-code/hooks)在任何工具执行之前或之后运行自定义命令。

例如，您可以在 Claude 修改 Python 文件后自动运行 Python 格式化程序，或者通过阻止对某些路径的写入操作来防止修改生产配置文件。

## 另请参阅

*   [**身份和访问管理**](https://docs.anthropic.com/zh-CN/docs/claude-code/iam#configuring-permissions) - 了解 Claude Code 的权限系统
    
*   [**IAM 和访问控制**](https://docs.anthropic.com/zh-CN/docs/claude-code/iam#enterprise-managed-policy-settings) - 企业策略管理
    
*   [**故障排除**](https://docs.anthropic.com/zh-CN/docs/claude-code/troubleshooting#auto-updater-issues) - 常见配置问题的解决方案
    

# 将 Claude Code 添加到您的 IDE

了解如何将 Claude Code 添加到您喜爱的 IDE

Claude Code 与流行的集成开发环境 (IDE) 无缝集成，以增强您的编码工作流程。这种集成允许您直接在您首选的开发环境中利用 Claude 的功能。

## 支持的 IDE

Claude Code 目前支持两个主要的 IDE 系列：

*   **Visual Studio Code**（包括 Cursor 和 Windsurf 等流行分支）
    
*   **JetBrains IDEs**（包括 PyCharm、WebStorm、IntelliJ 和 GoLand）
    

## 功能

*   **快速启动**：使用 `Cmd+Esc`（Mac）或 `Ctrl+Esc`（Windows/Linux）直接从编辑器打开 Claude Code，或点击 UI 中的 Claude Code 按钮
    
*   **差异查看**：代码更改可以直接在 IDE 差异查看器中显示，而不是在终端中。您可以在 `/config` 中配置此功能
    
*   **选择上下文**：IDE 中的当前选择/标签页会自动与 Claude Code 共享
    
*   **文件引用快捷键**：使用 `Cmd+Option+K`（Mac）或 `Alt+Ctrl+K`（Linux/Windows）插入文件引用（例如，@File#L1-99）
    
*   **诊断共享**：IDE 中的诊断错误（lint、语法等）会在您工作时自动与 Claude 共享
    

## 安装

### VS Code

1.  打开 VSCode
    
2.  打开集成终端
    
3.  运行 `claude` - 扩展将自动安装
    

今后您也可以在任何外部终端中使用 `/ide` 命令连接到 IDE。

这些安装说明也适用于 VS Code 分支，如 Cursor 和 Windsurf。

### JetBrains IDEs

从市场安装 [**Claude Code 插件**](https://docs.anthropic.com/s/claude-code-jetbrains) 并重启您的 IDE。

当您在集成终端中运行 `claude` 时，插件也可能会自动安装。必须完全重启 IDE 才能生效。

**远程开发限制**：使用 JetBrains 远程开发时，您必须通过 `Settings > Plugin (Host)` 在远程主机中安装插件。

## 配置

两种集成都与 Claude Code 的配置系统兼容。要启用 IDE 特定功能：

1.  通过在内置终端中运行 `claude` 将 Claude Code 连接到您的 IDE
    
2.  运行 `/config` 命令
    
3.  将差异工具设置为 `auto` 以进行自动 IDE 检测
    
4.  Claude Code 将根据您的 IDE 自动使用适当的查看器
    

如果您使用外部终端（而不是 IDE 的内置终端），您仍然可以在启动 Claude Code 后使用 `/ide` 命令连接到您的 IDE。这允许您即使从单独的终端应用程序运行 Claude 时也能受益于 IDE 集成功能。这适用于 VS Code 和 JetBrains IDEs。

使用外部终端时，为确保 Claude 默认访问与您的 IDE 相同的文件，请从与您的 IDE 项目根目录相同的目录启动 Claude。

## 故障排除

### VS Code 扩展未安装

*   确保您从 VS Code 的集成终端运行 Claude Code
    
*   确保安装了与您的 IDE 对应的 CLI：
    
    *   对于 VS Code：`code` 命令应该可用
        
    *   对于 Cursor：`cursor` 命令应该可用
        
    *   对于 Windsurf：`windsurf` 命令应该可用
        
    *   如果未安装，使用 `Cmd+Shift+P`（Mac）或 `Ctrl+Shift+P`（Windows/Linux）并搜索”Shell Command: Install ‘code’ command in PATH”（或您的 IDE 的等效命令）
    
*   检查 VS Code 是否有安装扩展的权限
    

### JetBrains 插件不工作

*   确保您从项目根目录运行 Claude Code
    
*   检查 JetBrains 插件是否在 IDE 设置中启用
    
*   完全重启 IDE。您可能需要多次执行此操作
    
*   对于 JetBrains 远程开发，确保 Claude Code 插件安装在远程主机中，而不是本地客户端上
    

如需更多帮助，请参考我们的[**故障排除指南**](https://docs.anthropic.com/zh-CN/docs/claude-code/troubleshooting)或联系支持。

# 优化您的终端设置

Claude Code在终端正确配置时效果最佳。遵循这些指南来优化您的体验。

### 主题和外观

Claude无法控制您终端的主题。这由您的终端应用程序处理。您可以随时通过`/config`命令将Claude Code的主题与您的终端匹配。

### 换行

您有几种选项可以在Claude Code中输入换行符：

*   **快速转义**：输入`\`然后按Enter键创建新行
    
*   **键盘快捷键**：设置键绑定来插入新行
    

#### 设置Shift+Enter（VS Code或iTerm2）：

在Claude Code中运行`/terminal-setup`来自动配置Shift+Enter。

#### 设置Option+Enter（VS Code、iTerm2或macOS Terminal.app）：

**对于Mac Terminal.app：**

1.  打开设置 → 配置文件 → 键盘
    
2.  勾选”使用Option作为Meta键”
    

**对于iTerm2和VS Code终端：**

1.  打开设置 → 配置文件 → 键
    
2.  在常规下，将左/右Option键设置为”Esc+“
    

### 通知设置

通过正确的通知配置，永远不会错过Claude完成任务的时机：

#### 终端铃声通知

在任务完成时启用声音警报：

```sh
claude config set --global preferredNotifChannel terminal_bell

```

**对于macOS用户**：不要忘记在系统设置 → 通知 → \[您的终端应用\]中启用通知权限。

#### iTerm 2系统通知

对于iTerm 2在任务完成时的警报：

1.  打开iTerm 2偏好设置
    
2.  导航到配置文件 → 终端
    
3.  启用”静音铃声”和过滤警报 → “发送转义序列生成的警报”
    
4.  设置您偏好的通知延迟
    

请注意，这些通知特定于iTerm 2，在默认的macOS终端中不可用。

#### 自定义通知钩子

对于高级通知处理，您可以创建[**通知钩子**](https://docs.anthropic.com/zh-CN/docs/claude-code/hooks#notification)来运行您自己的逻辑。

### 处理大型输入

在处理大量代码或长指令时：

*   **避免直接粘贴**：Claude Code可能难以处理非常长的粘贴内容
    
*   **使用基于文件的工作流程**：将内容写入文件并要求Claude读取它
    
*   **注意VS Code限制**：VS Code终端特别容易截断长粘贴
    

### Vim模式

Claude Code支持Vim键绑定的子集，可以通过`/vim`启用或通过`/config`配置。

支持的子集包括：

*   模式切换：`Esc`（到NORMAL），`i`/`I`，`a`/`A`，`o`/`O`（到INSERT）
    
*   导航：`h`/`j`/`k`/`l`，`w`/`e`/`b`，`0`/`$`/`^`，`gg`/`G`
    
*   编辑：`x`，`dw`/`de`/`db`/`dd`/`D`，`cw`/`ce`/`cb`/`cc`/`C`，`.`（重复）
    

# 管理 Claude 的内存

了解如何使用不同的内存位置和最佳实践来管理 Claude Code 跨会话的内存。

Claude Code 可以跨会话记住您的偏好设置，比如样式指南和工作流程中的常用命令。

## 确定内存类型

Claude Code 提供三种内存位置，每种都有不同的用途：

| **内存类型** | **位置** | **用途** | **使用案例示例** |
| --- | --- | --- | --- |
| **项目内存** | `./CLAUDE.md` | 项目的团队共享指令 | 项目架构、编码标准、常见工作流程 |
| **用户内存** | `~/.claude/CLAUDE.md` | 所有项目的个人偏好设置 | 代码样式偏好、个人工具快捷方式 |
| **项目内存（本地）** | `./CLAUDE.local.md` | 个人项目特定偏好设置 | _（已弃用，见下文）_ 您的沙盒 URL、首选测试数据 |

所有内存文件在启动 Claude Code 时都会自动加载到上下文中。

## CLAUDE.md 导入

CLAUDE.md 文件可以使用 `@path/to/import` 语法导入其他文件。以下示例导入了 3 个文件：

```shell
查看 @README 了解项目概述，查看 @package.json 了解此项目可用的 npm 命令。

# 附加说明
- git 工作流程 @docs/git-instructions.md
```

相对路径和绝对路径都是允许的。特别是，导入用户主目录中的文件是让团队成员提供不会检入存储库的个人指令的便捷方式。以前 CLAUDE.local.md 有类似的用途，但现在已弃用，改用导入功能，因为它们在多个 git 工作树中工作得更好。

```shell
# 个人偏好设置
- @~/.claude/my-project-instructions.md
```

为了避免潜在的冲突，导入不会在 markdown 代码段和代码块内进行评估。

```shell
此代码段不会被视为导入：`@anthropic-ai/claude-code`
```

导入的文件可以递归导入其他文件，最大深度为 5 跳。您可以通过运行 `/memory` 命令查看加载了哪些内存文件。

## Claude 如何查找内存

Claude Code 递归读取内存：从当前工作目录开始，Claude Code 向上递归到（但不包括）根目录 _/_ 并读取它找到的任何 CLAUDE.md 或 CLAUDE.local.md 文件。这在大型存储库中工作时特别方便，您在 _foo/bar/_ 中运行 Claude Code，并且在 _foo/CLAUDE.md_ 和 _foo/bar/CLAUDE.md_ 中都有内存。

Claude 还会发现嵌套在当前工作目录下子树中的 CLAUDE.md。它们不会在启动时加载，只有当 Claude 读取这些子树中的文件时才会包含。

## 使用 

## `**#**` 快捷方式快速添加内存

添加内存的最快方法是在输入开头使用 `#` 字符：

```shell
# 始终使用描述性变量名
```

系统会提示您选择要将此内容存储在哪个内存文件中。

## 使用 

## `**/memory**` 直接编辑内存

在会话期间使用 `/memory` 斜杠命令在系统编辑器中打开任何内存文件，以进行更广泛的添加或组织。

## 设置项目内存

假设您想要设置一个 CLAUDE.md 文件来存储重要的项目信息、约定和常用命令。

使用以下命令为您的代码库引导一个 CLAUDE.md：

```shell
> /init
```

提示：

*   包含常用命令（构建、测试、代码检查）以避免重复搜索
    
*   记录代码样式偏好和命名约定
    
*   添加项目特定的重要架构模式
    
*   CLAUDE.md 内存可用于与团队共享的指令和您的个人偏好设置。
    

## 内存最佳实践

*   **要具体**：“使用 2 空格缩进”比”正确格式化代码”更好。
    
*   **使用结构来组织**：将每个单独的内存格式化为项目符号，并在描述性 markdown 标题下对相关内存进行分组。
    
*   **定期审查**：随着项目的发展更新内存，以确保 Claude 始终使用最新的信息和上下文。
    

# CLI 参考

Claude Code 命令行界面的完整参考，包括命令和标志。

## CLI 命令

| **命令** | **描述** | **示例** |
| --- | --- | --- |
| `claude` | 启动交互式 REPL | `claude` |
| `claude "query"` | 使用初始提示启动 REPL | `claude "explain this project"` |
| `claude -p "query"` | 通过 SDK 查询，然后退出 | `claude -p "explain this function"` |
| `cat file \| claude -p "query"` | 处理管道内容 | `cat logs.txt \| claude -p "explain"` |
| `claude -c` | 继续最近的对话 | `claude -c` |
| `claude -c -p "query"` | 通过 SDK 继续 | `claude -c -p "Check for type errors"` |
| `claude -r "<session-id>" "query"` | 通过 ID 恢复会话 | `claude -r "abc123" "Finish this PR"` |
| `claude update` | 更新到最新版本 | `claude update` |
| `claude mcp` | 配置模型上下文协议 (MCP) 服务器 | 请参阅 [**Claude Code MCP 文档**](https://docs.anthropic.com/zh-CN/docs/claude-code/mcp)。 |

## CLI 标志

使用这些命令行标志自定义 Claude Code 的行为：

| **标志** | **描述** | **示例** |
| --- | --- | --- |
| `--add-dir` | 添加额外的工作目录供 Claude 访问（验证每个路径是否作为目录存在） | `claude --add-dir ../apps ../lib` |
| `--allowedTools` | 除了 [**settings.json 文件**](https://docs.anthropic.com/zh-CN/docs/claude-code/settings) 之外，应该在不提示用户许可的情况下允许的工具列表 | `"Bash(git log:*)" "Bash(git diff:*)" "Read"` |
| `--disallowedTools` | 除了 [**settings.json 文件**](https://docs.anthropic.com/zh-CN/docs/claude-code/settings) 之外，应该在不提示用户许可的情况下禁止的工具列表 | `"Bash(git log:*)" "Bash(git diff:*)" "Edit"` |
| `--print`, `-p` | 打印响应而不使用交互模式（有关编程使用详细信息，请参阅 [**SDK 文档**](https://docs.anthropic.com/zh-CN/docs/claude-code/sdk)） | `claude -p "query"` |
| `--output-format` | 指定打印模式的输出格式（选项：`text`、`json`、`stream-json`） | `claude -p "query" --output-format json` |
| `--input-format` | 指定打印模式的输入格式（选项：`text`、`stream-json`） | `claude -p --output-format json --input-format stream-json` |
| `--verbose` | 启用详细日志记录，显示完整的逐轮输出（在打印和交互模式下都有助于调试） | `claude --verbose` |
| `--max-turns` | 限制非交互模式下的代理轮数 | `claude -p --max-turns 3 "query"` |
| `--model` | 使用最新模型的别名（`sonnet` 或 `opus`）或模型的全名为当前会话设置模型 | `claude --model claude-sonnet-4-20250514` |
| `--permission-mode` | 在指定的 [**权限模式**](https://docs.anthropic.com/zh-CN/docs/claude-code/iam#permission-modes) 下开始 | `claude --permission-mode plan` |
| `--permission-prompt-tool` | 指定一个 MCP 工具来处理非交互模式下的权限提示 | `claude -p --permission-prompt-tool mcp_auth_tool "query"` |
| `--resume` | 通过 ID 恢复特定会话，或在交互模式下选择 | `claude --resume abc123 "query"` |
| `--continue` | 在当前目录中加载最近的对话 | `claude --continue` |
| `--dangerously-skip-permissions` | 跳过权限提示（谨慎使用） | `claude --dangerously-skip-permissions` |

`--output-format json` 标志对于脚本编写和自动化特别有用，允许您以编程方式解析 Claude 的响应。

有关打印模式（`-p`）的详细信息，包括输出格式、流式传输、详细日志记录和编程使用，请参阅 [**SDK 文档**](https://docs.anthropic.com/zh-CN/docs/claude-code/sdk)。

# 交互模式

Claude Code 会话中键盘快捷键、输入模式和交互功能的完整参考。

## 键盘快捷键

### 通用控制

| **快捷键** | **描述** | **上下文** |
| --- | --- | --- |
| `Ctrl+C` | 取消当前输入或生成 | 标准中断 |
| `Ctrl+D` | 退出 Claude Code 会话 | EOF 信号 |
| `Ctrl+L` | 清除终端屏幕 | 保留对话历史 |
| `上/下箭头` | 导航命令历史 | 回调之前的输入 |
| `Esc` + `Esc` | 编辑上一条消息 | 双击 Escape 键修改 |

### 多行输入

| **方法** | **快捷键** | **上下文** |
| --- | --- | --- |
| 快速转义 | `\` + `Enter` | 在所有终端中工作 |
| macOS 默认 | `Option+Enter` | macOS 上的默认设置 |
| 终端设置 | `Shift+Enter` | 在 `/terminal-setup` 之后 |
| 粘贴模式 | 直接粘贴 | 用于代码块、日志 |

### 快速命令

| **快捷键** | **描述** | **注释** |
| --- | --- | --- |
| 开头的 `#` | 内存快捷键 - 添加到 CLAUDE.md | 提示文件选择 |
| 开头的 `/` | 斜杠命令 | 参见 [**斜杠命令**](https://docs.anthropic.com/zh-CN/docs/claude-code/slash-commands) |

## Vim 模式

使用 `/vim` 命令启用 vim 风格编辑，或通过 `/config` 永久配置。

### 模式切换

| **命令** | **动作** | **从模式** |
| --- | --- | --- |
| `Esc` | 进入 NORMAL 模式 | INSERT |
| `i` | 在光标前插入 | NORMAL |
| `I` | 在行首插入 | NORMAL |
| `a` | 在光标后插入 | NORMAL |
| `A` | 在行尾插入 | NORMAL |
| `o` | 在下方打开新行 | NORMAL |
| `O` | 在上方打开新行 | NORMAL |

### 导航（NORMAL 模式）

| **命令** | **动作** |
| --- | --- |
| `h`/`j`/`k`/`l` | 向左/下/上/右移动 |
| `w` | 下一个单词 |
| `e` | 单词末尾 |
| `b` | 上一个单词 |
| `0` | 行首 |
| `$` | 行尾 |
| `^` | 第一个非空白字符 |
| `gg` | 输入开头 |
| `G` | 输入结尾 |

### 编辑（NORMAL 模式）

| **命令** | **动作** |
| --- | --- |
| `x` | 删除字符 |
| `dd` | 删除行 |
| `D` | 删除到行尾 |
| `dw`/`de`/`db` | 删除单词/到末尾/向后 |
| `cc` | 更改行 |
| `C` | 更改到行尾 |
| `cw`/`ce`/`cb` | 更改单词/到末尾/向后 |
| `.` | 重复上次更改 |

在终端设置中配置您首选的换行行为。运行 `/terminal-setup` 为 iTerm2 和 VSCode 终端安装 Shift+Enter 绑定。

## 命令历史

Claude Code 为当前会话维护命令历史：

*   历史按工作目录存储
    
*   使用 `/clear` 命令清除
    
*   使用上/下箭头导航（参见上面的键盘快捷键）
    
*   **Ctrl+R**：反向搜索历史（如果终端支持）
    
*   **注意**：历史扩展（`!`）默认禁用
    

# 斜杠命令

在交互式会话中使用斜杠命令控制 Claude 的行为。

## 内置斜杠命令

| **命令** | **用途** |
| --- | --- |
| `/add-dir` | 添加额外的工作目录 |
| `/bug` | 报告错误（将对话发送给 Anthropic） |
| `/clear` | 清除对话历史 |
| `/compact [instructions]` | 压缩对话，可选择性地提供重点指令 |
| `/config` | 查看/修改配置 |
| `/cost` | 显示令牌使用统计 |
| `/doctor` | 检查您的 Claude Code 安装的健康状况 |
| `/help` | 获取使用帮助 |
| `/init` | 使用 CLAUDE.md 指南初始化项目 |
| `/login` | 切换 Anthropic 账户 |
| `/logout` | 从您的 Anthropic 账户登出 |
| `/mcp` | 管理 MCP 服务器连接和 OAuth 身份验证 |
| `/memory` | 编辑 CLAUDE.md 内存文件 |
| `/model` | 选择或更改 AI 模型 |
| `/permissions` | 查看或更新[**权限**](https://docs.anthropic.com/zh-CN/docs/claude-code/iam#configuring-permissions) |
| `/pr_comments` | 查看拉取请求评论 |
| `/review` | 请求代码审查 |
| `/status` | 查看账户和系统状态 |
| `/terminal-setup` | 安装 Shift+Enter 键绑定用于换行（仅限 iTerm2 和 VSCode） |
| `/vim` | 进入 vim 模式，在插入和命令模式之间切换 |

# 钩子

通过注册shell命令来自定义和扩展Claude Code的行为

# 介绍

Claude Code钩子是用户定义的shell命令，在Claude Code生命周期的各个点执行。钩子提供对Claude Code行为的确定性控制，确保某些操作总是发生，而不是依赖LLM选择运行它们。

示例用例包括：

*   **通知**：自定义当Claude Code等待您的输入或运行某些内容的权限时如何获得通知。
    
*   **自动格式化**：在每次文件编辑后对.ts文件运行`prettier`，对.go文件运行`gofmt`等。
    
*   **日志记录**：跟踪和计算所有执行的命令以用于合规性或调试。
    
*   **反馈**：当Claude Code产生不遵循您的代码库约定的代码时提供自动反馈。
    
*   **自定义权限**：阻止对生产文件或敏感目录的修改。
    

通过将这些规则编码为钩子而不是提示指令，您将建议转换为每次预期运行时都会执行的应用程序级代码。

钩子在没有确认的情况下以您的完整用户权限执行shell命令。您有责任确保您的钩子是安全可靠的。Anthropic不对因钩子使用而导致的任何数据丢失或系统损坏承担责任。请查看[**安全考虑**](https://docs.anthropic.com/zh-CN/docs/claude-code/hooks#security-considerations)。

## 快速开始

在这个快速开始中，您将添加一个钩子来记录Claude Code运行的shell命令。

快速开始先决条件：安装`jq`用于命令行中的JSON处理。

### 步骤1：打开钩子配置

运行`/hooks` [**斜杠命令**](https://docs.anthropic.com/zh-CN/docs/claude-code/slash-commands)并选择`PreToolUse`钩子事件。

`PreToolUse`钩子在工具调用之前运行，可以阻止它们同时向Claude提供关于如何做不同事情的反馈。

### 步骤2：添加匹配器

选择`+ Add new matcher…`仅在Bash工具调用上运行您的钩子。

为匹配器输入`Bash`。

### 步骤3：添加钩子

选择`+ Add new hook…`并输入此命令：

```bash
jq -r '"\(.tool_input.command) - \(.tool_input.description // "No description")"' >> ~/.claude/bash-command-log.txt

```

### 步骤4：保存您的配置

对于存储位置，选择`User settings`，因为您要记录到您的主目录。然后此钩子将应用于所有项目，而不仅仅是您当前的项目。

然后按Esc直到返回到REPL。您的钩子现在已注册！

### 步骤5：验证您的钩子

再次运行`/hooks`或检查`~/.claude/settings.json`以查看您的配置：

```json
"hooks": {
  "PreToolUse": [
    {
      "matcher": "Bash",
      "hooks": [
        {
          "type": "command",
          "command": "jq -r '\"\(.tool_input.command) - \(.tool_input.description // \"No description\")\"' >> ~/.claude/bash-command-log.txt"
        }
      ]
    }
  ]
}

```

## 配置

Claude Code钩子在您的[**设置文件**](https://docs.anthropic.com/zh-CN/docs/claude-code/settings)中配置：

*   `~/.claude/settings.json` - 用户设置
    
*   `.claude/settings.json` - 项目设置
    
*   `.claude/settings.local.json` - 本地项目设置（不提交）
    
*   企业管理策略设置
    

### 结构

钩子按匹配器组织，其中每个匹配器可以有多个钩子：

```json
{
  "hooks": {
    "EventName": [
      {
        "matcher": "ToolPattern",
        "hooks": [
          {
            "type": "command",
            "command": "your-command-here"
          }
        ]
      }
    ]
  }
}

```

*   **matcher**：匹配工具名称的模式（仅适用于
    

`PreToolUse`和`PostToolUse`）

*   简单字符串精确匹配：`Write`仅匹配Write工具
    
*   支持正则表达式：`Edit|Write`或`Notebook.*`
    
*   如果省略或为空字符串，钩子对所有匹配事件运行
    
*   **hooks**：当模式匹配时要执行的命令数组
    
*   `type`：目前仅支持`"command"`
    
*   `command`：要执行的bash命令
    
*   `timeout`：（可选）命令应该运行多长时间（以秒为单位），然后取消所有正在进行的钩子。
    

## 钩子事件

### PreToolUse

在Claude创建工具参数之后和处理工具调用之前运行。

**常见匹配器：**

*   `Task` - 代理任务
    
*   `Bash` - Shell命令
    
*   `Glob` - 文件模式匹配
    
*   `Grep` - 内容搜索
    
*   `Read` - 文件读取
    
*   `Edit`, `MultiEdit` - 文件编辑
    
*   `Write` - 文件写入
    
*   `WebFetch`, `WebSearch` - Web操作
    

### PostToolUse

在工具成功完成后立即运行。

识别与PreToolUse相同的匹配器值。

### Notification

当Claude Code发送通知时运行。

### Stop

当主Claude Code代理完成响应时运行。

### SubagentStop

当Claude Code子代理（Task工具调用）完成响应时运行。

## 钩子输入

钩子通过stdin接收包含会话信息和事件特定数据的JSON数据：

```typescript
{
  // 通用字段
  session_id: string
  transcript_path: string  // 对话JSON的路径

  // 事件特定字段
  ...
}

```

### PreToolUse输入

`tool_input`的确切模式取决于工具。

```json
{
  "session_id": "abc123",
  "transcript_path": "~/.claude/projects/.../00893aaf-19fa-41d2-8238-13269b9b3ca0.jsonl",
  "tool_name": "Write",
  "tool_input": {
    "file_path": "/path/to/file.txt",
    "content": "file content"
  }
}

```

### PostToolUse输入

`tool_input`和`tool_response`的确切模式取决于工具。

```json
{
  "session_id": "abc123",
  "transcript_path": "~/.claude/projects/.../00893aaf-19fa-41d2-8238-13269b9b3ca0.jsonl",
  "tool_name": "Write",
  "tool_input": {
    "file_path": "/path/to/file.txt",
    "content": "file content"
  },
  "tool_response": {
    "filePath": "/path/to/file.txt",
    "success": true
  }
}

```

### Notification输入

```json
{
  "session_id": "abc123",
  "transcript_path": "~/.claude/projects/.../00893aaf-19fa-41d2-8238-13269b9b3ca0.jsonl",
  "message": "Task completed successfully",
  "title": "Claude Code"
}

```

### Stop和SubagentStop输入

当Claude Code已经由于停止钩子而继续时，`stop_hook_active`为true。检查此值或处理记录以防止Claude Code无限运行。

```json
{
  "session_id": "abc123",
  "transcript_path": "~/.claude/projects/.../00893aaf-19fa-41d2-8238-13269b9b3ca0.jsonl",
  "stop_hook_active": true
}

```

## 钩子输出

钩子有两种方式将输出返回给Claude Code。输出传达是否阻止以及应该向Claude和用户显示的任何反馈。

### 简单：退出代码

钩子通过退出代码、stdout和stderr传达状态：

*   **退出代码0**：成功。`stdout`在记录模式（CTRL-R）中显示给用户。
    
*   **退出代码2**：阻塞错误。`stderr`反馈给Claude自动处理。请参阅下面的每个钩子事件行为。
    
*   **其他退出代码**：非阻塞错误。`stderr`显示给用户，执行继续。
    

提醒：如果退出代码为0，Claude Code不会看到stdout。

#### 退出代码2行为

| **钩子事件** | **行为** |
| --- | --- |
| `PreToolUse` | 阻止工具调用，向Claude显示错误 |
| `PostToolUse` | 向Claude显示错误（工具已运行） |
| `Notification` | 不适用，仅向用户显示stderr |
| `Stop` | 阻止停止，向Claude显示错误 |
| `SubagentStop` | 阻止停止，向Claude子代理显示错误 |

### 高级：JSON输出

钩子可以在`stdout`中返回结构化JSON以获得更复杂的控制：

#### 通用JSON字段

所有钩子类型都可以包含这些可选字段：

```json
{
  "continue": true, // Claude是否应该在钩子执行后继续（默认：true）
  "stopReason": "string" // 当continue为false时显示的消息
  "suppressOutput": true, // 在记录模式中隐藏stdout（默认：false）
}

```

如果`continue`为false，Claude在钩子运行后停止处理。

*   对于`PreToolUse`，这与`"decision": "block"`不同，后者仅阻止特定工具调用并向Claude提供自动反馈。
    
*   对于`PostToolUse`，这与`"decision": "block"`不同，后者向Claude提供自动反馈。
    
*   对于`Stop`和`SubagentStop`，这优先于任何`"decision": "block"`输出。
    
*   在所有情况下，`"continue" = false`优先于任何`"decision": "block"`输出。
    

`stopReason`伴随`continue`提供显示给用户的原因，不显示给Claude。

#### `**PreToolUse**`决策控制

`PreToolUse`钩子可以控制工具调用是否继续。

*   “approve”绕过权限系统。`reason`显示给用户但不显示给Claude。
    
*   “block”阻止工具调用执行。`reason`显示给Claude。
    
*   `undefined`导致现有权限流程。`reason`被忽略。
    

```json
{
  "decision": "approve" | "block" | undefined,
  "reason": "Explanation for decision"
}

```

#### `**PostToolUse**`决策控制

`PostToolUse`钩子可以控制工具调用是否继续。

*   “block”自动用`reason`提示Claude。
    
*   `undefined`什么都不做。`reason`被忽略。
    

```json
{
  "decision": "block" | undefined,
  "reason": "Explanation for decision"
}

```

#### `**Stop**`/`**SubagentStop**`决策控制

`Stop`和`SubagentStop`钩子可以控制Claude是否必须继续。

*   “block”阻止Claude停止。您必须填充`reason`让Claude知道如何继续。
    
*   `undefined`允许Claude停止。`reason`被忽略。
    

```json
{
  "decision": "block" | undefined,
  "reason": "Must be provided when Claude is blocked from stopping"
}

```

#### JSON输出示例：Bash命令编辑

```python
#!/usr/bin/env python3
import json
import re
import sys

# 将验证规则定义为（正则表达式模式，消息）元组列表
VALIDATION_RULES = [
    (
        r"\bgrep\b(?!.*\|)",
        "Use 'rg' (ripgrep) instead of 'grep' for better performance and features",
    ),
    (
        r"\bfind\s+\S+\s+-name\b",
        "Use 'rg --files | rg pattern' or 'rg --files -g pattern' instead of 'find -name' for better performance",
    ),
]


def validate_command(command: str) -> list[str]:
    issues = []
    for pattern, message in VALIDATION_RULES:
        if re.search(pattern, command):
            issues.append(message)
    return issues


try:
    input_data = json.load(sys.stdin)
except json.JSONDecodeError as e:
    print(f"Error: Invalid JSON input: {e}", file=sys.stderr)
    sys.exit(1)

tool_name = input_data.get("tool_name", "")
tool_input = input_data.get("tool_input", {})
command = tool_input.get("command", "")

if tool_name != "Bash" or not command:
    sys.exit(1)

# 验证命令
issues = validate_command(command)

if issues:
    for message in issues:
        print(f"• {message}", file=sys.stderr)
    # 退出代码2阻止工具调用并向Claude显示stderr
    sys.exit(2)

```

## 使用MCP工具

Claude Code钩子与[**模型上下文协议（MCP）工具**](https://docs.anthropic.com/zh-CN/docs/claude-code/mcp)无缝协作。当MCP服务器提供工具时，它们以特殊的命名模式出现，您可以在钩子中匹配。

### MCP工具命名

MCP工具遵循模式`mcp__<server>__<tool>`，例如：

*   `mcp__memory__create_entities` - 内存服务器的创建实体工具
    
*   `mcp__filesystem__read_file` - 文件系统服务器的读取文件工具
    
*   `mcp__github__search_repositories` - GitHub服务器的搜索工具
    

### 为MCP工具配置钩子

您可以针对特定的MCP工具或整个MCP服务器：

```json
{
  "hooks": {
    "PreToolUse": [
      {
        "matcher": "mcp__memory__.*",
        "hooks": [
          {
            "type": "command",
            "command": "echo 'Memory operation initiated' >> ~/mcp-operations.log"
          }
        ]
      },
      {
        "matcher": "mcp__.*__write.*",
        "hooks": [
          {
            "type": "command",
            "command": "/home/user/scripts/validate-mcp-write.py"
          }
        ]
      }
    ]
  }
}

```

## 示例

### 代码格式化

在文件修改后自动格式化代码：

```json
{
  "hooks": {
    "PostToolUse": [
      {
        "matcher": "Write|Edit|MultiEdit",
        "hooks": [
          {
            "type": "command",
            "command": "/home/user/scripts/format-code.sh"
          }
        ]
      }
    ]
  }
}

```

### 通知

自定义当Claude Code请求权限或提示输入变为空闲时发送的通知。

```json
{
  "hooks": {
    "Notification": [
      {
        "matcher": "",
        "hooks": [
          {
            "type": "command",
            "command": "python3 ~/my_custom_notifier.py"
          }
        ]
      }
    ]
  }
}

```

## 安全考虑

### 免责声明

**使用风险自负**：Claude Code钩子在您的系统上自动执行任意shell命令。通过使用钩子，您承认：

*   您对配置的命令完全负责
    
*   钩子可以修改、删除或访问您的用户帐户可以访问的任何文件
    
*   恶意或编写不当的钩子可能导致数据丢失或系统损坏
    
*   Anthropic不提供任何保证，并且不对因钩子使用而导致的任何损坏承担责任
    
*   您应该在生产使用之前在安全环境中彻底测试钩子
    

在将任何钩子命令添加到您的配置之前，请始终审查和理解它们。

### 安全最佳实践

以下是编写更安全钩子的一些关键实践：

1.  **验证和清理输入** - 永远不要盲目信任输入数据
    
2.  **始终引用shell变量** - 使用`"$VAR"`而不是`$VAR`
    
3.  **阻止路径遍历** - 检查文件路径中的`..`
    
4.  **使用绝对路径** - 为脚本指定完整路径
    
5.  **跳过敏感文件** - 避免`.env`、`.git/`、密钥等。
    

### 配置安全

对设置文件中钩子的直接编辑不会立即生效。Claude Code：

1.  在启动时捕获钩子快照
    
2.  在整个会话中使用此快照
    
3.  如果钩子被外部修改则发出警告
    
4.  需要在`/hooks`菜单中审查更改才能应用
    

这防止恶意钩子修改影响您当前的会话。

## 钩子执行详细信息

*   **超时**：默认60秒执行限制，每个命令可配置。
    
    *   如果任何单个命令超时，所有正在进行的钩子都会被取消。
    
*   **并行化**：所有匹配的钩子并行运行
    
*   **环境**：在当前目录中使用Claude Code的环境运行
    
*   **输入**：通过stdin的JSON
    
*   **输出**：
    
    *   PreToolUse/PostToolUse/Stop：进度显示在记录中（Ctrl-R）
        
    *   Notification：仅记录到调试（`--debug`）
        

## 调试

要排除钩子故障：

1.  检查`/hooks`菜单是否显示您的配置
    
2.  验证您的[**设置文件**](https://docs.anthropic.com/zh-CN/docs/claude-code/settings)是有效的JSON
    
3.  手动测试命令
    
4.  检查退出代码
    
5.  审查stdout和stderr格式期望
    
6.  确保正确的引号转义
    
7.  使用`claude --debug`调试您的钩子。成功钩子的输出如下所示。
    

```plaintext
[DEBUG] Executing hooks for PostToolUse:Write
[DEBUG] Getting matching hook commands for PostToolUse with query: Write
[DEBUG] Found 1 hook matchers in settings
[DEBUG] Matched 1 hooks for query "Write"
[DEBUG] Found 1 hook commands to execute
[DEBUG] Executing hook command: <Your command> with timeout 60000ms
[DEBUG] Hook command completed with status 0: <Your stdout>

```

进度消息出现在记录模式（Ctrl-R）中，显示：

*   正在运行哪个钩子
    
*   正在执行的命令
    
*   成功/失败状态
    
*   输出或错误消息