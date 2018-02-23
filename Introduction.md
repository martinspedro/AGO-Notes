# Antenas e Guias de Onda - Aula Introdutória

**Corpo Docente:**

- Teóricas:
	- Nuno Borges de Carvalho
	- nbcarvalho@ua.pt
- Práticas:
	- Adão Silva
	- adao@ua.pt

#Organização das aulas teóricas

Aulas de 1 hora + 30/45 min de exerc+icios

# Avaliação
 - Prática (50%)
	1. **Trabalho de filtros**
		- É dada uma especificação de um filtro
		- Guiões seguem as perspetiva de que temos uma missão/problema
		- O guião fornece as **apenas** especificações/requisitos que o filtro têm de cumprir
		- Implica a elaboração de um Relatório
	2. **Trabalho de Amplificadores[^1]**
		> Qandor um engenheiro de RF faz um amplificador sai um oscilador, quando fazemos um oscilador sai um amplificador
		- Apenas simulação
	3. **Trabalho de Antenas**
		- Vamos montar antenas
		- 
- Teórica (50%)
	1. Exame a meio do semestre
	2. Exame na época de exames

[^1]: O DETI não tem capacidade de produzir amplificadores de RF para todos

# Introdução
- Seguimento de POE
- Conmceitos de propagação em linha

- Conceitos importantes
	- stub
	- adaptação
	- VSWR
	- Impendância característica
	- Linhs de Transmissão


## Cap 1. Utilização de linhas de transmissão em circuitos RF
Em RF:
- Uso matrizes de parâmetros S e parâmetros T para caracterizar os circuitos
- Os **circuitos amplificadores** convencionais não servem
	- Não posso assumir que são instantâneos
	- Ocorre **propagação do sinal no interior do amplificador**
	- Os circuitos de amplicação a que estavamos habituados até agora não podem existir.
	- É preciso repensar os amplificadores para circuitos RF
	- Será necessário **polarizar** estes amplifcadores usando circuitos RF
- Devo assumir que estou em **condições de propagação de sinal** sempre que: $d = \approx \frac{1}{16} \lambda$
- **Não podemos desprezar as capacidades parasitas:**
	- mesmo sendo da ordem de grandeza dos fF, terão implicações na propagação do sinal, porque a frequência é grande
- Qualquer **fio** representa uma **linha de transmissão**
- O que interessa é a potência, não a tensão e/ou corrente
- **Todos os circuitos são `passa baixo`**, eventualmente
	- A sua largura de banda é sempre finita
	- Existirá sempre uma frequência que irão atenuar
- **Não posso fazer filtros com circuitos RC**:
		- Dissipam potência: $P=RI^2$
		- A energia à entrada do circuito não chega na totalidade à saída [^1]
		- diminuir/eliminar a dissipação $\implies$ substituir a resistência $\implies$ circuito LC
- **Desenhar filtros implica:**
	- Obter uma função de transferência em função de uma dada resposta em frequência pretendida
	- A obtenção dos pólos e dos zeros dessa função de transferência é feita usando a decomposição das frações em tipos especiais de polinómios, $H(jw) = \frac{P(w)}{Q(w)}$
	- Como transformar as caractereósticas da resposta em frequência do filtro para obter os coeficientes do filtro
		1. Partir da resposta em freq
		2. Dimensionar pólos e zeros dos filtros
		3. converter em polinómios
		4. Implementar o circuito que implementa esses polinómios
	- O descrito só se aplica a filtros passivos.

[^1]: Mesmo supondo componentes ideais

## Cap. II - Guais de onda em paredes metálicas
- Para frequências mutio elevadas não posso usar cabos coaxiais
- **Guia de Onda:**
	- Forçar a energia da onda a propagar-se a dentro de um meio guiado
	- tubos metálicos com forma cilindrica, retangular, quadrada, etc
	- Objetivo: guiar a propagação da onda que seria, caso contrário, feita em meio livre 
- **Formas de propagação:**
	- ou tipicamente campo elétrico
	- ou tipicamente campo magnético
	- uma das duas
- 

## Cap.III - Fibras Óticas
- Que Tipos de fibras?
- Como caracterizar a Onda refletida?


## Cap IV - Radiação
- Antenas
- Não guias de onda 
- Tenho de transmitir o meu cmpo electromagnéticos para o espaço

Tipos de Antenas:

- Patched antenna
- Antenas YAGGI

> Grande parte do desenho de antenas é por intuição 




# Simuladores a serem usados nas aulas práticas
- Princípio de funcionamento equivalente ao Cadence, mas para RF
- Harmonic Balance
- Microwave Office
- ADS (Advanced Digital System)
- CST (Computer Simualtion System) 
	- Simulação Eletromagnética
	- Simualões medicinais
	- Simulações de aviões, carros, etc
	- Antena vai ser construída usando CST


# Bibliografia
- **David M. Pozar, Microwave Engineering** (60%)
- Gerd Keiser, Optical Fiber Communications (10%)
- Constantine A. Balanis, Antenna Theory - Analysis and Design (30%)


