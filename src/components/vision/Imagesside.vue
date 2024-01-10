<template>
  <div class="imagesside mt-md-16 mt-10 pt-md-8 pt-5 text-center" style="top: 0">
    <img :src="img1" class=""/>
    <img :src="img2" class=""/>
    <img :src="img3" class=""/>
  </div>
</template>
<script>
import img1 from "../../assets/image/remal.png";
import img2 from "../../assets/image/serv1.png";
import img3 from "../../assets/image/Img3.png";
export default {
  data() {
    return {
      img1,
      img2,
      img3
    };
  },
};
</script>
<style lang="scss" scoped>

@keyframes example {
	0% {transform: scale(1)  }
	50% { transform: scale(1.1) }
  100% { transform: scale(1) }
}
.imagesside img{
    display: block;
border-radius:50% ;
border: 2px solid #fff;
animation: example 3s infinite;

box-shadow: 0px 25px 23px 0px rgba(0, 0, 0, 0.15);
}
.imagesside img:first-child{
    margin: auto;
width: 100px;
height: 100px;
}
.imagesside img:nth-child(2){
    margin-right: auto;
width: 200px;
height: 200px;
}
.imagesside img:last-child{
    margin-right: 55px;
    margin-top: -85px;
    width: 240px;
    height: 240px;
}
@media (max-width: 1399px) { 
    .imagesside img:last-child{
    margin-right: 0;
   
}
    
}
@media (max-width: 1199px) {

}
@media (max-width: 960px) {
.imagesside{
    width: 60%;
    margin: auto;
}

}
@media (max-width: 767px) {
    .imagesside{
    width: 75%;
}
}
@media (max-width: 575px) {
    .imagesside img:first-child{
width: 90px;
height: 90px;
}
.imagesside img:nth-child(2){
width: 140px;
height: 140px;
}
.imagesside img:last-child{
    margin-top: -50px;
    width: 180px;
    height: 180px;
}
    .imagesside{
    width: 100%;
}
}
</style>
