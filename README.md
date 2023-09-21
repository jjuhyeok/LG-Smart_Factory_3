# LG-AI_Radar [(Link)](https://dacon.io/competitions/official/236080/leaderboard)

## 🏆 Result
# **Public score 1st** 0.77428 | **Private score 5th** 0.69342

주최 : ```LG AI Research + LG Display```

규모 : 총 1800여명 참가

  

  
## 🧐 About
실제 스마트 공장 데이터를 기반으로 제품의 품질 상태를 분류하는   
AI 모델을 개발하여 **품질 편차를 최소화**해 생산 **경제성과 안정성**을 확보하기 위한 대회   
  
  
  
  

## 🔥**대회 느낀점**
미련을 가지면 안되지만, LG AI Research 대회를 진행할 때마다 미련이 정말 남는다.  
저번 LG 1기 대회때는 public, private 리더보드 모두 1등을 차지하고 코드 검증까지 다 통과를 하고 2차 평가 발표까지 진행하였지만,  
최종 발표 하루 전날 갑작스럽게 실격 통보를 받아서, 정말 며칠간은 정신적으로 힘들었었다.  
```하지만 꼭 다음 LG AI Research 주최 대회는 1등을 하겠다는 다짐을 계속```해서 하였다.  

6개월이 지난 후, LG AI Research사가 주최한 새로운 대회가 시작되었다.    
온라인 예선을 무난하게 통과한 후 수상자를 결정짓는 오프라인 대회가 1박 2일간 진행되었다.    
오프라인 해커톤은 초반부터 상위권에 있다가, 기존의 방법론에서 벗어나 새로운 데이터 구조로 접근하였다.  
그 결과 public 리더보드 1등을 기록하였고, 모두가 자러간 새벽~아침7시까지 하였을 때, 2위와 차이를 점점 더 벌려 나갔었다.  

그리고 대회가 끝나기 1시간 전, 지금까지 학습했던 모델들로 voting ensemble을 하였다.  
voting ensemble을 좀 특별하게, 최소한 한 개의 모델이 클래스 불균형이 존재하는 0과 2의 (불량)class에 대해 예측을 한다면  
그 sample은 불량으로 처리를 해 주었다.  

그러자 public 점수가 정말 말도안되게 높아졌다. 2등과는 차이가 엄청 심한 압도적인 1등이었다.  
voting 후 F1 Score는 0.77428을 기록했고 2등부터 7등까지는 0.7545 ~ 0.75 8등부터 20등까지는 0.74 ~ 0.71 의 F1 score를 기록하였다.  

해커톤 대회가 종료되기 전 최종 채점받을 오직 "1"개의 csv를 제출해야 했었는데,  
이때 정말 고민을 많이 하였다.  
0.77428의 1등 score를 기록한 csv를 제출하는게 맞아 보였다.  
하지만 온라인 예선때의 기억이 스쳐 지나갔다.  
온라인 예선때도 public 3위라는 높은 등수를 가졌었고,    
1등,2등,3등 public 점수를 가진 팀들이 4등 ~ 상위권 팀들보다 압도적으로 F1 score가 높았다.    
하지만 private score 채점을 들어가자, 1등,2등,3등 팀들 모두 등수가 폭락하였다.    
overfitting이었다.  
2등분은 온라인 예선 통과조차 할 수 없었고, 1등 분은 거의 턱걸이로 오프라인 예선에 참여할 수 있었고,  
3등인 우리는 그나마 안정적으로 참여할 수 있었다.  

맞다, 이때의 기억이 떠올랐다. 현재 압도적인 1등 점수에 신뢰가 가지 않았다.  
나는 이러한 걱정을 말해주었고 팀원들은 압도적인 이 점수의 csv를 최종 제출을 해야한다, 하지말아야 한다로 분열되었고  
팀장인 나는 결정을 해야 했다.  

정말 그 짧은 몇십분의 시간동안, 정말로 별에 별 생각이 다 들었다.  
만약 내가 잘못 결정을 해서 우리 팀이 2차 평가에 진출을 하지 못하면 어떻게하지? 부터 시작해서.. 정말 힘들었다.    

나는 결정을 내렸다.  
1등이 아닌, 2등~최상위권 팀들과 비슷한 점수의 csv를 제출하기로..  

private 채점 결과 5등이 되었다.   
1등부터 5등까지 2차평가 진출 대상자여서 2차 평가에 진출을 할 수 있었다.   

하지만 문제가 있었다.  
예측 성능에 너무 시간을 쏟다 보니, 2차 평가를 위한 ppt 제작 시간이 존재하지 않았다.  
다른 팀들은 온라인 예선때 쓴 ppt를 수정만 해서 사용한 것 같았는데,  
우리 팀은 1박 2일이라는 그 짧은 시간동안 데이터 구조 변경, 새로운 기법 등등 온라인 예선과는 완전히 다른 ppt 자료가 필요했고  
주어진 2시간이라는 ppt 제작 시간동안 각자 목차를 나누어 ppt를 새로 작성하였다.  
심지어 발표도 1순위여서 완성된 ppt를 제대로 봐 볼 시간도 부족했다.  
그냥 완성 후 리허설도 없이 바로 발표였다.   

팀장으로서 팀원분들께 미안한 마음이 크다.   
압도적 1등 모델이 아닌, 점수가 더 낮은 강건한 모델을 최종 제출하자고 했던 결정이 잘못되었던 결정인지,   
성능 욕심에 7시까지 혼자서 성능 조금이라도 더 올려보겠다고  
비록 성능은 올랐지만 Phase 2에서 하던 아키텍처와 다른 아키텍처를 설계해서  
다른 팀처럼 Phase2에서 사용하던 ppt 기반이 아닌, 2시간이라는 짧은 시간에 새롭게 ppt를 만들게 되어서  
완벽하지 못한 결과 ppt를 만들게 되었던 과정이 잘못되었는지.  
나의 결정들이 잘못된 게 아닐까 후회만 남고 믿고 따라와 준 팀원분들에게 미안하고  
지금 이 글을 작성하는 이 순간에도 1등 csv를 최종 제출 했으면 결과는 달라졌을까 라는 생각에 아직도 괴롭긴하다.  

더 자세한 인터뷰는    
https://dacon.io/ranking/interview/259  
... 
