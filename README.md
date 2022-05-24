# Redes-Neurais-Artificiais
Introdução de conceitos, códigos exemplo.

* Redes Neurais Artificiais (RNAs) fornecem um método geral e prático para a aprendizagem de funções de valor real e de valor discreto a partir de exemplos.
* Algoritmos como o backpropagation (retro-propagação) utilizam a "descida do gradiente" para ajustar os parâmetros das redes para melhor adaptar um conjunto de treinamentos de pares entrada - saída (ou vetor de atributos - valor do conceito alvo).
* A aprendizagem de reder neurais é robusta a erros e ruídos nos dados de treinamento.
** Perceptron 
*Rede neural elementar baseada em uma unidade chamada Perceptron criada por Rosenblatt em 1958.
* Um perceptron:
    1. Recebe um vetor de entradas de valor real;
    2. Calcula uma combinação linear destas entradas
    3. Fornece na saída:
       * "+1" se o resultado é maior que algum limiar
       * "-1" caso contrário
*Mais precisamente, fornecidas as entradas x^1...x^n, a saída o(x^1...x^n) calculada pelo perceptron é . . .
* onde:
    * Cada elemento wî, é uma constante de valor real, ou peso, que determina a contribuição da entrada x^i na saída do perceptron.
* a aprendizagem do perceptron envolve:
    * A escolha dos valores dos pesos w^o a w^n.
* A camada de entrada deve possuir uma unidade especial conhecida como bias, qu eé um termo constante que não depende de nenhum valor de entrada.

* Superfície de decisão:
* Podemos "ver" o perceptron como uma superfície de separação em um espaço n-dimensional de instâncias.
* O perceptron fornece "1" para instâncias dispostas em um lado do hiperplano e "-1" para instâncias dispostas no outro lado.
* Um único perceptron consegue separar somente conjuntos de exemplo linearmente separáveis.
* Regras de treinamento perceptron
* Os pesos do perceptron são modificados a cada passo de acordo com a regra de treinamento do perceptron, que modifica o peso w^i, associado a entrada w^i de acordo com a regra:
* wi <- wi + delta|wi
* onde
* delta|wi = n(t-o)xi
* t é o valor alvo para o exemplo de treinamento
* o é a saída gerada pelo perceptron
* n é uma constante pequena (0.1) chamada de taxa de aprendizagem
* Se o exemplo de treinamento é classificado incorretamete, o valor de delta|wi é alterado.
* Pode se provar que este procedimento de aprendizagem converge dentro de um número finito de passos quando:
    * As classes dos dados de treinamento são linearmente separáveis
    * n é suficientemente pequeno
* Porém: falha em convergir se as classes forem linearmente não-separáveis.
* Solução: algoritmo descida do gradiente.
* Descida do gradiente:
* Para dados não linearmente separáveis, a regra delta converge em direção a aproximação que melhor se ajusta ao conceito alvo.
* Ideia chave: usar a descida do gradiente para procurar o melhor vetor de pesos.
* Pegar um vetor inicial aleatório de pesos;
* Aplicar a unidade linear para todos os exemplos de treinamento e calcular delta|w, para cada peso de acordo com a equação anterior;
* Atualizar cada peso wi adicionando delta|wi e então repetir este processo.
* O algoritmo convergirá para um vetor de pesos com erro mínimo.

* Redes Multicamadas
* Perceptrons expressam somente superfícies de decisão linear.
* Redes multicamadas treinadas pelo algoritmo backpropagation são capazes de expressar uma rica variedade de superficies de decisão não lineares.
* Redes são capazes de representar funções altamente não lineares.

* Algoritmo Backpropagation
* Aprende os pesos para uma rede multicamadas, dada uma rede com um npumero fixo de unidades e interconexões.
* O algoritmo backpropagation emprega "descida do gradiente" para minimizar o erro quadrático entre saída da rede e os valores alvos para estas saídas.
* Notação:
* Um indice é atribuido a cada nó da rede, onde nó pode ser uma entrada da rede ou a saída de alguma unidade da rede.
* x^ji indica a entrada a partir do nó i unidade j e w^ji indica o peso correspondete
* 6^n indica o termo do erro associado com a unidade n.
* Similar a (t-o)
* Descida do gradiente sobre o vetor de pesos inteiro da rede
* Encontrará um erro mínimo local (não necessariamente global)
* Na prática, geralmente funciona bem (pode executar múltiplas vezes)
* 15/18
