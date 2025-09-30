# 🎬IMAGEdit🎬: Let Any Subject Transform
[![Project Page](https://img.shields.io/badge/Project-Page-green)](https://muzishen.github.io/IMAGEdit/)
[![Technique Report](https://img.shields.io/badge/Technique-Report-red)](https://muzishen.github.io/IMAGEdit/)
[![Dataset MSVBench](https://img.shields.io/badge/Dataset-MSVBench-orange)](https://muzishen.github.io/IMAGEdit/)
[![GitHub stars](https://img.shields.io/github/stars/XWH-A/IMAGEdit?style=social)](https://github.com/XWH-A/IMAGEdit)

<!-- [![🤗 Hugging Face Model](https://img.shields.io/badge/🤗%20Hugging%20Face-model-blue)](PLACEHOLDER_URL)
[![Dataset MSVBench](https://img.shields.io/badge/Dataset-MSVBench-orange)](PLACEHOLDER_URL) -->


**IMAGEdit: Let Any Subject Transform [[Project](https://muzishen.github.io/IMAGEdit/)] [[Code](https://github.com/XWH-A/IMAGEdit)]** <br />  
[Fei Shen](https://muzishen.github.io/), [Weihao Xu]([https://muzishen.github.io/IMAGEdit/](https://github.com/XWH-A/)), [Rui Yan](https://ruiyan1995.github.io/), [Dong Zhang](https://dongzhang89.github.io/), [Xiangbo Shu](https://shuxb104.github.io/), [Jinhui Tang](https://scholar.google.com/citations?user=ByBLlEwAAAAJ&hl=en) <br />



## 📅 Release

- [2025/10/1] 🎉 We launch the [project page](https://muzishen.github.io/IMAGEdit/) of IMAGEdit.



----

### 🚀 **Key Features:**
1. **Training-Free & Plug-and-Play**: IMAGEdit requires no additional training and can be seamlessly integrated into existing mask-driven video editing backbones.  
2. **Prompt-Guided Multimodal Alignment**: Aligns user prompts with visual semantics to ensure accurate subject replacement and category transformation.  
3. **Prior-Based Mask Retargeting**: Leverages depth and temporal priors to generate smooth, time-consistent mask motion sequences, even in crowded scenes.  
4. **Robust Any-Subject Editing**: Supports flexible editing for single or multiple subjects while preserving background and maintaining temporal coherence across frames.  



## 💡 Introduction

We presented IMAGEdit, a training free framework for video editing with any number of subjects that changes designated categories. IMAGEdit provides robust multimodal conditioning and precise mask motion sequences through two key components, a prompt guided multimodal alignment module and a prior based mask retargeting module. By leveraging the understanding and generation capabilities of large pretrained models, these components produce aligned multimodal signals and time consistent masks that effectively remedy insufficient prompt side conditioning and overcome mask boundary entanglement in crowded scenes. The framework then conditions a pretrained mask driven video generator to synthesize the edited video. IMAGEdit is plug and play with a wide range of mask driven backbones and consistently improves overall performance. Extensive experiments on the new multi subject benchmark MSVBench verify that IMAGEdit surpasses state of the art methods. Code, dataset, and weights will be released to support further research.
## 🔥 DatasetDemo
## 🔥 Examples


<table align="center">
  <tr>
    <td align="center" style="width: 150px; padding-right: 15px;">
      <img src="asset/ori_720_16_gif/tuk-tuk_processed.gif" width="150"/>
    </td>
    <td align="center" style="width: 150px; padding-left: 15px;">
      <img src="asset/IMAGEdit_720_16_gif/tuk-tuk_processed.gif" width="150"/>
    </td>
    <td style="position: relative; width: 2px; padding: 0;">
      <div style="position: absolute; top: 0; bottom: 0; left: 0; right: 0; border-left: 2px solid #ddd;"></div>
    </td> <!-- 固定分界线位置 -->
    <td align="center" style="width: 150px; padding-right: 15px;">
      <img src="asset/ori_720_16_gif/Football-Match-Start_processed.gif" width="150"/>
    </td>
    <td align="center" style="width: 150px; padding-left: 15px;">
      <img src="asset/IMAGEdit_720_16_gif/Football-Match-Start_processed.gif" width="150"/>
    </td>
  </tr>
  <tr>
    <td colspan="2" align="center" style="padding: 10px;">Three [People -> Super Mario] sitting in car backseat.</td>
    <td style="padding: 0;"></td> <!-- 空白单元格 -->
    <td colspan="2" align="center" style="padding: 10px;">Four [People -> Robots] standing on football court.</td>
  </tr>
</table>

<table align="center">
  <tr>
    <td align="center" style="width: 150px; padding-right: 15px;">
      <img src="asset/ori_720_16_gif/dogs-gathering-around-food_processed.gif" width="150"/>
    </td>
    <td align="center" style="width: 150px; padding-left: 15px;">
      <img src="asset/IMAGEdit_720_16_gif/dogs-gathering-around-food_processed.gif" width="150"/>
    </td>
    <td style="position: relative; width: 2px; padding: 0;">
      <div style="position: absolute; top: 0; bottom: 0; left: 0; right: 0; border-left: 2px solid #ddd;"></div>
    </td> <!-- 固定分界线位置 -->
    <td align="center" style="width: 150px; padding-right: 15px;">
      <img src="asset/ori_720_16_gif/people-training-boxing-class_processed.gif" width="150"/>
    </td>
    <td align="center" style="width: 150px; padding-left: 15px;">
      <img src="asset/IMAGEdit_720_16_gif/people-training-boxing-class_processed.gif" width="150"/>
    </td>
  </tr>
  <tr>
    <td colspan="2" align="center" style="padding: 10px;">Four [Hungry Dogs -> Robot Wolves] surrounding a bowl of food outdoors.</td>
    <td style="padding: 0;"></td> <!-- 空白单元格 -->
    <td colspan="2" align="center" style="padding: 10px;">A group of [People -> Astronauts] practicing boxing in a fitness studio.</td>
  </tr>
</table>

<table align="center">
  <tr>
    <td align="center" style="width: 150px; padding-right: 15px;">
      <img src="asset/ori_720_16_gif/team-rowing-on-river_processed2.gif" width="150"/>
    </td>
    <td align="center" style="width: 150px; padding-left: 15px;">
      <img src="asset/IMAGEdit_720_16_gif/team-rowing-on-river_processed2.gif" width="150"/>
    </td>
    <td style="position: relative; width: 2px; padding: 0;">
      <div style="position: absolute; top: 0; bottom: 0; left: 0; right: 0; border-left: 2px solid #ddd;"></div>
    </td> <!-- 固定分界线位置 -->
    <td align="center" style="width: 150px; padding-right: 15px;">
      <img src="asset/ori_720_16_gif/110m-Hurdles-Mid-Air-Dash_processed.gif" width="150"/>
    </td>
    <td align="center" style="width: 150px; padding-left: 15px;">
      <img src="asset/IMAGEdit_720_16_gif/110m-Hurdles-Mid-Air-Dash_processed.gif" width="150"/>
    </td>
  </tr>
  <tr>
    <td colspan="2" align="center" style="padding: 10px;">A team of [Men -> Spider-Men] rowing together on a river.</td>
    <td style="padding: 0;"></td> <!-- 空白单元格 -->
    <td colspan="2" align="center" style="padding: 10px;">Eight [Hurdlers -> Iron Men] leap mid-race over purple hurdles.</td>
  </tr>
</table>



## Acknowledgement
We would like to thank the contributors to the [IDM-VTON](https://github.com/yisol/IDM-VTON), [MagicClothing](https://github.com/ShineChen1024/MagicClothing), [IP-Adapter](https://github.com/tencent-ailab/IP-Adapter), [ControlNet](https://github.com/lllyasviel/ControlNet), [T2I-Adapter](https://github.com/TencentARC/T2I-Adapter), and [AnimateDiff](https://github.com/guoyww/AnimateDiff) repositories, for their open research and exploration.

The IMAGDressing code is available for both academic and commercial use. However, the models available for manual and automatic download from IMAGEdit are intended solely for non-commercial research purposes. Similarly, our released checkpoints are restricted to research use only. Users are free to create images using this tool, but they must adhere to local laws and use it responsibly. The developers disclaim any liability for potential misuse by users.

## 📝 Citation

If you find IMAGEdit useful for your research and applications, please cite using this BibTeX:

```bibtex
@article{shenimagedit,
  title={IMAGEdit: Let Any Subject Transform},
  author={Shen, Fei and Xu, Weihao and Yan, Rui and Zhang, Dong and Shu, Xiangbo and Tang, Jinhui},
  booktitle={arXiv preprint arXiv:2509.xx},
  year={2024}
}
```

## 🕒 TODO List
- [x] Gradio demo
- [x] Inference code
- [x] Model weights (512 sized version)
- [x] Support inpaint
- [ ] Model weights (More higher sized version)
- [x] Paper
- [x] Evaluate metric code
- [x] IGPair dataset
- [x] Training code
- [ ] Video Dressing
- [ ] Others, such as User-Needed Requirements


## 👉 **Our other projects:**  
- [IMAGDressing](https://github.com/muzishen/IMAGDressing): Controllable dressing generation. [可控穿衣生成]
- [IMAGGarment](https://github.com/muzishen/IMAGGarment): Fine-grained controllable garment generation.  [可控服装生成]
- [IMAGHarmony](https://github.com/muzishen/IMAGHarmony): Controllable image editing with consistent object layout.  [可控多目标编辑]
- [IMAGPose](https://github.com/muzishen/IMAGPose): Pose-guided person generation with high fidelity.  [可控多模式人物生成]
- [RCDMs](https://github.com/muzishen/RCDMs): Rich-contextual conditional diffusion for story visualization.  [可控故事生成]
- [PCDMs](https://github.com/tencent-ailab/PCDMs): Progressive conditional diffusion for pose-guided image synthesis. [可控人物生成]
- [V-Express](https://github.com/tencent-ailab/V-Express/): Explores strong and weak conditional relationships for portrait video generation. [可控数字人生成]
- [FaceShot](https://github.com/open-mmlab/FaceShot/): Talkingface plugin for any character. [可控动漫数字人生成]
- [CharacterShot](https://github.com/Jeoyal/CharacterShot): Controllable and consistent 4D character animation framework. [可控4D角色生成]
- [StyleTailor](https://github.com/mahb-THU/StyleTailor): An Agent for personalized fashion styling. [个性化时尚Agent]
- [SignVip](https://github.com/umnooob/signvip/): Controllable sign language video generation. [可控手语生成]


## 📨 Contact
If you have any questions, please feel free to contact with me at xxx or shenfei140721@126.com.
