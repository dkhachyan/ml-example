# ml-example

```
docker run -d  --rm -p8000:8000 -p8001:8001 -p8002:8002 -v ./triton-models:/models nvcr.io/nvidia/tritonserver:22.08-py3 tritonserver --model-repository=/models
```

```
curl -i -X POST  0.0.0.0:8000/v2/models/hello-world/infer  -d @input.json
```