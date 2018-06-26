add_library(imgui
"imgui.cpp"
"imgui.h"
"imgui_draw.cpp"
)
add_executable(imgui_example_ogl2
"examples/example_glfw_opengl2/main.cpp"
"imgui_demo.cpp"
"examples/imgui_impl_glfw.cpp"
"examples/imgui_impl_glfw.h"
"examples/imgui_impl_opengl2.h"
"examples/imgui_impl_opengl2.cpp"
)
include_directories(./ "examples")

target_link_libraries(imgui_example_ogl2 imgui glfw gl3w)