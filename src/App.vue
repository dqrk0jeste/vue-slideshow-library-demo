<script setup lang="ts">
import type { DefineComponent } from 'vue';
import Test from './components/Test.vue'
import { Slideshow } from 'vue-slideshow-library';
</script>

<template>
  <div
    style="
      z-index:20;
      width: 100%;
      height: 1000px;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 5rem;
      color: white;
      background-color: red;
    ">
      BEFORE
  </div>
  <Slideshow :slides="[
      {
        component: Test as DefineComponent,
        props: {
          title: 'SLIDE 1'
        },
        backgroundColor: 'green',
        transitionName: 'left'
      },
      {
        component: Test as DefineComponent,
        props: {
          title: 'SLIDE 2'
        },
        backgroundColor: 'blue',
        transitionName: 'left'
      },
      {
        component: Test as DefineComponent,
        props: {
          title: 'SLIDE 3'
        },
        backgroundColor: 'violet',
        transitionName: 'left'
      },
      {
        component: Test as DefineComponent,
        props: {
          title: 'SLIDE 4'
        },
        backgroundColor: 'red',
        transitionName: 'left'
      }
    ]"
    :background-color-transition-duration-in-miliseconds="1000"
    :background-color-transition-mode="'ease-in'" 
  />
  <div
    style="
      z-index:20;
      width: 100%;
      height: 1000px;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 5rem;
      color: black;
      background-color: yellow;
    ">
      AFTER
  </div>
</template>

