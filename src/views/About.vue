<template>
  <div class="root">
    <div class="mypaper"></div>

    <mu-paper class="demo-paper" :z-depth="4" id="mypaper">
      <div class="title">
        <div id="myicon">
          <img src="../assets/input.png" alt width="20px" />
        </div>
        <div class="text">输入条件</div>
        <div class="condition">
          <mu-text-field v-model="value2" placeholder="转速n" help-text="rpm"></mu-text-field>
          <br />
          <mu-text-field v-model="value2" placeholder="扬程H" help-text="m"></mu-text-field>
          <br />
          <mu-text-field v-model="value2" placeholder="流量Q" help-text="m^3/s"></mu-text-field>
          <br />
        </div>
        <div class="buttons">
          <mu-button small color="#7A7E83">计算</mu-button>

          <mu-paper class="demo-paper" :z-depth="5" id="mybutton">
            <mu-button small>清空</mu-button>
          </mu-paper>
        </div>
      </div>
    </mu-paper>

    <mu-paper class="demo-paper" :z-depth="4" id="mypaper">
      <div class="title">
        <div id="myicon">
          <img src="../assets/result.png" alt width="20px" />
        </div>
        <div class="text">计算结果</div>
        <div class="padding10">
          <h3 class="myh3">比转速(Ns)=</h3>

          <div id="res">
            <font color="#f44336">3.570</font>
          </div>
        </div>
      </div>
    </mu-paper>

    <mu-paper class="demo-paper" :z-depth="4" id="mypaper">
      <div id="inline">
        <div id="myicon">
          <img src="../assets/note.png" alt width="20px" />
        </div>
        <div class="text">备注</div>
      </div>
      <img src="../assets/formula.png" alt width="50%" />
      <div class="center">
        <p
          class="para"
        >&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;比转速（数）是从相似理论中引出来的一个综合性参数，它说明着流量、扬程、转数之间的相互关系。同一台水泵，在不同的工况下具有不同的比转数。一般是取最高效率工况时的比转速（数）做为水泵的比转速（数）。在＝150~250的范围，泵的效率最好，当＜60时，泵的效率显著下降；采用单吸叶轮过大时，可考虑改用双吸，反之采用双吸过小时，可考虑改用单吸叶轮。</p>
      </div>
    </mu-paper>
  </div>
</template>
<style scoped>
.text {
  font-size: 22px;
  font-weight: bold;
  clear: both;
  display: inline-block;
  padding-bottom: 10px;
  /* border: 1px solid red; */
}
#myicon {
  padding-top: 10px;
  display: inline-block;
  /* border: 1px solid red; */
  margin-right: 5px;
}
.about {
  text-align: left;
  overflow: auto;
}
.title {
  margin: 10px 10px;
}
#mypaper {
  border-radius: 10px;
  width: 90%;
  margin: auto;
}
#mybutton {
  display: inline;
  margin-left: 10%;
}
.buttons {
  padding: 5%;
}
.myh3 {
  display: inline;
}
#res {
  font-size: 17px;
  font-weight: bold;
  clear: both;
  display: inline-block;
}
.padding10 {
  padding-bottom: 10px;
}
.para {
  text-align: justify;
  width: 90%;
}
.center {
  display: flex;
  justify-content: center;
  align-item: center;
  margin-top: -10px;
}
</style>