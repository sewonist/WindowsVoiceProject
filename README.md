# WindowsVoiceProject + Unity3D

출처 : https://chadweisshaar.com/blog/2015/07/02/microsoft-speech-for-unity/

본 저장소는 원 출처의 소스와 유니티 예제를 포함합니다.

### Build

![Windows 8.1 SDK](http://sewonist.com/wp-content/uploads/2019/11/Screenshot_51.png)

WindowsVoiceProject 를 빌드하기 위해서는 Windows8.1 SDK 가 설치되어 있어야 합니다.


![Windows 8.1 SDK](http://sewonist.com/wp-content/uploads/2019/11/Screenshot_52.png)

이미 윈도우에 설치된 음성만 사용 가능합니다. 음성을 선택하기 위해서는 dllmain.cpp 에서 아래 부분의 소스를 수정해야 합니다.

```void speechThreadFunc()
  {
    ISpVoice * pVoice = NULL;

    ... 중략 ...

	if (SUCCEEDED(hr))
	{
		hr = cpEnum->Item(3, &cpVoiceToken); // 원하는 음성의 인덱스를 선택 
	}
 ```

### Demo
[![Demo](https://img.youtube.com/vi/lWRVBhOZ_8c/0.jpg)](https://www.youtube.com/watch?v=lWRVBhOZ_8c)

