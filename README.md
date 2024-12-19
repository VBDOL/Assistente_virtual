# Projeto: Assistente Virtual com Processamento de Linguagem Natural

## Introdução
Este projeto é um assistente virtual desenvolvido em Python, utilizando bibliotecas de Processamento de Linguagem Natural (PLN) e reconhecimento de fala. Ele pode converter texto em áudio, reconhecer comandos de voz e executar funções automatizadas como:

- Realizar buscas no YouTube e Wikipedia;
- Contar piadas;
- Informar o horário atual;
- Reproduzir músicas (localmente);
- Encerrar o programa ao comando "exit".

## Soluções Utilizadas

### 1. **Conversão de Texto em Áudio (Text-to-Speech)**
Para converter texto em áudio, utilizamos a biblioteca `gTTS`:
- **Configuração:**
  - Instalação da biblioteca: `!pip install gTTS`
  - Utiliza o serviço de síntese de fala do Google para gerar áudio a partir de textos.

### 2. **Conversão de Fala em Texto (Speech-to-Text)**
A biblioteca `speech_recognition` é usada para captar e transcrever áudio:
- **Configuração:**
  - Instalação de dependências necessárias como `speech_recognition`.
  - No Colab, como o `PyAudio` não é suportado, substituímos a captura de áudio ao vivo por entradas de texto simuladas com `input()`.

### 3. **Execução de Comandos**
Comandos de voz ou texto permitem ao assistente executar tarefas como:
- Pesquisar no YouTube:
  - Abrir o navegador com resultados para um termo de busca fornecido.
- Consultar a Wikipedia:
  - Exibir e ler um resumo de três sentenças sobre um tópico.
- Contar Piadas:
  - Usar a biblioteca `pyjokes` para gerar piadas em inglês.
- Informar Horário Atual:
  - Utilizar `datetime` para obter e informar o horário.

### 4. **Simulação no Google Colab**
Devido às limitações do ambiente Colab:
- Funções que dependem de microfone (PyAudio) foram adaptadas para utilizar `input()`.
- A função de esvaziar a lixeira (Windows) foi desativada.

### 5. **Execução Local (Opção Completa)**
Para usar todas as funcionalidades, é necessário rodar o código localmente com:
- Python instalado;
- Microfone e o `PyAudio` configurados corretamente;
- Diretório de músicas definido para reprodução.

## Como Executar
1. Clone o repositório ou copie o código para seu ambiente.
2. Instale as dependências:
   ```bash
   !pip install gTTS speechrecognition pyjokes wikipedia
   ```
3. Rode o script e interaja com o assistente por texto ou comandos de voz (se local).

## Fluxo do Projeto
1. **Inicialização do Assistente:** O assistente aguarda comandos.
2. **Recebe Entrada:** Captura áudio ou texto do usuário.
3. **Processamento:** Identifica o comando e executa a tarefa correspondente.
4. **Resposta:** Retorna a resposta em texto e áudio ao usuário.

## Ilustração do Projeto
![Ilustração do Projeto](assistente.webp)

Essa representação captura a essência do projeto, mostrando um assistente virtual em ação e suas funções em um ambiente moderno.

