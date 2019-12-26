FROM python:3.8.1

# Install pipenv python package and virtual env manager
RUN pip install pipenv

# Add project files to the image
WORKDIR /workspace
COPY . /workspace

# Install dependencies
RUN pipenv install --deploy --ignore-pipfile --dev

EXPOSE 8888

CMD ["pipenv", "run", "jupyter", "lab", "--ip='*'", "--port=8888", "--no-browser", "--allow-root"]
