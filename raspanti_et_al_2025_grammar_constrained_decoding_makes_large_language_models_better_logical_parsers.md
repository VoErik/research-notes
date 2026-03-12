# Paper: raspanti_et_al_2025_grammar_constrained_decoding_makes_large_language_models_better_logical_parsers
* **Date:** $(date +%Y-%m-%d)
* **Source:**
  * **Link**: [Raspanti et al. GCD Makes LLMs Better Logical Parsers](https://aclanthology.org/2025.acl-industry.34/)
  * **Code Repo:** [https://github.com/federaspa/gcd-llm-logical-parsing](https://github.com/federaspa/gcd-llm-logical-parsing)


## 📝 Summary
- 
This paper decouples LLM reasoning from constrained decoding as previous papers have shown that the reasoning ability degrades if the LLM is constrained.
They apply it for logical parsing, where the LLM only produces the input to the logical reasoning system. This way the actual reasoning is decoupled from the LLM.Their results indicate the GCD improves performance, especially for smaller models.


## 💡 Thoughts & Analysis
- 
* Test under different settings, I currently only consider 0-shot for BFCL, might also want to include few-shot.
* For larger models they observe that the unconstrained version occasionally outperforms the constrained version. This is in line with what I observed. The question remains why?
* They note the complementarity of GCD and ICL 

## 🔗 Related Work / References
* [Tam et al. 2024: Let Me Speak Freely? A Study on the Impact of Format Restrictions on Performance of Large Language Models](https://arxiv.org/pdf/2408.02442)
* [Geng et al. 2024: Sketch-Guided Constrained Decoding for Boosting Blackbox Large Language Models without Logit Access](https://arxiv.org/pdf/2401.09967)
* [Ye et al. 2025: Efficient and Asymptotically Unbiased Constrained Decoding for Large Language Models](https://arxiv.org/pdf/2504.09135)


