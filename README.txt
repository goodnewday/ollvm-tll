LLVM 6.0 + Ollvm + Armariris
================================
编译:

mkdir -p /opt/ollvm/
mkdir build
cd build
cmake  -G "Unix Makefiles" -DCMAKE_BUILD_TYPE=Release --prefix=/opt/ollvm/  DLLVM_INCLUDE_TESTS=OFF ../
make -j8

使用:
/opt/ollvm/bin/clang a.c -mllvm -fla  -mllvm -sobf  -mllvm -bcf  -o a

注意:
发现混淆字符串对于密钥的混淆有遗漏，混淆后应使用IDA确认一下;
