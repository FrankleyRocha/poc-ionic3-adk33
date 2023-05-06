# POC IONIC 3 COM ADK 33

Este é um exemplo de uma aplicação utilizando ionic 3 pronta para compilação com base no android 13 ou ADK 33.

## Configuração de compilação
```
 <platform name="android">
    ...
    <preference name="android-minSdkVersion" value="19" />
    <preference name="android-compileSdkVersion" value="33" />
    <preference name="android-targetSdkVersion" value="33" />
    ...
 </platform>
```

## Declaração exigida a partir do android ADK 31
```
<platform name="android">
    ...
    <edit-config file="AndroidManifest.xml" mode="merge" target="/manifest/application/activity[@android:name='MainActivity']" xmlns:android="http://schemas.android.com/apk/res/android">
        <activity android:exported="true" />
    </edit-config>
    ...
</platform>
```