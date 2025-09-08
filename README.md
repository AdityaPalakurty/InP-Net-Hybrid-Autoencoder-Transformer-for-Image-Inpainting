# InP-Net-Hybrid-Autoencoder-Transformer-for-Image-Inpainting-



📌 Overview

InP-Net is a hybrid deep learning framework for image inpainting, designed to recover missing or corrupted regions of an image with high fidelity and realism. The model integrates the global contextual reasoning power of Vision Transformers (ViTs) with the spatial reconstruction capabilities of Autoencoders, striking a balance between semantic understanding and texture-level detail.

Unlike traditional inpainting methods, InP-Net introduces flexible masking strategies, skip connections, and a lightweight decoder, enabling efficient and high-quality reconstruction across a wide range of occlusion patterns.

✨ Key Features

Hybrid Architecture: Combines Autoencoders for local detail preservation with Transformers for global semantic understanding.

Flexible Masking: Supports both random and structured masking (center, corners, edges) with ratios configurable from 0% to 90%.

Dynamic Inference: At inference, masking ratio can be set to 0%, enabling direct auto-reconstruction for restoration tasks.

Skip Connections: Improves gradient flow and texture recovery by passing intermediate transformer features to the decoder.

Lightweight Decoder: Shallow CNN-based decoder reduces computation while maintaining reconstruction fidelity.

Self-Supervised Learning: Trains without labeled data, leveraging large-scale unlabeled datasets like Places365.

Loss Functions: Supports both MSE reconstruction loss and adversarial (GAN) loss for sharper, realistic outputs.

🏗️ Architecture

Patch Embedding – Split images into tokens and embed with positional encodings.

Transformer Encoder – Captures long-range semantic dependencies.

Skip Connections – Fuse multi-level encoder features into the decoding stage.

Lightweight Decoder – Performs upsampling and refinement using transposed convolutions.

Flexible Masking – Handles random and structured occlusions during training & inference.

📊 Results

Outperforms baseline Masked Autoencoder (MAE) in both reconstruction quality and visual realism.

Handles diverse occlusion patterns (center, corners, structured blocks) more robustly than fixed-mask models.

Achieves high-quality inpainting while being computationally efficient, making it suitable for real-world applications such as:

Old photo restoration

Object removal & editing

Scene completion

Content-aware enhancement
