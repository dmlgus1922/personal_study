* nvidia, cuda 설치 진행 중 버전 이슈 때문인지 컴퓨터 부팅이 되지 않는 현상이 발생했다. 다른 프로그램 설치 후 위와 같은 현상이 나타나 disk를 다 밀어야 했다. 시간 절약을 위해 nvidia, cuda 설치를 먼저 하는 것을 권고한다.

### nvidia 설치

1. 그래픽카드 정보, 드라이버 확인하기
	- $ ubuntu-drivers devices
		그래픽카드 및 설치 가능한 드라이버 확인 (권장 드라이버가 보임)
	- $ lshw –numeric –C display
	  $ lspci | grep –i nvidia
		현재 사용 중인 그래픽카드 확인

2. 드라이버 설치
	- $ sudo ubuntu-drivers autoinstall
		권장 드라이버 자동 설치
	- $ sudo apt install nvidia-driver-xxx
		원하는 버전 수동 설치
	- 설치 후 재부팅 (sudo reboot)

3. cuda 설치
	- 다른 블로그 등을 참고할 필요 없이 nvidia developer 사이트로 가서 cuda toolkit을 다운로드 한다.
	- 기기 운영체제, 사양 등에 맞춰 install 하면 된다.





	* cuda toolkit을 설치하면 nvidia driver가 저절로 설치되는 것 같다.
	* cuda toolkit을 먼저 설치하고 $ nividia-smi 확인해 nvidia driver가 없다면 그때 사양에 맞는 driver를 설치하는 것이 올바른 순서인 듯하다.

