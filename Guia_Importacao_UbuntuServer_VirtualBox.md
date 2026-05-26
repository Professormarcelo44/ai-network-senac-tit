# Guia Prático — Importar a Máquina Virtual Ubuntu Server 22.04.4 LTS no Oracle VirtualBox 7.2

## Objetivo
Importar a imagem virtual `UbuntuServer-OnPremises.ova` no Oracle VirtualBox 7.2, configurar a rede em modo **Bridge (Ponte)** utilizando a rede cabeada do laboratório e iniciar a máquina virtual para acesso remoto via SSH.

---

# 🖥️ Pré-requisitos

Antes de iniciar, confirme os seguintes itens:

- ✅ Sistema operacional: Microsoft Windows 11
- ✅ Oracle VirtualBox 7.2 instalado
- ✅ Arquivo da máquina virtual disponível:

```text
Downloads\UbuntuServer-OnPremises.ova
```

- ✅ Cabo de rede conectado no computador do laboratório
- ✅ Permissão para utilização da rede local

---

# 📥 Etapa 1 — Abrir o Oracle VirtualBox

1. Clique no botão **Iniciar** do Windows.
2. Pesquise por:

```text
Oracle VirtualBox
```

3. Clique em **Oracle VirtualBox** para abrir.

---

# 📦 Etapa 2 — Importar a Imagem OVA

1. No menu superior clique em:

```text
Arquivo → Importar Appliance
```

ou utilize o ícone:

📂 **Importar**

---

## Selecionar o arquivo OVA

1. Clique em **Selecionar Arquivo**.
2. Navegue até a pasta:

```text
Downloads
```

3. Selecione o arquivo:

```text
UbuntuServer-OnPremises.ova
```

4. Clique em:

```text
Abrir
```

5. Clique em:

```text
Próximo
```

---

# ⚙️ Etapa 3 — Revisar Configurações da Importação

O VirtualBox exibirá as configurações da máquina virtual.

## Verifique:

- ✅ Nome da VM
- ✅ Sistema Operacional Linux Ubuntu (64-bit)
- ✅ Memória RAM
- ✅ Disco Virtual
- ✅ Controladora de Rede

---

## Importar

1. Clique em:

```text
Finalizar
```

2. Aguarde o processo de importação.

⏳ O tempo pode variar conforme o computador.

---

# 🌐 Etapa 4 — Configurar Rede em Modo Bridge (Ponte)

Após a importação:

1. Selecione a máquina virtual no VirtualBox.
2. Clique em:

```text
Configurações
```

ou no ícone:

⚙️ **Settings**

---

## Abrir Configurações de Rede

1. Clique na opção:

```text
Rede
```

---

## Configurar Adaptador 1

### Habilitar Adaptador

Confirme:

- ✅ Habilitar Placa de Rede

---

## Alterar modo de rede

Na opção:

```text
Conectado a:
```

Selecione:

```text
Placa em modo Bridge
```

---

## Selecionar a placa física do laboratório

Na opção:

```text
Nome:
```

Selecione a placa de rede cabeada do computador.

Exemplos:

```text
Intel(R) Ethernet Connection
Realtek PCIe GbE Family Controller
```

⚠️ Não selecionar adaptadores Wi-Fi ou Bluetooth.

---

## Confirmar configuração

1. Clique em:

```text
OK
```

---

# ▶️ Etapa 5 — Iniciar a Máquina Virtual

1. Selecione a VM.
2. Clique em:

```text
Iniciar
```

ou no ícone:

▶️ **Start**

---

# 🔐 Etapa 6 — Verificar Endereço IP do Ubuntu Server

Após a inicialização do Ubuntu Server:

Faça login utilizando o usuário e senha disponibilizados pelo Professor.

---

## Descobrir o endereço IP

No terminal do Ubuntu execute:

```bash
ip a
```

ou:

```bash
hostname -I
```

---

## Identificar IP da rede local

Exemplo:

```text
192.168.0.120
```

Esse será o IP utilizado para acesso remoto via SSH.

---

# 🖧 Etapa 7 — Testar Conectividade

No Windows:

1. Pressione:

```text
Windows + R
```

2. Digite:

```text
cmd
```

3. Clique em:

```text
OK
```

---

## Testar comunicação com a VM

No Prompt de Comando execute:

```cmd
ping IP_DA_VM
```

Exemplo:

```cmd
ping 192.168.0.120
```

---

# 🔑 Etapa 8 — Acessar via SSH

No Windows 11 o cliente SSH já vem instalado.

No Prompt de Comando execute:

```bash
ssh usuario@IP_DA_VM
```

Exemplo:

```bash
ssh aluno@192.168.0.120
```

---

## Primeiro acesso

Quando aparecer:

```text
Are you sure you want to continue connecting (yes/no)?
```

Digite:

```text
yes
```

---

## Inserir senha

Digite a senha do usuário Linux.

⚠️ A senha não aparece na tela durante a digitação.

---

# ✅ Resultado Esperado

Ao finalizar:

- ✅ Máquina virtual importada com sucesso
- ✅ Rede Bridge configurada
- ✅ Ubuntu Server conectado na rede local
- ✅ Comunicação via ping funcionando
- ✅ Acesso remoto SSH operacional

---

# 📌 Observações Importantes

- Utilize sempre a rede cabeada do laboratório.
- Não altere configurações avançadas sem orientação do Professor.
- O endereço IP pode mudar dependendo do DHCP da rede.
- Caso o SSH não funcione, verificar:
  - Conectividade da rede
  - Firewall do Windows
  - Serviço SSH do Ubuntu

---

# 🎓 SENAC São Paulo — Unidade Lapa Tito
Curso Livre de Inteligência Artificial Voltada a Redes de Computadores

Material de apoio para aulas práticas utilizando GNU/Linux Ubuntu Server 22.04.4 LTS no Oracle VirtualBox 7.2.
