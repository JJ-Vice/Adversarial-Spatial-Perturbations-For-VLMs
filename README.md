# On the Reliability of Vision-Language Models Under Adversarial Frequency-Domain Perturbations
![safety_without_semantic_disruptions](https://github.com/JJ-Vice/Adversarial-Spatial-Perturbations-For-VLMs/blob/main/high-level-fig_V3.png)

We explore how VLM outputs are influenced by changes in frequency domain features across two tasks: (i) authenticity detection and (ii) automated image captioning. Querying VLMs with unperturbed images (synthetic or real) may result in $P_r(I)$ prediction in-line with the ground truth (e.g. $P_r(I) = \frac{4}{10}$). However, subtle spatial frequency perturbations can induce unreliable VLM behavior, shifting the VLM output across the decision boundary ($P_r(I)=\frac{4 \rightarrow 8}{10}$).Likewise, perturbations are also applied to manipulate the quality of VLM-generated captions.

## Description
Vision-Language Models (VLMs) are increasingly deployed for tasks such as image captioning and DeepFake detection, but remain vulnerable to subtle, structured perturbations in the frequency domain. This project investigates how visually-imperceptible spatial frequency transformations can systematically alter VLM outputs under realistic black-box conditions. We design targeted frequency-domain perturbations that generalize across multiple state-of-the-art models (e.g., Qwen2/2.5, BLIP). Results reveal that VLM judgments often rely on frequency-based cues rather than pure semantic content, challenging their reliability in critical applications and underscoring the need for more robust multimodal perception systems.

This repository contains all code and data necessary to replicate experiments in the paper:

J. Vice, N. Akhtar, Y. Gao, R. Hartley and A. Mian, "On the Reliability of Vision-Language Models Under Adversarial Frequency-Domain Perturbations," ArXiv Preprint. Available at: https://arxiv.org/abs/2507.22398.


## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/JJ-Vice/Adversarial-Spatial-Perturbations-For-VLMs.git
cd Adversarial-Spatial-Perturbations-For-VLMs
```
### 2. Install dependencies
We recommend using a virtual environment (e.g., venv or conda) before installing.

This project is relatively lightweight. It mainly requires acess to torch and the HuggingFace transformers package to access models. PIL is used for image processing. In summary, the required packages (outside of basic Python-distributed packages) are:
- numpy
- pillow
- transformers
- qwen-vl-utils *(if Qwen VLM is the target model)*

We expose the reliability concerns in VLMs across two tasks:
1. Image Realism / DeepFake Detection, accessible via **Fooling_VLMS_Realness_<MODEL>.ipynb** notebooks
2. Automated Image Captioning, accessible via **Fooling_VLMS_Captioning_<MODEL>.ipynb** notebooks

We demonstrate the viability of our approach across BLIP and Qwen-based VLMs, providing necessary code books for each. We do not recommend adjusting the perturbation strength beyond a perceptible threshold. We purposefully constrain our perturbation severity such that **visual changes in adversarial images are imperceptible**. We provide a zoomed in example of this in the figure below.
![safety_without_semantic_disruptions](https://github.com/JJ-Vice/Adversarial-Spatial-Perturbations-For-VLMs/blob/main/high-level-fig_V3.png)



## Citation
If our code, metrics or paper are used to further your research, please cite our paper:
```BibTeX
@article{Vice2025Reliability,
      title={On the Reliability of Vision-Language Models Under Adversarial Frequency-Domain Perturbations}, 
      author={Jordan Vice and Naveed Akhtar and Yansong Gao and Richard Hartley and Ajmal Mian},
      year={2025},
      eprint={2507.22398},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2507.22398}, 
}
```

If you have any questions/queries or if you want to simply strike a conversation, please reach out to Jordan Vice at: jordan.vice@uwa.edu.au or raise an issue in the [Issues tab](https://github.com/JJ-Vice/Adversarial-Spatial-Perturbations-For-VLMs/issues)
