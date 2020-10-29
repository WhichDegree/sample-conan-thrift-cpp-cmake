# Hello Thrift C++

here's how I got the thrift dependencies installed via conan

```
cd build_gcc
conan install .. -g compiler_args

g++ ../src/hello_client.cpp ../src/gen-cpp/helloSvc.cpp @conanbuildinfo.args -o client -Wall -std=c++11
g++ ../src/hello_server.cpp ../src/gen-cpp/helloSvc.cpp @conanbuildinfo.args -o server -Wall -std=c++11

chmod +x client
chmod +x server
```
