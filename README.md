# ans
1.	На сервер устанавливаем следующие пакеты:
1.1	yum install –y epel-release
1.2	yum install –y ansible git
2.	клонируем репозиторий
git clone https://github.com/VasilyMoose/ans.git
3.	удаляем каталоги «ansible», что прописались при установке и переносим каталоги из клонированного репозитория.
rm -rf /etc/ansible/*
mv -f /root/ans/* /etc/ansible/
4.	в фале /etc/ ansible/hosts
прописываем ip address серверов и логин, и пароль
5.	запускаем ansible
ansible-playbook /etc/ansible/play.yml
