# AbnTex 2 IME

Este é o modelo LaTex de tese e dissertação de pós-graduação do Instituto Militar de Engenharia.

Os objetivos deste modelo são:

- Padronizar o texto de trabalhos acadêmicos de acordo com as normas da ABNT
- Acelerar a checagem de formatação dos trabalhos acadêmicos pela biblioteca para a emissão de certificado de conclusão de curso

## Citações

O modelo usa por padrão citações numéricas e com parênteses, e.g. (1), permitido pela ABNT.

Se quiser usar o citação alfabética, e.g. (MOREIRA et al., 2019), procure e alterne o comentário do seguinte trecho do arquivo *main.tex*.

```
De:
\usepackage[num,abnt-etal-list=0,bibjustif]{./abntex2cite} % Citações numéricas (ordem de apresentação)
%\usepackage[alf,abnt-etal-list=0,bibjustif]{./abntex2cite} % Citações autor-data (ordem alfabética)

Para:
%\usepackage[num,abnt-etal-list=0,bibjustif]{./abntex2cite} % Citações numéricas (ordem de apresentação)
\usepackage[alf,abnt-etal-list=0,bibjustif]{./abntex2cite} % Citações autor-data (ordem alfabética)
```


## Criar e remover arquivos de conteúdo

Arquivos podem ser incluídos no documento com o comando *\input{}*

```
\input{nome-do-arquivo_sem-tex}
```

Se o seu arquivo se chama resultados.tex, então:

```
\input{resultados}
```

Para remover os arquivos de exemplo do seu documento procure pelas linhas abaixo no arquivo *main.tex*.

```
\input{exemplo-intro}
\input{exemplo-cap-01}
\input{exemplo-cap-02}
\input{exemplo-conclusao}
...
\input{exemplo-apendice}
...
\input{exemplo-anexo}
```

Tenha cuidado para adicionar os elementos textuais, o apendice e o anexo nos locais onde estão no arquivo *main.tex*, pois a ordem e o local onde aparecem influi no documento final gerado.

## Outras informações

Mais informações podem ser encontradas em https://www.abntex.net.br/