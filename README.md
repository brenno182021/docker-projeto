# Biblioteca IA — Docker Projeto

Biblioteca digital em português sobre inteligência artificial, Codex e aprendizado em desenvolvimento. Projeto educacional com HTML, CSS e Apache executado pelo Docker Compose.

![Ilustração da biblioteca](website/assets/library.svg)

## O que você encontra

- Página responsiva com navegação por seções e cartões de leitura.
- Artigo sobre as vantagens do Codex e o papel da revisão humana.
- Quatro ilustrações SVG originais e locais, sem dependências externas.
- HTML semântico, foco visível, link para pular ao conteúdo e respeito à preferência por movimento reduzido.
- Nenhum framework, etapa de build, chave de API ou serviço pago.

## Executar com Docker

Instale o Docker Desktop (ou Docker Engine com Compose) e mantenha-o em execução. No Windows, compartilhe a unidade do projeto com o Docker caso necessário.

```powershell
cd D:\programacao\dio\docker-projeto
docker compose up -d
```

Acesse **http://localhost**. O Compose usa Apache `httpd:2.4`, publica a porta 80 e monta `website/` como somente leitura. Alterações nos arquivos aparecem após atualizar a página.

```powershell
docker compose ps
docker compose logs apache
docker compose down
```

Se a porta 80 estiver ocupada, altere o mapeamento em `compose.yml` para `8080:80`, recrie o contêiner com `docker compose up -d` e acesse http://localhost:8080.

Também é possível abrir `website/index.html` no navegador para visualizar o conteúdo sem Docker.

## Estrutura

```text
docker-projeto/
├── compose.yml
├── README.md
├── LICENSE
└── website/
    ├── index.html
    └── assets/
        ├── style.css
        ├── library.svg
        ├── code.svg
        ├── books.svg
        └── containers.svg
```

## Personalizar

Edite o conteúdo em `website/index.html` e as cores, espaçamentos e comportamento responsivo em `website/assets/style.css`. Os SVGs podem ser editados como texto ou com um editor vetorial.

## Referência

O artigo usa a [biblioteca oficial de recursos do Codex da OpenAI](https://developers.openai.com/learn/codex) como referência. Os benefícios dependem do contexto e da revisão; resultados gerados por IA precisam ser verificados. Este projeto é independente e não tem afiliação com a OpenAI ou a DIO.

## Autor e licença

Criado por [Glayson Brenno](https://github.com/brenno182021). Código, conteúdo e ilustrações deste repositório estão disponíveis sob a [licença MIT](LICENSE).
