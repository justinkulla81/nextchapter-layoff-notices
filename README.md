# U.S. layoff notices (WARN Act), updated weekly

Layoff notices filed under the WARN Act and published by U.S. state labor departments, collected by [NextChapter](https://launchyournextchapter.com/layoffs) into one file.

- **File:** [`data/layoffs.csv`](data/layoffs.csv), one row per filing, refreshed every week from https://launchyournextchapter.com/data/layoffs.csv
- **License:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Free to use and share, including commercially, with a link back.
- **Live JSON API:** https://launchyournextchapter.com/api/public/layoffs (description: https://launchyournextchapter.com/api/public/openapi.json)
- **Agents:** a free MCP server at https://launchyournextchapter.com/api/mcp has a `recent_layoff_notices` tool.

## Columns

| Column | Meaning |
|---|---|
| `state` | Two-letter state code of the state that published the notice |
| `employer` | Employer as the state published it |
| `notice_date` | Date the notice was filed. Empty when the state publishes only the effective date |
| `effective_date` | Date the layoffs take effect, when given |
| `workers` | Number of workers the notice names. Empty when the notice does not give one |
| `layoff_type` | The state's wording, such as closure or layoff |
| `place` | City or county, whichever the state gives |
| `source_url` | The state's own record |
| `nextchapter_url` | The employer's page on NextChapter |

## What the data does and does not say

A WARN notice is the advance notice larger employers give before a plant closing or mass layoff. It states the number of workers and the dates the employer reported. It does not say why, and it does not cover every layoff: smaller layoffs and states that publish no list are not in it. Counts are of filings, so one layoff can appear as several rows when an employer files for several sites.

## How to cite

NextChapter layoff tracker, WARN Act notices collected from state labor departments. https://launchyournextchapter.com/layoffs

A machine-readable citation is in [`CITATION.cff`](CITATION.cff), and the dataset description is in [`datapackage.json`](datapackage.json).

## Updates

A weekly GitHub Action downloads the current file and commits it when it changed. The history of the file shows how the record grew.
