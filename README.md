# OpenGL_Exercises

## Overview (概要)
GLFW3を使ったモダンなOpenGLの練習  
環境はmacOS Sierra

## Requirement (依存関係のインストール)
```sh
$ brew install cmake,glfw3,glew,glm,assimp
```
	
## Build (ビルド方法)
### 通常
```sh
$ git clone https://github.com/ShaderKid/OpenGL_Exercises.git
$ cd OpenGL_Exercises
$ mkdir build
$ cd build
$ cmake ..
$ make
```

### Xcode8
```sh
$ git clone https://github.com/ShaderKid/OpenGL_Exercises.git
$ cd OpenGL_Exercises
$ mkdir build
$ cd build
$ cmake -G Xcode ..
$ open OpenGL_Exercises.xcodeproj
```