# 📋 Documentação Técnica de Servidor GNU/Linux
### Ubuntu Server 24.04.4 LTS — Ambiente Docker-CE
> Gerado para fins de auditoria, troubleshooting e gestão de ativos de TI

---

## 1. 🖥️ Informações Gerais do Servidor

| Categoria | Descrição | Configuração |
|-----------|-----------|--------------|
| 🖥️ Geral | Nome do Servidor (Hostname) | `ctlinux01` |
| 🖥️ Geral | Sistema Operacional | Ubuntu 24.04.4 LTS (Noble Numbat) |
| 🖥️ Geral | Kernel | Linux 6.8.0-106-generic |
| 🖥️ Geral | Arquitetura | x86-64 (64 bits) |
| 🖥️ Geral | Tipo de Máquina | Máquina Virtual (VM) |
| 🖥️ Geral | Uptime (Tempo Ativo) | 48 minutos com 2 usuários ativos |
| 🖥️ Geral | Carga do Sistema (Load Average) | 0.00 / 0.00 / 0.00 (ocioso) |
| 🖥️ Geral | ID da Máquina | `05c2865e767d44c4870777b482ba0652` |
| 🖥️ Geral | Boot ID | `a69a259f420941678c605f28b8e0a737` |

> 💡 **Para o gestor:** Este servidor é uma máquina virtual (como um computador dentro de outro computador), rodando Ubuntu — um sistema operacional Linux amplamente usado em ambientes corporativos. Ele estava em funcionamento há apenas 48 minutos no momento da coleta dos dados, o que indica uma reinicialização recente. A carga do sistema estava praticamente zero, ou seja, o servidor estava ocioso e com folga de processamento.

---

## 2. ⚙️ Informações de Hardware do Servidor

| Categoria | Descrição | Configuração |
|-----------|-----------|--------------|
| ⚙️ Hardware | Fabricante do Hardware | innotek GmbH |
| ⚙️ Hardware | Modelo do Hardware | VirtualBox |
| ⚙️ Hardware | Plataforma de Virtualização | Oracle VirtualBox |
| ⚙️ Hardware | Versão do Firmware | VirtualBox |
| ⚙️ Hardware | Data do Firmware | 01/12/2006 |
| ⚙️ Hardware | Memória RAM Total | 3.915 MB (~4 GB) |
| ⚙️ Hardware | Memória RAM em Uso | 525 MB |
| ⚙️ Hardware | Memória RAM Livre | 3.021 MB |
| ⚙️ Hardware | Memória RAM Disponível | 3.390 MB |
| ⚙️ Hardware | Swap Total | 3.914 MB (~4 GB) |
| ⚙️ Hardware | Swap em Uso | 0 MB |
| ⚙️ Hardware | Disco Principal (sda) | 50 GB |
| ⚙️ Hardware | Partição de Boot (/boot) | 2 GB — 198 MB usados (11%) |
| ⚙️ Hardware | Partição Principal (/) | 48 GB — 8,3 GB usados (19%) |
| ⚙️ Hardware | Espaço Livre no Disco Principal | 37 GB disponíveis |

> 💡 **Para o gestor:** O servidor possui 4 GB de memória RAM e está usando apenas 525 MB, ou seja, está bem folgado em termos de memória. O disco de 50 GB está utilizando apenas 19% do espaço total, com 37 GB ainda livres — sem risco imediato de esgotamento de armazenamento. A memória swap (reserva de emergência de memória) não está sendo utilizada, o que é um bom sinal de saúde do sistema.

---

## 3. 🌐 Informações de Rede do Servidor

### 3.1 Interfaces de Rede

| Categoria | Descrição | Configuração |
|-----------|-----------|--------------|
| 🌐 Rede | Status de Conectividade | Offline (sem rota para internet) |
| 🌐 Rede | Interface Loopback (lo) | 127.0.0.1/8 — ativa, apenas uso interno |
| 🌐 Rede | Interface Principal (enp0s3) | 10.24.82.221/24 — ativa |
| 🌐 Rede | MAC Address (enp0s3) | 08:00:27:f1:74:10 (Intel Corporation) |
| 🌐 Rede | Gateway Padrão | 10.24.82.1 |
| 🌐 Rede | Interface Docker (docker0) | 172.17.0.1/16 — ativa (bridge interna) |
| 🌐 Rede | Interface Virtual Docker (veth4ffa819) | Conectada ao bridge docker0 |

### 3.2 DNS (Resolução de Nomes)

| Categoria | Descrição | Configuração |
|-----------|-----------|--------------|
| 🌐 DNS | Servidor DNS Primário | 8.8.8.8 (Google) |
| 🌐 DNS | Servidor DNS Secundário | 8.8.4.4 (Google) |
| 🌐 DNS | Modo resolv.conf | stub |
| 🌐 DNS | DNS sobre TLS | Desativado |
| 🌐 DNS | DNSSEC | Não suportado |

### 3.3 Portas em Escuta (Firewall / Exposição)

| Categoria | Descrição | Configuração |
|-----------|-----------|--------------|
| 🔒 Portas | SSH (acesso remoto) | Porta 22 — escutando em 0.0.0.0 (todas as interfaces) |
| 🔒 Portas | DNS local (stub resolver) | Porta 53 — escutando em 127.0.0.54 |
| 🔒 Portas | Aplicação / Serviço Docker | Porta 9000 — escutando em 0.0.0.0 (todas as interfaces) |

> 💡 **Para o gestor:** Este servidor está conectado à rede interna com o endereço IP `10.24.82.221`. O servidor de DNS (responsável por traduzir nomes de sites em endereços de rede) está configurado com os servidores do Google. A porta 22 (acesso remoto SSH) e a porta 9000 (provavelmente painel do Portainer — gerenciador Docker) estão abertas e acessíveis pela rede. **Atenção:** Recomenda-se revisar se o acesso SSH à porta 22 está protegido por autenticação forte, já que está exposta para toda a rede.

---

## 4. 🔧 Informações de Serviços e Processos

| Categoria | Serviço | Status | Descrição |
|-----------|---------|--------|-----------|
| 🐳 Docker | `containerd.service` | ✅ Ativo | Motor de containers (núcleo do Docker) |
| 🐳 Docker | `docker.service` | ✅ Ativo | Docker — plataforma de containers |
| 🐳 Docker | `portainer.service` | ✅ Ativo | Painel web de gerenciamento Docker |
| 🔒 Segurança | `ssh.service` | ✅ Ativo | Servidor SSH (acesso remoto seguro) |
| 🔒 Segurança | `polkit.service` | ✅ Ativo | Gerenciador de autorizações do sistema |
| 🔒 Segurança | `fwupd.service` | ✅ Ativo | Daemon de atualização de firmware |
| 🖥️ Sistema | `systemd-networkd.service` | ✅ Ativo | Gerenciamento de rede |
| 🖥️ Sistema | `systemd-resolved.service` | ✅ Ativo | Resolução de nomes de rede (DNS) |
| 🖥️ Sistema | `systemd-timesyncd.service` | ✅ Ativo | Sincronização de horário pela rede |
| 🖥️ Sistema | `systemd-udevd.service` | ✅ Ativo | Gerenciamento de dispositivos |
| 🖥️ Sistema | `systemd-journald.service` | ✅ Ativo | Serviço de logs do sistema |
| 🖥️ Sistema | `systemd-logind.service` | ✅ Ativo | Gerenciamento de sessões de usuário |
| 🖥️ Sistema | `rsyslog.service` | ✅ Ativo | Serviço de log do sistema |
| 🖥️ Sistema | `cron.service` | ✅ Ativo | Agendador de tarefas automáticas |
| 🖥️ Sistema | `dbus.service` | ✅ Ativo | Barramento de mensagens do sistema |
| 🖥️ Sistema | `multipathd.service` | ✅ Ativo | Gerenciamento de múltiplos caminhos de disco |
| 🖥️ Sistema | `udisks2.service` | ✅ Ativo | Gerenciador de discos |
| 🖥️ Sistema | `upower.service` | ✅ Ativo | Daemon de gerenciamento de energia |
| 🖥️ Sistema | `ModemManager.service` | ✅ Ativo | Gerenciador de modems |
| 🖥️ Sistema | `getty@tty1.service` | ✅ Ativo | Terminal de login físico (tty1) |
| 🖥️ Sistema | `user@1000.service` | ✅ Ativo | Sessão do usuário UID 1000 |
| 🔄 Atualização | `unattended-upgrades.service` | ✅ Ativo | Serviço de atualizações automáticas |

> 💡 **Para o gestor:** O servidor está rodando ativamente o Docker e o Portainer. O **Docker** é a plataforma que executa os containers (ambientes isolados de aplicações), e o **Portainer** é um painel visual acessível pelo navegador web na porta 9000, que permite gerenciar esses containers sem usar linha de comando. Todos os 22 serviços monitorados estão em funcionamento normal. O servidor também possui atualização automática de segurança ativada, o que é uma boa prática.

---

## 5. 🔄 Informações de Software e Atualização

| Categoria | Descrição | Configuração |
|-----------|-----------|--------------|
| 🔄 Atualização | Serviço de Atualizações Automáticas | `unattended-upgrades` — ✅ Ativo |
| 🔄 Atualização | Modo de Operação | Atualizações de segurança aplicadas automaticamente |
| 🔄 Atualização | Atualização de Firmware | `fwupd` — ✅ Ativo |
| 🔄 Atualização | Sincronização de Horário (NTP) | `systemd-timesyncd` — ✅ Ativo |
| 🔄 Atualização | Versão do SO | Ubuntu 24.04.4 LTS (suporte até Abril/2029) |
| 🔄 Atualização | Versão do Kernel | 6.8.0-106-generic (compilado em 06/03/2026) |

> 💡 **Para o gestor:** Este servidor está configurado para aplicar atualizações de segurança automaticamente, sem necessidade de intervenção manual — isso reduz o risco de vulnerabilidades. O sistema operacional Ubuntu 24.04 LTS tem suporte garantido pela Canonical (fabricante do Ubuntu) até **abril de 2029**, o que garante estabilidade e correções de segurança por vários anos. O relógio do servidor também está sincronizado automaticamente pela internet, o que é fundamental para logs e auditorias precisas.

---

## 📌 Resumo Executivo

| Indicador | Status |
|-----------|--------|
| 🟢 Sistema Operacional | Ubuntu 24.04.4 LTS — Suportado até 2029 |
| 🟢 Saúde Geral | Servidor estável, carga baixa |
| 🟢 Memória RAM | 13% em uso — folgada |
| 🟢 Disco | 19% em uso — sem risco imediato |
| 🟢 Docker | Ativo e operacional |
| 🟢 Portainer | Ativo na porta 9000 |
| 🟢 Atualizações Automáticas | Ativas |
| 🟡 Acesso SSH | Porta 22 aberta — verificar política de acesso |
| 🔴 Conectividade Externa | Sem rota para internet no momento da coleta |

> 💡 **Para o gestor:** De forma geral, o servidor está saudável e bem configurado. Os dois pontos de atenção são: (1) a porta de acesso remoto SSH está aberta para a rede — recomenda-se garantir que apenas usuários autorizados consigam acessar; e (2) no momento da coleta dos dados, o servidor não possuía rota para a internet, o que pode impedir atualizações automáticas e comunicações externas.

---
*Documentação gerada com base em coleta manual de dados do servidor `ctlinux01` — Ubuntu Server 24.04.4 LTS*
