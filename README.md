# minikey

Faster BTC MINI private key 22 or 30 generator and supports converting mini key to hex key output.

**Please read all this document before to use the program**

## Download

To clone the repository:

```
git clone https://github.com/8891689/minikey.git
```

don't forget change to the minikey directory

`cd minikey`


## How to build

Just compile:

```
make
```

# usage

This program only have a few possibles arguments

```
./minikey -u 
```

the `-u` option is for generate keys without the byte verification, `u` stand for `unverified` keys,  if you don't specify the keys generated will be always valid with the byte verification.

```
./minikey -s 22
```

the `-s 22` or `-s 30` option is for generate only keys of the specified size, `s` stand for `size`, if you don't specify this option the default value is 22

```
./minikey -m SECUN34uVQKk3UkMBAiTLSoLTUWfwS
```
the `-m` option is for specify a star key this string need to fit in 22 or 30 characters `m` stand for `minikey`, if you don't specify this option the star value is chossen randomly

```
./minikey -a 23456789ABCDEFGHJKLMNPQRSTUVWXYZabcdefghijkmnopqrstuvwxyz
```

the `-a` option is for specify the alphabet to be use I hear that the Series 2 Coin don't have number 1 in his minikey, if you don't specify this optin the defaul alphabet is `123456789ABCDEFGHJKLMNPQRSTUVWXYZabcdefghijkmnopqrstuvwxyz` 

```
./minikey -t 2
```

the `-t` option is for specify the thread number, default number of threads is 1.

```
./minikey -r
```

the `-r` option is to generate just random keys without any special order, `r` stand for `random`. This option is OS dependent and only works with `/dev/urandom`

Of course you can use all the option together to fit you needs.

```
./minikey -d
```
Add -d command to convert miniwifkey into hexadecimal private key output, which can be used with other commands.

```
./minikey -r -d
```
Adding -r can randomly generate a valid miniwif, and adding the -d command can convert the miniwifkey into a hexadecimal private key output.

## Examples
```
./minikey -r
SGPqaH1vT4ZStcBPDS9oGW
SiGvvWU8MKC5byukoMMDJi
ST9Ds8EFjMjo1nH7HbD3Uc
Sekbnn4ZVTAfkYbF1LU8Fe
Svww8NdQFPjDcbKxrobYSg
SNdQFPjDcbKxrobYSgXUaN
SCbsQ56Ex2m2S8YggHWiHK
SpdfVYKn64vAJ8MCpKVpAe
SN1F5fTdMvr7CqkvjLwKJ7
SXHtUdtWgrPYZN23Zh2uy2
SJC85qXyxuouvbris2Shan
SkCqyL5vZe3jw32yT3GnwB
SNpT3wfsfacSqjC9p5MKFL
SiHjpNBitbMGCPgqHkLqbs
SoLS1G5NFrDPMA9Bp351i5
SxNxFFYC2yxF4gW3EUUy4e
SPjm8sv4VkkU8nApRNWCye
SmAJ88eTc78Y8ubWhNW81F

./minikey -r -d
18c8f3acb6896cdfaafebf1c4c2c181e2cb27498e015afddb820851b3e03abc4
c9b38867bc1c1cacf95787a298ba1c60f883ead33df140befb16cea3b9a143bc
b50f57a8aa673241f63ed02a897c40c8e52525de2d3d0c69d774660f5463e387
ca48a08ab9c67f0d9092998febe08bde21fa60770da7001b17e7ac546384df54
fdc06cf3d8606f0ee0abb98a90dff7c1b3e757acc703de1fb1bb7db447439200
987f5c730d16619f8e4c171c321b5c839b9877282ce347b69f45db43528dc576
6103a2612b4099b08e7def3068a6dd79533a6eae5574bbe84a1e6d925362b83d
625160e99445c75d67ba45d3d525f334e4562bdd3c132a89b2007e8113384bc6
2b7929aa9193f5f288baeae5565b9d079e43bf980a0da65c1ea640737b4ee63a
9fbd5be2648fe02a6d1a7ca55a652717f29f59c5d0d0b587ddd03f179e429bbc
19a82f32095462ceb59f4bfded54fca5cbe9579579d0b1b4a05b58f66c1d95be
a4284400eac00b09297af4158872f8ae4e4ac2adc0b84473c5d25c6796554bd9
8da60ac515b515e5d8e7b670ff062af613cc9c271859205fa93c07dd55bc04f0
69019a857eb5dfcb43813de86428b18dc06b3047bd916d94f9bb83b9ec7ea773
ca1e426ac595a9c5122545c5dba1bdab0e891a4d07f12b70382896f2639eb844
dd310692610c19414bcbcb1ad3170025397fc8e830717adbcf6d5756847b332b
408eb2660b84a7b16178f9b0972f9009ed940f4311ab5414d9fa6506f5ebeffd
e929d7684de8082e7d8b876765b6092e8b00a2dbfd56297eb58dd70a45930d59
4e5ba9b063993a3713fef076dbed4d7dbc89624e31dfa4552f215284591d9fd4
41cbbd6fbf7a9beab4d83da0dec23d59204d9a735777997b2b5a0ae9737e381d
```

## Just a key generator


You need redirect the output og this program to brainflayer please check https://github.com/ryancdotorg/brainflayer

./minikey -r -d | ./brainflayer -v -b hash160.blf -f hash160.bin -t priv -x -c uc > result.txt

## Free Code

This code is free of charge, see the licence for more details. https://github.com/albertobsd/minikeyg/blob/main/LICENSE

This is a hobby for me but is still a lot of work.

## ¡Beta!

This version is still a **beta** version, there are a lot of things that can be fail. And absoluly there are some bugs 

# Donations

- BTC: 1Coffee1jV4gB5gaXfHgSHDz9xx9QSECVW
- ETH: 0x6222978c984C22d21b11b5b6b0Dd839C75821069
- DOGE: DKAG4g2HwVFCLzs7YWdgtcsK6v5jym1ErV

All the donations will be use only for two things:

- Buy coffee to develop from dusk till dawn
- Get an affordable desktop computer with decent GPU, not highend, just to start the GPU version of all my programs
