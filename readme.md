
# compression

This repository contains a decompressor for a tweaked compression intended for compressing demos and assets
which i derived to compress some of my noncritical data. The format is based on machine learning, prediction
by partial matching and suffix sorting. The decompressor is a 7 kilobyte PE EXE, which has been tested to work
on Windows 10.

The decompressor accomplishes an amazing binary size to compression quality ratio.

|              File |       Compressed | Uncompressed      | Ratio (d/c)  | Ratio (LZMA, -e)       | Ratio (gzip, -9)         |
|-------------------|------------------|-------------------|--------------|------------------------|--------------------------|
| bee.txt           | 16,896 bytes     | 5,615,100 bytes   | ~ **332.33**     | 21,584 bytes, ~ **260**    | 2,080,490 bytes, ~ **2.69**  |
| kalashnikov.wav   | 8,651,028 bytes  | 18,780,204 bytes  | ~ **2.1709**     | 15,800,024 bytes, ~ **1.1** | 18,224,021 bytes, ~ **1.03** |
| megalovania.xm    | 186,628 bytes    | 353,107 bytes     | ~ **1.892**      | 207,413 bytes, ~ **1.70**  | 231,892 bytes, ~ **1.52**    |
| urls.txt          | 498,505 bytes    | 6,154,115 bytes   | ~ **12.345**    | 544,615 bytes, ~ **11.2**  | 1,334,992 bytes, ~ **4.06**  |

| Method | Decompressor size |
|--------|-------------------|
| gzip   | 98,048 bytes      |
| lzma   | 158,400 (liblzma) + 81,192 (lzma) = 239,592 bytes |
| unpack | **7,516 bytes**       |

# license

all rights reserved (no copying, no redistributing, no disassembling and sharing the results),
except test data - i have no clue where most of it came from.
