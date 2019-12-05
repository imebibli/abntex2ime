# AbnTex 2 IME

Este é o modelo LaTex de documento adotado pelo Instituto Militar de Engenharia como formato de seus trabalhos de tese e dissertação de pós-graduação.

Os objetivos deste modelo são:

- Padronizar o modelo de texto de trabalhos acadêmicos
- Acelerar os procedimentos de revisão de trabalhos acadêmicos
- Manter a aderência às normas da ABNT nos textos produzidos
- Manter a simplicidade do modelo AbnTex2

O modelo se encontra em desenvolvimento e somente receberá número de versão 1.0 quando o primeiro trabalho usando o modelo for aprovado pela Subdivisão de Cursos de Pós-Graduação do IME.

## Migração

Alguns alunos já utilizam o modelo Latex não-oficial do IME, esta sessão tem por objetivo apontar as principais diferenças observadas na migração para este modelo.

### Migração de citações

O modelo não-oficial do IME utiliza a biblioteca de citações *natlib* enquanto este modelo possui seu próprio formato, o *abntex2cite*.

Usando *natlib*, estas são as citações mais usadas e suas representações no texto.

```
\citet{jon90}  ⇒ Jones et al. (1990)
\citep{jon90}  ⇒ (Jones et al., 1990)
\citet*{jon90} ⇒ Jones, Baker, and Williams (1990)
\citep*{jon90} ⇒ (Jones, Baker, and Williams, 1990)
```

Neste modelo, optamos por citações numéricas e com colchetes, e.g. [1], seguindo um padrão de citação bastante utilizado em artigos internacionais e permitido pela ABNT. Assim, no *abntex2cite* podemos citar da seguinte maneira:

```
\cite{plataforma}        ⇒ [36]
\citeonline{jon90}       ⇒  36
\citeyear{jon90}         ⇒ 2017
\citeauthor{jon90}       ⇒  Bernardo, Silva e Rosa[36]
\citeauthoronline{jon90} ⇒ Bernardo, Silva e Rosa
\citetext{plataforma}    ⇒  BERNARDO, R. M.; SILVA,L. C. B. da; ROSA, P. F. F. Concepção de uma plataforma de vant de baixo custo do tipo quadricóptero para uso em pesquisas. In:Workshop de Comunicação em SistemasEmbarcados Críticos (WoCCES). Belém: SBC, 2017. p. 56–65.
```

A norma faculta o uso de referências no modo alfabético, para usá-lo consulte a documentação do [*abntex2cite*](http://mirrors.ibiblio.org/CTAN/macros/latex/contrib/abntex2/doc/abntex2cite.pdf).
