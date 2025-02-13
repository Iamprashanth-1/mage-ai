# Run selected models (and optionally exclude others)

![](https://raw.githubusercontent.com/mage-ai/assets/main/dbt/add-dbt-models.gif)

1. Under the data loader block you just added, click the button <b>`DBT model`</b>,
then click the option `All models`.
1. In the `DBT project name` input field, enter the name of the DBT project that
contains the models you want to build and run (e.g. `demo`).
1. In the `DBT profile target` input field, enter the name of the DBT connection profile
(e.g. `dev`) that you want to use when running the selected DBT models.
1. In the text area of the code block, write the models you want to select or exclude
using DBT’s `--select` and `--exclude` flags and syntax.

    For more information on the `--select` and `--exclude` syntax,
    [read DBT’s documentation](https://docs.getdbt.com/reference/node-selection/syntax#examples).
    For example:

    ```yaml
    $ dbt run --select my_dbt_project_name   # runs all models in your project
    $ dbt run --select my_dbt_model          # runs a specific model
    $ dbt run --select path.to.my.models     # runs all models in a specific directory
    $ dbt run --select my_package.some_model # run a specific model in a specific package
    $ dbt run --select tag:nightly           # run models with the "nightly" tag
    $ dbt run --select path/to/models        # run models contained in path/to/models
    $ dbt run --select path/to/my_model.sql  # run a specific model by its path
    ```

    ```yaml
    $ dbt run --exclude my_dbt_project_name
    $ dbt run --exclude my_dbt_model
    $ dbt run --exclude path.to.my.models
    $ dbt run --exclude my_package.some_model
    $ dbt run --exclude tag:nightly
    $ dbt run --exclude path/to/models
    $ dbt run --exclude path/to/my_model.sql
    ```
