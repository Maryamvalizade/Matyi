# Matyi<!DOCTYPE html>
<html lang="fa">
<head>
<meta charset="UTF-8">
<title>بزرگنمایی تصویر</title>
<style>
body {
  font-family: sans-serif;
  text-align: center;
  background: #111;
  color: white;
}
img {
  width: 200px;
  cursor: pointer;
  transition: 0.3s;
}
#overlay {
  display: none;
  position: fixed;
  top: 0; left: 0;
  width: 100%; height: 100%;
  background: rgba(0,0,0,0.8);
  justify-content: center;
  align-items: center;
}
#overlay img {
  width: 80%;
  max-width: 500px;
}
</style>
</head>
<body>

<h2>نمونه بزرگ‌نمایی تصویر</h2>

<img src="image.jpg" id="small" alt="عکس کوچک">

<div id="overlay">
  <img src="image.jpg" id="large" alt="عکس بزرگ">
</div>

<script>
const small = document.getElementById('small');
const overlay = document.getElementById('overlay');
overlay.addEventListener('click', () => overlay.style.display = 'none');
small.addEventListener('click', () => overlay.style.display = 'flex');
</script>

</body>
</html>