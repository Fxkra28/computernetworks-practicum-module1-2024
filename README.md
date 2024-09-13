[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/8b_y5Av8)
| Name           | NRP        | Kelas     |
| ---            | ---        | ----------|
| Omar Shinichi Ghifari | 5025231004 | Jaringan Komputer (IUP) |
| Muiz Surya Fata | 5025231005 | Jaringan Komputer (IUP) |

## Task 1

> a. Berapa banyak packet yang terekam pada file pcapng?

> _a. How many packets are recorded in the pcapng file?_

**Answer:**

- Flag

  `JARKOM24{K4mu_K3r3n_C6PUUQH8IDI37ADBCM8M3DJZ6WYRJP0xL4ugh9wezdo17j94yqejwdr0eaa0}`

- Filter expression

  We didin't put any filter.
  
- Explanation

  Just look at the bottom of the WIreshark, it shows the packets that are recorded in the pcapng file.

- Output result

  ![image](https://github.com/user-attachments/assets/1ab8de79-d5cd-4ae8-8107-71c4fc072ba7)


<br>
<br>

> b. Ada berapa jenis protocol yang terekam pada traffic

> _b. How many types of protocols are recorded in the traffic?_

**Answer:**

- Flag

  `JARKOM24{K4mu_K3r3n_C6PUUQH8IDI37ADBCM8M3DJZ6WYRJP0xL4ugh9wezdo17j94yqejwdr0eaa0}`

- Filter expression

  We didin't use any filters.
  
- Explanation

  Head to "Statistic" bar, then select "Protocol Hierarchy".

- Output result

  We didin't documented the result, but we do keep the wsl output. Here's the wsl output:
```
akira@Unknown:~$ nc 165.22.53.139 45000
Choose your language [1/2]:
[1] English
[2] Bahasa Indonesia
> 2
Berapa banyak packet yang terekam pada file pcapng?
> 1089
Ada berapa jenis protocol yang terekam pada traffic?
> 4500
Incorrect Answer
Berapa banyak packet yang terekam pada file pcapng?
> 1089
Ada berapa jenis protocol yang terekam pada traffic?
> 4
sebutkan secara berurutan berdasarkan alfabet menurun dengan koma sebagai separator dan dalam bentuk uppercase
contoh: PROTOCOL1,PROTOCOL2
> TCP,SSDP,MDNS,HTTP
Incorrect Answer
Berapa banyak packet yang terekam pada file pcapng?
> 1089
Ada berapa jenis protocol yang terekam pada traffic?
> 4
sebutkan secara berurutan berdasarkan alfabet menurun dengan koma sebagai separator dan dalam bentuk uppercase
contoh: PROTOCOL1,PROTOCOL2
> HTTP,MDNS,SSDP,TCP
Correct! Here is your flag: JARKOM24{K4mu_K3r3n_C6PUUQH8IDI37ADBCM8M3DJZ6WYRJP0xL4ugh9wezdo17j94yqejwdr0eaa0}
```


<br>
<br>

> c. Sebutkan secara berurutan berdasarkan alfabet menurun dengan koma sebagai separator, contoh: protocol1,protocol2

> _c. List the protocols in descending alphabetical order, separated by commas. Example: protocol1,protocol2_

**Answer:**

- Flag

  `JARKOM24{K4mu_K3r3n_C6PUUQH8IDI37ADBCM8M3DJZ6WYRJP0xL4ugh9wezdo17j94yqejwdr0eaa0}`

- Filter expression

  We didin't use any filters.
  
- Explanation

 We detect the protocols manually.

- Output result
We didin't documented the result, but we do keep the wsl output. Here's the wsl output:
```
akira@Unknown:~$ nc 165.22.53.139 45000
Choose your language [1/2]:
[1] English
[2] Bahasa Indonesia
> 2
Berapa banyak packet yang terekam pada file pcapng?
> 1089
Ada berapa jenis protocol yang terekam pada traffic?
> 4500
Incorrect Answer
Berapa banyak packet yang terekam pada file pcapng?
> 1089
Ada berapa jenis protocol yang terekam pada traffic?
> 4
sebutkan secara berurutan berdasarkan alfabet menurun dengan koma sebagai separator dan dalam bentuk uppercase
contoh: PROTOCOL1,PROTOCOL2
> TCP,SSDP,MDNS,HTTP
Incorrect Answer
Berapa banyak packet yang terekam pada file pcapng?
> 1089
Ada berapa jenis protocol yang terekam pada traffic?
> 4
sebutkan secara berurutan berdasarkan alfabet menurun dengan koma sebagai separator dan dalam bentuk uppercase
contoh: PROTOCOL1,PROTOCOL2
> HTTP,MDNS,SSDP,TCP
Correct! Here is your flag: JARKOM24{K4mu_K3r3n_C6PUUQH8IDI37ADBCM8M3DJZ6WYRJP0xL4ugh9wezdo17j94yqejwdr0eaa0}
```


## Task 2

> a. Berapa banyak packet berbasis TCP yang memiliki flag [RST, ACK]

> _a. How many TCP based packets have the flags [RST, ACK]?_

**Answer:**

- Flag

  `JARKOM24{W0w_4nother_Sh0t_KRNEMVCPFDH0mptyseqipnvpgwxbrsqnowdnM4r151974754484178268392}`

- Filter expression

  `tcp.flags.ack == 1 && tcp.flags.reset == 1`
  
- Explanation

  Simply set the `tcp.flags.ack` and `tcp.flags.reset` value to one, so it will filters ack and rst

- Output result

  I didin't documented the output on the wireshark, but here's the output on the wsl:
 ```akira@Unknown:~$ nc 165.22.53.139 46000
Choose your language [1/2]:
[1] English
[2] Bahasa Indonesia
> 2
Berapa banyak packet berbasis TCP yang memiliki flag [RST, ACK]?
> 411
Berapa banyak packet berbasis TCP yang hanya memiliki flag [SYN]?
> 413
Incorrect Answer
Berapa banyak packet berbasis TCP yang memiliki flag [RST, ACK]?
> 411
Berapa banyak packet berbasis TCP yang hanya memiliki flag [SYN]?
> 412
Berapa banyak packet berbasis TCP yang memiliki flag ack, tapi tidak memiliki syn, dan tidak memiliki rst
> 217
Correct! Here is your flag: JARKOM24{W0w_4nother_Sh0t_KRNEMVCPFDH0mptyseqipnvpgwxbrsqnowdnM4r151974754484178268392}
```


<br>
<br>

> b. How many TCP based packets have only the [SYN] flag?

> _b. How many TCP based packets have only the [SYN] flag?_

**Answer:**

- Flag

  `JARKOM24{W0w_4nother_Sh0t_KRNEMVCPFDH0mptyseqipnvpgwxbrsqnowdnM4r151974754484178268392}`

- Filter expression

  `Put your filter expression here (if any)`
  
- Explanation

  For this one, We tried the same thing as the previous one, but we set the `tcpflags.syn == 1` and `tcp.flags.ack == 0`. So it will only displays TCP based packets that have only the [SYN] flag.

- Output result

  I didin't documented the output on the wireshark, but here's the output on the wsl:
 ```akira@Unknown:~$ nc 165.22.53.139 46000
Choose your language [1/2]:
[1] English
[2] Bahasa Indonesia
> 2
Berapa banyak packet berbasis TCP yang memiliki flag [RST, ACK]?
> 411
Berapa banyak packet berbasis TCP yang hanya memiliki flag [SYN]?
> 413
Incorrect Answer
Berapa banyak packet berbasis TCP yang memiliki flag [RST, ACK]?
> 411
Berapa banyak packet berbasis TCP yang hanya memiliki flag [SYN]?
> 412
Berapa banyak packet berbasis TCP yang memiliki flag ack, tapi tidak memiliki syn, dan tidak memiliki rst
> 217
Correct! Here is your flag: JARKOM24{W0w_4nother_Sh0t_KRNEMVCPFDH0mptyseqipnvpgwxbrsqnowdnM4r151974754484178268392}
```


<br>
<br>

> c. How many TCP based packets have the ACK flag but do not have SYN or RST?

> _c. How many TCP based packets have the ACK flag but do not have SYN or RST?_

**Answer:**

- Flag

  `JARKOM24{W0w_4nother_Sh0t_KRNEMVCPFDH0mptyseqipnvpgwxbrsqnowdnM4r151974754484178268392}`

- Filter expression

  `tcp.flags.ack==1 && tcpflags.syn==0&&tcp.flags.reset==0`
  
- Explanation

  Just like previous, 1 means true and 0 means false. So it will only filters the one we set 1 as it's value.

- Output result

  I didin't documented the output on the wireshark, but here's the output on the wsl:
 ```akira@Unknown:~$ nc 165.22.53.139 46000
Choose your language [1/2]:
[1] English
[2] Bahasa Indonesia
> 2
Berapa banyak packet berbasis TCP yang memiliki flag [RST, ACK]?
> 411
Berapa banyak packet berbasis TCP yang hanya memiliki flag [SYN]?
> 413
Incorrect Answer
Berapa banyak packet berbasis TCP yang memiliki flag [RST, ACK]?
> 411
Berapa banyak packet berbasis TCP yang hanya memiliki flag [SYN]?
> 412
Berapa banyak packet berbasis TCP yang memiliki flag ack, tapi tidak memiliki syn, dan tidak memiliki rst
> 217
Correct! Here is your flag: JARKOM24{W0w_4nother_Sh0t_KRNEMVCPFDH0mptyseqipnvpgwxbrsqnowdnM4r151974754484178268392}
```


<br>
<br>

## Task 3

> a. Pada port berapa server http terbuka?

> _a. On which port is the HTTP server open?_


**Answer:**

- Flag

  `JARKOM24{Y0u_4r3_4_g00d_4nalyz3r_7W1RPL1tsew25m80xwj11jmaonbntzq}`

- Filter expression

  `http`
  
- Explanation

  Simply put `http` on the filter tab. It'll filter any HTTP ports.

- Output result

  We didin't documented the result, but we do keep the wsl output. Here's the wsl output:
```  
akira@Unknown:~$ nc 165.22.53.139 47000
Choose your language [1/2]:
[1] English
[2] Bahasa Indonesia
> 2
Pada port berapa server http terbuka?
> 9282
Berapa byte file response yang dikirim dari server?
> 427
Berapa jumlah file yang terdapat pada server?
> 2
Incorrect Answer
Pada port berapa server http terbuka?
> 9282
Berapa byte file response yang dikirim dari server?
> 427
Berapa jumlah file yang terdapat pada server?
> 1
Incorrect Answer
Pada port berapa server http terbuka?
> 9282
Berapa byte file response yang dikirim dari server?
> 427
Berapa jumlah file yang terdapat pada server?
> 4
sebutkan nama file secara berurutan berdasarkan alfabet menurun dengan koma sebagai separator, contoh: file1,file2
> file.pdf,hello.html,lion.jpg,present.pptx
Correct! Here is your flag: JARKOM24{Y0u_4r3_4_g00d_4nalyz3r_7W1RPL1tsew25m80xwj11jmaonbntzq}
```

<br>
<br>

> b. Berapa byte file response yang dikirim dari server

> _b. How many bytes of file response are sent from the server?_


**Answer:**

- Flag

  `JARKOM24{Y0u_4r3_4_g00d_4nalyz3r_7W1RPL1tsew25m80xwj11jmaonbntzq}`

- Filter expression

  We didin't filter anything
  
- Explanation

  When filtering the server, you should seen some status one the bottom left side of the wireshark. It shows the size of the file response that were sent from the server. It should be something like this:
![image](https://github.com/user-attachments/assets/0d20e9c4-3ed4-45be-936b-66951ba41540)
(this is not the actual documentation from the answer, just an example)


- Output result

    We didin't documented the result, but we do keep the wsl output. Here's the wsl output:
```  
akira@Unknown:~$ nc 165.22.53.139 47000
Choose your language [1/2]:
[1] English
[2] Bahasa Indonesia
> 2
Pada port berapa server http terbuka?
> 9282
Berapa byte file response yang dikirim dari server?
> 427
Berapa jumlah file yang terdapat pada server?
> 2
Incorrect Answer
Pada port berapa server http terbuka?
> 9282
Berapa byte file response yang dikirim dari server?
> 427
Berapa jumlah file yang terdapat pada server?
> 1
Incorrect Answer
Pada port berapa server http terbuka?
> 9282
Berapa byte file response yang dikirim dari server?
> 427
Berapa jumlah file yang terdapat pada server?
> 4
sebutkan nama file secara berurutan berdasarkan alfabet menurun dengan koma sebagai separator, contoh: file1,file2
> file.pdf,hello.html,lion.jpg,present.pptx
Correct! Here is your flag: JARKOM24{Y0u_4r3_4_g00d_4nalyz3r_7W1RPL1tsew25m80xwj11jmaonbntzq}
```


<br>
<br>

> c. Berapa jumlah file yang terdapat pada server?

> _c. How many files are there on the server?_


**Answer:**

- Flag

  `JARKOM24{Y0u_4r3_4_g00d_4nalyz3r_7W1RPL1tsew25m80xwj11jmaonbntzq}`

- Filter expression

  We didin't use any filters.
  
- Explanation

  We right clicked the tcp, and select "Follow TCP Stream". And it shows the files that are exist on the server. It should shows something like this:
![3-2 1](https://github.com/user-attachments/assets/97634e2c-d277-4633-87dc-eec4aabdf052)


- Output result

    We didin't documented the result, but we do keep the wsl output. Here's the wsl output:
```  
akira@Unknown:~$ nc 165.22.53.139 47000
Choose your language [1/2]:
[1] English
[2] Bahasa Indonesia
> 2
Pada port berapa server http terbuka?
> 9282
Berapa byte file response yang dikirim dari server?
> 427
Berapa jumlah file yang terdapat pada server?
> 2
Incorrect Answer
Pada port berapa server http terbuka?
> 9282
Berapa byte file response yang dikirim dari server?
> 427
Berapa jumlah file yang terdapat pada server?
> 1
Incorrect Answer
Pada port berapa server http terbuka?
> 9282
Berapa byte file response yang dikirim dari server?
> 427
Berapa jumlah file yang terdapat pada server?
> 4
sebutkan nama file secara berurutan berdasarkan alfabet menurun dengan koma sebagai separator, contoh: file1,file2
> file.pdf,hello.html,lion.jpg,present.pptx
Correct! Here is your flag: JARKOM24{Y0u_4r3_4_g00d_4nalyz3r_7W1RPL1tsew25m80xwj11jmaonbntzq}
```


<br>
<br>

> d. Sebutkan nama file secara berurutan berdasarkan alfabet menurun dengan koma sebagai separator, contoh: file1,file2

> _d. List the filenames in descending alphabetical order, separated by commas. Example: file1,file2_


**Answer:**

- Flag

  `Put your flag in here`

- Filter expression

  We didin't filter anything.
  
- Explanation

  From the previous section, we can detect the file names

- Output result

     We didin't documented the result, but we do keep the wsl output. Here's the wsl output:
```  
akira@Unknown:~$ nc 165.22.53.139 47000
Choose your language [1/2]:
[1] English
[2] Bahasa Indonesia
> 2
Pada port berapa server http terbuka?
> 9282
Berapa byte file response yang dikirim dari server?
> 427
Berapa jumlah file yang terdapat pada server?
> 2
Incorrect Answer
Pada port berapa server http terbuka?
> 9282
Berapa byte file response yang dikirim dari server?
> 427
Berapa jumlah file yang terdapat pada server?
> 1
Incorrect Answer
Pada port berapa server http terbuka?
> 9282
Berapa byte file response yang dikirim dari server?
> 427
Berapa jumlah file yang terdapat pada server?
> 4
sebutkan nama file secara berurutan berdasarkan alfabet menurun dengan koma sebagai separator, contoh: file1,file2
> file.pdf,hello.html,lion.jpg,present.pptx
Correct! Here is your flag: JARKOM24{Y0u_4r3_4_g00d_4nalyz3r_7W1RPL1tsew25m80xwj11jmaonbntzq}
```


<br>
<br>

## Task 4

> Protokol apa yang paling banyak terdapat di file hasil capture traffic?

> _Which protocol is the most frequent in the traffic capture file?_


**Answer:**

- Flag

  `Put your flag in here`

- Filter expression

  `Put your filter expression here (if any)`
  
- Explanation

  `Describe how you solve the questions`

- Output result

  `Attach the screenshot of the output result of your flag`

<br>
<br>

## Task 5

> Berdasarkan hasil bruteforce, apa user yang tepat dari hasil bruteforce?

> _Based on the brute force results, what is the correct username?_


**Answer:**

- Flag

  `Put your flag in here`

- Filter expression

  `Put your filter expression here (if any)`
  
- Explanation

  `Describe how you solve the questions`

- Output result

  `Attach the screenshot of the output result of your flag`

<br>
<br>

## Task 6

> Apa password yang tepat?

> _What is the correct password?_


**Answer:**

- Flag

  `JARKOM24{h1s_fr1end_1s_g3d4g3d1g3d4g3d03_F4J71VNDBCyksnUmfxddstcoaeB4Sur1XMYNNXSYMB}`

- Filter expression

  `tcp contains “successful”`
  
- Explanation

  - So we thinking that to find the successful passwords, there is must been successful status when we try to login in the website, so we used filter expressions `tcp` that contained keyword “successful”, and so we found one line packet only that contain that word.
  ![image](https://github.com/user-attachments/assets/ff31b44e-0986-40a0-a672-b75d6ee63ae7)

- Output result
```
akira@Unknown:~$ nc 165.22.53.139 50000

Choose your language [1/2]:
[1] English
[2] Bahasa Indonesia

2

Apa password yang tepat dari hasil bruteforce?
gedagedigedagedao
Incorrect Answer
Apa password yang tepat dari hasil bruteforce?
gedagedigedagedoe
Correct! Here is your flag: JARKOM24{h1s_fr1end_1s_g3d4g3d1g3d4g3d03_F4J71VNDBCyksnUmfxddstcoaeB4Sur1XMYNNXSYMB}
```

<br>
<br>

## Task 7

> Pada port berapa telnet yang bisa diakses?

> _On which port is Telnet accessible?_


**Answer:**

- Flag

  `JARKOM24{Gr34t_Sn1ff3r_QFRU5yksnUmli1qgqa5gaT3t0tJKsGbjzNib}`

- Filter expression

  `There is no filter expressions`
  
- Explanation

  - So we could check and clicked the line packet, and we could saw from this sections
 ![image](https://github.com/user-attachments/assets/66691d15-c728-4ee9-b8b2-10f5b0d6ee45)
  - From this image, we can see the src port (Where the file can accessed) which is Port 2423

- Output result

```
akira@Unknown:~$ nc 165.22.53.139 51000
Choose your language [1/2]:
[1] English
[2] Bahasa Indonesia
>
Pada port berapa telnet yang bisa diakses?
> 50214
Incorrect Answer
Pada port berapa telnet yang bisa diakses?
> 2423
Correct! Here is your flag: JARKOM24{Gr34t_Sn1ff3r_QFRU5yksnUmli1qgqa5gaT3t0tJKsGbjzNib}
```

<br>
<br>

## Task 8

> Ada berapa file di dalam server?

> _How many files are on the server?_


**Answer:**

- Flag

  `JARKOM24{P4ck3t_4n4lyz3r_nxYhAV7fPi3112ihhctmiuhjS1SVYSNNKVSJR}`

- Filter expression

  `tcp contains “FOUND”`
  
- Explanation
  - So we wanted to figure out file that can be founded first, we used “http/tcp” filter. The packets contains 32 files, but there is no packets on it.
  - And after that, we tried to use `tcp contains “found”` and `tcp contains “Found”` based on our perceptions towards the files that detected by packets, but there is no results, until we use `tcp contains “FOUND”`, we found 7 lines of packets that contained that keywords.
![image](https://github.com/user-attachments/assets/1293dbbb-4ccb-408f-8cf1-9e06536d28e2)
  - we tried to answer 6 files that contained in, perhaps that the upmost line packets didn’t necessary, but answer was incorrect. Then we tried to answered 7 to make it sure that the upmost line packets are categorized as a file too. Then it’s correct!

- Output result
```
akira@Unknown:~$ nc 165.22.53.139 52000
Choose your language [1/2]:
[1] English
[2] Bahasa Indonesia
> 2
Ada berapa file di dalam server?
> 30
Incorrect Answer
Ada berapa file di dalam server?
> 32
Incorrect Answer
Ada berapa file di dalam server?
> 6
Incorrect Answer
Ada berapa file di dalam server?
> 7
Correct! Here is your flag: JARKOM24{P4ck3t_4n4lyz3r_nxYhAV7fPi3112ihhctmiuhjS1SVYSNNKVSJR}
```

<br>
<br>

## Task 9

> Apa nama file yang dieksekusi oleh user?

> _What is the name of the file executed by the user?_


**Answer:**

- Flag
  
`JARKOM24{333ch000_us3r_942484903812fLyaVLocGld33d9EZM3LPIKR}`

- Filter expression

  `tcp contains “user”`
  
- Explanation
    - So first of all, we want to filter the activity by finding which one is contained user (the one who do the execute command). And then we find 2 lines :
![image](https://github.com/user-attachments/assets/ef40a8f9-20af-486b-9b25-1861c3588a41)
    - And we clicked the second packets, and then here’s one of many text in the packets content :
 ![image](https://github.com/user-attachments/assets/5b2689f2-0329-4445-b374-9a3dfecb0379)
    - We owe apologies for the unnecessary numerous line of our output results due to baited to the contents of the second packages. We thought the files that being executed by the users, so we answered lots of many files that included output after executed `ls` command.
    - But we just realized that the files included after `ls` command was being executed automatically by function, with that we don’t have idea, so we try bruteforce, once again, we really sorry for our silly mistakes.
    - So we tried to worked on number 10 first, when the questions was the output of the file with base64 format, suddenly we tried to found the base64 format, and we found it! :
![image](https://github.com/user-attachments/assets/10c6a527-b8e9-48b8-ba61-5f26d90e9b98)
    - At first sight, we clicked all of the lines, including `stories$`, but after that, we clicked again for the second time, and we realizes that after the `==` sign is not the part of the output. Instead it was the telnet identifier.
    - With this clue, we try to scrolled up and finding that before these output, there is text called `echo`
 ![image](https://github.com/user-attachments/assets/e04297cb-92cc-4709-a5e6-cca934fff30e)
    - At that time we didn’t have idea and clue what the answer was, so we tried to answered `echo` instead, and it worked!
    - So to sum it up, we tried to open question number 10 first to got the clue, and then we scrolled up before the Base64 output format, and we tried to answer `echo`, and luckily got it right. 

- Output result

```
akira@Unknown:~$ nc 165.22.53.139 53000
Choose your language [1/2]:
[1] English
[2] Bahasa Indonesia
> 2
apa nama file yang dieksekusi oleh user?
> akra.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> akra
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> de07.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> manto.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> 01;32mdjumanto.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> jumanto.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> 32mdjumanto.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> mdjumanto.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> mchakra.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> jungoo.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> dongsoo.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> chakra.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> stories
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> junggoo.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> stories
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> chakra.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> charka.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> JUMANTO.TXT
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> gedagedigedagedao.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> user.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> ubuntu.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> ubuntu
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> telnet
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> junggoo.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> mgendra.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> gendra.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> glugglug.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> ondongsoo.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> vinorian.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> u
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> u.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> shooamii.txt
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> sleep
Incorrect Answer
apa nama file yang dieksekusi oleh user?
> echo
Correct! Here is your flag: JARKOM24{333ch000_us3r_942484903812fLyaVLocGld33d9EZM3LPIKR}
```

<br>
<br>

## Task 10

> Apa output dari file dalam bentuk base64 decode?

> _What is the output of the file in base64-decoded form?_


**Answer:**

- Flag

  `JARKOM24{tH4ts_1t_w3ll_d0n3_64176602881337uztrp8cm1p1231421421HMFLL8L8LBAOVM8}`

- Filter expression

   `tcp contains “user”` 
  
- Explanation
   
    - So after we answered number 9, we already got the output file when we tried to found the hint/clue. After that, we copy the output and convert it into base 64 decoder websites.
![image](https://github.com/user-attachments/assets/c63c89fe-c781-49d0-9c2b-f5448151104a)
  
    - Then we copy the decode results, and then we paste to the questions, and got it right.
 
- Output result
```
akira@Unknown:~$ nc 165.22.53.139 54000
Choose your language [1/2]:
[1] English
[2] Bahasa Indonesia
> 2
apa output dari file dalam bentuk base64 decode? [Gunakan tools atau command di linux]
> Djumanto mencoba menenangkan kuda kesayangannya, Glukgluk, yang tiba-tiba melompat-lompat di kandang sambil berteriak, 'Tenang, Glukgluk, ini cuma payung, bukan alien!'
Correct! Here is your flag: JARKOM24{tH4ts_1t_w3ll_d0n3_64176602881337uztrp8cm1p1231421421HMFLL8L8LBAOVM8}
```

<br>
<br>

## Summary
So to sum it up, there are 7 General Steps to finish the tasks:
1. We tried to log in into the `165.22.53.139` link websites that provided by lecture assitants.
2. Then we open the flag that provided and open gdrive the link.
![image](https://github.com/user-attachments/assets/1fe42c31-3f0f-467d-bf2a-f4e784b6bd3c)
3. We download the packets, and after the downloaded have been finished, we open the packets.
4. Opening the WSL, and execute command `nc 165.22.53.139 [Port Number]` And we try to answer the questions.
5. To help Answer the questions, we can filter the packets in the wireshark app.
6. To see the content of the packets, we can double-click our mouse/touchpad, click follow, and click tcp/http stream.
7. If we already answered the questions, we could got the flag and submit it to the websites before.

## Problems
- Maybe our problems were the website's responsiveness. We hope that if we use the same websites, please divide into different time sessions, to make sure the website can handle the client (team's activity) traffic.
