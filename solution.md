- Mude para os repositórios de arquivo do Base usando:

```
sudo vi /etc/yum.repos.d/CentOS-Base.repo
```

obs: caso tenha conteúdo, pressione ```insert``` para poder apagar os dados.

- copie/cole o seguinte e observe a versão do seu SO. Altere se necessário. Nesta configuração está a versão 7.9.2009:

```
[base]
name=CentOS-$releasever - Base
baseurl=http://archive.kernel.org/centos-vault/7.9.2009/os/$basearch/
enabled=1
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7

#released updates
[updates]
name=CentOS-$releasever - Updates
baseurl=http://archive.kernel.org/centos-vault/7.9.2009/updates/$basearch/
enabled=1
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7

#additional packages that may be useful
[extras]
name=CentOS-$releasever - Extras
baseurl=http://archive.kernel.org/centos-vault/7.9.2009/extras/$basearch/
enabled=1
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7

#additional packages that extend functionality of existing packages
[centosplus]
name=CentOS-$releasever - Plus
baseurl=http://archive.kernel.org/centos-vault/7.9.2009/centosplus/$basearch/
enabled=0
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-7
```

- Para salvar o conteúdo você precisa fazer os seguintes passos:

1. Pressionar ```esc```
2. Depois digitar ```:wq```
3. Pressionar enter
