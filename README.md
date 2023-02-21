# AWS-Dynamo-DB

# Setup
# Clone the code available at https://github.com/OT-BUILDPIPER-MARKETPLACE/AWS-Dynamo-DB
# Build the docker image

git submodule init
git submodule update
docker build -t ot/tf-dynamodb-step:0.1 .

# Do local testing via image only
# Terraform Plan
docker run -it --rm -v $PWD:/src -e WORKSPACE=/src -e AWS_ACCESS_KEY_ID=<?> -e AWS_SECRET_ACCESS_KEY=<?> -e INSTRUCTION=plan ot/tf-dynamodb-step:0.1

# Terraform Apply (Default)
docker run -it --rm -v $PWD:/src -e WORKSPACE=/src -e AWS_ACCESS_KEY_ID=<?> -e AWS_SECRET_ACCESS_KEY=<?> -e INSTRUCTION=apply ot/tf-dynamodb-step:0.1
