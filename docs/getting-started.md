# Getting started

- Populate `.env` with any necessary secrets
- Populate `jupyter/requirements.in` with any necessary requirements
- Run `docker-compose up --build jupyter`
- Wait for the service to build, and then click the link beginning `http://127.0.0.1:8888/lab?token=`
- In the browser, navigate to the `notebooks/` directory and create a new notebook using the default Python 3 kernel. Your requirements will have been installed during the build.
- Save any data artefacts created during the course of your analysis to `../data`. They will be persisted in the `jupyter/data/` directory.
- If anything about your system config changes (environment variables, requirements, etc) you'll need to shut down the container (`docker-compose down`) and rebuild it using the same command as you used to start it.
