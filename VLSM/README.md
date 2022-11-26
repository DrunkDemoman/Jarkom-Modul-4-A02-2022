## VLSM - Cisco Packet Tracer

### Penggabungan Subnet

Berikut penggabungan subnet dengan metode VLSM

### Penghitungan IP

Berikut pohon subnet yang dibentuk sesuai dengan penggabungan subnet sebelumnya

Didapat tabel data setiap subnet, yakni NID dan Netmask

| Subnet | Network ID |     Netmask     |
| :----: | :--------: | :-------------: |
|   A1   |  10.0.8.0  |  255.255.252.0  |
|   A2   |  10.0.0.0  | 255.255.255.252 |
|   A3   |  10.0.2.0  |  255.255.255.0  |
|   A4   |  10.0.0.4  | 255.255.255.252 |
|   A5   | 10.0.0.64  | 255.255.255.192 |
|   A6   |  10.0.0.8  | 255.255.255.252 |
|   A7   | 10.0.0.12  | 255.255.255.252 |
|   A8   | 10.0.0.128 | 255.255.255.128 |
|   A9   | 10.0.0.16  | 255.255.255.252 |
|  A10   |  10.0.3.0  |  255.255.255.0  |
|  A11   | 10.0.0.20  | 255.255.255.252 |
|  A12   |  10.0.4.0  |  255.255.254.0  |
|  A13   | 10.0.0.24  | 255.255.255.252 |
|  A14   |  10.0.1.0  | 255.255.255.128 |
|  A15   | 10.0.1.128 | 255.255.255.128 |
|  A16   | 10.0.0.28  | 255.255.255.252 |
|  A17   |  10.0.6.0  |  255.255.254.0  |
|  A18   | 10.0.0.32  | 255.255.255.252 |




### Topologi CPT

### Subnetting

Setelah dihitung ip untuk tiap subnet, maka sekarang saatnya mengatur ip pada tiap router, client dan server. Setiap interface node diatur sesuai ip yang telah dihitung melalui GUI aplikasi.

#### The Resonance

```
FastEthernet0/0 
FastEthernet0/1 10.0.0.29 255.255.255.252
Ethernet0/3/0 10.0.0.9 255.255.255.252
FastEthernet1/0 10.0.0.33 255.255.255.252
FastEthernet1/1 10.0.0.13 255.255.255.252
```

#### The Order

```
FastEthernet0/0 10.0.0.10 255.255.255.252
FastEthernet0/1 10.0.0.65 255.255.255.192
FastEthernet1/0 10.0.0.5 255.255.255.252
FastEthernet1/1
```

#### The Minister

```
FastEthernet0/0 10.0.0.6 255.255.255.252
FastEthernet0/1 10.0.8.1 255.255.252.0
FastEthernet1/0 10.0.0.1 255.255.255.252
FastEthernet1/1
```

#### The DauntLess

```
FastEthernet0/0 10.0.0.2 255.255.255.252
FastEthernet0/1 10.0.2.1 255.255.255.0
```

#### The Intrument

```
FastEthernet0/0 10.0.0.14 255.255.255.252
FastEthernet0/1 10.0.0.129 255.255.255.128
FastEthernet1/0 10.0.0.17 255.255.255.252
FastEthernet1/1 10.0.0.25 255.255.255.252
```

#### The Firefist

```
FastEthernet0/0 10.0.0.18 255.255.255.252
FastEthernet0/1 10.0.3.1 255.255.255.0
FastEthernet1/0 10.0.4.1 255.255.254.0
FastEthernet1/1
```

#### The Queen

```
FastEthernet0/0 10.0.3.2 255.255.255.0
FastEthernet0/1 10.0.0.21 255.255.255.252
```

#### The Profound

```
FastEthernet0/0 10.0.0.26 255.255.255.252
FastEthernet0/1 10.0.1.129 255.255.255.128
FastEthernet1/0 10.0.1.1 255.255.255.128
FastEthernet1/1
```

#### The Magical

```
FastEthernet0/0 10.0.0.30 255.255.255.252
FastEthernet0/1 10.0.6.1 255.255.254.0
FastEthernet1/0
FastEthernet1/1
```

#### Johan

```
FastEthernet0 10.0.2.2 255.255.255.0
Default Gateway 10.0.2.1
```

#### Phanora

```
FastEthernet0 10.0.2.3 255.255.255.0
Default Gateway 10.0.2.1
```

#### Guideau

```
FastEthernet0 10.0.8.2 255.255.252.0
Default Gateway 10.0.8.1
```

#### Ashaf

```
FastEthernet0 10.0.0.66 255.255.255.192
Default Gateway 10.0.0.65
```

#### The Witch

```
FastEthernet0 10.0.0.22 255.255.255.252
Default Gateway 10.0.0.21
```

#### Keith

```
FastEthernet0 10.0.3.3 255.255.255.0
Default Gateway 10.0.3.1
```

#### Oakleave

```
FastEthernet0 10.0.4.2 255.255.254.0
Default Gateway 10.0.4.1
```

#### Matt Cugat

```
FastEthernet0 10.0.0.130 255.255.255.128
Default Gateway 10.0.0.129
```

#### Helga

```
FastEthernet0 10.0.1.2 255.255.255.128
Default Gateway 10.0.1.1
```

#### Spendrow

```
FastEthernet0 10.0.1.130 255.255.255.128
Default Gateway 10.0.1.129
```

#### Corvekt

```
FastEthernet0 10.0.6.3 255.255.254.0
Default Gateway 10.0.6.1
```

#### Haines

```
FastEthernet0 10.0.6.2 255.255.254.0
Default Gateway 10.0.6.1
```

#### The Beast

```
FastEthernet0 10.0.0.34 255.255.255.252
Default Gateway 10.0.0.33
```

### Routing

Setelah pengaturan IP selesai, dilanjutkan dengan routing pada router-router seperti berikut.

#### The Resonance

```
ip route 10.0.6.0 255.255.254.0 10.0.0.30
ip route 10.0.3.0 255.255.255.0 10.0.0.14
ip route 10.0.0.20 255.255.255.252 10.0.0.14
ip route 10.0.0.128 255.255.255.128 10.0.0.14
ip route 10.0.4.0 255.255.254.0 10.0.0.14
ip route 10.0.0.16 255.255.255.252 10.0.0.14
ip route 10.0.0.24 255.255.255.252 10.0.0.14
ip route 10.0.1.128 255.255.255.128 10.0.0.14
ip route 10.0.1.0 255.255.255.128 10.0.0.14
ip route 10.0.0.64 255.255.255.192 10.0.0.10
ip route 10.0.8.0 255.255.252.0 10.0.0.10
ip route 10.0.2.0 255.255.255.0 10.0.0.10
ip route 10.0.0.0 255.255.255.252 10.0.0.10
ip route 10.0.0.4 255.255.255.252 10.0.0.10
```

#### The Order

```
ip route 0.0.0.0 0.0.0.0 10.0.0.9
ip route 10.0.8.0 255.255.252.0 10.0.0.6
ip route 10.0.2.0 255.255.255.0 10.0.0.6
ip route 10.0.0.0 255.255.255.252 10.0.0.6
ip route 10.0.0.4 255.255.254.252 10.0.0.6
```

#### The Minister

```
ip route 0.0.0.0 0.0.0.0 10.0.0.5
ip route 10.0.2.0 255.255.255.0 10.0.0.2
```

#### The DauntLess

```
ip route 0.0.0.0 0.0.0.0 10.0.0.1
```

#### The Intrument

```
ip route 0.0.0.0 0.0.0.0 10.0.0.13
ip route 10.0.3.0 255.255.255.0 10.0.0.18
ip route 10.0.0.20 255.255.255.252 10.0.0.18
ip route 10.0.4.0 255.255.254.0 10.0.0.18
ip route 10.0.0.16 255.255.255.252 10.0.0.18
ip route 10.0.0.24 255.255.255.252 10.0.0.26
ip route 10.0.1.128 255.255.255.128 10.0.0.26
ip route 10.0.1.0 255.255.255.128 10.0.0.26
```

#### The Firefist

```
ip route 0.0.0.0 0.0.0.0 10.0.0.17
ip route 10.0.0.20 255.255.255.252 10.0.3.2
```

#### The Queen

```
ip route 0.0.0.0 0.0.0.0 10.0.3.1
```

#### The Profound

```
ip route 0.0.0.0 0.0.0.0 10.0.0.25
```

#### The Magical

```
ip route 0.0.0.0 0.0.0.0 10.0.0.29
```

### Tes Ping

1. Ping `The Dauntless` to `The Profound`
    ![Ping `The Dauntless` to `The Profound`](img/ping-1.png)

2. Ping `Guideau` to `The Firefist`
    ![Ping `Guideau` to `The Firefist`](img/ping-2.png)

3. Ping `The Witch` to `The Order`
    ![Ping `The Witch` to `The Order`](img/ping-3.png)

4. Ping `Helga` to `Phanora`
    ![Ping `Helga` to `Phanora`](img/ping-4.png)

5. Ping `The Beast` to `The Instrument`
    ![Ping `The Beast` to `The Instrument`](img/ping-5.png)

6. Ping `The Witch` to `The Beast`
    ![Ping `The Witch` to `The Beast`](img/ping-6.png)

7. Ping `Matt Cugatt` to `Corvekt`
    ![Ping `Matt Cugatt` to `Corvekt`](img/ping-7.png)

8. Ping `The Beast` to `Spendrow`
    ![Ping `The Beast` to `Spendrow`](img/ping-8.png)

9. Ping `Haines` to `Keith`
    ![Ping `Haines` to `Keith`](img/ping-9.png)

10. Ping `Johan` to `Queen`
    ![Ping `Johan` to `Queen`](img/ping-10.png)

11. Ping `Oakleave` to `The Witch`
    ![Ping `Oakleave` to `The Witch`](img/ping-11.png)

12. Ping `Ashaf` to `The Resonance`
    ![Ping `Ashaf` to `The Resonance`](img/ping-12.png)

13. Ping `Corvekt` to `The Minister`
    ![Ping `Corvekt` to `The Minister`](img/ping-13.png)

14. Ping `Guideau` to `Helga`
    ![Ping `Guideau` to `Helga`](img/ping-14.png)

15. Ping `Ashaf` to `The Queen`
    ![Ping `Ashaf` to `The Queen`](img/ping-15.png)


## Kendala