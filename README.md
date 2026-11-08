# NOMO — Plataforma Centralizada de Prévias Médicas

Ecossistema digital de alta conversão desenvolvido para apresentação de conceitos e prévias de sites para médicos e cirurgiões plásticos, hospedado em domínio único na **Vercel**.

---

## 🏛️ Arquitetura do Projeto

```text
├── index.html            <- Plataforma Principal de Gestão & Tela de Proteção / Segurança
├── vercel.json           <- Regras de roteamento limpo (cleanUrls), rewrites e cache
├── clients_data.json     <- Base de dados com os 57 clientes/médicos mapeados
├── package.json          <- Configuração do projeto estático
└── p/                    <- Diretório contendo os 57 sites médicos independentes
    ├── dr-carlos-gaspar/
    │   ├── index.html    <- Site puro do Dr. Carlos Gaspar (otimizado mobile)
    │   └── arquivos/     <- Imagens em alta resolução
    ├── dr-edson-freitas/
    ├── dra-camilla-rossiter/
    └── ... (57 médicos)
```

---

## 🔒 1. Segurança & Tela Pública Anti-Curioso

Caso algum médico, cliente ou visitante tente **apagar o final da URL** e acessar o domínio raiz (`https://nomo-sites.vercel.app`):
- Ele **NÃO** verá a lista de concorrentes nem os dados dos outros clientes.
- Ele verá uma **página de alto padrão institucional** (*NOMO - Ambiente Exclusivo de Homologação*).
- Há um botão de destaque redirecionando para o **seu WhatsApp**: `(11) 93953-7491`.
- **Acesso ao Painel do Gestor:**
  - Clique no botão discreto **"Acesso Gestor"** no canto superior direito ou rodapé.
  - Insira o PIN de segurança padrão: **`2026`**.
  - O painel desbloqueia instantaneamente com busca, filtros e botões de cópia.

---

## 📱 2. Otimizações Mobile Implementadas em Cada Site

Todos os 57 sites receberam um tratamento de design e performance para versão mobile:
1. **Tipografia Fluida:** Títulos ajustados dinamicamente para não quebrarem palavras no celular.
2. **Correção de Hover em Telas Touch:** A descrição dos procedimentos agora é imediatamente visível em smartphones.
3. **Menu & Ação Rápida no Topo:** Botão "Agendar" direto na barra de navegação no celular.
4. **Espaçamento Harmônico:** Redução do respiro excessivo vertical no mobile para rolagem fluida e confortável.
5. **Preloader Ágil:** Redução do tempo de espera de 1.5s para 500ms suave.
6. **Botão de WhatsApp Flutuante:** Posicionado considerando a área segura (*safe area*) do iPhone e Android com link verificado para o WhatsApp de cada doutor.
7. **Formulário de Aplicação Conectado:** Submissão do formulário redireciona diretamente para o WhatsApp do respectivo doutor com mensagem preenchida.

---

## 🌐 3. Sugestões de Domínios para a Vercel

Ao criar o projeto na [Vercel](https://vercel.com), você pode escolher um nome personalizado para o subdomínio `.vercel.app`:

| Sugestão de Subdomínio | URL Completa | Perfil de Posicionamento |
| :--- | :--- | :--- |
| **nomo-sites** *(Oficial)* | `nomo-sites.vercel.app` | Domínio oficial de produção da plataforma |
| **medpreview** | `medpreview.vercel.app` | Direto ao ponto, internacional e tecnológico |
| **medprevia** | `medprevia.vercel.app` | Claro e natural em português |
| **vitrinemedica** | `vitrinemedica.vercel.app` | Comercial e de alto valor percebido |
| **privadomed** | `privadomed.vercel.app` | Enfatiza sigilo e exclusividade |
| **exclusivamed** | `exclusivamed.vercel.app` | Posicionamento premium para cirurgia estética |

*(Caso o nome exato já esteja em uso por outro usuário global, basta adicionar um sufixo leve, ex: `nomo-br.vercel.app` ou `nomo-labs.vercel.app`)*.

---

## 🚀 4. Como Hospedar na Vercel em 2 Minutos

### Opção A: Pelo Terminal (Vercel CLI)
1. Abra o terminal nesta pasta (`sitess`).
2. Digite:
   ```bash
   npx vercel
   ```
3. Siga as instruções no terminal:
   - *Set up and deploy?* **Y**
   - *Which scope?* Selecione sua conta
   - *Link to existing project?* **N**
   - *What's your project's name?* Digite o nome: `nomo-sites`
   - *In which directory is your code located?* `./` (Enter)
4. Pronto! O projeto será carregado e a URL ao vivo será gerada.

### Opção B: Pelo Painel Web da Vercel (Import Git / Deploy)
1. Suba esta pasta para um repositório no seu GitHub.
2. Acesse [vercel.com/new](https://vercel.com/new) e importe o repositório.
3. Clique em **Deploy**. A Vercel detectará o projeto estático automaticamente.

---

## 📋 5. Lista Completa dos 57 Médicos e Links de Prévia

| # | Médico / Clínica | Telefone / WhatsApp | Rota Limpa no Domínio |
| :--- | :--- | :--- | :--- |
| 1 | Clínica Dr. Carlos Gaspar | (11) 96015-8581 | `/p/dr-carlos-gaspar/` |
| 2 | Dr. Edson Freitas | (71) 99610-1799 | `/p/dr-edson-freitas/` |
| 3 | Dra. Marcelly Cardoso | (21) 99265-7252 | `/p/dra-marcelly-cardoso/` |
| 4 | Dra. Ariane Ribeiro | (63) 98464-9004 | `/p/dra-ariane-ribeiro/` |
| 5 | Dra. Camilla Rossiter | (82) 98828-3324 | `/p/dra-camilla-rossiter/` |
| 6 | Dr. Adriano Pereira | (11) 98990-8993 | `/p/dr-adriano-pereira/` |
| 7 | Dra. Érica Nascimento | (71) 99655-7734 | `/p/dra-erica-nascimento/` |
| 8 | Dra. Lorena Amaral & Dr. Daniel Gonçalves | (91) 98306-3222 | `/p/dra-lorena-amaral-dr-daniel-goncalves/` |
| 9 | Dra. Estela Biazotto Leão | (34) 99941-0603 | `/p/dra-estela-biazotto-leao/` |
| 10 | Clínica Dra. Mariana Moraes | (11) 96016-3781 | `/p/clinica-dra-mariana-moraes/` |
| 11 | Dra. Thaís Mathias | (21) 97302-0796 | `/p/dra-thais-mathias/` |
| 12 | Clinica Barcellos (Dra. Cláudia & Dra. Cristiane) | (51) 99258-7637 | `/p/clinica-barcellos/` |
| 13 | Dr. Cleber Santos Junior | (51) 99377-1048 | `/p/dr-cleber-santos-jr/` |
| 14 | Dr. Geovani Baptista | (54) 99674-4996 | `/p/dr-geovani-baptista/` |
| 15 | Dra. Bárbara Regert | (51) 99744-6593 | `/p/dra-barbara-regert/` |
| 16 | Dr. João Carlos Müller | (53) 98401-6961 | `/p/dr-joao-carlos-muller/` |
| 17 | Dr. Giovani Godinho | (62) 98330-1651 | `/p/dr-giovani-godinho/` |
| 18 | Dr. William de C. Teixeira | (15) 99823-4727 | `/p/dr-william-teixeira/` |
| 19 | Dr. Rodrigo Inácio Fernandes | (18) 99760-4080 | `/p/dr-rodrigo-inacio-fernandes/` |
| 20 | Clínica Dr. Josué Okabayashi | (18) 99691-4943 | `/p/dr-josue-okabayashi/` |
| 21 | Dr. Ádamo Yoshiki | (12) 99190-1755 | `/p/dr-adamo-yoshiki/` |
| 22 | Dr. Eric Frederik | (21) 97047-4076 | `/p/dr-eric-frederik/` |
| 23 | Dr. Ricardo Picanço | (21) 99299-5153 | `/p/dr-ricardo-picanco/` |
| 24 | Dr. Alberto Andrade | (21) 95959-3577 | `/p/dr-alberto-andrade/` |
| 25 | Dr. Marcelo Nanci | (21) 96740-0615 | `/p/dr-marcelo-nanci/` |
| 26 | Clínica Dra. Ana Mamari | (21) 99994-6662 | `/p/clinica-dra-ana-mamari/` |
| 27 | Dra. Karin Lerner | (21) 99871-8121 | `/p/dra-karin-lerner/` |
| 28 | Dr. Cláudio Ramos | (21) 96784-7519 | `/p/dr-claudio-ramos/` |
| 29 | Dr. André Ramos | (21) 99591-2024 | `/p/dr-andre-ramos/` |
| 30 | Dra. Milena Burégio | (21) 99705-2591 | `/p/dra-milena-buregio/` |
| 31 | Dr. Raul Kastrup | (21) 99968-6189 | `/p/dr-raul-kastrup/` |
| 32 | Dra. Wania Furtado | (22) 99797-0222 | `/p/dra-wania-furtado/` |
| 33 | Dr. Dante Locateli | (24) 99961-0177 | `/p/dr-dante-locateli/` |
| 34 | Dr. Paulo Hvenegaard | (24) 99811-1277 | `/p/dr-paulo-hvenegaard/` |
| 35 | Dr. Carlos Henrique Aquino | (22) 99975-1817 | `/p/dr-carlos-henrique-aquino/` |
| 36 | Dr. Márcio Mittmann | (94) 99199-3490 | `/p/dr-marcio-mittmann/` |
| 37 | Dra. Laís Isobe | (43) 98828-3181 | `/p/dra-lais-isobe/` |
| 38 | La Sève Cirurgia Plástica | (16) 99258-1181 | `/p/la-seve-cirurgia-plastica/` |
| 39 | Dra. Vanessa Rajo | (21) 99664-0714 | `/p/dra-vanessa-rajo/` |
| 40 | Plastical | (31) 98046-1092 | `/p/plastical/` |
| 41 | Unique Cirurgia Plástica | (61) 98314-7771 | `/p/unique-cirurgia-plastica/` |
| 42 | Dr. Wolff Hans | (71) 99201-8177 | `/p/dr-wolff-hans/` |
| 43 | Dr. Lauro Avellan | (31) 98987-5659 | `/p/dr-lauro-avellan/` |
| 44 | Dr. Johnny Hayck | (31) 99449-2468 | `/p/dr-johnny-hayck/` |
| 45 | Dr. Daniel Dias | (81) 98220-9416 | `/p/dr-daniel-dias/` |
| 46 | Dr. Rubem Lima | (81) 99252-5334 | `/p/dr-rubem-lima/` |
| 47 | Dra. Rafaela Cavaca | (11) 91628-7180 | `/p/dra-rafaela-cavaca/` |
| 48 | Dra. Leila Azem | (21) 99661-0612 | `/p/dra-leila-azem/` |
| 49 | Dr. Ricardo Fabrini | (21) 99168-9799 | `/p/dr-ricardo-fabrini/` |
| 50 | Dr. Bruno Janin | (21) 97100-4710 | `/p/dr-bruno-janin/` |
| 51 | Dr. Bruno Gazire | (22) 99824-3581 | `/p/dr-bruno-gazire/` |
| 52 | Dr. Euller Granato | (33) 98428-7294 | `/p/dr-euller-granato/` |
| 53 | Dr. Iarley Peron Faria | (33) 99978-1367 | `/p/dr-iarley-peron-faria/` |
| 54 | Dr. Manoel Lopes | (33) 99180-1100 | `/p/dr-manoel-lopes/` |
| 55 | Dr. Afrânio Bernardes | (41) 99621-9875 | `/p/dr-afranio-bernardes/` |
| 56 | Dr. Leandro Vasques | (41) 98843-2406 | `/p/dr-leandro-vasques/` |
| 57 | Dr. Antônio Dourado | (41) 98507-4952 | `/p/dr-antonio-dourado/` |

---
*Desenvolvido e estruturado para alta conversão e abordagem de autoridade.*
