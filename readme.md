# Dataset Correspondence
CHME-HD -> hallucination.jsonl
CHME-DD -> diagnose.jsonl
CHME-CE -> mesh.jsonl

# Dataset Introduction
## CHME-HD
Each sample contains three fields: question, answer, and neg. The model needs to determine whether the answer contains incorrect information. Neg = True indicates that the answer contains incorrect information. Among the negative samples, the first 387 samples are generated samples, while the remaining 613 samples are tampered samples.

## CHME-DD
Each sample contains four fields: id, patient_info, disease, and icd-10. The model needs to predict the disease based on the patient_info. Users can differentiate the samples based on the id. To calculate the disease matching F1 score, you can run the script in the icd-10 folder to obtain the score.

## CHME-CE
This dataset contains three fields: questions, options, and answer. It is recommended to process it into the format in mesh_sample.jsonl for testing purposes.