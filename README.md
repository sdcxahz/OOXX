FIR
===

GoBang / Gomoku / Renju / Five in a Row / FIR / 五子棋 Game with Reinforcement Learning 强化学习

C++实现带有自学习能力的五子棋对弈软件




操作键有
<br\>上下左右控制落子光标
<br\>X x O o 可分别强制落黑棋白棋
<br\>回车和空格可以按下棋落子
<br\>退格 < ,可以悔棋
<br\>\> .可以重落子



五子棋禁手规则简介

<br\>术语 定义     判定优先级由上至下
<br\>长连 连子多于五
<br\>成五 五连(黑棋) 五连或长连(白棋)
<br\>活四 有两点可成五同时连子为四
<br\>眠四 有一点可成五
<br\>活三 至少有一点可成活四
<br\>眠三 至少有一点可成眠四
<br\>活二 至少有一点可成活三
<br\>眠二 至少有一点可成眠三
<br\>活一 至少有一点可成活二
<br\>眠一 至少有一点可成眠二


黑棋有禁手 
<br\>  长连 
<br\>	四四(一点同时生成大于等于两个四(活四或眠四)) 
<br\>	三三(一点同时生成大于等于两个活三) 

注意事项:
<br\>1.成五优先于禁手， 即同时成五和禁手，算黑棋赢
<br\>2.平行的四四三种情况
<br\>	X . X(X)X . X
<br\>	X X . X(X). X X
<br\>	X X X .(X). X X X
<br\>3.假三三/多重禁手 

如括号中就是假三三点 因为最下一排的“三”的活四点是禁手点
<br\>. . . X . . . . 
<br\>. . . X . . . X
<br\>. . . X . . X . 
<br\>. . X . X(.). . 

更经典的情况  括号点不是禁手(四重禁手判断)
<br\>. . X X . . 
<br\>. X(.). X .
<br\>. X . . X .
<br\>. . X X . .


