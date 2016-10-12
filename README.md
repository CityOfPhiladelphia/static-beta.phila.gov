1. Clone the [site-snapshot](https://github.com/CityOfPhiladelphia/site-snapshot) tool to make a snapshot of beta.phila.gov

    ```bash
    git clone git@github.com:CityOfPhiladelphia/site-snapshot.git
    cd site-snapshot
    git clone git@github.com:CityOfPhiladelphia/static-beta.phila.gov.git _site
    ```

2. Run the snapshot tool

    ```bash
    scripts/snapshot.sh beta.phila.gov
    ```

3. Go into the `_site` folder and test the site

    ```bash
    cd _site
    python -m SimpleHTTPServer
    ```

4. Restore the README, commit the entire folder and push

    ```bash
    git checkout README.md
    git add .
    git commit -m "Site snapshot from $(date)"
    git push
    ```
