---
layout: base
title: Tesseract and Leptonica
date: 2022-10-01
---
Platform: Ubuntu 22.04
```sh
sudo apt install libtesseract-dev
sudo apt-get install libleptonica-dev
```
include these into your CMakeLists.txt
```cmake
target_link_libraries(${PROJECT_NAME} PRIVATE tesseract)
target_link_libraries(${PROJECT_NAME} PRIVATE leptonica)
```
