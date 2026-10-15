# arm-wordlists

Wordlists curadas para pentest, bug bounty e red team. Enumeração de API, DNS, conteúdo web, usuários e senhas.

## Estrutura

```
arm-wordlists/
├── Discovery-API/              # 13 wordlists — endpoints, objetos e ações de API
├── Discovery-DNS/              # 14 wordlists — subdomínios e resolvers DNS
├── Discovery-Web-Content/      # 19 wordlists — diretórios, arquivos e extensões web
├── Passwords/
│   ├── Common-Credentials/     # 16 listas — senhas mais usadas/vazadas
│   └── Default-Credentials/    # 11 listas — credenciais padrão por serviço
├── Usernames/                  # 6 wordlists de nomes de usuário
├── words_and_files_top*.txt    # listas gerais (100 a 20000 entradas)
├── npm-10000.txt
├── pincodes.txt
├── dotfiles.txt
└── files_top20.txt

```

## Uso

```bash
git clone https://github.com/Armidge/arm-wordlists.git

# Enumeração de conteúdo web
ffuf -u https://armidge[.]com/FUZZ -w Discovery-Web-Content/common.txt

# Credenciais padrão de um serviço específico
hydra -L Usernames/top-usernames-shortlist.txt -P Passwords/Default-Credentials/ssh-betterdefaultpasslist.txt ssh://armidge[.].com

```

> Use apenas em sistemas que você possui ou nos quais tem autorização explícita para testar.

## Licença

Este repositório é distribuído sob a licença [MIT](https://github.com/Armidge/arm-wordlists/blob/main/LICENSE).

Parte do conteúdo foi adaptada e reestruturada a partir de:

-   **[SecLists](https://github.com/danielmiessler/SecLists)** (Daniel Miessler, Jason Haddix, Ignacio Portal, g0tmi1k) — MIT. Ver [THIRD-PARTY-LICENSES.md](https://github.com/Armidge/arm-wordlists/blob/main/THIRD-PARTY-LICENSES.md).
-   **[onvio/wordlists](https://github.com/onvio/wordlists)** — sem licença definida no repositório original; crédito incluído por transparência.

## arm-wordlists --author

Por Jeyson S. Rodrigues (Armidge). | Email: [jsonsecurity@gmail.com](mailto:jsonsecurity@gmail.com) // 💬 Telegram: [@Armidge](https://t.me/Armidge)
