# Data Version Control Example

Install dvc with s3 support as `pip install dvc[s3]`

**Note**: dvc does not replace git, it works along with git

Steps: 
1. Initialize dvc repository with `dvc init`
2. Stage data files with `dvc add data/data.csv`
3. Ignore the actual data file from git with `git add data/data.csv.dvc data/.gitignore`
4. Connect S3 remote `dvc remote add -d <remote-name> s3://<bucket-name>` # Remote name can be anything, just like commit messages
5. Push the data file with `dvc push`
