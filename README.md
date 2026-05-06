# 📡 Projeto de Sistema de Comunicação Digital (SCD)

Neste projeto, desenvolvi uma cadeia completa de comunicação digital em banda base utilizando Python. A simulação engloba desde a conversão da mensagem em bits até à sua recuperação no receptor, passando por um canal com distorções realistas.

## 🎯 O Diferencial do Projeto
O grande foco que dei neste projeto foi garantir uma simulação realista. O meu receptor não "trapaceia" usando o texto original como referência; ele conhece apenas um pequeno preâmbulo no início da transmissão. 

É exclusivamente a partir desse preâmbulo que o código consegue calcular o atraso, sincronizar e equalizar o sinal para reverter os efeitos do canal (como ruído AWGN e desvanecimento). O texto final é recuperado "na raça", provando que a cadeia de comunicação funciona de ponta a ponta.

## ⚙️ Principais Características
- **Cadeia Completa:** Transmissor → Canal → Receptor.
- **Sincronização Realista:** Feita por correlação usando um preâmbulo.
- **Canal Adverso:** Implementação de ruído AWGN, atraso temporal e canal seletivo em frequência.
- **Equalização:** Aplicada antes da decisão dos símbolos.
- **Múltiplas Visualizações:** Gráficos no tempo, frequência, Constelação e Trajetória I/Q.
- **Hardware Ready:** O sinal gerado pode ser exportado em colunas `I,Q` para ser testado num AWG (Arbitrary Waveform Generator).

## 📊 Visualizações no Plano I/Q
Fiz questão de incluir duas visualizações no plano I/Q: 
1. **A constelação normal:** Onde vemos claramente os pontos de decisão.
2. **A trajetória I/Q:** Que mostra o comportamento real do sinal, revelando como ele se movimenta e transita entre os símbolos após a filtragem e interpolação, algo que a constelação sozinha não mostra.
