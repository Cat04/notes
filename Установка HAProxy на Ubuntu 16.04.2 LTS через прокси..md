Для того, чтобы установить HAProxy на Ubuntu 16.04.2 LTS через прокси необходимо выполнить следующие найстроки: 
 1. в файле /etc/apt/apt.conf прописать настройки прокси сервера: 
> Acquire::http::proxy "http://username:password@proxy:3128/";
> Acquire::https::proxy "https://username:password@proxy:3128/";
> Acquire::ftp::proxy "ftp://username:password@proxy:3128/";
 2. в файле /etc/environment также прописать настройки прокси сервера: 
> PATH="/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games"
> http_proxy="http://username:password@proxy:3128/"
> https_proxy="https://username:password@proxy:3128/"
> ftp_proxy="ftp://username:password@proxy:3128/"
 3. открыть новую ssh-сессию;
 4. выполнить установку HAProxy версии 1.5: 
> sudo apt-get install software-properties-common
> sudo add-apt-repository ppa:vbernat/haproxy-1.5
> sudo apt-get update
> sudo apt-get install haproxy=1.5.\*

