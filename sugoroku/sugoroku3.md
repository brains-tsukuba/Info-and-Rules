# すごろくを作るstep3
## 仕様


- プレイヤーはユーザーの入力（2以上、6未満）で決める 
 - それ以外の入力は受け付けず、入力し直させる。
- マスの数はユーザーの入力（20以上、40未満）で決める。 
 - それ以外の入力は受け付けず、入力し直させる。
- マスには、それぞれ(1~10)のポイントをランダムに割り当てる。 
 - ゲームをリセットするたびに、割当を変える。

 - 毎ターン、到達したマスに割り当てられたポイントを各プレイヤーのポイントとして加算していく。
 - 各プレイヤーは０ポイントを持っている状態で始まる。
-  ゴールしたら、（総プレイヤー数/ゴール順位）分足す。
-  サイコロは8面。
 - 出た目が偶数なら、目の数だけ進む。
 - 出た目が奇数なら、目の数だけ戻る。
 -  振り出しより手前に戻ることになったら、振り出しにそのプレーヤーは戻る。
- 戻った時のスコア追加はなし。だが持ってたスコアは継続。

- １ターンとは、以下のように定義する。 
 -  プレイヤー１がサイコロを振る。
 -  プレーヤー１のコマを出た目の数だけ進む/戻る。
 - プレーヤー２がサイコロを振る。
 - プレーヤー２のコマを出た目の数だけ進む/戻る。
 - 以下プレーヤーの数だけ繰り返す

- １ターンが終わったら、次のターンに入る。
- ゴールはぴったりでないといけない。 
 - 超えたら、振り出しに戻る。

- 全員がゴールしたら、ポイントを比較し、ポイントが一番高いプレーヤーを示す。
	* CUIでもGUIでも構わない。

## 注意点
- なお、今後色々な仕様変更が考えられる。
- 言語は問わない。
-  GitHubを使うことを激しく推奨する。
- Step2は、1の動作確認ができるまで見てはならない。
