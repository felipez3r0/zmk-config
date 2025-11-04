# ZMK Firmware - Lily58 Configuration

Configuração personalizada do firmware ZMK para o teclado mecânico split Lily58 com controlador Nice!Nano v2.

## 🎯 Sobre o Projeto

Este repositório contém a configuração do firmware ZMK (Zephyr Mechanical Keyboard) para o teclado Lily58. O ZMK é um firmware de código aberto focado em teclados sem fio, oferecendo baixo consumo de energia e suporte Bluetooth.

## ⚙️ Hardware

- **Teclado**: Lily58 (58 teclas split)
- **Controlador**: Nice!Nano v2
- **Display**: OLED habilitado com tela de status customizada
- **Encoder**: Rotary encoder habilitado (controle de volume)
- **Conectividade**: Bluetooth Low Energy

## 🔧 Características Habilitadas

### Funcionalidades Principais
- ✅ Display OLED com status customizado
- ✅ Encoder rotativo (controle de volume)
- ✅ Potência de transmissão Bluetooth aumentada (+8dBm)
- ✅ Conexões BLE experimentais otimizadas
- ✅ ZMK Studio desbloqueado (sem trava)
- ✅ 2 camadas de teclas personalizadas

### Layout de Teclas

#### Camada 0 - Default Layer
Layout principal com teclas alfanuméricas, modificadores e acesso à camada inferior.

**Características**:
- Layout QWERTY padrão
- Modificadores: Ctrl, Shift, Alt, GUI
- Teclas de navegação: Home, End
- Backspace e Enter nas posições do polegar

#### Camada 1 - Lower Layer
Camada com teclas de função, símbolos e controles do sistema.

**Características**:
- Teclas de função (F1-F12)
- Controles Bluetooth (limpar, selecionar dispositivos)
- Controles de energia externa (on/off/toggle)
- Símbolos especiais e parênteses
- Macro de screenshot (⌘+⇧+4)

## 📦 Estrutura do Projeto

```
zmk-config/
├── build.yaml          # Configuração de build do GitHub Actions
├── config/
│   ├── lily58.conf     # Configurações do hardware
│   ├── lily58.keymap   # Mapeamento de teclas
│   └── west.yml        # Gerenciamento de dependências
├── boards/shields/     # Shields personalizados (se houver)
└── zephyr/
    └── module.yml      # Configuração do módulo Zephyr
```

## 🚀 Como Usar

### Compilação Automática (GitHub Actions)

1. Faça fork deste repositório
2. Clone o fork para sua máquina local
3. Faça as modificações desejadas em `config/lily58.keymap`
4. Commit e push das alterações
5. O GitHub Actions irá compilar automaticamente o firmware
6. Baixe os arquivos `.uf2` gerados na aba **Actions**

### Flashando o Firmware

1. Baixe os arquivos `lily58_left-nice_nano_v2.uf2` e `lily58_right-nice_nano_v2.uf2`
2. Conecte o lado esquerdo do teclado via USB
3. Pressione o botão reset duas vezes rapidamente
4. Copie o arquivo `lily58_left-nice_nano_v2.uf2` para o volume USB que apareceu
5. Repita o processo para o lado direito

## ✏️ Personalização

### Modificando o Layout

Edite o arquivo `config/lily58.keymap` para alterar o mapeamento de teclas. Consulte a [documentação do ZMK](https://zmk.dev/docs/keymaps) para mais informações sobre behaviors e keycodes.

### Ajustando Configurações

Edite `config/lily58.conf` para modificar:
- Configurações de display
- Configurações de encoder
- Configurações de Bluetooth
- Outras opções de hardware

## 📚 Recursos Úteis

- [Documentação Oficial do ZMK](https://zmk.dev/)
- [Lista de Keycodes](https://zmk.dev/docs/keymaps/keycodes)
- [Behaviors Disponíveis](https://zmk.dev/docs/keymaps/behaviors)
- [Configuração de Bluetooth](https://zmk.dev/docs/features/bluetooth)

## 📄 Licença

Este projeto está licenciado sob a licença MIT - veja os cabeçalhos dos arquivos para detalhes.

---

**Feito com ❤️ para a comunidade de teclados mecânicos**
