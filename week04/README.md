
# 자동화와 협업
## 디렉터리

	절대 경로 /home/neary/devops/week03/qwen-web/start.sh
	상대 경로 ./week03/qwen-web/start.sh (단, 현재 위치가 ~/devops 일 때)
		또는 week03/qwen-web/start.sh
	현재 위치 .
	상위 위치 ..
	홈 ~
	루트 /

## grep, find, 파이프

```shell
find . -type f -name "*.sh" # sh(셸 스크립트) 파일 찾기
grep -R -n "exit 1" week03 2>/dev/null # exit 1 포함하는 파일 찾기
grep -R -n "exit 1" week03 2>/dev/null | wc -l # exit 1 포함 파일 개수
# 파이프(|)를 통해 앞 명령의 표준 출력을 뒤 명령 표준 입력으로 전달한다
```

## 프로그램/프로세스

- 프로그램
	- 디스크에 저장된 코드
- 프로세스
	- 메모리에 올라간, 즉 실행중인 프로그램
	- 프로세스 고유 식별을 위한 PID가 존재

## Git/Github

- .gitignore로 관리에서 제외할 결과물 선정
- Branch -> Commit/Push -> Pull Request -> Merge

---

# 네트워크
## IP

- 네트워크 장치 식별을 위한 고유 주소

## 포트

- 장치에서 제공하는 서비스를 구분하는 번호

## DNS

- 도메인 이름에 대응하는 IP 주소를 찾는 서비스
