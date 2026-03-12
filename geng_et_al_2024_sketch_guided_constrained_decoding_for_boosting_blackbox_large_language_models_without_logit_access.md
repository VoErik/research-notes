# Paper: geng_et_al_2024_sketch_guided_constrained_decoding_for_boosting_blackbox_large_language_models_without_logit_access
* **Date:** 12/03/2026
* **Source:** 
  * **Link**: [Geng et al. 2024: Sketch-Guided Constrained Decoding for Boosting Blackbox Large Language Models without Logit Access](https://arxiv.org/pdf/2401.09967)
  * **Code Repo:** [https://github.com/epfl-dlab/SketchGCD](https://github.com/epfl-dlab/SketchGCD)

## 📝 Summary

This paper tackles the problem of non-available token distributions by using a surrogate model that takes the outputs of the original model as input and then constraining that.

## 💡 Thoughts & Analysis

* This introduces another model call.
* This requires the surrogate model to have at least some power - the question is: how much weaker can the surrogate model be? They use a 7B param model -- while this is smaller than the sketcher (blackbox model), for which they test GPT-4, 3.5 Turbo, Claude and Claude-instant; 7B parameters are quite substantial. Can we go even smaller? Since the task is *only* refining the output of a stronger model such that it adheres to a given grammar.
* Increasing the size of the constrained decoding model does not always improve performance -- they do not provide an explanation for this (beyond some non-convincing intuition)
* They stress the importance of beam search over greedy decoding -- this could be interesting for the tool calling scenario?

