# IA responsável na educação potiguar

Site estático que acompanha os três folders da série **IA responsável na educação potiguar**. É o destino dos QR codes impressos e reúne:

- o texto integral e acessível de cada folder;
- os documentos citados (Referencial do MEC, Decreto RN nº 32.815/2023, IN CONTROL/RN nº 02/2023, Lei nº 14.533/2023);
- as referências completas em ABNT, com links;
- autoria, como citar, licença e a declaração de uso de IA.

Realização: GT de Inteligência Artificial na Educação (2026.2), PPgITE/IMD/UFRN.

## Estrutura

```
.
├── index.html                    Página inicial (destino geral)
├── protecao-de-dados.html        Folder "Dado público não vai para conta pessoal"
├── trabalho-do-gestor.html       Folder "A IA rascunha. Você confere e assina."
├── orientacao-nas-escolas.html   Folder "Primeiro aprender sobre a IA..."
├── referencias.html              Referências completas e documentos
├── sobre.html                    Autoria, como citar, licença, uso de IA
├── 404.html
├── assets/css/style.css
├── assets/img/icone.svg
├── documentos/                   PDFs citados e PDF de impressão dos folders
└── vercel.json                   URLs sem ".html" e cabeçalhos
```

Não há etapa de build: o Vercel publica os arquivos como estão.

## Publicar

1. Crie um repositório no GitHub e envie o conteúdo desta pasta para a raiz dele.
2. No Vercel: **Add New → Project**, importe o repositório.
   - Framework Preset: **Other**
   - Build Command: deixe vazio
   - Output Directory: deixe vazio (raiz)
3. Clique em **Deploy**. Cada novo commit na branch principal republica o site.
4. Opcional: em **Settings → Domains**, associe um domínio institucional. Um endereço da UFRN ou do Governo do RN é melhor que um encurtador ou serviço pessoal, por coerência com a mensagem dos folders.

O arquivo `documentos/referencial-ia-educacao-mec-2026.pdf` tem cerca de 28 MB, abaixo do limite de 100 MB por arquivo do GitHub.

## QR codes

Endereços sugeridos para cada folder impresso:

| Folder | Endereço |
| --- | --- |
| Dado público não vai para conta pessoal | `https://SEU-DOMINIO/protecao-de-dados` |
| A IA rascunha. Você confere e assina. | `https://SEU-DOMINIO/trabalho-do-gestor` |
| Primeiro aprender sobre a IA... | `https://SEU-DOMINIO/orientacao-nas-escolas` |
| Um QR único para os três | `https://SEU-DOMINIO/` |

Para gerar o QR em SVG (vetorial, bom para impressão), com Node instalado:

```
npx qrcode -t svg -e M -o qr-protecao-de-dados.svg "https://SEU-DOMINIO/protecao-de-dados"
```

Imprima com pelo menos 2 cm de lado e teste a leitura em dois ou três celulares antes da tiragem.

## O que confirmar antes de divulgar

Os trechos destacados em amarelo no site (`[entre colchetes]`) aguardam confirmação:

- [ ] URL oficial do Referencial no portal do MEC
- [ ] Links oficiais: Resolução CNE/CEB nº 2/2025, Enunciado CD/ANPD nº 1/2023, guia da Secom, painel Escolas Conectadas, página do PPgITE
- [ ] Contato do encarregado de dados da SEEC/RN e canal de suporte de TI
- [ ] Domínio do e-mail institucional
- [ ] Protocolos de incidente com dados e de montagens com IA entre estudantes
- [ ] Lista oficial de ferramentas de IA autorizadas; edição do Workspace contratada e situação do Gemini
- [ ] Nomes e funções da equipe do GT, licença e redação final da declaração de uso de IA
- [ ] URL final deste site (seção "Como citar" em `sobre.html`)

Para editar, altere o HTML diretamente. Os textos dos folders estão nos três arquivos de folder; o rodapé e o menu se repetem em todas as páginas.

## Atualização

Termos de serviço e normas mudam. Ao revisar, atualize a data no rodapé de cada página ("Versão 1.0 · outubro de 2026") e a seção "Versão" em `sobre.html`.
