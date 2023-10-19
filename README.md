
[![Build status](https://api.travis-ci.org/troydhanson/uthash.svg?branch=master)](https://travis-ci.org/troydhanson/uthash)
[![GitHub CI status](https://github.com/troydhanson/uthash/actions/workflows/build.yml/badge.svg)](https://github.com/troydhanson/uthash/actions/workflows/build.yml)

Documentation for uthash is available at:

https://troydhanson.github.io/uthash/


uthash：为 C 语言提供哈希表的库。由于 C 语言中没有类似字典的数据结构，该库提供了哈希表常见的查询、插入、删除、排序等函数。使用方法简单，仅需引入一个头文件

#include "uthash.h"

struct my_struct {
    int id;            /* we'll use this field as the key */
    char name[10];
    UT_hash_handle hh; /* makes this structure hashable */
};

struct my_struct *users = NULL;

void add_user(struct my_struct *s) {
    HASH_ADD_INT( users, id, s );
}
