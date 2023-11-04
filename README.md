# 高松市スマートマップのテスト

高松市が公開している[高松市スマートマップ](https://github.com/takamatsu-city/maps.takamatsu-fact.com)をコピーしてテスト用にカスタマイズします。  
坂出の情報を表示できるようにしたいと思います。  
坂出市が[オープンデータ](https://www.city.sakaide.lg.jp/soshiki/kouminrenkei/opendata.html)とし公開しているデータの一部を地図上に表示させるが目標です。  

テスト用のサイトは以下のURLで動作しています。  
https://komasn.github.io/test_smartmap/build/

## 課題管理
- https://github.com/takamatsu-city/maps.takamatsu-fact.com をローカル環境で動作させる(完了：20231103)
- 上記をGitHub Pages で動作させる(完了：20231103)
- ページのタイトルを"坂出市スマートマップテスト"に変更する(完了：20231103)
- 坂出市境界のグレーアウト表示を解除する(完了：20231104)  
  srcの中のMainMap.tsx を修正することで色の変更ができた  
  （negative-city-mask-layerおよびnegative-city-mask-layer-borderのCOLORを修正したことによる）  
  おそらく negative-city-mask の指定から坂出市をはずすことができれば実現すると思う。
  乱暴な方法としては、マスクの色を透明にするという方法もある。←この方法を採用した。
- 各種アイコンを坂出市のものにする
- 坂出市がオープンデータとして公開している情報を掲載する