<div align="center">


  ## Awesome Speech and Audio Continual Learning

[![Awesome](https://img.shields.io/badge/Awesome-0066CC?style=for-the-badge&logo=awesome-lists&logoColor=white)](https://github.com/sindresorhus/awesome) [![Survey](https://img.shields.io/badge/Survey--ArXiv-A42C25?style=for-the-badge&logo=latex&logoColor=white)](../ieee_main.pdf) [![Github](https://img.shields.io/badge/Awesome--CL--for--Speech--and--Audio-000000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/swagshaw/Awesome-Speech-and-Audio-Continual-Learning/)

<br>
<img src="CL speech.png" style="width: 68%;"/>


</div>

> A curated paper list for continual learning in speech and audio, covering ASR, TTS, speaker-related tasks, audio classification, SED/SELD, sound source localization, audio-visual learning, separation, deepfake detection, speech SSL, and speech LLMs. We welcome issues and pull requests for missing or newly released work.

## News

- **[2026-04-25]** 🔥 We are excited to introduce a collection of papers on CL for speech and audio models!

## Citation

If you find this list helpful, please cite our work:

```bibtex
@article{speech_audio_cl_survey_2026,
  title={A Survey of Continual Learning in Speech and Audio},
  author={Yang Xiao},
  year={2026},
}
```

## Contents

- [📖 Overview](#overview)
- [📄 Paper List](#paper-list)
  - [Foundations, Surveys, and Benchmarks](#foundations-surveys-and-benchmarks)
  - [ASR: Domain, Acoustic Models, and End-to-End Learning](#asr-domain-acoustic-models-and-end-to-end-learning)
  - [ASR: Online, On-device, and Deployment-oriented Learning](#asr-online-on-device-and-deployment-oriented-learning)
  - [ASR: Multilingual, Whisper, and Language Extension](#asr-multilingual-whisper-and-language-extension)
  - [Speech SSL and Continual Pretraining](#speech-ssl-and-continual-pretraining)
  - [TTS and Generative Speech](#tts-and-generative-speech)
  - [Speech LLMs and Multimodal Speech Models](#speech-llms-and-multimodal-speech-models)
  - [Audio-Visual and Multimodal Audio Continual Learning](#audio-visual-and-multimodal-audio-continual-learning)
  - [Speaker-related Tasks and Speech Emotion Recognition](#speaker-related-tasks-and-speech-emotion-recognition)
  - [Keyword Spotting and Spoken Language Understanding](#keyword-spotting-and-spoken-language-understanding)
  - [Audio Classification and Acoustic Scenes](#audio-classification-and-acoustic-scenes)
  - [Sound Event Detection, Localization, and Bioacoustics](#sound-event-detection-localization-and-bioacoustics)
  - [Audio Deepfake Detection](#audio-deepfake-detection)
  - [Audio Captioning, Separation, Enhancement, and Audio-Text Learning](#audio-captioning-separation-enhancement-and-audio-text-learning)

## 📖 Overview
<img src="./overview.png" alt="Overview diagram of continual learning for speech and audio" width="90%">
This list follows the taxonomy used in the survey:

1. **Settings:** domain-, class-, task-, online-, and model-scale continual learning.
2. **Method families:** regularization, replay, architecture-based methods, PEFT, averaging, continual pretraining, and multimodal post-training.
3. **Tasks:** speech recognition and synthesis, speaker-aware interfaces, environmental audio, event detection and localization, audio-visual learning, separation, deepfake detection, and speech-capable foundation models.

## 📄 Paper List

### Foundations, Surveys, and Benchmarks

| Year | Title | Venue | Paper | TLDR |
|:-:|:-|:-|:-:|:-|
| 2026 | Closing the Modality Reasoning Gap for Speech Large Language Models | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2601.05543) | Studies how speech LLMs retain reasoning ability when cross-modal speech modules are added. |
| 2025 | Continual Learning for Acoustic Event Classification | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2512.17932) | Frames acoustic event recognition as sequential class learning and evaluates retention under incremental updates. |
| 2025 | Closing the Gap Between Text and Speech Understanding in LLMs | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2510.13632) | Analyzes speech-LLM adaptation as a trade-off between new speech understanding and preserved text capability. |
| 2025 | Cross-Modal Knowledge Distillation for Speech Large Language Models | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp55912.2026.11464272) | Uses cross-modal distillation to transfer speech knowledge while limiting capability degradation. |
| 2025 | Analyzing Mitigation Strategies for Catastrophic Forgetting in End-to-End Training of Spoken Language Models | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2025-409) | Compares practical forgetting-mitigation strategies for end-to-end spoken language model training. |
| 2025 | Few-Shot Keyword-incremental Learning Using Compositional Information | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp49660.2025.10889790) | Uses compositional cues to add new keywords from few examples without retraining the full KWS model. |
| 2024 | Few-Shot Keyword-Incremental Learning with Total Calibration | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2024-1823) | Calibrates few-shot keyword classifiers so new classes can be added without overwhelming old ones. |
| 2024 | Towards Robust Audio Deepfake Detection: A Evolving Benchmark for Continual Learning | - | - | Proposes an evolving evaluation setting for audio deepfake detection under newly emerging attack types. |
| 2024 | Disentangled Prototype-Guided Dynamic Memory Replay for Continual Learning in Acoustic Signal Classification | IEEE Access | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/access.2024.3482105) | Combines prototype guidance and dynamic replay memory for acoustic signal classification. |
| 2023 | CL-MASR: A Continual Learning Benchmark for Multilingual ASR | IEEE/ACM TASLP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.36227/techrxiv.24430876.v1) | Establishes a multilingual ASR benchmark for measuring language acquisition and forgetting. |
| 2023 | M-CTRL: A Continual Representation Learning Framework with Slowly Improving Past Pre-Trained Model | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp49357.2023.10096793) | Extends CTRL with a gradually updated teacher to stabilize continual speech representation learning. |
| 2023 | Mitigating Catastrophic Forgetting for Few-Shot Spoken Word Classification Through Meta-Learning | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2023-385) | Applies meta-learning to preserve old spoken-word classes during few-shot class expansion. |
| 2023 | Continually Learning New Languages | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2211.11703) | Studies language-incremental ASR, including regularization and model-averaging style retention methods. |
| 2022 | Towards Continually Learning New Languages | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2023-1867) | Introduces language expansion as a continual-learning problem for multilingual ASR. |
| 2022 | Privacy Preserving Synthetic Respiratory Sounds for Class Incremental Learning | Smart Health | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1016/j.smhl.2021.100232) | Uses synthetic respiratory audio to support privacy-preserving class-incremental learning. |
| 2021 | An Incremental Class-Learning Approach with Acoustic Novelty Detection for Acoustic Event Recognition | Sensors | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.3390/s21196622) | Couples novelty detection with incremental acoustic event recognition. |
| 2019 | A Progressive Model to Enable Continual Learning for Semantic Slot Filling | EMNLP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.18653/v1/d19-1126) | Early progressive-network style approach for continual semantic slot filling. |
| 1993 | Catastrophic Forgetting in Neural Networks: The Role of Rehearsal Mechanisms | ANNES | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/annes.1993.323080) | Classic rehearsal study that motivates later replay-based continual-learning methods. |

### ASR: Domain, Acoustic Models, and End-to-End Learning

| Year | Title | Venue | Paper | TLDR |
|:-:|:-|:-|:-:|:-|
| 2026 | Continual Adaptation for Pacific Indigenous Speech Recognition | - | - | Applies parameter-efficient continual adaptation to low-resource Indigenous speech recognition. |
| 2026 | Efficient Rehearsal for Continual Learning in ASR via Singular Value Tuning | IEEE/ACM TASLP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/taslpro.2026.3658931) | Combines compact rehearsal with singular-value tuning for efficient ASR adaptation. |
| 2025 | Continuous Learning for Children's ASR: Overcoming Catastrophic Forgetting with Elastic Weight Consolidation and Synaptic Intelligence | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2505.20216) | Tests EWC and SI for child-speech adaptation, where age-related acoustic shifts create realistic forgetting pressure. |
| 2026 | Inverse-Hessian Regularization for Continual Learning in ASR | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp55912.2026.11461503) | Uses curvature-aware regularization to protect important ASR parameters during sequential training. |
| 2025 | Continual Test-Time Dynamic Speech Recognition via Adaptive Threshold | CMLDS | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1117/12.3072469) | Adapts ASR at test time with thresholding for changing deployment conditions. |
| 2025 | Weight Factorization and Centralization for Continual Learning in Speech Recognition | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2025-1701) | Uses factorized and centralized weights to reduce forgetting in sequential ASR updates. |
| 2025 | Low-Resource Speech Recognition of Radiotelephony Communications Based on Continuous Learning of In-Domain and Out-of-Domain Knowledge | IEEE Signal Processing Letters | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/lsp.2025.3545955) | Mixes in-domain and out-of-domain knowledge for low-resource radiotelephony ASR. |
| 2024 | Parameter Averaging Is All You Need To Prevent Forgetting | SLT | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/slt61566.2024.10832275) | Shows that simple parameter averaging can be a strong anti-forgetting baseline for ASR. |
| 2024 | Sequential Editing for Lifelong Training of Speech Recognition Models | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2024-2027) | Treats ASR updates as sequential edits rather than full retraining. |
| 2024 | Bayesian Parameter-Efficient Fine-Tuning for Overcoming Catastrophic Forgetting | IEEE/ACM TASLP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/taslp.2024.3463395) | Adds Bayesian PEFT machinery to stabilize ASR fine-tuning across tasks. |
| 2024 | Continuously Learning New Words in Automatic Speech Recognition | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp49660.2025.10889216) | Focuses on adding new vocabulary to ASR while preserving existing recognition ability. |
| 2023 | CLRL-Tuning: A Novel Continual Learning Approach for Automatic Speech Recognition | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2023-503) | Proposes a continual tuning strategy for updating ASR models without full retraining. |
| 2023 | Continual Learning for End-to-End ASR by Averaging Domain Experts | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2305.09681) | Averages domain experts to balance new-domain adaptation and old-domain retention. |
| 2023 | Residual Adapters for Targeted Updates in RNN-Transducer Based Speech Recognition System | SLT | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/slt54892.2023.10022622) | Uses residual adapters for localized RNN-T updates. |
| 2023 | Domain Expansion for End-to-End Speech Recognition: Applications for Accent/Dialect Speech | IEEE/ACM TASLP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/taslp.2022.3233238) | Studies accent and dialect expansion in end-to-end ASR with forgetting-aware adaptation. |
| 2022 | Weight Averaging: A Simple Yet Effective Method to Overcome Catastrophic Forgetting in Automatic Speech Recognition | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp49357.2023.10095147) | Introduces weight averaging as a simple ASR retention method. |
| 2022 | Damage Control During Domain Adaptation for Transducer Based Automatic Speech Recognition | SLT | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/slt54892.2023.10023219) | Uses adapter-style targeted updates to limit forgetting in transducer ASR adaptation. |
| 2022 | Incremental Learning for RNN-Transducer Based Speech Recognition Models | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2022-10795) | Studies incremental learning for production-style RNN-T ASR models. |
| 2022 | Dealing with Unknowns in Continual Learning for End-to-end Automatic Speech Recognition | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2022-11139) | Handles unknown classes/domains in continual end-to-end ASR. |
| 2022 | Updating Only Encoders Prevents Catastrophic Forgetting of End-to-End ASR Models | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2022-11282) | Shows that encoder-only updates can reduce forgetting in end-to-end ASR. |
| 2022 | Using Adapters to Overcome Catastrophic Forgetting in End-to-End Automatic Speech Recognition | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp49357.2023.10095837) | Applies adapters as parameter-efficient modules for continual ASR. |
| 2021 | Continual Learning for Monolingual End-to-End Automatic Speech Recognition | EUSIPCO | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.23919/eusipco55093.2022.9909589) | Early monolingual end-to-end ASR study of domain adaptation and forgetting. |
| 2021 | Continual Learning Using Lattice-Free MMI for Speech Recognition | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp43922.2022.9746260) | Adapts LF-MMI acoustic models with continual-learning regularization. |
| 2021 | Towards Lifelong Learning of End-to-end ASR | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2021-563) | Foundational end-to-end ASR paper framing lifelong domain expansion. |
| 2020 | Continual Learning for Multi-Dialect Acoustic Models | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2020-1797) | Studies dialect-incremental acoustic modeling. |
| 2020 | Continual Learning in Automatic Speech Recognition | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2020-2962) | Early ASR-specific comparison of continual-learning strategies. |
| 2020 | Incremental Learning for End-to-End Automatic Speech Recognition | ASRU | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/asru51503.2021.9687910) | Uses distillation-style incremental learning for end-to-end ASR. |
| 2019 | Domain Expansion in DNN-Based Acoustic Models for Robust Speech Recognition | ASRU | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/asru46091.2019.9003769) | Introduces domain expansion for DNN acoustic models under forgetting constraints. |
| 2019 | A Multi-Task Learning Framework for Overcoming the Catastrophic Forgetting in Automatic Speech Recognition | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/1904.08039) | Uses multi-task learning to reduce forgetting in ASR adaptation. |

### ASR: Online, On-device, and Deployment-oriented Learning

| Year | Title | Venue | Paper | TLDR |
|:-:|:-|:-|:-:|:-|
| 2026 | No Label? No Problem: Unsupervised Continual Learning for Adaptive Medical ASR | EACL Industry | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://aclanthology.org/2026.eacl-industry.24/) | Studies privacy-conscious unsupervised adaptation for medical ASR without labeled target speech. |
| 2024 | Continual Test-time Adaptation for End-to-end Speech Recognition on Noisy Speech | EMNLP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://aclanthology.org/2024.emnlp-main.1116/) | Treats changing noisy conditions as a continual test-time adaptation problem. |
| 2024 | Unsupervised Online Continual Learning for Automatic Speech Recognition | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2024-136) | Updates ASR online from unlabeled streams. |
| 2023 | Rehearsal-Free Online Continual Learning for Automatic Speech Recognition | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2023-788) | Removes rehearsal storage from online ASR continual learning. |
| 2022 | Continual Learning for On-Device Speech Recognition Using Disentangled Conformers | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp49357.2023.10095484) | Uses disentangled Conformers for user/device-specific ASR adaptation. |
| 2022 | Online Continual Learning of End-to-End Speech Recognition Models | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2022-11093) | Studies replay and regularization for streaming end-to-end ASR updates. |

### ASR: Multilingual, Whisper, and Language Extension

| Year | Title | Venue | Paper | TLDR |
|:-:|:-|:-|:-:|:-|
| 2024 | Continual Learning With Embedding Layer Surgery and Task-Wise Beam Search Using Whisper | SLT | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/slt61566.2024.10832213) | Extends Whisper to new tasks/languages with embedding surgery and task-wise decoding. |
| 2024 | Towards Rehearsal-Free Multilingual ASR: A LoRA-based Case Study on Whisper | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2024-1953) | Uses LoRA to extend Whisper multilingual ASR without replay. |
| 2024 | Continual Learning Optimizations for Auto-regressive Decoder of Multilingual ASR Systems | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2024-205) | Targets the autoregressive decoder as the main bottleneck in multilingual ASR extension. |
| 2024 | A Parameter-efficient Language Extension Framework for Multilingual ASR | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2024-1745) | Adds new ASR languages through parameter-efficient language-extension modules. |

### Speech SSL and Continual Pretraining

| Year | Title | Venue | Paper | TLDR |
|:-:|:-|:-|:-:|:-|
| 2025 | SONAR: Self-Distilled Continual Pre-training for Domain Adaptive Audio Representation | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp55912.2026.11465067) | Uses self-distillation to adapt audio representations while keeping prior-domain performance. |
| 2024 | What Happens in Continued Pre-Training? Analysis of Self-Supervised Speech Models with Continued Pre-Training for Colloquial Finnish ASR | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2024-476) | Diagnoses what continued SSL pretraining changes during Finnish ASR adaptation. |
| 2024 | Less Forgetting for Better Generalization: Exploring Continual-learning Fine-tuning Methods for Speech Self-supervised Representations | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2407.00756) | Compares continual fine-tuning methods for speech SSL representations. |
| 2024 | Multi-Modal Continual Pre-Training For Audio Encoders | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp48485.2024.10446424) | Continually pretrains audio encoders with multimodal signals while preserving earlier representations. |
| 2024 | SOA: Reducing Domain Mismatch in SSL Pipeline by Speech Only Adaptation for Low Resource ASR | ICASSPW | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icasspw62465.2024.10625884) | Uses speech-only SSL adaptation to reduce low-resource ASR domain mismatch. |
| 2023 | FusDom: Combining in-Domain and Out-of-Domain Knowledge for Continuous Self-Supervised Learning | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp48485.2024.10448147) | Blends in-domain and out-of-domain data for continual self-supervised speech learning. |
| 2023 | Stable Distillation: Regularizing Continued Pre-Training for Low-Resource Automatic Speech Recognition | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp48485.2024.10446335) | Regularizes continued pretraining through distillation for low-resource ASR. |
| 2022 | CTRL: Continual Representation Learning to Transfer Information of Pre-trained for WAV2VEC 2.0 | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2022-10063) | Transfers wav2vec 2.0 knowledge across sequential representation-learning stages. |
| 2021 | An Adapter Based Pre-Training for Efficient and Scalable Self-Supervised Speech Representation Learning | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp43922.2022.9747374) | Adds adapters to make speech SSL pretraining and downstream updates more modular. |
| 2021 | Continual-Wav2vec2: An Application of Continual Learning for Self-Supervised Automatic Speech Recognition | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2107.13530) | Applies continual-learning ideas to wav2vec 2.0 pretraining and ASR fine-tuning. |

### TTS and Generative Speech

| Year | Title | Venue | Paper | TLDR |
|:-:|:-|:-|:-:|:-|
| 2025 | F5-TTS-RO: Extending F5-TTS to Romanian TTS via Lightweight Input Adaptation | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2512.12297) | Adapts F5-TTS to Romanian through lightweight input-side changes. |
| 2025 | Parameter-Efficient Fine-Tuning for Low-Resource Text-to-Speech via Cross-Lingual Continual Learning | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2025-1344) | Uses PEFT for cross-lingual, low-resource TTS extension. |
| 2025 | Unseen Speaker and Language Adaptation for Lightweight Text-to-Speech with Adapters | MLSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/mlsp62443.2025.11204217) | Adds unseen speakers and languages to lightweight TTS with adapters. |
| 2024 | Continual Gated Adapter for Bilingual Codec Text-to-Speech | O-COCOSDA | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/o-cocosda64382.2024.10800072) | Uses gated adapters for bilingual codec TTS continual adaptation. |
| 2024 | Continual Learning in Machine Speech Chain Using Gradient Episodic Memory | O-COCOSDA | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/o-cocosda64382.2024.10800352) | Applies GEM to a machine speech chain coupling ASR and TTS. |
| 2022 | Adapter-Based Extension of Multi-Speaker Text-to-Speech Model for New Speakers | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2023-2313) | Extends multi-speaker TTS to new speakers through adapters. |
| 2022 | Adversarial and Sequential Training for Cross-lingual Prosody Transfer TTS | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2022-865) | Uses sequential training for cross-lingual prosody transfer in TTS. |
| 2021 | Towards Lifelong Learning of Multilingual Text-to-Speech Synthesis | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp43922.2022.9746968) | Early lifelong multilingual TTS work using task-wise language expansion. |
| 2021 | FedSpeech: Federated Text-to-Speech with Continual Learning | IJCAI | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.24963/ijcai.2021/527) | Combines federated training with continual TTS speaker adaptation. |
| 2021 | Continual Speaker Adaptation for Text-to-Speech Synthesis | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2103.14512) | Adds new TTS speakers sequentially while preserving old speaker quality. |

### Speech LLMs and Multimodal Speech Models

| Year | Title | Venue | Paper | TLDR |
|:-:|:-|:-|:-:|:-|
| 2025 | Understanding Textual Capability Degradation in Speech LLMs via Parameter Importance Analysis | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp55912.2026.11461684) | Analyzes which parameters drive text-skill degradation after speech adaptation. |
| 2025 | Balancing Speech Understanding and Generation Using Continual Pre-training for Codec-based Speech LLM | - | - | Uses continual pretraining to balance speech understanding and speech generation in codec-based LLMs. |

### Audio-Visual and Multimodal Audio Continual Learning

| Year | Title | Venue | Paper | TLDR |
|:-:|:-|:-|:-:|:-|
| 2026 | Audio-Visual Continual Test-Time Adaptation without Forgetting | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2602.18528) | Adapts audio-visual models at test time while explicitly targeting forgetting. |
| 2025 | AVQACL: A Novel Benchmark for Audio-Visual Question Answering Continual Learning | CVPR | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://openaccess.thecvf.com/content/CVPR2025/html/Wu_AVQACL_A_Novel_Benchmark_for_Audio-Visual_Question_Answering_Continual_Learning_CVPR_2025_paper.html) | Introduces Split-AVQA and Split-MUSIC-AVQA for continual audio-visual reasoning. |
| 2025 | Few-Shot Audio-Visual Class-Incremental Learning with Temporal Prompting and Regularization | AAAI | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1609/aaai.v39i15.33770) | Uses temporal prompting and regularization for few-shot audio-visual class expansion. |
| 2025 | Audio-Visual Class-Incremental Learning for Fish Feeding Intensity Assessment in Aquaculture | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2504.15171) | Applies audio-visual class-incremental learning to aquaculture acoustic-visual monitoring. |
| 2024 | STELLA: Continual Audio-Video Pre-training with SpatioTemporal Localized Alignment | ICML | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://proceedings.mlr.press/v235/lee24ac.html) | Continually pretrains audio-video models with localized spatiotemporal alignment. |
| 2024 | MMAL: Multi-Modal Analytic Learning for Exemplar-Free Audio-Visual Class Incremental Tasks | ACM MM | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1145/3664647.3681607) | Provides an exemplar-free analytic-learning method for audio-visual class-incremental tasks. |
| 2023 | Audio-Visual Class-Incremental Learning | ICCV | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2308.11073) | Defines a core audio-visual class-incremental setting and benchmark. |

### Speaker-related Tasks and Speech Emotion Recognition

| Year | Title | Venue | Paper | TLDR |
|:-:|:-|:-|:-:|:-|
| 2024 | SeQuiFi: Mitigating Catastrophic Forgetting in Speech Emotion Recognition with Sequential Class-Finetuning | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2410.12567) | Studies class-sequential speech emotion recognition with forgetting mitigation. |
| 2023 | Continual Self-Supervised Domain Adaptation for End-to-End Speaker Diarization | SLT | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/slt54892.2023.10023195) | Adapts speaker diarization one conversation at a time using self-supervision. |
| 2022 | Dynamic Recognition of Speakers for Consent Management by Contrastive Embedding Replay | IEEE TNNLS | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/tnnls.2023.3317493) | Uses contrastive replay for dynamic speaker recognition in consent management. |
| 2021 | Internet of Emotional People: Towards Continual Affective Computing Cross Cultures via Audiovisual Signals | Future Generation Computer Systems | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1016/j.future.2020.08.002) | Extends affective computing across cultures using audiovisual continual learning. |
| 2021 | Efficient Continual Learning for Keyword Spotting and Speaker Identification | - | - | Studies efficient continual updates for small speech recognition and speaker-ID tasks. |
| 2010 | A GMM-Based Robust Incremental Adaptation with a Forgetting Factor for Speaker Verification | ICIC | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1007/978-3-642-14932-0_24) | Early incremental speaker-verification adaptation using an explicit forgetting factor. |

### Keyword Spotting and Spoken Language Understanding

| Year | Title | Venue | Paper | TLDR |
|:-:|:-|:-|:-:|:-|
| 2025 | Continual Speech Learning with Fused Speech Features | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2506.01496) | Studies cross-task continual speech learning using fused speech features. |
| 2024 | Evaluating and Improving Continual Learning in Spoken Language Understanding | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2402.10427) | Directly evaluates continual SLU forgetting and mitigation strategies. |
| 2025 | AnalyticKWS: Towards Exemplar-Free Analytic Class Incremental Learning for Small-footprint Keyword Spotting | ACL Findings | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.18653/v1/2025.findings-acl.728) | Uses analytic class-incremental learning for exemplar-free small-footprint KWS. |
| 2024 | Dark Experience for Incremental Keyword Spotting | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp49660.2025.10890228) | Adapts dark-experience replay ideas to incremental keyword spotting. |
| 2023 | Continual Contrastive Spoken Language Understanding | ACL Findings | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.18653/v1/2024.findings-acl.223) | Uses contrastive learning to improve continual spoken language understanding. |
| 2023 | Dual-Memory Multi-Modal Learning for Continual Spoken Keyword Spotting with Confidence Selection and Diversity Enhancement | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2023-613) | Maintains dual memories for multimodal continual KWS. |
| 2023 | Online Continual Learning in Keyword Spotting for Low-Resource Devices via Pooling High-Order Temporal Statistics | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2023-90) | Designs online KWS learning for low-resource devices. |
| 2023 | Sequence-Level Knowledge Distillation for Class-Incremental End-to-End Spoken Language Understanding | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2023-242) | Applies sequence-level distillation to class-incremental SLU. |
| 2023 | Conditional Online Learning for Keyword Spotting | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2305.13332) | Updates KWS models online only when conditions justify adaptation. |
| 2022 | An Investigation of the Combination of Rehearsal and Knowledge Distillation in Continual Learning for Spoken Language Understanding | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2023-198) | Empirically studies rehearsal plus distillation for continual SLU. |
| 2022 | Rainbow Keywords: Efficient Incremental Learning for Online Spoken Keyword Spotting | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2022-10500) | Provides an efficient online incremental-learning framework for KWS. |
| 2022 | Progressive Continual Learning for Spoken Keyword Spotting | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp43922.2022.9746488) | Uses progressive model growth to preserve old keywords. |
| 2022 | Exploring the Joint Use of Rehearsal and Knowledge Distillation in Continual Learning for Spoken Language Understanding | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2211.08161) | Preprint counterpart studying rehearsal and distillation for continual SLU. |
| 2020 | Two-Stage Textual Knowledge Distillation for End-to-End Spoken Language Understanding | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp39728.2021.9414619) | Distills textual knowledge into end-to-end SLU, useful for cross-modal transfer discussions. |

### Audio Classification and Acoustic Scenes

| Year | Title | Venue | Paper | TLDR |
|:-:|:-|:-|:-:|:-|
| 2026 | Incremental Learning for Audio Classification with Hebbian Deep Neural Networks | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2604.18270) | Explores Hebbian deep networks as a biologically inspired route to audio incremental learning. |
| 2025 | Online Incremental Learning for Audio Classification Using a Pretrained Audio Model | WASPAA | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/waspaa66052.2025.11230989) | Updates pretrained audio classifiers online with lightweight classifier changes. |
| 2025 | Max-Informative Unlabeled Sample Replay for Semi-Supervised Class-Incremental Learning in Audio Classification | JCC | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/jcc67032.2025.00019) | Selects informative unlabeled samples for replay in semi-supervised audio CIL. |
| 2025 | A Closer Look at Class-Incremental Learning for Multi-Label Audio Classification | IEEE/ACM TASLP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/taslpro.2025.3547233) | Re-examines multi-label audio CIL and its evaluation pitfalls. |
| 2025 | Few-Shot Class-Incremental Audio Classification Using Pseudo-Incrementally Trained Embedding Learner and Continually Updated Stochastic Classifier | IEEE/ACM TASLP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/taslpro.2025.3610050) | Combines pseudo-incremental embedding training with stochastic classifier updates. |
| 2024 | Domain-Incremental Learning for Audio Classification | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp49660.2025.10890481) | Studies domain-incremental shifts in general audio classification. |
| 2024 | Online Domain-Incremental Learning Approach to Classify Acoustic Scenes in All Locations | EUSIPCO | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.23919/eusipco63174.2024.10715156) | Handles location shifts in online acoustic scene classification. |
| 2024 | Fully Few-shot Class-incremental Audio Classification Using Expandable Dual-embedding Extractor | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2024-1758) | Expands dual embeddings for fully few-shot audio class increments. |
| 2024 | Improving Continual Learning of Acoustic Scene Classification via Mutual Information Optimization | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp48485.2024.10446846) | Uses mutual-information optimization to improve continual acoustic scene classification. |
| 2024 | Class-Incremental Learning for Multi-Label Audio Classification | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp48485.2024.10447952) | Establishes a class-incremental setting for multi-label audio tagging. |
| 2024 | Few-Shot Class-Incremental Audio Classification With Adaptive Mitigation of Forgetting and Overfitting | IEEE/ACM TASLP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/taslp.2024.3385287) | Balances forgetting and overfitting in few-shot audio class increments. |
| 2024 | Deep Generative Replay With Denoising Diffusion Probabilistic Models for Continual Learning in Audio Classification | IEEE Access | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/access.2024.3459954) | Uses diffusion-generated replay samples for audio classification. |
| 2023 | Online Continual Learning in Acoustic Scene Classification: An Empirical Study | Sensors | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.3390/s23156893) | Provides an empirical study of online continual acoustic scene classification. |
| 2023 | Few-Shot Class-incremental Audio Classification Using Stochastic Classifier | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2023-1610) | Introduces stochastic classifiers for few-shot audio class increments. |
| 2023 | Few-Shot Class-Incremental Audio Classification Using Dynamically Expanded Classifier With Self-Attention Modified Prototypes | IEEE Transactions on Multimedia | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/tmm.2023.3280011) | Expands classifiers dynamically with self-attention-modified prototypes. |
| 2023 | Few-Shot Class-incremental Audio Classification Using Adaptively-refined Prototypes | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2023-1380) | Refines prototypes adaptively for few-shot audio class increments. |
| 2023 | Few-Shot Class-Incremental Audio Classification via Discriminative Prototype Learning | Expert Systems with Applications | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1016/j.eswa.2023.120044) | Learns discriminative prototypes for audio FSCIL. |
| 2023 | Adapter Incremental Continual Learning of Efficient Audio Spectrogram Transformers | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2023-1189) | Adds adapters to Audio Spectrogram Transformers for efficient continual learning. |
| 2023 | Incremental Learning of Acoustic Scenes and Sound Events | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2302.14815) | Studies incremental learning jointly for acoustic scenes and sound events. |
| 2023 | Episodic Memory Based Continual Learning Without Catastrophic Forgetting for Environmental Sound Classification | Journal of Ambient Intelligence and Humanized Computing | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1007/s12652-023-04561-5) | Uses episodic memory for environmental sound classification. |
| 2022 | Task Incremental Learning With Static Memory for Audio Classification Without Catastrophic Interference | IEEE Consumer Electronics Magazine | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/mce.2022.3145724) | Uses static memory to avoid interference in task-incremental audio classification. |
| 2022 | Learning Representations for New Sound Classes With Continual Self-Supervised Learning | IEEE Signal Processing Letters | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/lsp.2022.3229643) | Learns representations for new sound classes through continual SSL. |
| 2021 | Few-Shot Continual Learning for Audio Classification | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp39728.2021.9413584) | Foundational few-shot continual audio classification paper. |
| 2019 | Continual Learning of New Sound Classes Using Generative Replay | WASPAA | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/waspaa.2019.8937236) | Uses generative replay to add new sound classes. |

### Sound Event Detection, Localization, and Bioacoustics

| Year | Title | Venue | Paper | TLDR |
|:-:|:-|:-|:-:|:-|
| 2025 | Learning Order Matters in Class-Incremental Learning for Sound Localization and Detection | EUSIPCO | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.23919/eusipco63237.2025.11226063) | Shows that task order strongly affects SELD class-incremental performance. |
| 2026 | Analytic Incremental Learning for Sound Source Localization with Imbalance Rectification | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2601.18335) | Uses analytic incremental learning with imbalance correction for sound source localization. |
| 2024 | Analytic Class Incremental Learning for Sound Source Localization with Privacy Protection | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2409.07224) | Frames sound source localization as privacy-preserving class-incremental learning. |
| 2024 | Class-Incremental Learning for Sound Event Localization and Detection | ICASSPW | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icasspw65056.2025.11011278) | Establishes class-incremental learning for SELD. |
| 2024 | UCIL: An Unsupervised Class Incremental Learning Approach for Sound Event Detection | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp49660.2025.10887631) | Adds unsupervised learning to class-incremental sound event detection. |
| 2024 | Where's That Voice Coming? Continual Learning for Sound Source Localization | ICME | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icme59968.2025.11209062) | Studies continual sound source localization as sources/classes evolve. |
| 2024 | Double Mixture: Towards Continual Event Detection from Speech | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2404.13289) | Uses a mixture-based approach for continual event detection from speech. |
| 2023 | FEW-Shot Continual Learning with Weight Alignment and Positive Enhancement for Bioacoustic Event Detection | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp49357.2023.10096307) | Adapts few-shot continual learning to bioacoustic event detection. |

### Audio Deepfake Detection

| Year | Title | Venue | Paper | TLDR |
|:-:|:-|:-|:-:|:-|
| 2025 | Continual Audio Deepfake Detection via Universal Adversarial Perturbation | APSIPA ASC | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/apsipaasc65261.2025.11249335) | Uses universal adversarial perturbations for continual audio deepfake detection. |
| 2025 | Rehearsal with Auxiliary-Informed Sampling for Audio Deepfake Detection | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2025-2298) | Improves deepfake replay by selecting auxiliary-informed samples. |
| 2025 | Listen, Analyze, and Adapt to Learn New Attacks: An Exemplar-Free Class Incremental Learning Method for Audio Deepfake Source Tracing | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2025-16) | Adds new spoofing-source classes without storing exemplars. |
| 2025 | Continual Unsupervised Domain Adaptation for Audio Deepfake Detection | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp49660.2025.10890538) | Adapts fake-audio detectors to new unlabeled domains. |
| 2025 | What Affects the Performance of Fake Audio Detection? Analyzing Factors in a Continual Learning Setting | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp49660.2025.10888114) | Analyzes what factors govern fake-audio detector performance under continual updates. |
| 2024 | Region-Based Optimization in Continual Learning for Audio Deepfake Detection | AAAI | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1609/aaai.v39i22.34535) | Optimizes discriminative regions to retain old fake-audio attack knowledge. |
| 2024 | Advancing Continual Learning for Robust Deepfake Audio Classification | TENCON | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/tencon61640.2024.10902761) | Applies continual-learning methods to robust fake-audio classification. |
| 2024 | Freeze and Learn: Continual Learning with Selective Freezing for Speech Deepfake Detection | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp49660.2025.10889357) | Selectively freezes detector components while learning new spoofing attacks. |
| 2023 | What to Remember: Self-Adaptive Continual Learning for Audio Deepfake Detection | AAAI | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1609/aaai.v38i17.29929) | Learns what past samples or features matter most for deepfake retention. |
| 2023 | Do You Remember? Overcoming Catastrophic Forgetting for Fake Audio Detection | ICML | - | Studies catastrophic forgetting in fake-audio detection. |
| 2023 | Adaptive Fake Audio Detection with Low-Rank Model Squeezing | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2306.04956) | Uses low-rank model squeezing for adaptive fake-audio detection. |
| 2021 | Continual Learning for Fake Audio Detection | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2021-794) | Early continual-learning study for fake-audio detection. |

### Audio Captioning, Separation, Enhancement, and Audio-Text Learning

| Year | Title | Venue | Paper | TLDR |
|:-:|:-|:-|:-:|:-|
| 2026 | CORD: Bridging the Audio-Text Reasoning Gap via Weighted On-policy Cross-modal Distillation | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2601.16547) | Uses on-policy cross-modal distillation to improve audio-text reasoning. |
| 2025 | Continual Learning for Singing Voice Separation with Human in the Loop Adaptation | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2512.02432) | Brings continual learning to singing voice separation with human-guided adaptation. |
| 2025 | TAIL: Text-Audio Incremental Learning | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2503.04258) | Defines incremental learning for text-audio models. |
| 2024 | Continual Audio-Visual Sound Separation | NeurIPS | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.52202/079017-2421) | Studies sound separation when audio-visual mixtures arrive sequentially. |
| 2024 | Lifelong Learning MOS Prediction for Synthetic Speech Quality Evaluation | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2024-959) | Treats MOS prediction as a lifelong learning task for evolving synthetic speech. |
| 2024 | Learning Noise Adapters for Incremental Speech Enhancement | IEEE Signal Processing Letters | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/lsp.2024.3482171) | Adds noise-specific adapters for incremental speech enhancement. |
| 2023 | Universal Sound Separation Using Replay-based Data Sampling in Incremental Learning | APSIPA ASC | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/apsipaasc58517.2023.10317582) | Uses replay-based sampling for incremental universal sound separation. |
| 2023 | DeCoR: Defy Knowledge Forgetting by Predicting Earlier Audio Codes | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2023-2297) | Preserves audio knowledge by predicting earlier audio codes during updates. |
| 2021 | Continual Self-Training With Bootstrapped Remixing For Speech Enhancement | ICASSP | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.1109/icassp43922.2022.9747463) | Uses bootstrapped remixing for continual self-training in speech enhancement. |
| 2021 | Continual Learning for Automated Audio Captioning Using The Learning Without Forgetting Approach | arXiv | [![Paper](https://img.shields.io/badge/Paper-A42C25?style=for-the-badge&logo=arxiv&logoColor=white)](https://arxiv.org/abs/2107.08028) | Applies learning-without-forgetting to automated audio captioning. |
| 2020 | SERIL: Noise Adaptive Speech Enhancement Using Regularization-based Incremental Learning | INTERSPEECH | [![Paper](https://img.shields.io/badge/Paper-1F4E79?style=for-the-badge)](https://doi.org/10.21437/interspeech.2020-2213) | Early regularization-based incremental learning method for speech enhancement. |

## Acknowledgment

We are deeply grateful to all contributors for their efforts, and we sincerely thank them for their interest in **Awesome Speech and Audio Continual Learning**. 

## ✨ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=swagshaw/Awesome-Speech-and-Audio-Continual-Learning&type=Date)](https://www.star-history.com/#swagshaw/Awesome-Speech-and-Audio-Continual-Learning&Date)
