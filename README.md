# 클럽 다이너스티 2026 — GitHub Pages 배포판

이 폴더는 **클럽 다이너스티 2026**을 GitHub Pages에 바로 게시하기 위한 정적 웹게임 패키지입니다.

## 반드시 유지할 구조

```text
club-dynasty-2026/
├── index.html
├── .nojekyll
├── README.md
└── assets/
    ├── club_campus_overview.jpg
    ├── acquisition_cinematic.mp4
    └── ...
```

`index.html`과 `assets` 폴더를 반드시 같은 저장소의 최상위에 유지해야 이미지·영상이 작동합니다. `index.html`만 업로드하거나 `assets` 폴더 이름을 바꾸면 게임 화면의 캠퍼스·인물·비서·영상 자산이 보이지 않습니다.

## GitHub Pages 게시 방법

1. GitHub에서 새 공개 저장소를 만들고 이름을 `club-dynasty-2026`으로 지정합니다.
2. 이 폴더의 **내용 전체**를 새 저장소의 최상위에 업로드합니다. 폴더 자체가 한 단계 더 들어가지 않도록 주의합니다.
3. 저장소의 **Settings → Pages**로 이동합니다.
4. **Build and deployment → Source**에서 **Deploy from a branch**를 선택합니다.
5. Branch는 `main`, Folder는 `/(root)`를 선택하고 **Save**를 누릅니다.
6. Pages 배포가 완료되면 `https://<GitHub사용자이름>.github.io/club-dynasty-2026/` 주소로 접속합니다.

GitHub Pages는 처음 게시 또는 업데이트 뒤 반영까지 시간이 걸릴 수 있습니다. 사이트가 열렸는데 이미지·영상이 보이지 않으면 저장소 최상위의 `assets` 폴더와 `index.html`이 함께 올라갔는지 먼저 확인합니다.

## 저장 데이터

게임 저장 데이터는 각 사용자의 브라우저 `localStorage`에 보관됩니다. 같은 기기·같은 브라우저에서는 이어하기가 가능하지만, 브라우저 데이터를 삭제하거나 다른 기기로 바꾸면 저장 내용이 자동으로 옮겨지지 않습니다.

## 업데이트 방법

새 다운로드 버전이 나오면 최신 `index.html`과 변경된 `assets` 파일을 같은 경로에 덮어쓴 뒤 GitHub에 커밋·업로드합니다. GitHub Pages가 다시 배포하면 기존 링크에서 새 버전이 열립니다.
