# Roblox Dev: Ansible 코어 허브

> *"로블록스 프론티어 내 모든 구현의 중심 좌표."*

**Ansible Station**의 로블록스 개발 인프라를 총괄하는 최상위 코어 리포지토리입니다. @AnsibleMage의 모든 Roblox 게임 프로젝트에 걸쳐 공유 문서, 개발 방법론, 툴체인 가이드 및 참조 자료를 관리합니다.

---

## 주요 특징

- **중앙 집중 인프라** -- 글로벌 설정 가이드, 보안 설정, 아키텍처 문서를 한 곳에서 관리
- **자체 개발 방법론** -- Roblox/Luau에 맞춤화된 VCR(Verify-Code-Refactor) 및 CJ AI 방법론
- **재사용 가능한 템플릿** -- 게임 개발용 PRD, Block 분해, 디버깅 로그 템플릿
- **프로젝트 포트폴리오 추적** -- 모든 Roblox 게임 프로젝트의 상태 및 문서 링크
- **보안 감사 완료** -- GitHub 공개 전 종합 보안 스캔 완료

---

## 프로젝트 포트폴리오

| 프로젝트 | 상태 | 장르 | 기술 |
|---------|------|------|------|
| [Ansible Logic Jump](https://github.com/AnsibleMage/Roblox_Logic_Jump) | 런칭 완료 | 극한 고공 점프맵 / 타임 어택 | Rojo 7.6.1, Lua/Luau, Python 3 |
| [Fly Paper Plane](https://github.com/AnsibleMage/Roblox_Fly_paper_plane) | 개발 중 | 종이비행기 비행 시뮬레이션 | Rojo 7.7.0-rc.1, Lua/Luau |

---

## 프로젝트 구조

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
│       ├── VCR 개발방법론 v1.1
│       ├── CJ AI Roblox 개발방법론 v1.0
│       ├── 조사분석 보고서
│       └── 템플릿 (PRD, Block, 디버깅 로그)
├── SECURITY_AUDIT.md
└── README.md
```

---

## 문서

### 인프라 가이드

| 문서 | 설명 |
|------|------|
| [102 Setup Guide](./doc/102_Roblox_Setup_and_AI_Integration_Guide.md) | 맥북 프로 Roblox 개발 환경 구축 |
| [111 MCP Server](./doc/111_Roblox_Studio_MCP_Server_Execution_Guide.md) | Model Context Protocol 기반 AI 연결 |
| [112 Security Settings](./doc/112_Roblox_Game_Settings_and_Publish_Guide.md) | 게임 설정 및 퍼블리싱 가이드 |
| [117 Core Architecture](./doc/117_Roblox_Project_Core_Architecture_Guide.md) | 전체 프로젝트 아키텍처 및 규칙 |

### 개발 방법론

| 문서 | 설명 |
|------|------|
| [VCR 개발방법론 v1.1](./doc/Roblox_Dev%20Methodology/203_VCR_%EA%B0%9C%EB%B0%9C%EB%B0%A9%EB%B2%95%EB%A1%A0_v1.1.md) | Roblox 전용 Verify-Code-Refactor 사이클 |
| [CJ AI 개발방법론 v1.0](./doc/Roblox_Dev%20Methodology/202_CJ_AI_%EA%B0%9C%EB%B0%9C%EB%B0%A9%EB%B2%95%EB%A1%A0_Roblox_v1.0.md) | AI 협업 개발 표준 |
| [조사분석 보고서](./doc/Roblox_Dev%20Methodology/200_Roblox_%EA%B0%9C%EB%B0%9C%EB%B0%A9%EB%B2%95%EB%A1%A0_%EC%A1%B0%EC%82%AC%EB%B6%84%EC%84%9D_%EB%B3%B4%EA%B3%A0%EC%84%9C.md) | 방법론 분석 및 비교 |

---

## 기술 스택

| 분류 | 도구 |
|------|------|
| 엔진 | Roblox Studio |
| 동기화 | Rojo 7.6.1+ |
| 스크립트 | Lua / Luau |
| 자동화 | Python 3 |
| 린터 | Selene |
| 포매터 | StyLua |
| AI 프로토콜 | Model Context Protocol (MCP) |

---

## 시작하기

### 필수 도구

1. Roblox Studio (최신 버전)
2. [Rojo](https://rojo.space/) 7.6.1+
3. [Selene](https://kampf-karren.github.io/selene/) (린터)
4. [StyLua](https://github.com/JohnnyMorganz/StyLua) (포매터)

### 개발 워크플로우

```bash
# 게임 프로젝트 디렉토리로 이동
cd <project-folder>

# Rojo 동기화 서버 시작
rojo serve

# Roblox Studio에서: Plugins > Rojo > Connect
```

---

## 아키텍처

이 리포지토리는 **Core-Local 아키텍처**를 따릅니다:

- **Core Hub (`/doc`)** -- 글로벌 설정, 툴체인 가이드, 공유 방법론
- **Localized Projects** -- 각 게임은 프로젝트별 전용 문서와 함께 별도 리포지토리에서 관리

---

## 라이선스

이 프로젝트는 [MIT 라이선스](LICENSE)에 따라 배포됩니다.
