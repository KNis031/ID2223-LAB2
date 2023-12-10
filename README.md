# ID2223-LAB2

## Description
For LAB2 i fine-tuned the [Whisper-small](https://huggingface.co/openai/whisper-small) model with the [common voice dataset](https://commonvoice.mozilla.org/sv-SE/datasets) (~51 hours) for swedish speech-to-text transcription. You are able to test the model preformance by either speaking into a microphone or uploading a file through an [app](https://huggingface.co/spaces/karl-sim/ID2223-lab2) hosted on hugging-face spaces.

While the model's predictive power is arguably OK (Best WER 33%), it is nowhere near as good as it could be. Possible improvents include:
* **Data centric**: Using a newer version of the [common voice dataset](https://commonvoice.mozilla.org/sv-SE/datasets), containing more voice-data would likely improve results. Additional datasets such as the [NST](https://www.nb.no/sprakbanken/en/resource-catalogue/oai-nb-no-sbr-56/#corpus-info) dataset could also be used.
* **Model centric**: Experimenting with batch size and other hyperparams could improve results. I was training the model through [colab](https://colab.google/), utilizing Nvidia T4 and later V100 CPUs. As colab limits your resources, and would sometimes disconnect, I opted for a smaller batch size and less training steps to reduce the training time. The model likely suffered from this. From the evaluation logs it would seem as the evaluation loss stabilized, but the WER started to increase after just a few initial steps, possibly sugessting overfitting(?). Another possibility is that the evaluation loss would start to decrease again given more time.
* **Model centric**: Another possible improvement could be to start with a larger whisper model such as whisper-large (1550 M parameters).
* **Task centric** Lastly, we could specify the task of the problem even more. Making it a domain specific task to say, medicine or biology speech recognition, we could for instance weigh sentences (data points) based on their relevance for that domain. Changing the task is a major step though, and there are likely more that should/could be changed in that case.

### Links to the huggingface spaces app
https://huggingface.co/spaces/karl-sim/ID2223-lab2

### Blog post explaining pipeline
https://huggingface.co/blog/fine-tune-whisper

### Dataset
https://commonvoice.mozilla.org/sv-SE/datasets
