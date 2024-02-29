<template>
   <!-- นาฟบาร์ของต้า -->
   <nav class="bg-white"> 
      <div id="menu" class="flex justify-between items-center px-12">
          <div id="logo">
              <a href="#"><img src="public/logo.png" class="size-20"></a>
          </div>
          <ul class="flex font-bold text-black ">
              <li class="hover:text-[#0075BE] p-3"><a href="#">หน้าแรก</a></li>
              <li class="hover:text-[#0075BE] p-3"><a href="#">การชำระเงิน</a></li>
              <li class="hover:text-[#0075BE] p-3"><a href="#">ติดต่อเรา</a></li>
              <li class="hover:text-[#0075BE] p-3"><a href="#">เกี่ยวกับเรา</a></li>
          </ul>
          <div id="message-profile" class="flex justify-center">
              <div class="px-2 py-1 m-1 flex items-center justify-center hover:bg-slate-200">
                  <a href="#" class=""><i class="fa-regular fa-envelope"></i></a>
              </div>
              <div class="px-2 py-1 m-1 flex items-center justify-center hover:bg-slate-200">
                  <a href="#" class=""><i class="fa-regular fa-user"></i></a>
              </div>
          </div>
      </div>
    </nav>
    
    <!-- หัวข้อ -->
    <body>
        <div class="head items-center">
        <p id="head"></p>
        </div>
    </body>
    <div>
      <br>
        <p class="title"><b>การแจ้งเตือน</b></p>
    </div>
    <!-- --------- -->
    
    
    
  <div class="alerts">
    <alert-box v-for="(message, index) in messages" :key="index" :boxColor="index === 0 ? '#D9D9D9' : '#D9D9D9'">
      <span v-html="index === 0 ? coloredText(message) : message"></span>
    </alert-box>
  </div>

    <!-- <footer> -->
      <div class="flex justify-between bg-[#304269]">
    <div class="flex py-8 text-2xl">
        <a href="#"><i class="fa-brands fa-facebook  ml-10 pr-1"></i></a>
        <a href="#"><i class="fa-brands fa-instagram ml-10 pr-1"></i></a>
        <a href="#"><i class="fa-brands fa-x-twitter ml-10 pr-1"></i></a>
    </div>
    <div class="flex py-8 text-xl ">
        <a href="#"><p class="px-5 hover:underline">กฎกติกา</p></a>
        <a href="#"><p class="px-5 hover:underline">ลงโฆษณา</p></a>
        <a href="#"><p class="px-5 hover:underline">สมัครงาน</p></a>
    </div>
  </div>
  <!-- -------------- -->
</template>

<script>
import AlertBox from './AlertBox.vue'; // เรียกใช้ AlertBox component

export default {
  components: {
    AlertBox
  },
  data() {
    return {
      messages: [
        "รายละเอียดการชำระค่าเช่าของห้องพัก A1 <span style='color: #3D9DD9;'>ชำระเสร็จสมบูรณ์</span> <span style='float: right;'>15/08/2590</span>",
        "สถานะเครื่องซักผ้าเครื่องที่ 1   <span style='color: #6E7346;'> ดำเนินการอยู่อีก 8 นาที</span> <span style='float: right;'>15/08/2590</span>",
        "สถานะเครื่องซักผ้าเครื่องที่ 2    <span style='color: #3D9DD9;'> งดใช้ชั่วคราว</span> <span style='float: right;'>15/08/2590</span>",
        "สถานะเครื่องซักผ้าเครื่องที่ 3 <span style='color: #3D9DD9;'>ว่าง</span> <span style='float: right;'>15/08/2590</span>",
        "สถานะเครื่องซักผ้าเครื่องที่ 4<span style='color: #3D9DD9;'>ดำเนินการอยู่อีก 58 นาที</span> <span style='float: right;'>15/08/2590</span>",
        "สถานะเครื่องกดน้ำเครื่องที่ 1 <span style='color: #3D9DD9;'>ดำเนินการอยู่อีก 5 นาที</span> <span style='float: right;'>15/08/2590</span>",
        "สถานะเครื่องกดน้ำเครื่องที่ 2  <span style='color: #3D9DD9;'>ว่าง</span> <span style='float: right;'>15/08/2590</span>",
        "สถานะเครื่องกดน้ำเครื่องที่ 3  <span style='color: #3D9DD9;'>งดใช้ชั่วคราว</span> <span style='float: right;'>15/08/2590</span>",
        "สถานะเครื่องกดน้ำเครื่องที่ 4<span style='color: #3D9DD9;'> ดำเนินการอยู่อีก 2 นาที</span> <span style='float: right;'>15/08/2590</span>",
        "แจ้งให้ทราบในวันที่ 16/08/2590 การไฟฟาแจ้งว่าจะมีการตัดไฟเพื่อซ่อมบำรุงบริเวณหอพักของเรา ในเวลา 08:00 - 16:00 น. <br>จึงขอแจ้งให้ทราบและขออภัยในความไม่สะดวก<span style='float: right;'>15/08/2590</span>",
        "แจ้งให้ทราบในวันที่ 16/08/2590 การประปาแจ้งว่าจะมีการตัดไฟเพื่อซ่อมบำรุงบริเวณหอพักของเรา ในเวลา 08:00 - 09:00 น. <br>จึงขอแจ้งให้ทราบและขออภัยในความไม่สะดวก<span style='float: right;'>15/08/2590</span>",
        
      ]
    };
  },
  methods: {
    coloredText(message) {
      return message.replace(/<span style='color: #3D9DD9;'>/g, "<span style='color: #3D9DD9;'>");
      return message.replace(/<span style='color: #6E7346;'>/g, "<span style='color: #6E7346;'>");
    }
  }
  
};
</script>
<style scoped>


.title {
  margin-left: 100px;
  font-size: larger;
}

</style>