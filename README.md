# Ego4d_Compositional
This repo will help you to construct your experiments about Compositional action recognition using Ego4d dataset. Not their original Benchmark.
By using **Ego4d's Forecasting benchmark** and **Ego4d's OSCC(object state change classification)**, I construct task ___"Compositional Action recognition"___ where Video model predicts action as a pair of (verb, noun) 
Each sample is extracted from Ego4d's lta, sta. All action clip's duration is 8 seconds. it is annotated original annotation

# Notice & Terminology
* The test subset is unannotated, it is not included in this repository
* **One clip**: A clip used original benchmark (duration: variable about a few minutes)
* **Atome action clip**: Extracted from a clip, its duration is 8s. it is marked original [annotations](Annotations/fho_lta_train.json) 
****
# Related Repository
## Reference
>Paper
>> Ego4D_Around_the_World_in_3000_Hours_of_Egocentric_Video: [PDF link](https://openaccess.thecvf.com/content/CVPR2022/papers/Grauman_Ego4D_Around_the_World_in_3000_Hours_of_Egocentric_Video_CVPR_2022_paper.pdf)

>facebookresearch
>> Github: [facebookresearch/Ego4d](https://github.com/facebookresearch/Ego4d.git)

>EGO4D
>>Github: [EGO4D/forecasting](https://github.com/EGO4D/forecasting)

>Ego4d Official Website 
>>[start-here](https://ego4d-data.org/docs/start-here/)
## Related Task

>Epickitchens100 Compositional recognition
>>Papers with code: [action-recognition-on-epic-kitchens-100](https://paperswithcode.com/sota/action-recognition-on-epic-kitchens-100)

<br><br>

# Contents
## 1. Data ditribution
- [Data Distribution REAMDE](./Data_analysis_notebook/README.md)
- Analysis each benchmark's Data ditribution such as number of atom actions
    The code is available as notebooks and offer visualization graph
1. Number of atom actions
2. Distribution of overlapping between each atom action because one clip have many overlapped atom actions to predict long term action.
   

****
<br>

## 2. Trimming
- [Trimming](./Trimming/README.md)
- Resize and Clipping
- It gives you the good data compression method. 
- The data can be rescaled like 256 * 256 spatial resoultion, and also frames can be reduced properly By using ffmepeg.
  
    We have to detach atom action clips from each benchmark, So Trimming is preceded before making annotations
****
<br>

## 3. Custom Annotations
- [Annotations](./Custom_Annotations/README.md)
- Annotations for compositional recognition. Each Atom action's verb, noun, file_id, timestamp..etc
- You can make you own annotations by using my notebook.
****
<br>
