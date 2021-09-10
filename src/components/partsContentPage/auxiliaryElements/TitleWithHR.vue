<template>
  <div>
    <div class="boldText">
        <slot />
    </div>
	<hr id='hr'/>
  </div>
</template>


<script>
export default {
  props: {},
  data() {
    return {}
},
  components: {}
}
</script>


<style scoped>
.boldText {
		font-weight: bold;
		font-size: 24px;
		line-height: 32px;
}

#hr {
    width: 832px;
    border: 0px;
    height: 1px;
    background-color: rgba(0, 0, 0, 0.2);;
}

</style>