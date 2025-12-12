# RaviSomaTools — Bulk Gene ID Resolver

This is a simple, zero-maintenance browser tool that resolves gene identifiers (UniProt AC, Ensembl Gene ID, NCBI Entrez ID) for many genes at once using live API calls to UniProt, Ensembl and NCBI.

## Features
- Paste a list of gene symbols (one per line) or upload a CSV with a `Gene` column.
- Bulk lookup (100+ genes supported).
- Live progress bar and per-gene success/failure status.
- Local cache (browser localStorage) to avoid repeated lookups.
- Throttling + retry/backoff to reduce API rate limit issues.
- Export results as CSV or XLSX (Excel).
- Default species: **Rattus norvegicus** (changeable).

## How to use
1. Open the site: `https://<your-username>.github.io/RaviSomaTools/`
2. Paste gene symbols or upload a CSV.
3. Choose species (default: Rattus norvegicus).
4. Click **Start Lookup**.
5. When finished, download CSV or XLSX.

## Notes & Tips
- For extremely large lists (>500 genes), run in batches of 200 to be safe.
- The tool caches results locally — to force fresh queries, click **Clear cache**.
- This tool runs entirely in the browser; no server or account is required.
- If you need automated large-scale retrieval (thousands of genes), consider using server-side scripts with appropriate API keys.

## Development
- Single-file HTML + JavaScript app. Uses UniProt REST, Ensembl REST and NCBI Datasets suggestions API.
- Uses SheetJS (CDN) to export XLSX.

## License
MIT
