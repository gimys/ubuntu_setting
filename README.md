# 우분투 세팅 기록  

## 1. 키보드 설정
(1) 한글 입력기 설치
참고 사이트 : https://driz2le.tistory.com/253  

(2) 오른쪽 alt를 오직 한/영으로만 쓰기(설정 안하면 alt랑 섞여 쓰여짐)  
설치 참고 사이트 : https://geundung.dev/89  
설정 : keyboard&mouse -> additional layout options -> Right Alt as Hangul, right Ctrl as Hanja만 체크  

## 2. 트랙패드 설정
(1) 트랙 패드 입력 프로그램 설치  
설치 참고 사이트 : https://conservative-vector.tistory.com/entry/Ubuntu-%ED%84%B0%EC%B9%98%ED%8C%A8%EB%93%9C%EB%A5%BC-%ED%8E%B8%ED%95%98%EA%B2%8C-Fusuma  
설정 :
config.yml을 아래와 같이 설정하면
3손가락 좌우 스와이프로 크롬 창 앞뒤
4손가락 상하로 모든 프로그램 보기, 좌우로 프로그램 이동
2손가락 모으기/벌리기로 창 축소/확대

swipe:  
  3:  
    left:  
      command: 'xdotool key alt+Right'  
    right:  
      command: 'xdotool key alt+Left'  
  4:  
    left:  
      command: 'xdotool key alt+Tab'  
    right:  
      command: 'xdotool key Super+Shift+Tab'  
    up:  
      command: 'xdotool key super'  
    down:   
      command: 'xdotool key super'  
pinch:  
  2:   
    in:  
      command: 'xdotool key ctrl+plus'  
      threshold: 0.1  
    out:  
      command: 'xdotool key ctrl+minus'  
      threshold: 0.1  
  
threshold:  
  swipe: 1  
  pinch: 1  
   
interval:  
  swipe: 1  
  pinch: 1  


(2) 위 프로그램이 안되면 이걸로 설치(한성 TFX245는 이걸로 설치)  
설치 참고 사이트 : https://medium.com/@jjeaby/mac-%EC%B2%98%EB%9F%BC-linux-touchpad-gesture-%EC%82%AC%EC%9A%A9-1d018e235249 
config는 아래와 같이 하기


gesture swipe up    4    xdotool key super  
gesture swipe down  4    xdotool key super  
gesture swipe left  4    xdotool key alt+tab  
gesture swipe right 4    xdotool key ctrl+super+tab  
  
gesture swipe left  3    xdotool key alt+Right  
gesture swipe right 3    xdotool key alt+Left  
  
gesture pinch   in    2  xdotool key ctrl+minus  
gesture pinch   out   2  xdotool key ctrl+plus  
