cmake_minimum_required(VERSION 2.8)
project(coin_signing)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

file(GLOB SOURCE_ED "../../crypto_ops/crypto/ed25519_src/*.c" # All files in directory:
    )

set(SOURCE_FILES main.cpp c_token.cpp c_wallet.cpp c_mint.cpp c_encryption c_user.cpp
                 ${SOURCE_ED}
                 ../../crypto_ops/crypto/sha_src/sha512.cpp)

add_executable(coin_signing ${SOURCE_FILES})
