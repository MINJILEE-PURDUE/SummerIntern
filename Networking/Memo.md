## Router/Switch different type 4 mode

Switch>


유저모드는 '>표시가 나오는 상태로 스위치 상태 보기만 가능하고 주로 ping test 하기 위해 사용된다.
enable 명령어를 사용해 Privileged Mode로 들어갈 수 있다.


Privileged Mode

Switch>enable
Switch#
프리빌리지 모드는 관리자 모드라고도 불리며 '#'표시가 붙여지며 주로 show 명령어를 통해 장비의 구성 및 상태를 확인할 때 사용된다.
configure terminal 명령어를 사용하여 Global Mode로 들어갈 수 있다.

Global Mode
Switch#configure terminal
Switch(config)#
'(config)' 표시가 붙으며 이 부분에서 호스트설정 및 IP설정 등 대부분의 작업이 처리된다.
interface 명령어를 사용하여 해당 인터페이스 모드로 들어갈 수 있다.

Interface Mode
Switch(config)#interface
Switch(config-if)#
(config)에 if가 추가된 (config-if)를 표시하며 해당 인터페이스의 상세 설정을 위해 사용된다.
해당 인터페이스의 IP나 Subnet 값을 설정할 수 있다. 

CLI: https://www.cisco.com/c/en/us/td/docs/switches/datacenter/nexus1000/sw/4_2_1_s_v_2_2_1/layer2/b_Cisco_Nexus_1000V_Layer_2_Switching_Configuration_Guide_Release_4_2_1_SV_2_2_1/b_Cisco_Nexus_1000V_Layer_2_Switching_Configuration_Guide_Release_4_2_1_SV_2_2_1_chapter_011.html#concept_213B0ADDE7204425A199BD9FB3A2528D

Mac Address Table Explanation (Static and Dynamic)
https://facelight.tistory.com/23
