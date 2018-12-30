<template>
  <div class="test">
    <input type="text" v-model="title"/>
    <h1>{{title}}</h1>
    <p v-if="showName">{{user.first_name}}</p>
    <p v-else>Nobody</p>
    <ul>
      <li v-for="item in items">{{item.title}}</li>
    </ul>
    <button v-on:click="greet('hello worldd')">Say greeting</button>
    <br>
    <input type="text" v-on:keydown="pressKey" v-on:keyup.f="enterHit"/>
    <hr/>
    <label>
      firstname
      <input type="text" v-model="user.first_name">
    </label>
    <br/>
    <label>
      firstname
      <input type="text" v-model="user.last_name">
    </label>
    <h3>{{fullName}}</h3>

    <h2>{{msg}}</h2>
  </div>
</template>

<script>
  export default {
      name : 'test',
      props: {
          msg: {
            type:String,
            default:'Foobar'
          }
      },
      data() {
          return {
              title: 'Hello world',
              user: {
                  first_name: 'John',
                  last_name: 'Doe'
              },
              showName:true,
              items: [
                {title:'Item one'},
                {title: 'Item two'},
                {title: 'Item three'}
              ]
          }
      },
    methods: {
        greet: function (hello) {
          alert(hello);
        },
        pressKey: function (e) {
            console.log(e.target.value);
        },
        enterHit: function () {
            console.log('hit enter');
        }
    },
    computed: {
        fullName: function () {
            return this.user.first_name + ' ' + this.user.last_name;
        }
    }
  }
</script>

<style scoped>

</style>
