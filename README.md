# Jarkom-Modul-4-A02-2022
Kelompok A02
+ Ferdinand Putra Gumilang Silalahi - 5025201176
+ Naufal Adli Purnama - 5025201195
+ Bimantara Tito Wahyudi - 5025201227

## Soal
### Topologi
![Gambar Topologi](soal_shift_4.1.png)
## VLSM - CPT

## CIDR - GNS3

### Penggabungan Subnet

Berikut penggabungan subnet dengan metode CIDR dimulai dari subnet terjauh

### Penghitungan IP

Berikut pohon subnet yang dibentuk sesuai dengan penggabungan subnet sebelumnya

Didapat tabel data setiap subnet, yakni NID dan Netmask

Subnet | Network ID | Netmask
|:---:|:---:|:---:|
A1|10.0.4.0|255.255.252.0
A2|10.0.1.0|255.255.255.252
A3|10.0.0.0|255.255.255.0
A4|10.0.8.0|255.255.255.252
A5|10.0.16.0|255.255.255.192
A6|10.0.32.0|255.255.255.252
A7|10.0.144.0|255.255.255.252
A8|10.0.138.0|255.255.255.128
A9|10.0.132.0|255.255.255.252
A10|10.0.128.0|255.255.255.0
A11|10.0.129.0|255.255.255.252
A12|10.0.130.0|255.255.254.0
A13|10.0.137.0|255.255.255.252
A14|10.0.136.0|255.255.255.128
A15|10.0.136.128|255.255.255.128
A16|10.0.160.0|255.255.255.252
A17|10.0.162.0|255.255.254.0
A18|10.0.64.0|255.255.255.252




### Topologi GNS3

### Subnetting

Setelah dihitung ip untuk tiap subnet, maka sekarang saatnya mengatur ip pada tiap router, client dan server. Setiap interface node diatur sesuai ip yang telah dihitung dengan mengedit file `/etc/network/interfaces`. Setelah itu, jalankan command `iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE -s 10.0.0.0/16` untuk router `The Resonance` dan command `echo nameserver 192.168.122.1 > /etc/resolv.conf` untuk semua node lainnya. Command tersebut kemudian disimpan dalam `.bashrc` untuk otomasi.

#### The Resonance

```
auto eth0
iface eth0 inet dhcp
auto eth1
iface eth1 inet static
	address 10.0.32.1
	netmask 255.255.255.252
auto eth2
iface eth2 inet static
	address 10.0.144.1
	netmask 255.255.255.252
auto eth3
iface eth3 inet static
	address 10.0.160.1
	netmask 255.255.255.252
auto eth4
iface eth4 inet static
	address 10.0.64.1
	netmask 255.255.255.252
```

#### The Order

```
auto eth0
iface eth0 inet static
	address 10.0.32.2
	netmask 255.255.255.252
auto eth1
iface eth1 inet static
	address 10.0.16.1
	netmask 255.255.255.192
auto eth2
iface eth2 inet static
	address 10.0.8.1
	netmask 255.255.255.252
```

#### The Minister

```
auto eth0
iface eth0 inet static
	address 10.0.8.2
	netmask 255.255.255.252
auto eth1
iface eth1 inet static
	address 10.0.4.1
	netmask 255.255.252.0
auto eth2
iface eth2 inet static
	address 10.0.1.1
	netmask 255.255.255.252
```

#### The DauntLess

```
auto eth0
iface eth0 inet static
	address 10.0.1.2
	netmask 255.255.255.252
auto eth1
iface eth1 inet static
	address 10.0.0.1
	netmask 255.255.255.0
```

#### The Intrument

```
auto eth0
iface eth0 inet static
	address 10.0.144.2
	netmask 255.255.255.252
auto eth1
iface eth1 inet static
	address 10.0.138.1
	netmask 255.255.255.128
auto eth2
iface eth2 inet static
	address 10.0.132.1
	netmask 255.255.255.252
auto eth3
iface eth3 inet static
	address 10.0.137.1
	netmask 255.255.255.252
```

#### The Firefist

```
auto eth0
iface eth0 inet static
	address 10.0.132.2
	netmask 255.255.255.252
auto eth1
iface eth1 inet static
	address 10.0.128.1
	netmask 255.255.255.0
auto eth2
iface eth2 inet static
	address 10.0.130.1
	netmask 255.255.254.0
```

#### The Queen

```
auto eth0
iface eth0 inet static
	address 10.0.128.2
	netmask 255.255.255.0
auto eth1
iface eth1 inet static
	address 10.0.129.1
	netmask 255.255.255.252
```

#### The Profound

```
auto eth0
iface eth0 inet static
	address 10.0.137.2
	netmask 255.255.255.252
auto eth1
iface eth1 inet static
	address 10.0.136.1
	netmask 255.255.255.128
auto eth2
iface eth2 inet static
	address 10.0.136.129
	netmask 255.255.255.128
```

#### The Magical

```
auto eth0
iface eth0 inet static
	address 10.0.160.2
	netmask 255.255.255.252
auto eth1
iface eth1 inet static
	address 10.0.162.1
	netmask 255.255.254.0
```

#### Johan

```
auto eth0
iface eth0 inet static
	address 10.0.0.2
	netmask 255.255.255.0
	gateway 10.0.0.1
```

#### Phanora

```
auto eth0
iface eth0 inet static
	address 10.0.0.3
	netmask 255.255.255.0
	gateway 10.0.0.1
```

#### Guideau

```
auto eth0
iface eth0 inet static
	address 10.0.4.2
	netmask 255.255.252.0
	gateway 10.0.4.1
```

#### Ashaf

```
auto eth0
iface eth0 inet static
	address 10.0.16.2
	netmask 255.255.255.192
	gateway 10.0.16.1
```

#### The Witch

```
auto eth0
iface eth0 inet static
	address 10.0.129.2
	netmask 255.255.255.252
	gateway 10.0.129.1
```

#### Keith

```
auto eth0
iface eth0 inet static
	address 10.0.128.2
	netmask 255.255.255.0
	gateway 10.0.128.1
```

#### Oakleave

```
auto eth0
iface eth0 inet static
	address 10.0.130.2
	netmask 255.255.254.0
	gateway 10.0.130.1
```

#### Matt Cugat

```
auto eth0
iface eth0 inet static
	address 10.0.138.2
	netmask 255.255.255.128
	gateway 10.0.138.1
```

#### Helga

```
auto eth0
iface eth0 inet static
	address 10.0.136.2
	netmask 255.255.255.128
	gateway 10.0.136.1
```

#### Spendrow

```
auto eth0
iface eth0 inet static
	address 10.0.136.130
	netmask 255.255.255.128
	gateway 10.0.136.129
```

#### Corvekt

```
auto eth0
iface eth0 inet static
	address 10.0.162.2
	netmask 255.255.254.0
	gateway 10.0.162.1
```

#### Haines

```
auto eth0
iface eth0 inet static
	address 10.0.162.3
	netmask 255.255.254.0
	gateway 10.0.162.1
```

#### The Beast

```
auto eth0
iface eth0 inet static
	address 10.0.64.2
	netmask 255.255.255.252
	gateway 10.0.64.1
```

### Routing

Setelah pengaturan IP selesai, dilanjutkan dengan routing. Semua router menjalankan command route sesuai posisi dalam topologi. Command route ini kemudian disimpan dalam `.bashrc` untuk otomasi.

#### The Resonance

```
route add -net 10.0.4.0 netmask 255.255.252.0 gw 10.0.32.2
route add -net 10.0.1.0 netmask 255.255.255.252 gw 10.0.32.2
route add -net 10.0.0.0 netmask 255.255.255.0 gw 10.0.32.2
route add -net 10.0.8.0 netmask 255.255.255.252 gw 10.0.32.2
route add -net 10.0.16.0 netmask 255.255.255.192 gw 10.0.32.2
route add -net 10.0.138.0 netmask 255.255.255.128 gw 10.0.144.2
route add -net 10.0.132.0 netmask 255.255.255.252 gw 10.0.144.2
route add -net 10.0.128.0 netmask 255.255.255.0 gw 10.0.144.2
route add -net 10.0.129.0 netmask 255.255.255.252 gw 10.0.144.2
route add -net 10.0.130.0 netmask 255.255.254.0 gw 10.0.144.2
route add -net 10.0.137.0 netmask 255.255.255.252 gw 10.0.144.2
route add -net 10.0.136.0 netmask 255.255.255.128 gw 10.0.144.2
route add -net 10.0.136.128 netmask 255.255.255.128 gw 10.0.144.2
route add -net 10.0.162.0 netmask 255.255.254.0 gw 10.0.160.2
```

#### The Order

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.0.32.1
route add -net 10.0.4.0 netmask 255.255.252.0 gw 10.0.8.2
route add -net 10.0.1.0 netmask 255.255.255.252 gw 10.0.8.2
route add -net 10.0.0.0 netmask 255.255.255.0 gw 10.0.8.2
```

#### The Minister

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.0.8.1
route add -net 10.0.0.0 netmask 255.255.255.0 gw 10.0.1.2
```

#### The DauntLess

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.0.1.1
```

#### The Intrument

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.0.144.1
route add -net 10.0.128.0 netmask 255.255.255.0 gw 10.0.132.2
route add -net 10.0.129.0 netmask 255.255.255.252 gw 10.0.132.2
route add -net 10.0.130.0 netmask 255.255.254.0 gw 10.0.132.2
route add -net 10.0.136.0 netmask 255.255.255.128 gw 10.0.137.2
route add -net 10.0.136.128 netmask 255.255.255.128 gw 10.0.137.2
```

#### The Firefist

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.0.132.1
route add -net 10.0.129.0 netmask 255.255.255.252 gw 10.0.128.2

```

#### The Queen

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.0.128.1
```

#### The Profound

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.0.137.1
```

#### The Magical

```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 10.0.160.1
```

### Tes Ping

Ping `Guideau` to `The Witch`

Ping  `Guideau` to `google.com`

## Kendala
