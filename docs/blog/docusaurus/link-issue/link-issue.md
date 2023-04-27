---
date: 2023-04-27
modified: 2023-04-27
---

## 마크다운 경로에서 .md 가 안사라져서 URL 오류가 나던 문제

`[WARNING] Blog markdown link couldn't be resolved:~~~` 이라는 오류가 뜨는 것이 .md 가 안되었다라는 것을 의미하는데
이 프로세스가 해당하는 프로세스 뿐 만 아니라 정상적으로 작성한 다른 프로세스에도 영향을 미치는 것으로 추정된다

> 이 문제의 증상은 링크에 .md 가 붙어서 경로가 깨진다

경로가 유실되면 오류가 발생한다
md 파일 내에 외부 링크도 좀 있는데 .... 어떻게 될지 체크를 해봐야할 것 같다

## 폴더 링크와 내부 폴더간 링크 문제

파일 구조적으로는 A 안에 A B C 가 있으면 A B C 는 같은 깊이를 가지지만
도큐사우르스에서는 A 는 A 와 같은 깊이를 가지고 B C 가 A 옆에 있기 때문에 B C 도 같은 높이를 가진다
[T2023-03-30 | 개발 정보 모음](https://mineclover.github.io/docs/topic/tech-review/T2023-03-30) 이쪽 글을 보면 같은 경로 내에 있는 파일을 가르키고 있는 링크가 깨진 것을 볼 수 있다

이는 같은 이름의 폴더나 index.md 로 된 폴더는 그 폴더의 메인 컨텐츠로 간주하는 것 같다
그래서 해결 방법은 두가지다
- 하나는 링크를 하지 않는 것
- 다른 하나는 다른 글들도 폴더로 감싸는 것이다
- 