# 📋 Documentação Técnica do Servidor Ubuntu Docker

**Servidor:** ctlinux01  
**Data da Coleta:** Junho de 2026  
**Ambiente:** Produção - Container Docker

---

## 1. 🖥️ Informações Gerais do Servidor

| Categoria | Descrição | Configuração |
|-----------|-----------|--------------|
| 🐧 **Sistema Operacional** | Distribuição Linux | Ubuntu 24.04.4 LTS (Noble Numbat) |
| 📦 **Versão do SO** | Código de lançamento | 24.04 |
| 🔧 **Kernel** | Versão do núcleo do sistema | 6.8.0-107-generic #107-Ubuntu |
| 🏗️ **Arquitetura** | Tipo de processador | x86-64 (64 bits) |
| 🏢 **Tipo de Máquina** | Ambiente de execução | Máquina Virtual (VirtualBox) |
| 🌐 **Hypervisor** | Virtualizador | Oracle VirtualBox |
| ⏱️ **Tempo de Atividade** | Quanto tempo servidor está ligado | 1 hora e 59 minutos |
| 👥 **Usuários Conectados** | Quantidade de acessos simultâneos | 10 usuários |
| 📊 **Carga Média** | Processamento em uso (últimos 1, 5 e 15 min) | 0.06 / 0.02 / 0.00 |

### 📌 Interpretação para Gestores:
Este servidor é uma máquina virtual baseada em Ubuntu, versão recente e estável, otimizada para produção. O sistema está em funcionamento há quase 2 horas e está operando com baixa utilização de processamento. A máquina suporta até 10 usuários simultâneos sem apresentar problemas de desempenho.

---

## 2. 💾 Informações de Hardware do Servidor

| Categoria | Descrição | Configuração |
|-----------|-----------|--------------|
| 🧠 **Memória RAM** | Memória total disponível | 3.915 GB |
| ✅ **RAM em Uso** | Memória sendo utilizada no momento | 582 MB (14,8%) |
| 🟢 **RAM Disponível** | Memória livre para usar | 3.333 GB |
| 💫 **Cache/Buffer** | Memória para otimização | 615 MB |
| 🔄 **Swap Total** | Espaço em disco para quando RAM fica cheia | 3.914 GB |
| 📀 **Disco Rígido Principal** | Capacidade total de armazenamento | 50 GB |
| 📊 **Espaço em Disco Usado** | Quanto está sendo utilizado | 8.5 GB (19%) |
| 🆓 **Espaço em Disco Livre** | Quanto ainda tem disponível | 37 GB (81%) |
| 🖴 **Tipo de Armazenamento** | Sistema de gerenciamento | LVM (Logical Volume Manager) |
| 🔌 **Discos Detectados** | Quantidade de mídias conectadas | 1 disco SATA + 1 drive óptico (CDROM) |

### 📌 Interpretação para Gestores:
O servidor possui capacidade moderada com 4 GB de RAM, sendo apenas 14,8% utilizado no momento. O espaço em disco está bastante disponível (81% livre), o que é saudável. O servidor não está próximo de atingir limites críticos. Recomenda-se monitorar o uso em horários de pico.

---

## 3. 🌐 Informações de Rede do Servidor

| Categoria | Descrição | Configuração |
|-----------|-----------|--------------|
| 🔗 **Interface Principal** | Nome da placa de rede | enp0s3 |
| 📍 **Endereço IPv4** | IP da rede corporativa | 10.24.82.200/24 |
| 🎯 **Gateway Padrão** | Rota para acesso à internet | 10.24.82.1 |
| 📡 **Broadcast** | Endereço de difusão | 10.24.82.255 |
| 🔐 **MAC Address** | Identificador único da placa | 08:00:27:42:90:a5 |
| 🐳 **Interface Docker** | Interface para containers | docker0 |
| 🖧 **Rede Docker** | Faixa de IPs para containers | 172.17.0.0/16 |
| 🔗 **Ponte Virtual Docker** | Interface virtual para containers | veth1321de1 |
| 🌍 **Servidor DNS 1** | Resolvedor de nomes principal | 8.8.8.8 |
| 🌍 **Servidor DNS 2** | Resolvedor de nomes secundário | 8.8.4.4 |
| 📶 **Status da Rede** | Estado da conexão | UP (Ativa) |
| 🔗 **MTU** | Tamanho máximo de pacote | 1500 bytes |

### 📌 Interpretação para Gestores:
O servidor está conectado à rede corporativa com IP 10.24.82.200. Está totalmente operacional e pronto para receber/enviar dados. O Docker está configurado com sua própria rede interna (172.17.0.0/16) para gerenciar os containers isoladamente. Os servidores DNS utilizados são públicos (Google), garantindo resolução de nomes confiável.

---

## 4. ⚙️ Informações de Serviços e Processos

### 4.1 Serviços Críticos em Execução

| Categoria | Descrição | Status |
|-----------|-----------|--------|
| 🐳 **Docker** | Engine para gerenciar containers | ✅ Ativo e Rodando |
| 🔐 **SSH** | Serviço de acesso remoto seguro | ✅ Ativo e Rodando |
| 📧 **Syslog (rsyslog)** | Serviço de registros de logs | ✅ Ativo e Rodando |
| 🔄 **Portainer** | Interface gráfica para gerenciar Docker | ✅ Ativo e Rodando |
| ⏰ **Cron** | Agendador de tarefas automáticas | ✅ Ativo e Rodando |
| 🕐 **NTP (systemd-timesyncd)** | Sincronizador de horário do sistema | ✅ Ativo e Rodando |
| 📋 **D-Bus** | Sistema de comunicação entre serviços | ✅ Ativo e Rodando |
| 🔌 **Systemd-resolved** | Serviço de DNS do sistema | ✅ Ativo e Rodando |

### 4.2 Serviços de Suporte e Gerenciamento

| Categoria | Descrição | Status |
|-----------|-----------|--------|
| 💿 **UDisks2** | Gerenciador de discos | ✅ Ativo e Rodando |
| ⚡ **UPower** | Gerenciador de energia | ✅ Ativo e Rodando |
| 🔐 **Polkit** | Gerenciador de permissões | ✅ Ativo e Rodando |
| 🛠️ **ModemManager** | Gerenciador de modem/conexão | ✅ Ativo e Rodando |
| 🔧 **Multipath** | Gerenciador de caminhos de disco | ✅ Ativo e Rodando |
| 📦 **PackageKit** | Gerenciador de pacotes de software | ✅ Ativo e Rodando |
| 🔄 **systemd-networkd** | Configurador de rede | ✅ Ativo e Rodando |
| 🚀 **Unattended-upgrades** | Sistema de atualizações automáticas | ✅ Ativo e Rodando |
| 🔧 **fwupd** | Atualizador de firmware | ✅ Ativo e Rodando |

### 4.3 Portas Abertas (Serviços em Escuta)

| Porta | Protocolo | Serviço | Status |
|-------|-----------|---------|--------|
| 22 | TCP | SSH (Acesso Remoto) | 🟢 Ativo |
| 53 | TCP/UDP | DNS | 🟢 Ativo |
| 9000 | TCP | Portainer (Gerenciamento Docker) | 🟢 Ativo |

### 📌 Interpretação para Gestores:
O servidor possui todos os serviços essenciais em execução. Docker está rodando corretamente para gerenciar containers. SSH está ativo para acesso remoto seguro. Portainer fornece uma interface visual para gerenciar os containers sem usar linhas de comando. Todas as portas críticas estão abiertas e monitoradas. O sistema realiza atualizações automáticas regularmente, mantendo a segurança em dia.

---

## 5. 📦 Informações de Softwares e Atualizações

### 5.1 Status de Atualização do Sistema

| Categoria | Descrição | Status |
|-----------|-----------|--------|
| 🔄 **Atualizações Disponíveis** | Pacotes que podem ser atualizados | 17 pacotes |
| ⚠️ **Sistema** | Status geral de atualização | Parcialmente Desatualizado |
| 🔐 **Crítico** | Atualizações de segurança pendentes | Sim |
| 📊 **Última Verificação** | Quando foi feita a última verificação | Junho de 2026 |

### 5.2 Pacotes com Atualizações Disponíveis

| Pacote | Versão Atual | Versão Disponível | Tipo |
|--------|--------------|-------------------|------|
| systemd | 255.4-1ubuntu8.14 | 255.4-1ubuntu8.15 | Sistema |
| udev | 255.4-1ubuntu8.14 | 255.4-1ubuntu8.15 | Sistema |
| systemd-resolved | 255.4-1ubuntu8.14 | 255.4-1ubuntu8.15 | Rede |
| systemd-timesyncd | 255.4-1ubuntu8.14 | 255.4-1ubuntu8.15 | Sistema |
| systemd-sysv | 255.4-1ubuntu8.14 | 255.4-1ubuntu8.15 | Sistema |
| systemd-dev | 255.4-1ubuntu8.14 | 255.4-1ubuntu8.15 | Desenvolvimento |
| netplan.io | 1.1.2-8ubuntu1~24.04.1 | 1.1.2-8ubuntu1~24.04.2 | Rede |
| netplan-generator | 1.1.2-8ubuntu1~24.04.1 | 1.1.2-8ubuntu1~24.04.2 | Rede |
| python3-netplan | 1.1.2-8ubuntu1~24.04.1 | 1.1.2-8ubuntu1~24.04.2 | Desenvolvimento |
| nftables | 1.0.9-1build1 | 1.0.9-1ubuntu0.1 | Firewall |
| lshw | 02.19.git.2021.06.19.996aaad9c7-2build3 | 02.19.git.2021.06.19.996aaad9c7-2ubuntu0.24.04.1 | Hardware |
| sosreport | 4.9.2-0ubuntu0~24.04.1 | 4.10.2-0ubuntu0~24.04.1 | Diagnóstico |
| ubuntu-drivers-common | 1:0.9.7.6ubuntu3.5 | 1:0.9.7.6ubuntu3.6 | Driver |

### 📌 Interpretação para Gestores:
Existem 17 atualizações de software disponíveis, principalmente para o sistema operacional (systemd) e componentes de rede. Recomenda-se agendar uma janela de manutenção para aplicar estas atualizações, pois melhoram estabilidade e segurança do servidor. As atualizações automáticas estão ativas, mas estas específicas precisam de verificação antes da aplicação.

---

## 📊 Resumo Executivo

### ✅ Pontos Positivos:
- ✓ Sistema operacional recente e estável (Ubuntu 24.04.4 LTS)
- ✓ Docker instalado e funcionando corretamente
- ✓ Espaço em disco abundante (81% livre)
- ✓ Memória RAM com uso moderado (14,8%)
- ✓ Todos os serviços críticos em operação
- ✓ Conectividade de rede ativa e estável
- ✓ Sistema de atualizações automáticas ativo

### ⚠️ Recomendações:
1. Aplicar as 17 atualizações de software disponíveis em uma janela de manutenção
2. Manter monitoramento de uso de memória em períodos de pico
3. Realizar backups regularmente dos dados dos containers
4. Revisar configurações de segurança de rede (firewall)
5. Monitorar logs de Docker e serviços regularmente

### 🔍 Próximas Ações:
- Agendar atualização do sistema
- Implementar monitoramento contínuo de performance
- Documentar políticas de backup
- Treinar equipe nos procedimentos de troubleshooting do Docker

---

**Documento Gerado:** Junho de 2026  
**Responsável pela Coleta:** SysAdmin de Redes - Ubuntu Server & Docker  
**Classificação:** Documentação Técnica Interna
