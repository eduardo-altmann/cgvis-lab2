# Relatório - Coelinhos do Brasil

> [!CAUTION]
> - Lembre-se que você <ins>**não pode utilizar ferramentas de IA para
>   escrever este relatório**</ins>

## Dados do aluno

- **Cartão UFRGS**: <mark>`594993`</mark>
- **Nome**: <mark>`Eduardo Altmann de Bem`</mark>

## Passos que eu segui para resolver o problema especificado (em formato de *"prompt"*)

> [!IMPORTANT]
> - Coloque aqui todas as informações necessárias para que alguém
>   (pessoa ou ferramenta de IA) possa reproduzir os seus passos para
>   solucionar o problema
> - Escreva em formato imperativo, como se fosse um *prompt* com as
>   instruções a serem seguidas na solução do problema
> - Seja objetivo e conciso: quanto *menos palavras* você utilizar,
>   melhor
> - Seja técnico e use terminologia adequada: assuma que quem irá ler
>   os seus passos possui conhecimento de Ciência da Computação e
>   Computação Gráfica
> - Caso você queira incluir informações "longas" (como algum *prompt*
>   grande usado com alguma ferramenta de IA), crie arquivos à parte e
>   adicione links no texto (por exemplo, crie o arquivo `PROMPTS.md`
>   e adicione um link markdown `[os prompts detalhados estão
>   aqui](PROMPTS.md)`)
> - Novamente, lembre-se que você *não pode utilizar ferramentas
>   de IA para escrever este relatório*

Ajuste o cenário: remova a esfera, amplie o plano, ajuste câmera e distância de renderização, definir escala dos coelhos e corrija altura para apoiar as patas no chão.

Crie uma função para organizar o desenho dos coelhos, ela deve receber posição, orientação, inclinação e material.  Isso facilita multiplicar os coelhos

Monte o retângulo estático dos verdes. Depois, monte o losango amarelo e o círculo azul. 24 verdes, 14 amarelos e 8 azuis. Todos eles distribuídos por distância ao longo dos contornos.

Faça os coelhos percorrerem as formas. Calcule o tempo em segundos para a velocidade não depender da taxa de quadros. Cada coelho começa de um ponto diferente, circulando no sentido horário, preservando contornos e espaçamento. Adicione velocidades diferentes por grupo, com aproximadamente o mesmo tempo de volta.

Ajuste a orientação dos coelhos na direção do movimento deles. Identifique a frente do modelo e gire-o ao redor do seu eixo vertical. No círculo deve acompanhar a tangente, no retângulo e losango mudar nas quinas.

Adicione os saltos: ciclo de subida, descida e contato com o chão, mantendo a posição horizontal sobre o percurso. Faça o ajuste fino de altura (0,85), duração (ciclo de 3s e alternância azul de meio ciclo)e sincronização. O salto deve ser parabólico com fases diferentes entre coelhos e alternância entre vizinhos azuis.

Adicione inclinação para frente e depois para trás: sincronizar a inclinação com o pulo e voltar à postura normal quando aterrissar. Usar um pivô próximo à base do coelho e aplicar a inclinação no seu sistema local para funcionar em todas as direções

Adicionar as boinas aos coelhos, feitas com esferas achatadas herdando as transformações dos coelhos.

## Principais dificuldades encontradas durante o desenvolvimento (formato livre)

Foi difícil implementar delay de pulo, tempo no ar, a diferença de fase entre vizinhos e a velocidade de deslocamento

A principal dificuldade foi conseguir reproduzir a dinâmica do pulo, com inclinação, primeiro para frente e depois para trás, de modo a ficar semelhante ao exemplo.

Além disso, sincronizar a velocidade dos coelhos de cada cor para ficar como o vídeo exemplo foi outra barreira.

De modo geral, pode-se dizer que foram necessárias muitas comparações com o vídeo e correções sucessivas


## Você acha que conseguiu resolver o problema de forma adequada?

Sim, creio que o resultado final ficou bem fiel ao vídeo exemplo, pois detalhes como inclinação, tempo de pulo, alternância entre coelhos no círculo azul foram todos minuciosamente ajustados.


