# cookiecutter-templete-docker-asteristics
In this repository, we can find template for lauch asteristics apps using cookiecutter properties

# cookiecutter-templete-docker-asteristics

This project helps asteristics team to create the that every Elixir API needs
at the beginning of the development process.

By using this template you can generate a project directory with the follow:

* **README.md**: Custom readme with usage instructions
* **.gitignore**: Custom ignores for elixir development
* **.github/workflows/deploy-production.yml** Github actions workflow for asteristics continuos integration process
* **Dockerfile**: Docker image instructions to release astristics projects
* **.dockerignore**: Custom docker ignore rules for asteristics projects

## Install

You need to install `cookiecutter` on your local with another testing tools:

``` shell
$ brew install cookiecutter
```

Additional you can use `yamllint` to validate that the generated manifests are valid.

``` shell
$ brew install yamllint
```

## Usage

Generate a template:

``` shell
$ cookiecutter git@github.com:resuelve/cookiecutter-templete-docker-asteristics.git
```

This command will ask you for your project attributes, and after that
creates a directory with your project's name, for example:

``` shell
$ find example-api
example-api
example-api/Dockerfile
example-api/.editorconfig
example-api/README.md
example-api/.dockerignore
example-api/.gitignore
example-api/.github
example-api/.github/workflows
example-api/.github/workflows/deploy-production.yml
example-api/.github/PULL_REQUEST_TEMPLATE.md
```

### Test resulting yaml

You can use `yamllint` to lint your resulting Github actions workflow, for example:

```shell
$ yamllint example-api/.github/workflows/deploy-production.yml
```

Remember to test locally and fix any error reported by the linter before commit.

### Usage for CD workflows

If you wan to build this inside your CI/CD process using Github actions, you can
run cookiecutter without user intervention:

``` shell
$ cd data/vcs
$ cookiecutter git@github.com/resuelve/cookiecutter-templete-docker-asteristics.git \
  --no-input \
  --overwrite-if-exists \
  project_name=example-api
```
### Contributions

I you find this useful please buy me a coffee :P, I'm just kidding, just try to use it and give feedback.

### References

Please read the follow references for more details:

* [Cookicutter home](https://github.com/cookiecutter/cookiecutter)
* [Cookicutter documentation](https://cookiecutter.readthedocs.io/en/stable/)
