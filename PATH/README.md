<div align="center">
<h1>HumanBench: <br>Towards General Human-centric Perception with Projector Assisted Pretraining</h1>

Shixiang Tang<sup>1,4*</sup>, Cheng Chen<sup>4*</sup>, Qingsong Xie<sup>4</sup>, Meilin Chen<sup>2,4</sup>, Yizhou Wang<sup>2,4</sup>, Yuanzheng Ci<sup>1</sup>, Lei Bai<sup>3</sup>, Feng Zhu<sup>4</sup>, Haiyang Yang<sup>4</sup>, Li Yi<sup>4</sup>, Rui Zhao<sup>4,5</sup>, Wanli Ouyang<sup>3</sup>

<sup>1</sup>The University of Sydney; <sup>2</sup>Zhejiang University; <sup>3</sup>Shanghai Artifical Laboratory; <sup>4</sup>SenseTime Research; <sup>5</sup>Qing Yuan Research Institute, Shanghai Jiao Tong University; 

CVPR 2023


<br>
  
<image src="asset/teaser.png" width="1280px" />
<br>

</div>

<br>

Human-centric perceptions include a variety of vision tasks, which have widespread industrial applications, including surveillance, autonomous driving, and the metaverse. It is desirable to have a general pretrain model for versatile human-centric downstream tasks. This paper forges ahead along this path from the aspects of both benchmark and pretraining methods. Specifically, we propose a HumanBench based on existing datasets to comprehensively evaluate on the common ground the generalization abilities of different pretraining methods on 19 datasets from 6 diverse downstream tasks, including person ReID, pose estimation, human parsing, pedestrian attribute recognition, pedestrian detection, and crowd counting. To learn both coarse-grained and fine-grained knowledge in human bodies, we further propose a Projector AssisTed Hierarchical pretraining method (PATH) to learn diverse knowledge at different granularity levels. Comprehensive evaluations on HumanBench show that our PATH achieves new state-of-the-art results on 17 downstream datasets and on-par results on the other 2 datasets. 


[[Paper]](https://arxiv.org/abs/2303.05675)

## Hightlights

### $\text{\color{#2F6EBA}{A\ Large-scale\ and\ Diverse\ Human-Centric\ Benchmark}}$ 

- collected 11,019,187 pretraining images from 39 datasets among 5 tasks from global to local tasks.
- constructed 19 evaluation datasets from 6 tasks.
- 3 evaluation protocols to assess the generalization ability of pretrained models: in-datasets evaluation, out-of-datasets evaluation, unseen-tasks evaluation.

### $\text{\color{#2F6EBA}{A\ Projector\ Assisted\ Pretraining\ Method}}$ 

- Designed a Task-specific MLP Projector to Enhance Generalization Ability of Supervised Pretraining.
- Designed Hierarchical Weight Sharing Strategy to Reduce Task Conflicts.

### $\text{\color{#2F6EBA}{Push\ the\ Limits\ of\  Human-Centric\ Tasks}}$  
- Higher Performance than States-of-the-art Methods on 17 Datasets and On-par Performance than States-of-the-art Methods on 2 Datasets.
- Even the Tasks do NOT Exist in the Training Data.


## Installation
See [installation instructions](asset/INSTALL.md).

## Data
See [data instructions](asset/DATA.md). 

We also provide a small training config, with 10% samples of the whole pretraining dataset. 

## Training
Download pre-trained MAE ViT-Large model from [here](https://dl.fbaipublicfiles.com/mae/pretrain/mae_pretrain_vit_large.pth) and update `path/to/mae_pretrain_vit_large.pth` in `$Painter_ROOT/train_painter_vit_large.sh`. 


```bash
bash train_painter_vit_large.sh
```

## Evaluation
See [evaluation instructions](docs/EVAL.md). 

A pre-trained Painter is available at [🤗 google drive](https://huggingface.co/BAAI/Painter/blob/main/painter_vit_large.pth). The results on various tasks are summarized below:


## Project Release
- [ ] Hugging Face Release
- [ ] Detailed and Convinent Methods for Data Preparation.
- [x] PATH-B finetune configs
- [x] PATH-B/L HumanBench pretrained models
- [x] PATH Pretraining Code

## Citation

```
@article{tang2023humanbench,
  title={HumanBench: Towards General Human-centric Perception with Projector Assisted Pretraining},
  author={Tang, Shixiang and Chen, Cheng and Xie, Qingsong and Chen, Meilin and Wang, Yizhou and Ci, Yuanzheng and Bai, Lei and Zhu, Feng and Yang, Haiyang and Yi, Li and others},
  journal={arXiv preprint arXiv:2303.05675},
  year={2023}
}
```

## Acknowledgement
[MAE](https://github.com/facebookresearch/mae), [Mask2Former](https://github.com/facebookresearch/Mask2Former), [bts](https://github.com/cleinc/bts), [mmcv](https://github.com/open-mmlab/mmcv), [mmdetetection](https://github.com/open-mmlab/mmdetection), [mmpose](https://github.com/open-mmlab/mmpose).

## Contact

**We are hiring** at all levels at 2d-3d Human-Centric Foundation Model Team, including full-time researchers, engineers and interns. 
If you are interested in working with us on **human-centric foundation model and human-centric AIGC driven by foundation model**, please contact [Shixiang Tang](`tangshixiang2016@gmail.com`).

