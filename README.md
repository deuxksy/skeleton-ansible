# skeleton

## 목차
1. 실행하기
2. 폴더구조

## 1. 실행 하기
```bash
    ansible-playbook -i hosts.yml site.yml
```


## 2. 폴더 구조
```
skeleton
├─group_vars
└─roles
    ├─common
    │  ├─defaults          #
    │  ├─files             #
    │  ├─handlers          #
    │  ├─meta              #
    │  ├─tasks             #
    │  ├─templates         #
    │  ├─tests             #
    │  └─vars              #
    └─module
        ├─defaults          #
        │  └─mainn.yml     #
        ├─files             # copy, script tasks 는 /path/to/file 쓰지 않고도 참조 가능
        ├─handlers          #
        │  └─mainn.yml     # handlers 추가
        ├─meta              #
        │  └─mainn.yml     # role dependencies 추가
        ├─tasks             # include tasks 는 /path/to/file 쓰지 않고도 참조 가능
        │  └─mainn.yml     # task 추가
        ├─templates         # template tasks 는 /path/to/file 쓰지 않고도 참조 가능
        │  └─tests         #
        └─vars              #
            └─mainn.yml     # variable 추가
```