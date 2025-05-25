# LLMs and AI Tools for Extracting Animations from Videos

## Overview

This report examines recent developments in Large Language Models (LLMs) and AI tools for extracting animations from videos, with a focus on applications for WebXR fitness instructors. As of May 2025, the field has seen significant advancements in AI-driven motion capture, animation extraction, and 3D character animation, making these technologies increasingly accessible to developers without specialized motion capture equipment.

The integration of LLMs with motion capture technologies has enabled more efficient, accurate, and interactive human motion generation and editing. This report covers single and multi-angle approaches, costs, accuracy metrics, limitations, and the latest developments in the field.

## Key Tools & Models

### AI Motion Capture Solutions

#### 1. **Rokoko Vision**
- **Technology**: Browser-based AI mocap using webcams or uploaded videos
- **Approach**: Offers both single-camera and dual-camera setups
- **Output**: Exports to FBX or BVH formats for use in 3D software
- **Pricing**: Free for recordings up to 15 seconds; subscription required for dual-camera setup
- **Integration**: Works with Rokoko Studio software for cleanup and retargeting
- **URL**: [Rokoko Vision](https://www.rokoko.com/products/vision)

#### 2. **DeepMotion Animate 3D**
- **Technology**: AI-driven motion capture from 2D videos
- **Features**: Markerless motion capture, multi-person tracking
- **Output**: Exports in multiple formats (FBX, BVH, GLB)
- **Integration**: APIs and SDKs for embedding in web applications
- **URL**: [DeepMotion](https://www.deepmotion.com/)

#### 3. **Plask**
- **Technology**: AI-powered 3D animation from videos
- **Features**: Effortless video import, seamless model animation
- **Output**: High-quality video renders or 3D assets compatible with industry tools
- **Integration**: Exports to Unreal, Maya, and Blender
- **URL**: [Plask](https://plask.ai/)

#### 4. **Cartwheel**
- **Technology**: AI platform for 3D animation creation
- **Features**: Converts text, video, or motion library prompts into rigged 3D characters
- **Capabilities**: Text-to-motion generation, motion remixing, in-browser rigging
- **Impact**: Reduces animation creation time from days to minutes
- **Backing**: Investors include Jeffrey Katzenberg's WndrCo, with leadership from Pixar, Google, and OpenAI veterans

#### 5. **QuickMagic AI**
- **Technology**: AI motion capture for extracting animations from smartphone videos
- **Integration**: Compatible with Unreal Engine 5 for WebXR applications
- **URL**: [QuickMagic](https://www.quickmagic.ai/)

### LLM-Driven Motion Systems

#### 1. **Motion-Agent**
- **Technology**: Conversational framework for human motion generation with LLMs
- **Approach**: Uses open-source pre-trained LLMs to develop versatile human motion generation systems
- **Method**: Employs a motion-language bridge by encoding and quantizing human motions into discrete tokens
- **Capabilities**: Enables complex motion generation, editing, and understanding without extensive retraining
- **Reference**: [arXiv:2405.17013](https://arxiv.org/abs/2405.17013)

#### 2. **MotionGPT**
- **Technology**: Treats human motion as a "foreign language" by converting 3D motion data into tokens
- **Capabilities**: Text-driven motion generation, captioning, and prediction
- **Reference**: [MotionGPT](https://motion-gpt.github.io)

#### 3. **MotionLLM**
- **Technology**: Jointly models motion, text, and video data
- **Capabilities**: Facilitates human behavior comprehension and real-time interaction
- **Reference**: [Hugging Face Blog](https://huggingface.co/blog/EvanTHU/motionllm)

## Comparison Matrix

| Tool/Platform | Approach | Cost | Accuracy | Single vs Multi-view | Licensing | WebXR Integration |
|---------------|----------|------|----------|----------------------|-----------|-------------------|
| **Rokoko Vision** | AI webcam mocap | Free (15s), Subscription for dual-cam | Good (better with dual-cam) | Both supported | Commercial use allowed | Via FBX/BVH export |
| **DeepMotion** | AI video-to-3D | Subscription-based | High for simple movements | Single-view | Commercial use allowed | API available |
| **Plask** | AI video-to-animation | Free tier available | High for visible movements | Single-view | Commercial use allowed | Via standard formats |
| **Cartwheel** | AI text/video-to-3D | Not publicly disclosed | Very high | Single-view | Commercial | Via export to standard formats |
| **QuickMagic** | AI smartphone video | Not publicly disclosed | Medium-high | Single-view | Commercial | Unreal Engine 5 integration |
| **Motion-Agent** | LLM-driven | Research model | High for supported motions | N/A (text-based) | Research | Requires implementation |
| **MotionGPT** | LLM-driven | Research model | High for supported motions | N/A (text-based) | Research | Requires implementation |

### Pricing Considerations

AI animation and video generation platforms typically offer tiered pricing models:

- **Basic plans**: $8-15/month for essential features
- **Professional plans**: $30-35/month for advanced features like longer clips, higher resolution
- **Enterprise options**: $30-225/month with features like scene control, multiple languages, and API access

Most platforms use either credit-based systems (pay per minute/clip) or subscription tiers with varying feature access.

## Latest Developments (≤ May 2025)

### 1. **Enhanced Multimodal Fusion**
Recent advancements incorporate hyperbolic embeddings, hierarchical fusion modules, and advanced attention mechanisms to better capture semantic relationships between text and motion, leading to more precise and context-aware motion extraction.

### 2. **Zero-Shot and Few-Shot Learning**
Leveraging the zero-shot capabilities of large language models, newer motion capture systems require less annotated data, enabling rapid adaptation to new motion styles, activities, or environments with minimal fine-tuning.

### 3. **Real-Time, Interactive Systems**
The integration of LLMs with game engines and WebXR platforms has improved, enabling real-time, natural language-driven motion control and editing, essential for immersive VR, AR, and human-computer interaction.

### 4. **NeRF to Rigged Mesh Conversion**
Recent techniques like MeshLRM (2024) and NeRF2Mesh (2024) enable high-quality mesh extraction from Neural Radiance Fields (NeRFs), supporting rigged animations and deformation. These approaches enhance the ability to generate riggable, animated meshes directly from NeRFs.

### 5. **Hybrid Explicit Representation**
New approaches combine NeRF with explicit mesh and Gaussian splatting techniques, allowing for head avatars and complex scene reconstructions that are both view-dependent and riggable.

## Limitations & Open Issues

### 1. **Accuracy and Occlusion Challenges**

- **Single-view limitations**: Single-camera systems show higher measurement errors due to occlusion and perspective limitations, with joint position errors often exceeding 20mm in less ideal configurations.
- **Multi-view advantages**: Multi-camera systems significantly improve accuracy, with joint position errors below 10mm, comparable to marker-based systems.
- **Occlusion handling**: Single-camera systems struggle with occluded limbs, while multi-camera setups maintain measurement integrity during complex movements.

### 2. **Technical Constraints**

- **Quality vs. rendering fidelity**: Achieving precise geometry while maintaining view-dependent effects remains challenging.
- **Real-time performance**: While methods like MeshLRM aim for fast inference, integrating these into real-time pipelines for complex scenes is ongoing work.
- **Rigging complex scenes**: Automating rigging for detailed, textured, and deformable NeRF-derived meshes is an active area of research.

### 3. **Data and Training Limitations**

- **Data scarcity and bias**: Despite large datasets, capturing the full diversity of human motion remains challenging, and models may inherit biases present in training data.
- **Semantic granularity**: Achieving fine-grained, semantically accurate motion generation from complex textual descriptions continues to be a technical hurdle.
- **Computational efficiency**: Balancing model complexity with real-time performance is essential for practical deployment in interactive applications.

## Integration Tips for WebXR (C#/Java dev)

### 1. **WebXR Animation Pipeline Optimization**

- **Asset optimization**: Use low-poly models with optimized textures, normal maps, and procedural textures to reduce resource demands.
- **Rig simplification**: Employ simplified rigs with fewer joints and efficient skinning methods (linear or dual quaternion skinning) to reduce runtime costs.
- **Animation data compression**: Apply skeletal compression (reducing joints by up to 70%), mesh compression, and texture compression to minimize data size.
- **Runtime rendering optimization**: Utilize WebGL/WebGPU with Level of Detail (LOD), culling, batching, and baking animations to reduce CPU/GPU load.

### 2. **Framework Selection**

- **A-Frame**: Open-source web framework built on three.js, allowing declarative creation of VR scenes with built-in animation components.
- **Needle Engine**: Comprehensive WebXR development platform supporting WebXR standards across devices, with built-in components for XR scene management and animation.
- **three.js**: Powerful JavaScript library for 3D rendering, supporting complex animations via keyframes, morph targets, and custom shaders.

### 3. **Implementation Strategies**

- **Avatar animation**: Use rigged avatars from VRoid or ReadyPlayerMe, animate using keyframes in Blender or Unity, export as glTF, and import into WebXR via Needle Engine or A-Frame.
- **Interactive feedback**: Overlay instructional UI elements using DOM overlays or 2D sprites, and animate feedback cues with A-Frame's animation component or Needle scripting.
- **Realistic movement**: Use motion capture data from AI tools like Rokoko Vision or DeepMotion, blend animations for transitions between exercises, and incorporate procedural animations for dynamic feedback.

### 4. **Performance Considerations**

- **Data streaming**: Implement animation streaming to reduce initial load times and memory usage.
- **Hybrid rendering**: Focus rendering resources where the user is looking to optimize performance without sacrificing visual fidelity.
- **Cloud computing**: Consider offloading complex calculations and streaming optimized assets to lower local processing costs.

## References/Links

1. Rokoko Vision. (2025). Free AI motion capture tool. https://www.rokoko.com/products/vision

2. DeepMotion. (2025). Bringing Digital Humans to Life With AI. https://www.deepmotion.com/

3. Plask. (2025). AI-Powered 3D Animation. https://plask.ai/

4. QuickMagic. (2025). AI Motion Capture for 3D Animation Generation. https://www.quickmagic.ai/

5. arXiv:2405.17013 [cs.CV]. (2025). Motion-Agent: A Conversational Framework for Human Motion Generation with LLMs. https://arxiv.org/abs/2405.17013

6. Jiang et al., NeurIPS 2023. (2023). MotionGPT. https://motion-gpt.github.io

7. Hugging Face Blog. (2024). MotionLLM. https://huggingface.co/blog/EvanTHU/motionllm

8. Fast Company. (2025). Cartwheel uses AI to make 3D animation 100 times faster for creators and studios. https://www.fastcompany.com/91337364/cartwheel-uses-ai-to-make-3d-animation-100-times-faster-for-creators-and-studios

9. Nature Scientific Reports. (2023). Comparison of markerless and marker-based motion capture systems using 95% functional limits of agreement in a linear mixed-effects modelling framework. https://www.nature.com/articles/s41598-023-49360-2

10. Needle Engine Documentation. (2025). WebXR. https://engine.needle.tools/docs/xr.html

11. MDN Web Docs. (2023). Rendering and the WebXR frame animation callback. https://developer.mozilla.org/en-US/docs/Web/API/WebXR_Device_API/Rendering

12. OWNverse. (2023). XR Animation Pipelines for Maximum Efficiency. https://ownverse.medium.com/xr-animation-pipelines-for-maximum-efficiency-ba00216ce67c
