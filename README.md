
# 🚛 Otimizador de Carga de Caminhão com Algoritmo Genético

Este projeto implementa um **algoritmo genético** para resolver um problema real de **otimização logística**: escolher as melhores cargas a serem transportadas em um caminhão, visando **maximizar o valor total**, respeitando **limites de peso e volume**.

---

## 📌 Objetivo do Projeto

Selecionar a melhor combinação de cargas, dentre **500 opções aleatórias**, que maximize o **valor transportado**, **sem ultrapassar**:
- Peso máximo do caminhão: **30.000 kg**
- Volume máximo: **300 m³**

---

## ⚙️ Técnicas Utilizadas

### 🧬 Algoritmo Genético (AG)

O AG é inspirado na seleção natural, onde soluções evoluem ao longo das gerações. Ele foi implementado com os seguintes elementos:

| Componente        | Implementação                                      |
|-------------------|----------------------------------------------------|
| **Indivíduo**     | Vetor binário com 500 posições (1 = carga incluída) |
| **População**     | Grupo de soluções candidatas                       |
| **Fitness**       | Valor total das cargas incluídas, se viável        |
| **Seleção**       | Seleção dos N melhores indivíduos (elitismo)       |
| **Crossover**     | Corte aleatório entre dois pais                    |
| **Mutação**       | Inversão aleatória de genes com 10% de chance      |

---

## 🧩 Implementação Técnica

### 1. Geração de Cargas
Geramos **500 cargas aleatórias**, com peso, volume e valor baseados em uma lista realista de tipos de carga.

### 2. Representação dos Indivíduos
Cada indivíduo é um vetor binário. Apenas **5 a 30 cargas** são escolhidas aleatoriamente para cada indivíduo inicial, evitando sobrepeso.

### 3. Função de Fitness
Calcula o valor total das cargas incluídas, retornando 0 se ultrapassar peso/volume ou se valor < valor_minimo.

### 4. Evolução da População
A população evolui por 1000 gerações, com:
- Seleção dos **5 melhores** indivíduos.
- Crossover + Mutação para gerar novos indivíduos.
- Substituição da população antiga pela nova.

---

## 📈 Resultados

O algoritmo foi testado com:
- `peso_maximo = 30.000 kg`
- `volume_maximo = 300 m³`
- `valor_minimo = 50.000 R$`

O gráfico gerado mostra a evolução do valor (fitness) ao longo das gerações.

> 💡 Quanto maior o número de gerações, melhor a combinação de cargas encontrada.

---

## 🎥 Entrega e Demonstração

- **Vídeo explicativo**: [https://youtu.be/mCHXPoZ3OW8](#)

---

## 👨‍💻 Autores

Este projeto foi desenvolvido como parte do **Tech Challenge - Fase 2**.

Aluno: IGOR FANTICHELI OLIVEIRA rm364892

Aluno: LINCOLN ARAUJO DIAS rm364892
