# CONAN-MT-SP

CONAN-SP is a a new dataset for Spanish counter-narrative. It include a hate-speech comment (HS) and the corresponded counter-narrative (CN). 

# How is constructed?

The English CONAN Multitarget (CONAN-MT) corpus ([Margherita Fanton et al. , 2021](https://aclanthology.org/2021.acl-long.250.pdf) is taken as a starting point and an automatic translation is carried out using the API of DeepL to obtain the CONAN-MT-SP (CONAN Multitarget in Spanish) corpus.  CONAN-MT consists of 5003 HS-CN pairs covering multiple hate targets (DISABLED, JEWS, LGBT+, MIGRANTS, MUSLIMS, PEOPLE OF COLOR (POC), WOMEN)

GPT-4 model based on GPT technologies, is applied to the HS part of this corpus, which is provided as prompting together with 8 ContraNarrative (CN) examples.

Each instance of the corpus consists of the HS and CN part translated directly into Spanish with DeepL from the CONAN Multitarget corpus, plus the CN generated by GPT4. In addition, evaluations by human experts have also been included as part of the CONAN-MT-SP corpus. 

To construct CONAN-MT-SP, we remove the pairs that contain duplicates of hate-speech texts and the examples used in the prompt for the model to generate the counter-narrative. The prompt strategy used in GPT-4 model consist in a task description and 8 examples of HS-CN pairs (one for each target).

![CONAN-MT-SP scheme](https://github.com/sinai-uja/CONAN-MT-SP/blob/main/CONAN-MT-SP.png)

The structure of CONAN-MT-SP is the hate-speech and counternarrative provided by CONAN-MT and the counter-narrative texts generated by GPT-4 model. We do not apply any filter to the CN generated by GPT-4. Furthermore, we associated the values of the different metrics used in the manual evaluation carried by humans.

The evaluation metrics are:
- Offensiveness:  
	- 0 (not sure)  
	- 1 (not offensive)  
	- 2 (maybe offensive)  
	- 3 (completely offensive)  
- Stance:  
	- 0 (irrelevant)  
	- 1 (strongly agree)  
	- 2 (slightly agree/disagree)  
	- 3 (strongly disagree)  
- Informativeness: 
	- 0 (irrelevant)  
	- 1 (not informative)  
	- 2 (generic and uninformative statement)  
	- 3 (specific and informative)  
- Truthfulness:  
	- 0 (not sure)  
	- 1 (not true)  
	- 2 (partially true)  
	- 3 (completely true)
- Editing required: 
	- 0 (no editing)  
	- 1 (yes editing)  
- Comparison between H-M:  
	- 0 (both CN are equally valid)  
	- 1 (human generates a better CN)  
	- 2 (machine generates a better CN)  
	- 3 (neither CN is good)
# Citation
   María Estrella Vallecillo Rodríguez, María Victoria Cantero Romero, Isabel Cabrera De Castro, Arturo Montejo Ráez and María Teresa Martín Valdivia (2024). CONAN-MT-SP: A Spanish Corpus for Counternarrative using GPT Models. In Proceedings of The Joint International Conference on Computational Linguistics, Language Resources and Evaluation (LREC-COLING 2024). Torino (Italia) on 20-25 May, 2024 (Accepted and pending publication).
