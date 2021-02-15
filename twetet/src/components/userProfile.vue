<template>
    <div>
        <h1 > {{fullName}} aka @{{user.userName}} is logged in</h1>
    <p> Followers: {{followers}} </p>
    <div class="user-badge" v-if="user.isAdmin"> Admin</div>
    <button @click="followUser" > Follow me</button>
    <div class="tweets" :key="i" v-for="(tweet,i) in user.tweets">
        {{tweet.content}}

    </div>

    </div>
</template>

<script>
export default {
     data(){
    return{
      followers: 0,
      user:{
        id: 1,
        userName: 'alaf',
        firstName: 'Abdullah',
        lastName: 'olalekan',
        email: 'bashxyz@gmail.com',
        isAdmin: true,
        tweets:[
            {id:1, content:"Follow back everyone. I am here to stay"},
            {id:2, content:"come to my home on monday."},
            {id:3, content:"I'm here bitches"}
        ]
      }
    }

  },
  computed: {
    fullName(){
      return `${this.user.firstName} ${this.user.lastName} `
    }
  },
  methods: {
    followUser(){
      this.followers++;
    }
  },
  mounted(){
      this.followUser();
  }
 
}
</script>

<style scoped>
.user-badge{
    background-color: rebeccapurple;
    font-weight: 700;
    width: 100px;
    border-radius: 4px;
    text-align: center;
    margin: 5px auto;
    padding: 5px;
    list-style-type:armenian;
    color: white;
}
</style>