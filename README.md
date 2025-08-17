# I2C_proxy_RP2040_RP2350
Um proxy para o I2C do RP2040 e RP2350, ele pode ser ajustado facilmente para outros microcontroladores abstraindo assim o acesso HAL sem muito overhead.

## Como obter este módulo (via workspace principal)

Para garantir compatibilidade de paths e dependências entre projetos que consomem esta biblioteca, recomenda-se clonar o repositório raiz (monorepo) com submódulos:

```bash
git clone --recurse-submodules https://github.com/RapportTecnologia/Sensores_e_Atuadores_do_Kit_BitDogLab.git Sensores_e_Atuadores_do_KIT
cd Sensores_e_Atuadores_do_KIT
git submodule update --init --recursive
```

Para atualizar submódulos (quando aplicável):

```bash
git submodule update --remote --merge --recursive
```

Caso use este repositório isoladamente, ajuste manualmente referências relativas usadas por projetos que esperam `../I2C` a partir do diretório do módulo consumidor.

## Visão Geral

Biblioteca/proxy de I2C com API simples (estilo `Wire`) para facilitar portabilidade entre HALs. Fornece `begin()`, `setClock()`, `beginTransmission()`, `write()`, `requestFrom()`, `read()`, etc.

## Estrutura do projeto

```
I2C-proxy-RP2040-RP2350/
├─ I2C.h
├─ I2C.cpp
├─ CMakeLists.txt
└─ Doxyfile (quando aplicável)
```

## Pré-requisitos

- Pico SDK configurado (para projetos que o utilizem)
- CMake 3.13+ (para build com CMake)

## Documentação

Para gerar documentação local com Doxygen (se configurado):

```bash
doxygen Doxyfile
```

## Licença

Consulte o arquivo `LICENSE` deste repositório ou o arquivo `LICENSE` na raiz do workspace principal para os termos.

## Autores e Colaboradores

- Carlos Delfino — consultoria@carlosdelfino.eti.br — GitHub: [@carlosdelfino](https://github.com/carlosdelfino)
