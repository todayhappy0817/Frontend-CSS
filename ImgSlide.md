##HTML

```

    <div id="slide">
        
        <input type="radio" name="pos" id="pos1" checked>
        <input type="radio" name="pos" id="pos2" >
        <input type="radio" name="pos" id="pos3">
        <input type="radio" name="pos" id="pos4">
        <ul>
            <li>slid1</li>
            <li>slide2</li>
            <li>slide3</li>
            <li>slide4</li>
        </ul>
        <p class="pos">
            <!-- 선택시 자동으로 radio 버튼이 클릭이 된다 for안에 input id를 집어넣어서 사용한다.-->
            <label for="pos1"></label> 
            <label for="pos2"></label>
            <label for="pos3"></label>
            <label for="pos4"></label>
        </p>
    </div>



```


##CSS

```
*{margin:0;padding:0;}

ul,li{list-style:none;}

#slide{height:300px;position:relative;overflow:hidden;}

#slide ul{width:400%;height:100%;transition:1s;}
/* trasition의 s값을 통해  그 동안 변경됨 */
#slide ul:after{content:"";display:block;clear:both;} 
/* contant속성은 생성한 값으로 요소를 대체한다 after은 그 후 값을 변경한다*/

#slide li{float:left;width:25%;height:100%;}

#slide li:nth-child(1){background:#faa;}

#slide li:nth-child(2){background:#ffa;}

#slide li:nth-child(3){background:#faF;}

#slide li:nth-child(4){background:#aaf;}

#slide input{display:none;}

#slide label{
    display:inline-block;
    vertical-align:middle;
    width:10px;height:10px;
    border:2px solid #666;
    background:#fff;
    transition:0.3s;
    border-radius:50%;
    cursor:pointer;
}
#slide .pos{
    text-align:center;
    position:absolute;
    bottom:10px;left:0;
    width:100%;
    text-align:center;
}

#pos1:checked~ul{margin-left:0%;}

#pos2:checked~ul{margin-left:-100%;}

#pos3:checked~ul{margin-left:-200%;}

#pos4:checked~ul{margin-left:-300%;}

#pos1:checked~.pos>label:nth-child(1){background:#666;}

#pos2:checked~.pos>label:nth-child(2){background:#666;}

#pos3:checked~.pos>label:nth-child(3){background:#666;}

#pos4:checked~.pos>label:nth-child(4){background:#666;}


```
