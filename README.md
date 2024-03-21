<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Animasi CSS</title>
<style>
  @keyframes example {
    0% {background-color: red;}
    50% {background-color: yellow;}
    100% {background-color: blue;}
  }
  
  div {
    width: 100px;
    height: 100px;
    background-color: red;
    position: relative;
    animation: example 5s infinite;
  }
</style>
</head>
<body>
  <div></div>
</body>
</html>
