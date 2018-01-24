# maya_unity　連携機能２
maya unity 連携機能２（アニメーション　簡易移動編）  

1. 前回から引き続き、今回はアニメーションを設定していきます。  
[前回ページはこちら](https://github.com/175B005/maya_unity)  
[FBXのアセット](http://u3d.as/XWD)をインポート  
1. 連携は起動ごとに更新されてしまうので、  
前回のページを参考にInstall Unity Integrationからmayaを起動(連携してある場合はやらなくてよい)  
1. 前回言い忘れていましたが、mayaでの作業はアウトライナ<UnityFbxExportSetの子要素として  
おいてあります。（この中に入れれば、後からmaya側で作成したオブジェクトでも、くっつけることが可能）
![](https://github.com/175B005/maya_unity2/blob/master/directionanim3.jpg?raw=true)
1. maya側で画面右「チャネルボックス」からキー値を設定していきます。  
今回はｘ座標のみを動かしていますが、パラメータはｘｙｚと回転など、  
いろいろありますので、自由に移動できます。
1. ｘを１にして(変更するオブジェクトを選択した上で)、設定している数値の上で右クリック。  
すぐ上に出てくる「選択項目のキー設定」を押す。すると、下部にあるアニメーションのバーがあるので、  
今いるフレームにキーを設定できました。  
このバーを最初に１に設定してから行います。６０など数値が右にもありますが、  
フレーム数で、調節すると、全体のアニメーションの長さを設定できます。（後で変更も可能ですが最初にめどをつけておきましょう。）
![](https://github.com/175B005/maya_unity2/blob/master/directionanim4.jpg?raw=true)
1. 上部メニューを「ポリゴン」から「アニメーション」に変更し、メニューを出しておくと、ショートカットができて、便利。  
中央部くらいの十字みたいなマークで、先ほどのキー値設定がワンクリックでできます。
1. 今回は１と３０と６０にキー値を設定し、それぞれ1　 -1　 1と設定しています。  
キーの値を設定するだけで、その間を等速で平行移動してくれます。 
1. 右下の再生ボタンを押すと動き出します。
※動きが早すぎる場合
右下の非常口マーク的なものがあるので、そこをクリックすると、設定画面が出てくるので、  
タイムスライダ< 再生< 再生スピードを設定すると、遅くなったり早くなったりします。  
動きが大きいほど早く動いてしまうので、注意です。
![](https://github.com/175B005/maya_unity2/blob/master/directionanim5.jpg?raw=true)
1. アニメーションが設定できたら、unityに戻ります。（maya側でExportしてください）
1. 変更したオブジェクトを選択するとInspectorにRigの項目があるので、none →Genericに変えます。
![](https://github.com/175B005/maya_unity2/blob/master/directionanim7.jpg?raw=true)
1. Appryします。
![](https://github.com/175B005/maya_unity2/blob/master/directionanim13.jpg?raw=true)
1. その後、Animationの項目にいき、ここで先ほど調整したアニメーションの設定がいろいろできます。  
今回はLoop Timeにチェックをいれて見ると、このアニメーションは呼び出された後、ループすることになります。  
下の再生ボタンでそのアニメを確認することができます。
![](https://github.com/175B005/maya_unity2/blob/master/directionanim9.jpg?raw=true)
1. アニメーション自体の設定が終わったので、今度は動かします。
1. create< animator Controllerでコントローラーを作ります。
![](https://raw.githubusercontent.com/175B005/maya_unity2/master/directionanim10.jpg)
1. 作ったコントローラをダブルクリックすると、Animetorのウィンドウが出てくるので、  
その中に、変更していたオブジェクトの中にあるアニメデータをドラッグ＆ドロップ  
Animetorの中にいれます。すると勝手にEntryとつながるので、これでコントローラの完成です。
![](https://github.com/175B005/maya_unity2/blob/master/directionanim11.jpg?raw=true)
1. 最後に変更していたオブジェクトを選択して、追加されている
1. AnimatorのControllerに今作ったコントローラを入れ、これで完了です。
![](https://github.com/175B005/maya_unity2/blob/master/directionanim12.jpg?raw=true)
1. 実行して確認してみてください。設定したように上下か左右に動き続けるようになったはずです。

