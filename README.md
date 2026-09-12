# claude-humanize-skill

한국어 글을 사람이 읽기 자연스럽게 다듬는 [Claude Code](https://docs.claude.com/en/docs/claude-code) 스킬이다.

AI가 쓴 글에 흔한 em dash(—), 과도한 이모지, 한국어에서 어색한 문장부호를 걷어내고, 명사 서술어 종결과 문장 흐름을 다듬는다. 의미는 그대로 두고 어투만 손본다.

## 무엇을 하나

- em dash(—)를 마침표·쉼표·괄호·콜론으로 바꾼다.
- 장식용 이모지를 뺀다.
- 한국어에서 잘 안 쓰는 부호를 정리한다(가운뎃점·화살표는 자연스러우면 유지).
- 정의·격식 문장의 명사 서술어 종결을 다듬는다(`문서다` → `문서이다`).
- 긴 문장을 끊고, 기계 번역 같은 연결과 군더더기를 덜어낸다.

자세한 규칙은 [`humanize/SKILL.md`](./humanize/SKILL.md)에 있다.

## 설치

`humanize` 폴더를 스킬 디렉터리 아래로 복사한다.

```bash
git clone https://github.com/yuyeol3/claude-humanize-skill.git

# 특정 프로젝트에서만 쓰려면
cp -r claude-humanize-skill/humanize <프로젝트>/.claude/skills/

# 모든 프로젝트에서 쓰려면
cp -r claude-humanize-skill/humanize ~/.claude/skills/
```

## 사용

Claude Code에서 이렇게 요청하면 된다.

- "이 문서 humanize 해줘"
- "글 어투 자연스럽게 다듬어줘"
- "em dash랑 이모지 걷어내줘"
