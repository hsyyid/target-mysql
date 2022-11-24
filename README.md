# target-oracle

`target-oracle` is a Singer target for Oracle.

Build with the [Meltano Target SDK](https://sdk.meltano.com).

<!--

Developer TODO: Update the below as needed to correctly describe the install procedure. For instance, if you do not have a PyPi repo, or if you want users to directly install from your git repo, you can modify this step as appropriate.

## Installation

Install from PyPi:

```bash
pipx install target-oracle
```

Install from GitHub:

```bash
pipx install git+https://github.com/ORG_NAME/target-oracle.git@main
```

-->

## Configuration

### Accepted Config Options

<!--
Developer TODO: Provide a list of config options accepted by the target.

This section can be created by copy-pasting the CLI output from:

```
target-oracle --about --format=markdown
```
-->

A full list of supported settings and capabilities for this
target is available by running:

```bash
target-oracle --about
```

### Configure using environment variables

This Singer target will automatically import any environment variables within the working directory's
`.env` if the `--config=ENV` is provided, such that config values will be considered if a matching
environment variable is set either in the terminal context or in the `.env` file.

### Source Authentication and Authorization

<!--
Developer TODO: If your target requires special access on the destination system, or any special authentication requirements, provide those here.
-->

## Usage

You can easily run `target-oracle` by itself or in a pipeline using [Meltano](https://meltano.com/).

### Executing the Target Directly

```bash
target-oracle --version
target-oracle --help
# Test using the "Carbon Intensity" sample:
tap-carbon-intensity | target-oracle --config /path/to/target-oracle-config.json
```

## Developer Resources

Follow these instructions to contribute to this project.

### Initialize your Development Environment

```bash
pipx install poetry
poetry install
```

### Create and Run Tests

Create tests within the `target_oracle/tests` subfolder and
  then run:

```bash
poetry run pytest
```

You can also test the `target-oracle` CLI interface directly using `poetry run`:

```bash
poetry run target-oracle --help
```

### Testing with [Meltano](https://meltano.com/)

_**Note:** This target will work in any Singer environment and does not require Meltano.
Examples here are for convenience and to streamline end-to-end orchestration scenarios._

<!--
Developer TODO:
Your project comes with a custom `meltano.yml` project file already created. Open the `meltano.yml` and follow any "TODO" items listed in
the file.
-->

Next, install Meltano (if you haven't already) and any needed plugins:

```bash
# Install meltano
pipx install meltano
# Initialize meltano within this directory
cd target-oracle
meltano install
```

Now you can test and orchestrate using Meltano:

```bash
# Test invocation:
meltano invoke target-oracle --version
# OR run a test `elt` pipeline with the Carbon Intensity sample tap:
meltano elt tap-carbon-intensity target-oracle
```

### SDK Dev Guide

See the [dev guide](https://sdk.meltano.com/en/latest/dev_guide.html) for more instructions on how to use the Meltano Singer SDK to
develop your own Singer taps and targets.
