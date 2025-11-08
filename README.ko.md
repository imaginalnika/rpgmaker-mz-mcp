# 🎮 RPG Maker MZ MCP 서버

<div align="center">

**완전한 RPG Maker MZ 게임 개발을 위한 MCP 서버**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Node.js Version](https://img.shields.io/badge/node-%3E%3D18.0.0-brightgreen)](https://nodejs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue)](https://www.typescriptlang.org/)

**MCP 도구만으로 RPG 게임을 완전히 제작 가능 + AI 이미지 생성 지원!**

📖 **[초보자 가이드](./GETTING_STARTED.md)** | [특징](#-특징) • [설치](#-설정) • [사용 예제](#-사용-예제) • [도구 목록](#-사용-가능한-도구)

</div>

## 🌟 특징

이 MCP 서버는 **RPG Maker MZ의 완전한 게임 개발 환경**을 프로그래밍 방식으로 제공합니다. GUI를 열지 않고도 코드나 AI 에이전트를 사용하여 본격적인 RPG 게임을 만들 수 있습니다.

### 🎯 주요 특징

- 🤖 **🆕 자율적 전자동 게임 생성**: 컨셉만 입력하면 3-7분 안에 완전한 RPG 생성!
- 🚀 **완전한 프로젝트 생성**: 처음부터 RPG Maker MZ 프로젝트 생성
- 🗺️ **맵 에디터**: 프로그래밍 방식으로 맵과 타일 편집
- 🎭 **이벤트 시스템**: 복잡한 게임 이벤트와 스토리 구현
- 📊 **데이터베이스 관리**: 액터, 스킬, 아이템 등 모든 데이터 편집
- 🎨 **AI 이미지 생성**: Gemini 2.5 Flash (nanobanana)로 게임 에셋 자동 생성
- 📖 **AI 시나리오 생성**: Gemini API로 완전한 스토리·맵·이벤트 자동 생성
- 🔧 **MCP 통합**: Model Context Protocol을 사용한 완전한 툴체인

### 🤖 자율적 전자동 게임 생성(NEW!)

**단 한 줄의 명령어로 완전한 RPG 생성!**

```bash
npx rpgmaker-mz-mcp auto-create "/games/MyRPG" "fantasy adventure with dragons"
```

**또는 Claude Code에서:**
```
"cyberpunk detective story" 컨셉으로 RPG를 자동 생성해줘
```

**자동으로 실행되는 8단계:**
1. ✅ 프로젝트 생성
2. ✅ 컨셉 분석
3. ✅ 시나리오 생성(맵·캐릭터·이벤트)
4. ✅ 전투 시스템(적·스킬)
5. ✅ 퀘스트 시스템
6. ✅ AI 이미지 에셋 생성
7. ✅ 스탯 밸런스 조정
8. ✅ 프로젝트 최적화

**⏱️ 소요 시간: 3-7분 → 바로 플레이 가능!**

자세한 내용은 [AUTONOMOUS_CREATION.md](./AUTONOMOUS_CREATION.md) 참조.

### 🎨 AI 이미지 생성(NEW!)

Gemini 2.5 Flash API를 사용하여 RPG Maker MZ용 에셋 자동 생성:

- **캐릭터 스프라이트** (144x192px, 3x4 그리드)
- **얼굴 그래픽** (144x144px, 2x2 그리드)
- **타일셋** (768x768px)
- **배틀백** (1000x740px)
- **적 그래픽** (816x624px)
- **사이드뷰 배틀러** (576x384px, 9x6 그리드)
- **픽처** (816x624px)

## 📦 사용 가능한 도구

### 🎮 프로젝트 관리
| 도구 | 설명 |
|--------|------|
| `create_project` | 새 프로젝트 생성 |
| `list_projects` | 프로젝트 목록 표시 |
| `read_project_info` | 프로젝트 정보 읽기 |
| `generate_project_context` | 컨텍스트 문서 생성 |
| `analyze_project_structure` | 프로젝트 구조 분석 |
| `extract_game_design_patterns` | 게임 디자인 패턴 추출 |

### 🗺️ 맵 편집
| 도구 | 설명 |
|--------|------|
| `create_map` | 새 맵 생성 |
| `list_maps` | 맵 목록 표시 |
| `read_map` | 맵 데이터 읽기 |
| `update_map_tile` | 타일 업데이트 |

### 🎭 이벤트 편집
| 도구 | 설명 |
|--------|------|
| `add_event` | 이벤트 추가 |
| `add_event_command` | 이벤트 명령 추가 |

**지원 이벤트 명령 예제:**
- `101` - 텍스트 표시
- `201` - 플레이어 이동
- `122` - 변수 조작
- `111` - 조건 분기
- 기타 RPG Maker MZ 전체 명령 지원

### 📊 데이터베이스 편집
| 도구 | 설명 |
|--------|------|
| `add_actor` | 액터 추가 |
| `add_class` | 클래스 추가 |
| `add_skill` | 스킬 추가 |
| `add_item` | 아이템 추가 |
| `update_database` | 전체 데이터베이스 업데이트 |

### 🎨 AI 이미지 생성
| 도구 | 설명 |
|--------|------|
| `generate_asset` | Gemini 2.5 Flash로 에셋 생성 |
| `generate_asset_batch` | 여러 에셋 일괄 생성 |
| `describe_asset` | 기존 에셋 AI 분석 |

### 🤖 자율적 게임 생성(NEW!)
| 도구 | 설명 |
|--------|------|
| `autonomous_create_game` | 컨셉에서 완전한 RPG를 자동 생성(8단계 전자동) |

### 📖 AI 시나리오 생성
| 도구 | 설명 |
|--------|------|
| `generate_scenario` | Gemini AI로 완전한 RPG 시나리오 생성 |
| `implement_scenario` | 생성된 시나리오를 프로젝트에 구현 |
| `generate_and_implement_scenario` | 시나리오 생성과 구현을 한 번에 |
| `generate_scenario_variations` | 여러 시나리오 변형 생성 |

### 🔌 플러그인 관리
| 도구 | 설명 |
|--------|------|
| `list_plugins` | 플러그인 목록 표시 |

## 🚀 설정

### 필수 사항

- Node.js 18 이상
- npm 또는 yarn
- Gemini API Key (AI 이미지 생성 사용 시)

### 설치

```bash
# 리포지토리 클론
git clone https://github.com/ShunsukeHayashi/rpgmaker-mz-mcp.git
cd rpgmaker-mz-mcp

# 의존성 설치
npm install

# 빌드
npm run build
```

### MCP 설정

Claude Desktop 또는 다른 MCP 클라이언트의 설정 파일에 추가:

```json
{
  "mcpServers": {
    "rpgmaker-mz": {
      "command": "node",
      "args": ["/path/to/rpgmaker-mz-mcp/dist/index.js"],
      "env": {
        "GEMINI_API_KEY": "your-gemini-api-key-here"
      }
    }
  }
}
```

### 환경 변수

AI 이미지 생성 기능을 사용하는 경우 다음 환경 변수 설정:

```bash
export GEMINI_API_KEY="your-api-key"
```

## 💡 사용 예제

### 기본 게임 생성 흐름

```typescript
// 1️⃣ 프로젝트 생성
create_project({
  project_path: "/path/to/MyFantasyRPG",
  game_title: "Fantasy Adventure"
})

// 2️⃣ 맵 생성
create_map({
  project_path: "/path/to/MyFantasyRPG",
  map_id: 2,
  name: "Town Square",
  width: 25,
  height: 20
})

// 3️⃣ NPC 이벤트 추가
add_event({
  project_path: "/path/to/MyFantasyRPG",
  map_id: 2,
  event_id: 1,
  name: "Town Elder",
  x: 12,
  y: 10
})

// 4️⃣ 대화 이벤트 추가
add_event_command({
  project_path: "/path/to/MyFantasyRPG",
  map_id: 2,
  event_id: 1,
  page_index: 0,
  code: 101,  // Show Text
  parameters: ["", 0, 0, 2]
})

add_event_command({
  project_path: "/path/to/MyFantasyRPG",
  map_id: 2,
  event_id: 1,
  page_index: 0,
  code: 401,  // Text continuation
  parameters: ["Welcome to our town, traveler!"]
})

// 5️⃣ 플레이어 캐릭터 추가
add_actor({
  project_path: "/path/to/MyFantasyRPG",
  id: 1,
  name: "Hero"
})

add_class({
  project_path: "/path/to/MyFantasyRPG",
  id: 1,
  name: "Warrior"
})
```

### 🎨 AI 이미지 생성 사용 예제

```typescript
// 캐릭터 스프라이트 생성
generate_asset({
  project_path: "/path/to/MyFantasyRPG",
  asset_type: "character",
  prompt: "A brave knight with silver armor and red cape, pixel art style, walking animation sprite sheet",
  filename: "Knight.png"
})

// 얼굴 그래픽 생성
generate_asset({
  project_path: "/path/to/MyFantasyRPG",
  asset_type: "face",
  prompt: "Female mage with blue robes and long purple hair, multiple expressions (normal, happy, sad, angry)",
  filename: "Mage_Face.png"
})

// 일괄 생성
generate_asset_batch({
  requests: [
    {
      project_path: "/path/to/MyFantasyRPG",
      asset_type: "enemy",
      prompt: "Fire dragon boss, menacing pose",
      filename: "Dragon.png"
    },
    {
      project_path: "/path/to/MyFantasyRPG",
      asset_type: "enemy",
      prompt: "Goblin warrior with wooden club",
      filename: "Goblin.png"
    }
  ]
})

// 기존 에셋 분석
describe_asset({
  project_path: "/path/to/MyFantasyRPG",
  asset_type: "character",
  filename: "Knight.png"
})
// → "This character sprite shows a knight in silver armor..."
```

### 📖 AI 시나리오 자동 생성(초강력!)

```typescript
// 명령어 하나로 완전한 RPG 생성!
generate_and_implement_scenario({
  project_path: "/path/to/MyFantasyRPG",
  theme: "medieval fantasy adventure with dragons",
  style: "epic and heroic",
  length: "medium"
})

// 생성되는 내용:
// - 스토리와 세계관
// - 맵(마을, 던전, 필드 등)
// - 캐릭터(주인공, 동료, NPC)
// - 이벤트(대화, 퀘스트, 전투)
// - 아이템과 스킬
// 모두 자동으로 구현됩니다!

// 여러 변형 생성하여 비교
generate_scenario_variations({
  project_path: "/path/to/MyFantasyRPG",
  theme: "cyberpunk detective story",
  style: "noir and mysterious",
  length: "short",
  count: 3
})
// → 3개의 다른 스토리를 생성하여 최적의 것을 선택
```

### 📊 프로젝트 분석

```typescript
// 프로젝트 구조 분석
analyze_project_structure({
  project_path: "/path/to/MyFantasyRPG"
})

// 컨텍스트 생성
generate_project_context({
  project_path: "/path/to/MyFantasyRPG",
  include_maps: true,
  include_events: true,
  include_plugins: true
})

// 디자인 패턴 추출
extract_game_design_patterns({
  project_path: "/path/to/MyFantasyRPG"
})
```

## 🎯 사용 사례

### 1. 🤖 완전 자동 게임 생성
```
"판타지 RPG 만들어줘" → AI가 자동으로 스토리, 맵, 캐릭터, 이벤트 생성!
```

### 2. 🎨 AI 기반 개발 워크플로우
```
시나리오 생성 → 에셋 생성 → 구현 → 완성
모두 AI가 지원
```

### 3. 📚 게임 프로토타입 대량 생성
```
여러 스토리 컨셉을 시도하여 최적의 것을 선택
```

### 4. 🔄 프로그래밍 방식 게임 개발
```
Python 스크립트나 워크플로우 도구에서 게임 생성
```

### 5. 🧪 테스트 데이터 자동 생성
```
게임 엔진 테스트용 프로젝트를 즉시 생성
```

### 6. 🎓 교육·학습
```
RPG Maker MZ 학습용 샘플 자동 생성
```

## 📊 개발 상황

| 기능 | 상태 |
|------|------|
| ✅ 프로젝트 생성·관리 | 완료 |
| ✅ 맵 생성·편집 | 완료 |
| ✅ 이벤트 생성·편집 | 완료 |
| ✅ 데이터베이스 편집 | 완료 |
| ✅ AI 이미지 생성 (Gemini 2.5 Flash) | 완료 |
| ✅ AI 시나리오 자동 생성 | **NEW!** |
| ✅ 컨텍스트 엔지니어링 | 완료 |
| ✅ 완전한 게임 생성 워크플로우 | 완료 |

## 🌟 특별 기능

### 🚀 한 줄 명령어 RPG 생성
```bash
# 단 하나의 명령어로 완전한 RPG 게임 생성
generate_and_implement_scenario({
  theme: "your game idea",
  style: "your preferred style",
  length: "short"
})
# → 몇 분 안에 플레이 가능한 RPG 완성!
```

### 🎨 완전 AI 기반 개발
- **시나리오**: Gemini AI가 자동 생성
- **에셋**: Gemini 2.5 Flash가 이미지 생성
- **구현**: MCP 도구가 자동 구현
- **결과**: 완전히 작동하는 RPG Maker MZ 프로젝트

## 🤝 기여

Pull Request를 환영합니다!

## 📄 라이선스

MIT License

## 🔗 링크

- [RPG Maker MZ 공식](https://rpgmakerofficial.com/product/mz/)
- [Model Context Protocol](https://modelcontextprotocol.io/)
- [Gemini API](https://ai.google.dev/)

---

<div align="center">

**🎮 MCP 도구만으로 RPG Maker MZ 게임을 완전히 제작 가능! 🎮**

Made with ❤️ by [ShunsukeHayashi](https://github.com/ShunsukeHayashi)

</div>
