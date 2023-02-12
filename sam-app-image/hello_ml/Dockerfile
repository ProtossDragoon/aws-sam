FROM public.ecr.aws/lambda/python:3.8-arm64

COPY requirements.txt ./

RUN python3.8 -m pip install -r requirements.txt --no-cache-dir

COPY mlp-model/ mlp-model/

COPY app.py auto-mpg.csv myopslib.py ./

# Command can be overwritten by providing a different command in the template directly.
CMD ["app.lambda_handler"]
