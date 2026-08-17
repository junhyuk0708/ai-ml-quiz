# AI & 머신러닝 기초 모바일 4지선다

휴대폰에서 한 문제씩 넘기며 복습할 수 있는 125문제 퀴즈입니다.

## GitHub Pages 배포

### 웹에서 업로드하는 가장 쉬운 방법

1. GitHub에서 새 저장소를 만들고 이름을 `ai-ml-quiz`로 지정합니다.
2. 저장소 공개 범위는 `Public`으로 선택합니다.
3. 이 폴더의 파일을 모두 저장소 최상위에 업로드합니다.
4. 저장소의 `Settings` → `Pages`로 이동합니다.
5. `Build and deployment`의 `Source`를 `Deploy from a branch`로 설정합니다.
6. Branch는 `main`, 폴더는 `/(root)`를 선택하고 `Save`를 누릅니다.
7. 잠시 뒤 `https://<GitHub아이디>.github.io/ai-ml-quiz/`로 접속합니다.

### Git 명령어로 올리는 방법

```bash
git init
git add .
git commit -m "Deploy AI ML quiz"
git branch -M main
git remote add origin https://github.com/<GitHub아이디>/ai-ml-quiz.git
git push -u origin main
```

그다음 GitHub 저장소의 `Settings` → `Pages`에서 `main` / `/(root)`를 선택합니다.

## 휴대폰 홈 화면에 추가

- Android Chrome: 우측 상단 `⋮` → `홈 화면에 추가` 또는 `앱 설치`
- iPhone Safari: 공유 버튼 → `홈 화면에 추가`

첫 접속 후에는 앱 셸이 캐시에 저장되어 네트워크가 불안정한 상황에서도 다시 열 수 있습니다. 퀴즈 진도와 오답 기록은 해당 브라우저의 로컬 저장소에 저장됩니다.

## 파일 구성

- `index.html`: 퀴즈 본체
- `manifest.webmanifest`: 홈 화면 앱 정보
- `sw.js`: 오프라인 캐시
- `icon-192.png`, `icon-512.png`: 홈 화면 아이콘
- `.nojekyll`: 정적 파일을 그대로 배포하기 위한 설정
