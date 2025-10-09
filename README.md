          ┌──────────────────┐
          │   MRI Data (T1w) │
          └──────┬───────────┘
                 │
        Preprocessing (MONAI)
                 │
       3D ResNet-50 (MedicalNet)
                 │
      ┌──────────┴──────────┐
      │  MRI Embedding (512)│
      └──────────┬──────────┘
                 │
                 │
                 ▼
      ┌──────────────────┐
      │  Genetic Data    │
      └──────┬───────────┘
             │
     Preprocessing (PLINK)
             │
       Autoencoder Model
             │
      Genetic Embedding (64)
             │
             ▼
        
 ┌────────────────────────────────┐
 │   Concatenate MRI + Genetic    │
 │   Embeddings → Multimodal Vec  │
 └────────────────────────────────┘
             │
     Random Forest Classifier
             │
             ▼
     Alzheimer’s Classification
     (AD / MCI / Normal Control)





     
