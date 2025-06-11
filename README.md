# DeltaMap: Repositório de Dados Geoespaciais do Delta da Foz do Amazonas

	Este repositório é parte integrante do TCC de ARTUR DOS SANTOS PEREIRA NETO, BERNARDO REGIS GUIMARÃES DE OLIVEIRA, LUICK FERNANDES DE MELO, VITOR COUTO VIEIRA (Pós-graduação em Geoprocessamento UFABC) e tem como objetivo disponibilizar de forma organizada e reproduzível um conjunto de dados e ferramentas para o armazenamento, processamento, análise e visualização de informações espaciais referentes ao Delta da Foz do Amazonas.

---

🗺️ Visão Geral do Projeto

	Área de estudo: Estuário e ilhas do Delta da Foz do Amazonas, cobrindo regiões de manguezais, canais e unidades de conservação nas coordenadas aproximadas de 00°30′ N a 01°00′ S e 50°00′ W a 49°00′ W.
* Tecnologias: PostgreSQL/PostGIS para banco espacial, Python (GeoPandas, Shapely, SQLAlchemy), R, Bash, Google Colab para prototipagem em nuvem, Git/GitHub para versionamento.
* Módulos do fluxo de trabalho:

  1. Ingestão de dados: importação de shapefiles, GeoTIFFs e tabelas via scripts SQL e Python.
  2. Modelagem e armazenamento: definição de esquemas, tabelas e índices espaciais no PostGIS.
  3. Análise geoespacial: consultas SQL (interseção, área, distância), análises em Python (buffers, spatial join, estatísticas) e scripts R (opcional).
  4. Visualização: geração de mapas com Matplotlib, Folium e ferramentas GIS.
  5. Exportação de resultados: extração de tabelas para CSV, GeoJSON, exportação de mapas estáticos.
  6. Governança e colaboração: gestão de issues, pull requests e pipelines de CI/CD no GitHub.

---

## 📂 Estrutura de Pastas

```
/ (raiz)
├── README.md
├── data/                    # Dados brutos organizados por tema (shapefiles completos)
│   ├── Vegetacao/
│   ├── UCs/
│   ├── Carta_Nautica/
│   └── ...
├── scripts/                 # Ferramentas e automações
│   ├── sql/                 # Notebooks e .sql para criar schema, tabelas e carregar dados
│   ├── gitbash/             # Bash: git_interactions.sh para versionamento via terminal
│   └── python/              # python_postgis_colab.py e análises geoespaciais em Colab
├── notebooks/               # Exploração e prototipagem (Jupyter Notebooks)
```

---

⚙️ Pré-requisitos

Antes de iniciar, verifique se você possui instalado:

1. Git (versão 2.20+) e **Git Bash** (Windows)
2. Conta no GitHub (gratuita ou paga)
3. PostgreSQL com **PostGIS** (local ou servidor remoto)
4. Python 3.8+ com bibliotecas: pandas, geopandas, shapely, matplotlib, contextily, rasterio, fiona, sqlalchemy, psycopg2-binary, geoalchemy2
5. Google Colab (opcional) para executar scripts na nuvem

---

🚀 Passo a Passo de Acesso ao GitHub

1. Criar ou entrar na conta GitHub

* Acesse [https://github.com](https://github.com) e faça login ou cadastre-se.

2. Navegar até o repositório

* No menu superior, clique em **Your repositories** ou use o campo de busca para localizar **deltamap**.

3. Clonar o repositório

* Clique no botão verde **Code**, copie o URL HTTPS ou SSH.
* No Git Bash, execute:

  ```bash
  git clone <URL_copiado>
  cd deltamap
  ```

4. Explorar as branches

* Liste as branches disponíveis:

  ```bash
  git branch -a
  ```

5. Criar sua branch de trabalho

* Para implementar uma nova funcionalidade ou corrigir um bug:

  ```bash
  git checkout -b feature/minha-feature
  ```

6. Sincronizar com o repositório remoto

* Antes de começar, sempre atualize:

  ```bash
  git pull origin main
  ```

7. Fazer alterações e commitar

* Após editar arquivos, adicione e faça commit:

  ```bash
  git add <arquivos>
  git commit -m "Descrição das mudanças"
  ```

8. Enviar para o GitHub e abrir PR

* Envie sua branch:

  ```bash
  git push origin feature/minha-feature
  ```
* No GitHub, clique em **Compare & pull request**, descreva as alterações e submeta para revisão.


---

📜 Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

---

*Desenvolvido por ARTUR DOS SANTOS PEREIRA NETO, BERNARDO REGIS GUIMARÃES DE OLIVEIRA, LUICK FERNANDES DE MELO, VITOR COUTO VIEIRA como parte do Trabalho de Conclusão de Curso em Geoprocessamento.*
