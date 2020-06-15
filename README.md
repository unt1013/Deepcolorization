# Deepcolorization

download the pretrained model by running bash pretrained_models/download_siggraph_model.sh, which will give you a few models.
Original caffe weights [Recommended] ./checkpoints/siggraph_caffemodel/latest_net_G.pth is the original caffemodel weights, converted to PyTorch. It is recommended. Be sure to set --mask_cent 0 when running it.
Retrained model: ./checkpoints/siggraph_retrained/latest_net_G.pth. The model achieves better PSNR but performs qualitatively differently. Note that this repository is an approximate reimplementation of the siggraph paper.
