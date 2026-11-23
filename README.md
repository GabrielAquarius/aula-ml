# Aula ML - Versionamento de Dados e Modelos

Projeto pratico de versionamento de dados, particoes e modelos utilizando Git e DVC.

## Pre-requisitos
- Python 3.10+
- Git
- DVC 3.x

## Configuracao do Armazenamento DVC
O armazenamento remoto local esta configurado na pasta irma ../dvc-storage:

    dvc remote add -d storage ../dvc-storage

## Restauracao de Versao (Exemplo com modelo-r1)
Para recuperar os artefatos exatos de uma versao anterior sem reexecutar o treinamento:

    git clone [https://github.com/GabrielAquarius/aula-ml.git](https://github.com/GabrielAquarius/aula-ml.git) aula-ml-restauracao
    cd aula-ml-restauracao
    git switch --detach modelo-r1
    dvc pull
