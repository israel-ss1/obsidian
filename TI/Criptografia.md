#PF 

É o estudo à aplicação de técnicas para comunicação e armazenamento seguro de dados em sistemas computacionais. 

Criptografia significa "escrita secreta"

**Texto Plano ou Puro**: Dados não encriptados.

**Texto Cifrado**: Dados encriptados, inteligíveis.

**Chave** (Key): Termo chave para a aplicação do método de criptografia.

**Algoritmo**: Técnica para tornar o texto inteligível.

**Criptoanálise**: é a quebra de dados cifrados sem a posse da chave.

**Webcrawlers**: Robos de indexação de motores de busca

## Requerimentos de segurança em comunicações

**Autenticação**: Garantir que a mensagem realmente saiu do remetente.

**Integridade**: Deve-se garantir que o conteúdo de uma mensagem deve ser o mesmo que saiu do remetente no destino.

**Confidencialidade**: Garantir que a informação não está disponível a pessoas ou processos que não tenham autorização.

**Não-repúdio**: Garantir que o transmissor não pode se negar de que transmitiu a mensagem.


## Cifras de fluxo (Stream Cipher)
Combina os bits do texto plano com um fluxo de bits pseudo aleatórios, utilizando a porta lógica XOR. Essa chave é bem menor ficando entre 64 a 128 bits, porém é pseudo randômica.
Ex.: RC4, Salsa20, SEAL.
## Cifras de bloco (Block Cipher)
O texto plano é divido em vários planos que serão submetidos à criptografia sequencialmente. Poderá acontecer eventualmente de haver dois blocos iguais, o que é um problema de segurança, então utiliza-se o método de realimentação, onde o resultado anterior é utilizado para criptografia do bloco seguinte. O primeiro bloco é feito com um vetor de inicialização.
Ex.: IDEA, RC5, RC6, AES, Blowfish, CAST, Rijndael, 3DES

## Tipo de criptografia
### Simétrica ou chave privada
A encriptação é feita com uma chave e a decriptação é feita pela mesma chave. A mesma chave é utilizada pelo emissor e pelo receptor. Usada no modo stream.
Ex.: DES, 3DES, Blowfish, AES, OTP (One Time Pad). A chave funciona como uma espécie de seed (semente), que alimenta um gerador de chaves.

Ex.: RC4, Salsa20, SEAL.
#### Cifras simétricas
Uma cifra é definida sobre um par de algoritmos de encriptação e desencriptação. Utiliza cifragem de fluxo e de bloco. 

![[Pasted image 20250602190231.png]]

![[Pasted image 20250602191017.png]]

Algoritmos de encriptação são sempre randomizados.
Algoritmos de desencriptação são sempre determinísticos.

**One Time Pad**
A chave é uma string de bits aleatórias. com pelo menos o mesmo tamanho da mensagem. 
Diz-se que este é um sistema inquebrável. Utiliza-se a porta lógica XOR para encriptar.
### Assimétrica ou chave pública
A encriptação é feita por uma chave pública do receptor e decriptografada por uma chave privada do receptor. Duas chaves são utilizadas no processo.
Usada no modo de bloco. Tamanhos variam de 512 a 2028 bits.
Ex.: DSA, RSA, GPG
### Funções de hash
Utiliza o valor de hash, que é gerado em cima de um texto plano.
Ex.: MD5, SHA1 e SHA2




# Assinatura Digital

ICT Brasil - Padrão oficial de certificação digital no Brasil. É um controle lógico de segurança. Está relacionado a hash de arquivo e troca de certificados de segurança para troca de chaves assimétricas.

## Autenticidade

Certeza de que o documento foi emitido por quem diz ser. Garante autenticidade, integridade e irretratabilidade (não repúdio). Não garante confidencialidade (sigilo). Quem garante o sigilo é a criptografia que pode estar associada a assinatura mas não faz parte dela.

## Integridade

Garantia de que o documento não foi alterado.

## Não repúdio

Uma vez assinado, há a garantia de que o assinante não poderá mais negar a autoria ou que o assinou, também conhecido por irretratabilidade.


# Certificado Digital

Processo eletrônico que é gerado e assinado por uma terceira parte entre duas partes. As empresas que prestam serviço é intermediária entre as partes. Cria um par de chaves criptográficas para cada ente.

## ICP Brasil

Infraestrutura de chaves públicas brasileira, é o processo de certificação digital do Brasil. Dá validade jurídica à transações eletrônicas. Está ligado ao ITI (Instituto Nacional de TEcnologia da Informação) e este tem um AC Raiz.
O ITI credencia as AC (Autoridade Certificadora) e as AR que são as autoridades de registros.

As chaves devem constar: 
- Chave pública do titular;
- Dados do titular;
- Período de validade do certificado;
- Nome da autoridade certificadora;
- Número de série;
- Assinatura digital da AC.

### Tipos de certificados
- De assinatura: A1, A2, A3 e A4.
- De sigilo: S1, S2, S3, e S4
- De tempo: T3 e T4

Certificados de nível 1 valem por 1 ano, de nível 2 por 2 anos, de nível 3 por 5 anos, de nível 4 por 11 anos se for de cadeias hierárquicas em curvas elípticas, se não por 6 anos.
## ACT Autoridade Certificadora do Tempo

Responsável por emitir carimbos do tempo em documentos.


# Mecanismos de autenticação

Os mecanismos de autenticação estão enquadrados em 3 grandes grupos:
- Aquilo que você é - ex.: biometria;
- Aquilo que você possui - ex.: tokens;
- Aquilo que você sabe - ex.: senhas.

