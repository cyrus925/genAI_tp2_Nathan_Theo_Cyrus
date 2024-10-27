# genAI_tp2_Nathan_Theo_Cyrus
## 1st part : Activity Class
Critère de Succès : Avoir un modèle qui envoie des réponses en phase avec la doc sur la majeur 


Benchmark review: search online for some of the benchmarks used to evaluate and compare language models.
1. GLUE
2. MMLU
3. TruthfulQA
4. WinoGrande
5. GSM8K
6. HellaSwag

Results Benchmark review :

HellaSwag (10-shot)	61.52
MMLU (5-shot)	26.79
TruthfulQA (0-shot)	42.42
Winogrande (5-shot)	61.8
GSM8K (5-shot)	0.08

https://huggingface.co/pankajmathur/orca_mini_3b

## 2nd part : validation policy 

### Objectives and Validation Metrics

To validate the quality and performance of the LLM application, we’ve defined key metrics covering response quality, user experience, performance, and costs.

#### 1. Response Quality Measures
These metrics evaluate the relevance and accuracy of generated responses:
- **Response Accuracy**: Measured with benchmarks like **MMLU** to assess contextual knowledge and the model's ability to answer corretly.
- **Response Relevance**: Using the **HellaSwag** score, which tests model consistency and common sense in narrative scenarios.

#### 2. User Experience Measures
These metrics aim to enhance user satisfaction:
- **Response Time**: The average time required to generate a response.

#### 3. Performance Indicators
These indicators are critical for ensuring smooth and continuous use:
- **Average Latency**: Measures the model’s response speed.
- **Performance Stability**: Verifies the model’s consistency under a load of simultaneous requests, tested with stress benchmarking tools.

#### 4. Cost Indicators
These indicators help control resources:
- **Cost per Query**: Evaluates the average cost per API call or generation.
- **GPU/CPU Resource Usage**: Evaluates model efficiency to optimize infrastructure costs by tracking average usage per query.

### Reference Datasets

To evaluate our LLM model, we use reference datasets that cover the above areas.

| Dataset Name | Description | Link | Relevance to the Application |
|--------------------|-------------|------|--------------------------------|
| **GLUE** | General language understanding benchmark assessing accuracy in multiple NLP tasks such as sentiment analysis and textual similarity. | [GLUE Benchmark](https://gluebenchmark.com/) | Helps evaluate general response quality and textual coherence. |
| **MMLU** | Multi-domain knowledge benchmark covering various subjects, used to evaluate reasoning and model understanding. | [MMLU](https://github.com/hendrycks/test) | Essential for testing specific knowledge and generalization ability. |
| **TruthfulQA** | Benchmark focused on answer truthfulness, testing the model’s ability to avoid misleading information. | [TruthfulQA](https://github.com/openai/truthfulqa) | Relevant to ensure the model provides reliable responses. |
| **HellaSwag** | Logical consistency benchmark, testing the model in scenarios where common sense is required. | [HellaSwag](https://leaderboard.allenai.org/hellaswag) | Measures logic and coherence in generated responses. |
| **Winogrande** | Logical reasoning benchmark with multiple-choice questions involving syntactic and contextual ambiguity resolution. | [Winogrande](https://leaderboard.allenai.org/winogrande) | Relevant for implicit reasoning tasks, evaluating the ability to understand contextual relationships. |

### Validation Results of Similar Models
Currently, Orca Mini 3B shows the following results on some of the selected benchmarks:
- **MMLU (5-shot)**: 26.79%
- **TruthfulQA (0-shot)**: 42.42%
- **HellaSwag (10-shot)**: 61.52%
- **Winogrande (5-shot)**: 61.8%

These scores serve as benchmarks for our application’s expected performance, and regular testing will be conducted to ensure we meet required standards.
