# Disease Classification in Corn Crops

**Throughout the project Jupyter notebook, I provide detailed comments with insights and explanations about the techniques and methodologies used and how they impact the solution.**

This project uses a VGG16 network with fine-tuning, regularization, dual pooling, dense attention layers, and several techniques such as **data augmentation**.  
Additionally, this project employs **Grad-CAM** to generate interpretable visualizations highlighting the most important image regions that influenced the network’s decision.  
The network was trained to classify leaf images into four classes:

<div style="display: flex; justify-content: center;">  
	<table style="border-collapse: collapse; width: 60%; text-align: center; font-size: 16px;">  
		<tr style="background-color: #f2f2f2;">  
			<th style="border: 1px solid #ddd; padding: 10px;">Class</th>  
			<th style="border: 1px solid #ddd; padding: 10px;">Description</th>  
		</tr>  
		<tr>  
			<td style="border: 1px solid #ddd; padding: 10px;">healthy</td>  
			<td style="border: 1px solid #ddd; padding: 10px;">Corn leaves with no visible signs of disease.</td>  
		</tr>  
		<tr style="background-color: #f9f9f9;">  
			<td style="border: 1px solid #ddd; padding: 10px;">cercospora</td>  
			<td style="border: 1px solid #ddd; padding: 10px;">Gray Leaf Spot (Cercospora zeae-maydis).</td>  
		</tr>  
		<tr>  
			<td style="border: 1px solid #ddd; padding: 10px;">rust</td>  
			<td style="border: 1px solid #ddd; padding: 10px;">Corn Rust (Puccinia sorghi or Puccinia polysora).</td>  
		</tr>  
		<tr style="background-color: #f9f9f9;">  
			<td style="border: 1px solid #ddd; padding: 10px;">northern_leaf_blight</td>  
			<td style="border: 1px solid #ddd; padding: 10px;">Northern Leaf Blight (Exserohilum turcicum).</td>  
		</tr>  
	</table>  
</div>   

---

### Dataset Structure

```
datasets/
├── train/
│ ├── healthy/
│ ├── cercospora/
│ ├── rust/
│ └── northern_leaf_blight/
├── val/
│ ├── healthy/
│ ├── cercospora/
│ ├── rust/
│ └── northern_leaf_blight/
```

---

### Dataset Distribution
<p align="center">
 <img src="https://github.com/phaa/corn-diseases-detection/blob/main/dev/images/distribuicao.png" title="Dataset Distribution" width="800" />
</p>

---

## Results

The model achieved **very high accuracy**, with excellent validation metrics. Confusion matrices and visual prediction examples were also generated to qualitatively evaluate the model.

### Validation Predictions
<p align="center">
 <img src="https://github.com/phaa/corn-diseases-detection/blob/main/dev/images/predicoes.png" title="Predictions" width="800" />
</p>

### Classification Report and Confusion Matrix 
<p align="center">
 <img src="https://github.com/phaa/corn-diseases-detection/blob/main/dev/images/resultados.png" title="Results" width="800" />
</p>

---

## Techniques Used
**Throughout the project notebook, I leave detailed insights and comments about the techniques and methodologies used and their impact on the solution.**

- Pretrained VGG16 (ImageNet)
- Fine-tuning of final layers
- Data Augmentation with `ImageDataGenerator`
- Dual Pooling (Average + Max)
- L2 Regularization + BatchNormalization
- Attention mechanism Layers
- Grad-CAM for visual interpretation
- Visualization with OpenCV and Matplotlib

**Main technologies:**
- TensorFlow
- Keras
- NumPy
- Pandas
- OpenCV
- Matplotlib

---

## Applications
This project demonstrates how Computer Vision combined with Deep Learning can improve productivity, reduce incorrect pesticide usage, and minimize crop losses due to diseases.

- Precision Agriculture
- Automated monitoring via drones
- Prescription of correct agrochemicals
- Mitigation of human diagnostic errors

---

## Why is this project relevant for agriculture?
The development of an automated plant disease classification system is highly relevant to agriculture due to several practical and economic reasons:

- Complexity of pathogen study: Fungi and bacteria affecting crops have complex life cycles with multiple stages that must be understood to manage diseases effectively.
- Prevention and remediation: Proper disease management relies on prevention, which is more cost-effective and efficient than treatment after symptoms appear.
- Reliable diagnostics: Farmers often face misdiagnoses, leading to trial-and-error treatment, increasing costs and risks.
- Importance of early detection: Identifying diseases in their early stages is crucial to prevent progression and yield loss.
- Avoiding phytotoxicity: Proper dosing (spray volume, droplet size, coverage proportion) is necessary to avoid damaging plants with agrochemicals.
- Optimization of agrochemical use: Each curative application could often be replaced by preventive applications, improving sustainability and reducing expenses.

This system helps farmers identify diseases accurately and quickly, guiding appropriate interventions that save resources, reduce errors, and increase crop productivity.

---

## How to run

### 1. Clone this repo

```bash
git clone https://github.com/phaa/corn-diseases-detection.git
cd corn-diseases-detection
```

### 2. Activate your env

```bash
conda activate env
```

### 3. Open Jupyter lab

```bash
jupyter lab
```

### 4. Run the notebook

All dependencies are installed directly via the notebook.

## Author

Developed by <a href='https://www.linkedin.com/in/pedro-henrique-amorim-de-azevedo/' target='_blank'>Pedro Henrique Amorim de Azevedo</a>

---
