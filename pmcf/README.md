# PMCFの地理

私jekto.vatimelijuがPMCFの地理についてなにも分かっていなかったのでまとめる。

## 基本的情報

> ちなみに割とどうでもいいんですが、現PMCFに当たる諸島は王朝時代は贅品庁であったというのは有名なことだと思いますが、ADLP以降はリナエスト人が多く移住して、リナエスト島（現・マナナ島）と呼ばれていました。
リパラオネ共和国とラネーメ共和国の国土係争地でしたが、後者が共和国革命でアルダーリーパに加わるとこの問題は有耶無耶にされてしまいます。PMCFは（ラネーメ人も含め）全然「父祖伝来」の土地ではないということは注意すべきかなと思われます。 ― Fafs F. Sashimi

jekto.vatimeliju『ということが知られているけど、バート人がamáma bohúの結果pedeに集中したのってなぜなんだろう（元から少数のバート人がいて縁故を頼りにそこに大量にバート人が押し寄せたりしたのか？）』  
falira.lyjotafis『なんだろうなあ』

* マナナ島は「アイル共和国に属する島でPMCFの経済の中心」

jekto.vatimeliju『リナエスト・オルス共和国ってどこにあるんですか（素朴な疑問）』  
skarsna haltxeafis nirxavija『[ここ](https://sites.google.com/site/riparaincangku/yuesureone-ren-gong-shi-jie-she-ding/li-shi/philerl/rinaesuto-orusu-gong-he-guo)には"リナエスト本島"とあって、その理解をしていた』  
falira.lyjotafis『内戦期に紙幣から消える島です』   
jekto.vatimeliju『そうよな、えーとそれはつまり』

![紙幣](https://github.com/jurliyuuri/stydyl/blob/master/pmcf/1sur.png)

jekto.vatimeliju『んでアイルがこれ』

![アイル共和国](https://github.com/jurliyuuri/stydyl/blob/master/pmcf/text4182.png)

falira.lyjotafis『めちゃくちゃややこしいんですが旧リナエスト島とリナエスト本島は違う概念です』  
skarsna haltxeafis nirxavija『うわあ…完全に勘違いしてた。こう考えるとLO本当に小さいなあ…』  
falira.lyjotafis『いにしへの白地図を発掘。下の四島とpede島横の一島を含む領域がリナエスト・オルスかな』

（ここに画像が入る）

jekto.vatimeliju『ふむふむ』

![色分け](https://github.com/jurliyuuri/stydyl/blob/master/pmcf/pmcfmap_-_.png)

jekto.vatimeliju『とりあえず面積比だけ出しときますかね。文字なし版ないですか（作業がつらい）』  
skarsna.meloviliju『この面積って本当にこの色が塗られているところだけですか？かつての支配地域とか合わせた公称値だったりしない？』  
falira.lyjotafis『大陸に領有を主張していたり描画されてない小さい島がやたら多いとかはあり得る』 
Fafs F. Sashimi『少なくともヴェフィスはリパラオネ共和国の正統後継者を名乗っているけど大陸の領土主張は面積の数値に計上されていない。』

falira.lyjotafis『svgがあるので文字消すか』

![文字なし枠あり](https://github.com/jurliyuuri/stydyl/blob/master/pmcf/text4186.png)

falira.lyjotafis『ごく狭い範囲なので緯度差は無視できるかな』  
jekto.vatimeliju『枠線の太さがわりとでかい誤差になるので、あんま気にしなくてよさそう』
falira.lyjotafis『たしかに』

とりあえず[ググって出てきたもの](https://www.imagemagick.org/discourse-server/viewtopic.php?t=16177)を頼りにピクセル数を数える。

jekto.vatimeliju『はい』

```
149710: (128,0,0,255) #800000FF maroon
65693: (0,0,128,255) #000080FF navy
31034: (255,255,0,255) #FFFF00FF yellow
```

jekto.vatimeliju『枠線全部塗りつぶした画像も貰えます？誤差範囲の把握は重要なので』

![文字なし枠なし](https://github.com/jurliyuuri/stydyl/blob/master/pmcf/text4186_2.png)

```
154952: (128,0,0,255) #800000FF maroon
69504: (0,0,128,255) #000080FF navy
34226: (255,255,0,255) #FFFF00FF yellow
```

falira.lyjotafis『雑に見積もって5:2:1くらいか』  
jekto.vatimeliju『9:4:2が誤差の範囲内に収まるっぽい。16906ピクセルを1とすると9:4:2が誤差の範囲内』

## 島の面積測るよ

16906ピクセルを「半LO」として島を測ると捗りそう。

jekto.vatimeliju『とりあえずシーレーオー（xi -r- LO）単位で各島の面積を求めとくか』

共和国ずつで処理するか。ということで分割する。

### アイル共和国

![アイル枠あり](bordered_air.png)
![アイル枠なし](nonbordered_air.png)

えーmanmanaを赤、pedeを黄、aikitを緑、atalamを紫に塗った状態にした。

borderedはこのようである。

```
      1664: (128,0,255,255) #8000FFFF srgba(128,0,255,1)
      1432: (128,255,0,255) #80FF00FF srgba(128,255,0,1)
    145806: (255,0,0,255) #FF0000FF red
       808: (255,255,0,255) #FFFF00FF yellow
```

1664+1432+145806+808 は 149710 であるので問題ない。

nonborderedはこのようである。

```
        32: (128,0,0,255) #800000FF maroon
      1996: (128,0,255,255) #8000FFFF srgba(128,0,255,1)
      1830: (128,255,0,255) #80FF00FF srgba(128,255,0,1)
    149943: (255,0,0,255) #FF0000FF red
      1151: (255,255,0,255) #FFFF00FF yellow
```

32+1996+1830+149943+1151 は 154952 であるので問題ない。32ピクセルほど塗り残したmaroonがあるということになるが、微小なので当然無視してよい。

ということで、

| 島名 | ピクセル数 | xirleror
|------|-----------|----------| 
| manmana | 145806 ~ 149943 | 8.624 ~ 8.870
| pede | 808 ~ 1151 | 0.048 ~ 0.068
| atalam | 1664 ~ 1996 | 0.098 ~ 0.118
| aikit | 1432 ~ 1830 | 0.085 ~ 0.108 
| (三島合計) | 3904 ~ 4977 | 0.231 ~ 0.294

やっぱりマナナ島でかいんだよな。

### ヴェフィス共和国

![ヴェフィス枠あり](bordered_vefisait.png)
![ヴェフィス枠なし](nonbordered_vefisait.png)

えーと青がkawakija / [kaka](https://sites.google.com/site/riparaincangku/yuesureone-ren-gong-shi-jie-she-ding/li-shi/philerl/cv)、tealがpokjut、cyanが多分[タムシエルミワ](https://sites.google.com/site/riparaincangku/yuesureone-ren-gong-shi-jie-she-ding/li-shi/philerl/cv#TOC--20)で緑が「「「小島」」」。

borderedはこのようである。

```
     50768: (0,0,255,255) #0000FFFF blue
     12303: (0,128,128,255) #008080FF teal
       640: (0,255,0,255) #00FF00FF lime
      1982: (0,255,255,255) #00FFFFFF cyan
```

50768+12303+640+1982 は 65693 であるので問題ない。

nonborderedはこのようである。

```
        18: (0,0,128,255) #000080FF navy
     52857: (0,0,255,255) #0000FFFF blue
     13272: (0,128,128,255) #008080FF teal
       895: (0,255,0,255) #00FF00FF lime
      2462: (0,255,255,255) #00FFFFFF cyan
```

18+52857+13272+895+2462 は 69504 であるので問題ない。

ということで、

| 島名 | ピクセル数 | xirleror
|------|-----------|----------| 
| kawakija / kaka | 50768 ~ 52857 | 3.003 ~ 3.127
| pokjut | 12303 ~ 13272 | 0.728 ~ 0.785
| タムシエルミワ | 1982 ~ 2462 | 0.117 ~ 0.146
| 「「「小島」」」 | 640 ~ 895 | 0.038 ~ 0.053

### リナエスト・オルス連合共和国

![リナエスト・オルス枠あり](bordered_linaest.png)
![リナエスト・オルス枠なし](nonbordered_linaest.png)

オレンジ(255, 128, 0)がkamut、残りの島が上から

* 仮称α; 赤(255, 0, 0)
* 仮称β; マゼンタ(255, 0, 255)
* 仮称γ; サーモンピンク(255, 128, 128)
* 仮称δ; オリーブ(128, 128, 0)
* 仮称ε; こげ茶(128, 0, 0)

である。名前考えてもらわんと。

borderedはこのようである。

```
       592: (128,0,0,255) #800000FF maroon
       718: (128,128,0,255) #808000FF olive
       364: (255,0,0,255) #FF0000FF red
       872: (255,0,255,255) #FF00FFFF magenta
     28073: (255,128,0,255) #FF8000FF srgba(255,128,0,1)
       421: (255,128,128,255) #FF8080FF srgba(255,128,128,1)
```

592+718+364+872+28073+421 は 31040 でなんか6ピクセル増えてるけどまあいいや。そういうこともある。誤差誤差。

nonborderedはこのようである。

```
       903: (128,0,0,255) #800000FF maroon
       950: (128,128,0,255) #808000FF olive
       604: (255,0,0,255) #FF0000FF red
      1151: (255,0,255,255) #FF00FFFF magenta
     29971: (255,128,0,255) #FF8000FF srgba(255,128,0,1)
       647: (255,128,128,255) #FF8080FF srgba(255,128,128,1)
```

903+950+604+1151+29971+647 は 34226 なので問題ない。

ということで、

| 島名 | ピクセル数 | xirleror
|------|-----------|----------| 
| kamut | 28073 ~ 29971 | 1.660 ~ 1.773
| 仮称α | 364 ~ 604 | 0.022 ~ 0.036
| 仮称β | 872 ~ 1151 | 0.052 ~ 0.068
| 仮称γ | 421 ~ 647 | 0.025 ~ 0.038
| 仮称δ | 718 ~ 950 | 0.042 ~ 0.056
| 仮称ε | 592 ~ 903 | 0.035 ~ 0.053
| (五島合計) | 2967 ~ 4255 | 0.175 ~ 0.252

という感じか。

## シーレーオー

シーレーオー、16906ピクセルということは130×130として書けるな。書いてみよう。

![シーレーオーつき地図](text4186_2_with_xirleror.png)

ということは、極度に抽象化した地図を描くことができ、

![抽象化](abstraction.png)

せっかくならドット絵も生やしてみると

![ドット絵](text4186_2_dot.png)

## 名前の対訳

[対訳](https://docs.google.com/spreadsheets/d/1A6B08DpPzdD-USgXPahUbUq1omaJzYB5UknWE_rlE0Q/edit#gid=0) を一気に立てた。それなりに立った。

![対訳](pmcf_islands_2020_04_20.png)

ということでリナエスト語地図はこんな感じ。

![リナエスト語地図](text4186_linaest.png)

skarsna haltxeafis nirxavija『おおおーありがとうございます！すごくいい感じ！！！そして読めん！！！（自爆）』

パイグ語準拠燐字地図を立てようと思ったら「民」の字形がまだ定まっていなかったので、とりあえずアイル共和国だけ。

![アイル共和国地図with燐字](air_with_lin_marn.png)
