# S2JUnit4 compatibility test

S2JUnit4がJUnit4.4とJUnit4.11の両方で動作することを確認するtestプロジェクトです。

確認する組み合わせは次の2つです。

- S2JUnit4 + JUnit4.4
- S2JUnit4 + JUnit4.11

## 方針

S2TigerのソースからS2JUnitのtestコードをそのまま移植し、それぞれのJUnitのバージョンでtestが通ることを確認します。

S2Tiger 2.4.47 + JUnit4.11の組み合わせでは2つfailします。
S2Tiger 2.4.48以降では、JUnit4.4 / JUnit4.11 のいずれでも通るはずです。


## 実行環境

- Java5
- maven2 (maven3でも動作しています)


manholeの使用環境1

```
>mvn -v
Maven version: 2.0.9
Java version: 1.5.0_22
OS name: "windows 7" version: "6.1" arch: "x86" Family: "windows"
```

manholeの使用環境2

```
$ mvn -v
Apache Maven 3.2.1 (ea8b2b07643dbb1b84b6d16e1f08391b666bc1e9; 2014-02-14T17:37:52+00:00)
Maven home: /xxx/apache-maven-3.2.1
Java version: 1.6.0_65, vendor: Apple Inc.
Java home: /System/Library/Java/JavaVirtualMachines/1.6.0.jdk/Contents/Home
Default locale: en_JP, platform encoding: UTF-8
OS name: "mac os x", version: "10.9.4", arch: "x86_64", family: "mac"
```

## テスト実行方法

### S2JUnit4 + JUnit4.4

```
mvn clean test
```

### S2JUnit4 + JUnit4.11

```
mvn clean test -P junit411
```
