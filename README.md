# Reconhecimento Facial com Deep Learning (DIO)

Este projeto implementa um sistema de **detecção e reconhecimento facial** do zero, utilizando Python, TensorFlow e Scikit-learn. O trabalho foi desenvolvido como desafio no curso de **Machine Learning da Digital Innovation One (DIO)**.

## 🚀 Tecnologias
- [TensorFlow](https://www.tensorflow.org/) — extração de embeddings (MobileNetV2)
- [MTCNN](https://pypi.org/project/mtcnn/) — detecção de rostos
- [Scikit-learn](https://scikit-learn.org/stable/) — classificador SVM
- [OpenCV](https://opencv.org/) — pré-processamento de imagens

## 📂 Estrutura do Projeto

- `faces_dataset/` → faces recortadas automaticamente com MTCNN  
- `train_faces/` e `val_faces/` → conjuntos de treino/validação estratificados  
- `FacialRecognition.ipynb` → notebook principal com todo o pipeline  

## 🧠 Pipeline
1. **Detecção de rostos** com MTCNN  
2. **Recorte e padronização** das imagens (160×160 px)  
3. **Extração de embeddings** com MobileNetV2 pré-treinada (ImageNet)  
4. **Treinamento de SVM** com GridSearch para classificação  
5. **Inferência** em imagens novas, com detecção + reconhecimento múltiplo  

## 📊 Resultados
- Dataset pequeno, expandido via **data augmentation**  
- **Acurácia de validação** próxima de 100% no conjunto gerado  
- Identificação funcionando em imagens com múltiplas faces  

## 📌 Melhorias Futuras
- Coletar mais imagens reais e variadas de cada classe  
- Usar modelos especializados em reconhecimento facial (ArcFace, FaceNet)  
- Implementar detecção de "desconhecido" com dataset negativo  

## ✨ Autor
Fabio Vinicius Guidotti — Desenvolvido como desafio do curso de Machine Learning (DIO).
