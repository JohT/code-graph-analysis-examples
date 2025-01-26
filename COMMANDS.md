# Code Graph Analysis Pipeline - Commands

<!-- TOC -->

- [Generate Markdown References](#generate-markdown-references)
    - [Generate CSV Cypher Query Results Report Reference](#generate-csv-cypher-query-results-report-reference)
    - [Generate Jupyter Notebook Report Reference](#generate-jupyter-notebook-report-reference)
    - [Generate Image Reference](#generate-image-reference)

<!-- /TOC -->

## Generate Markdown References

### Generate CSV Cypher Query Results Report Reference

Change into the [analysis-results](./analysis-results/) directory e.g. with `cd analysis-results` and then execute the script [generateCsvReportReference.sh](./documentation/analysis-reports-reference/generateCsvReportReference.sh) with the following command:

👉**Note:** This script is automatically triggered in the pipeline [internal-report-reference-documentation.yml](.github/workflows/internal-report-reference-documentation.yml) and doesn't need to be executed manually normally.

```script
./../documentation/analysis-reports-reference/generateCsvReportReference.sh
```

### Generate Jupyter Notebook Report Reference

Change into the [analysis-results](./analysis-results/) directory e.g. with `cd analysis-results` and then execute the script [generateJupyterReportReference.sh](./documentation/analysis-reports-reference/generateJupyterReportReference.sh) with the following command:

👉**Note:** This script is automatically triggered in the pipeline [internal-report-reference-documentation.yml](.github/workflows/internal-report-reference-documentation.yml) and doesn't need to be executed manually normally.

```script
./../documentation/analysis-reports-reference/generateJupyterReportReference.sh
```

### Generate Image Reference

Change into the [analysis-results](./analysis-results/) directory e.g. with `cd analysis-results` and then execute the script [generateImageReference.sh](./documentation/analysis-reports-reference/generateImageReference.sh) with the following command:

👉**Note:** This script is automatically triggered in the pipeline [internal-report-reference-documentation.yml](.github/workflows/internal-report-reference-documentation.yml) and doesn't need to be executed manually normally.

```script
./../documentation/analysis-reports-reference/generateImageReference.sh
```
