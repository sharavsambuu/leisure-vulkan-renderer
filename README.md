# About

    This is my personal Vulkan API learning project.
    I will keep things general as much as I can, meaning only a few core abstractions 
    will be implemented in the single header and more complex Vulkan things expected 
    to be created on the fly.
    Demos in my another project called leisure-software-renderer will be implemented
    in this Vulkan based project.


# Todos
    
Core Vulkan Abstractions will be implemented as single header in the near fututure

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

    sudo apt update && sudo apt install mesa-vulkan-drivers vulkan-tools libvulkan-dev
    vulkaninfo | less


# Compilation steps

    cd cpp-folders && mkdir build && cd build && cmake ..
    make -j20

    cd src && cd hello-world-vulkan
    ./HelloVulkanSDL2



# References
