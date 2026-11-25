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
| 2 | Eigenfaces con PCA en Olivetti Faces y búsqueda por distancia | PCA (62 componentes): euclídea top-1 74/80 (92.5%) y top-5 78/80 (97.5%); coseno top-1 73/80 (91.2%) y top-5 75/80 (93.8%). Píxeles crudos, euclídea: 74/80 (92.5%) y 78/80 (97.5%). Agrupamiento ward: ARI 0.526, NMI 0.825; K-means: ARI 0.451, NMI 0.785. |
| 3 | Recomendación con NMF y coseno en 20 Newsgroups | Precisión@5: NMF (20 temas) 44.7%, TF-IDF directo 63.4%, azar 5.1%. TF-IDF obtuvo el mejor resultado en esta métrica. |

En Eigenfaces, PCA y los agrupamientos no supervisados se ajustan sin etiquetas; las etiquetas solo se usan para evaluar. La identidad devuelta es la del rostro de galería más cercano; no entrenamos un modelo de clasificación ni usamos redes neuronales. En el caso NMF, algunos componentes son genéricos o poco claros.

## Ejecución

Cada integrante puede ejecutar los cuadernos en Jupyter, Visual Studio Code o Google Colab, según su entorno. Instalen las dependencias en el entorno que usarán:

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
