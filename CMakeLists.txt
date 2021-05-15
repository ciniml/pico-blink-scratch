cmake_minimum_required(VERSION 3.12)
# SDKの検索スクリプトをinclude (pico-sdk/externalからコピー)
include(pico_sdk_import.cmake)
# プロジェクトの基本設定
project(blink-scratch C CXX ASM)
set(CMAKE_C_STANDARD 11)   # C言語の規格=C11
set(CMAKE_CXX_STANDARD 17) # C++言語の規格=C++17
# SDKの初期化
pico_sdk_init()
# ソースコードの追加
add_executable(blink-scratch
    src/main.cpp
    )
# SDKのライブラリをリンク
target_link_libraries(blink-scratch pico_stdlib)
# 追加出力ファイルを設定
pico_add_extra_outputs(blink-scratch)

