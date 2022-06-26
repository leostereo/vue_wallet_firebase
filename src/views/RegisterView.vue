<template>
  <h1> Reg 
    <button @click="signInWithGoogle">
Google
    </button>
  </h1>
</template>


<script setup>
//import {ref} from 'vue'
import {getAuth, GoogleAuthProvider , signInWithPopup} from "firebase/auth"


const signInWithGoogle = () => {
  console.log('sgin wit google')
  const provider = new GoogleAuthProvider();
  signInWithPopup(getAuth(),provider)
  .then((result)=> {
    console.log(result.user)
    

  });
}

</script>