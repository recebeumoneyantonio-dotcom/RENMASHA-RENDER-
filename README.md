#🔥 RENMASHA Render

A Mali-optimized OpenGL ES rendering layer.

RENMASHA Render is a low-level rendering layer designed to optimize shader execution on Mali GPUs.
It intercepts and adapts the rendering pipeline to match Tile-Based Deferred Rendering (TBDR) architecture, enabling efficient shader execution without requiring modifications to shader packs.

#🎯 What is RENMASHA?

RENMASHA is not a mod.

It is a rendering backend layer that:

Translates generic shader behavior to Mali-optimized execution
Reduces memory bandwidth usage
Enables hardware-specific features (PLS, Framebuffer Fetch)
Improves performance and stability on mobile GPUs

#⚙️ Core Responsibilities

#🧠 Hardware Awareness

Detects GPU architecture (Bifrost / Valhall)
Maps real OpenGL ES capabilities
Handles incomplete extension exposure (MobileGlues)

#🔄 Shader Adaptation Layer

Injects hardware-specific defines
Sanitizes GLSL for OpenGL ES compatibility
Redirects unsupported features to safe paths

#⚡ Execution Optimization

Uses Tile-Based Rendering paths
Avoids unnecessary framebuffer flushes
Minimizes DRAM bandwidth usage

#💾 Binary Shader Cache

Uses GL_ARM_mali_shader_binary
Eliminates runtime compilation stutter

#🎨 Rendering Enhancements (Optional Layer)

Lighting correction (PLS-based)
Bloom (optimized multi-pass)
HDR-safe pipeline

#📉 Performance Management

Real-time FPS monitoring
Dynamic quality scaling
Safe fallback paths

#🔌 Integration Model

RENMASHA is designed to sit below high-level systems:

Layer
Role
Shader Packs
Visual logic
Iris Shaders
Shader loader
Sodium
Renderer replacement
RENMASHA
Execution optimization layer

#🚧 Current Limitations

MobileGlues may restrict extension visibility
Some shader packs assume desktop OpenGL behavior
Iris integration still partial (no full pipeline control yet)

#🧭 Roadmap

*Phase 3*
Stable PLS + FBFetch pipeline
Shader sanitization system

*Phase 4*

Full shader adaptation layer (Iris integration)
Zero-copy rendering paths

*Phase 5*
Independent shader execution pipeline
Mali-native shader ecosystem

*🧬 Philosophy
*The problem is not shaders.
The problem is how they are executed.*
