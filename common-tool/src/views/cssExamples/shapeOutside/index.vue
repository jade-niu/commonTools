<template>
  <div class="wraper">
    <h2>shape-outside</h2>
    <p>shape-outside属性指定使用下面列表的值来定义浮动元素的浮动区域。这个浮动区域决定了行内内容（浮动元素）所包裹的形状。<br>
      shape-image-threshold 通过设定一个alpha通道的界限值来提取shape-outside 值为图像的形状。
    </p>
    <div class="examples">
      <div class="item"
           v-for="item in shapeList"
           :key="item.key">
        <h4>{{item.title}}</h4>
        <shape-img :class="'shapes'+item.key"></shape-img>
        <shape-text></shape-text>
      </div>
    </div>
  </div>
</template>

<script>
import shapeText from "./shapeText.vue";
import shapeImg from "./shapeImg.vue";
export default {
  name: "shapeOutside",
  data() {
    return {
      shapeList: [
        {
          key: "1",
          title: "创建圆:shape-outside: circle(50%);"
        },
        {
          key: "2",
          title: "创建多边形:shape-outside: polygon(100% 0, 100% 100%, 0 100%);"
        },
        {
          key: "3",
          title: "创建椭圆:shape-outside: ellipse(72px 88px);"
        },
        {
          key: "4",
          title: "创建矩形: shape-outside: inset(72px 88px);"
        },
        {
          key: "5",
          title:
            "创建渐变图像：shape-outside: linear-gradient(30deg, #2d8cf0, transparent 80%, transparent);shape-image-threshold: 0.2;"
        }
      ]
    };
  },
  components: { shapeText, shapeImg }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.wraper {
  display: flex;
  flex-wrap: wrap;
}
h4 ,p{
  text-align: left;
}

.wraper .item {
  width: 390px;
  height: 400px;
  overflow: hidden;
  float: left;
}
.examples {
  width: 100%;
}
.examples::after {
  content: "";
  clear: both;
}
.shapes1 {
  shape-outside: circle(50%);
}

.shapes2 {
  shape-outside: polygon(10px 0, 100% 100%, 0 100%);
}

.shapes3 {
  shape-outside: ellipse();
}

.shapes4 {
  shape-outside: inset(72px 88px);
}
.shapes5 {
  shape-outside: linear-gradient(30deg, #2d8cf0, transparent 80%, transparent);
  shape-image-threshold: 0.2;
  border-radius: 0;
  border: 0;
}
</style>
