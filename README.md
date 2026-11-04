# Projeto Solidariedade — Linhares/ES

Protótipo de site comunitário para apresentar iniciativas sociais de Linhares (ES) e aproximar pessoas interessadas em contribuir. O projeto mantém a proposta visual e os recursos do HTML original: navegação por seções, abas institucionais, simulador de impacto, filtro de projetos, Radar Solidário com modal, prestação de contas, mapa interativo, FAQ, depoimentos e área de doação.

## Demonstração

Depois de publicar no GitHub Pages, o site ficará disponível no endereço:

`https://SEU-USUARIO.github.io/NOME-DO-REPOSITORIO/`

## Como executar localmente

1. Baixe ou clone este repositório.
2. Abra a pasta do projeto.
3. Abra `index.html` no navegador.

Para uma experiência mais próxima da hospedagem, também é possível iniciar um servidor local simples:

```bash
python -m http.server 8000
```

Depois, acesse `http://localhost:8000`.

## Publicar no GitHub Pages

1. Entre no GitHub e crie um repositório (por exemplo, `projeto-solidariedade-linhares`).
2. Envie os arquivos deste projeto para a raiz do repositório. O arquivo inicial precisa se chamar **`index.html`**.
3. No repositório, abra **Settings → Pages**.
4. Em **Build and deployment**, selecione **Deploy from a branch**.
5. Escolha a branch `main` e a pasta `/ (root)`.
6. Clique em **Save** e aguarde a publicação.
7. O GitHub exibirá o endereço público do site na mesma tela.

## Estrutura

```text
Projeto-Solidariedade-GitHub/
├── index.html
└── README.md
```

O projeto é estático: não exige PHP, banco de dados ou processo de build. O GitHub Pages consegue hospedar os arquivos diretamente.

## Bibliotecas e serviços externos

- [Leaflet](https://leafletjs.com/) — mapa interativo.
- [OpenStreetMap](https://www.openstreetmap.org/) — camada de mapas.
- [Font Awesome](https://fontawesome.com/) — ícones.
- [QR Server](https://goqr.me/api/) — geração visual do QR Code apresentado no protótipo.

Esses recursos são carregados por CDN/serviços externos; portanto, o navegador precisa de conexão com a internet para exibi-los. Respeite os termos e atribuições de cada serviço.

## Atenção antes de divulgar publicamente

Esta entrega é uma adaptação técnica do protótipo fornecido, não uma auditoria das instituições ou das informações nele apresentadas. Antes de divulgar o endereço como canal oficial de doação:

- **Mapa:** os quatro pares de coordenadas foram mantidos do arquivo original, mas não estavam acompanhados de endereços comprovados. Os marcadores estão identificados no site como aproximados/ilustrativos. Confirme cada endereço e substitua latitude/longitude no array `locais`, no final do `index.html`.
- **Instituições, histórias, depoimentos e relatórios:** confirme nomes, descrições, datas, números e autorizações de publicação. Conteúdos narrativos e dados de prestação de contas do protótipo não devem ser tratados como comprovação documental.
- **PIX e QR Code:** a chave de e-mail e o QR Code foram preservados do HTML original. Confirme formalmente o titular e a titularidade da chave com a instituição responsável antes de receber ou divulgar doações. O QR Code atual é gerado a partir do texto da chave e não comprova, por si só, a titularidade nem garante uma cobrança PIX válida.
- **WhatsApp:** substitua o número de exemplo `5527999999999` pelo contato oficial.
- **Formulário:** nesta versão, o formulário apenas valida os campos no navegador e exibe um aviso. Ele **não envia nem armazena** os dados. Para receber inscrições, conecte um serviço de formulários ou desenvolva um backend com política de privacidade e proteção de dados.
- **Relatório PDF:** o botão foi identificado como demonstrativo porque o arquivo original não continha um PDF para download. Inclua o documento oficial e atualize o botão para apontar para o arquivo real.
- **Declarações de segurança/auditoria:** só use expressões como “verificada”, “auditada” ou “100% segura” quando houver processo e evidências que sustentem essas afirmações.

## Personalização do mapa

No final do `index.html`, procure o bloco:

```javascript
const locais = [
    { nome: "CLAM - Centro Linharense", lat: -19.3950, lng: -40.0650 },
    { nome: "Associação Pestalozzi", lat: -19.3850, lng: -40.0780 },
    { nome: "ADEFIL Linhares", lat: -19.3980, lng: -40.0600 },
    { nome: "Abrigo de Luz", lat: -19.4020, lng: -40.0710 }
];
```

Troque `lat` e `lng` pelas coordenadas confirmadas de cada instituição. Você pode obtê-las no OpenStreetMap ou em outro serviço de mapas, conferindo o endereço com a própria instituição. Não publique coordenadas residenciais ou dados pessoais sem autorização.

## Licença

Nenhuma licença foi definida nesta versão. Se pretende permitir reutilização pública do código, escolha e adicione uma licença (por exemplo, MIT) somente se tiver os direitos necessários sobre todo o conteúdo e os recursos utilizados.
