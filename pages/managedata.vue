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
 <div class="shad"></div>
<div class="user-profile">


 <!-- ข้อมูลพื้นฐาน -->
 <section>
   <h2><b>ข้อมูลพื้นฐาน</b></h2>
   <div>
     <p><strong>ชื่อ-สกุล:</strong> <span>{{ userProfile.name }}</span> </p>
   </div>
 </section>

 <!-- เพศ -->
 <section>
  
   <div>
     <p><strong>เพศ:</strong> {{ userProfile.gender }} </p>
   </div>
 </section>

 <!-- ข้อมูลติดต่อ -->
 <section>
  <div><b>ข้อมูลติดต่อ</b></div>
 
   <div>
     <p><strong>อีเมล:</strong> {{ userProfile.email }} </p>
     <p><strong>เบอร์โทร:</strong> {{ userProfile.phone }} </p>
     <p><strong>ที่อยู่:</strong> {{ userProfile.address || 'ไม่ระบุ' }} </p>
   </div>
 </section>


    <!-- ปุ่มแก้ไข -->
     <!-- ปุ่มยืนยัน -->
     <div class="centered">
    <button @click="editProfile">ยืนยัน</button>
  </div>
  
  </div>

</template>

<script>
export default {
  data() {
    return {
      userProfile: {
        name: 'นาย แสงศักดิ์ วิบวับ',
        gender: 'ชาย',
        email: 'AAAAAAAA@gmail.com',
        phone: '08XXXXXXXX',
        address: null // ถ้าไม่มีที่อยู่ให้เป็น null
      }
    };
  },
  methods: {
    editProfile() {
      // การจัดการเหตุการณ์เมื่อคลิกที่ปุ่ม
      console.log('ยืนยัน');
    }
  }
};

</script>

<style scoped>
.user-profile {
  font-family: Arial, sans-serif;
  margin:  auto;
  max-width: 600px;
  padding: 10px;
}

section {
  margin-bottom: 30px;
}

h1 {
  text-align: center;
}

h2 {
  margin-bottom: 10px;
}

.bold {
  font-weight: bold;
}

.change-password {
  color: #56F000;
  cursor: pointer;
}

button {
  background-color: #007BFF;
  color: white;
  padding: 5px 10px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  
}

button:hover {
  background-color: #49f128;
}
.shad {
  background: linear-gradient(rgb(240, 240, 240), rgb(255, 255, 255)); /* Standard syntax */
  height: 20px;
}
.centered {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 10px; /* กำหนดความสูงของพื้นที่มองเห็น */
}
</style>
<!---->
<!---->