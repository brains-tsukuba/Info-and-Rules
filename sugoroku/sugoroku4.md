
# すごろくを作るstep4
## 仕様
- プレイヤ数ーはユーザーの入力（2以上、4以下）で決める 
 - それ以外の入力は受け付けず、入力し直させる。

- マスの数はユーザーの入力（20以上、30以下）で決める。 
 - それ以外の入力は受け付けず、入力し直させる。
- ゴールは最後のマスとし、スタートは最初のマスとはしない。		 
 - つまり、20マスを指定したなら、、、		* 
  - [スタート, マス1, マス2, マス3, ... , マス20]
  - これのマス20がゴールとなる。

- サイコロは8面。
 - 出た目が偶数なら、目の数だけ進む。
 - 出た目が奇数なら、目の数だけ戻る。 
    - スタート地点より手前に戻ることになったら、そのプレーヤーはスタート地点に戻る。

- マスには、それぞれ(1~10)のポイントをランダムに割り当てる。  
 - ゲームをリセットするたびに、割当を変える。
 - 毎ターン、到達したマス割り当てられたポイントを各プレイヤーのポイントとして加算していく。
 - スタート地点と、ゴール地点（最後のマス）にポイントは割り当てられてないため、そこに到達してもポイント加算はない。

- 各プレイヤーは０ポイントを持っている状態で始まる。
- ゴールはぴったりでないといけない。  
 - 超えたら、超えた分戻る。
 - 超えて戻った時に着地したマスの加点はする。
 - 超えたら、そのプレイヤーのスコアは5点減点。
- 誰かゴールしたら、
 - その時点でターン終了。もうサイコロは誰も振らない。
 - 誰かゴール時、各プレイヤーのスコアに（総プレイヤー数 X 3 / その時点での各プレイヤー順位）”ボーナススコア”として加点する。
		- ゴール時点での順位は、よりゴールに近い順に1,2,3...位となる。
 - 最終的ポイントを比較し、ポイントが一番高いプレーヤーを示し、勝者とする。

- １ターンとは、以下のように定義する。 
 - プレイヤー１がサイコロを振る。
 - プレーヤー１のコマを出た目の数だけ進む/戻る。
 - ポイントを加算する
 - プレーヤー２がサイコロを振る。
 - プレーヤー２のコマを出た目の数だけ進む/戻る。
 - ポイントを加算する
 - 以下プレーヤーの数だけ繰り返す

- １ターンが終わったら、次のターンに入る。
- CUIでもGUIでも構わない。

## 注意点
- なお、今後色々な仕様変更が考えられる。
- 言語は問わない。
- GitHubを使うことを激しく推奨する。
- 次のStepは、動作確認ができるまで見てはならない。

