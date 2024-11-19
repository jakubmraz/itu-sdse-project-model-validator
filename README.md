# ITU BDS SDSE'24 - Project - Model Validator Action

## What is this?

GitHub Action for validating trained model artifact.

Check the [project description](https://github.com/lasselundstenjensen/itu-sdse-project) for more information.


## How to use?

### 1. Upload the model to store it as an artifact in the workflow

```yaml
- name: Upload Model Artifact
  uses: actions/upload-artifact@v4.4.0
  with:
    name: model
    path: <your path>/<model>.pkl
```

The artifact should look like this when uploaded successfully (size may differ).

<img width="1373" alt="image" src="https://github.com/user-attachments/assets/51ee28e2-331f-4f84-8ba4-b7f313b92b5c">


### 2. Run this inference test action

Insert the following code into your GitHub workflow after the model artifact has been uploaded in order to run a test inference on it. This will validate that the model was trained correctly.

```yaml
- name: Run Model Inference Test Action
  uses: lasselundstenjensen/itu-sdse-project-model-validator@main
```
