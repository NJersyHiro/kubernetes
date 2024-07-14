# kubernetes

## postgres接続
k exec -it svc/postgres -- bash
psql -U user -d mydatabase

## langflow接続
k port-forward svc/langflow 7860 7860

## load image on kind
kind load docker-image langflow/langflow

## vector接続
k exec -it svc/vector -- bash

## TODO
p133 install vs code speech
launch.json（起動構成）を確認

## good to know
Ctrl + Pで最近開いたファイルを選択できる
F12で定義された箇所へ移動できる
Ctrl + Shift + O or Ctrl + P → @ シンボルへ移動
Ctrl + T 名前でシンボルを開く
タスク機能


## 使うか分からんけど一応メモ
Ctrl + Shift + \ （対応するカッコに移動

## need to know
kubebuilderのコードはどこで実行されるのか、ビルドしてどうなるのか
