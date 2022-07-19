<html>
    <head>
        <link rel="stylesheet" href="style.css">
        <link>
        <meta charset="utf-8">
            <script>
                var money = 0;
                var doble = 1;
                var auto_money = 0;
                var shop_sell1 = 100;
                var shop_sell2 = 30;
                
                function a(){
                    money = money + doble;
                    naw = document.getElementById("i1");
                    naw.innerHTML = money;
                }
                
                function time(){
                    money = money + auto_money;
                    naw = document.getElementById("i1");
                    naw.innerHTML = money;
                    setTimeout(time, 1000);
                }
                
                function shop1(){
                    
                    if (money >= shop_sell1){
                        money = money - shop_sell1;
                        shop_sell1 = shop_sell1 += shop_sell1/2;
                        shop_sell1 = Math.round( shop_sell1 )
                        var naw = document.getElementById("i2");
                        naw.innerHTML = "+1/" + shop_sell1 + "руб";
                        auto_money = auto_money + 1
                        
                    }
                }
                function shop2(){
                    if (money >= shop_sell2){
                        money = money - shop_sell2;
                        shop_sell2 = shop_sell2 += shop_sell2/2;
                        shop_sell2 = Math.round( shop_sell2 )
                        var naw = document.getElementById("i3");
                        var naw2 = document.getElementById("submit");
                        naw.innerHTML = "+1/" + shop_sell2 + "руб";
                        doble = doble + 1
                        naw2.innerHTML = "+"+doble;
                        
                    }
                }
                setTimeout(time, 1000);
                
            </script>
    </head>
    <body>
        <div class="new1">
            <div class="f2">
                <div class="f3">
                    <label>auto</label>
                    <button id="i2" onclick="shop1()">+1/100руб</button>
                </div>
                <div class="f1">
                    <div>
                        <label id = "i1" class="font1"> 0 </label>
                    </div>
                    <div>
                        <button type="submit" id="submit" class="btn" onclick="a();">+1</button>
                    </div>
                </div>
                
                <div class="f3">
                    <label>onclick</label>
                    <button id="i3" onclick="shop2()">+1/30руб</button>
                </div>
            </div>
            
        </div>
        
    </body>
</html>




