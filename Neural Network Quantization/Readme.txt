Title:
Neural Network Quantization

Project Description:
This project demonstrates Neural Network Quantization using PyTorch. Quantization reduces the memory and computational requirements of deep learning models by representing weights and activations with lower precision (e.g., 8-bit integers). Three quantization techniques are showcased:

Dynamic Quantization: Applies quantization during inference without requiring training data.
Static Quantization: Utilizes calibration data to perform quantization based on observed input ranges.
Quantization Aware Training (QAT): Simulates quantization during training to improve accuracy post-quantization.
These techniques help deploy efficient models on resource-constrained devices like mobile phones or edge devices.

Approach:
1. Dynamic Quantization:
The model (SimpleModel) is defined with fully connected layers and ReLU activation.
Quantization is applied dynamically to the nn.Linear layers using torch.quantization.quantize_dynamic.
Weights are quantized to qint8 (8-bit integer) at runtime, while activations remain in floating point.
2. Static Quantization:
The model is prepared with a quantization configuration (qconfig), leveraging PyTorch's FBGEMM backend.
Calibration data is fed to the prepared model to determine the activation ranges.
The model is then converted to a fully quantized version using torch.quantization.convert.
3. Quantization Aware Training (QAT):
The model is prepared with QAT configuration (get_default_qat_qconfig) and put into training mode.
Training involves simulating quantized forward passes to adjust weights for quantization-induced errors.
After training, the model is converted to a quantized version.

Metrics:
Model Size Reduction:

Measures the reduction in memory usage compared to the original model.
Inference Latency:

Evaluates the time taken for a forward pass on quantized vs. non-quantized models.
Accuracy Retention:

Assesses the accuracy of the quantized model relative to the original floating-point model.