# scrape-runner

Lend your free GitHub Actions minutes to [scrape-hub](https://scrape.s1d.me). This template gives you a repository with one
workflow. The hub starts it when there is scraping to do; the runs fetch public tender data and report it to the hub.

## Join in four steps

1. **Make your copy.** At the top of this page click **Use this template** -> **Create a new repository**. Owner: you. Name:
   `scrape-runner`. Choose **Public** (public repositories get free Actions minutes; private ones use up your quota).
2. **Allow Actions.** In your new repository open **Settings -> Actions -> General**, choose **Allow all actions and reusable
   workflows**, and save.
3. **Create a token** at GitHub **Settings -> Developer settings -> Personal access tokens -> Fine-grained tokens -> Generate
   new token**:
   - Resource owner: **you**
   - Repository access: **Only select repositories** -> `scrape-runner`
   - Permissions -> Repository permissions: **Actions: Read and write** (Metadata: Read-only is added by itself)
   - Expiration: whatever you like, up to 1 year

   Copy the token now; GitHub shows it only once.
4. **Tell the hub.** On https://scrape.s1d.me open **Runners** and add your GitHub username, the repository name
   (`scrape-runner`) and the token.

## What happens next

Nothing you need to do. The hub starts runs in your repository when it has work (you will see them under the **Actions**
tab) and decides how many runners to use. You never press anything.

The workflow file here only points at `s1d-labs/scrapers`, where the scraper code lives, so code updates arrive by themselves.
Do not edit `.github/workflows/run.yml`.

The token can only start and read Actions runs in this one repository; it cannot read your code or touch anything else. To
leave, delete the token (or the repository), or remove yourself on the Runners page.
