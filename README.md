# django-practice


﻿
django를 설치하기에 앞서 가상환경을 구축해야 합니다.


windows 10 기준 'ubuntu'라는 WSL을 사용하여 django 설치및 프로젝트를 만들어 보겠습니다.


WSL(Windows Subsystem for Linux)는 윈도우에서 리눅스라는 운영체제를 사용할 수 있게 해주는 프로그램입니다.


먼저 설치하기에 앞서 체크해야 할 부분이 있습니다.



1.'Linux용 Windows 하위 시스템' 체크박스를 체크



윈도우 검색창에 'windows 기능 켜기/끄기' 를 검색하면 위와같이 뜹니다.




'Linux용 Windows 하위 시스템' 체크박스를 체크하고 확인을 눌러줍니다.

이 부분을 진행하지 않으면 wsl을 설치하고 실행해도 사용할 수가 없습니다.



2. Ubuntu 설치

위 단계를 진행했으면 microsoft store에서 'ubuntu'를 검색한 후 설치해 줍니다.

※저는 18.04 버젼을 설치했으니 참고 바랍니다. 각자 맞는 버젼으로 설치해 주세요!





3. Ubuntu 업데이트


이제 한번 ubuntu를 실행해 봅시다.


처음 실행하면 user name 과 user password를 설정해야 합니다.


password는 블라인드 처리 되어있습니다.



이제 설정이 완료되었고 ubuntu의 업데이트를 해주어야 합니다.

해당 코드를 복사해서 붙여넣기 하면 됩니다.



sudo apt-get update
내용을 입력하세요.
그런데 붙여넣기가 되지 않는데요.


창의 젤 윗부분을 우클릭하여 속성에 들어갑니다.




ctrl+shift+c/v를 복사 붙여넣기로 사용 체크박스를 체크해주면

ctrl + c 로 복사하고 ctrl+shift+v로 해당 코드를 ubuntu에 붙여넣을 수 있습니다.


sudo apt-get install -y make build-essential \
 libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev \
 wget curl llvm libncurses5-dev libncursesw5-dev \
 xz-utils tk-dev git python-pip

해당 코드도 동일한 방식으로 붙여넣고 enter를 눌러주면 설치가 진행됩니다.



4. 가상환경 세팅 및 django 설치


pyenv를 사용해서 python 가상환경을 만들어 보겠습니다.



mkdir meohyun-django
cd meohyun-django
code .

해당 코드를 1줄씩 써주세요.


mkdir ~ 은 해당 이름으로 디렉토리를 생성하는 것입니다. 저같은 경우에는 meohyun-django라고 이름을 붙였습니다.

cd 는 해당 상위 디렉토리로 이동하는 코드입니다.

code . 은 해당 디렉토리를 VSC로 실행할 수 있는 코드입니다. 이 코드를 사용해서 프로젝트의 파일을 열수 있습니다.


현재는 프로젝트 및 앱을 만들어 주지 않았기 때문에 아무 파일도 없습니다.


다시 vsc를 끄고 ubuntu도 재실행 해줍니다.




이제 가상환경을 만들어 보겠습니다.


해당 코드를 복사해서 붙여넣기 해주세요.


curl https://pyenv.run | bash
내용을 입력하세요.
설치가 완료되면



사진 삭제
사진 설명을 입력하세요.

export로 시작하는 부분을 찾아

이 3줄의 코드를 복사해줍니다.


cd~ 를 사용해서 다시 홈 디렉토리로 이동해줍니다.

여기서 vsc를 실행하는 코드인 code . 을 입력하고 vsc를 켜줍니다.




파일명 " .bashrc" 를 찾아서 제일 끝 부분에 복사한 3줄의 코드를 붙여넣어 줍니다.



eval "$(pyenv virtualenv-init -)"
내용을 입력하세요.
1줄을 추가로 적어줍니다.

저장해주고 다시 ubuntu를 실행해 봅시다.




pyenv --version
내용을 입력하세요.
ubuntu에 해당 코드를 입력해보면 설치된 pyenv와 그 버젼을 알 수있습니다.


이제 가상환경을 구축할 세팅이 완료되었습니다. 다음 글에서 가상환경 구축과 django를 설치해보겠습니다.




﻿
