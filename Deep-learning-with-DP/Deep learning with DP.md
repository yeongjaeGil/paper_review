Deep Learning with Differential Privacy
---
- Recent Talk
    - 코딩 테스트 준비
    - ML 이론 공부
    - 기술 스펙 쌓기
    - 논문 읽기
    


---
- Lots:
    - we call such a group a lot, to distinguish from the computational grouping that is commonly called a batch, then group several batches into a lot for adding noise.
- Privacy accounting
    - For DP-SGD, an immporttant issue is computing the overall privacy cost of the training.
    - The composability of differential privacy allows us to implement an "accountant" procedure that computes the privacy cost at each access to the training data, and accumulates this cost as the training progresses. 
    - Each step of traininig typically require gradients at **multiple layers**, and the accountant accumulates the cost that corresponds to all of them.
---
- Moments accountant
    - For the Gaussian noise that we use, if we choose $\sigma$ in Algirithm 1 to be $\sqrt{2log\frac{1.25}{\delta}}/\epsilon$, then by standard arguments each step is $(\epsilon,\delta)- DP$ with respect to the lot.
    - Lot itself is a random sample from the database, the privacy amplification theorem implies that each step is $(O(q\epsilon),q\delta))-DP$ respect to the full database where q = L/N is the sampling ratio per lot and $\epsilon <=1$.
    - 
    
---
- 3.3 Hyperparameter Tunning
    - hyperparameters that we can tune in order to balance privacy, accuracy and performance.
    - model accuracy is more sensitive to training parameters such as batch size and nose level than to the structure of a neural network.
    - 
    
    
---
- Distributed Deep Learning under Differential Privacy with the Teacher-Student Paradigm
-