# Unpickler
> Small library to help with pickle issues


## Install

`pip install unpickler`

## How to use

Ever run into a situation (perhaps running PyTorch inference on a server) where you can't import a module despite it being defined in your `lib`? This library fixes that through a custom unpickler:
> for our example we will use fastai's `load_learner`

```
#slow
from unpickler.core import UnpicklerModule
from fastai.learner import load_learner

load_learner('export.pkl', pickle_module=UnpicklerModule)
```
