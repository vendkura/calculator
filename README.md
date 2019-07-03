<!doctype.html>
<html>
<head> 
    <script>
        function insert(num)
        {
            document.form.textview.value=  document.form.textview.value+num
        }
        function equal()
        {
            var exp= document.form.textview.value;
            if (exp)
                {
                    document.form.textview.value = eval(document.form.textview.value);
                }
        }
        function clean()
        {
             document.form.textview.value = "";
        }
        function back()
        {
            var exp= document.form.textview.value;
            document.form.textview.value = exp.substring(0,exp.length-1);
            
        }
    </script>
    <style>
        *
        {
            margin:  0;
            padding: 0;
        }
        .button
        {
            width: 50px;
            height: 50px;
            font-size: 25;
            margin: 2;
            cursor: pointer;
            background: #ff9800 ;
            border: none;
            color: white
        }
        .textview
        {
            width: 218px;
            margin: 5px;
            padding:5px;
            font-size: 25px;
            border: none;
            color: #ff9800
        }
        .main
        {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translateX(-50%) translateY(-50%);
        }
        .bg
        {
            background: linear-gradient(to right, #00bcd4, #ffc107);
            height: 100%;   
        }
    </style>
    </head>

<body>
    <div class="bg"></div>
    <div class="main">
    <form name="form">
        <input class="textview" name="textview">
    </form>
    <table>
        <tr>
            <td><input class="button" type="button" value="C" onclick="clean()"></td>
            <td><input class="button" type="button" value="<" onclick="back()"></td>
            <td><input class="button" type="button" value="/" onclick="insert('/')"></td>
            <td><input  class="button" type="button" value="X" onclick="insert('*')"></td>
        </tr>
          
          <tr>
            <td><input class="button" type="button" value="7" onclick="insert(7)"></td>
            <td><input class="button" type="button" value="8" onclick="insert(8)"></td>
            <td><input class="button" type="button" value="9" onclick="insert(9)"></td>
            <td><input class="button" type="button" value="-" onclick="insert('-')"></td>
        </tr>
        <tr>
            <td><input class="button" type="button" value="4" onclick="insert(4)"></td>
            <td><input class="button" type="button" value="5" onclick="insert(5)"></td>
            <td><input class="button" type="button" value="6" onclick="insert(6)"></td>
            <td><input class="button" type="button" value="+" onclick="insert('+')"></td>
        </tr>
          <tr>
            <td><input class="button" type="button" value="1" onclick="insert(1)"></td>
            <td><input class="button" type="button" value="2" onclick="insert(2)"></td>
            <td><input class="button" type="button" value="3" onclick="insert(3)"></td>
            <td rowspan="5"><input style="height: 106px" class="button" type="button" value="=" onclick="equal()"></td>
        </tr>
        
          <tr>
            <td colspan="2"><input style="width:106px" class="button" type="button" value="0" onclick="insert(0)"></td>
            <td><input class="button" type="button" value="." onclick="insert('.')"></td>
        </tr>
        
        </table></div>
    
    </body>
</html>
