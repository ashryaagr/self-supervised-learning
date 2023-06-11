## Escaping supervision: self-supervised visual representation learning

#### Summary
In this project, we explore two self-supervised learning techniques to train networks for visual representation extraction. The pretext tasks that we consider for self-supervision are image inpainting and global context-based similarity. For both the techniques we train a neural network in a self-supervised setting. Further, we investigate the usefulness of these techniques by evaluating the performance of the trained network on downstream tasks of classification and segmentation. For these evaluations we use datasets that have an entirely different domain to reason about the usefulness. 

### Self supervised learning tasks - Files and work

#### Inpainting
Following are the jupyter notebooks for the inpainting task
- Inpainting - Classification.ipynb
- Inpainting-VOC-OxfordIITPet.ipynb


#### global context-based similarity
Following are the jupyter notebooks for the inpainting task
- evaluate-with-contrastive.ipynb
- eval_classification_contrastive.ipynb
- data_util.ipynb


### Instructions to run

#### Installation

```bash
python3 -m venv .env
source .env/bin/activate
pip install -r requiremnts.txt

```

#### Datasets
The datasets will be downloaded from the jupyter notebooks by using the boolean flag for download. If the dataset is already present, then it uses the current dataset.

#### Inpainting
- Run the notebook: Inpainting - Classification.ipynb, which uses the SSL task to train the encoders. This downloads OxfordPet dataset.
- When we run the torch.save cell in the previous notebook, we get a ssl_model.pth file with weights.
- Run cells in Inpainting-VOC-OxfordIITPet.ipynb for the downstream task of segmentation on VOC dataset.

#### global context-based similarity
- Run the notebooks evaluate-with-contrastive.ipynb and eval_classification_contrastive.ipynb to obtain the downstream results