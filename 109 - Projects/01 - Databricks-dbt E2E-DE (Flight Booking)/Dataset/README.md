# Sparse Checkout for Specific Folder

This guide explains how to clone only a specific folder from a large Git repository using Git sparse-checkout.

## Goal
Clone only the `Dataset` folder from the project without downloading the entire repository.

## Steps

1. Clone the repository without checking out files:
   ```bash
   git clone --filter=blob:none --no-checkout https://github.com/datarithmus/data-analytics-engineering.git
   cd data-analytics-engineering
   ```

2.  Initialize sparse-checkout:
    ```bash
    git sparse-checkout init --cone
    ```

3.  Set the target folder:
    ```bash
    git sparse-checkout set "109 - Projects/01 - Databricks-dbt E2E-DE (Flight Booking)/Dataset"
    ```

4.  Checkout the branch:
    ```bash
    git checkout main
    ```
