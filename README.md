# begin_and_end_of_work_bot
백호부대에 입대한 친구들을 위한, 병무청 제출용, 출퇴근 기록 파일 생성 슬랙봇

## 개요
1. 매일 AM 8:30 이후 슬랙에 온라인된 순간 해당 멤버한테 `출근하셨나요?` 라고 물어보며 `Yes`와 `No`의 선택지를 줌.
    1. `No` 라고 답하면, 오프라인 후 재온라인된 순간 1을 반복.
    2. `Yes`라고 답하면, 해당 시간을 출근시간으로 보고, 구글 스프레드시트에 기록.
2. 퇴근할 때 멤버가 봇에게 `Bye` 라고 DM을 보냄.  
3. 봇이 즉시 \#general에 `우리의 (수식어 랜덤) 멤버(Display Name)가 (YY-MM-DD HH:MM)에 가방을 싸고 있습니다! (수고 메시지 랜덤)`  메세지를 남김.
4. 주간 또는 월간 출퇴근 시간이 기록된 구글 스프레드시트를 \#general에 공유해 줌.

## 이슈
* 슬랙 온라인/오프라인 순간 캐치 방법
* 출근시간 체크
	* 멤버한테 물어보고 체크하기 때문에 부정확할 수 있음
		* 멤버들의 양심에 맡길 수 밖에 없음

## 구현
* 언어: Python
	1. 기존에 도훈이가 작업한 슬랙봇의 언어가 Python임.
	2. Python을 이 기회에 처음 사용해보고 싶음.
