cmake_minimum_required(VERSION 3.27)

project(imgui VERSION 1.91.2)

add_library(imgui STATIC)
target_include_directories(imgui PUBLIC .)
target_sources(imgui PRIVATE
	imgui.cpp
	imgui_draw.cpp
	imgui_widgets.cpp
	imgui_demo.cpp
	imgui_tables.cpp
	backends/imgui_impl_glfw.cpp
	backends/imgui_impl_opengl3.cpp
	misc/cpp/imgui_stdlib.cpp
)
target_link_libraries(imgui PRIVATE glfw glad)
