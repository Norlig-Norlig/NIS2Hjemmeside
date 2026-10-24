# NIS2Hjemmeside

Hjemmesiden deployes automatisk til Simply.com via FTP, hver gang der pushes til `main`.

## Deployment

Workflowet i `.github/workflows/deploy.yml` uploader repoets filer til webhotellet. Kun ændrede filer uploades.
Det kræver disse secrets under **Settings > Secrets and variables > Actions**:

| Secret | Eksempel | Påkrævet |
| --- | --- | --- |
| `FTP_HOST` | `linux123.unoeuro.com` (se Simply kontrolpanel) | Ja |
| `FTP_USERNAME` | `ditdomæne.dk` | Ja |
| `FTP_PASSWORD` | FTP-adgangskoden | Ja |
| `FTP_SERVER_DIR` | `/public_html/` (skal slutte med `/`) | Nej, standard er `/public_html/` |

Deploy kan også startes manuelt under fanen **Actions**.
