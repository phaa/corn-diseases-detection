# 🌿 Classificação de Doenças em lavouras de milho

Este projeto utiliza uma rede VGG16 com fine-tuning, regularização, pooling duplo, camada de atenção densa e diversas técnicas como **data augmentation**. 
Além disso, esse projeto utiliza **Grad-CAM** para gerar visualizações interpretáveis das regiões mais importantes da imagem que influenciaram a decisão da rede. 
A rede foi treinada para classificar imagens de folhas em quatro classes:

<div style="display: flex; justify-content: center;">  
	<table style="border-collapse: collapse; width: 60%; text-align: center; font-size: 16px;">  
		<tr style="background-color: #f2f2f2;">  
			<th style="border: 1px solid #ddd; padding: 10px;">Classe</th>  
			<th style="border: 1px solid #ddd; padding: 10px;">Descrição</th>  
		</tr>  
		<tr>  
			<td style="border: 1px solid #ddd; padding: 10px;">saudavel</td>  
			<td style="border: 1px solid #ddd; padding: 10px;">Folhas de milho sem sinais visíveis de doenças.</td>  
		</tr>  
		<tr style="background-color: #f9f9f9;">  
			<td style="border: 1px solid #ddd; padding: 10px;">cercospora</td>  
			<td style="border: 1px solid #ddd; padding: 10px;">Mancha Cinzenta da Folha (Cercospora zeae-maydis).</td>  
		</tr>  
		<tr>  
			<td style="border: 1px solid #ddd; padding: 10px;">ferrugem</td>  
			<td style="border: 1px solid #ddd; padding: 10px;">Ferrugem do Milho (Puccinia sorghi ou Puccinia polysora).</td>  
		</tr>  
		<tr style="background-color: #f9f9f9;">  
			<td style="border: 1px solid #ddd; padding: 10px;">queima_do_norte</td>  
			<td style="border: 1px solid #ddd; padding: 10px;">Queima do Norte (Exserohilum turcicum).</td>  
		</tr>  
	</table>  
</div>   

---


### Estrutura do dataset

```
datasets/
├── train/
│   ├── saudavel/
│   ├── cercospora/
│   ├── ferrugem/
│   └── queima_do_norte/
├── val/
│   ├── saudavel/
│   ├── cercospora/
│   ├── ferrugem/
│   └── queima_do_norte/
```

---

### Distribuição do dataset
<p align="center">
 <img src="https://github.com/phaa/corn-diseases-detection/blob/main/dev/images/distribuicao.png" title="book" width="800" />
</p>

---

## Resultados

O modelo obteve **altíssima acurácia**, com excelente desempenho nas métricas de validação. Também foram geradas **matrizes de confusão** e **exemplos visuais preditivos** para avaliar qualitativamente o modelo.

### Predições de validação
<p align="center">
 <img src="https://github.com/phaa/corn-diseases-detection/blob/main/dev/images/predicoes.png" title="book" width="800" />
</p>

### Relatório de classificação e matriz de confusão 
<p align="center">
 <img src="https://github.com/phaa/corn-diseases-detection/blob/main/dev/images/resultados.png" title="book" width="800" />
</p>

---

## Técnicas Usadas
**Ao longo do projeto, deixo vários comentários com insights e comentários a respeito das escolhas feitas ao longo do projeto e como elas impactam a solução.**

- VGG16 pré-treinada (ImageNet)
- Fine-tuning das camadas finais
- Data Augmentation com `ImageDataGenerator`
- Pooling duplo (Average + Max)
- Regularização L2 + BatchNormalization
- Camadas de Atenção Densa
- Grad-CAM para interpretação visual
- Visualização com OpenCV e Matplotlib

**Tecnologias principais:**
- TensorFlow
- Keras
- NumPy
- Pandas
- OpenCV
- Matplotlib

---

## ✅ Aplicações
Esse projeto demonstra como a Visão Computacional aliada ao Deep Learning pode melhorar a produtividade, reduzir o uso de defensivos incorretamente e minimizar perdas por doenças.

- Agricultura de Precisão
- Monitoramento automatizado por drones
- Prescrição de defensivos agrícolas corretos
- Mitigar erros de diagnóstico por humanos

---


## Como executar

### 1. Clone o repositório

```bash
git clone https://github.com/phaa/corn-diseases-detection.git
cd corn-diseases-detection
```

### 2. Inicie seu ambiente

```bash
conda activate env
```

### 3. Abra o Jupyter lab

```bash
jupyter lab
```

### 4. Execute o notebook
Todas as dependencias são instaladas diretamente pelo notebook

## Créditos

Desenvolvido com ❤️ por <a href='https://www.linkedin.com/in/pedro-henrique-amorim-de-azevedo/' target='_blank'>Pedro Henrique Amorim de Azevedo</a>

---
