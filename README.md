# MLOPs_Complete_ML_Pipeline
In this project we will Understanding the ML Pipeline and working with DVC and using DVC  for experiment tracking and Data versioning by using AWS S3

# Expermients with DVC:
12> pip install dvclive
13> Add the dvclive code block (mentioned below)
14> Do "dvc exp run", it will create a new dvc.yaml(if already not there) and dvclive directory (each run will be considered as an experiment by DVC)
15> Do "dvc exp show" on terminal to see the experiments or use extension on VSCode (install dvc extension)
16> Do "dvc exp remove {exp-name}" to remove exp (optional) | "dvc exp apply {exp-name}" to reproduce prev exp
17> Change params, re-run code (produce new experiments)
18> Now git add, commit, push

# Adding a remote S3 storage to DVC:

Create IAM User (straight forward process)
Create S3(enter unique name and create)
pip install dvc[s3]
pip install awscli
>> "aws configure" run this comman on terminal
dvc remote add -d dvcstore s3://bucketname
dvc commit-push the exp outcome that you want to keep.
finally git add, commit, push.