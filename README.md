# life_game

Surface Evolverを用いて球面上でのライフゲームをつくりました。

## life_game_board

Surface Evolverに元々あるcube.feでgogoを一回実行しただけ。
形状を変えても面白いかもしれない(変わるのは見た目だけだけど………)

## life_game_command

白いファセットを草食動物、黒を肉食動物、緑を草としている。
周りに草が多いと肉食動物は死に、草食動物は繁殖する。
周りに肉食動物が多いと草食動物は死に、草は繁殖する。
周りに草食動物が多いと草は死に、肉食動物は繁殖する。

肉食動物が過密の場合は草が生える。
草食動物が過密の場合は肉食動物が繁栄する。
草が過密の場合は草食動物が繁栄する。

そのほかはそのまま。

上のようにファセットの色を変えていき、その変化を観察する。

startプロシージャはファセットの色を白黒緑の三色にランダムに分ける。
print_mapプロシージャはhistmapというテキストファイルに色ごとのファセットの数を書き込む。
playは全ファセットに関して一回計算する。

##初期値依存性

最初にファセットの色をランダムに振り分けてから1000ステップ計算(playを10回実行)した。

![ランダムな状態からスタート](https://imgur.com/a/yGUSYQ1)

全て緑にしてから同様に計算した。

![全て緑の状態からスタート](https://imgur.com/Mv1jkpZ)
