# ID2223-LAB2

## Description
For LAB2 i fine-tuned the [Whisper-small](https://huggingface.co/openai/whisper-small) model with the [common voice dataset](https://commonvoice.mozilla.org/sv-SE/datasets) for swedish transcription. You are able to test the model preformance through an [app](https://huggingface.co/spaces/karl-sim/ID2223-lab2) hosted on hugging-face spaces.

While the models predictive power is fine, it is nowhere near as good as it could be. Possible improvents are:
* Using a newer version of the [common voice dataset](https://commonvoice.mozilla.org/sv-SE/datasets). Containing more voice-data. Additionally, even more data such as the [NST](https://www.nb.no/sprakbanken/en/resource-catalogue/oai-nb-no-sbr-56/#corpus-info) dataset could be used.
* Due to some problems during training ... val loss keeps decreaqsing, wer increases
* Lastly we could start with the larger whisper model...

### Links to the huggingface spaces app
https://huggingface.co/spaces/karl-sim/ID2223-lab2

### Dataset
https://commonvoice.mozilla.org/sv-SE/datasets
