# clock_project

 <title>Clock</title>
    <style>
        h2{
            font-size: 100px;
            font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
            color: darkgreen;
            text-align: center;
        }
    </style>
</head>
<body onload="showTime()">
                <h2>                    
                </h2>
             <script>
                function showTime(){
                        var a = new Date();
                        var h = a.getHours();
                        var m = a.getMinutes();
                        var s = a.getSeconds();
                        var session = "AM";
                          if (h>=12){
                            session = "PM";
                          }                                             
                        if (h > 12)
                        {
                            h = h-12;
                            //  if there will be 13 then 13-12= 1 will display
                        }
                        h = h < 10 ? "0"+h : h;       // it is used for show single digit hour 1-9 with display 0 like 01 , 02 , 03........and here used ternuary operator because if h is less than 10 then display with 0 or if graeter than 10 (like 10, 11, 12..  )then display as it is.
                        m = m < 10 ? "0"+m : m;
                        s = s < 10 ? "0"+s : s;
                        var time = h + " : " + m + " : " + s + "  "  + session;           // used for hour : minute : second format
                        document.getElementsByTagName('h2')[0].innerText = time;
                        setTimeout(showTime,1000);      // it is used for refresh each second automatically
                }
             </script>   
</body>
