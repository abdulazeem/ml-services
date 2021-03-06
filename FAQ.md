# FAQ
## Common Lab Problems & Errors
| Section | Question | Answer |
|---------|----------|--------|
|     6.9 | I can't find the `outputs` folder | The files are generated in the folder that contains the opened `.ipynb` jupyter file. Most likely, they will be at `udacity-intro-to-ml-labs/aml-visual-interface/lab-19/notebook/outputs` [[view post](https://microsoftmlchallenge.slack.com/archives/C016D8H6BJR/p1595699977334800?thread_ts=1595699834.334500&cid=C016D8H6BJR)] |
|    6.13 | plotted graph has lines instead of dots | you can manually change it to lines using the menu, it seems like everyone has lines, don't worry. [[view post](https://microsoftmlchallenge.slack.com/archives/C016D8H6BJR/p1595813904409300)] |
|    6.18 | error `Invalid graph: You have invalid dataset(s)` when trying to create a real-time inference pipeline | click the button to the right of the deploy button (three dots) and choose cloning. Once you clone, try again and the issue should be resolved. [[view post](https://microsoftmlchallenge.slack.com/archives/C016D8H6BJR/p1595857522439400?thread_ts=1595857465.438700&cid=C016D8H6BJR)] | 
|    6.18 | error `You don't have a compute target for deployment yet` / no Azure Kubernetes Service Cluster found | create a new compute target (a 1- or 3-node AKS cluster in centralus) by going to compute, create it, wait for it to be ready and continue with cluster selection [[view post 1](https://microsoftmlchallenge.slack.com/archives/C016D8H6BJR/p1596041393041800?thread_ts=1596039964.038200&cid=C016D8H6BJR), [view post 2](https://microsoftmlchallenge.slack.com/archives/C016D8H6BJR/p1596089882058500?thread_ts=1596067059.055000&cid=C016D8H6BJR)] | 

## Technical Questions

| Section | Question | Answer |
|---------|----------|--------|
|     6.9 | inside the code of the notebook there is the following code: ```run = experiment.start_logging(); run.log(“alpha_value”, alpha)```. From what i understand that opens a log files and logs in there the information we ask it to log. is that right ? If that is right did anyone figure out where we can check this log file after we execute the notebook ? | The name logs is a bit misleading, but it's a special type of log on the experiment object. Those values are available as "Metrics" under the given experiment. [[view post](https://microsoftmlchallenge.slack.com/archives/C016D8H6BJR/p1595102336147800?thread_ts=1595100329.146000&cid=C016D8H6BJR)] |
|     6.9 | When opening the output file, i see "Error! [filename] is not UTF-8 encoded. Saving disabled. See Console for more details." | In this lab we are saving the models for every value of alpha as pkl (Python pickle) files. The pkl files cannot be "read" into a browser by clicking on them. The pkl files are written using `joblib.dump` and in principle should be readable using `joblib.load` or `pickle.load`. However, both ways: `python -c "from sklearn.externals import joblib; joblib.load('model_alpha_0.1.pkl')"` and `python -c "import pickle; pickle.load(open('model_alpha_0.1.pkl'), 'rb'))"` are failing with `ValueError: unregistered extension code 40` and a workaround is currently unknown. [[view post](https://microsoftmlchallenge.slack.com/archives/C0174DS4R08/p1595873241063300?thread_ts=1595770954.402500&cid=C0174DS4R08)] |
|     6.9 | how to commit to a github repository from a jupyter instance? | Assuming you have write access to the repository, from a terminal, push to the repository over https. Use the following commands: `git clone https://github.com/mygithubusername/udacity-intro-to-ml-labs`, `cd udacity-intro-to-ml-labs`, `git config --global user.name "My Name"` , `git config --global user.email myemail@example.com`, `git add .`, `git commit -m"Added changes ..."`, `git push`. [[git tutorial](https://www.youtube.com/channel/UCshmCws1MijkZLMkPmOmzbQ)] 


## Understanding Questions
| Section | Question | Answer |
|---------|----------|--------|
|     6.5 | What's the diference between Real-time Inferencing, Batch Inferencing and Lambda architecture? | lamba is the architecture where it helps you to process 2 types of requests. Real time data is usually a single input request where the priority is to get results  asap within millsecs. Time is the constraint. Like avoid fraud attacks right there itself. Batch inferencing allows delays to process request and drive results. It's more to be used if you want to analyze batch of new input data and make some changes to your existing model architecture. [[view post](https://microsoftmlchallenge.slack.com/archives/C016D8H6BJR/p1595868804463200?thread_ts=1595868551.462000&cid=C016D8H6BJR)]
|     6.4 | What's the difference between compute resources, compute instances and compute clusters? | a compute resource refers to a compute object that can be used in the Azure machine learning environment. That resource can either be a compute instance or a compute cluster.   A compute cluster is a cluster of computers created using single/multiple compute nodes [[view post 1 (overview)](https://microsoftmlchallenge.slack.com/archives/C016D8H6BJR/p1595832933429000?thread_ts=1595830898.428800&cid=C016D8H6BJR), [view post 2 (detailed)](https://microsoftmlchallenge.slack.com/archives/C0171MB80FP/p1595918534474500)] |

## Errors already fixed by Udacity
| Section | Question | Answer |
|---------|----------|--------|
|    6.18 | deploy error: "Failed on step CreateServiceFromModels" | bug has been fixed [[view post](https://microsoftmlchallenge.slack.com/archives/C016D8H6BJR/p1595356166207200?thread_ts=1594546510.490300&cid=C016D8H6BJR)]
