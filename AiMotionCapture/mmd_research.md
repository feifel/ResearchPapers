# MikuMikuDance (MMD) for Fitness Animation: Research Report

## Introduction

MikuMikuDance (MMD) is a free 3D animation software originally developed for creating animations featuring Vocaloid characters. This report explores its potential application for fitness animation in WebXR environments, with a focus on AI-assisted animation capabilities, learning curve, costs, open-source status, and ability to handle multiple persons and fitness equipment.

## AI-Assisted Animation from Video

### Current Capabilities

As of May 2025, several AI-powered solutions have emerged that significantly enhance MMD's capabilities for fitness animation:

1. **MiKaPo (MikuMikuDance Pose Picker)**: 
   - A web-based tool that automatically poses MMD models from video input in real-time
   - Developed by AmyangXYZ (available on [GitHub](https://github.com/AmyangXYZ/MiKaPo))
   - Uses Mediapipe for 3D keypoint detection, Babylon.js for 3D rendering, and babylon-mmd for MMD model support
   - Supports pose detection, face detection, and experimental hand detection
   - Features a Rust-WASM based pose-to-quaternion solver for accurate motion capture
   - Allows both video upload and webcam input options
   - Supports VMD import/export (requires recording at least one motion)

2. **Plask Motion**:
   - AI-powered motion capture from videos
   - Transforms simple footage into professional 3D animations
   - Supports exporting animations compatible with industry-standard software
   - Can animate MMD models with high fidelity

3. **Rokoko Vision**:
   - Free AI mocap tool enabling motion recording via webcam or uploaded videos
   - Supports single or dual-camera setups for improved accuracy
   - Exports data in formats like FBX and BVH, compatible with various 3D software

### Limitations and Challenges

- Current AI motion capture solutions may struggle with complex movements or when viewing from different angles
- Hand and finger tracking remains experimental in most solutions
- Performance optimization is necessary for real-time applications
- Accuracy may vary depending on video quality and lighting conditions

## Learning Curve

MMD has a moderate to steep learning curve, especially for users without prior 3D animation experience. However, AI-assisted tools have significantly reduced this barrier:

1. **Traditional MMD Workflow**:
   - Requires understanding of 3D animation principles
   - Manual keyframing and posing can be time-consuming
   - Physics simulation setup can be complex
   - Japanese interface in original software can be challenging for non-Japanese speakers

2. **AI-Assisted Workflow**:
   - Tools like MiKaPo significantly reduce the learning curve by automating the posing process
   - Web-based interfaces are generally more user-friendly than the original MMD software
   - Real-time feedback allows for quicker iteration and learning
   - Still requires understanding of basic 3D concepts and file formats

For a professional C# and Java programmer with limited 3D modeling knowledge, the learning curve would be manageable, especially with AI-assisted tools. The programming background would be beneficial for understanding the technical aspects and potentially extending the functionality through scripting or custom tools.

## Costs and Licensing

### Software Costs

1. **MMD Core Software**:
   - **Cost: Free** (distributed as freeware)
   - No licensing fee for its use
   - Available for free download from various sources

2. **AI-Assisted Tools**:
   - **MiKaPo**: Free and open-source (GPL-3.0 license)
   - **Plask Motion**: Freemium model with basic features free, premium features for subscribers
   - **Rokoko Vision**: Free basic version, with premium options for professional use

3. **Models, Motions, and Plugins**:
   - Most community models and motions are shared under Creative Commons licenses (free)
   - Some premium models and plugins may have associated costs
   - Commercial models might require licensing fees

### Open-Source Status

- **MMD Core**: Not open-source, but freely available as freeware
- **MiKaPo**: Fully open-source under GPL-3.0 license
- **Related Projects**: Several open-source projects enhance MMD functionality:
  - mmdagent-ex/MMDAgent-EX: Open-source platform compatible with MMD
  - blender_mmd_tools: Addon for Blender to import/export MMD models and motions
  - takahirox/mmd-viewer-js: Web-based MMD viewer (available on [GitHub](https://github.com/takahirox/mmd-viewer-js))

## Multi-Person and Equipment Support

### Multi-Person Animation

1. **Native Capabilities**:
   - MMD inherently supports multiple character models in a single scene
   - Each character can have independent animations and physics

2. **AI-Assisted Multi-Person Capture**:
   - Current AI solutions like MiKaPo primarily focus on single-person capture
   - Multi-person motion capture remains challenging but is an active area of development
   - Some workarounds include:
     - Capturing individuals separately and combining in post-processing
     - Using specialized multi-person mocap solutions and importing the data

### Fitness Equipment Support

1. **Equipment Representation**:
   - MMD can import and animate 3D models of fitness equipment
   - Models can be created in external 3D modeling software and imported into MMD
   - Physics simulation can be applied to equipment for realistic interaction

2. **Interaction Challenges**:
   - Realistic interaction between characters and equipment requires careful setup
   - Physics-based interactions may need manual adjustment for realistic results
   - AI motion capture may struggle to accurately capture equipment interaction

3. **Available Resources**:
   - Some fitness equipment models are available in MMD-compatible formats
   - Custom equipment can be modeled in software like Blender and exported to MMD
   - Specialized equipment like hurdle sets for agility training are available in MMD format

## Latest Developments and Integrations (May 2025)

### WebXR Integration

1. **Current Status**:
   - MMD models can be integrated into WebXR environments through various frameworks
   - Babylon.js with babylon-mmd plugin provides robust support for MMD in web environments
   - Three.js also offers MMD loaders and animation support

2. **Workflow**:
   - Models are typically converted from PMX/PMD to glTF or FBX formats
   - Animations can be applied using animation-mixer components
   - WebXR-compatible pages can embed these models for immersive experiences

### Unity Integration

1. **Unity 2025 Features**:
   - Unity's 2025 roadmap includes several features beneficial for MMD integration:
     - New animation system with procedural rigging and remapping capabilities
     - Support for animation blending with per-bone masking
     - AI-driven animation tools including video-to-motion conversion
     - Improved performance for complex scenes with many characters

2. **VRM Support**:
   - VRM format (an extension of glTF) is increasingly supported across platforms
   - Allows for standardized avatar use across applications
   - Tools like XR Animator plugin provide drag-and-drop interfaces to load MMD motions onto VRM models

### Performance Optimizations

1. **Web-Based Rendering**:
   - WebGL 2.0 and WebGPU advancements improve performance for browser-based applications
   - Optimized shaders and rendering techniques enable more complex scenes

2. **Mobile Support**:
   - Improved mobile GPU capabilities allow for more complex MMD models on smartphones and standalone VR headsets
   - Optimized model formats and LOD systems help maintain performance

## Conclusion

MikuMikuDance, especially when enhanced with AI-assisted animation tools, presents a viable option for creating fitness animations for WebXR applications. The combination of free/low-cost software, increasingly user-friendly interfaces, and powerful AI motion capture capabilities makes it accessible even for users with limited 3D animation experience.

For a professional programmer looking to create a virtual fitness instructor, the MMD ecosystem offers several advantages:

1. **Cost-Effective**: The core software and many tools are free or low-cost
2. **AI-Assisted Workflow**: Significantly reduces the learning curve and production time
3. **Web Integration**: Strong support for web-based deployment through WebXR
4. **Active Development**: Ongoing improvements in AI motion capture and web rendering

However, challenges remain in multi-person capture and equipment interaction, which may require additional work or alternative solutions for complex fitness scenarios.

## Recommendations

1. **Start with MiKaPo**: As an open-source, web-based solution, it offers the most accessible entry point for AI-assisted MMD animation
2. **Consider Unity Integration**: For more complex applications, Unity's upcoming animation features provide powerful capabilities
3. **Test with Simple Exercises**: Begin with single-person exercises without equipment before attempting more complex scenarios
4. **Explore VRM Format**: For cross-platform compatibility, consider using or converting to VRM format
5. **Combine with Other Tools**: For professional results, consider using MMD in conjunction with other specialized tools for specific aspects of the workflow

## Sources

1. [MiKaPo GitHub Repository](https://github.com/AmyangXYZ/MiKaPo)
2. [MiKaPo Demo on Babylon.js Forum](https://forum.babylonjs.com/t/mikapo-ai-pose-picker-for-mmd-model-demo/53617)
3. [MMD Viewer JS GitHub Repository](https://github.com/takahirox/mmd-viewer-js)
4. [Unity 2025 Product Roadmap](https://www.cgchannel.com/2025/03/unity-unveils-its-2025-product-roadmap/)
5. [Army PRT: Military Movement Drill Information](https://www.armyprt.com/endurance_and_mobility_activities/military-movement-drill-2-mmd-2.shtml)
