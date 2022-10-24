# stonks-jupyter (work-in-progress)
Jupyter notebooks for chart patterns backtesting


## stock patterns

### SMAs all up & gap up
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

### SMAs all up and fakeout
[d]H.0 > [d]H.1 \n\
AND [d]C.0 < [d]C.1 \n\
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

### SMAs all up & 1st time over previous day high
[d]C.0 > [d]C.1 \n\
AND [d]C.1 < [d]C.2 \n\
AND [d]C.2 < [d]C.3 \n\
AND [d]C.3 < [d]C.4 \n\
AND [d]C.4 < [d]C.5 \n\
AND [d]C.5 < [d]C.6 \n\
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
