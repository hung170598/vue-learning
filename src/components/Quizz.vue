<template>
  <div id="Quizz">
    <div class="question-box">
      <h1>Bài Tập</h1>
      <div class="question">Câu hỏi 1: Đây là câu hỏi a a thứ 1?</div>
      <div class="answer">Trả lời</div>
      <div class="answer">Trả lời</div>
      <div class="answer">Trả lời</div>
      <div class="answer">Trả lời</div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
#Quizz {
  margin-top: 160px;
  width: 100%;
  display: flex;
  justify-content: center;
  position: fixed;
}
.question-box {
  text-align: center;
  width: 500px;
  height: 400px;
  border: 2px solid black;
  background-color: gainsboro;
  border-radius: 10px;
}
.question-box h1 {
  color: green;
  font: 20pt;
}
.question {
  background-color: green;
  color: white;
  width: 98%;
  margin: 20px 1%;
  font: 20pt black;
  font-weight: bold;
  border-radius: 10px;
}
.answer {
  background-color: white;
  width: 98%;
  margin: 20px 1%;
  font: 20pt black;
  font-weight: bold;
  border-radius: 10px;
}
</style>