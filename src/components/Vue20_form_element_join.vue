<template>
  <h1>form element Join</h1>
  <form action="./" ref="frm" method="get">
  <fieldset>
    <legend>회원 가입</legend>
    <div>
      <label for="id" class="title">ID</label>
      <input type="text" ref="id" id="id">
    </div>

    <div>
      <label for="id" class="title">Name</label>
      <input type="text" ref="name" id="name">
    </div>

    <div>
      <label for="pass" class="title">Password</label>
      <input type="password" ref="pass" id="pass">
    </div>

    <div>
      <label for="repass" class="title">RePassword</label>
      <input type="password" ref="repass" id="repass">
    </div>

    <div>
      <label class="title">Hobby</label>
      <label :for="item" v-for="(item, i) in hobbyList" :key="i">
        {{item}}<input type="checkbox" name="hobby" id="item" value="item">
    </label>
    </div>

    <div>
      <label class="title">Gender</label>
      <label :for="item" v-for="(item, i) in genderList" :key="i">
        <input type="radio" name="gender" :id="item" :ref="item" :value="item" v-model="gender">{{item}}
    </label>
    </div>

    <div class="plz">
      <label for="id">Mobile</label>
      <div class="plz1">
      <select v-model="mobile" ref="m1" class="plz-1" name="mobile" id="mobile">
        <option :value="item" v-for="(item, i) in mobileList" :key="i">{{item}}</option>
      </select> - <input type="text" ref="m2" id="mobile1" class="m1"> - <input type="text" ref="m3" class="m1" id="mobile2"></div>
      <input type="hidden" ref="mobile">
    </div>

    <div>
      <label class="title"></label>
      <button ref="btnJoin" class="btn-margin" @click.prevent="join">가입</button>
      <button ref="btnCancel" v-on:click.prevent="cancel" type="submit">취소</button>
    </div>
  </fieldset>
  </form>
</template>

<script>
export default {
  data: () => ({
    hobby: [],
    hobbyList: ['축구', '배구', '농구'],
    gender: '여',
    genderList: ['남', '여'],
    mobile: '010',
    mobileList: ['010', '011', '016']
  }),
  methods: {
    join() {
      const frm = this.$refs.frm
      const id = this.$refs.id
      const name = this.$refs.name
      const pass = this.$refs.pass
      const repass = this.$refs.repass
      const m1 = this.$refs.m1
      const m2 = this.$refs.m2
      const m3 = this.$refs.m3
      const mobile = this.$refs.mobile
      
      if(frm.value=="") {
          alert("폼을 입력하세요")
          frm.focus()
          return
      }
      if(id.value=="") {
        alert("아이디를 입력하세요")
        id.focus()
        return
      }
      if(name.value=="") {
        alert("이름을 입력하세요")
        name.focus()
        return
      }
      if(pass.value=="") {
        alert("비밀번호를 입력하세요")
        pass.focus()
        return
      }
      if(pass.value!==repass.value) {
        alert("비밀번호가 서로 다릅니다")
        pass.value=""
        repass.value=""
        pass.focus()
        return
      }
      if(m2.value=="") {
        alert("전화번호를 입력하세요")
        m2.focus()
        return
      }
      if(m3.value=="") {
        alert("전화번호를 입력하세요")
        m3.focus()
        return
      }
      mobile.value = m1.value + m2.value + m3.value;
      frm.submit();
    },
    cancel() {
      this.$refs.frm.reset()
      document.querySelector('#여').checked = true // 단순히 document의 값을 초기화
    }
  }
}
</script>

<style>
  .title {
    display: inline-block;
    width: 120px;
    margin: 5px;
    text-align: left;
  }
  .m1 {
    width: 50px;
  }
  .btn-margin {
    margin: 10px;
  }
  legend {
    text-align: center;
  }
  .plz {
    display: flex;
    position: relative;
    left: 5px;
    
  }
  .plz1 {
    position: relative;
    left: 77px;
  }
  /* fieldset div {
    width: 250px;
    text-align: left;
  } */
</style>