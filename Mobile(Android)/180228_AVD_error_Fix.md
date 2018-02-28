# Android Studio AVD 에러 해결

***

* **Ubuntu 17.10** 버전에서 **Android Studio** **AVD** 실행시 에러 24개(제정신?) 발생
  * 보통의 경우 정상적인 방법대로 했음에도 이렇게나 많은 에러가 한꺼번에 발생할 때..
  오히려 문제는 하나일 경우가 있어 검색을 해보았다.
  블로그에도 포스팅 되었던 내용이다.
<br>
* 자세한 내용은 잘 모르겠지만 다음 커맨드를 그대로 터미널에 입력하니 바로 해결 되었다.

>  `sudo apt-get install mesa-utils` 사실 이건 필요한지 모르겠다.
  `cd ~/Android/Sdk/emulator/lib64/libstdc++`
  `mv libstdc++.so.6 libstdc++.so.6.bak`
  `ln -s /usr/lib/x86_64-linux-gnu/libstdc++.so.6 libstdc++.so.6`
  <br>
* ~~사실 다음 세팅때는 여기서 복붙 해갈 요랑으로 작성되었다.~~
