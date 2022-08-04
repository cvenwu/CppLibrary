# CppLibrary
一些C/C++的常用工具库

## 使用步骤
1. `git clone git@github.com:sivanWu0222/CppLibrary.git`到本地
2. 编写的项目引入对应项目名称下的头文件(位于include目录)
3. 编写的项目链接对应项目名称下的库文件(位于lib目录)

## jsoncpp
> jsoncpp的使用

1. `git clone git@github.com:sivanWu0222/CppLibrary.git`
2. 编写使用jsoncpp的main.cpp：
        ```c++
    #include <iostream>
    #include <json.h>

    using namespace std;
    using namespace Json;

    int main()
    {
        Value root;
        root.append("123");
        
        FastWriter writer;
        cout << writer.write(root) << endl;
        cout << root.toStyledString() << endl;


        Value result(Json::objectValue);

        result["name"] = "12w3";

        // 判断是否是类对应的成员
        cout << result.isMember("name") << endl;

        cout << result.isObject() << endl;

        return 0;
    }
    ```
3. 编译该文件：`g++ main.cpp -o main -I CppLibrary/jsoncpp/include -L CppLibrary/jsoncpp/lib -l jsoncpp`