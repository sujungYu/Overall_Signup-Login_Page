<template>
  <div class="signup">
      <p>회원가입</p>
      <form v-on:submit.prevent="submitForm">
      <input type="text" id="user" placeholder="아이디" v-model="user"><br>
      <input type="password" id="password" placeholder="비밀번호" v-model="password"><br>
      <button>가입하기</button>
      <span>또는 <router-link to="/">로그인</router-link>으로 돌아가기</span>
      </form>
  </div>
</template>

<script>
// import { registerUser } from '@/api/index';
// import axios from 'axios'


export default {
    name: 'signUp',
    data() {
        return {
            user: '',
            password: ''

        }
    },
//     methods: {
//         async submitForm() { // 비동기 객체가 오기때문에 비동기 처리
//       console.log('submit');
//       const userData = {
//         user: this.user,
//         password: this.password,
//       };
//       const { data } = await registerUser(userData); // Destructuring
//       this.logMessage = `${data.username}님이 가입되었습니다.`;
//       //template literal(백틱문법) 자바스크립변수를 문자열과 합침
//       this.initForm();
//     },
//     initForm() {
//       this.user = '';
//       this.password = '';
//     },
//   },

//     }
    methods: {
        submitForm() {
            // axios.post('/api/user/join', {
            //     user: this.user,
            //     password: this.password
            // }).then(res=> {
            //     console.log(res.data);
            // })
			console.log('dd');
		},
    }
}
</script>

<style>
.signup {
    margin-top: 40px;
}
input {
    margin: 10px 0;
    width: 20%;
    padding: 15px;
}
button {
    margin-top: 20px;
    width: 10%;
    cursor: pointer;
}
p {
    margin-top: 40px;
    font-size: 20px;
}
span {
    display: block;
    margin-top: 20px;
    font-size: 15px;
}
</style>