{

  "mcpServers": {

    "mcp-test": {

      "command": "mcp",

      "args": [

        "run",

        "D:/demo/mcp-test/main.py"

      ]

    },

    "supabase": {

      "url": "https://mcp.composio.dev/supabase/howling-harsh-mouse-tDzQe9"

    },

    "github": {

      "url": "https://mcp.composio.dev/github/howling-harsh-mouse-tDzQe9"

    },

    "figma-mcp": {

      "command": "npx",

      "args": [

        "figma-mcp"

      ],

      "env": {

        "FIGMA_API_KEY": "figd_Gn-X70EOrxy3QOLNZCC55jB4v1ZMgNScbpNJJ5eQ"

      }

    },

    "figma-developer-mcp": {

      "command": "npx",

      "args": [

        "-y",

        "figma-developer-mcp",

        "--stdio"

      ],

      "env": {

        "FIGMA_API_KEY": "figd_Gn-X70EOrxy3QOLNZCC55jB4v1ZMgNScbpNJJ5eQ"

      }

    },

    "browsermcp": {

      "command": "npx",

      "args": [

        "@browsermcp/mcp@latest"

      ]

    },

    "browser-tools": {

      "command": "npx",

      "args": [

        "@agentdeskai/browser-tools-server@1.2.0"

      ]

    },

    "browser-tools-mcp": {

      "command": "wsl",

      "args": [

        "bash",

        "-c",

        "cmd /c npx -y @agentdeskai/browser-tools-mcp@1.2.0"

      ],

      "enabled": true

    },

    "@21st-dev/magic": {

      "command": "cmd",

      "args": [

        "/c",

        "npx",

        "-y",

        "@21st-dev/magic@latest",

        "API_KEY=\"dbd8d2b9a9411353b813aea5bbf0d8391cb994c4a02097aa73aac72af5bd4465\""

      ]

    },

    "prompt-server": {

        "command": "node",

        "args": [

          "D:/git/mcp-prompt-server/src/index.js"

        ],

        "transport": "stdio"

    },

    "context7": {

      "command": "npx",

      "args": ["-y", "@upstash/context7-mcp"]

    },

    "sequential-thinking": {

      "command": "npx",

      "args": ["-y", "@modelcontextprotocol/server-sequential-thinking"]

    },

    "mcp-feedback-enhanced": {

      "command": "uvx",

      "args": ["mcp-feedback-enhanced@latest"],

      "timeout": 600,

      "env": {

        "FORCE_WEB": "true",

        "MCP_DEBUG": "false"

      },

      "autoApprove": ["interactive_feedback"]

    }

  }

}