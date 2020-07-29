# Epidemiology Example

This example explores the linelistrecord Type in the Covid-19 Datalake. Symptom records are combined to build a profile of the most prevalent symptoms of Covid-19. A similar example is given at the end of the python startup notebook on C3.ai's public Datalake documentation here: https://github.com/c3-e/c3aidatalake-notebooks/raw/master/c3aidatalake-notebooks-python.zip

## Python Implementation

The python implementation is in the `python` directory. This directory contains a useful conda environment definition file `env.yaml`. Create a conda environment using `conda env create -f env.yaml -p <path_to_prefix>` or `conda env create -f env.yaml -n <environment_name>`. Then launch juptyer with `jupyter notebook` and start the notebook [`EpidemiologyExample.ipynb`](./python/EpidemiologyExample.ipynb).

Once the notebook is started, you can run the notebook cells which implement the example!

## C3 Implementation

The C3 implementation of this example is in the directory `c3-python-connector`. Make sure you have access to a C3 tag which has the Datalake package provisioned either directly, or as a dependency of your current package. To ensure your python environment has everything needed, we recommend provisioning a conda environment with

```
conda env create -f ./env.yaml -p ./venv
```

After which you can launch jupyter notebook, and open the notebook `casesExample.ipynb`.

When running the jupyter notebook, there's a cell at the top meant to connect to a running C3 tag. If you're running python/jupyter 'remotely' that is not through C3's system, you will need to replace the `<vanity_url>`, `<tenant>`, and `<tag>` in the cell negotiating the connection to C3. It should look like this:

```
c3 = get_c3('<vanity_url>', '<tenant>', '<tag>')
```
