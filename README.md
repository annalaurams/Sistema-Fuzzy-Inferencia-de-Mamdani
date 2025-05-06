# Sistema Fuzzy para Controle de Ventilação em Ambientes Fechados

Este projeto implementa um sistema de inferência fuzzy baseado no modelo de Mamdani para controle da ventilação em ambientes fechados. As variáveis de entrada são:

- Temperatura (baixa, média, alta)
- Umidade (baixa, média, alta)
- Número de pessoas (poucas, média, muitas)

A saída é a **intensidade da ventilação**: fraca, moderada ou forte.

## Sobre o Projeto

Este sistema fuzzy utiliza funções de pertinência trapezoidais para representar conjuntos linguísticos como "baixa", "média" e "alta". A função trapezoidal foi implementada manualmente em Python:

```python
def trapezoidal(x, a, b, c, d):
    return np.maximum(
        np.minimum(np.minimum((x - a) / (b - a + 1e-6), 1), (d - x) / (d - c + 1e-6)),
        0
    )
```

Essa função é utilizada para todas as variáveis fuzzy de entrada (temperatura, umidade, número de pessoas) e de saída (intensidade da ventilação).

## Funcionalidades

- Permite variação dos operadores lógicos AND (min, produto) e OR (max, soma)
- Visualização gráfica do grau de ativação (α) de cada regra fuzzy
- Suporte a técnicas de defuzzificação: centroide, bissetriz e média do máximo


## Como Executar

Este projeto foi desenvolvido e testado em um ambiente Jupyter Notebook (`.ipynb`). Para rodar localmente:

```bash
pip install notebook numpy matplotlib
jupyter notebook
```

E abra o arquivo `.ipynb` diretamente no navegador.

> Alternativamente, você pode usar o [Google Colab](https://colab.research.google.com/) para execução online.

## Autores e Contato

<div>
 <p align="justify"><strong>Anna Laura Moura Santana</strong></p>
 <a href="https://t.me/">
 <img align="center" src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white"/> 
 </a>
</div>
<a style="color:black" href="mailto:nalauramoura@gmail.com?subject=[GitHub]%20Source%20Dynamic%20Lists">
✉️ <i>nalauramoura@gmail.com</i>
</a>

<div>
 <br><p align="justify"><strong>Letícia de Oliveira</strong></p>
 <a href="https://t.me/letolsilva">
 <img align="center" src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white"/> 
 </a>
</div>
<a style="color:black" href="mailto:letolsilva22@gmail.com?subject=[GitHub]%20Source%20Dynamic%20Lists">
✉️ <i>letolsilva22@gmail.com</i>
</a>

<div>
 <br><p align="justify"><strong>Lucas Lima de Oliveira</strong></p>
 <a href="https://t.me/">
 <img align="center" src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white"/> 
 </a>
</div>
<a style="color:black" href="mailto:lucaslimadeoliveira80@gmail.com?subject=[GitHub]%20Source%20Dynamic%20Lists">
✉️ <i>lucaslimadeoliveira80@gmail.com</i>
</a>