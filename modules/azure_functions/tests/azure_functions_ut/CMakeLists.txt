#Copyright (c) Microsoft. All rights reserved.
#Licensed under the MIT license. See LICENSE file in the project root for full license information.

cmake_minimum_required(VERSION 2.8.11)

compileAsC99()
set(theseTestsName azure_functions_ut)

set(${theseTestsName}_test_files
${theseTestsName}.c
)

set(${theseTestsName}_c_files
	../../src/azure_functions.c	
)

set(${theseTestsName}_h_files
)

include_directories(${GW_INC})

build_c_test_artifacts(${theseTestsName} ON "gateway_modules_tests")