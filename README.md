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

# Colorization

- 해당 이미지와 같이 256x256 크기(권장)의 이미지를 input data로 넣습니다. (256x256 크기가 아니어도 되지만 resize 과정에서 픽셀이 깨지는 현상이 발생합니다)

![00000000_0p031_real](https://user-images.githubusercontent.com/29967386/84729526-df23a380-afce-11ea-8093-42a74fd5528b.png)

- 해당 이미지에서 특정 부분의 색상값을 가져와 해당 픽셀부분에 적용시킵니다.

![00000000_0p031_hint_ab](https://user-images.githubusercontent.com/29967386/84729446-af749b80-afce-11ea-9541-126a7bfbfa8b.png)
![00000000_0p031_fake_reg](https://user-images.githubusercontent.com/29967386/84729470-be5b4e00-afce-11ea-8fae-bd77dd6de507.png)
