# Deepcolorization

- 모델 다운로드:
    * 해당 프로젝트를 실행시키기 위한 모델을 다운로드 받습니다.
    ```
    mkdir -p ./checkpoints/siggraph_retrained
    MODEL_FILE=./checkpoints/siggraph_retrained/latest_net_G.pth
    URL=http://colorization.eecs.berkeley.edu/siggraph/models/pytorch.pth
    wget -N $URL -O $MODEL_FILE
    ```
    * ./checkpoints/siggraph_retrained/latest_net_G.pth 에 맞게 경로를 설정해주세요.
    
- 프로젝트 실행:
    ``` python manage.py runserver ```
    를 입력해 실행합니다.

- 해당 이미지와 같이 256x256 크기의 이미지를 input data로 넣습니다. 
![00000000_0p031_fake_reg](https://user-images.githubusercontent.com/29967386/84729296-53aa1280-afce-11ea-818a-028d35ea793b.png)

