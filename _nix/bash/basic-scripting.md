---

link: http://kvz.io/blog/2013/11/21/bash-best-practices/

---

Самый минимум для нормально программирования на bash:

- Нужно использовать полные названия опций `logger --priority` вместо `logger -p`
- `set -o errexit`, `set -e` - выходит из скрипта при ошибке
- `|| true` - разрешает команде выполняться с ошибкой
- `set -o nounset`, `set -u` - выходить при обращении к неопределённой переменной
- `echo ${NAME:-bubujka}` - значение по умолчанию, если переменная не определена
- `set -o xtrace`, `set -x` - печатать каждую команду что исполняется
- `set -o pipefail` - обрывать выполнение если хоть одна команда в пайпе вернула ненулевой статус. `mysqldump | gzip`
- Переменные нужно брать в фигурные скобки `ls /srv/${ENV}_app`
