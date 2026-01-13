# About

    This is my personal Vulkan API learning project.
    I will keep things general as much as I can, meaning only a few core abstractions 
    will be implemented in the single header and more complex Vulkan things expected 
    to be created on the fly.
    Demos in my another project called leisure-software-renderer will be implemented
    in this Vulkan based project.
    
    My implementation philosophy in Vulkan terms, like new abstraction on demand becomes
    - New resource bundle struct (my RenderTarget pattern in the leisure-software-renderer)
        RT_ColorDepthMotion { Image color, depth, motion; }
    - New pass struct
        MotionBlurPass { Pipeline p; DescriptorSet ds; record(...) } so on...


# Todos
    
Core Vulkan Abstractions will be implemented as single header in the near future

    Context     : instance/device/queue/surface + function loader + allocator
    Swapchain   : swap images/views + format/extent + resize/recreate
    Frame       : cmd pool/buffer + fence + acquire/render semaphores
    Image       : image + view + allocation + format/extent/usage + currentLayout
    Buffer      : buffer + allocation + size/usage + map/unmap (and staging helper)
    Descriptors : set layout + pool + allocate/update set, descriptor writer helper
    Pipeline    : pipeline + layout (+ shader modules), graphics + compute variants
    Pass        : record(cmd, inputs, outputs); owns pipeline + descriptor set(s)

Demos

    Hello World Triangle
    Hello 3D Model Wireframe
    Hello Various 3D lighntening models like Bling-Phong...
    Hello Multi Pass, motion blur, depth of field so on...

Some advanced and ambitious things will be considered in the future

    IBL
    Physically Based Rendering
    Pseudo lens flare
    Motion blur
    Depth of Field
    God rays
    Shadow mapping
    Ambient Occlusion
    Global Illumination
    Path tracing

    Deferred Rendering
    Tiled Forward+



# ENV and Dependencies

Windows 11 + WSL2 + Vulkan 1.3+

    sudo apt install automake m4 libtool cmake build-essential
    sudo apt install libssl-dev
    sudo apt install libsdl2-dev
    sudo apt install libpng-dev
    sudo apt install libsdl2-image-dev
    sudo apt install libglm-dev
    sudo apt install libassimp-dev
    sudo apt install mesa-vulkan-drivers 
    sudo apt install vulkan-tools 
    sudo apt install libvulkan-dev
    sudo ldconfig
    vulkaninfo | less


# Compilation steps

    cd cpp-folders && mkdir build && cd build && cmake ..
    make -j20

    cd src && cd hello-world-vulkan
    ./HelloVulkanSDL2



# References
