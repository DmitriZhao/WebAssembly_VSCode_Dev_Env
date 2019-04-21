# WebAssembly Developing Environment in VSCode Demo

## Check before use

1. Setup your Docker-Emscripten environment: [[中文]] [[EN]]

2. In .vscode/task.json:

        docker run --rm -it -v %cd%:/src apiaryio/emcc emcc hello.cc -o ./wwwroot/hello.js"

    *%cd%* stands for current directory in Windows. In a POSIX environment (Linux or macOS), it should be changed into:

        docker run --rm -it -v `pwd`:/src apiaryio/emcc emcc hello.cc -o ./wwwroot/hello.js"

[中文]: https://github.com/3dgen/cppwasm-book/blob/master/zh/ch1-quick-guide/ch1-01-install.md#112-docker%E7%8E%AF%E5%A2%83%E5%AE%89%E8%A3%85emscripten   "cppwasm-book §1.1.2: Docker环境安装Emscripten"

[EN]: https://github.com/3dgen/cppwasm-book/blob/master/en/ch1-quick-guide/ch1-01-install.md#112-installing-emscripten-in-a-docker-environment   "cppwasm-book §1.1.2: Installing Emscripten in a Docker environment"