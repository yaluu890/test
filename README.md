<!doctype html>
<html lang="zh-tw">
  <head>
    <!-- Required meta tags -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.1/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-+0n0xVW2eSR5OomGNYDnhzAbDsOXxcvSN1TPprVMTNDbiYZCxYbOOl7+AMvyTG2x" crossorigin="anonymous">

    <title>Hello, world!</title>
  </head>
  <body>
    <h1>Hello, world!</h1>
    <div class="container-fluid">
        <div class="row">
            <div class="col-md-4">test01</div>
            <div class="col-md-8"><div style="border:2px rgb(0, 255, 157) solid;text-align: center"；>BMI計算器</div>
            <div style="border:5px rgb(255, 196, 0) solid;text-align: center">BMI計算公式=體重(公斤) / 身高2(公尺2)</div>
        <script>
          var BMI={};
         BMI.getBMI=function(a,b){
            var bmi=b/((a/100)*(a/100));
            return bmi;
          };
          BMI.idealweight=function(a){
            var x=(a-100)*0.9;
            return x;
          };
          function Cal(form){
            var a=eval(form.height.value);
            var b=eval(form.weight.value);
            var bmi=eval(form.BMI.value);
            var bmiValue =BMI.getBMI(a,b);
            BMI.disp_alert(bmiValue );
            form.IW.value=BMI.idealweight(a);
            form.BMI.value= bmiValue ;
          }
          BMI.disp_alert = function(bmi){
            if (bmi < 18.5)
            {
              alert("過輕"); 
            }
            else if (bmi >= 18.5 && bmi < 25)
            {
              alert("正常");
            }
            else if (bmi >= 25 && bmi< 30)
            {
              alert("過重");
            }
            else
            {
              alert("過重");
            }
          }
        </script>
        </head>
        <body>
        <form method=post>
            <div style="border:2px rgb(45, 45, 122) solid;width:20%;display:inline-block;text-align: center">你的身高(cm):<input type="text" name="height"></div><br>
          <br/>
          <div style="border:2px rgb(99, 169, 201) solid;width:20%;display:inline-block;text-align: center">你的體重(kg):<input type="text" name="weight"></div><br>
          <br/>
        <input type="button" value="開始計算" onclick="Cal(this.form)">
          <br/>
          <br/>
          你的理想體重:<input type="text" name="IW"><br/>
          <br/>
          <div style="border:2px rgb(158, 99, 201) solid;width:20%;display:inline-block;text-align: center">您的BMI:<input type="text" name="BMI"></div>
        </form> </div>
        </div>
    </div>

    <!-- Optional JavaScript; choose one of the two! -->

    <!-- Option 1: Bootstrap Bundle with Popper -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.1/dist/js/bootstrap.bundle.min.js" integrity="sha384-gtEjrD/SeCtmISkJkNUaaKMoLD0//ElJ19smozuHV6z3Iehds+3Ulb9Bn9Plx0x4" crossorigin="anonymous"></script>

    <!-- Option 2: Separate Popper and Bootstrap JS -->
    <!--
    <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.9.2/dist/umd/popper.min.js" integrity="sha384-IQsoLXl5PILFhosVNubq5LC7Qb9DXgDA9i+tQ8Zj3iwWAwPtgFTxbJ8NT4GN1R8p" crossorigin="anonymous"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.0.1/dist/js/bootstrap.min.js" integrity="sha384-Atwg2Pkwv9vp0ygtn1JAojH0nYbwNJLPhwyoVbhoPwBhjQPR5VtM2+xf0Uwh9KtT" crossorigin="anonymous"></script>
    -->
  </body>
</html>
