# cibersecurity-desafio-phishing
O objetivo deste laboratório foi demonstrar a eficácia de ataques de Engenharia Social utilizando a ferramenta *Social-Engineering Toolkit (SET)* para a criação de uma página de phishing e captura de credenciais (Credential Harvester).

Este projeto foi desenvolvido estritamente para fins educacionais e acadêmicos. O uso das técnicas aqui apresentadas em cenários reais sem autorização é ilegal e antiético.

Configurando o phishing no kali linux:
Ambiente Utilizado
* *Atacante:* Kali Linux (IP: 192.168.0.105)
* *Vítima:* Windows 10 (Navegador Edge/Chrome)
* *Ferramenta:* SEToolkit (Website Attack Vectors -> Credential Harvester)
* *Túnel/Exposição:* Python3 HTTP Server (para PoC controlada)

Passo a passo:

-Acesso root sudo su

-Iniciando o setoolkit: setoolkit

-Tipo de ataque: Social-Engineering Attacks

-Vetor de ataque: Web Site Attack Vectors

-Método de ataque: Credential Harvester Attack Method 

-Método de ataque: Site Cloner

-Obtendo o endereço de URL (192.168.0.5)

-URL para clone: http://www.facebook.com


**Resutados:**

<img width="1053" height="665" alt="Captura de tela 2026-01-25 182501" src="https://github.com/user-attachments/assets/dff08f05-0321-435c-bf12-8c5d5b0717d8" />

Durante os testes iniciais, observou-se que grandes plataformas utilizam defesas modernas que dificultam a clonagem automática via SEToolkit

<img width="621" height="262" alt="Captura de tela 2026-01-25 182701" src="https://github.com/user-attachments/assets/ae1028e3-b9e3-417d-896d-23e10d8cd232" />

Até mesmo no log da ferramenta não se encontra nada, até mesmo usando o comando grep para pesquisar pelo nome ficticio do email criado, sem resultados, e tambem na pasta expecifica do web clone.

Podemos ver que alguns sites ultilizam do login em duas etapas, como é o caso do mercado livre, dificultando assim o phishing com ferramentas como essa, onde na primeira pagina e o login e na segunda pagina a senha.

<img width="731" height="464" alt="Captura de tela 2026-01-25 184756" src="https://github.com/user-attachments/assets/3e7de450-123c-4aa8-9564-6350616c7966" />

<img width="1103" height="443" alt="Captura de tela 2026-01-31 213440" src="https://github.com/user-attachments/assets/1038ecf3-f0a7-4789-8b4b-7d42891c32d9" />


Solução Final: PoC com Custom HTML
Para validar o funcionamento da captura de dados (POST), foi desenvolvida uma página de login simplificada em HTML5, hospedada localmente via Python e clonada pelo SEToolkit.

#### Passo a passo da execução:
1. Criação do arquivo simples.html.
2. Inicialização do servidor: python3 -m http.server 8080.
3. Configuração do SEToolkit para clonar a URL local.
4. Acesso da vítima e inserção de dados.

<img width="1143" height="573" alt="Captura de tela 2026-01-30 095235" src="https://github.com/user-attachments/assets/2d4a1052-fb39-4bb7-be16-486a3e0d38ef" />
<img width="689" height="319" alt="Captura de tela 2026-01-30 095211" src="https://github.com/user-attachments/assets/3a5b81d8-7c34-415a-9ac3-9ffc7280cb5b" />
O desafio se encerraria por ai, até vir a ideia de testar um site de jogos que tem login e senha na mesma etapa, Rockstar Games:
<img width="1282" height="676" alt="Captura de tela 2026-01-31 210627" src="https://github.com/user-attachments/assets/8f31a81d-1527-4f4e-9095-3705984cc473" />
<img width="857" height="157" alt="Captura de tela 2026-01-31 210052" src="https://github.com/user-attachments/assets/f6a5db21-d19e-41bd-9716-1544e4c4e0ce" />

Conclusão
O laboratório comprovou que, embora defesas modernas dificultem ataques genéricos, a Engenharia Social aliada a páginas customizadas continua sendo um vetor crítico, uma URL falsa quando passa disapercebido pode causar graves problemas. A principal defesa contra esse ataque é o treinamento de usuários e o uso de autenticação multifator.
