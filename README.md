# TOPSIS-Based Evaluation for Text Summarization Models

## Overview
This project applies the **Technique for Order of Preference by Similarity to Ideal Solution (TOPSIS)** to rank five pre-trained text summarization models based on multiple evaluation criteria. The models compared are:

- **BART**
- **PEGASUS**
- **T5**
- **GPT-3**
- **LED**

## Criteria for Evaluation
The models are evaluated on the following criteria:

### Benefit Criteria:
- **ROUGE-1**: Measures the overlap of unigrams between the generated and reference summaries.
- **ROUGE-2**: Measures the overlap of bigrams.
- **ROUGE-L**: Measures the longest common subsequence.

### Cost Criteria:
- **Inference Time**: The time taken to generate summaries (lower is better).
- **Model Size**: The size of the model in MBs (lower is better).
- **FLOPs**: Floating Point Operations required for inference (lower is better).
- **Memory Usage**: RAM consumption during inference (lower is better).

## Methodology
1. **Decision Matrix Creation**: Hypothetical scores are assigned to each model.
2. **Normalization**: Data is normalized to account for different scales.
3. **Weight Assignment**: Weights are applied to reflect the importance of each criterion.
4. **Ideal and Negative-Ideal Solutions**: Determined for benefit and cost criteria.
5. **Separation Measures**: Calculated to measure each model's distance from the ideal and negative-ideal solutions.
6. **Closeness Coefficient**: Computed to rank the models.

## Results
The final rankings are based on the closeness coefficient, where a higher value indicates better performance relative to the ideal solution.

## How to Run
1. Ensure Python is installed with the following libraries:
   ```bash
   pip install numpy pandas 
   ```
2. Run the provided Python script.
3. Analyze the output and visualizations.

## Sample TOPSIS Rank Report
The script outputs a rank report showcasing:
- Model name
- Closeness coefficient
- Final rank

## License
This project is for academic and research purposes.

## Author
Sonal Kasana
