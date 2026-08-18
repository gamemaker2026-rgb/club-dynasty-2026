# 클럽 다이너스티 2026 GitHub Pages 배포 안내

이 안내서는 GitHub 계정으로 **클럽 다이너스티 2026**을 링크 클릭 즉시 플레이 가능한 웹게임으로 공개하는 방법을 설명합니다. 이 패키지는 빌드 과정이 필요 없는 순수 정적 파일이므로 GitHub Pages의 `main` 브랜치 최상위 폴더에서 바로 제공할 수 있습니다.

## 시작 전 확인

| 항목 | 현재 패키지 상태 | 업로드 시 주의점 |
|---|---:|---|
| `index.html` | 포함 | 반드시 저장소 최상위에 배치 |
| `assets/` 폴더 | 45개 이미지·영상 포함 | 폴더 이름과 내부 파일 구조를 변경하지 않음 |
| 전체 용량 | 약 191 MiB | ZIP 자체를 올리지 않고 압축을 푼 폴더 **내용**을 업로드 |
| 개별 최대 자산 | 약 5.93 MiB | 일반 GitHub 파일 크기 제한보다 작음 |
| `.nojekyll` | 포함 | Pages가 게임 파일을 그대로 제공하도록 유지 |

## 1. GitHub 저장소 만들기

1. [GitHub](https://github.com)에 로그인합니다.
2. 우측 상단의 **+** 메뉴에서 **New repository**를 선택합니다.
3. Repository name에는 `club-dynasty-2026`을 입력합니다.
4. Visibility는 **Public**을 선택합니다. GitHub Free 계정에서 Pages를 사용하는 경우 공개 저장소가 필요합니다.[1]
5. **Add a README file**을 켠 뒤 **Create repository**를 누릅니다.

저장소 주소는 아래처럼 만들어집니다.

```text
https://github.com/<GitHub사용자이름>/club-dynasty-2026
```

## 2. 게임 파일 전체 올리기

1. 이 패키지 ZIP을 컴퓨터에서 압축 해제합니다.
2. 방금 만든 GitHub 저장소의 **Code** 탭에서 **Add file → Upload files**를 선택합니다.
3. 압축을 푼 폴더 안의 `index.html`, `.nojekyll`, `README.md`, `GITHUB_PAGES_DEPLOYMENT_GUIDE.md`, `assets` 폴더를 함께 끌어다 놓습니다.
4. 업로드가 끝나면 아래 구조가 저장소 최상위에 있는지 확인합니다.

```text
club-dynasty-2026/
├── index.html
├── .nojekyll
├── README.md
├── GITHUB_PAGES_DEPLOYMENT_GUIDE.md
└── assets/
    ├── club_campus_overview.jpg
    ├── acquisition_cinematic.mp4
    ├── assistant_f01.jpg
    └── ...
```

5. 아래의 **Commit changes**를 눌러 업로드를 확정합니다.

> `assets` 폴더가 `club-dynasty-2026/assets`가 아니라 `club-dynasty-2026/다른폴더/assets`처럼 한 단계 더 안쪽에 들어가면 이미지·영상이 표시되지 않습니다.

## 3. GitHub Pages 켜기

1. 저장소 상단의 **Settings**를 선택합니다.
2. 왼쪽 메뉴 **Code and automation → Pages**를 선택합니다.
3. **Build and deployment → Source**에서 **Deploy from a branch**를 선택합니다.
4. Branch는 **main**, Folder는 **/(root)**를 선택합니다.
5. **Save**를 누릅니다.

GitHub Pages는 `index.html`을 진입 파일로 찾아 정적 사이트를 배포합니다.[2] 처음 배포하거나 업데이트한 뒤 실제 반영까지 시간이 걸릴 수 있습니다.[2]

## 4. 플레이 링크 확인 및 공유

배포가 완료되면 Pages 화면에 링크가 표시됩니다. 이 저장소 이름을 사용했다면 기본 링크는 보통 아래 형식입니다.

```text
https://<GitHub사용자이름>.github.io/club-dynasty-2026/
```

이 링크를 갤럭시 Chrome, 아이폰 Safari, PC Chrome에서 열면 다운로드·압축 해제 없이 바로 시작 화면이 열립니다. 이미지·영상은 `assets` 폴더에서 HTTPS로 제공되므로 Android의 `file://` 실행 제한도 발생하지 않습니다.

## 5. 업데이트 방법

새 버전이 나오면 최신 `index.html`과 변경된 `assets` 파일을 같은 경로에 덮어써서 업로드하고 **Commit changes**를 누릅니다. Pages가 재배포되면 공유했던 링크는 그대로 유지하면서 최신 게임이 열립니다.

## 문제 해결

| 증상 | 먼저 확인할 내용 |
|---|---|
| 404 페이지 | Settings → Pages에서 `main`과 `/(root)`가 선택됐는지 확인 |
| 게임은 열리지만 이미지·영상이 없음 | 저장소 최상위에 `assets` 폴더가 있고 폴더명이 바뀌지 않았는지 확인 |
| 업데이트가 바로 보이지 않음 | Pages 배포 완료 여부를 확인하고 브라우저 새로고침 또는 잠시 후 재접속 |
| 저장 게임이 사라짐 | 다른 브라우저·기기에서는 저장이 공유되지 않음. 브라우저 데이터 삭제 여부 확인 |

## 참고 자료

[1] [GitHub Pages 사이트 생성 공식 문서](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)

[2] [GitHub Pages 게시 원본 설정 공식 문서](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
