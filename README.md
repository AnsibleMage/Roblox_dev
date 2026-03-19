# Roblox Dev: The Ansible Core Hub

> *"The central coordinates for all manifestations within the Roblox frontier."*

The top-level core repository that oversees the Roblox development infrastructure for **Ansible Station**. This hub manages shared documentation, development methodologies, toolchain guides, and references across all Roblox game projects by @AnsibleMage.

---

## Key Features

- **Centralized Infrastructure** -- Global setup guides, security settings, and architecture documentation in one place
- **Custom Development Methodologies** -- VCR (Verify-Code-Refactor) and CJ AI methodology adapted for Roblox/Luau
- **Reusable Templates** -- PRD, Block decomposition, and Debugging Log templates for game development
- **Project Portfolio Tracking** -- Status and documentation links for all Roblox game projects
- **Security Audited** -- Comprehensive security scan completed before GitHub publication

---

## Project Portfolio

| Project | Status | Genre | Tech |
|---------|--------|-------|------|
| [Ansible Logic Jump](https://github.com/AnsibleMage/Roblox_Logic_Jump) | Launched | Extreme Sky Platformer / Time Attack | Rojo 7.6.1, Lua/Luau, Python 3 |
| [Fly Paper Plane](https://github.com/AnsibleMage/Roblox_Fly_paper_plane) | In Development | Paper Airplane Flight Simulation | Rojo 7.7.0-rc.1, Lua/Luau |

---

## Project Structure

```
Roblox_dev/
├── doc/
│   ├── 100_Roblox_Development_Trends_Report.md
│   ├── 102_Roblox_Setup_and_AI_Integration_Guide.md
│   ├── 103_Roblox_AI_Connection_Architecture.md
│   ├── 104_Installation_and_Permission_Guide.md
│   ├── 105_Roblox_Project_Scaffolding.md
│   ├── 111_Roblox_Studio_MCP_Server_Execution_Guide.md
│   ├── 112_Roblox_Game_Settings_and_Publish_Guide.md
│   ├── 113_Roblox_Plugin_Installation_Execution_Guide.md
│   ├── 117_Roblox_Project_Core_Architecture_Guide.md
│   └── Roblox_Dev Methodology/
│       ├── VCR Development Methodology v1.1
│       ├── CJ AI Roblox Methodology v1.0
│       ├── Research & Analysis Reports
│       └── Templates (PRD, Block, Debugging Log)
├── SECURITY_AUDIT.md
└── README.md
```

---

## Documentation

### Infrastructure Guides

| Document | Description |
|----------|-------------|
| [102 Setup Guide](./doc/102_Roblox_Setup_and_AI_Integration_Guide.md) | MacBook Pro environment setup for Roblox development |
| [111 MCP Server](./doc/111_Roblox_Studio_MCP_Server_Execution_Guide.md) | AI integration via Model Context Protocol |
| [112 Security Settings](./doc/112_Roblox_Game_Settings_and_Publish_Guide.md) | Game settings and publishing guide |
| [117 Core Architecture](./doc/117_Roblox_Project_Core_Architecture_Guide.md) | Overall project architecture and conventions |

### Development Methodology

| Document | Description |
|----------|-------------|
| [VCR Methodology v1.1](./doc/Roblox_Dev%20Methodology/203_VCR_%EA%B0%9C%EB%B0%9C%EB%B0%A9%EB%B2%95%EB%A1%A0_v1.1.md) | Verify-Code-Refactor cycle for Roblox |
| [CJ AI Methodology v1.0](./doc/Roblox_Dev%20Methodology/202_CJ_AI_%EA%B0%9C%EB%B0%9C%EB%B0%A9%EB%B2%95%EB%A1%A0_Roblox_v1.0.md) | AI-collaborative development standard |
| [Research Report](./doc/Roblox_Dev%20Methodology/200_Roblox_%EA%B0%9C%EB%B0%9C%EB%B0%A9%EB%B2%95%EB%A1%A0_%EC%A1%B0%EC%82%AC%EB%B6%84%EC%84%9D_%EB%B3%B4%EA%B3%A0%EC%84%9C.md) | Methodology analysis and comparison |

---

## Tech Stack

| Category | Tool |
|----------|------|
| Engine | Roblox Studio |
| Sync | Rojo 7.6.1+ |
| Scripts | Lua / Luau |
| Automation | Python 3 |
| Linter | Selene |
| Formatter | StyLua |
| AI Protocol | Model Context Protocol (MCP) |

---

## Getting Started

### Prerequisites

1. Roblox Studio (latest version)
2. [Rojo](https://rojo.space/) 7.6.1+
3. [Selene](https://kampf-karren.github.io/selene/) (linter)
4. [StyLua](https://github.com/JohnnyMorganz/StyLua) (formatter)

### Development Workflow

```bash
# Navigate to a game project directory
cd <project-folder>

# Start Rojo sync server
rojo serve

# In Roblox Studio: Plugins > Rojo > Connect
```

---

## Architecture

This repository follows a **Core-Local Architecture**:

- **Core Hub (`/doc`)** -- Global configuration, toolchain guides, and shared methodologies
- **Localized Projects** -- Each game lives in its own separate repository with project-specific documentation

---

## License

This project is licensed under the [MIT License](LICENSE).
