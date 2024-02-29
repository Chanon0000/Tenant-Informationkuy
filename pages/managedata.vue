<template>
  <div class="user-profile">
 

    <!-- ข้อมูลพื้นฐาน -->
    <section>
      <h2>ข้อมูลพื้นฐาน</h2>
      <div>
        <p><strong>ชื่อ-สกุล:</strong> <span>{{ userProfile.name }}</span></p>
      </div>
    </section>

    <!-- เพศ -->
    <section>
     
      <div>
        <p><strong>เพศ:</strong> {{ userProfile.gender }}</p>
      </div>
    </section>

    <!-- ข้อมูลติดต่อ -->
    <section>
     
      <div>
        <p><strong>อีเมล:</strong> {{ userProfile.email }}</p>
        <p><strong>เบอร์โทร:</strong> {{ userProfile.phone }}</p>
        <p><strong>ที่อยู่:</strong> {{ userProfile.address || 'ไม่ระบุ' }}</p>
      </div>
    </section>

    <!-- รหัสผ่าน -->
    <section>
      
      <div>
        <p><strong>รหัสผ่าน:</strong> ********</p>
      </div>
      
    </section>

    <!-- ปุ่มแก้ไข -->
    <button @click="editProfile">แก้ไข</button>
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
      // เพิ่มโค้ดที่ต้องการทำเมื่อคลิกปุ่มแก้ไข
      alert('กำลังเข้าสู่โหมดแก้ไขข้อมูลผู้ใช้');
    }
  }
};
</script>

<style scoped>
.user-profile {
  font-family: Arial, sans-serif;
  margin: 0 auto;
  max-width: 600px;
  padding: 20px;
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
  background-color: #0056b3;
}
</style>
