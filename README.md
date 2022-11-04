# stonks-jupyter (work-in-progress)
Jupyter notebooks for chart patterns backtesting


## stock patterns

### SMAs all up & gap up
```
[d]O.0 / [d]C.1 > 1.2 \n\
AND [d]C.1 > [d]AVGC20.0 \n\
AND [d]AVGC10.0 > [d]AVGC20.0 \n\
AND [d]AVGC20.0 > [d]AVGC50.0 \n\
AND [d]AVGC50.0 > [d]AVGC100.0 \n\
AND [d]AVGC100.0 > [d]AVGC200.0 \n\
AND [d]AVGC100.0 > [d]AVGC200.0 \n\
AND (\n\
    [d]DV.0 > 1.0 \n\
    OR [d]MINDV3.1 > 2.0\n\
    OR [d]AVGDV20.0 > 3.0\n\
)\n\
AND (\n\
    [d]ATR1.0 > 8.0 \n\
    OR [d]ATR20.0 > 5.0 \n\
    OR [d]ATR20.20 > 5.0 \n\
    OR [d]ATR20.40 > 5.0 \n\
)\
```

### SMAs all up and fakeout
```
[d]H.0 * 0.99 > [d]MAXH20.1 \n\
AND [d]H.1 < [d]MAXH20.2 \n\
AND [d]H.2 < [d]MAXH20.3 \n\
AND [d]H.3 < [d]MAXH20.4 \n\
AND [d]C.0 < [d]O.0 \n\
AND [d]C.0 < [d]C.1 \n\
AND [d]C.1 < [d]AVGC50.0 \n\
AND [d]AVGC10.0 < [d]AVGC20.0 \n\
AND (\n\
    [d]DV.0 > 1.0 \n\
    OR [d]MINDV3.1 > 2.0\n\
    OR [d]AVGDV20.0 > 3.0\n\
)\n\
AND (\n\
    [d]ATR1.0 > 8.0 \n\
    OR [d]ATR20.0 > 5.0 \n\
    OR [d]ATR20.20 > 5.0 \n\
    OR [d]ATR20.40 > 5.0 \n\
)\
```

### 1st red day
```
[d]C.0 < [d]C.1 \n\
AND [d]C.0 < [d]O.0 \n\
AND [d]C.1 > [d]C.2 \n\
AND [d]C.2 > [d]C.3 \n\
AND [d]C.3 > [d]C.4 \n\
AND [d]C.4 > [d]C.5 \n\
AND [d]C.5 > [d]C.6 \n\
AND [d]C.1 > [d]AVGC20.0 \n\
AND (\n\
    [d]DV.0 > 1.0 \n\
    OR [d]MINDV3.1 > 2.0\n\
    OR [d]AVGDV20.0 > 3.0\n\
)\n\
AND (\n\
    [d]ATR1.0 > 8.0 \n\
    OR [d]ATR20.0 > 5.0 \n\
    OR [d]ATR20.20 > 5.0 \n\
    OR [d]ATR20.40 > 5.0 \n\
)\
```

### downtrending & touching EMA 50
```
[d]H.0 / [d]AVGC50.0 >= 0.98 \n\
AND [d]H.0 / [d]AVGC50.0 <= 1.02 \n\
AND [d]C.0 / [d]C.50 <= 0.6 \n\
AND (\n\
    #[d]AVGC10.0 < [d]AVGC20.0 \n\
    [d]AVGC20.0 < [d]AVGC50.0 \n\
    AND [d]AVGC50.0 < [d]AVGC100.0 \n\
    AND [d]AVGC100.0 < [d]AVGC200.0 \n\
)\n\
AND (\n\
    [d]DV.0 > 1.0 \n\
    OR [d]MINDV3.1 > 2.0\n\
    OR [d]AVGDV20.0 > 3.0\n\
)\n\
AND (\n\
    [d]ATR1.0 > 8.0 \n\
    OR [d]ATR20.0 > 5.0 \n\
    OR [d]ATR20.20 > 5.0 \n\
    OR [d]ATR20.40 > 5.0 \n\
)\
```

### First close under EMA 200
```
[d]C.1 / [d]C.250 >= 2.0 \n\
AND [d]C.0 < [d]AVGC200.0 \n\
AND (\n\
    [d]C.1 > [d]AVGC200.1 \n\
    AND [d]C.2 > [d]AVGC200.2 \n\
    AND [d]C.3 > [d]AVGC200.3 \n\
    AND [d]C.4 > [d]AVGC200.4 \n\
    AND [d]C.5 > [d]AVGC200.5 \n\
    AND [d]C.6 > [d]AVGC200.6 \n\
    AND [d]C.7 > [d]AVGC200.7 \n\
    AND [d]C.8 > [d]AVGC200.8 \n\
    AND [d]C.9 > [d]AVGC200.9 \n\
)\n\
AND (\n\
    [d]AVGC10.0 < [d]AVGC20.0 \n\
    AND [d]AVGC20.0 < [d]AVGC50.0 \n\
    AND [d]AVGC50.0 < [d]AVGC100.0 \n\
    AND [d]AVGC100.0 < [d]AVGC200.0 \n\
)\n\
AND (\n\
    [d]DV.0 > 1.0 \n\
    OR [d]MINDV3.1 > 2.0\n\
    OR [d]AVGDV20.0 > 3.0\n\
)\n\
AND (\n\
    [d]ATR1.0 > 8.0 \n\
    OR [d]ATR20.0 > 5.0 \n\
    OR [d]ATR20.20 > 5.0 \n\
    OR [d]ATR20.40 > 5.0 \n\
)\
```
![image](https://user-images.githubusercontent.com/15132795/199727001-00182fc6-aa1e-4d85-b890-fec7d82555ad.png)
![image](https://user-images.githubusercontent.com/15132795/199727993-d2070d61-d225-4e47-a132-a273542d10bf.png)

### up big, first time below 50 with downtrending 10&20
![image](https://user-images.githubusercontent.com/15132795/199724898-28124aa8-b8a6-451f-a63f-72c0f64be348.png)

### MA cluster (e10-e20-s50)
![image](https://user-images.githubusercontent.com/15132795/199741907-20be4268-460f-4e4e-9c7c-3c24e44b1837.png)

### SMAs all up (except 10) dip buy
![image](https://user-images.githubusercontent.com/15132795/200084309-d9940090-70b3-4b6a-891a-49115682fc91.png)


