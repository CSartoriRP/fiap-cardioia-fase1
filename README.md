# CardioIA — Fase 1: Batimentos de Dados

## Mapeando o Coração Moderno

O **CardioIA** é um projeto acadêmico da FIAP que propõe a construção progressiva de um ecossistema de cardiologia inteligente apoiado por Inteligência Artificial.

Nesta primeira fase, o objetivo é estabelecer uma base de dados multimodal reutilizável nas etapas futuras. Foram preparados **dados clínicos estruturados**, **textos relacionados à saúde cardiovascular** e **imagens de eletrocardiogramas (ECG)**.

A estratégia conecta conceitualmente:

**dados do paciente → conhecimento médico → exame cardíaco → futuras aplicações de IA**

Os conjuntos não representam necessariamente os mesmos pacientes e não existe associação individual entre registros numéricos, textos e imagens.

## 1. Dados Numéricos

**Arquivo:** `data/numeric/heart_disease_simulated.csv`

Foi criado um dataset **simulado** com **200 registros fictícios** e 11 variáveis relacionadas à avaliação cardiovascular.

| Variável | Descrição |
|---|---|
| `patient_id` | Identificador fictício |
| `age` | Idade |
| `sex` | Sexo |
| `resting_blood_pressure_mmHg` | Pressão arterial em repouso |
| `cholesterol_mg_dL` | Colesterol |
| `fasting_glucose_mg_dL` | Glicemia em jejum |
| `max_heart_rate_bpm` | Frequência cardíaca máxima |
| `chest_pain_type` | Tipo de dor torácica |
| `resting_ecg` | Resultado categórico do ECG em repouso |
| `exercise_induced_angina` | Angina induzida por exercício |
| `cardiovascular_disease` | Variável-alvo simulada |

O conjunto possui 80 registros com presença simulada de doença cardiovascular e 120 com ausência.

### Relevância e potencial para IA

As variáveis representam informações relacionadas à avaliação cardiovascular. Em fases futuras, o conjunto poderá ser utilizado em análise exploratória e experimentos supervisionados de classificação usando `cardiovascular_disease` como variável-alvo.

Como os dados são simulados, possuem finalidade exclusivamente didática e **não representam um modelo clínico validado**.

## 2. Dados Textuais — Processamento de Linguagem Natural

Os documentos estão em `data/text/`.

### Doenças Cardiovasculares

**Arquivo:** `cardiovascular_diseases_who.txt`  
**Fonte temática:** World Health Organization (WHO)  
**Fonte original:** https://www.who.int/news-room/fact-sheets/detail/cardiovascular-diseases-(cvds)

O documento é uma síntese educacional sobre doenças cardiovasculares, fatores de risco, sintomas e prevenção.

### Eletrocardiograma

**Arquivo:** `electrocardiogram_medlineplus.txt`  
**Fonte temática:** MedlinePlus — U.S. National Library of Medicine  
**Fonte original:** https://medlineplus.gov/lab-tests/electrocardiogram/

O documento é uma síntese educacional sobre eletrocardiograma, atividade elétrica cardíaca, componentes do traçado e aplicações clínicas.

### Potencial para NLP

Os textos poderão ser utilizados para extração de sintomas, reconhecimento de doenças, identificação de fatores de risco, exames e tratamentos, reconhecimento de entidades, classificação temática e sumarização.

## 3. Dados Visuais — Visão Computacional

**Fonte:** ECG Images dataset of Cardiac Patients — Mendeley Data  
**Dataset original:** https://data.mendeley.com/datasets/gwbz3fsgp8/2  
**Licença informada pela fonte:** CC BY 4.0

Foi selecionada uma amostra balanceada de **100 imagens JPG de ECG**:

| Categoria | Imagens |
|---|---:|
| Batimento cardíaco anormal (Abnormal Heartbeat) | 25 |
| Histórico de infarto do miocárdio (History of MI) | 25 |
| Infarto do miocárdio (Myocardial Infarction) | 25 |
| Normal | 25 |
| **Total** | **100** |

### Acesso ao conjunto completo

Devido ao tamanho dos arquivos, as 100 imagens foram compactadas e disponibilizadas em armazenamento externo público, conforme permitido pelo enunciado.

**Google Drive — 100 imagens de ECG:**  
https://drive.google.com/file/d/1U3q3aBCRKs19cd5Xl6TDOn4l43gjKi3n/view?usp=sharing

O link está configurado para leitura por qualquer pessoa que possua o endereço.

### Potencial para Visão Computacional

A organização por categorias permite futura utilização em classificação de ECGs, reconhecimento de padrões, identificação de alterações no traçado e diferenciação entre exames normais e categorias anormais.

## 4. Integração Conceitual

| Tipo de dado | Área de IA | Aplicação futura |
|---|---|---|
| Dados clínicos | Machine Learning | Classificação de risco/doença |
| Textos médicos | NLP | Extração e organização de informação |
| Imagens de ECG | Visão Computacional | Classificação e reconhecimento de padrões |

A integração nesta fase é **conceitual**. Não existe correspondência individual entre os pacientes simulados e os pacientes presentes no dataset visual.

## 5. Governança, Privacidade, Ética e Viés

O dataset numérico é simulado e não contém informações pessoais reais. As imagens são provenientes de dataset acadêmico público e permanecem vinculadas à fonte e licença originais.

As fontes estão registradas em `docs/sources.md`.

Os conjuntos não devem ser considerados representativos de toda a população. O dataset numérico reflete as regras usadas na simulação, enquanto o dataset visual pode conter vieses de população, coleta, equipamentos e distribuição das categorias.

O CardioIA possui finalidade acadêmica. Nenhum dado, resultado ou futuro modelo deve ser interpretado como ferramenta clínica validada ou utilizado isoladamente para diagnóstico, tratamento ou decisão médica.

## 6. Estrutura da Entrega

```text
fiap-cardioia-fase1/
├── README.md
├── data/
│   ├── numeric/
│   │   └── heart_disease_simulated.csv
│   └── text/
│       ├── cardiovascular_diseases_who.txt
│       └── electrocardiogram_medlineplus.txt
└── docs/
    └── sources.md
```

O conjunto visual completo está hospedado externamente no Google Drive devido ao tamanho dos arquivos.

## 7. Próximas Fases

A base poderá ser reutilizada em notebooks Python/Colab para análise exploratória, Machine Learning, Processamento de Linguagem Natural e Visão Computacional.

## Referências

- World Health Organization. **Cardiovascular diseases (CVDs)**. https://www.who.int/news-room/fact-sheets/detail/cardiovascular-diseases-(cvds)
- MedlinePlus — U.S. National Library of Medicine. **Electrocardiogram**. https://medlineplus.gov/lab-tests/electrocardiogram/
- Mendeley Data. **ECG Images dataset of Cardiac Patients**. https://data.mendeley.com/datasets/gwbz3fsgp8/2
