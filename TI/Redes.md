#PF 


## Modelo OSI

![[Pasted image 20250702201141.png]]

### 7 - Aplicação

Camada de negócio. Onde estão os programas, bancos de dados e SO. É livre e independente do modelo.

1. DNS - Tradução de url para IP
2. DHCP - Resolução dinâmica de IPs
3. SMTP - protocolo de comunicação transferência de e-mail entre servidores e de envio de e-mail do cliente para o servidor.
4. POP e IMAP - protocolo de recebimento de e-mails do servidor para o cliente.
5. FTP - protocolo de transferência de arquivos. TFTP é o mesmo protocolo porém é mais rápido porque não verifica conexões e nem as entregas, não sendo confiável. SFTP é o mesmo protocolo com criptografia segura.
6. HTTP e HTTPS - protocolo de comunicação de sites.
7. SNMP - protocolo para mensageria entre dispositivos de rede.
### 6 - Apresentação

Fornece serviços para a camada 7. Onde estão os formatos de dados, criptografia e compactação.

1. MPEG - compressão e transmissão de áudio e vídeo.
2. JPEG - compressão e transmissão de dados, geralmente imagens fotográficas.
3. GIF - compressão e transmissão de imagens de baixa resolução e ícones.
4. ASCII
5. EBCDIC
### 5 - Sessão

Provê serviços para a camada de apresentação. Início e fim de conexão entre os dispositivos. Sincronia, pausa e reinício entre hosts.
### 4 - Transporte

Conexão fim a fim. Onde ficam os firewall. Segmenta e reconstrói os dados, controlando o fluxo e a perda de dados (retransmissão). 
#### Handshake triple

Handshake triplo consiste em uma sincronização iniciada pelo cliente ao servidor. O dispositivo que está iniciando a comunicação envia um segmento contendoum número de sequência inicial indicando um início de omunicação. Este é o SYN inicial. O dispositivo receptor responde com um SYN/ACK confirmando a comunicação. O dispositivo que iniciou a comunicação responde a confirmação, completando o estabelecimento e sincronização da comunicação. Após os dados serem transmitidos, a sessão precisa ser encerrada, conforme demonstra a figura a seguir.

#### Port ou porta

Número que identifica a aplicação que irá receber a informação. Existem três faixas de números de portas. A primeira vai até 1024 (2 elevado a 10). As principais aplicações estabelecidas são:
- FTP - 20, 21 - transferência de arquivos
- SSH - 22 - acesso remoto
- Telnet - 23 - acesso remoto
- SMTP - 25 - tráfego de e-mails entre servidores
- DNS - 53 - resolução de ip/url
- TFTP - 69 - transferência de arquivos não segura
- HTTP - 80 - páginas web
- POP - 110 - recebimento de e-mails cliente/servidor
- IMAP - 143 - recebimento de e-mails cliente/servidor
- HTTPS - 443 - páginas web criptografadas.

A segunda faixa são as portas registradas. Estas identificam aplicações e processos do usuário. Vão de 1024 até 49151. 
A terceira faixa são portas privadas ou dinâmicas, usadas pelos dispositivos para transmissão. Vão de 49152 até 65535 (2 elevado a 15)

#### BGP, ou Border Gateway Protocol

==É  um protocolo de roteamento usado na internet para trocar informações sobre a acessibilidade das redes e determinar a melhor rota para o tráfego de dados entre diferentes sistemas autônomos (ASs)==. Em termos simples, o BGP é o protocolo que permite que a internet funcione, garantindo que os dados cheguem ao destino correto. 

O que o BGP faz?

- **Roteamento dinâmico:**
    
    O BGP é um protocolo de roteamento dinâmico, o que significa que ele aprende automaticamente as rotas entre diferentes redes e sites, reduzindo a necessidade de configuração manual de rotas em roteadores. 
    

- **Troca de informações:**
    
    O BGP permite que os roteadores compartilhem informações sobre as redes disponíveis e os melhores caminhos para alcançar esses destinos, utilizando sessões de "peering" com outros roteadores. 
    

- **Seleção da melhor rota:**
    
    O BGP analisa todos os caminhos disponíveis e escolhe a rota mais eficiente para o tráfego, considerando fatores como distância, políticas de rede e custos. 
    

- **Funcionamento como "correio":**
    
    Imagine o BGP como o serviço de correio da internet. Quando você envia uma mensagem, o BGP seleciona a rota mais rápida e eficiente para entregá-la ao destinatário, assim como os serviços de correio selecionam a rota mais adequada para entregar uma carta. 
    

Sistemas Autônomos (ASs):

- Os ASs são redes independentes, como provedores de serviços de internet (ISPs) ou grandes redes corporativas, que são responsáveis pelo roteamento de tráfego em suas próprias áreas. 

- O BGP é usado para o roteamento entre diferentes ASs, permitindo que a internet funcione como uma rede global interconectada. 

BGP interno (iBGP) e BGP externo (eBGP):

- **BGP interno (iBGP):** Usado para roteamento dentro do mesmo sistema autônomo. 

- **BGP externo (eBGP):** Usado para roteamento entre sistemas autônomos diferentes.
#### OSPF (Open Shortest Path First) 

==É um protocolo de roteamento de estado de enlace usado em redes IP para determinar a melhor rota para o tráfego de dados==. Ele calcula as rotas usando o algoritmo SPF (Shortest Path First), também conhecido como algoritmo Dijkstra, com base em informações de estado do enlace. O OSPF é um protocolo IGP (Interior Gateway Protocol) usado dentro de um sistema autônomo (AS). 

Características principais do OSPF:

- **Roteamento de estado de enlace:**
    
    O OSPF, ao contrário do RIP (Routing Information Protocol) que usa contagem de saltos, utiliza informações de estado do enlace para determinar as rotas. Isso significa que cada roteador OSPF mantém um banco de dados com a topologia completa da rede e calcula o caminho mais curto para cada destino localmente. 
    

- **Algoritmo SPF (Dijkstra):**
    
    O algoritmo SPF (Shortest Path First), também conhecido como algoritmo de Dijkstra, é usado para calcular o caminho mais curto para cada destino. Ele considera o custo associado a cada enlace e constrói uma árvore SPF com a rota mais eficiente. 
    

- **Áreas:**
    
    O OSPF permite a divisão de redes em áreas para melhorar a escalabilidade e reduzir o tamanho das tabelas de roteamento. A área de backbone (área 0) é a área central da rede e todas as outras áreas precisam se conectar a ela. 
    

- **Custo:**
    
    O custo em OSPF é baseado na largura de banda do enlace. O valor padrão é 100 Mbps para cálculo do custo, e a fórmula é 100 Mbps / largura de banda do enlace. 
    

- **Roteador Designado (DR):**
    
    Em redes multiacesso, o OSPF escolhe um roteador designado (DR) para coordenar a troca de informações de estado de enlace. Isso ajuda a reduzir o número de atualizações de roteamento e melhora a eficiência da rede.
#### TLS (Transport Layer Security)

== É um protocolo de segurança que criptografa a comunicação entre aplicações e servidores, garantindo a privacidade e integridade dos dados transmitidos==. Ele funciona como uma camada de segurança sobre protocolos de rede como TCP/IP, protegendo dados em trânsito. 

Em detalhes:

- **Criptografia:**
    
    O TLS usa algoritmos de criptografia para proteger os dados, tornando-os ilegíveis para terceiros não autorizados. 
    
- **Autenticação:**
    
    O TLS verifica a identidade do servidor e, opcionalmente, do cliente, garantindo que as partes envolvidas na comunicação são quem dizem ser. 
    

- **Integridade:**
    
    O TLS garante que os dados não foram alterados durante a transmissão, verificando se houve alguma modificação. 
    

- **Camadas:**
    
    O TLS opera entre a camada de aplicação (como HTTP) e a camada de transporte (TCP/IP), protegendo a comunicação entre elas. 
    

- **HTTPS:**
    
    O TLS é usado para implementar o HTTPS, a versão segura do protocolo HTTP, permitindo que sites e serviços web usem criptografia. 
    

- **Histórico:**
    
    O TLS evoluiu do protocolo SSL (Secure Sockets Layer), sendo desenvolvido inicialmente pela Netscape e posteriormente padronizado pela IETF. 
    

- **Atualizações:**
    
    O TLS possui diferentes versões (1.0, 1.1, 1.2, 1.3), com versões mais recentes oferecendo melhor segurança e desempenho. 
    

- **Certificados:**
    
    Para usar o TLS, um site ou aplicação precisa ter um certificado TLS (ou SSL) instalado, emitido por uma autoridade de certificação.
#### SSL (Secure Sockets Layer) 

==É um protocolo de segurança que estabelece uma conexão criptografada entre um servidor e um cliente, como um navegador web, para garantir a privacidade e a integridade dos dados transmitidos==. Ele impede que terceiros interceptem e leiam informações confidenciais, como senhas, dados de cartão de crédito e outras informações pessoais. O SSL é amplamente utilizado para proteger sites através do protocolo HTTPS e é um componente essencial para a segurança online. 

O que é o SSL?

- **Conexão segura:**
    
    O SSL cria uma conexão criptografada entre o cliente e o servidor, garantindo que os dados transmitidos sejam protegidos contra acesso não autorizado. 
    

- **Autenticação:**
    
    Além da criptografia, o SSL também autentica o servidor, verificando sua identidade e garantindo que o usuário está se comunicando com o site correto. 
    

- **Integridade dos dados:**
    
    O SSL protege a integridade dos dados, garantindo que eles não sejam alterados durante a transmissão. 
    

Como funciona o SSL?

- **1.** **Handshake SSL:**
    
    Ocorre uma troca inicial de mensagens entre o cliente e o servidor para estabelecer a conexão segura. Isso inclui a seleção de um algoritmo de criptografia e a troca de chaves de segurança. 
    

- **2.** **Criptografia:**
    
    Uma vez estabelecida a conexão segura, todos os dados transmitidos são criptografados utilizando a chave de sessão criada durante o handshake. 
    

- **3.** **Descriptografia:**
    
    O servidor recebe os dados criptografados e os descriptografa utilizando a chave de sessão para processá-los. 
    

Onde o SSL é utilizado?

- **HTTPS:**
    
    O SSL é a base do protocolo HTTPS, que é a versão segura do protocolo HTTP. O HTTPS é usado para proteger a comunicação entre navegadores e servidores web. 
    

- **E-mail:**
    
    O SSL também pode ser usado para proteger a comunicação entre servidores de e-mail e clientes de e-mail, como o Outlook. 
    

- **Outras aplicações:**
    
    O SSL pode ser utilizado em diversas outras aplicações que exigem comunicação segura, como redes privadas virtuais (VPNs). 
    

SSL vs. TLS:

- **Evolução:**
    
    O SSL é o antecessor do protocolo TLS (Transport Layer Security), que é a versão mais recente e segura do protocolo.
    

- **Uso comum:**
    
    Embora o TLS seja a versão mais atual, muitos ainda se referem ao protocolo de segurança como SSL, mesmo que estejam utilizando o TLS.
    

- **Atualização:**
    
    É importante manter os sistemas atualizados com a versão mais recente do TLS para garantir a segurança da comunicação
#### TCP - Transmission Control Protocol

Administra os recursos de entrega ordenada, confiável e com controle de
fluxo. 

Confira, a seguir, uma análise dos principais campos do segmento TCP.
**a) Porta de origem**: campo de 16 bits que contém o número da porta origem.
**b) Porta de destino:** campo de 16 bits que contém o número da porta de
destino.
**c) Número de Sequência**: campo de 32 bits utilizado para ordenar os segmentos.
**d) Número de reconhecimento**: campo de 32 bits com o número de confirmação que indica o próximo segmento TCP esperado.
**e) Comprimento do cabeçalho:** campo de 4 bits que indica o tamanho do
cabeçalho do segmento.
**f) Janela:** campo de 16 bits com o número de segmentos que poderão ser
transmitidos antes de aguardar uma confirmação.
**g) Checksum1**: campo de 16 bits para o cálculo de verificação de erros.
**h) Dados**: campo com os dados das camadas superiores.

#### UDP - User Datagram Protocol

**a) Porta de origem**: campo de 16 bits que contém o número da porta origem.
**b) Porta de destino:** Campo de 16 bits que contém o número da porta de
destino.
**c) Comprimento:** Campo de 16 bits que indica o tamanho do datagrama, incluindo os dados.
**d) Checksum:** Campo de 16 bits para o cálculo de verificação de erros.
**e) Dados:** Campo com os dados das camadas superiores.

#### SCTP (Stream Control Transmission Protocol) 

É é um protocolo de transporte que oferece uma comunicação confiável e orientada a mensagens, combinando características do TCP e do UDP==. Ele foi projetado para aplicações que precisam de transferência de dados com alta confiabilidade, mas que também podem se beneficiar da transferência orientada a mensagens, como é o caso do UDP. O SCTP se destaca por sua capacidade de multihoming, permitindo que uma conexão use múltiplos endereços IP para aumentar a resiliência e tolerância a falhas, e por suportar múltiplas streams dentro de uma única associação. 

Principais características do SCTP:

- **Confiabilidade e Orientação a Mensagens:**
    
    O SCTP garante a entrega de dados sem erros, em ordem e sem duplicações, semelhante ao TCP, mas também suporta a transferência de dados em formato de mensagens, como o UDP. 
    
- **Multihoming:**
    
    Permite que um endpoint tenha múltiplos endereços IP, o que aumenta a redundância e a tolerância a falhas, pois a comunicação pode ser transferida para um endereço alternativo em caso de falha. 
    

- **Multistreaming:**
    
    Possibilita que vários fluxos de dados independentes sejam transferidos através de uma única associação SCTP. 
    

- **Detecção de Falhas:**
    
    Inclui mecanismos como heartbeat para monitorar a conectividade da sessão e detectar falhas. 
    

- **Segurança:**
    
    Oferece mecanismos de segurança, como a troca de cookies durante a configuração da associação, para proteger contra ataques de negação de serviço. 
    

- **Fragmentação:**
    
    O SCTP pode fragmentar dados em pacotes menores para otimizar a transmissão e lidar com diferentes tamanhos de Unidade Máxima de Transmissão (MTU) em diferentes caminhos. 
    

Aplicações do SCTP:

O SCTP é frequentemente utilizado em aplicações de telecomunicações, como a comunicação entre redes SS7 e redes IP, onde a confiabilidade e a tolerância a falhas são cruciais. Também é uma opção para aplicações que demandam transferência de dados orientada a mensagens com alta confiabilidade, como aplicações de sinalização em redes móveis.
### 3 - Rede

Roteamento entre redes diferentes. Para onde estão os roteadores. 
Essa camada possui quatro processos básicos bem definidos:
**a) endereçamento** – é o processo de definir endereços para os dispositivos existentes em uma rede que permite a comunicação de dados. Existem padrões de endereçamento de acordo com o protocolo de camada de rede
utilizado pelo dispositivo.

**b) encapsulamento** – é o processo de empacotar, moldar, segmentar o fluxo
de dados a ser transmitido pela rede dentro da PDU do protocolo da camada de rede utilizado. Neste processo, são criados os pacotes com as informações
a serem entregues ao destino da comunicação.

**c) roteamento** – é o processo que consiste na tarefa de direcionar estes pacotes montados no processo de encapsulamento, por meio da rede de dados. O roteamento é tradicionalmente realizado por dispositivos que trabalham na camada 3 com o intuito de escolher o melhor caminho para a entrega eficiente de cada pacote ao seu destino. Normalmente, esta função é realizada por equipamentos chamados de roteadores.

**e) desencapsulamento** – é o processo de desempacotar, retirar o conteúdo de
dados constante no pacote recebido e entregar para a camada superior do
modelo de referência OSI, no caso, a camada de transporte.

#### IPv4

Cada pacote criado pelo IPv4 em uma comunicação, é tratado isoladamente
durante toda a sua vida durante o tráfego na rede. Por este motivo, é dito que o IPv4 é um protocolo sem conexão, no qual seus pacotes são tratados e avaliados em cada equipamento por onde os mesmos trafegam

##### Pacote IP
O pacote IP, também chamado de datagrama, é a unidade básica de transferência da camada de rede. É ele que define o layout dos pacotes a serem transferidos. É dividido em cabeçalho e dados.

![[Pasted image 20250702210719.png]]
Veja uma análise dos principais campos do pacote IP.
a) **Versão**: versão do protocolo, no caso 4.
b) **Tamheader**: corresponde ao tamanho do cabeçalho contado em números de palavras de 32 bits (4 bytes).
c)**Tipo serviço**: é o campo que contém a indicação de qualidade do serviço
desejado para o encaminhamento do pacote. Esse campo possui 8 bits.
d) **Tampacote**: campo que contém o tamanho do pacote em quantidade de
octetos (bytes). O valor máximo é 65.535 bits.
e) **Identificação**: é o campo preenchido pela origem do pacote que o identifica. É utilizado na montagem da sequência dos pacotes no destino. Um
pacote que precisa ser fragmentado por outro equipamento no caminho até
o seu destino, utiliza, neste campo, o mesmo valor para todos os fragmentos
resultantes.
f) **Flags**: campo de 3 bits que identifica se o pacote pode ser fragmentado no
caminho até o destino e também se já ocorreu fragmentação. O primeiro bit
é sempre 0, o segundo bit indica se pode ou não fragmentar (0 = pode fragmentar, 1 = não pode fragmentar), e o terceiro bit indica se este pacote é (1) ou não é (0) o último fragmento.
g) **Deslocamento**: caso tenha ocorrido fragmentação, este campo indica o
deslocamento dos dados do pacote em relação ao campo de dados do pacote
original (antes da fragmentação). Este campo é primordial para a remontagem
do pacote e considera como unidade um octeto (1byte).
h) **TTL** (Time to live): representa a quantidade de saltos por onde um pacote
pode trafegar. Cada ativo de rede que roteia este pacote diminui o TTL de 1,
sendo descartado quando este valor chega a zero.
i) **Protocolo**: campo preenchido com um valor numérico que identifica para
qual protocolo da camada superior a camada de rede deve entregar o conteúdo deste pacote, no momento em que o mesmo chegar ao destino. Exemplo: 6 – TCP, 17 – UDP, 1 – ICMP, 89 – OSPF, etc.
j) **CheckSum** do cabeçalho: é o campo calculado e checado para cada salto
que o pacote passa na rede, a fim de verificar a integridade do cabeçalho.
k) **Endereço de origem**: é o endereço de origem do pacote, composto por 32
bits. banco (DE AVA - Gerenciamento)
l) **Endereço de destino**: é o endereço de destino do pacote, composto por 32
bits.
m) **Opções do pacote IP**: este campo é opcional, mas requerido para algumas
implementações. A origem do pacote colocará nesse campo as opções selecionadas. Esse campo é variável em seu tamanho e vai depender das opções definidas pela origem.
n)**Preenchimento**: é o campo para preencher o cabeçalho mantendo sempre o alinhamento do mesmo em 32 bits.

##### NAT 
O protocolo NAT (Network Address Translation) ==é usado para traduzir endereços IP privados de uma rede interna para endereços IP públicos==, permitindo que dispositivos com endereços privados se comuniquem com a internet. Ele atua como um tradutor entre a rede local e a internet, possibilitando o compartilhamento de um único endereço IP público por vários dispositivos internos. 

Como funciona o NAT:

- Quando um dispositivo em uma rede privada envia um pacote para a internet, o roteador NAT altera o endereço IP de origem do pacote para seu próprio endereço IP público.

- Ao receber a resposta, o roteador reverte essa tradução, encaminhando o pacote de volta ao dispositivo correto na rede interna.

- Essa operação é transparente para os dispositivos na rede interna e externa, permitindo uma comunicação suave entre as duas redes. 

Tipos de NAT:

- **NAT Estático:**
    
    Um mapeamento um-para-um entre um endereço IP privado e um endereço IP público. 
    

- **NAT Dinâmico:**
    
    Um mapeamento de um conjunto de endereços IP privados para um conjunto de endereços IP públicos. 
    

- **NAT de Sobrecarga (PAT):**
    
    Permite que vários dispositivos compartilhem um único endereço IP público, utilizando diferentes números de porta para distinguir as conexões.

#### A RFC 1918
Define os intervalos de endereços IP que são reservados para uso em redes privadas==, ou seja, redes que não são diretamente acessíveis pela internet pública. Esses endereços não são roteáveis na internet globalmente, permitindo que várias organizações usem os mesmos intervalos de endereços em suas redes internas sem conflitos. 

Os intervalos de endereços IP privados definidos pela RFC 1918 são: 

- **10.0.0.0 a 10.255.255.255**: (10.0.0.0/8)
- **172.16.0.0 a 172.31.255.255**: (172.16.0.0/12)
- **192.168.0.0 a 192.168.255.255**: (192.168.0.0/16) 

Esses endereços são comumente utilizados em redes domésticas, corporativas e outras redes privadas, onde a comunicação é restrita ao ambiente interno ou usa tradução de endereços de rede (NAT) para acessar a internet.

#### IPv6

Estes grupos de 16 bits são representados utilizando a notação hexadecimal,
sendo que cada dígito hexadecimal representa 4 bits separados:  2001:0000:130F:0000:0000:01B1:2341:AA45

#### ICMP - Internet Control Message Protocol

É um protocolo de controle. Não transmite dados. É usado par mensageria entre hoteadores para controle da comunicação.

O protocolo ICMP (Internet Control Message Protocol) ==é um protocolo auxiliar da camada de rede utilizado para enviar mensagens de erro e informações de controle em redes IP==. Ele permite que dispositivos de rede, como roteadores e computadores, comuniquem problemas na transmissão de dados e testem a conectividade. 

O que o ICMP faz:

- **Notifica erros:**
    
    O ICMP informa sobre problemas como pacotes perdidos, rotas inacessíveis, tempo de vida (TTL) expirado ou erros de sintaxe no cabeçalho IP. 
    

- **Testa a conectividade:**
    
    O comando "ping" utiliza o ICMP para verificar se um host está ativo e acessível, enviando pacotes ICMP Echo Request e recebendo Echo Reply. 
    

- **Fornece informações sobre rotas:**
    
    Roteadores podem usar o ICMP para informar sobre rotas alternativas, caso a rota original esteja congestionada ou indisponível. 
    

- **Auxilia em diagnósticos de rede:**
    
    O ICMP é usado em ferramentas como o traceroute para identificar os roteadores ao longo do caminho de um pacote IP. 
    

Como o ICMP funciona:

- O ICMP encapsula suas mensagens em pacotes IP, sendo assim, um usuário do protocolo IP. 

- O ICMP utiliza tipos e códigos de mensagens para especificar o tipo de informação ou erro relatado. 

- Um pacote ICMP pode ser usado para fins maliciosos, como ataques de negação de serviço (DoS), onde pacotes ICMP são enviados em excesso para sobrecarregar um sistema. 

Exemplos de mensagens ICMP:

- **Echo Request/Reply:** Usado pelo comando "ping" para verificar a conectividade.

- **Destination Unreachable:** Informa que o destino do pacote não pode ser alcançado.

- **Time Exceeded:** Informa que o tempo de vida do pacote expirou.

- **Redirect:** Informa sobre rotas alternativas.

- **Parameter Problem:** Informa sobre erros de sintaxe no cabeçalho IP. 

Ataques ICMP:

O ICMP pode ser explorado para ataques de rede, como: 

- **Ping Flood:** Inunda um sistema com pacotes ICMP Echo Request, sobrecarregando-o.

- **Smurf Attack:** Utiliza endereços IP falsificados para amplificar o ataque e sobrecarregar o destino.

- **Ping of Death:** Envia pacotes ICMP com tamanhos maiores que o permitido, podendo causar travamentos.

#### ARP - Address Resolution Protocol

Protocolo para mapeamento de endereços lógicos. 
#### Domínios de broadcast.

### 2 - Enlace de dados

Dispositivos ponto a ponto, intra-rede e controle de fluxo  e de erros
### 1 - Física

Transmissão de bits, convenção de sinais, dispositivos físicos e conexões.


# Protocolo  TCP/IP

## Aplicação

Apresentação dos dados. Criptografia. Certificado digital. 
## Transporte

Comunicação entre dispositivos.
## Internet

Aplicação de endereço IP e melhor caminho pela rede.
## Acesso a rede


# Componentes físicos e camadas de interesse

## Alimentação
Nobreak, baterias, alimentação energia elétrica e refrigeração. 

## Transmissão de dados
Transmissão de dados, configuração de portas, gerenciamento de acessos para segurança.

## Segurança


## Armazenamento


## Processamento


## Acesso

