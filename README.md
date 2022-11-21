# JavaScript를 이용한 영상 읽기

## 코드 작성

---

```jsx
<html>
    <script defer src="rfile.js"></script>
    <input type='file' accept='image/*' onchange='openFile(event)'><br>
    <img id='imageUpload'>
<html>
```

위 코드를 메모장을 활용하여 파일명을 index.html로 생성한다.

```jsx
var openFile = function(file) {
  var input = file.target;
  var reader = new FileReader();
  reader.onload = function(){
    var dataURL = reader.result;
    var imageUpload = document.getElementById('imageUpload');
    imageUpload.src = dataURL;
  };
  reader.readAsDataURL(input.files[0]);
};
```

위 코드를 메모장을 활용하여 파일명을 rfile.js로 생성한다.

## 서버 구동

---

![2211](https://user-images.githubusercontent.com/86837707/203015129-3347f0b8-da74-4e0c-991e-5432100fb8fe.png)

![2121](https://user-images.githubusercontent.com/86837707/203014759-3c689300-1700-4940-a586-59c481391168.png)

위 확장을 이용하여 서버를 구동시켜준다.

## 결과

---

![img1122](https://user-images.githubusercontent.com/86837707/203015598-a601ee0d-4738-4f5c-a684-88feb1d2c5ab.JPG)


정상적으로 작동되는 것을 확인할 수 있다.
