---
title: リリースについて
intro: 他の人が使用できるようにソフトウェア、リリースノート、バイナリファイルへのリンクをパッケージしたリリースを作成できます。
redirect_from:
  - /articles/downloading-files-from-the-command-line
  - /articles/downloading-files-with-curl
  - /articles/about-releases
  - /articles/getting-the-download-count-for-your-releases
  - /github/administering-a-repository/getting-the-download-count-for-your-releases
  - /github/administering-a-repository/about-releases
  - /github/administering-a-repository/releasing-projects-on-github/about-releases
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Repositories
---

## リリースについて

{% ifversion fpt or ghec or ghes > 3.3 or ghae-issue-4974 %}
![リリースの概要](/assets/images/help/releases/refreshed-releases-overview-with-contributors.png)
{% elsif ghae-issue-4972 %}
![リリースの概要](/assets/images/help/releases/releases-overview-with-contributors.png)
{% else %}
![リリースの概要](/assets/images/help/releases/releases-overview.png)
{% endif %}

リリースは、パッケージ化して、より多くのユーザがダウンロードして使用できるようにすることができるデプロイ可能なソフトウェアのイテレーションです。

リリースは [Git タグ](https://git-scm.com/book/en/Git-Basics-Tagging)に基づきます。タグは、リポジトリの履歴の特定の地点をマークするものです。 タグの日付は異なる時点で作成できるため、リリースの日付とは異なる場合があります。 既存のタグの表示に関する詳細は「[リポジトリのリリースとタグを表示する](/github/administering-a-repository/viewing-your-repositorys-releases-and-tags)」を参照してください。

リポジトリで新しいリリースが公開されたときに通知を受け取り、リポジトリで他の更新があったときには通知を受け取らないでいることができます。 For more information, see "[Viewing your subscriptions](/github/managing-subscriptions-and-notifications-on-github/viewing-your-subscriptions)."

リポジトリへの読み取りアクセス権を持つ人はリリースを表示および比較できますが、リリースの管理はリポジトリへの書き込み権限を持つ人のみができます。 詳細は「[リポジトリのリリースを管理する](/github/administering-a-repository/managing-releases-in-a-repository)」を参照してください。

{% ifversion fpt or ghec or ghes > 3.3 or ghae-issue-4974 %}
You can manually create release notes while managing a release. Alternatively, you can automatically generate release notes from a default template, or customize your own release notes template. For more information, see "[Automatically generated release notes](/repositories/releasing-projects-on-github/automatically-generated-release-notes)."
{% endif %}

{% ifversion fpt or ghec %}
リポジトリへの管理者権限を持つユーザは、{% data variables.large_files.product_name_long %}（{% data variables.large_files.product_name_short %}）オブジェクトを、{% data variables.product.product_name %} がリリースごとに作成する ZIP ファイルと tarball に含めるかどうかを選択できます。 詳しい情報については、「[リポジトリのアーカイブ内の {% data variables.large_files.product_name_short %} オブジェクトを管理する](/repositories/managing-your-repositorys-settings-and-features/managing-repository-settings/managing-git-lfs-objects-in-archives-of-your-repository)」を参照してください。

リリースでセキュリティの脆弱性が修正された場合は、リポジトリにセキュリティアドバイザリを公開する必要があります。 {% data variables.product.prodname_dotcom %} は公開された各セキュリティアドバイザリを確認し、それを使用して、影響を受けるリポジトリに {% data variables.product.prodname_dependabot_alerts %} を送信できます。 詳しい情報については、「[GitHub セキュリティアドバイザリについて](/github/managing-security-vulnerabilities/about-github-security-advisories)」 を参照してください。

リポジトリ内のコードに依存しているリポジトリとパッケージを確認するために、依存関係グラフの [**依存関係**] タブを表示することができますが、それによって、新しいリリースの影響を受ける可能性があります。 詳しい情報については、「[依存関係グラフについて](/github/visualizing-repository-data-with-graphs/about-the-dependency-graph)」を参照してください。
{% endif %}

リリースAPIを使用して、リリースアセットがダウンロードされた回数などの情報を収集することもできます。 詳しい情報については、「[リリース](/rest/reference/releases)」を参照してください。

{% ifversion fpt or ghec %}
## ストレージと帯域幅の容量

 リリースに含まれる各ファイルは、{% data variables.large_files.max_file_size %}以下でなければなりません。 リリースの合計サイズにも帯域幅の使用量にも制限はありません。

{% endif %}
