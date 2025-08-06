## fastfetch config
#### WIN
![screenshot](https://i.imgur.com/99o0mx6.png)
#### MAC
![screenshot](https://i.imgur.com/CEygkEi.png)
개요
---

이 저장소는 저의 Fastfetch 설정을 여러 기기에서 쉽게 동기화하고 변경 사항을 추적하기 위해 만들어졌습니다. 


사용 방법
---
먼저 이글의 모든 작업은 [fastfetch 공식문서](https://github.com/fastfetch-cli/fastfetch)를 기반으로 했습니다. 자세한 사항을 알고 싶다면 참고하길 바랍니다.

윈도우 환경의 경우 `winget`으로 `fastfetch`를 설치 받을 수 있지만 로고 이미지 출력에 제약사항이 있다고 판단했고 MSYS2를 통해 `fastfetch`를 설치하기로 결정했습니다. MSYS2가 설치되어 있다면
[MSYS2 Packages](https://packages.msys2.org/packages/mingw-w64-ucrt-x86_64-fastfetch)를 통해 `fastfetch`를 내려 받을 수 있습니다.

아래 명령어를 통해 특정경로가 출력되며 이 repo를 그 경로에 클론하면 바로 적용할 수 있습니다.    

```
fastfetch --gen-config
```
#### WIN
MSYS2에 [magick](https://packages.msys2.org/packages/mingw-w64-x86_64-imagemagick)이 설치되어 있다면 이미지파일을 sixel 변환 작업없이 로고설정이 가능합니다. 로고의 원본 경로는 절대 경로만 사용할 수 있습니다. 다만 윈도우의 경우 환경변수가 지원되므로 `fastfetch --gen-config` 에서 출력된 경로를 `%fastfatch%`로 등록했습니다.


Windows Terminal에서[투명한 배경이 적용 되는 않는 문제](https://github.com/fastfetch-cli/fastfetch/issues/656#issuecomment-1849448969)를 참고해 시도해 보아도 여전히 투명색이 정상적으로 출력되지 않는 문제점이 있습니다.


![screen](https://i.imgur.com/MgtMc4t.png)
chafa로 배경을 지운 sixel 파일을 windows terminal pwsh에 출력해보면 정상적으로 나오는 모습을 볼 수 있지만 `config.jsonc`내 logo 설정에 어떤 타입을 시도해보아도 깨진 이미지로 출력이 됩니다. 

![screen](https://i.imgur.com/9DwXu2O.png)
주어진 환경 내에서 이 문제를 해결할 방법은 없는것 같습니다. `Wezterm`을 이용하거나 다른 `fetcher`설치하길 바랍니다.  