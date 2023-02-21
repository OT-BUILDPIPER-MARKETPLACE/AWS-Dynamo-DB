
# AWS-Dynamo-DB

Setting up Dynamo-DB using opstree tf module



## Setup
* Clone the code available at [AWS-Dynamo-DB](https://github.com/OT-BUILDPIPER-MARKETPLACE/AWS-Dynamo-DB)

* Build the docker image

```bash
git submodule init
git submodule update
docker build -t ot/tf-dynamodb-step:0.1 .
```
* Do local testing via image only

Terraform Plan
```bash
docker run -it --rm -v $PWD:/src -e WORKSPACE=/src -e AWS_ACCESS_KEY_ID=<?> -e AWS_SECRET_ACCESS_KEY=<?> -e INSTRUCTION=plan ot/tf-dynamodb-step:0.1
```
Terrafom Apply (Default)
```bash
docker run -it --rm -v $PWD:/src -e WORKSPACE=/src -e AWS_ACCESS_KEY_ID=<?> -e AWS_SECRET_ACCESS_KEY=<?> -e INSTRUCTION=apply ot/tf-dynamodb-step:0.1
```