# Actividad 05: Clustering jerárquico, PCA y NMF

**Universidad Nacional del Altiplano Puno · Ingeniería de Sistemas**  
**Curso:** Aprendizaje de Máquina · Semestre IX  
**Docente:** Ing. Mayenka Fernández Chambi

**Integrantes:** Katherine Megumi Flores Tito; Cristian Alexis Loza Torres; Roger Golber Mamani Panca

**Repositorio:** https://github.com/lozatorrescristianalexis-debug/actividad05-linkage-pca-nmf

## Casos y resultados

| Caso | Método y datos | Resultado |
|---|---|---|
| 1 | Clustering jerárquico de 20 Newsgroups; cuatro linkages | `ward` fue el mejor (ARI 0.260, NMI 0.366), aunque la pureza global fue 59.2%. `single` reunió 99.3% de los documentos en su cluster mayor. |
| 2 | Eigenfaces con PCA en Olivetti Faces; 1-NN y SVM | Prueba: píxeles + 1-NN 92.5%, PCA (40 componentes) + 1-NN 91.2%, PCA + SVM 98.8% (79/80). |
| 3 | Recomendación con NMF y coseno en 20 Newsgroups | Precisión@5: NMF (20 temas) 44.7%, TF-IDF directo 63.4%, azar 5.1%. TF-IDF obtuvo el mejor resultado en esta métrica. |

En Eigenfaces usamos PCA y clasificadores clásicos, sin redes neuronales. En el caso NMF, algunos componentes son genéricos o poco claros.

## Ejecución

Cada integrante puede trabajar con la herramienta que tenga disponible: Jupyter Notebook, Visual Studio Code o Google Colab. Instalen las dependencias en el entorno que usará cada uno:

```bash
pip install -r requirements.txt
```

Después, abran y ejecuten los cuadernos, uno por uno, en este orden:

1. `caso1_clustering_jerarquico.ipynb`
2. `caso2_eigenfaces_pca.ipynb`
3. `caso3_recomendador_nmf.ipynb`

## Estructura

```text
README.md
.gitignore
requirements.txt
Informe_Actividad05.pdf
caso1_clustering_jerarquico.ipynb
caso2_eigenfaces_pca.ipynb
caso3_recomendador_nmf.ipynb
resultados/   # métricas JSON de los tres casos
figuras/      # gráficos de los tres casos
```
