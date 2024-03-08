# Research Data Management

This repo provides the documentation for the research data management processes at the [Quantitative Biology Center](https://ror.org/00v34f693) [<img src="https://raw.githubusercontent.com/ror-community/ror-logos/main/ror-icon-rgb.svg" height=18>](https://ror.org/00v34f693), [University of Tübingen](https://ror.org/03a1kwz48) [Quantitative Biology Center](https://ror.org/00v34f693) [<img src="https://raw.githubusercontent.com/ror-community/ror-logos/main/ror-icon-rgb.svg" height=18>](https://ror.org/00v34f693).

[![Built with Material for MkDocs](https://img.shields.io/badge/Material_for_MkDocs-526CFE?style=for-the-badge&logo=MaterialForMkDocs&logoColor=white)](https://squidfunk.github.io/mkdocs-material/)

> #### Latest documentation
>
> [qbicsoftware.github.io/research-data-management](https://qbicsoftware.github.io/research-data-management)
> 

## Local Development

The documentation is written in pure Markdown, rendered and deployed with [MkDocs](https://www.mkdocs.org/) and [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/). Both can be installed with the Python tool [pip](https://pypi.org/project/pip/):

```bash
pip install mkdocs mkdocs-material
```

If you want to see the live preview, run:

```bash
mkdocs serve
```

In the default configuration, you can see a live preview following the URL displayed in the console log, e.g. http://127.0.0.1:8000:

```bash
mkdocs serve                                   
INFO    -  Building documentation...
INFO    -  Cleaning site directory
INFO    -  Documentation built in 0.24 seconds
INFO    -  [08:41:47] Watching paths for changes: 'docs', 'mkdocs.yml'
INFO    -  [08:41:47] Serving on http://127.0.0.1:8000/

```

## Documentation

The documentation source files themselves are located in this repository's `./docs` folder. You can use simple [Markdown](https://www.markdownguide.org/) syntax for providing more content.

## Deployment

The deployment of the live side is implemented with Github actions, once a commit is done to the `main` branch.

The live site of the build documentation can be then found on https://qbicsoftware.github.io/research-data-management. 

## License

Any **repository code** and configuration is licensed under the [MIT-license](https://mit-license.org/).

The **creative work** of the documentation found in the `./docs` directory of this repository is licensed under [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/) <img src="https://mirrors.creativecommons.org/presskit/buttons/88x31/png/by.png" height=20px>.

Attribution to *QBiC, University of Tübingen*
