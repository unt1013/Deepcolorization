# Deepcolorization

- 모델 다운로드:
    * (1) 해당 프로젝트를 실행시키기 위한 모델을 다운로드 받습니다.
      ```mkdir -p ./checkpoints/siggraph_retrained
         MODEL_FILE=./checkpoints/siggraph_retrained/latest_net_G.pth
         URL=http://colorization.eecs.berkeley.edu/siggraph/models/pytorch.pth
         wget -N $URL -O $MODEL_FILE```
        * `./checkpoints/siggraph_retrained/latest_net_G.pth` 에 맞게 경로를 설정해주세요.
