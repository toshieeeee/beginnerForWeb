#Webサイトを作ろう（超初心者向け）

##▼HTML

```
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
</head>
<body>

  <h1>キクチです</h1>

  <p>エンジニアをやっています。</p>

  <p>趣味はサバイバルです</p>

  <button class="button">2017年の運勢を占う</button>

  <p class="result"></p>

  <div><img src="yuusha.gif" class="image"></div>
  
</body>
</html>

```

##▼CSS

```

<style type="text/css">

  body{
   /*background: green;*/
  }
  
  h1 {
    font-size: 24px;
    font-weight: 100;
  }

  h1:hover {
    color:red;
  }

  p {
    font-size :12px;
    font-weight: 100;
  }

  img {
    margin-top: 120px;
    position: absolute;
  }

  .result{
    font-size: 24px;
  }

</style>

```

##▼JavaScript - jQuery 

```

<!--<script type="text/javascript" src="./js/jquery.js"></script>-->
<script type="text/javascript" src="http://ajax.googleapis.com/ajax/libs/jquery/1.10.2/jquery.min.js"></script>
<script>


$('.button').click(function(){ // クリックしたら、イベントを実行

  /***********************
  ▼使用するデータを定義
  ************************/

  var $name = Array('NAME_1','NAME_2','NAME_3','NAME_4'); // おみくじの中身を、定義する
  var $unsei = Array('大吉','中吉','小吉','末吉'); // おみくじの中身を、定義する

  /***********************
  ▼処理を追加
  ************************/

  var $num = Math.round(Math.random() * 3); // ランダムな処理を、付け加える

  /***********************
  ▼結果を出力
  ************************/

  $('.result').text('「' + $name[$num] + '」さんの今年の運勢は・・・ 「' + $unsei[$num] + '」です！');

  $(".image").delay(500).animate({top:"0px"},{duration:300})
             .animate({top:"200px"},{duration:300})
             .animate({top:"0px"},{duration:300})
             .animate({top:"200px"},{duration:300});

});

</script>

```
