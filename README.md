## sesion 1-2 R -- 24/10/2022

## 1. Cálculos básicos

###1.1 Suma
1+1

### 1.2 Calcular el 15% de $1.900
0.15*1900

### 2. Instalar estos Paquetes 
install.packages("tidyverse")
install.packages("dplyr")
install.packages("plyr")
install.packages("tidyr")
install.packages("mlogit")
install.packages("stargazer")
install.packages("rsq")
install.packages("sjPlot")
install.packages("dslabs")

### 2.1 Cargar desde la biblioteca estos Paquetes
library(tidyverse)
library(dplyr)
library(plyr)
library(tidyr)
library(mlogit)
library(stargazer)
library(rsq)
library(sjPlot)
library(dslabs)

## 2. Encuesta CEP
### 2.1 Link: https://www.cepchile.cl/cep/encuestas-cep/encuestas-2010-2021/estudio-nacional-de-opinion-publica-n-86-abril-mayo-de-2022

### 2.2 Importar base de datos
library(readxl)
base_86 <- read_excel("C:/Users/Samsa/Downloads/encuesta_cep_abr_may2022 a)/encuesta_cep_abr-may2022/base_86.xlsx")
View(base_86)

# 2.3Variable numérica
base_86[sapply(base_86, is.numeric)] <- lapply(base_86[sapply(base_86, is.numeric)], as.factor)

## 3. Análisis descriptivo

### 3.1 Frecuencias

### Variable Inicial: sexo
table(base_86$sexo)

### Variable 2: Confianza Fuerzas Armadas
table(base_86$confianza_6_c)

### Variable 3: Confianza Carabineros
table(base_86$confianza_6_h)

### Variable 4: Confianza PDI
table(base_86$confianza_6_r)

### Variable 5: 2da vuelta elección presidencial
table(base_86$elec_pres_144_a)

### Variable 6: Escolaridad nivel 1
table(base_86$esc_nivel_1)

### Variable 7:info Trabajo remunerado
table(base_86$info_enc_35)

### Variable 8: actividad
table(base_86$info_enc_62)

### Variable 8: actividad
table(base_86$info_enc_62)
