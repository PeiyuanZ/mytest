<script setup lang="ts">
import { onMounted } from 'vue'

function submitComment() {
  var comment = (document.getElementById('comment-input') as HTMLInputElement ).value;
            (document.getElementById('user-comment') as HTMLElement ).innerText = comment;
}

onMounted(() => {
  
})
</script>

<template>
  <div class="box">
    <h1>User Comments</h1>
    
    <!-- 用户评论区域 -->
    <div id="comments">
        <!-- 用户输入的评论 -->
        <p id="user-comment"></p>
    </div>

    <!-- 用户评论输入框 -->
    <textarea id="comment-input" placeholder="Leave a comment..."></textarea>
    <button @click="submitComment">Submit Comment</button>
  </div>
</template>

<style scoped>
.box {
  width: 10px;
  height: 10px;
  background-color: aqua;
}
</style>
