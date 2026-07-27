# youngbin03.github.io 배포

## 1. GitHub에서 저장소 만들기
1. https://github.com/new
2. **Repository name**: `youngbin03.github.io` (계정 아이디와 정확히 일치해야 함)
3. **Public** 선택, README·.gitignore·license는 **체크하지 않음**
4. Create repository

## 2. 터미널에서 업로드
이 폴더(`_site`)에서 그대로 실행하세요.

```bash
cd ~/Downloads/portfolio/_site

git init -b main
git add .
git commit -m "portfolio site"
git remote add origin https://github.com/youngbin03/youngbin03.github.io.git
git push -u origin main
```

푸시할 때 비밀번호를 물으면 GitHub 계정 비밀번호가 아니라
**Personal Access Token**(github.com → Settings → Developer settings →
Personal access tokens → Tokens (classic) → repo 권한)을 붙여넣으면 됩니다.

## 3. Pages 켜기
보통 `<아이디>.github.io` 저장소는 자동으로 켜집니다.
안 되면 저장소 → **Settings → Pages → Source: Deploy from a branch → main / (root)** → Save.

1~2분 뒤 **https://youngbin03.github.io** 에서 확인.

## 4. 이후 수정 반영
원본 폴더(`~/Downloads/portfolio`)에서 내용을 고친 뒤,
바뀐 html과 reference 파일을 `_site`로 복사하고:

```bash
cd ~/Downloads/portfolio/_site
git add .
git commit -m "update"
git push
```

## 담긴 것
- html 7개 (index + 상세 6)
- reference/ 실제로 쓰이는 자산 11개 (약 11MB)
- `.nojekyll` — GitHub Pages의 Jekyll 처리를 끔 (언더스코어 파일·폴더 보호)

원고(md)·rtf·`_build.py`·archive·미사용 이미지는 포함하지 않았습니다.
