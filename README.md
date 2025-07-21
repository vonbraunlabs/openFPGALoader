# openFPGALoader

Este é um fork do [openFPGALoader]([github.com/phdussud/pico-dirtyJtag](https://github.com/trabucayre/openFPGALoader)), tendo um apenas um patch para o funcionamento da versão em webassembly para usar a tangprimer20k.

## 🛠️ Configuração Rápida

### Pré-requisitos

- As dependências para compilação estão listados no passo 1 da próxima seção.


### Compilação do projeto

Para mais detalhes, [siga as instruções completas](https://trabucayre.github.io/openFPGALoader/guide/install.html)

Aqui vai uma versão resumida:

1. **Instale as dependências**
   ```bash
   sudo apt install \
    git \
    gzip \
    libftdi1-2 \
    libftdi1-dev \
    libhidapi-hidraw0 \
    libhidapi-dev \
    libudev-dev \
    zlib1g-dev \
    cmake \
    pkg-config \
    make \
    g++
   ```
2. **No diretório do projeto, faça a compilação**

```bash
mkdir build
cd build
cmake .. # add -DBUILD_STATIC=ON to build a static version
         # add -DENABLE_UDEV=OFF to disable udev support and -d /dev/xxx
         # add -DENABLE_CMSISDAP=OFF to disable CMSIS DAP support
cmake --build .
# or
make -j$(nproc)
```
