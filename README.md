# Análise de Sentimentos com Language Studio no Azure AI

## Azure Speech Studio

O Azure Speech Studio é uma interface gráfica e um conjunto de ferramentas que facilita a criação, personalização e gerenciamento de aplicações que utilizam o serviço **Azure AI Speech**.

| Recurso Principal | Descrição |
| :--- | :--- |
| **Fala para Texto (Speech-to-Text)** | Transcreve áudio em texto escrito, com suporte para modelos de linguagem e acústicos personalizados para alta precisão. |
| **Texto para Fala (Text-to-Speech)** | Sintetiza texto em fala de som natural, permitindo a criação de vozes neurais personalizadas (Custom Neural Voice). |

**Função na Análise de Sentimentos:** Serve como o **pré-processador**, convertendo dados de áudio (como gravações de chamadas) em texto legível para a próxima etapa.

## Azure Language Studio

O Azure Language Studio é um conjunto de ferramentas e uma interface gráfica que centraliza os recursos de **Processamento de Linguagem Natural (NLP)** e **Compreensão de Linguagem Natural (NLU)** do serviço **Azure AI Language**.

| Recurso Principal | Descrição |
| :--- | :--- |
| **Análise de Sentimentos** | Determina o tom emocional geral de um texto (Positivo, Negativo ou Neutro). |
| **Mineração de Opinião** | Vai além do sentimento geral, identificando sentimentos em relação a aspectos específicos ou entidades dentro do texto. |
| **NER (Reconhecimento de Entidades Nomeadas)** | Identifica e classifica entidades no texto (pessoas, locais, datas, etc.). |

**Função na Análise de Sentimentos:** Serve como o **analisador principal**, processando o texto de entrada para determinar e quantificar o sentimento.

## Fluxo de Análise de Sentimentos (Voz)

A análise de sentimentos em dados de voz é um processo de duas etapas que combina as capacidades de ambos os serviços:

1.  **Transcrição (via Speech Studio):** O áudio (voz) é alimentado no **Speech Studio**, que usa o recurso **Speech-to-Text** para gerar uma transcrição de texto precisa.
2.  **Análise (via Language Studio):** O texto transcrito é enviado ao **Language Studio**, que aplica a funcionalidade de **Análise de Sentimentos** para classificar o humor do falante (ex: frustrado, satisfeito) e gerar uma pontuação de confiança.
