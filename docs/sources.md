# Fontes de Dados --- CardioIA Fase 1

Este documento registra a origem e a natureza das fontes utilizadas na
Fase 1 do projeto CardioIA.

## 1. Dataset Numérico

### Origem

O dataset numérico utilizado neste projeto é **simulado** e foi gerado
especificamente para fins acadêmicos na Fase 1 do CardioIA.

O conjunto contém 200 registros fictícios de pacientes e não representa
indivíduos reais.

### Características

O dataset contém as seguintes variáveis:

-   `patient_id`: identificador fictício do paciente;
-   `age`: idade;
-   `sex`: sexo;
-   `resting_blood_pressure_mmHg`: pressão arterial em repouso;
-   `cholesterol_mg_dL`: colesterol;
-   `fasting_glucose_mg_dL`: glicemia em jejum;
-   `max_heart_rate_bpm`: frequência cardíaca máxima;
-   `chest_pain_type`: tipo de dor torácica;
-   `resting_ecg`: resultado categórico do ECG em repouso;
-   `exercise_induced_angina`: ocorrência de angina induzida por
    exercício;
-   `cardiovascular_disease`: variável-alvo simulada indicando presença
    ou ausência de doença cardiovascular.

Os valores foram gerados de maneira probabilística para produzir um
conjunto didático coerente com o domínio cardiovascular. O dataset não
possui validade clínica e não deve ser utilizado para diagnóstico,
tratamento ou tomada de decisão médica.

## 2. Dados Textuais

Foram preparados dois documentos textuais para futuras aplicações de
Processamento de Linguagem Natural (NLP).

Os arquivos são sínteses educacionais elaboradas para o projeto,
baseadas em informações disponibilizadas por fontes institucionais. Não
correspondem à reprodução integral dos conteúdos originais.

### 2.1 Cardiovascular Diseases

**Fonte temática:** World Health Organization (WHO)

**Documento:** Cardiovascular diseases (CVDs)

**URL:**
https://www.who.int/news-room/fact-sheets/detail/cardiovascular-diseases-(cvds)

**Conteúdo utilizado:** conceitos relacionados a doenças
cardiovasculares, fatores de risco, sintomas, prevenção e tratamento.

**Arquivo do projeto:** `cardiovascular_diseases_who.txt`

### 2.2 Electrocardiogram

**Fonte temática:** MedlinePlus --- U.S. National Library of Medicine

**Documento:** Electrocardiogram

**URL:** https://medlineplus.gov/lab-tests/electrocardiogram/

**Conteúdo utilizado:** conceitos sobre eletrocardiograma, atividade
elétrica cardíaca, ondas do ECG, aplicações clínicas e condições
cardiovasculares relacionadas.

**Arquivo do projeto:** `electrocardiogram_medlineplus.txt`

## 3. Dataset Visual

### ECG Images Dataset of Cardiac Patients

**Fonte:** Mendeley Data

**Dataset:** ECG Images dataset of Cardiac Patients

**URL:** https://data.mendeley.com/datasets/gwbz3fsgp8/2

**Licença informada pela fonte:** CC BY 4.0

O dataset original contém imagens de eletrocardiogramas organizadas em
diferentes categorias clínicas.

Para a Fase 1 do CardioIA foi selecionada uma amostra balanceada de 100
imagens, distribuídas da seguinte forma:

  Classe                               Quantidade
  ---------------------------------- ------------
  Abnormal Heartbeat                           25
  History of Myocardial Infarction             25
  Myocardial Infarction                        25
  Normal                                       25
  **Total**                               **100**

As imagens foram preservadas em suas categorias para permitir futura
utilização em tarefas supervisionadas de Visão Computacional.

## 4. Governança e Uso dos Dados

O projeto utiliza duas estratégias distintas de dados:

-   **dados numéricos simulados**, sem associação com pacientes reais;
-   **dados públicos e materiais derivados de fontes institucionais**,
    utilizados respeitando sua origem e finalidade acadêmica.

Nenhuma informação pessoal identificável foi criada ou adicionada ao
dataset numérico.

As imagens de ECG utilizadas são provenientes de dataset acadêmico
público e devem permanecer associadas à sua fonte e licença original.

Todo o conteúdo desta fase destina-se exclusivamente a fins educacionais
e experimentais no contexto do projeto CardioIA.
