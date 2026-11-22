# Modelagem Matemática do Lançamento de um Foguete

Projeto da Global Solution (FIAP), feito em um Jupyter Notebook com NumPy e Matplotlib. O objetivo é propor dois modelos matemáticos simples para fenômenos de um lançamento e interpretar os modelos usando derivadas.

## 1. Pressão aerodinâmica ao longo do tempo

Modelo:

$$P(t) = 7{,}2 \cdot t \cdot e^{-0{,}04t}, \quad t \ge 0$$

- Começa em zero no lançamento, cresce, atinge um pico e depois cai.
- Derivando, $P'(t) = 0$ dá o ponto de pressão máxima (Max Q) em $t^* = 1/k = 25$ s.
- O notebook plota a curva e marca o Max Q.

## 2. Risco de falha em função da temperatura

Modelo:

$$R(T) = 0{,}02 + 0{,}60 \cdot e^{-0{,}08(T-20)}$$

- O risco é maior no frio (referência: o problema dos O-rings no Challenger) e cai com o aumento da temperatura.
- Existe um risco residual de 2% (assíntota horizontal).
- $R'(T) < 0$ em todo o domínio, ou seja, o risco sempre diminui quando a temperatura sobe.

## 3. Validação

O notebook define o domínio e as unidades de cada modelo e interpreta o sinal das derivadas. Por fim, verifica se o comportamento faz sentido físico.

> Os parâmetros foram escolhidos para representar o comportamento esperado. Não foram usados dados reais de telemetria.

## Tecnologias

- Python 3
- NumPy
- Matplotlib
- Jupyter Notebook

## Como executar

```bash
pip install numpy matplotlib jupyter
jupyter notebook analise.ipynb
```

## Autor

Kayo Henderson, Ciência da Computação, FIAP.
