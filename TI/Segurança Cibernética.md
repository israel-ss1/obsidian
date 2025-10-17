#PF 

O que é Cyber Security? é a prática de proteção os ativos cibernéticos como: dados, redes, sistemas, equipamentos, dados, etc.

# Princípios

## Confidencialidade
Assegurar que apenas as pessoas autorizadas tenham acesso a informações restritas.
## Integridade
Assegurar a forma original da informação, através de cópias e rastreamento.

## Disponibilidade
Assegurar que sempre que se fizer necessário, as informações estejam disponíveis a pessoas autorizadas.

# Principais objetivos
- Roubo de informações: aquisição de informações.
- Ciberativismo: também conhecido com pichação, procurar manchar a imagem do alvo.
- Sequestro de informações: bloqueio de informações com pedido de resgate para desbloqueio.
- Negação de serviços: interromper o fornecimento de serviços com finalidade indiretas.
- Espionagem industrial: obtenção de informações sigilosas das empresas e governas para adquirir vantagem.
- Guerras modernas: vantagens políticas e militares em conflitos entre as nações.

# Atores
- Pessoas buscando recreação
- Hackers
- Maliciuos insiders
- Ativistas políticos
- Governos estrangeiros
- Terroristas

# Impactos
- Impactos técnicos
- Imagem / reputação
- Resultados financeiros
- Perda de parcerias
- Consequências jurídicas
- Multas e sanções regulatórias
- Perda de certificações e credenciamentos

![[Pasted image 20250602223529.png]]

# Malware

Programas desenvolvidos para se instalar em um sistema e executar serviços maliciosos de vários tipo. É um nome genérico e possui vários tipos de aplicabilidade e infecção. Pode ser conhecido por software malicioso, programa malicioso ou código malicioso. 
## Vírus

Programa malicioso que se propaga inserindo cópias de si mesmo se tornando parte de outros programas e arquivos. Precisa de um programa hospedeiro para funcionar. Possui partes para funcionar:
- Vetor (mecanismo) de infecção: meios pelos quais o vírus se propaga.
- Bomba lógica (mecanismo de ativação): evento ou condição que determina quando a carga útil é ativada (pode ser uma data ou dondição)
- Carga útil: o que o vírus faz causando dano.

Os principais meios de propagação são mídias removíveis, e-mails, páginas da web, downloads e transferência de arquivos.

### Tipos de vírus
- Boot: infectam os setores de inicialização de sistema ou de mídias (discos principalmente);
- Macro: infectam arquivos criados por programas de pacotes office que usam macros;
- Programas: infectam arquivos executáveis (.exe, .com, .bin, .dll, .sys, .pif);
- Script: produzidos em linguagens scripts, rotinas de automação e recebido ao acessar uma página na web ou por e-mail;
- Stealth: furtivo ou invisível. Utiliza técnicas para evitar detecção por softwares antivírus;
- Polimórficos: mutantes, mudam a assinatura ou o código base para não ser pego pelo antivírus. É baseado em criptografias para mudança dos códigos e precisa de heurística para ser detectado;
- Metamórficos: reescreve e converte seu próprio código, mudando seu comportamento para evitar a detecção por heurística. É uma variação dos vírus polimórficos.
## Worms

Também conhecido por verme. Se propaga na rede fazendo cópias de seu código em todos os pontos. Diferente dos vírus, não precisa de hospedeiro e não faz parte de outros programas. Aproveita as vulnerabilidade da rede para de propagar automaticamente, ou pela execução direta do arquivo. O principal problema é o consumo de recursos de rede

Processo de propagação:
- Identificação dos computadores alvo;
- Envio de cópias;
- Ativação das cópias;
- Reinício do processo.

## Trojan - Cavalos de Tróia

Também conhecido com trojan-horse. Mesma ideia da história do cavalo de troia, recebe um phishing para liberar as portas de comunicação para invasão dos cyber criminosos. Existem alguns tipos:
- Trojan Downloader: instala outros códigos maliciosos obtidos de sites na internet;
- Trojan Dropper: instala outros códigos maliciosos embutidos no próprio trojan;
- Trojan Backdoor: abre portas da máquina;
- Trojan DoS: torna serviços inacessíveis;
- Trojan Destrutivo: destrói mídias e periféricos;
- Trojan Clicker: utiliza a rede para gerar cliques em sites de monetização;
- Trojan Proxy: faz a máquina um servidor proxy para redirecionar tráfegos;
- Trojan Spy: utilizado para monitoramento da máquina e do usuário;
- Trojan Banker(Bancos): específico para coletar dados bancários.
## Spyware

Programa espião para monitorar as atividades do sistema enviando as informações para um terceiro. Pode ser utilizado de forma legítima se não for utilizado de forma ilegal, podendo inclusive ter apoio jurídico para investigação das forças de segurança.
- Keylogger: captura as teclas digitadas pelo usuário. Esse é o motivo de algumas instituições utilizarem teclados virtuais;
- Screenlogger: armazena a posição do mouse e a tela no momento do clique. Este é o motivo para ter botões digitais com mais de um dígito na mesma tecla;

## Ransomware

Programa que torna inacessível os dados de um equipamento utilizando criptografia. O propósito é cobrar resgate dos dados. O resgate geralmente é feito através de bitcoins. Não se propaga sozinho. O CESP considerar cifrar com o mesmo significado de criptografar.
- Ransonware Crypto;
- Ransomware Locker que bloqueia o acesso.
## Backdoor

É a criação de portas vulneráveis no sistema que aguardam o invasor retornar no sistema.

## Bot

Vem do acrônimo de Robot ou Robô. O Bot permite que o invasor controle remotamente o computador. A máquina infectada é chamada de zumbi. A propagação do bot pode ser automática explorando vulnerabilidades da rede, formando uma botnet. Essas botnet são utilizadas posteriormente para ataques DDoS.
## Rootkit

Conjunto de programas que permite a invasão e a manutenção do invasor na rede sem ser percebido. São programas do tipo root, su ou admin. Os sistemas tem dificuldades de detecção por causa desse perfil root.

## Adware - Advertising Ware

Malware que monitora as atividades do usuário a fim de exibir propagandas direciondas de acordo com o perfil de consumo do usuário.

## Fileless

Um malware sem arquivo. O código fica em memória e se utiliza de programas de sistema como o Powershell ou o WMI para executar ações maliciosas. Essa técnica é conhecida como LOTL ou Living Off The Land. Por estar em memória ele tem uma persistência limitada.


# Principais tipos de ciberataques

## Cross-site Scripting (XSS)
Tenta inserir scripts maliciosos em websites. O scripts vão em elementos dos próprios sites que não validam os dados de entrada.

## BotNet
Vários computadores que são infectados por malware formando uma rede para ataques em massa. Um dos malware mais comum é o Mirai. Este malware pega dispositivos que utilizam processadores ARC (IoT). 

## Zero Day Exploits

Ataque feito à uma vulnerabilidade que é explorado antes que o fornecedor disponibilize uma correção. São feitos através de Exploits. Estes são scripts, programas ou softwares que exploram possibilidades de vulnerabilidade através de comportamento acidental ou imprevisto. O Ataque permanece funcionando até a correção pelo fabricante.
## DoS e DDoS - negação de serviço distribuído

- Denial of Service = DoS
- Distribuited Denial of Service = DDoS

Tenta gerar instabilidade ou derrubar um serviço.
Geralmente acontece gerando milhares de requisições simultâneas, feitas através de máquinas sequestradas. Isso colapsa o serviços que fica indisponível ou lento. Pode ser usado como distração para outros tipos de ataque, para corromper a imagem de uma instituição. Refere-se ao ataque como inundação do alvo.

### Ping da morte
Explora vulnerabilidade de SOs antigos. Envia protocolos ICMP (Internet Control Message Protocol) excedendo o tamanho máximo permitido de bytes. É o sistema de mensageria para relatar erros dos sistemas. O tamanho máximo permitido é 65.535. É um ataque Dos. Atualmente não funciona mais. Ping utiliza o protocolo ICMP

### Ping Flood ou ICMP Flood
A mesma ideia do ping da morte, mas dessa vez, envia-se milhares de pacotes pequenos. Precisa ter vantagens de banda larga em relação ao alvo. A ideia é inundar o canal de comunicação. Geralmente o a ataque usa uma botnet para conseguir a vantagem.

### UDP Flood - User Datagram Protocol
Protocolo usado para transmissão de vídeo ou busca de DNS. Ele acelera a comunicação para gerar buffer, enviando mesmo sem estabelecer o enlace. 

### MAC Flooding

Inundação de endereços MAC acontece em redes feitas com switch e rede ethernet. Quando um switch recebe um quadro (frame) e não sabe para qual porta ele deve encaminhá-lo, o switch toma uma medida chamada de "flooding", onde ele retransmite o quadro recebido para todas as portas, exceto a porta pela qual o quadro foi recebido. Isso é feito na expectativa de que o dispositivo de destino esteja em uma das outras portas do switch. Se o dispositivo de destino responder, o switch aprenderá o endereço MAC dele e, em futuras comunicações, poderá encaminhar os quadros diretamente para essa porta. Isso pode ser usado para ataques DoS, indisponibilizando a rede.
### Smurf
Ataque usando o protocolo IP e ICMP onde, utilizando um IP falso, o malware manda uma requisição com um IP. O retorno do do ICMP é para um IP do próprio servidor, fazendo o  servidor entrar em loop.

## Phishing
Ataque efetuado por e-mail falso utilizando engenharia social. O objetivo é que se clique em algum link que baixa conteúdo maliciosos. Estes scripts poderão rodar processos em background sem permissão, sequestro de máquinas e roubo de informação.

## Ransoware
Ataque que criptografa os dados da vítima pedindo resgate para decriptogafar. Geralmente o computador é infectado por um malware e o pagamento é feito por criptomoedas.

## Main in the Middle
Atacante se insere em uma comunicação, se passando por uma das partes. Atualmente muito comum em golpes de whatsapp. Pode ser clonando aplicativos móveis, endereço IP ou MAC.

## Engenharia Social
Ataque que manipula uma vítima para obter informações preciosas. O ataque geralmente usa informações privadas para constranger funcionários a executar tarefas e quebrar protocolos. Pode ser também para adquirir acessos.

## Brute Force
Tenta descobrir login e senha do usuário através de combinação e processamento em massa.

## APT - Advanced Persistent Thread
O sistema é infectado por e segue infectando outros nós da rede, se tornando persist

## SQL Injection
Tentativa de injetar um comando de SQL para quebrar o aplicativo ou site através do banco de dados. Semelhante ao Cross-site Scripting.

## Drive-by download
Contaminação não intencional por download de código malicioso. Acontece com a simples visita ao site. Navegadores atuais previnem esse tipo de ação.

## Cryptojacking
Sequestro de processamento de computados para mineração de criptomoedas.

## Spoofing

Significa mascaramento. Pode estar associado a e-mai, IP ou ARP (Adress Resolution Protocol). É utilizado para não deixar rastros. 

## DNS Poisoning

Envenenamento por DNS ocorre quando informações falsas são inseridas no [cache de um servidor de nomes de domínio](https://www.fortinet.com/br/resources/cyberglossary/what-is-caching), resultando em consultas DNS produzindo uma resposta incorreta, enviando usuários para o site errado. O propósito é direcionar o atacado para um site malicioso. O Envenenamento pode acontecer através de e-mail, MITM (Main-In-The_Middle) ou em um sequestro de servidor DNS.
Uma infectado, o atacante pode roubar dados, sequestrar máquinas ou indisponibilizar serviços.

## APT - Advanced Persistent Threat

Ataques com períodos prolongados, disseminados por vários códigos que são difíceis de serem extirpados. Geralmente em grandes organizações de dados. Normalmente parece um tráfego de rede legítimo. Utiliza diversos protocolos de rede para transmitir ou receber informações do ponto de comando e controle do malware.

# Framework MITRE

## MITRE Attack

## MITRE Defense

## CIS Controls

## NIST Cybersecurity Framework


# Sinais de ciberataques

- Aumento considerável de banda reutilização de links de internet
- Redes lentas
- Antivírus desabilitado
- Falhas em logs de autenticação
- Programas de fontes desconhecidas

# Proteções de camada de perímetro

Esta é a camada com conexão direta a internet. Aqui é feita as primeiras demandas de defesa. Tem como boas práticas as DMZs e as Honeypot.
- DMZ: Zona desmilitarizada. Separa os servidores da extranet da intranet. Geralmente fica entre firewalls.
- Honeypot: solução para entender as táticas e técnicas utilizadas por um atacante para análise futura. 

## Firewall

Primeira camada. Monitora o tráfego de entrada e saída de rede, permitindo ou bloqueando através de políticas de segurança. Analisa o cabeçalho do pacote, inspecionando a origem e o destino, portas e protocolos.

Pode ser encontrado em várias camadas, como a de perímetro, rede, 

 Geralmente se bloqueia tudo para depois ir liberando o tráfego conhecido. Pode ser software, físico, appliance virtual ou solução em nuvem. Pode agregar outras funções como inspeções de SSL, criptografia ou VPN.

Firewall leste-oeste é um firewall embarcado usado entre data centers.

## IDS/IPS

Pode ser encontrada na perímetro e mais comum na camada de rede. Detecta e bloqueia intrusos. Trabalha inspecionando a assinatura dos pacotes, comparando com uma base do fabricante da solução. Geralmente é instalado junto com o firewall

## Analise avançada de malware - sanbox

Analisa arquivos e programas hostís ou suspeitos observando o comportamento do usuário. É usado em SaaS ou On Premisse. Protege situações como zero-day que é a primeira atuação do malware não conhecido.

## Antiphishing e Antispam

Soluções de mensageria e e-mail. Pode ser aprovisionado em PaaS, software, appliance virtual ou físico. Fazem varredura em todo o e-mail, usando estatística, heurística ou predição. 

## DLP
Data Link Prevention
Prevenção de vazamentos de informações, movimentações de dados através de monitoramento. Pode estar presente em todas as camadas. Pode ser usado em todos os tipos de mídias, serviços e protocolos; até mesmo clipboard (área de transferência)  e impressoras.

## Segurança física

Proteção física dos locais críticos aos equipamentos. Controles de acesso, câmeras de segurança, extintores, alarmes ...

# Proteções de camada de rede

## SBC - Session Border Controller 

Trata-se de controle de tráfego de voz. Protege o protocolo SIP, utilizado em plataformas VOIP (Voz sobre IP). Uma espécie de firewall, protege ligações com dados sensíveis como números de cartão de crédito.

Soluções
- ACL - Regras de tráfegos;
- Ataques DDOS;
- Gerenciamento de sessões SIP;
- Criptografia de sinalizações.

## MDM - Mobile Security

Certifica se os dispositivos seguem as politicas de segurança. 
- Aplicativos permitidos
- Versão do SO
- Path de segurança
- Wipe de dispositivos
- Tunelamento
- Monitoramento e rastreamento

## Proxy - Content Filtering

Solução de segurança que monitora a navegação e o acesso a web bloqueando conteúdos maliciosos ou impróprios. Pode ser vitual appliance (comum) ou agregado a um firewall UTM. Utiliza uma base de dados do fabricante que classifica os websites. Faz varreduras de malwares.

## NAC

Verifica a conformidade do endpoint (qualquer dispositivo) verificando as soluções de segurança. Verifica se os dispositivos estão saudáveis. Faz logs de conexões do usuário. O mais comum é a verificação se o dispositivo está autorizado a acessar o dispositivo, senão ele desabilita a porta. 
Vem sendo agregado a outras soluções como NDN.
- Antivírus;
- IPS;
- Autenticação;
- Políticas de segurança.

## Wireless Security

Protegido por soluções de WIPS (Wireless Intrusion). Oculta o SSID, filtra os MACs autorizados, certificados de segurança e criptografias. Protege contra:
- Rogue access points;
- Access Point mal configurado;
- MAC spoofing
- Man in the middle
- Ataques DDoS

## Remote Access Security

VPN client - Dois sites estabelecem um canal exclusivo com firewall nos dois pontos.
SSO Single Sign-on
PAM Privileged access management - protege e monitora e log e vídeo as contas privilegiadas
VDI ou DaaS (Desktop as a Service)
Zero Trust - Tudo que vem da internet tem zero de confiança.


# Proteções de camada de endpoint

Endpoint é tudo que participa da rede e comunicação.

## EPP EndPoint Protection

Um avanço dos antivirus. Pode ser convencional que é o PREVENT, destinado a prevenção e tem o DETECT + RESPONSE  que age em caso de ataques.

![[Pasted image 20250617203912.png]]
## Security Enforcement

Gerencia, monitora e mantem as políticas de segurança aplicadas. 
- Ansible (free);
- GPO - políticas nativas Microsoft.

## Path Management

Distribuição e aplicação de atualizações de versões de sistema., corrigindo vulnerabilidades e gerenciando proteções.


# Proteções da camada de aplicação

Proteção para aplicações e sistemas operacionais
## Code Review

Revisão de código é o processo que garante que uma aplicação foi desenvolvidos sem bugs ou vulnerabilidades de segurança. As principais chacagens são:
- Detecção de erros;
- Detecção de vulnerabilidades;
- Detecção de libs deprecated;
- Melhores práticas de desenvolvimento.

Solução mais popular é o Sonarqube

## Web Application Firewall (WAF)

Firewall específico para aplicação que filtra e monitora tráfegos de camada 7 como por exemplo HTTP, HTTPs e FTP. Este firewall não monitora somente os cabeçalhos, mas também o conteúdo dos pacotes. 
Protege principalmente ataques tipo XSS (Cross Site Scripting) e SQL Injection. Muito comum em modelos SaaS
Serve como proxy reverso pois cria uma camada de apresentação que fica antes do código.

## MFA - Multiplo Fator de Autenticação

Mecanismo que exige duas ou mais evidências para permitir o acesso a um sistema. Geralmente atua junto com e-mail, mensagens de texto, tokens físicos e apps de celulares.


## Boas práticas da camada de aplicação

### Desenvolvimento de aplicações em camadas.

Propõe segmentar o sistema em 3 em mais camadas, geralmente front-end, back-end e dados. Essas camadas também podem ser abstraídas como camada de apresentação (front-end), negócio (back-end) e camada de dados.
### DevSecOps

Cultura de engenharia de software que integra a equipe de desenvolvimento com as equipes de segurança da informação e de operação do sistema. Esse modelo iniciou com DevOps e posteriormente se estendeu para DevSecOps, agregando a segurança no meio, sempre conduzindo a segurança entre os fluxos.

A ideia é automatizar os processos de  inspeção de segurança e mitigar as vulnerabilidades rapidamente. Esse monitoramento permite correções constantes e imediatos em vulnerabilidades imediatas e também monitoramento do que está sendo desenvolvido.


# Proteções de camada de dados

## PKI - Public Key Infrastructure

Infraestrutura de chaves públicas. É um mecanismo de segurança utilizado para gerenciar chaves de criptografia de dados e garantir a autenticidade das entidade participantes em uma comunicação digital.

Permite criptografar uma comunicação, garantindo a autenticidade das entidades participantes. A autoridade que gerencia e emite as chaves podem ser interna ou externa. Uma mas entidades mais conhecidas é a CertSign. Protege principalmente ataques de Man-In_The-Middle.

SSLabs.com - Site para verificação dos certificados de segurança de um site.

## Data Wiping

Processo lógico utilizado para tornar o dado permanentemente ilegível por um processo que sobrescreve o dado. É utilizado quando o equipamento é roubado ou descartado para que não seja possível recuperar os dados por outros meios de análise de disco. 
O datawiping pode ser feito remotamente em caso de roubo.
- Single pass overwrite
- Three pass overwrite
- Seven pass overwrite
- Secure erase

## Classificação de dados

Organiza os dados atribuindo categorias, apoiando as políticas de segurança dos dados. Geralmente as classificações são em relação a confidencialidade como público, interno e privado. Poderia ser também com critério de urgência ou criticidade.


# Proteções de camadas de nuvem

## Zero Trust (ZTN ou ZTNA)

É um conceito que significa zero confiança. A ideia é que nenhum acesso é confiável e necessita de constante inspeção e monitoramento. É uma proposição de arquitetura de rede. Utiliza passos para a implementação dos acessos:
- Identifica a superfície de acessos;
- Faz o mapeamento dos acessos;
- Constrói a arquitetura Zero Trust;
- Monitora e mantem a política determinada pela arquitetura Zero Trust.

## CASB - Cloud Access Security Brocker

É uma espécie de gateway de segurança para acesso a serviços em nuvem que fica entre o usuário ou sistema que acessa o workload na nuvem. Está baseada em 4 pilares:
- Visibilidade;
- Conformidade;
- Segurança;
- Proteção.

Usa alguns critérios
- Geolocalização da tentativa de acesso;
- Tipo de dispositivo que está tentando acessar;
- Versão do Sistema Operacional que está tentando acessar;
- Nível de patch de segurança do dispositivo que está tentando acessar;
- Quais sistemas e aplicativos estão tentando acessar a nuvem;
- Pode verificar se o dispositivo está de acordo com a PSI da empresa;
- Pode usar ranqueamento de risco da tentativa de acesso.

CASB é importante principalmente quando você sabe que sua rede deverá ser acessada por dispositivos pessoais (BYOD - Bring Your Own Device) onde você não tem controle e visibilidade do mesmo.

BYOD, sigla para "Bring Your Own Device", ==é uma política corporativa que permite aos funcionários utilizarem seus próprios dispositivos (como laptops, smartphones, tablets) para acessar recursos e dados da empresa==.


# Prevenção e gerenciamento de políticas

