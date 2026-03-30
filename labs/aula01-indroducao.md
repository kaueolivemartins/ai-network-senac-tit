🧩 1) Importar a máquina virtual (.OVA)<br>
Abra o Oracle VM VirtualBox 7.2<br>
No menu superior: Arquivo → Importar Appliance<br>
Clique em 📂 Escolher arquivo<br>

Navegue até:0<br>

Downloads → UbuntuServer-OnPremises.ova<br>
Clique em Avançar<br>
Na tela de configurações:<br>
Pode manter padrão (ou ajustar RAM/CPU se necessário)<br>
Clique em Importar<br>
Aguarde a conclusão<br>

✔ Resultado: VM aparecerá na lista lateral

⚙️ 2) Configurar rede em modo Bridge (Ponte)
Selecione a VM importada
Clique em Configurações
Vá em Rede
Em Adaptador 1:
✔ Marcar: Habilitar placa de rede
🔽 Conectado a: Placa em modo Bridge
🔽 Nome: selecione a interface cabeada
(ex: Ethernet, Realtek, Intel(R) Ethernet)

⚠️ Importante:

NÃO usar Wi-Fi
Escolher placa física cabeada do laboratório
Clique em OK

✔ Resultado: VM receberá IP da mesma rede do laboratório (DHCP)

▶️ 3) Iniciar a máquina virtual
Selecione a VM
Clique em Iniciar

Aguarde o boot do Ubuntu Server 22.04.4 LTS

🌐 4) Descobrir o IP da máquina virtual

Após login no terminal da VM:

Execute:

ip a

Procure por:

eth0 ou enp0s3 → inet 192.168.x.x

✔ Esse é o IP da VM

🔐 5) Acessar via SSH (do Windows)

No Windows 11:

Abra o Prompt de Comando ou PowerShell
Execute:
ssh usuario@IP_DA_VM

Exemplo:

ssh aluno@192.168.0.25
Digite a senha quando solicitado

✔ Acesso remoto estabelecido

🧪 6) Teste rápido de conectividade

Se o SSH falhar:

Testar ping
ping 192.168.x.x
Verificar serviço SSH na VM
sudo systemctl status ssh

Se necessário:

sudo systemctl start ssh
⚠️ Problemas comuns (checagem rápida)
❌ Sem IP → Bridge configurado errado
❌ IP 10.x.x.x ou 192.168.56.x → está em NAT/Host-only
❌ Sem SSH → serviço não iniciado
❌ Não conecta → firewall da rede do laboratório
✅ Resultado esperado
VM importada corretamente
Rede em Bridge funcionando
IP válido da rede local
Acesso via SSH ativo

---
🧩 1) Importar a imagem (.OVA)
Abrir VirtualBox
Menu: Arquivo → Importar Appliance

📂 Selecionar:

Downloads → UbuntuServer-OnPremises.ova
Avançar
(Opcional) Ajustar recursos iniciais
Importar

✔ VM aparecerá na lista

⚡ 2) Otimização de desempenho (IMPORTANTE)

Hardware disponível (i7-14700K, 32GB RAM, NVMe) permite ajuste agressivo.

🔧 Sistema → Placa-mãe
🧠 Memória RAM: 8192 MB (8GB)
(pode subir até 12GB se necessário)
🔧 Sistema → Processador
⚙️ CPUs: 4 a 6 núcleos
✔ Habilitar PAE/NX
🔧 Sistema → Aceleração
✔ VT-x/AMD-V: ativado
✔ Paginação aninhada: ativado
🎮 Vídeo
Memória de vídeo: 128 MB
Controlador: VMSVGA
💽 Armazenamento
Controlador: SATA ou NVMe (se disponível)
✔ Ativar:
Cache de I/O do host
🌐 Rede (pré-ajuste)

Deixar para próxima etapa (Bridge)

✔ Resultado: VM com melhor uso de CPU, RAM e disco

🌐 3) Configurar rede em Bridge (Ponte)
Configurações → Rede
Adaptador 1:
✔ Habilitar placa de rede
🔽 Conectado a: Placa em modo Bridge
🔽 Nome: selecionar Ethernet (cabeada)

⚠️ Não usar Wi-Fi

✔ VM ficará na mesma rede do laboratório

▶️ 4) Iniciar a VM
Selecionar VM
Clique em Iniciar

Aguardar boot do Ubuntu Server 22.04.4 LTS

🌐 5) Descobrir o IP da VM

No terminal da VM:

ip a

Identificar:

eth0 ou enp0s3 → inet 192.168.x.x

✔ Esse é o IP válido da rede

🔐 6) Acesso remoto via SSH

No Windows:

Abrir PowerShell
Executar:
ssh usuario@IP_DA_VM

Exemplo:

ssh aluno@192.168.0.50
🧪 7) Validação rápida
Testar conectividade:
ping 192.168.x.x
Verificar SSH na VM:
sudo systemctl status ssh

Se necessário:

sudo systemctl enable ssh
sudo systemctl start ssh
🚀 Ajustes extras (opcional, mas recomendado)
⚡ Melhorar rede
Adaptador → Tipo:
Paravirtualized Network (virtio-net)
⚡ Melhorar disco

Dentro da VM:

sudo fstrim -av
⚡ Atualizar sistema
sudo apt update && sudo apt upgrade -y
⚠️ Problemas comuns
❌ IP 10.x / 192.168.56.x → está em NAT/Host-only
❌ Sem IP → Bridge incorreto
❌ SSH não conecta → serviço parado
❌ Sem rede → cabo desconectado no laboratório
✅ Resultado final esperado
VM importada corretamente
Performance otimizada (CPU/RAM/Disco)
Rede Bridge funcional
IP válido na rede local
Acesso SSH funcionando

---


| 🖥️ Servidor        | 🌐 Endereço IP   | 📏 Máscara de Rede | 🚪 Gateway       | 🔎 DNS            | 📝 Observação                  |
|-------------------|----------------|--------------------|-----------------|------------------|-------------------------------|
| 🟢 Servidor 01     | 10.24.82.10    | 255.255.255.0      | 10.24.82.1      | 10.24.40.190     | Uso geral / serviços principais |
| 🔵 Servidor 02     | 10.24.82.11    | 255.255.255.0      | 10.24.82.1      | 10.24.40.190     | Backup / serviços secundários  |

---
