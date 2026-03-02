# Autoencoders Variacionales en PyTorch

Este repositorio implementa variantes de Variational Autoencoders y aprendizaje semi-supervisado sobre MNIST binarizado.

<img width="640" height="480" alt="vae" src="https://github.com/user-attachments/assets/f6a8aed8-8c67-4dc7-bb82-a058c030b8c0" />



## modelos incluidos
- **VAE / β-VAE** (modelo base)  
- **GMVAE** (prior como mezcla de Gaussianas)  
- **SSVAE** (VAE semi-supervisado para clasificación en MNIST)  
- Utilidades para: ELBO/IWAE, KL, reconstrucción, binarización, evaluación de lower bounds y accuracy.

## resultados generales
En conjunto de prueba de MNIST:
- **VAE**: NELBO = 101.51 ± 0.17, KL = 19.34 ± 0.09, Rec = 82.17 ± 0.16  
- **GMVAE**: NELBO = 99.18, KL = 17.76, Rec = 81.42  
- **SSVAE (Accuracy)**:
  - Supervisado (sin ELBO(x)): 0.77
  - Semi-supervisado (con ELBO(x)): 0.86

 ## Cómo ejecutarlo
 - **generación de muestras al azar**: python3 generate_samples.py --model vae --run 0000 --iter_max 20000
 - **GMVAE**: python run_gmvae.py
 - **SSVAE supervisado**: python run_ssvae.py --gw 0
 - **SSVAE semi-supervisado**: python run_ssvae.py --gw 0



Proyecto realizado en el marco de ECI 2025 (UBA).
