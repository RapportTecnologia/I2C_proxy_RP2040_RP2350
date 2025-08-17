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
