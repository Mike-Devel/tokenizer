# Copyright 2018 Mike Dev
# Distributed under the Boost Software License, Version 1.0.
# See accompanying file LICENSE_1_0.txt or copy at http://www.boost.org/LICENSE_1_0.txt

cmake_minimum_required(VERSION 3.5)
project(BoostTokenizer LANGUAGES CXX)

add_library(boost_tokenizer INTERFACE)
add_library(Boost::tokenizer ALIAS boost_tokenizer)

target_include_directories(boost_tokenizer INTERFACE include)

target_link_libraries(boost_tokenizer
    INTERFACE
        Boost::assert
        Boost::config
        Boost::config
        Boost::iterator
        Boost::mpl
        Boost::throw_exception
        Boost::type_traits
)
