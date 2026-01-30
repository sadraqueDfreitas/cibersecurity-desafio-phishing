# cibersecurity-desafio-phishing
Desafio de phishing para capturas de senhas do facebook, ultilizando as ferramentas Kali linux e setoolkit

Configurando o phishing no kali linux:

-Acesso root sudo su

-Iniciando o setoolkit: setoolkit

-Tipo de ataque: Social-Engineering Attacks

-Vetor de ataque: Web Site Attack Vectors

-Método de ataque: Credential Harvester Attack Method 

-Método de ataque: Site Cloner

-Obtendo o endereço da máquina: ifconfig

-URL para clone: http://www.facebook.com


**Resutados:**

<img width="1053" height="665" alt="Captura de tela 2026-01-25 182501" src="https://github.com/user-attachments/assets/dff08f05-0321-435c-bf12-8c5d5b0717d8" />

Tentei o teste algomas vezes, porem sem resultado, logo imaginei que as defesas do facebook melhoraram desde a época do desafio do curso (4 anos atrás), ainda sim procurei pelo resultado no sistema de log do setoolkit:

<img width="621" height="262" alt="Captura de tela 2026-01-25 182701" src="https://github.com/user-attachments/assets/ae1028e3-b9e3-417d-896d-23e10d8cd232" />

Testei com o comando grep pesquisar pelo nome ficticio do email criado, no grande arquivo de log do set e sem resultados, e tambem na pasta expecifica do web clone, e sem resultados, e resolvi testar em outro site que foi o do mercado livre:

<img width="731" height="464" alt="Captura de tela 2026-01-25 184756" src="https://github.com/user-attachments/assets/3e7de450-123c-4aa8-9564-6350616c7966" />

Esses sites como mecanismo de segurança fazem login em duas etapas, primeiro o usuario e em seguida na proxima pagina onde se insere a senha, tirando assim a possibilidade de extrair as informações com ferramentas desse tipo. Pode se ver em vermelho onde apenas a informação de usuario foi extraida. E para finalizar, criei eu mesmo uma pagina para testar a ferramenta, pois nao estava encontrando possiveis
sites para realizar o desafio. Com a ferramenta Phyton3 e um simples codigo, criei uma pagina de login e senha:

<img width="1143" height="573" alt="Captura de tela 2026-01-30 095235" src="https://github.com/user-attachments/assets/2d4a1052-fb39-4bb7-be16-486a3e0d38ef" />
<img width="689" height="319" alt="Captura de tela 2026-01-30 095211" src="https://github.com/user-attachments/assets/3a5b81d8-7c34-415a-9ac3-9ffc7280cb5b" />
