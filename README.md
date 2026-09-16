# Análise de Tráfego HTTP com Wireshark

Artigo da disciplina **Segurança e Auditoria de Sistemas de Informação (SASI)**
- UFVJM, 2026/2, escrito no template LaTeX da SBC.

Autores: Murilo Santiago Escobedo e Pávila Miranda Cardoso.

## Estrutura

```
artigo/
  main.tex              # artigo principal (introdução, métodos, resultados, conclusão, referências)
  referencias.bib       # bibliografia (BibTeX)
  sbc-template.sty       # estilo oficial da SBC
  sbc.bst                # estilo de bibliografia da SBC
  img/                    # capturas de tela utilizadas como figuras
```

## Compilando localmente

```bash
cd artigo
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

## CI/CD

O workflow [`build-pdf.yml`](.github/workflows/build-pdf.yml) compila o artigo
automaticamente a cada push:

- Em qualquer push/PR, o PDF é compilado e disponibilizado como artefato do workflow.
- Em push na branch `main`, o PDF é publicado/atualizado na release `latest`.
- Ao criar uma tag `v*` ou publicar uma release, o PDF é anexado à release correspondente.

O PDF final é publicado com o nome `MURILO_SANTIAGO_PAVILA_MIRANDA_TRABALHO_SASI_2026_2.pdf`.
