# HackathonRunner

ハッカソンに対する不安を解消することで、ハッカソンに参加したい・参加する人たちを支援するためのWebアプリ。

<img src="https://user-images.githubusercontent.com/79685987/197310366-d45ea75e-e970-441c-88f5-f57601a65ef6.jpg">

**URL**: 公開準備中

## チームJavalerのHackathonRunner

このソフトウェアは、私が所属する[チームJavaler](https://github.com/Javaler/)において、2022年4月から2023年3月まで開発されていたアプリを、個人で継続開発しているものです。（もちろん、メンバーから許可は得ています。）

- [チームJavalerで開発したHackathonRunner](https://github.com/Javaler/HackathonRunner)
- [チームJavalerでの開発を振り返った記事](https://qiita.com/NMS/items/4d43e3acb02d29cc6cc4)

個人開発で改変を行ったファイルは以下の通りです。
```
HackathonRunner
 ├ git  # Remove
 ├ README.md  # Chnage
 ├ pom.xml  # Chnage
 ├ .gitignore  # Chnage
 ├ .github/workflows
 │  └ deploy-to-heroku.yml  # Remove
 ├ docs
 │  └ pull_request_template.md  # Add
 └ src/main
    ├ java/com/example/demo
    │   ├ controller
    │   │   ├ HomeController.java  # Chnage
    │   │   ├ PostController.java  # Remove
    │   │   ├ QuestionController.java  # Chnage
    │   │   └ RecruitmentController.java  # Remove
    │   ├ dao
    │   │   ├ PostDao.java  # Remove
    │   │   └ PostDaoImpl.java  # Remove
    │   ├ dto
    │   │   └ ResponseBody.java  # Remove
    │   ├ entity
    │   │   ├ Post.java  # Remove
    │   │   └ Recruitment.java  # Remove
    │   ├ form
    │   │   ├ PostForm.java  # Remove
    │   │   ├ PostQuery.java  # Remove
    │   │   └ RecruitmentForm.java  # Remove
    │   ├ repository
    │   │   ├ PostRepository.java  # Remove
    │   │   └ RecruitmentRepository.java  # Remove
    │   └ service
    │       └ PostService.java  # Remove
    └ resources
        ├ twitter4j.properties  # Remove
        ├ static
        │   ├ css
        │   │   └ postForm.css
        │   └ js
        │       └ postForm.js
        └ templates
            ├ fragments.html  # Chnage
            ├ home.html  # Chnage
            ├ postDetail.html  # Remove
            ├ postForm.html  # Remove
            ├ postList.html  # Remove
            ├ questionForm.html  # Chnage
            ├ questionResult.html  # Chnage
            ├ recruitmentForm.html  # Remove
            └ recruitmentList.html  # Remove
```

## 仕様/機能一覧

### 診断機能

- 選択式の質問約10個に回答すると、ハッカソンに対する技術レベルを診断し、「ハッカソンまでに何を準備しておけば良いか」や「ハッカソンでどう振る舞えば良いか」といった提案をする
- [HackathonRunner-Analysis-API](https://github.com/Javaler/HackathonRunner-Analysis-API) を叩いて、同じような技術レベルの人の投稿（どんなハッカソンに参加したかなど）を取得・表示する
- ハッカソンに対する技術レベルをチャートで表示する
- 使用時の画面(2022年10月時点)
<img src="https://user-images.githubusercontent.com/79685987/197223472-e6814061-015a-48e1-a347-02e690979ba6.mp4">

### 投稿機能

- 投稿の新規作成、一覧表示、詳細表示、検索
- 使用時の画面(2022年10月時点)
<img src="https://user-images.githubusercontent.com/79685987/197227396-ac8907ca-91b9-480f-9b52-e4ebb2113861.mp4">

### チームメンバー募集機能

- 開発仲間やハッカソンに一緒に参加できる人を集めるための投稿、表示
- 使用時の画面(2022年10月時点)
<img src="https://user-images.githubusercontent.com/79685987/197318073-827d3bae-7763-48c1-9e3f-ac4df6ddc05c.mp4">

## 使用技術(ツール)一覧

- **アプリケーション**
  - フロントエンド
    - **HTML/CSS**
    - **JavaScript**
    - **Bootstrap**
    - **Chart.js**
  - バックエンド
    - **Java**
    - **Maven**
    - **Spring Boot**
    - **[HackathonRunner-Analysis-API](https://github.com/Javaler/HackathonRunner-Analysis-API)**
- **バージョン/ソースコード管理**
  - **Git, GitHub**
- その他使用ツール
  - Visual Studio Code(フロントエンド, README等)
  - IntelliJ IDEA(バックエンド)
  - digrams.net(クラス図)
  - Figma(UIデザイン)
  - Notion(ドキュメント)
