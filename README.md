# supporting-tool-for-making-drum-chart
ドラム譜面作成支援ツール


NMNDベースの手法は実装が整ってなく現実的な計算時間で終わる気がしない＋解釈が難しい

ニューラルネットの学習済みモデルベースのモデルは公開されてるのが少ない＋スネアバスドラハイハットしか対応してないなど難点も多い。しかもハイハットの誤打が多い傾向にありそう。

自分で実装すればいいんだろうけど、他のことに時間を割きたい。よって本プロジェクトは凍結する。

# 開発環境
環境作成
```sh
cd docker
docker build -t masakiaota/drum_chart .
```

起動
```sh
docker run  --shm-size=2048m -v $PWD:/tmp/working -w=/tmp/working -p 8888:8888 --rm -it masakiaota/drum_chart  jupyter lab --no-browser --ip="0.0.0.0" --notebook-dir=/tmp/working --allow-root
```
