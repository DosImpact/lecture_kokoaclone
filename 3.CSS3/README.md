# CSS 정리하기

## Box Model

1. 항상 높이랑 너비를 신경써야 된다. 높이를 충분히 안주어서 정렬이 안되는 경우도 있다.

2. box모델의 크기와 너비는 margin과 padding값을 더 줬다면 크기가 더 커진다. border도 포함!!  
   따라서 두 박스모델을 나란히 세우려면 박스모델의 전체적인 크기를 봐야된다.

3. inline-block과 width를 %로 주었을때는 div 요소들이 서로 한줄에 있지 않는다.  
   이럴때는 width를 고정값으로 주어야 된다. %값으로 주는건 한줄을 차지한 상태에서 몇 %를 가져가는지 문제인듯!