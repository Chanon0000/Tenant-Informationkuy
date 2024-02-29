<template>
  <div class="user-profile">
   

    <!-- ข้อมูลพื้นฐาน -->
    <section>
      <h2>ข้อมูลพื้นฐาน</h2>
      <div>
        <p><strong>ชื่อ-สกุล:</strong> <span class="bold">{{ userProfile.name }}</span></p>
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
</style>
