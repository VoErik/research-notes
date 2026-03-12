# Paper: geng_et_al_2023_grammar_constrained_decoding_for_structured_nlp_tasks_without_finetuning
**Date:** $(date +%Y-%m-%d)
**Source:** **Code Repo:** [https://github.com/epfl-dlab/GCD](https://github.com/epfl-dlab/GCD)

## 📝 Summary
--- 
This paper deals with more classical NLP tasks and shows that the output spaces of them can be formulated using formal languages, which makes them amenable to grammar constrained decoding problems. Additionally, they introduce input dependent grammars because some tasks depend on the input sequence (e.g. entity disambiguation). They focus their experiments on closed information extraction, entity disambiguation, and constituency parsing. All experiments were done in a few-shot setting and show that GCD improves upon unconstrained LLM performance.


## 💡 Thoughts & Analysis
--- 
* A lot of things interesting currently are not classical NLP tasks, but instead focus on tool calling in agentic settings or producing easily parsable outputs.
* They observe a phenomenon where the most likely output token is an empty string (EOS token) which they attribute to a misalignment between the grammar and the language model stemming from the training objective of the LM (maximizing likelihood of human language)
* For constraining they prune the token distribution to only include the allowed tokens according to the grammar. This requires access to the token likelihood distribution at each decoding step.

## 🔗 Related Work / References
- 
