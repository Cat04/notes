 1. cконфигурировать Vagrant, добавить forwarded_port:
> config.vm.network "forwarded_port", guest: 8080, host: 8080
 2. выполнить:
> vagrant reload
 4. cконфигурировать Java:
>  -Dcom.sun.management.jmxremote \ 
> -Dcom.sun.management.jmxremote.port=9010 \  -Dcom.sun.management.jmxremote.rmi.port=9010 \  -Djava.rmi.server.hostname=127.0.0.1 \  -Dcom.sun.management.jmxremote.authenticate=false \  -Dcom.sun.management.jmxremote.ssl=false \
 4. подключиться при помощи jconsole или jvisualvm;

