# supporting-tool-for-making-drum-chart
ドラム譜面作成支援ツール


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
