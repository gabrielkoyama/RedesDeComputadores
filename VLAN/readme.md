# Sobre:
Configuração de uma VLAN

# AMBIENTE

[vlan](images/vlan.png)

# Cenário:

## SWITCH 01

* fa 0/1 192.168.1.10
* fa 0/1 192.168.1.11

* fa 0/3 192.168.1.20
* fa 0/4 192.168.1.21	

---

## SWITCH 02

fa 0/1 192.168.1.12
fa 0/1 192.168.1.13

fa 0/3 192.168.1.22
fa 0/4 192.168.1.23


---

# CONFIGURAÇÃO DOS SWHITCHS (VLAN)

>> Entrar no modo de superusuário

```

Switch>
Switch>enable
Switch#configure terminal

```

>> Criar uma VLAN

```
Switch(config)#vlan 100
Switch(config-vlan)#name alunos
Switch(config-vlan)#exit

Switch(config)#vlan 200
Switch(config-vlan)#name adm
Switch(config-vlan)#exit

```

>> Insrir uma porta em uma VLAN

```

Switch(config)#interface FastEthernet0/1
Switch(config-if)#switchport access vlan 100
Switch(config-if)#exit

```

>> Insrindo outra porta em uma VLAN

```

Switch(config)#interface FastEthernet0/2
Switch(config-if)#switchport access vlan 100
Switch(config-if)#exit

```



