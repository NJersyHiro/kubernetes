# **4.2.2**: Kaniko

* `kaniko-gcr.yaml`: Google Container Registry (GCR)を使う場合のKanikoのJobマニフェストの例 (リスト267) です。
  テキストを参考に、Secretリソース `kaniko-secret-ssh` および `kaniko-secret-gcp` を別途作成する必要があります。
  Gitリポジトリのパス `git.example.com:example/foo.git` や GCRイメージのパスi `asia.gcr.io/example/foo` は適当に置き換えてください。

* `kaniko-ecr.yaml`: Amazon Elastic Container Registry (ECR)を使う場合のKanikoのJobマニフェストの例 (リスト269) です。
  テキストを参考に、Secretリソース `kaniko-secret-docker` および `kaniko-secret-aws` を別途作成する必要があります。
  Gitリポジトリのパス `git.example.com:example/foo.git` や ECRイメージのパス `example.dkr.ecr.ap-northeast-1.amazonaws.com/foo` は適当に置き換えてください。

