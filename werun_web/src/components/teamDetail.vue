<template>
  <div style="position: relative">
    <div class="header">
      <img id="logo" src="https://i.loli.net/2020/09/23/O9CUbHKVoPci7q3.png" />
      <div class="name">
        <span>WERUN</span>
        <br />
        <span>C L U B</span>
      </div>
    </div>
    <div id="context">
      <div id="nav">
        <div class="grade_box"><span class="grade">2019</span></div>
        <div class="grade_box"><span class="grade">2018</span></div>
        <div class="grade_box"><span class="grade">2017</span></div>
        <div class="grade_box"><span class="grade">2016</span></div>
        <div class="grade_box"><span class="grade">2015</span></div>
        <div class="grade_box"><span class="grade">2014</span></div>
        <div class="grade_box"><span class="grade">2013</span></div>
        <div class="grade_box"><span class="grade">2012</span></div>
      </div>
      <div id="people">
        <div class="person" v-for="(item, index) in peopleList">
          <div class="personDetail">
            <img class="news_img" :src="item.img" />
            <span class="title1">{{ item.name }}</span>
            <div class="line"></div>
            <span class="description"
              >{{ item.grade }}、{{ item.major }}、{{ item.dir }}</span
            >
          </div>
        </div>
      </div>
    </div>
    <div id="footer">
      <myFooter></myFooter>
    </div>
  </div>
</template>
<script>
import myHeader from "@/components/header";
import myFooter from "@/components/footer";
export default {
  data() {
    return {
      peopleList: [
        {
          img: "https://i.loli.net/2020/09/24/XYgTzaldxZJksu2.jpg",
          name: "孙一恒",
          grade: "2017",
          major: "软件工程",
          dir: "后端",
        },
        {
          img: "https://i.loli.net/2020/09/24/uNwtjIHARCJKo9r.jpg",
          name: "鹿轶轩",
          grade: "2018",
          major: "软件工程",
          dir: "后端",
        },
        {
          img: "https://i.loli.net/2020/09/24/WH32b5Y1BxUO9jG.jpg",
          name: "莫张浩",
          grade: "2018",
          major: "计算机科学与技术",
          dir: "前端",
        },
        {
          img: "https://i.loli.net/2020/09/24/3bTWSMKkhIFVENv.jpg",
          name: "刘俊良",
          grade: "2018",
          major: "软件工程",
          dir: "后端",
        },
        {
          img: "https://i.loli.net/2020/09/24/XYgTzaldxZJksu2.jpg",
          name: "孙一恒",
          grade: "2017",
          major: "软件工程",
          dir: "后端",
        },
        {
          img: "https://i.loli.net/2020/09/24/uNwtjIHARCJKo9r.jpg",
          name: "鹿轶轩",
          grade: "2018",
          major: "软件工程",
          dir: "后端",
        },
        {
          img: "https://i.loli.net/2020/09/24/WH32b5Y1BxUO9jG.jpg",
          name: "莫张浩",
          grade: "2018",
          major: "计算机科学与技术",
          dir: "前端",
        },
        {
          img: "https://i.loli.net/2020/09/24/3bTWSMKkhIFVENv.jpg",
          name: "刘俊良",
          grade: "2018",
          major: "软件工程",
          dir: "后端",
        },
      ],
    };
  },
  methods: {},
  mounted() {},
  components: {
    myHeader,
    myFooter,
  },
};
</script>
<style scoped>
.personDetail {
  margin-left: 5px;
  height: 250px;
  width: 98%;
  /* border:2px solid gold; */
  background-color: rgb(255, 250, 250);
  margin-bottom: 10px;
}
.news_img {
  width: 110px;
  height: 110px;
  border-radius: 60px;
  float: left;
  margin-top: 20px;
  margin-left: 50px;
}
.title1 {
  position: absolute;
  left: 200px;
  font-size: 25px;
  font-weight: bold;
  display: inline-block;
  margin-top: 55px;
}
.description {
  position: absolute;
  left: 70px;
  font-size: 15px;
  display: inline-block;
  margin-top: 175px;
  color: grey;
}
.grade_box {
  width: 100%;
  height: 100px;
  background-color: #0d3590;
  border: 1px solid white;
  text-align: center;
}
.grade_box :hover {
  cursor: pointer;
  background-color: #204fbd;
  transition: all ease 0.3s;
  -webkit-transition: all ease 0.3s;
}
.grade {
  width: 100%;
  height: 100px;
  display: inline-block;
  font-size: 30px;
  line-height: 100px;
  /*margin-bottom: 2px;*/
  color: white;
  transition: all ease 0.3s;
  -webkit-transition: all ease 0.3s;
}
#people {
  position: relative;
  margin-left: 350px;
  height: 100%;
  /* border:5px solid green; */
  overflow: auto;
}
#context {
  margin: 195px;
  /* border:2px solid red; */
  flex: 1 1 auto;
  margin-top: 250px;
}
#nav {
  width: 350px;
  height: 100%;
  /* border:2px solid red; */
  float: left;
}
h1 {
  margin-top: 350px;
  font-size: 60px;
}

.header {
  height: 170px;
  width: 100%;
  position: fixed;
  top: 0px;
  z-index: 5;
  background-color: white;
  transition: background-color 0.5s linear;
}
#logo {
  margin-top: 70px;
  width: 50px;
  height: 50px;
  float: left;
  margin-left: 195px;
}
.name {
  float: left;
  margin-top: 67px;
  margin-left: 20px;
  color: #0d3590;
  font-size: 20px;
  font-weight: bold;
}
#context {
  height: 100vw;
}
#footer {
  height: 270px;
  background-color: #0d3590;
}
.line {
  position: absolute;
  margin-top: 150px;
  width: 90%;
  margin-left: 20px;
  border-top: 2px solid #0d3590;
}
</style>