# MLOpsDagsHubDemo
Step 1:
    Create a Git repository 
    Create DagsHub repository: https://dagshub.com

 Step 2:
    install DVC
    configure dvc:
        dvc remote add origin https://dagshub.com/borahparinita123/MLOpsDagshub.dvc
        dvc remote modify origin --local auth basic
        dvc remote modify origin --local user borahparinita123
        dvc remote modify origin --local password $DAGSHUB_TOKEN

        dvc pull -r origin
        dvc add data/raw
        git add data/.gitignore data/raw.dvc
        dvc config core.autostage true
        dvc push -r origin 