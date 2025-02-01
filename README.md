# **TOPSIS-Based Evaluation of Pre-trained Models for Text Generation**

## **Project Overview**
This project evaluates the performance of five advanced text generation models using the **TOPSIS (Technique for Order Preference by Similarity to Ideal Solution)** method. The evaluation considers multiple key performance metrics and ranks the models based on their overall effectiveness.

### **Evaluated Models**
The models assessed in this study include:
- **LLaMA-7B**
- **GPT-3.5-Turbo**
- **Mistral-7B**
- **Falcon-40B**
- **T5-Large**

## **Evaluation Criteria**
Each model is assessed based on the following criteria:

1. **Perplexity** - Measures how well the model predicts text (Lower is better)
2. **Generation Speed** - Words generated per second (Higher is better)
3. **Model Size (GB)** - The storage size of the model (Lower is better)
4. **Memory Usage (GB)** - RAM consumption during inference (Lower is better)
5. **BLEU Score** - Measures text generation quality (Higher is better)

A weighted decision matrix is used to quantify model performance based on these criteria.

## **Methodology**
1. **Data Collection**  
   - Performance data for each model is collected across the five evaluation criteria.

2. **Normalization**  
   - The decision matrix is normalized using **Min-Max Scaling** to standardize the values.

3. **Weighting & Decision Matrix Formation**  
   - Each criterion is assigned a weight to reflect its importance.

4. **TOPSIS Computation**  
   - Ideal best and worst values are determined.
   - Distance from ideal best and worst values is computed.
   - The **TOPSIS score** is calculated to rank models.

5. **Visualization & Report Generation**  
   - **Bar charts** and **Radar charts** visualize the performance.
   - The final ranked results are saved in a detailed report.

## **Installation & Dependencies**
To run the evaluation script, install the required Python libraries:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn plotly
```

## **Usage**
To run the evaluation, execute the following in Python:

```python
from model_evaluator import ModelEvaluator

evaluator = ModelEvaluator()
radar_plot, results = evaluator.plot_results()
full_report = evaluator.generate_report()

print("\nModel Rankings:")
print(results)

print("\nDetailed Analysis Report:")
print(full_report)

# Save results
radar_plot.write_html("model_comparison_radar.html")
```

## **Results & Insights**
![image](https://github.com/user-attachments/assets/789b605b-6337-4c9f-93c9-aa9a01d67236)
![image](https://github.com/user-attachments/assets/7a9c8b8c-1b7e-42b1-8e98-0f816c524baf)


## **Contributors**
- **BHAVYA**

## **License**
This project is licensed under the **MIT License**.


