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

![2211.PNG](JavaScript%E1%84%85%E1%85%B3%E1%86%AF%20%E1%84%8B%E1%85%B5%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%92%E1%85%A1%E1%86%AB%20%E1%84%8B%E1%85%A7%E1%86%BC%E1%84%89%E1%85%A1%E1%86%BC%20%E1%84%8B%E1%85%B5%E1%86%B0%E1%84%80%E1%85%B5%20d8ab777118f84fd895bc791d9f67df58/2211.png)

![2121](https://user-images.githubusercontent.com/86837707/203014759-3c689300-1700-4940-a586-59c481391168.png)

위 확장을 이용하여 서버를 구동시켜준다.

## 결과

---

![img1122.JPG](JavaScript%E1%84%85%E1%85%B3%E1%86%AF%20%E1%84%8B%E1%85%B5%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%92%E1%85%A1%E1%86%AB%20%E1%84%8B%E1%85%A7%E1%86%BC%E1%84%89%E1%85%A1%E1%86%BC%20%E1%84%8B%E1%85%B5%E1%86%B0%E1%84%80%E1%85%B5%20d8ab777118f84fd895bc791d9f67df58/img1122.jpg)

정상적으로 작동되는 것을 확인할 수 있다.
