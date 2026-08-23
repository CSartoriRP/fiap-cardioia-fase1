# CardioIA --- Fase 1: Batimentos de Dados

## Mapeando o Coração Moderno

O **CardioIA** é um projeto acadêmico da FIAP que propõe a construção
progressiva de um ecossistema de cardiologia inteligente apoiado por
Inteligência Artificial.

Nesta primeira fase, o objetivo é estabelecer uma base de dados
multimodal que possa ser reutilizada nas etapas futuras do projeto.
Foram preparados três tipos de dados: **dados clínicos estruturados**,
**textos relacionados à saúde cardiovascular** e **imagens de
eletrocardiogramas (ECG)**.

A estratégia adotada conecta conceitualmente:

**dados do paciente → conhecimento médico → exame cardíaco → futuras
aplicações de IA**

Os conjuntos não representam necessariamente os mesmos pacientes e,
portanto, não existe associação individual entre registros numéricos,
textos e imagens.

------------------------------------------------------------------------

## 1. Dados Numéricos

### Arquivo

`data/numeric/heart_disease_simulated.csv`

### Descrição

Foi criado um dataset **simulado** contendo **200 registros fictícios de
pacientes** e 11 variáveis relacionadas à avaliação cardiovascular.

  -----------------------------------------------------------------------
  Variável                            Descrição
  ----------------------------------- -----------------------------------
  `patient_id`                        Identificador fictício

  `age`                               Idade

  `sex`                               Sexo

  `resting_blood_pressure_mmHg`       Pressão arterial em repouso

  `cholesterol_mg_dL`                 Colesterol

  `fasting_glucose_mg_dL`             Glicemia em jejum

  `max_heart_rate_bpm`                Frequência cardíaca máxima

  `chest_pain_type`                   Tipo de dor torácica

  `resting_ecg`                       Resultado categórico do ECG em
                                      repouso

  `exercise_induced_angina`           Angina induzida por exercício

  `cardiovascular_disease`            Variável-alvo simulada de doença
                                      cardiovascular
  -----------------------------------------------------------------------

O conjunto possui 80 registros classificados como presença simulada de
doença cardiovascular e 120 como ausência.

### Relevância clínica

As variáveis escolhidas representam informações frequentemente
consideradas na avaliação cardiovascular, incluindo características
demográficas, pressão arterial, colesterol, glicemia, frequência
cardíaca, dor torácica, alterações relacionadas ao ECG e angina.

Como os dados são simulados, as relações existentes no dataset possuem
finalidade exclusivamente didática e **não representam um modelo clínico
validado**.

### Potencial para Machine Learning

O dataset foi estruturado de forma a permitir, em fases futuras,
experimentos supervisionados de classificação utilizando
`cardiovascular_disease` como variável-alvo.

Poderão ser exploradas atividades como:

-   análise exploratória;
-   preparação e transformação de variáveis;
-   treinamento de classificadores;
-   avaliação de desempenho;
-   análise da influência das características sobre as previsões.

O dataset não deve ser utilizado para diagnóstico ou decisão médica
real.

------------------------------------------------------------------------

## 2. Dados Textuais --- NLP

Os documentos estão armazenados em:

`data/text/`

Foram preparados dois textos em formato `.txt`, ambos como sínteses
educacionais baseadas em fontes institucionais.

### 2.1 Doenças Cardiovasculares

**Arquivo:** `cardiovascular_diseases_who.txt`

**Fonte temática:** World Health Organization (WHO)

O documento aborda doenças cardiovasculares, fatores de risco, sintomas,
prevenção e aspectos relacionados ao manejo dessas condições.

A fonte original pode ser consultada em:

https://www.who.int/news-room/fact-sheets/detail/cardiovascular-diseases-(cvds)

### 2.2 Eletrocardiograma

**Arquivo:** `electrocardiogram_medlineplus.txt`

**Fonte temática:** MedlinePlus --- U.S. National Library of Medicine

O documento aborda o eletrocardiograma, atividade elétrica cardíaca,
componentes básicos do traçado, aplicações clínicas e algumas condições
cardiovasculares relacionadas ao exame.

A fonte original pode ser consultada em:

https://medlineplus.gov/lab-tests/electrocardiogram/

### Potencial para NLP

Esses documentos poderão ser utilizados futuramente em tarefas de
Processamento de Linguagem Natural, como:

-   extração de sintomas;
-   reconhecimento de doenças e condições cardiovasculares;
-   identificação de fatores de risco;
-   identificação de exames e tratamentos;
-   reconhecimento de entidades;
-   classificação temática;
-   sumarização automática.

O uso de NLP poderá contribuir para transformar informação médica
textual não estruturada em informação estruturada que possa ser
utilizada por outros componentes do CardioIA.

------------------------------------------------------------------------

## 3. Dados Visuais --- Visão Computacional

### Fonte

**ECG Images dataset of Cardiac Patients --- Mendeley Data**

https://data.mendeley.com/datasets/gwbz3fsgp8/2

Licença informada pela fonte: **CC BY 4.0**.

### Amostra utilizada

Para esta fase foi selecionada uma amostra balanceada de **100 imagens
de ECG**, distribuídas em quatro categorias:

  Categoria                            Imagens
  ---------------------------------- ---------
  Abnormal Heartbeat                        25
  History of Myocardial Infarction          25
  Myocardial Infarction                     25
  Normal                                    25
  **Total**                            **100**

As imagens estão organizadas em:

`data/images/ecg/`

com uma subpasta para cada categoria.

### Potencial para Visão Computacional

A organização por classes permite que essas imagens sejam utilizadas
futuramente em experimentos supervisionados de Visão Computacional.

Entre as aplicações possíveis estão:

-   classificação de ECGs;
-   reconhecimento de padrões;
-   identificação de alterações no traçado;
-   diferenciação entre exames normais e categorias anormais;
-   extração de características visuais.

Nesta fase não é realizado diagnóstico automatizado. As imagens
constituem uma base inicial para experimentação acadêmica nas próximas
fases do CardioIA.

------------------------------------------------------------------------

## 4. Integração Conceitual

A base da Fase 1 foi planejada como uma fundação multimodal.

Os dados numéricos representam características clínicas estruturadas de
pacientes simulados.

Os textos representam conhecimento não estruturado sobre doenças
cardiovasculares e eletrocardiografia.

As imagens representam exames de ECG organizados por categorias.

Esses três componentes poderão alimentar diferentes técnicas de IA:

  -----------------------------------------------------------------------
  Tipo de dado            Área de IA              Aplicação futura
  ----------------------- ----------------------- -----------------------
  Dados clínicos          Machine Learning        Classificação de
                                                  risco/doença

  Textos médicos          NLP                     Extração e organização
                                                  de informação

  Imagens ECG             Visão Computacional     Classificação e
                                                  reconhecimento de
                                                  padrões
  -----------------------------------------------------------------------

A integração nesta fase é **conceitual**. Não existe correspondência
individual entre os pacientes simulados do dataset numérico e os
pacientes presentes no dataset de imagens.

------------------------------------------------------------------------

## 5. Governança, Privacidade, Ética e Viés

A preparação dos dados considerou aspectos iniciais de governança
relevantes para aplicações de IA em saúde.

### Privacidade

O dataset numérico é totalmente simulado e não contém informações
pessoais reais.

As imagens de ECG são provenientes de dataset acadêmico público e
permanecem vinculadas à fonte e licença originais.

### Proveniência

As fontes utilizadas estão registradas em:

`docs/sources.md`

Esse registro permite identificar a origem dos conteúdos e distinguir
claramente dados simulados de dados provenientes de fontes externas.

### Viés e representatividade

Os conjuntos utilizados não devem ser considerados representativos de
toda a população.

O dataset numérico é simulado e, portanto, reflete as regras utilizadas
em sua geração.

O dataset visual também pode conter vieses relacionados à população de
origem, processo de coleta, distribuição das categorias e
características dos equipamentos utilizados.

Modelos desenvolvidos futuramente deverão considerar essas limitações
antes de qualquer interpretação de desempenho.

### Uso responsável

O CardioIA possui finalidade acadêmica.

Nenhum dado, resultado ou futuro modelo desenvolvido a partir desta base
deve ser interpretado como ferramenta clínica validada ou utilizado
isoladamente para diagnóstico, tratamento ou tomada de decisão médica.

------------------------------------------------------------------------

## 6. Estrutura do Projeto

``` text
fiap-cardioia-fase1/
│
├── README.md
│
├── data/
│   ├── numeric/
│   │   └── heart_disease_simulated.csv
│   ├── text/
│   │   ├── cardiovascular_diseases_who.txt
│   │   └── electrocardiogram_medlineplus.txt
│   └── images/
│       └── ecg/
│           ├── abnormal_heartbeat/
│           ├── history_of_mi/
│           ├── myocardial_infarction/
│           └── normal/
│
└── docs/
    └── sources.md
```

------------------------------------------------------------------------

## 7. Objetivo das Próximas Fases

A base construída nesta etapa foi organizada para permitir sua evolução
ao longo do CardioIA.

Os dados poderão futuramente ser utilizados em notebooks Python/Colab
para análise exploratória, Machine Learning, NLP e Visão Computacional,
mantendo separação clara entre as diferentes modalidades e suas
respectivas origens.

------------------------------------------------------------------------

## Referências

-   World Health Organization. **Cardiovascular diseases (CVDs)**.
    https://www.who.int/news-room/fact-sheets/detail/cardiovascular-diseases-(cvds)
-   MedlinePlus --- U.S. National Library of Medicine.
    **Electrocardiogram**.
    https://medlineplus.gov/lab-tests/electrocardiogram/
-   Mendeley Data. **ECG Images dataset of Cardiac Patients**.
    https://data.mendeley.com/datasets/gwbz3fsgp8/2

Mais detalhes sobre origem e natureza dos dados estão disponíveis em
`docs/sources.md`.
