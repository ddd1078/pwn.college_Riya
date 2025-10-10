# Processes and Jobs

## 1. Listing Processes

### Solve
**Flag** `pwn.college{0DOOzvaUWHdzLRIm5nV-q7o6Srr.QX4MDO0wCMwEzNzEzW}`

```bash
hacker@processes~listing-processes:~$ ps -efww
UID          PID    PPID  C STIME TTY          TIME CMD
root           1       0  0 16:48 ?        00:00:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-workspace/bin/dojo-init /run/dojo/bin/sleep 6h
root           7       1  0 16:48 ?        00:00:00 /run/dojo/bin/sleep 6h
root         132       1  0 16:48 ?        00:00:00 /challenge/9814-run-30433
root         135     132  0 16:48 ?        00:00:00 sleep 6h
hacker       137       0  0 16:57 pts/0    00:00:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-interactive-5.2p37/bin/bash /run/dojo/bin/ssh-entrypoint
hacker       143     137  0 16:57 pts/0    00:00:00 /run/dojo/bin/bash --login
hacker       152     143  0 16:58 pts/0    00:00:00 ps -efww
hacker@processes~listing-processes:~$ ps -efww | grep challenge
root         132       1  0 16:48 ?        00:00:00 /challenge/9814-run-30433
hacker       154     143  0 16:59 pts/0    00:00:00 grep --color=auto challenge
hacker@processes~listing-processes:~$ /challenge/9814-run-3043
bash: /challenge/9814-run-3043: No such file or directory
hacker@processes~listing-processes:~$ /challenge/9814-run-30433
Yahaha, you found me! Here is your flag:
pwn.college{0DOOzvaUWHdzLRIm5nV-q7o6Srr.QX4MDO0wCMwEzNzEzW}
```

### New Learnings


## 2. Killing Processes

### Solve
**Flag** `pwn.college{MErYb5uXxvk6LlQyxCu8e1xBmm7.QXyQDO0wCMwEzNzEzW}`

```bash
hacker@processes~killing-processes:~$ ps -efww | grep dont_run
hacker       136     135  0 17:04 ?        00:00:00 /challenge/dont_run
hacker       155     145  0 17:05 pts/0    00:00:00 grep --color=auto dont_run
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ ps -efww | grep dont_run
hacker       157     145  0 17:06 pts/0    00:00:00 grep --color=auto dont_run
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{MErYb5uXxvk6LlQyxCu8e1xBmm7.QXyQDO0wCMwEzNzEzW}
```

### New Learnings

## 3. Interrupting Processes

### Solve
**Flag**  `pwn.college{w_6zdjIJv7RGorQCFBYD2Mhm8xJ.QXzQDO0wCMwEzNzEzW}`

```bash
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember,
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{w_6zdjIJv7RGorQCFBYD2Mhm8xJ.QXzQDO0wCMwEzNzEzW}
```

### New Learnings

## 4. Killing Misbehaving Processes

### Solve
**Flag** `pwn.college{IRFU-2_jvE2vPHON7hRkn-cfjcK.0FNzMDOxwCMwEzNzEzW}`

```bash
hacker@processes~killing-misbehaving-processes:~$ cat /tmp/flag_fifo & /challenge/run
[1] 165
pwn.college{OHqtkpLuX-szsleDj.hccpfZ2M.4ALHgtPBRKPmDBEd9mxR}
pwn.college{LXKsCUpEwSJWiQZa4b6wlF.nJs2TUeBm7ZuoItwVDESWqtV}
pwn.college{zbj2ebM3YbsG.23JZt9gCRltVPUJ4pXsHloq-.hZFbLfJ8h}
pwn.college{KvMMYTMDlkaVfD375NehH0jmH8ZDnzfMA0qQ0ktiQjesVUC}
pwn.college{o-io8pwuZKlzsTLBNwZUniyDxgZO3GsqUsp1m26SBwUh9wB}
pwn.college{b3nwd3thFbinF8GZNUxeLY6b6zvxZJvRpucQhq6Kt-IE6dE}
pwn.college{HZ0SFde1VAw8eNFhe4BaPM9eIiivglY4Q5PeDJ18Itumw0i}
pwn.college{6GGluKg0uj-xxe1IHg2G87GXWxsdD4ZJ9FiZq5nRFLmhfae}
pwn.college{AbD2xaRrwMfaSajjwVdsA4gPXqqZjIU4KazrFhRVMEkM8t5}
pwn.college{dylJFvys6d3CUCSHby1XR0wQH7gwYby5Tt0buA14NtCQq6g}
pwn.college{x1iVhIgCjq65E8BhGY4GqcSk0LccPXGwoqmRXs2S1DGGGt8}
pwn.college{1yPRlv7AR145mSiPU3XV6DeAlrqRtfy.iUFsx8OkKw-6v0k}
pwn.college{jA8DKWR0wF4PNEHLqyxYvTXMkw-W7lduEcEhsGoawjYXQZ2}
pwn.college{vS3sGFgpaBoBvk77C5RjiezZcYhWuZDClcdkImE1DqTanF9}
pwn.college{2YeqUl0vpuZ3Viqni7vhHuKav88re0YLClsVQo6KyGgadnM}
pwn.college{eJY7UJHayxL7QKN0xFy0zxeDhZP3V2yUZrDBsHEbqZp1tQN}
pwn.college{1jKDalW4ZGk5NAXvF.qm-BzG0z-Eow9Wt7zZYemVjIrl0t1}
pwn.college{RJIvPAMFHarNAI.2ZycMBK.Or6M6EPv9sDtEwAA3b.JXGcQ}
pwn.college{GVLPnU6LZV2zP-fCwJDK32gnvLnw-TOsFIDDgeP71X-L2RA}
pwn.college{poCXZU.dOVE0czuyzshyrY-775bT47bjZqDCfE3c5LjN2ri}
pwn.college{9.-qlImJA2ntlyuwFT7j74PuhEqeBsYnocke24g4oEa1Eqf}
pwn.college{c9jW-4tbdW8zi7b8XO30ZG0hCH-XvFdyPzKQNhGM9AkypfZ}
pwn.college{5AbIF7WS8YGoEiQM6lB6ShFzXhS49olIflLh5OZb2pLlz40}
pwn.college{qUEP.FEOS0uo995Pju9sVm9Ifg-yoRMpCRE8kC2O3XsL2px}
pwn.college{n0NyBeA74fA2kpTefJrynvfWfo6NhnXW37i1IlB.G9Qc7yS}
pwn.college{0CDgxYvjo17ubVB76aBUOHg8lf6Mcgf5Ejj.7sjVh.CDxEh}
pwn.college{n66fRutzRxgMKApFI2ya9JEA.s7a-UFPBoEK9irl8EBAniC}
pwn.college{gjitftSIILTzVeUaiZQqJhBGxG6cNMJcMXdN22M7M8BEssq}
pwn.college{Z-KcBYgxMkdjVQDb6K1DwCToQE25frguT8aVm0q76oKs2bE}
pwn.college{29X.YinAuw5yuL2v9BSkuC0ZBJ2CQHwfRc.I0aypizNWYXn}
pwn.college{AarFbsJTXOzCr65rSfLZYT8OCDoFYSvTrFJuuXdSIp6opjX}
pwn.college{vdKHVA6ZRA3gFKG7ea7uvmoER0sW20YiuN2Irjs8xUcJfa6}
pwn.college{MQGasQxO0NISCpROygGDTMxcg0e4d.qIqgY0FnqVR6Q1eWv}
pwn.college{Kqp.35loMFftBK15JGE8PcfP-P8tqso28sGac9x6sAqJfaL}
pwn.college{A-kyMM.fKectNcV3SO2.-n6OIh0hji.jNIOeo5A8L-XU6cj}
pwn.college{.yeSiWwWbd1hC28aLtVnQazmsNkqfPve2AC1hbSg12cuhCB}
pwn.college{hYoxARn9OncrEmncMwclf70QB76UPBfI-TZUpq2BzTyXu4.}
pwn.college{h3L3DvkR6X2ZYp4tbvk7wbKBGA39ypt0FdNh5PkcW8U2eGh}
pwn.college{2J9pvdNp73m.EhdIYrJSNvP.YhT0JMONsTlTrMCA4-EFeMF}
pwn.college{NAmoCAfRrgJ9Ry1qKWJYGVrRowecK4Ywx1JDJFyBiiAmuCB}
pwn.college{9TeX3RYpsGAMlNaVd9o0dyZnXQtriHP0z8ovx--nB-BHrSi}
pwn.college{JQJOxg5MFuh5rrZvl21J5u2iRKnav0.tfYGt8a370QyMZyz}
pwn.college{oWHqRvJr.2dW-1enNMEe8aCyprX7Rk24qn.auIEcarAJKzO}
pwn.college{yEbc-o5AZG6u3y.YRlUT3AsJWVgzCPP812wK.vBvUACx1PF}
pwn.college{waKsuqUUHlvgTzm2z7ateUFUNAeORkoR79p4eCsxu7wP1Dj}
pwn.college{jP0kMEv8o-QWWg3aBnjRQA80.VgKfbjn38qyeaqc3rcCbOz}
pwn.college{bKLoWudXTipFoEVB8Ws7XB-E3R2fSiKS4NpE.AhEaKyOuZN}
pwn.college{Cqn9LupKcOk0XIyYXmapM64k8TelC9oPN6c07dmdL6clA4T}
pwn.college{p8mcqUdnDoLlT1wxtMFfthfLcrwtmiaa8mld6O6CXv9.f3U}
pwn.college{8x4Pq7kTWZ47E75e1f3BlSaFOswkY87DcDCmbpLzIgN7I8m}
pwn.college{WQ3LN5teW0J0NQhROvozdqJf7mfdSc8UT1h-MLZpSC.dAsw}
pwn.college{EgppPTVUuWVE87cjs24ifnWR-uN7QkTu-ByCYE98qlYpTk0}
pwn.college{42.xljMobsvhRcQxqE8Q-E27BNP8DfcEHRQl1hPqbWN.8pB}
pwn.college{AIlBjwUZDgj29hAF9MUy-IGY.0B6HkCb7lJLTNncdlAl2bx}
pwn.college{5-70Jba83glqs1g3KfwGsy1OgpGZSfRCUJjtHYjzv4gp5H7}
pwn.college{BwWrSaFhLZ.Sd50PRFUyNFYMvHjF2-Luc2qAkISk4Zp7Ltz}
pwn.college{b3sBxT1t3JMjb.sAHhI-x-a0ZGKC69OEmcw-d.ui4buBZbW}
pwn.college{EdcwmHGscXrs71vd15UzdY90NWG91bkBYXxbKhJLzzN01G0}
pwn.college{-GA3-dsSpXMP-RH5QXftJN.nm053QZsx7dv1sT1egCNdmaf}
pwn.college{CPlQsdP9sGTwegpQY58Zd31yQ9lBzocX57TK2yZM1SsX5f-}
pwn.college{NWgHzW02wjguD5IIBM-VfpGxPK63JDgVuAxBkqhWnekxWG4}
pwn.college{wrxP0TN0B4qml11Aoaj-hJ9egAjuFAXhDskM.e0xF.SDH.s}
pwn.college{MlpNoBsexRcNvAnbLFrf.5-3Zuq0v-SIhUFOMZ8804kuVhM}
pwn.college{RhcHZWl.DSGJGo1yX4wPmbwsyx1DpjKYQPGiF99Qk7qpzMU}
pwn.college{vj.Dzuot.OazA58B8lf--m2XnGimieV3YyeJOcI6SlhmlBn}
pwn.college{nWb3FZe0bcQzfOWPuAuvaxTmNrKQmrl.KZJthrhSerWTrOH}
pwn.college{lvFK4-4sKDrgfQ62Ux74hah7klQ8Qn18xoGYWUbW145BuUR}
pwn.college{v7IET.N0OEwyVSHj87kxxvp8Sq0R.v3JgTGmPgt1ybHuGZo}
pwn.college{9H6Ztj2DwIHTRD9zOrZ1HHoO5q.AQr0iYXyp2R.9vHkCL4c}
pwn.college{DDMu1ogvlutsAFVW8Vdf1VCo-AQq5TPXcMo99f8xAesmpQU}
pwn.college{oNI1STal2zBqiB3HoKyU8PFSrYpA-OK.TyrhuN8Af1w1mS7}
pwn.college{SjnVrXa3mYlDMNbMH9gU6tTiQ55aV-jpWEj.qGY2XhTdPhW}
pwn.college{rPUOC6BlAj2sgwMp1ksSSCiZjtb-AzMip8Q9l28urBNFTYE}
pwn.college{V37hJy0kfBfC549QA.VTKE-1HFGtqgARS9IUvvwNZEZW7Ja}
pwn.college{e9PfZRVwQs5v8HwDObK7T0EeraoJUc-jCyn57viIrkc8LSK}
pwn.college{D-TUipL00fOWs7ppMBGwGCN5no2BlLqAD4kfCBR.kI3d5cm}
pwn.college{AEJDl8jztg8Eklq.gypvWmQZmbuAV0JBRH4U6i6MJ8xqTtK}
pwn.college{k5O3PmM09gRp0k.AM8e31D9swd0TTCkiKirsrtk0iDcujg1}
pwn.college{RdAI47gyyfEFgJZaU3PjcVAuOYQw5wSX7kj4vydUr3NJKgt}
pwn.college{fyGdzHmKE0oSm3n1IcCysMxd2oaQWLgGfUx.kfstEiFnkG.}
pwn.college{M8xvfM1r9IHU4sbd3G4yOskDIvf1La8LRpNMrpMxliQSG46}
pwn.college{XTi1edzi4kvPXPx9GRkLqxGpTr3PhwqWJ7yGUfzVTy7rFha}
pwn.college{d.5UUGdL8MYG7hZ5Vpqc7C0ePSmM2a7qr.WwTzHUPI-VRQQ}
pwn.college{p3mcTiMzV-4ohtCrVkxbP3DG87haMnLQpvLLzNVxTUL8HtW}
pwn.college{D5v7lkWP1vY386LeCYv8ta.A1cRalxS39KtHuB23ppPsSEp}
pwn.college{obmJ4kxEe6kj5ZOnm5BI0oacnzhzbG4K3fYMvDg64l2fHAt}
pwn.college{x65XCQhE.m0b3D6SyfeYisuoCCZk8xxASfXFzgL5mR6OuMk}
pwn.college{qoNN1FjYT-p1w3cQ1A8ZRP7clMhAK5zrx5yHzqmZ-M2Y5qX}
pwn.college{jEdJCaEou5twKJDxo62twEouDcOO5BijMq9XHMvfZEuKa7-}
pwn.college{pY-TrZvRuKuoFoFReDpkqrWCOLI16ZNG1XiZbDMdoa633rQ}
pwn.college{0VVkjmqYv3QAwTs-A4Qre.dmyGkJOTgWIPw.c8WD3NyuvGa}
pwn.college{Sh4CN4U6PG.H3yeOb1Dv7Uh.bt10v41Jix-F52HUOrsHXuJ}
pwn.college{M99T0ydwXTpGFqr.1oeCiMsmVtM2-H1uzeya1q.U-pytMZW}
pwn.college{vjkULMRZuSaLaQprTwAiXtat39-1TIpJqhvtinlzMlL8ZVc}
pwn.college{uoaAmNg8IixUnWuxAtr1delcB2On2X032Bp8OuWs5xh52uI}
pwn.college{WsFTdaQeyxfDMcAZdBtTk0gQDNJSqwAQRoRWqXKqhHy.Yey}
pwn.college{tNcBI6M5BLNq9mKmKpD8338yQqGKEqWHk97k4e1gTyWaXAM}
pwn.college{RJx1fY4W0FFr4kiWyyJ1khn4P65NmiCRmMSXmdhyTT0kayE}
pwn.college{W32V.bSwDUPhZ2PutgR-H8fw8V1mQPn-cVhF2ZlQcBkfyuQ}
pwn.college{qSoruoZGZicSHS29o5.B2JWSwt3jkUMPFPnAMExSVdDy6SI}
pwn.college{C3Br34tbxm6stEDLpz3EQytZWUytdpMP7vpdR4eBdf0BnT-}
pwn.college{wwdc2LcZXzmiac8Ytsssmx0KTpsC6TjWK8pKV4i9eDw19hK}
pwn.college{4KwtlkVdttvOjc1BcHTbQSBYVlCJOgrdvP9m8Mx5CtmmWB9}
pwn.college{9z2Brq8DwFn4SgyhKcZ85cZWoNs.CBall6NTUvT5DQSjylo}
pwn.college{2cVRDNesCe6rHzZIH86xWaUElnvnttj2Gs85j2WO6A8Xfwy}
pwn.college{bbCUbFAOftdspy8uPExapXtjxll5G6lVrxcpc3Zrq2Iy0Sn}
pwn.college{BfBsuv8DzCM2s1CleL8g1lodJt2xUvh4.X148UqNgPynkYP}
pwn.college{CMsbM.AmMcsEy1eeb-2ztCyEQcaxKTskMIuH4dRDiJsSkvh}
pwn.college{iw7j.lMIiNyQjQAz8wda-9CtAMy3DwXcr4yFflYoMEijPlC}
pwn.college{49TEysQ6GwFYpDmYyi97kEN6FyjgRIwzraGcxngtC65h6Bf}
pwn.college{8aoxke0K1iIs02f.CmAdSb1uoTGtntzwSHA4ZIk3KWamAr7}
pwn.college{R-HV9UjfbKlcePlkXwmfALFN3sIFuaLyBYfhtEhtyQgHAKD}
pwn.college{j9yta9vE7uAlGEhQKAGQecFaMWHb1pELarsOTcfA9g-o7so}
pwn.college{Hfd8qK.9Ja-Vyns8mszkQ-MHkezTULdMVto.fM0VHWPgEjh}
pwn.college{L8-yUy1SM9A..MhPCUuTzzyORERY6jut9ua1PSvhQORKg10}
pwn.college{sCbf-DeXe4XK9dce3CJ7QXyQyRKlTVYG7PV5hrktX-wXplq}
pwn.college{saAvLCOtaAKIBUCln-oybvthzWegMoM9eK.IG1o30HkWXCx}
pwn.college{V5cMI5aotPrK-QIFle403C0hBbgJpWHmhEYxDXYpFsN.J2p}
pwn.college{YjGqxutVGw7h8y1XD-0urSv0VHXHVVZc8sSUGnY0wqNyOGD}
pwn.college{XDUaW5R8lIrfpMwjQFk6QtCdQl9Gru2nz15TCw0xagdEiql}
pwn.college{9swmnUXtsnMWj9NK0fdfb5gXIgwCufbjib39ILLCUb4I8BA}
pwn.college{TEFoXqTBdeJhhU.vtpDmH74C75uK0EiTO4Qy56AmjxGt1OT}
pwn.college{oPQRwqys5Y3QN58FY7KG2cR2PbZqGhMHSrqXJAe..-4JnFP}
pwn.college{gv7N-AZTFs1msB4ERpR2W9qU5s9vs2WPe-ord5C-dObvSuq}
pwn.college{OmS3AVFQ69Xj2gSLvAbzfcXYHDpZBiIGM4raFtWHXBerQpn}
pwn.college{YaNzdMvWZKH1jbM8YWIoELffncThr-tQm9uQJ-FkIY58QB2}
pwn.college{nZVtTYh6pk0X-i51EPX18fnX6BZ7V58R1gKg6QtXlg2No7N}
pwn.college{KyCG2qaS4N8G.KJlIWWXVWsOgFWaAXESt8fII8l9vi2xJWT}
pwn.college{Aeru9pPnBVKz3c5V0pELN0Rz6ruSV44quVozHpf6d0TSPom}
pwn.college{52PjzhQZ9ezjkqwzTeNgNTVUSoppMh9l.UZHm4EJQNl9Nau}
pwn.college{TXWjAxh0fglsRbTd94vHfrBK0liVrb-6sWQ4.O32XcoYCo0}
pwn.college{FAKsTVxDuLoqToaVN9k8qFNaH4tOTR3K2-GziuMGwPmeoQI}
pwn.college{oQ.xY6XGjRV5dZnbYXoHnQjuHnk3bAJG3oPCZp8zFLXA4V7}
pwn.college{9zdMZQcjRGKyOuHD5Byw8rl5Pm84h.G59Lf0zVBM.jTxo6O}
Sending the flag to /tmp/flag_fifo!
pwn.college{IRFU-2_jvE2vPHON7hRkn-cfjcK.0FNzMDOxwCMwEzNzEzW}
```

### New Learnings

## 5. Suspending Processes

### Solve
**Flag** `pwn.college{k3uNdZWicslNeWMHZlEtvRyHNw1.QX1QDO0wCMwEzNzEzW}`

```bash
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         138     129  0 17:20 pts/0    00:00:00 bash /challenge/run
root         145     129  0 17:20 pts/0    00:00:00 bash /challenge/run
root         147     145  0 17:20 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{k3uNdZWicslNeWMHZlEtvRyHNw1.QX1QDO0wCMwEzNzEzW}
```

### New Learnings

## 6. Resuming Processes

### Solve
**Flag** `pwn.college{QanLnahasB9m6DtkGJLx8-0dfft.QX2QDO0wCMwEzNzEzW}`

```bash
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{QanLnahasB9m6DtkGJLx8-0dfft.QX2QDO0wCMwEzNzEzW}
Don't forget to press Enter to quit me!

Goodbye!
```

### New Learnings

## 7. Backrounding Processes

### Solve
**Flag** `pwn.college{Erc2cxU-2kwMHA_D3DHtXC23SWo.QX3QDO0wCMwEzNzEzW}`

```bash
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         139 S+   bash /challenge/run
root         141 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the
background, and then launch a new version of me! You can background me with
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~backgrounding-processes:~$


Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out.

hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         139 S    bash /challenge/run
root         149 S    sleep 6h
root         150 S+   bash /challenge/run
root         152 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{Erc2cxU-2kwMHA_D3DHtXC23SWo.QX3QDO0wCMwEzNzEzW}
```

### New Learnings

## 8. Foregrounding Processes

### Solve
**Flag** `pwn.college{scUDm67fPbZRLOYBzsktZ-xk13p.QX4QDO0wCMwEzNzEzW}`

``` bash
hacker@processes~foregrounding-processes:~$ /challenge/run
To pass this level, you need to suspend me, resume the suspended process in the
background, and *then* foreground it without re-suspending it! You can
background me with Ctrl-Z (and resume me in the background with 'bg') or, if
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~foregrounding-processes:~$


Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out. After that, resume me into the foreground with 'fg';
I'll wait.

hacker@processes~foregrounding-processes:~$ fg
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{scUDm67fPbZRLOYBzsktZ-xk13p.QX4QDO0wCMwEzNzEzW}
```

### New Learnings

## 9. Starting Backrounded Processes

### Solve
**Flag** `pwn.college{c3pa42ZWwg7lLp_zq07KN_B2OvT.QX5QDO0wCMwEzNzEzW}`

```bash
hacker@processes~starting-backgrounded-processes:~$ /challenge/run
You've started me in the foreground! You must start me in the background (by
appending '&' to the command) to get the flag!
hacker@processes~starting-backgrounded-processes:~$ /challenge/run & [1] 147
[1] 142
bash: [1]: command not found
hacker@processes~starting-backgrounded-processes:~$


Yay, you started me in the background! Because of that, this text will probably
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{c3pa42ZWwg7lLp_zq07KN_B2OvT.QX5QDO0wCMwEzNzEzW}
```

### New Learnings

## 10. Process Exit Codes

### Solve
**Flag** `pwn.college{opBfapUWsupmQUx0eM7l3bgrv3D.QX5YDO1wCMwEzNzEzW}`

```bash
hacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
66
hacker@processes~process-exit-codes:~$ /challenge/submit-code $?
Incorrect... Make sure to use $? immediately after running /challenge/get-code.
Your shell will overwrite the $? variable with the exit value of any other
command you run!
hacker@processes~process-exit-codes:~$ /challenge/get-code $?
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
72
hacker@processes~process-exit-codes:~$ /challenge/submit-code $?
Incorrect... Make sure to use $? immediately after running /challenge/get-code.
Your shell will overwrite the $? variable with the exit value of any other
command you run!
hacker@processes~process-exit-codes:~$ /challenge/72 $?
bash: /challenge/72: No such file or directory
hacker@processes~process-exit-codes:~$ /challenge/get-code && /challenge/submit-code $?
Exiting with an error code!
hacker@processes~process-exit-codes:~$  /challenge/get-code
/challenge/submit-code $?
Exiting with an error code!
CORRECT! Here is your flag:
pwn.college{opBfapUWsupmQUx0eM7l3bgrv3D.QX5YDO1wCMwEzNzEzW}
```

### New Learnings

