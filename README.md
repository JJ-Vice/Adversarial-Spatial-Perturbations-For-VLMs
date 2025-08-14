# On the Reliability of Vision-Language Models Under Adversarial Frequency-Domain Perturbations
![safety_without_semantic_disruptions](https://github.com/JJ-Vice/Adversarial-Spatial-Perturbations-For-VLMs/blob/main/high-level-fig_V3.png)

We explore how VLM outputs are influenced by changes in frequency domain features across two tasks: (i) authenticity detection and (ii) automated image captioning. Querying VLMs with unperturbed images (synthetic or real) may result in $P_r(I)$ prediction in-line with the ground truth (e.g. $P_r(I) = \frac{4}{10}$). However, subtle spatial frequency perturbations can induce unreliable VLM behavior, shifting the VLM output across the decision boundary ($P_r(I)=\frac{4 \rightarrow 8}{10}$).Likewise, perturbations are also applied to manipulate the quality of VLM-generated captions.


