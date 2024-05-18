---
date: "2024-05-18T14:03:19+03:00"
description: ""
id: vuy9wftd6mr4j524o0c7hvv
publish: true
title: Shell
updated: 1716037904821
---

Скриптовый язык оболочки

## Bash 4

Усовершенствованный вариант языка shell

<https://www.gnu.org/software/bash/manual/html_node/> - дока

### Ассоциативные массивы
  
```bash
# объявление ассоциативного массива
declare -A mydict

# присвоение значения ключу
mydict["name"]="alex"

# значения (см. Shell Parameter Expansion если не понятно как работает @)
{hashes[@]}

# ключи (см. Shell Parameter Expansion если не понятно как работает @)
{!hashes[@]}
```

### Парсинг коротких флагов

Двоеточие в строчке с флагами значит, что ожидается значение для флага

```bash
while getopts ":a:b" option; do
  case $option in
    a)
      # код исполняемый при получении флага "a"
      example_a="$OPTARG" # - $OPTARG - значение параметра
      ;;
    b)
      # код исполняемый при получении флага "b"
      example_a="$OPTARG"
      ;;
    *)
      # код исполняемый при неправильном флаге
      echo "Usage: $0 [-a a] [-b b]"
      exit 1
      ;;
  esac
done
```

