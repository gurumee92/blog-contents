---
title: Practical VIM 4일차 (팁 10-12)
tags:
  - vim
  - tip
  - begginer
---
## TIP 10. 간단한 산술에 실행 횟수 사용하기
* `{숫자}<C-a>`: 텍스트 숫자를 `{숫자}`만큼 증가
* `{숫자}<C-x>`: 텍스트 숫자를 `{숫자}`만큼 감소
* `cW`: 현재 커서에 있는 단어 제거 후 편집 모드

## TIP 11. 직접 반복할 수 있다면 실행 횟수 사용하지 않기
2단어를 지우는 명령어 중 어느 것이 더 좋을까?
* `d2w`
* `2dw`
* `dw.`

정답은 `dw.`. 반복할 수 있는 단위로 쪼개는 것이 좋다.

## TIP 12. 분할 정복

| 트리거 | 효과                           |
| :-: | ---------------------------- |
|  c  | 변경                           |
|  d  | 삭제                           |
|  y  | 레지스터로 복사                     |
| g~  | 대소문자 변환                      |
| gu  | 소문자 변환                       |
| gU  | 대문자 변환                       |
|  >  | 우측으로 탭 이동                    |
|  <  | 좌측으로 탭 이동                    |
|  =  | 자동으로 들여쓰기                    |
|  !  | {모션}에 해당하는 행 외부 프로그램 사용해 필터링 |
