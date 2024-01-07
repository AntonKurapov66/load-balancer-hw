# Домашнее задание к занятию "Отказоустойчивость в облаке" - `Курапов Антон`

### Задание 1
Возьмите за основу решение к заданию 1 из занятия «Подъём инфраструктуры в Яндекс Облаке».

* Теперь вместо одной виртуальной машины сделайте terraform playbook, который:
   * создаст 2 идентичные виртуальные машины. Используйте аргумент count для создания таких ресурсов;
   * создаст таргет-группу. Поместите в неё созданные на шаге 1 виртуальные машины;
   * создаст сетевой балансировщик нагрузки, который слушает на порту 80, отправляет трафик на порт 80 виртуальных машин и http healthcheck на порт 80 виртуальных машин.

* Установите на созданные виртуальные машины пакет Nginx любым удобным способом и запустите Nginx веб-сервер на порту 80.

* Перейдите в веб-консоль Yandex Cloud и убедитесь, что:
    * созданный балансировщик находится в статусе Active,
    * обе виртуальные машины в целевой группе находятся в состоянии healthy.
* Сделайте запрос на 80 порт на внешний IP-адрес балансировщика и убедитесь, что вы получаете ответ в виде дефолтной страницы Nginx.
  * В качестве результата пришлите:
    * Terraform Playbook.
    * Скриншот статуса балансировщика и целевой группы.
    * Скриншот страницы, которая открылась при запросе IP-адреса балансировщика.



 * Запуск и отработка тераформ плейбука:
   
![alt text](https://github.com/AntonKurapov66/load-balancer-hw/blob/main/img/scr_1.PNG)

![alt text](https://github.com/AntonKurapov66/load-balancer-hw/blob/main/img/scr_4.PNG)

* Скриншот статуса балансировщика и целевой группы.
![alt text](https://github.com/AntonKurapov66/load-balancer-hw/blob/main/img/scr_2.PNG)

![alt text](https://github.com/AntonKurapov66/load-balancer-hw/blob/main/img/scr_3.PNG)

![alt text](https://github.com/AntonKurapov66/load-balancer-hw/blob/main/img/scr_6.PNG)

* Скриншот страницы, которая открылась при запросе IP-адреса балансировщика.
![alt text](https://github.com/AntonKurapov66/load-balancer-hw/blob/main/img/scr_5.PNG)




terraform playbook: https://github.com/AntonKurapov66/load-balancer-hw/blob/main/fail-hw/main.tf

