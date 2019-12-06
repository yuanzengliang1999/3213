<template>
  <div class="home">
    <van-swipe @change="onChange">
      <van-swipe-item>1</van-swipe-item>
      <van-swipe-item>2</van-swipe-item>
      <van-swipe-item>3</van-swipe-item>
      <van-swipe-item>4</van-swipe-item>

      <div class="custom-indicator" slot="indicator">{{ current + 1 }}/4</div>
    </van-swipe>
  </div>
</template>

<script>
import Vue from 'vue';
import { Swipe, SwipeItem } from 'vant';

Vue.use(Swipe).use(SwipeItem);

// @ is an alias to /src

export default {
  data() {
    return {
      current: 0
    };
  },
  methods: {
    onChange(index) {
      this.current = index;
    }
  }
};
</script>
