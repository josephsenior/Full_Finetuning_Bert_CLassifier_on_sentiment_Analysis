Fine-tuning BERT for Text Classification
This notebook walks through the full process of fine-tuning a pretrained BERT model for text classification using the Hugging Face transformers library.
Steps Covered :

Dataset Loading
Load a dataset (e.g., from Hugging Face Datasets or CSV/JSON).
Split into training and test sets (if not already split).

Tokenization
Use AutoTokenizer to tokenize the text for BERT.
Pad and truncate sequences to the desired length.

Model Setup
Load a pretrained bert-base-uncased (or similar) model using AutoModelForSequenceClassification.
Set the number of output labels for classification.

Training Arguments
Define hyperparameters like learning rate, batch size, epochs, weight decay, logging steps, etc.

Trainer API
Use the Hugging Face Trainer class to:
Train the model.
Log metrics like loss and accuracy.
Save the model checkpoints.

Evaluation
Use standard metrics like accuracy, precision, recall, and F1.
Evaluate on the test dataset using Trainer.evaluate().

Model Saving
Save the fine-tuned model and tokenizer locally for future inference.

Inference
Load the model and tokenizer.
Use the Accelerate library to enable mixed precision (fp16) inference for faster performance.
Perform inference on new text samples with confidence scores.


ALL WHILE MAKING IT SIMPLE FOR EVERYONE TO UNDERSTAND AND MODIFY (
NB:THERE ARE MORE ADVANCED AND OPTIMIZED WAYS FOR TRAINING SUCH AS LORA AND QLORA FOR BETTER GPU USAGE AND FASTER TRAINING 
AND INFERENCE WITH ONNX FORMAT OR TENSOR RT BUT THAT IS NOT NECESSARY FOR THIS PROJECT BECAUSE THE MODEL ISN'T REALLY 
THAT LARGE AND THE INFERENCE TIME IS ALREADY GOOD (12-15ms) !
