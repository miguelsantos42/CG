# Transformações Geométricas 2D 

Existem 3 tipos de transformações geométricas: 
 - Translação;
 - Escalamento;
 - Rotação;

## 1. Translação
  
  - A **translação** em geometria é uma transformação que <u>desloca todas as coordenadas de uma figura</u> (ou de um ponto) por um mesmo vetor de translação 𝑇 = (𝑇𝑥,𝑇𝑦). Ou seja, cada ponto (x,y) de um objeto é mapeado para um novo ponto (𝑥′,𝑦′), onde:
    - 𝑥′ = 𝑥 + 𝑇𝑥 
    - 𝑦′ = 𝑦 + 𝑇𝑦

    Por exemplo: onde Tx = 3 e Ty = -4

    ![Translação](../Teóricas/Images/(Image1)Translação.png)

  
  - `Forma matricial (em coordenadas homogêneas):`
    Para representar a translação em forma de produto matricial, utiliza-se uma matriz de 3×3 (quando trabalhamos em 2D com coordenadas homogêneas):
    
    ![Forma Matricial](../Teóricas/Images/(Image2)TranslaçãoHomogenea.png)

## 2. Escalamento

O **escalamento** é uma transformação geométrica que <u>modifica o tamanho</u> (e possivelmente a orientação) de um objeto, multiplicando as coordenadas de cada ponto por fatores de escala ao longo dos eixos 𝑥 e 𝑦. Se chamarmos esses fatores de 𝑆𝑥 e 𝑆𝑦, então:
  - 𝑥′ = 𝑥 × 𝑆𝑥
  - 𝑦′ = 𝑦 × 𝑆𝑦

 
### Fatores de escala
  1. `𝑆𝑥 > 1 e/ou 𝑆𝑦 > 1`: o objeto é ampliado em relação ao(s) eixo(s) correspondente(s).
  2. `0 < 𝑆𝑥 < 1 e/ou 0 < 𝑆𝑦 < 1`: o objeto é reduzido em relação ao(s) eixo(s) correspondente(s).
  3. `𝑆𝑥 < 0 ou 𝑆𝑦 < 0`: além de redimensionar, ocorre uma reflexão (espelhamento) no eixo cujo fator é negativo.
  4. `𝑆𝑥 = 𝑆𝑦`: o escalamento é uniforme (isotrópico), ou seja, o objeto cresce ou diminui sem distorcer sua forma (mantém a proporção entre largura e altura).

### Exemplo:
 - Se `𝑆𝑥 = 2 e 𝑆𝑦 = 2`, o objeto é ampliado uniformemente para o dobro de seu tamanho original, mantendo a mesma forma.
 - Se `𝑆𝑥 = 2 e 𝑆𝑦 = −1.5`, o objeto é ampliado 2 vezes na direção 𝑥, e invertido (espelhado) no eixo 𝑦 e redimensionado em 1,5 vezes (em valor absoluto) na direção 𝑦.

  ![Escalamento](../Teóricas/Images/(Image3)Escalamento1.png)

Por padrão, o escalamento ocorre em relação à origem do sistema de coordenadas (0,0). Para escalonar em relação a outro ponto (𝑥0,𝑦0).

### Forma Matricial (em coordenadas homogêneas)
  Em 2D, podemos representar o escalamento em coordenadas homogêneas por uma matriz de 3×3 do tipo:
  ![Escalamento Homogéneo](../Teóricas/Images/(Image4)EscalamentoHomogeneo.png)

## 3. Rotação

A rotação em 2D é uma transformação geométrica que gira todos os pontos de um objeto em torno de um ponto fixo (normalmente a origem (0,0)) por um ângulo específico. Se chamarmos esse ângulo de 𝑏 as coordenadas (𝑥,𝑦) de cada ponto são transformadas em (𝑥′, 𝑦′)de acordo com:
  ![Rotação](../Teóricas/Images/(Image5)Rotação.png)

  - **Ângulo b positivo**: rotação no sentido anti-horário (contrário ao movimento dos ponteiros do relógio).
  - **Ângulo b negativo**: rotação no sentido horário.

### Forma Matricial:
  Em coordenadas cartesianas, podemos escrever a rotação em forma de produto matricial (utilizando coordenadas homogêneas, seria uma matriz 3×3, mas a ideia central em 2D é a mesma):
  ![Forma Matricial](../Teóricas/Images/(Image6)RotaçãoMatricial.png)

  Essa matriz de 2×2 gira o vetor (𝑥,𝑦) por um ângulo b em torno da origem.

-------------------------

A não comutatividade fica mais evidente quando combinamos:
    
    - translação + rotação,
    - translação + escala,
    - rotação + escala em torno de pontos distintos

Se as transformações forem todas translações ou todas rotações em torno do mesmo centro, então comutam. Mas, no caso de misturar rotação e translação, a ordem importa.

