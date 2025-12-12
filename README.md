# els_ema_data

this repository is associated with ecological momentary assessment (ema) data collected by the stanford neurodevelopment, affect, and psychopathology lab study of the consequences of early life stress for psychobiological development over the pubertal transition. contact eugiampe@stanford.edu if you have any questions.

## overview

this repository includes:

- raw mood, event, and sleep ema data exports  
- a merged and cleaned dataset containing all prompt and participant-level flags  
- supporting study materials (protocols and prompt wording)  
- rmarkdown script for data processing  

## the primary output is `data/clean/ema_flags_master.csv`
each row represents `id × date × session`. the file includes:

### harmonized identifiers and timing
- standardized ids  
- cleaned dates and session assignment (morning, afternoon, evening)  
- aligned mood and event surveys  
- merged sleep data for morning prompts  

### prompt-level summary scores
- mean and sd across 9 mood items  
- mean and sd across 3 event ratings  
- sleep quality and hours slept  

### prompt-level quality flags
- mood: speed, low variance, high modal responding, any-flag indicator  
- event: speed, low variance, high modal responding, any-flag indicator  
- sleep: fast completion, implausible hours, any-flag indicator  
- missingness: mood present / event missing, or event present / mood missing  
- timing drift between mood and event (> 3600 seconds)  

### participant-level indicators
- counts of valid mood, event, and sleep prompts  
- flags indicating whether minimum prompts are met for estimating:  
  - means  
  - variability  
  - slopes (reactivity)  

a detailed variable dictionary is provided in `data/clean/clean_data_codebook.xlsx`
