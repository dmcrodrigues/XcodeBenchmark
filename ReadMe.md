`XcodeBenchmark` contains a *large* codebase to measure the compilation time in Xcode.

You are probably familiar with the following question:
> "Should I buy an i5, i7, or even i9 processor for iOS/macOS development?".

`XcodeBenchmark` is initially created for [Max Tech](https://www.youtube.com/channel/UCptwuAv0XQHo1OQUSaO6NHw) YouTube channel to compare the performance of new iMacs 2020.

I believe the results will help developers to make the right *cost/performance* trade-off decision when choosing their next Mac.

## Score

|        Device        |           CPU           | RAM | SSD | HDD | Xcode |  macOS  | Time(sec) |
|:--------------------:|:-----------------------:|:---:|:---:|:---:|:-----:|:-------:|:---------:|
| MacBook Pro 13" 2020 |      Apple M1 8-core    |  16 | 1TB |     |  12.2 |   11.0  |    133    |
|     iMac 27" 2020    |    i9 3.6 GHz 10-core   |  64 | 512 |     |  11.6 | 10.15.6 |    217    |
|   iMac Pro 27" 2017  |  Xeon 3.0 GHz 10-core   |  64 | 1TB |     |  11.7 | 10.15.6 |    222    |
|     iMac 27" 2020    |    i7 3.8 GHz 8-core    |  64 | 512 |     |  11.6 | 10.15.6 |    229    |
|     iMac 27" 2020    |    i7 3.8 GHz 8-core    |  32 | 512 |     |  11.6 | 10.15.6 |    229    |
| MacBook Pro 16" 2019 |    i7 2.6 GHz 6-core    |  16 | 512 |     |  12.2 | 11.0.1  |    250    |
|     iMac 27" 2019    |    i9 3.6 GHz 8-core    |  64 | 2TB |     |  11.6 | 10.15.6 |    252    |
|   iMac Pro 27" 2017  |   Xeon 3.2 GHz 8-core   |  32 | 1TB |     |  11.6 | 10.15.6 |    263    |
|     Mac Mini 2018    |    i7 3.2 GHz 6-core    |  16 | 512 |     |  11.7 | 10.15.5 |    300    |
|       Ryzentosh      |  R5 3600 3.6 Ghz 6-core |  16 | 1TB |     |  11.7 | 10.15.6 |    312    |
| MacBook Pro 16" 2019 |    i9 2.3 GHz 8-core    |  32 | 2TB |     |  11.6 | 10.15.6 |    328    |
| MacBook Pro 16" 2019 |    i7 2.6 GHz 6-core    |  16 | 512 |     |  11.6 | 10.15.6 |    353    |
|     Mac Mini 2018    | i5-8500B 3.0 GHz 6-core |  8  | 512 |     |  11.7 | 10.15.6 |    383    |
|      Hackintosh      |  i5-8400 2.8 Ghz 6-core |  32 | 512 |     |  11.6 | 10.15.6 |    409    |
|     iMac 27" 2017    |    i7 4.2 GHz 4-core    |  48 | 2TB |     |  11.7 | 10.15.6 |    411    |
|    iMac 21.5" 2017   |  i7-7700 3.6 GHz 4-core |  16 | 1TB |     |  11.7 | 10.16.6 |    419    |
| MacBook Pro 15" 2018 |    i7 2.6 GHz 6-core    |  16 | 512 |     |  11.6 | 10.15.6 |    440    |
|     Mac Pro 2013     |E5-1650 v2 3.5 GHz 6-core|  32 | 1TB |     |  11.7 | 10.15.6 |    518    |
| MacBook Pro 15" 2017 |    i7 2.9 GHz 4-core    |  16 | 512 |     |  11.6 | 10.15.6 |    583    |
| MacBook Pro 15" 2015 |    i7 2.2 GHz 4-core    |  16 | 265 |     |  11.7 | 10.15.6 |    594    |
| MacBook Pro 15" 2016 |    i7 2.7 GHz 4-core    |  16 | 1TB |     |  11.7 | 10.15.6 |    642    |
|     Mac Mini 2014    |    i5 2.6 GHz 2-core    |  8  |     | 1TB |  11.7 | 10.15.6 |    1193   |

## Set up

- Download and install [Xcode](https://apps.apple.com/us/app/xcode/id497799835).
- Open Xcode and install `additional tools` (Xcode should suggest it automatically).
- [Download](https://github.com/devMEremenko/XcodeBenchmark/archive/master.zip) and unarchive XcodeBenchmark project.

## Before each test

1. Disconnect the network cable and turn off WiFi.
2. Make sure to disable all software running at startup
    - Go to `System Preferences` -> `Users and Groups` -> `User` -> `Login Items`.
    - Empty the list.
3. Update `Energy Saver` settings 
	- Go to `System Preferences` -> `Energy Saver` -> `Turn display off`  and set 15 min.
3. Reboot and cool down your Mac.
4. Connect to the power adapter if you use MacBook.

## Running a test

1. Open the `Terminal` app.
2. Write `cd ` and drag & drop `XcodeBenchmark` folder to the `Terminal` app to form `cd path/to/xcode-benchmark`.
2. Run `sh benchmark.sh` in `Terminal`.
3. When `XcodeBenchmark` has completed you will see [this information](img/contribution-example.png).
4. Upload your results, see [Contribution](https://github.com/devMEremenko/XcodeBenchmark#contribution) section.

## FAQ

**Q: What's inside?**

A framework that includes **42** popular CocoaPods libraries and **70+** dependencies in total.

| Language      | files | blank  | comment | code   |
|---------------|-------|--------|---------|--------|
| C/C++ Header  | 2785  | 58618  | 143659  | 215644 |
| C++           | 750   | 24771  | 30788   | 182663 |
| Objective C   | 882   | 27797  | 23183   | 148244 |
| Swift         | 1122  | 21821  | 35225   | 113945 |
| C             | 390   | 15064  | 23319   | 84119  |
| Objective C++ | 69    | 2980   | 2026    | 15561  |
| Markdown      | 61    | 4865   | 1       | 15131  |
| XML           | 144   | 1022   | 10      | 13047  |
| Bourne Shell  | 3     | 244    | 209     | 1321   |
| JSON          | 22    | 1      | 0       | 1114   |
| Pascal        | 2     | 87     | 185     | 180    |
| YAML          | 1     | 0      | 0       | 5      |
| SUM:          | 6231  | 157270 | 258605  | 790974 |

**Q: What do the results mean?**
1. First of all, the project is **huge**. Most projects are of a much smaller size.
2. The results show *relative* performance in Xcode, compared to other Macs running under similar conditions.

**Q: Why is CocoaPods not excluded from git-repo?**
- The project is also used by non-programmers. Let's *keep it simple*.

## Contribution

- **Preferred:** [Submit a pull request](https://github.com/devMEremenko/XcodeBenchmark/pulls) and add a row to the `Score` section.  
- [Open an issue](https://github.com/devMEremenko/XcodeBenchmark/issues/new/choose) and include all info to fill the `Score` section if you cannot submit a pull request.

Make sure:
- [All steps](https://github.com/devMEremenko/XcodeBenchmark#before-each-test) are performed
- `Time` column is still sorted after insertion.
- You are added to the end of the [Contributors](https://github.com/devMEremenko/XcodeBenchmark#contributors) list.
- Attach a screenshot with a compilation time. [Example](img/contribution-example.png).
- The content in cells is centered. You can use [this tool](https://www.tablesgenerator.com/markdown_tables) to edit a table.
    - File -> Paste table data
    - Select all cells -> Right click -> Text align -> Center

## Contributors

- [Maxim Eremenko](https://www.linkedin.com/in/maxim-eremenko/)
- [Max Tech](https://www.youtube.com/channel/UCptwuAv0XQHo1OQUSaO6NHw) YouTube channel
- [@bitsmakerde](https://github.com/bitsmakerde)
- [@ivanfeanor](https://github.com/ivanfeanor)
- [@sverrisson](https://github.com/sverrisson)
- [@radianttap](https://github.com/radianttap)
- [@rynaardb](https://github.com/rynaardb)
- [@ekhodykin](https://github.com/ekhodykin)
- [@N0un](https://github.com/N0un)
- [Paul Zabelin](https://github.com/paulz)
- [@theome](https://github.com/Theome)
- [@Kuluum](https://github.com/Kuluum)
- [@villy21](https://github.com/Villy21)
- [@zhi6w](https://github.com/zhi6w)
- [@soorinpark](https://github.com/soorinpark)
- [@igorkulman](https://github.com/igorkulman)
