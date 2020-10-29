# Hello Thrift C++

here's how I got the thrift dependencies installed via conan

```
cd build_cmake
conan install .. 

cmake .. -DCMAKE_BUILD_TYPE=Release
cmake --build .

cd bin/
chmod +x client
chmod +x server
```
