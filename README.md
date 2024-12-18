Phishing para Captura de Senhas do Facebook no Kali Linux
Objetivo: Criar um ataque de phishing utilizando o Kali Linux e o Social Engineering Toolkit (SET) para clonar a página de login do Facebook e capturar as credenciais dos usuários.

Ferramentas Usadas:
Kali Linux: Sistema operacional de segurança que contém diversas ferramentas de pentesting.
Social Engineering Toolkit (SET): Ferramenta especializada em ataques de engenharia social, incluindo phishing.
Passo a Passo Detalhado:
Acessar o Kali Linux como Root:

O acesso root é necessário para garantir permissões adequadas. Execute o comando:
bash
Copiar código
sudo su
Iniciar o Social Engineering Toolkit (SET):

Após obter privilégios de root, inicie o SET digitando:
bash
Copiar código
setoolkit
O SET exibirá um menu interativo.
Escolher o Tipo de Ataque:

Selecione a opção 1 para Social-Engineering Attacks.
Copiar código
1) Social-Engineering Attacks
Escolher o Vetor de Ataque:

Escolha a opção 2 para Website Attack Vectors.
mathematica
Copiar código
2) Website Attack Vectors
Escolher o Método de Ataque:

Escolha a opção 3 para Credential Harvester Attack Method.
mathematica
Copiar código
3) Credential Harvester Attack Method
Em seguida, escolha 2 para Site Cloner, que irá clonar o site de login do Facebook:
Copiar código
2) Site Cloner
Obter o Endereço IP da Máquina:

Utilize o comando ifconfig para encontrar o endereço IP da máquina Kali Linux. Isso é necessário para que a vítima acesse o servidor hospedado no seu Kali:
bash
Copiar código
ifconfig
Anote o endereço IP exibido. Este será utilizado no URL clonado.
Configurar o URL para o Clone:

O SET pedirá a URL do site que deseja clonar. Para clonar o Facebook, use:
arduino
Copiar código
http://www.facebook.com
Realizar o Ataque:

O SET começará a configurar um servidor web que hospeda uma réplica do site de login do Facebook. Assim que a vítima acessar o link que você fornecer, ela será redirecionada para o site falso.
Captura de Credenciais:

O SET registrará todas as credenciais inseridas no site clonado. Você pode visualizar as informações capturadas na tela.
Evidência de Resultados:
Após o ataque ser realizado, você poderá ver as credenciais capturadas através do terminal do Kali Linux. O SET exibe informações como usuário e senha que foram fornecidos no site clonado.

Resultado Esperado:
Aqui está uma captura de tela ilustrativa (hipotética) de como o SET exibe as credenciais capturadas:


Nota: A imagem acima é um exemplo hipotético de como as credenciais podem ser exibidas no terminal após um ataque bem-sucedido.

A saída pode ser parecida com a seguinte:

vbnet
Copiar código
[*] Credentials Harvested from Victim
Username: victim_username
Password: victim_password
Essas credenciais ficam salvas e podem ser acessadas na interface do SET, que registra cada login enviado pela vítima no site clonado.

Importante:
Legalidade: Este tutorial e as ferramentas apresentadas são destinadas a fins educativos. O phishing sem permissão explícita da vítima é ilegal e pode resultar em penalidades severas. Nunca realize esses ataques sem uma autorização explícita em ambientes controlados.
Ética: Utilize essas técnicas apenas em ambientes de teste ou auditorias de segurança com permissão, como parte de uma análise de vulnerabilidade autorizada.