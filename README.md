# Resumo - Computação em Nuvem
Este repositório contém um resumo introdutório sobre conceitos fundamentais de computação em nuvem, destacando pontos importantes para iniciantes.

## O que é Computação em Nuvem
Computação em nuvem é o fornecimento de serviços de TI (como servidores, armazenamento, bancos de dados e redes) pela internet.  
Permite que recursos sejam utilizados sob demanda, com escalabilidade e pagamento conforme o uso.

## Responsabilidade Compartilhada
Na nuvem, a segurança e a gestão são divididas entre **provedor** (Azure) e **cliente**:
- **Provedor**: infraestrutura, hardware, rede, datacenter.
- **Cliente**: dados, acessos, aplicativos e configurações.

O nível de responsabilidade do cliente depende do modelo de serviço (IaaS, PaaS ou SaaS).

## Modelos de Nuvem
- **Nuvem Pública**  
  Recursos oferecidos por terceiros, acessíveis via internet.  
  **Uso**: startups, empresas que precisam de elasticidade rápida.

- **Nuvem Privada**  
  Infraestrutura dedicada exclusivamente para uma organização.  
  **Uso**: empresas com requisitos rígidos de segurança ou regulamentação.

- **Nuvem Híbrida**  
  Combinação de nuvem pública e privada.  
  **Uso**: organizações que precisam manter dados sensíveis em ambiente privado, mas querem escalabilidade da nuvem pública.

## Modelos de Serviço
- **IaaS (Infrastructure as a Service)**  
  Fornece infraestrutura de TI (servidores, redes, armazenamento) para o cliente configurar.  
  **Exemplo**: máquinas virtuais no Azure.  

- **PaaS (Platform as a Service)**  
  Oferece uma plataforma pronta para desenvolvimento e hospedagem de aplicações, sem necessidade de gerenciar a infraestrutura.  
  **Exemplo**: Azure App Service.  

- **SaaS (Software as a Service)**  
  Entrega o software pronto via internet, sem necessidade de instalação ou manutenção.  
  **Exemplo**: Microsoft 365.
  
## CapEx vs OpEx
- **CapEx (Capital Expenditure)**: gasto de capital em infraestrutura própria (servidores físicos, datacenter). Envolve investimento inicial alto.  
- **OpEx (Operational Expenditure)**: custo operacional, como pagamento de serviços de nuvem conforme uso. Reduz investimento inicial e facilita escalabilidade.

---

# Parte 2 - Máquinas Virtuais no Azure

Após a introdução aos conceitos de nuvem, aprofundei meus estudos na criação e configuração de **Máquinas Virtuais (VMs) no Azure**.  

## Etapas para Criar uma Máquina Virtual
1. **Acessar o Portal Azure**  
   Entrei no portal e utilizei o recurso de "Máquinas Virtuais".  

2. **Escolha da Imagem do Sistema Operacional**  
   No meu caso, utilizei **Windows** como sistema operacional, acessando depois via RDP (Remote Desktop).  
   Também estão disponíveis opções de Linux, como Ubuntu.  

3. **Configuração de Recursos**  
   - Região (datacenter onde a VM ficará hospedada).  
   - Tamanho da máquina (quantidade de CPU, memória e disco).  
   - Rede virtual e IP público.  

4. **Autenticação**  
   Configurei a forma de acesso via **usuário e senha**, pois estava utilizando Windows.  

5. **Revisão e Criação**  
   Após revisar todas as opções, a VM foi criada e ficou disponível em poucos minutos.  

## O que Aprendi na Prática
- Como **iniciar, parar e reiniciar** a VM pelo portal.  
- Conectar na VM via **RDP** (Windows).  
- A importância de configurar regras de **Firewall/NSG (Network Security Group)** para liberar portas específicas, como `3389` para RDP.  
- Diferença entre **armazenamento temporário** (volátil) e discos permanentes.  
- Como **redimensionar (scale-up)** a máquina caso precise de mais recursos.  

## Experiência Obtida
- Criar uma VM no Azure é simples, mas exige atenção ao custo, que é cobrado pelo tempo em que a máquina está ativa.  
- É essencial **parar ou desalocar** a VM quando não estiver em uso.  
- Ganhei experiência em configurar e acessar ambientes Windows diretamente pela nuvem.  

## Impacto das Escolhas em SLA
- O **SLA (Service Level Agreement)** define a disponibilidade garantida pelo Azure.  
- Uma **VM básica de instância única** tem SLA de **99,9%** quando utiliza **discos premium**.  
- Caso seja configurada em um **Conjunto de Disponibilidade** ou **Zonas de Disponibilidade**, a SLA pode chegar a **99,95% ou 99,99%**.  
- Isso significa que a escolha do tipo de máquina, região e redundância impacta diretamente na **confiabilidade e tempo de atividade** garantidos.
  
## Por que Utilizar Máquinas Virtuais no Azure
- **Flexibilidade**: é possível escolher diferentes sistemas operacionais, tamanhos de máquina e configurações.  
- **Escalabilidade**: aumenta ou reduz os recursos de acordo com a demanda.  
- **Disponibilidade Global**: escolha de diversas regiões e datacenters ao redor do mundo.  
- **Integração**: fácil conexão com outros serviços do Azure, como bancos de dados, redes virtuais e balanceadores de carga.  
- **Custo sob demanda**: pagamento pelo uso, sem necessidade de investir em hardware físico.  
- **Segurança e Confiabilidade**: suporte a criptografia, firewall, backups e SLAs garantidos pela Microsoft.  

## Conhecimentos Fundamentais
- O Azure fornece flexibilidade para escolher o tamanho da VM conforme a necessidade.  
- Segurança deve ser considerada desde o início, evitando abrir portas desnecessárias.  
- SLA depende das escolhas de configuração — desde uma VM simples até arquiteturas mais resilientes.   
