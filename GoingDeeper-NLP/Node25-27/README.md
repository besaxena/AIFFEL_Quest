Aiffel에서 진행한 GoingDeeper 노드관련 코드들입니다!

----

루브릭
1. 기존 데이터셋을 추가 정제하고, generation 성능을 끌어올리기 위한 기법들을 실험해 모델 perfomance를 향상시켜보았는가?	
- 기존 데이터셋의 문제점을 분석하고 전처리 전략을 수립해 추가 정제를 진행했다. Beam search, Top-k(p) sampling 등 최선의 디코딩 전략을 수립해 향상된 모델 추론 결과를 제시했다. BLEU, ROUGE 등 생성된 텍스트를 평가하기 위한 메트릭을 적용한 정량적인 평가 결과와 주관적인 평가를 비교분석하였다.

2. 새로운 데이터를 수집해 전처리를 수행하여 모델을 재학습시켜보았는가?

- 모두의 말뭉치, AI hub 등에 공개된 데이터를 사용해 추가 데이터셋을 구축하기 위한 기준과 근거를 수립했다. ChatGPT API나 다양한 한국어 benchmark 데이터셋을 활용해 Human Feedback 을 대체할 수 있는 아이디어를 구현했다. 위를 바탕으로 SFT, RM, PPO 세 단계에 필요한 각 데이터셋을 적절히 구축하여, 모델 추론 결과와 수립한 가설을 비교해보았다.


3. 학습 전략 또는 foundation model을 변경해 모델을 재학습시켜보았는가?	
- 더 적절한 Instruction Tuning 기법을 적용해 SFT를 해보거나, Reward Model의 ranking algorithm을 개선해보았다. KoGPT-2가 아닌 다른 모델을 initial model로 사용하여 모델 학습을 성공시켰다. 허깅페이스의 accelerate, bitsandbytes 라이브러리 등을 사용하여 더 큰 스케일의 모델로 ChatGPT를 re-building해 모델 성능을 향상시켰다 

----


코더 : 김지원    

리뷰어 : 박태하

🔑 **PRT(Peer Review Template)**

- [ ]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
![image](https://github.com/besaxena/AIFFEL_Quest/assets/110083249/f57c2c30-4a77-4f5a-8262-5a8671015e43)
![image](https://github.com/besaxena/AIFFEL_Quest/assets/110083249/850fda8d-d8e6-4877-bfe2-0d4c7f02c9f1)
![image](https://github.com/besaxena/AIFFEL_Quest/assets/110083249/0e5c78df-8c68-4118-bf0a-4a566a58adbf)


    
- [ ]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**

        
- [ ]  **3. 에러가 난 부분을 디버깅하여 문제를 “해결한 기록을 남겼거나” 
”새로운 시도 또는 추가 실험을 수행”해봤나요?**
이번노드는 디버깅을 할만한 부분이 크게 없었다.
        
- [ ]  **4. 회고를 잘 작성했나요?**
![image](https://github.com/besaxena/AIFFEL_Quest/assets/110083249/e17f3886-3b63-44e0-88e1-fcf5b8216d61)


- [ ]  **5. 코드가 간결하고 효율적인가요?**
![image](https://github.com/besaxena/AIFFEL_Quest/assets/110083249/f37e78be-2712-40ec-b135-54c468ff449c)


Reference:

