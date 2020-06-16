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

# FilterRemover

- 필터가 씌워진 사진을 첨부합니다.

![unnamed](https://user-images.githubusercontent.com/29967386/84734705-983caa80-afdc-11ea-9138-47e4faa16745.jpg)
![unnamed (2)](https://user-images.githubusercontent.com/29967386/84734715-9d99f500-afdc-11ea-8da3-5393b4c62f45.jpg)
![unnamed (3)](https://user-images.githubusercontent.com/29967386/84734724-a1c61280-afdc-11ea-8a00-be5942ca0be4.jpg)

- 위 이미지들과 같이 필터가 씌워진 사진을 삽입하면, 필터가 제거된 이미지가 출력됩니다.

![00000000_0p031_real](https://user-images.githubusercontent.com/29967386/84729526-df23a380-afce-11ea-8093-42a74fd5528b.png)

# Colorization

- 해당 이미지와 같이 256x256 크기(권장)의 이미지를 input data로 넣습니다. (256x256 크기가 아니어도 되지만 resize 과정에서 픽셀이 깨지는 현상이 발생합니다)

![00000000_0p031_real](https://user-images.githubusercontent.com/29967386/84729526-df23a380-afce-11ea-8093-42a74fd5528b.png)

- 해당 이미지에서 특정 부분의 색상값을 가져와 해당 픽셀부분에 적용시킵니다.

![00000000_0p031_hint_ab](https://user-images.githubusercontent.com/29967386/84729446-af749b80-afce-11ea-9541-126a7bfbfa8b.png)
![00000000_0p031_fake_reg](https://user-images.githubusercontent.com/29967386/84729470-be5b4e00-afce-11ea-8fae-bd77dd6de507.png)

- 이 기술을 토대로, 사용자는 특정 부분에 원하는 색상값을 주입시킬 수 있습니다. 이를 통해 해당 부분에 새로운 색깔을 추가하는 것이 가능합니다

![00000001_0p031_hint_ab](https://user-images.githubusercontent.com/29967386/84729585-0ed2ab80-afcf-11ea-8586-ddcd71f8beb0.png)
![00000001_0p031_fake_reg](https://user-images.githubusercontent.com/29967386/84729588-109c6f00-afcf-11ea-9a0b-186112dd2484.png)
