<template>
  <v-from class="lgn">
    <v-container>
      <p class="title font-weight-bold">ลงชื่อเข้าใช้.</p>
      <v-col>
        <v-text-field
          v-model="usn"
          label="ชื่อผู้ใช้งาน"
          outlined
          required
          type="text"
        ></v-text-field>
      </v-col>
      <v-col>
        <v-text-field
          v-model="pwd"
          type="password"
          label="รหัสผ่าน"
          outlined
          required
        ></v-text-field>
      </v-col>
      <div class="btn">
        <v-btn class="sm justify-center" color="primary" @click="submit"
          >ยืนยัน</v-btn
        >
        <v-btn
          class="cc justify-center"
          outlined
          color="secondary"
          @click="cancle"
          >ยกเลิก</v-btn
        >
      </div>
    </v-container>
  </v-from>
</template>

<script>
export default {
  data: () => ({
    try: false,
    errMsg: '',
    cntEnt: false,
    usn: '',
    pwd: '',
  }),
}
</script>

<style lang="scss" scoped>
.lgn {
  width: 27%;
}
.btn {
  text-align: center;
}
.title {
  font-size: 60;
}
.sm {
  width: 25%;
}
.cc {
  margin-left: 20%;
  width: 25%;
}
</style>
