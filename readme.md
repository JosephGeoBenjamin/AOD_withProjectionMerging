
# Aerial Object Detection with Attention Projection Merging and Attention-enhanced Convolutions

![Method](https://github.com/JosephGeoBenjamin/rise-of-the-puppies/releases/download/Docs-1.0/MBZ-CV703_image.png)


## Work:
[Technical Report](https://docs.google.com/viewer?url=https://github.com/JosephGeoBenjamin/rise-of-the-puppies/releases/download/Docs-1.0/CV703_Project_FinalReport.pdf)


In this paper, inspired by Token Merging for image classification, we propose two novel test time mechanisms for reducing the computational cost of transformer-based object detection pipelines. The first mechanism is called token merging, which is a naive application of Token Merging for detection. We applied token merging to the DETR architecture, which involves merging similar tokens in the encoder to reduce the number of attention computations required on both the encoder and decoder sides. Our second novel mechanism, called attention projection merging, is applied to the VitDet architecture and involves merging the key and value projections independently to reduce the attention computation cost. Both mechanisms significantly reduce the number of computations required while still achieving competitive average precision results (only around 3% AP reduction while reducing half of the computation from transformer blocks) on object detection benchmarks. The proposed Attention Projection Merging (APM) also supports the 2D formation of attention in the self-attention block. The experimental results demonstrate that our proposed mechanisms can effectively reduce computational costs without sacrificing performance. Further to the computation cost reduction, we explore the AP performance with backbones and found LSK net provides better AP in faster RCNN architecture. We showed extensive experimentation and ablation on the iSAID dataset.


## Installations

Optional Not entirely needed
`python -m pip install -e Detectron2-modif`

## Acknowledgement
Completed as part of Project work for CV703 Course at MBZUAI. The codebase is based on the [Detectron](https://github.com/facebookresearch/detectron2) with modifications to include [Token Merging](https://github.com/facebookresearch/ToMe)
