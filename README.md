# 'Laboratórios de Redes de Computadores'

Este repositório foi criado para a disciplina de Redes de Computadores e tem como objetivo armazenar todos os códigos, notebooks de simulação e relatórios desenvolvidos ao longo da cadeira.

O foco é a implementação prática de conceitos teóricos de comunicação digital, codificação, modulação e análise de desempenho em canais com ruído.

# Lab 1: Modulação Digital com Áudio

## Objetivo do Laboratório

### O Lab 1, intitulado "Modulação Digital com Áudio", propôs a exploração da comunicação digital utilizando o canal de áudio (alto-falante $\to$ ar $\to$ microfone) para transmitir dados binários. ###

Os principais desafios foram:

Decodificar uma mensagem codificada em FSK (Frequency-Shift Keying) a partir de um arquivo de áudio (.wav).

Analisar o impacto do ruído (AWGN) no desempenho das modulações NRZ e Manchester.

Decodificar uma mensagem em um canal ruidoso real (dados_ar.wav), exigindo múltiplas transmissões para correção de erros.

Respostas e Resultados Chave

1. Modulação e Mensagem (Etapa 2)

Modulação Utilizada: NRZ com FSK ($440$ Hz para bit $0$ e $880$ Hz para bit $1$).

Mensagem de Teste (20 bits): 10110101001100101010

2. Análise de Ruído (Etapa 3 - A3.1)

O objetivo desta análise foi comparar a robustez de NRZ e Manchester submetidas a ruído.

Modulação

Falha Parcial (Primeiros Erros)

Falha Total (Todos os 20 bits errados)

NRZ

Em torno de $-6$ dB a $-9$ dB

$-21$ dB

Manchester

Em torno de $-12$ dB a $-18$ dB

$-27$ dB

Conclusão: A modulação Manchester provou ser superior em canais com ruído, tolerando um SNR aproximadamente $6$ dB mais baixo que o NRZ antes de falhar totalmente, devido ao seu mecanismo de auto-sincronização.

O relatório detalhado com a metodologia de simulação e a análise gráfica (relatorio_analise_ruido.tex) está incluído neste repositório.

Os gráficos de desempenho (Número de Erros vs. SNR e BER vs. SNR) foram gerados usando o script plot_comparacao_erros.py e comprovam a maior robustez do Manchester.

3. Ruído Real (Etapa 4)

Mensagem Decodificada (dados_ar.wav): 01011

Reproduções Necessárias: 3 vezes (Devido à complexidade do canal acústico real, foram necessárias múltiplas transmissões para garantir a correta sincronização e decodificação.)
