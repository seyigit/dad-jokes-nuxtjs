<template>
<div>
  <h2>
    <div> {{jokes}}</div>
  </h2>
</div>
</template>

<script>
export default {
head(){
    return {
        title : 'Welcome To Dad Jokes',
        meta : [
            {
                hid: 'description',
                name : 'description',
                content : 'Best place for corny dad jokes'
            }
        ]
    }
},
props : ["jokes"]
}
</script>

<style>

</style>
