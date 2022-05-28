### Hi there 👋
# Установка gh в Linux и BSD

Пакеты, загруженные с https://cli.github.com или с https://github.com/cli/cli/releases
считаются официальными двоичными файлами. Мы ориентируемся на популярные дистрибутивы Linux и
следующие архитектуры ЦП: i386, amd64, arm64, armhf.

Другие источники для установки поддерживаются сообществом и поэтому могут отставать.
наш график выпуска.

## Официальные источники

### Debian, Ubuntu Linux, ОС Raspberry Pi (подходит)

Установить:

``` ударить
curl -fsSL https://cli.github.com/packages/githubcli-archive-keyring.gpg | sudo dd of=/usr/share/keyrings/githubcli-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages стабильная основная" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null
судо подходящее обновление
sudo apt установить gh
```

Обновление:

``` ударить
судо подходящее обновление
sudo apt установить gh
```

### Fedora, CentOS, Red Hat Enterprise Linux (dnf)

Установите из нашего репозитория пакетов для немедленного доступа к последним выпускам:

``` ударить
sudo dnf install 'dnf-command (config-manager)'
sudo dnf config-manager --add-repo https://cli.github.com/packages/rpm/gh-cli.repo
sudo dnf установить gh
```

Также можно установить из [репозитория сообщества] (https://packages.fedoraproject.org/pkgs/gh/gh/):

``` ударить
sudo dnf установить gh
```

Обновление:

``` ударить
sudo dnf обновить gh
```

### openSUSE/SUSE Linux (zypper)

Установить:

``` ударить
sudo zypper addrepo https://cli.github.com/packages/rpm/gh-cli.repo
sudo zypper ссылка
sudo zypper установить gh
```

Обновление:

``` ударить
sudo zypper ссылка
sudo zypper обновить gh
```

## Ручная установка

* [Загрузить бинарные файлы релиза][страница релизов], соответствующие вашей платформе; или же
* [Сборка из исходников](./source.md).

## Неофициальные методы, поддерживаемые сообществом

Команда интерфейса командной строки GitHub не поддерживает следующие пакеты или репозитории, поэтому мы не можем обеспечить поддержку этих методов установки.

### Снап (не использовать)

Существует [так много проблем с Snap](https://github.com/casperdcl/cli/issues/7) в качестве механизма выполнения для таких приложений, как GitHub CLI, что наша команда предлагает _никогда не устанавливать gh как Snap_.

### Арх Линукс

Пользователи Arch Linux могут установить из [репозитория сообщества] [репозиторий Arch Linux]:

``` ударить
sudo pacman -S github-кли
```

В качестве альтернативы используйте [неофициальный пакет AUR][arch linux aur] для сборки GitHub CLI из исходного кода.

### Андроид

Пользователи Android 7+ могут установить через [Termux](https://wiki.termux.com/wiki/Main_Page):

``` ударить
пакет установить гх
```

### FreeBSD

Пользователи FreeBSD могут установить из [коллекции портов](https://www.freshports.org/devel/gh/):

``` ударить
cd /usr/ports/devel/gh/ && сделать установку чистой
```

Или через [pkg(8)](https://www.freebsd.org/cgi/man.cgi?pkg(8)):

``` ударить
пакет установить гх
```

### NetBSD/pkgsrc

Пользователи NetBSD и пользователи [платформ, поддерживаемых pkgsrc](https://pkgsrc.org/#index4h1) могут установить [пакет gh](https://pkgsrc.se/net/gh):

``` ударить
pkgin установить гх
```

Для установки из исходников:

``` ударить
cd /usr/pkgsrc/net/gh && make package-install
```

### OpenBSD

В -current или в выпусках, начиная с 7.0, пользователи OpenBSD могут устанавливать из пакетов:

```
pkg_add github-кли
```

### Funtoo

В Funtoo Linux есть автоматически сгенерированный пакет github-cli, расположенный в [dev-kit](https://github.com/funtoo/dev-kit/tree/1.4-release/dev-util/github-cli), который можно установил следующим образом:

``` баш
появление -av github-кли
```

Обновление можно выполнить, синхронизировав репозитории, а затем запросив обновление:

``` баш
синхронизация эго
выйти -u github-кли
```

### Генту

Пользователи Gentoo Linux могут установить из [основного дерева портежей](https://packages.gentoo.org/packages/dev-util/github-cli):

``` баш
появление -av github-кли
```

Обновление можно выполнить, обновив дерево портежей, а затем запросив обновление:

``` баш
появиться --sync
выйти -u github-кли
```

### Поцелуй Линукс

Пользователи Kiss Linux могут установить из [репозиториев сообщества] (https://github.com/kisslinux/community):

``` ударить
поцелуй б github-cli && поцелуй я github-cli
```

### Никс/НиксОС

Пользователи Nix/NixOS могут установить из [nixpkgs](https://search.nixos.org/packages?show=gitAndTools.gh&query=gh&from=0&size=30&sort=relevance&channel=20.03#disabled):

``` ударить
nix-env -iA nixos.gitAndTools.gh
```

### openSUSE Перекати-поле

Пользователи openSUSE Tumbleweed могут установить из [официального репозитория дистрибутива] (https://software.opensuse.org/package/gh):
``` ударить
sudo zypper в гх
```

### Альпийский Linux

Пользователи Alpine Linux могут установить из [репозиторий пакетов сообщества стабильных выпусков] (https://pkgs.alpinelinux.org/packages?name=github-cli&branch=v3.15).

``` ударить
apk добавить github-cli
```

Пользователи, которым нужна последняя версия CLI, не дожидаясь переноса в стабильную версию, которую они используют, должны использовать пограничную версию
репозиторий сообщества с помощью этого метода, описанного ниже, без смешивания пакетов из стабильных и нестабильных репозиториев.[^1]

``` ударить
echo "@community http://dl-cdn.alpinelinux.org/alpine/edge/community" >> /etc/apk/repositories
apk добавить github-cli@community
```

### Пустой линукс
Пользователи Void Linux могут установить из [официального репозитория дистрибутива] (https://voidlinux.org/packages/?arch=x86_64&q=github-cli):

``` ударить
sudo xbps-установить github-cli
```

[страница релизов]: https://github.com/cli/cli/releases/latest
[репозиторий Arch Linux]: https://www.archlinux.org/packages/community/x86_64/github-cli
[архив Linux aur]: https://aur.archlinux.org/packages/github-cli-git
[^1]: https://wiki.alpinelinux.org/wiki/Package_management#Repository_pinning
<!--
**Serik99/Serik99** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
