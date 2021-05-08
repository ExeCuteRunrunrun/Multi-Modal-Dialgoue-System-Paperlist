# Multi-Modal-Dialgoue-System-Paperlist

This is a paper list for the multimodal dialogue systems topic.

**Keyword**: Multi-modal, Dialogue system, visual, conversation

# Paperlist

## Dataset & Challenges

### Images
 
(1) [**Visual QA**](https://visualqa.org/workshop.html) VQA datasets in CVPR2021,2020,2019,..., containing open-ended questions about images. These questions require an understanding of vision, language and commonsense knowledge to answer.
- [VQA](https://visualqa.org/challenge) datasets [1.0](http://arxiv.org/abs/1505.00468) [2.0](https://arxiv.org/abs/1612.00837)
- [TextVQA](https://textvqa.org/paper) TextVQA requires models to read and reason about text in an image to answer questions based on them. In order to perform well on this task, models need to first detect and read text in the images. Models then need to reason about this to answer the question. 
- [TextCap](https://arxiv.org/abs/2003.12462) TextCaps requires models to read and reason about text in images to generate captions about them. Specifically, models need to incorporate a new modality of text present in the images and reason over it and visual content in the image to generate image descriptions.
- Issues : 
  - visual-explainable: the model should rely on the right visual regions when making decisions, 
  - question-sensitive: the model should be sensitive to the linguistic variations in question
  - reduce language biases: the model should not take the language shortcut to answer the question without looking at the image
- Further Papers 
  - Multi-task
    - [Visual Question Answering as a Multi-Task Problem](https://arxiv.org/pdf/2007.01780.pdf) arXiv2020
    - [Bottom-up and top-down attention for image captioning and visual question answering](https://arxiv.org/abs/1707.07998) in CVPR2018, winner of the 2017 Visual Question Answering challenge
  - Language prior issue
    - [AdaVQA: Overcoming Language Priors with Adapted Margin Cosine Loss](https://arxiv.org/pdf/2105.01993.pdf) in a perspective of feature space learning (not classification task)
    - [Making the V in VQA Matter: Elevating the Role of Image Understanding in Visual Question Answering](https://arxiv.org/abs/1612.00837) CVPR2017 VQA 2.0 is also for the purpose of balance language prior to images 
    - [Self-Critical Reasoning for Robust Visual Question Answering](https://arxiv.org/pdf/1905.09998.pdf) NeurIPS2019
    - [Overcoming Language Priors in Visual Question Answering with Adversarial Regularization](https://arxiv.org/pdf/1810.03649.pdf) NeurIPS2018, question-only model
    - [RUBi: Reducing Unimodal Biases in Visual Question Answering](https://arxiv.org/pdf/1906.10169.pdf) NeurIPS2019 also question-only model
  - Visual-explainable issue
    - [Counterfactual Samples Synthesizing for Robust Visual Question Answering](http://arxiv.org/pdf/2003.06576) CVPR2020
    - [Learning to Contrast the Counterfactual Samples for Robust Visual Question Answering](https://www.aclweb.org/anthology/2020.emnlp-main.265.pdf) EMNLP2020
    - [Learning What Makes a Difference from Counterfactual Examples and Gradient Supervision](https://arxiv.org/pdf/2004.09034.pdf) ECCV2020 leveraging overlooked supervisory signal found in existing datasets to improve generalization capabilities
  - Learning to reason / visual understanding / Graphs
    - [MUREL: Multimodal Relational Reasoning for Visual Question Answering](http://arxiv.org/pdf/1902.09487) CVPR2019, [[Code](github.com/Cadene/murel.bootstrap.pytorch)], represent and refine interactions between question words and image regions, more fine than attention-maps
    - [CRA-Net: Composed Relation Attention Network for Visual Question Answering](https://dl.acm.org/doi/10.1145/3343031.3350925) ACM 不让看哦？
    - [Relation-Aware Graph Attention Network for Visual Question Answering](http://arxiv.org/pdf/1903.12314) ICCV2019, explicit relations of geometric positions and semantic interactions between objects, implicit relations of hidden dynamics between image regions
    
  - Knowledge / Graphs
    - [Towards Knowledge-Augmented Visual Question Answering](https://www.aclweb.org/anthology/2020.coling-main.169.pdf) Coling2020, capture the interactions between objects in a visual scene and entities in an external knowledge source, with many many graphs ...
    - [ConceptBert: Concept-Aware Representation for Visual Question Answering](https://www.aclweb.org/anthology/2020.findings-emnlp.44.pdf) EMNLP2020, learn a joint Concept-Vision-Language embedding (maybe similar to [[this paper](https://openreview.net/references/pdf?id=Uhl6chXANP)] in the way of adding "entity embedding" ?)
    - 

(2) [**Visual Dialog**](https://visualdialog.org/) CVPR 2017, Open-domain dialogs & given an image, a dialog history, and a follow-up question about the image, the task is to answer the question. 
-  [VisDial v1.0 dataset](https://visualdialog.org/data) [[Paper](https://arxiv.org/abs/1611.08669)] [[Source Code to collect chat data](https://github.com/batra-mlp-lab/visdial-amt-chat)]
-  Further papers
  - [Improving Generative Visual Dialog by Answering Diverse Questions](https://arxiv.org/pdf/1909.10470.pdf) EMNLP 2019, [[Code](https://github.com/vmurahari3/visdial-diversity)]
  - [Learning Cooperative Visual Dialog Agents with Deep Reinforcement Learning](https://arxiv.org/abs/1703.06585) ICCV2017 oral, [[Code](https://github.com/batra-mlp-lab/visdial-rl)
  - [DualVD: An Adaptive Dual Encoding Model for Deep Visual Understanding in Visual Dialogue](https://arxiv.org/pdf/1911.07251.pdf)

(3) [**GuessWhat?!**](https://openaccess.thecvf.com/content_cvpr_2017/html/de_Vries_GuessWhat_Visual_Object_CVPR_2017_paper.html) Visual Object Discovery Through Multi-Modal Dialogue in CVPR2017, a two-player guessing game (1 oracle & 1 questioner). 
- [[Code]](https://github.com/GuessWhatGame/guesswhat)
- Further paper [End-to-end optimization of goal-driven and visually grounded dialogue systems](https://arxiv.org/abs/1703.05423) Reinforcement Learning applied to GuessWhat?! 

(4) [Image caption] generating natural language description of an image
- [MS COCO dataset 2014](https://arxiv.org/pdf/1405.0312.pdf) Images + captions (but captions are single words not sentences)
- Further papers
  - Feature images as a whole / and regions (early approachs) : 
    - [Deep visual-semantic alignments for generating image descriptions](https://cs.stanford.edu/people/karpathy/deepimagesent/devisagen.pdf) CVPR2015
    - [Densecap: Fully convolutional localization networks for dense captioning](https://cs.stanford.edu/people/karpathy/densecap/) CVPR2016
  - Attention based approaches :
    - [Bottom-up and top-down attention for image captioning and visual question answering](https://arxiv.org/abs/1707.07998) in CVPR2018, winner of the 2017 Visual Question Answering challenge
    - [Show, attend and tell: Neural image caption generation with visual attention](https://arxiv.org/abs/1502.03044) in ICML2015
    - [Review networks for caption generation](https://arxiv.org/abs/1605.07912) NIPS2016
    - [Image captioning with semantic attention](https://arxiv.org/abs/1603.03925) CVPR2016
  - Graph structured approaches :
    - [Exploring Visual Relationship for Image Captioning](https://arxiv.org/abs/1809.07041) ECCV2018
    - [Auto-encoding scene graphs for image captioning](https://arxiv.org/abs/1812.02378) CVPR2019
  - Reinforcement learning:
    - [Context-aware visual policy network for sequence-level image captioning](https://arxiv.org/abs/1808.05864) ACM2018
    - [Self-critical sequence training for image captioning](https://arxiv.org/abs/1612.00563)
  - Transformer based:
    - [Image captioning: transform objects into words](https://papers.nips.cc/paper/2019/file/680390c55bbd9ce416d1d69a9ab4760d-Paper.pdf) in NIPS2019 using Transformers focusing on objects and their spatial relationships
    - [Conceptual captions: A cleaned, hypernymed, image alt-text dataset for automatic image captioning](https://www.aclweb.org/anthology/P18-1238.pdf) in ACL2018, also a dataset

(5) [ReferIt](http://tamaraberg.com/referitgame/) [[paper](http://tamaraberg.com/papers/referit.pdf)] in EMNLP2014, 2-players game of refer & label

(6) [OpenViDial: A Large-Scale, Open-Domain Dialogue Dataset with Visual Contexts]

(7) [CLEVR-Dialog: A Diagnostic Dataset for Multi-Round Reasoning in Visual Dialog](https://www.aclweb.org/anthology/N19-1058) NAACL2019, [[code](https://github.com/satwikkottur/clevr-dialog)]

(8) [Talk the walk: Navigating new york city through grounded dialogue](https://arxiv.org/pdf/1807.03367.pdf)


#### 🌟🌟🌟 ----F-a-s-h-i-o-n----

(9) [**SIMMC**](https://github.com/facebookresearch/simmc) - Domains include furniture and fashion 🌟🌟🌟, it can be seen as a variant of [multiWOZ](https://github.com/budzianowski/multiwoz) or [schema guided dialogue dataset](https://github.com/google-research-datasets/dstc8-schema-guided-dialogue#scheme-representation%5D)
- [SIMMC 1.0](https://arxiv.org/abs/2006.01460) in Coling2020, [SIMMC 2.0](https://arxiv.org/pdf/2104.08667.pdf), track in [DSTC9](https://dstc9.dstc.community/home) and [DSTC10](https://sites.google.com/dstc.community/dstc10/tracks) 
- [[Code](https://github.com/facebookresearch/simmc)] 
- Further papers
  - [A Response Retrieval Approach for Dialogue Using a Multi-Attentive Transformer](https://arxiv.org/abs/2012.08148) second winner DSTC9 SIMMC fashion, [[code](https://github.com/D2KLab/dstc9-SIMMC)]
  - [Overview of the Ninth Dialog System Technology Challenge: DSTC9](https://arxiv.org/pdf/2011.06486.pdf) to better see the winners' models
  - [[Code winner1 TNU](https://github.com/billkunghappy/DSTC_TRACK4_ENTER)](有点乱), [[Code winner2 SU](https://github.com/inkoon/simmc), [[Code other](https://github.com/facebookresearch/simmc/blob/master/DSTC9_SIMMC_RESULTS.md)]

(10) [**Fashion IQ**](https://sites.google.com/view/cvcreative2020/fashion-iq) in CVPR2020 workshop, [[paper](https://arxiv.org/pdf/1905.12794.pdf)] [[dataset & startkit](https://github.com/XiaoxiaoGuo/fashion-iq)] 

(11) [**MMD** Towards Building Large Scale Multimodal Domain-Aware Conversation Systems](https://arxiv.org/abs/1704.00200), arXiv 2017, [[code](https://amritasaha1812.github.io/MMD/)]


### Video
 
(12) [Audio Visual Scene-Aware Dialog Track in DSTC8](http://workshop.colips.org/dstc7/dstc8/Audiovisual_Scene_Aware_Dialog.pdf) [[Paper]((https://ieeexplore.ieee.org/document/8953254)]  [[site]]((https://video-dialog.com/) 
- Related : [[TVQA](https://arxiv.org/abs/1809.01696)] [[MovieQA](http://movieqa.cs.toronto.edu/)] [[TGif-QA](https://arxiv.org/abs/1704.04497)]
- Further papers


### Charts / figures
(13) [LEAF-QA: Locate, Encode & Attend for Figure Question Answering](https://openaccess.thecvf.com/content_WACV_2020/papers/Chaudhry_LEAF-QA_Locate_Encode__Attend_for_Figure_Question_Answering_WACV_2020_paper.pdf)

### Meme
(14) [MOD Meme incorporated Open Dialogue](https://anonymous.4open.science/r/e7eaef6a-b6d5-47c6-896f-93265a0af4b1/README.md) WeChat conversations with meme / stickers in Chinese language.

# Survey
[Multimodal Research in Vision and Language: A Review of Current and Emerging Trends](https://arxiv.org/pdf/2010.09522v2.pdf)


# In general
- Often used model-elements :
  - [Faster R-CNN: Towards Real-Time Object Detection with Region Proposal Networks]() 2015
  - LSTM
  - Transformers
