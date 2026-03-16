# Paper: mohammadi_explaining_llm_decisions_using_shapley_values
* **Date:** 16.03.2026
* **Source:** 
  * **Link**: [Mohammadi (2024): Explaining Large Language Model Decisions Using Shapley Values](https://arxiv.org/pdf/2404.01332)
  * **Code Repo:** ---

## 📝 Summary

This paper uses a template based approach to create feature vectors that are then used for SHAP attribution. However, it seems to me that there is a misalignment as they force the templates to be on a word level -- whereas the model operates on a token level -- and the baseline vector is simply the original template without any values (they substitute " _ " as a default value). This creates an unnatural input for the LLM. Additionally, they claim to discover "token noise", where semantically irrelevant tokens have high SHAPley values. This neglects the nature of a transformer-based LM, where a token (or in their case: word) does not solely carry its own semantics, but is contextualized in the given context. All in all this paper kind of highlights the disconnect in the way the language models work vs. what we as humans need in terms of explanatory frameworks (e.g. token-based vs. word-based)

## 💡 Thoughts & Analysis

* Posed a binary decision problem (choose flight A or flight B), the LLM decision is unpredictably influenced by the addition of non-semantic newline tokens.
* Method: 
  * vectorize prompt --> prompt becomes a template that can be filled with arbitrary values, they use Jinja to replace only certain phrases in the prompt (not on a token level necessarily), the vector is then the filled in values (omitting the rest of the prompt), but then in sec. 3.2. they state that the arguments passed to the LLM is the prompt vector given the prompt template
## 🔗 Related Work / References
