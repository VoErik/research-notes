# Paper: ye_et_al_2025_efficient_and_asymptotically_unbiased_constrained_decoding_for_large_language_models
* **Date:** 12/03/2026
* **Source:** 
  * **Link**: [Ye et al. 2025: Efficient and Asymptotically Unbiased Constrained Decoding for Large Language Models](https://arxiv.org/pdf/2504.09135)
  * **Code Repo:** [https://github.com/YWolfeee/Large-Scale-Selection-for-LLMs](https://github.com/YWolfeee/Large-Scale-Selection-for-LLMs)

## 📝 Summary

This paper identifies the danger of biased output distributions induced by constraining methods. To alleviate this, they propose the DISC algorithm that asymptotically unbiases the generated sequences (i.e., if the algorithm cannot guarantee an unbiased sequence it will at least guarantee the least biased sequence). Additionally, they propose PPV which makes token sampling more computationally efficient.

## 💡 Thoughts & Analysis
* constraining introduces biases into the output distribution
* these biases stem from the unawareness of future constraints during autoregressive decoding: model selects trajectories that have high probability in the first generated tokens, but then are forced into selecting low probability tokens due to constraining --> thus the generated trajectory does not reflect the actual model reasoning capabilities / language generation patterns
* they also note that current implementations of constraining are inefficient computationally because they are implemented on the cpu and do not transfer well to the gpu --> questionable if that is still the case
* they propose DISC (Dynamic Importance Sampling Algorithm for Constrained Decoding) and PPV (Parallel Prefix Verfification). DISC is unbiased with a fixed expected sampling size; this ensures compliance with constraints
* they focus on set constraints, i.e., sets of predefined allowed sequences


