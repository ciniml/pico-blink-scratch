# blink-scratch

Raspberry Pi Pico用のLチカプログラムのメインのソースコードをC++に置き換え + VSCode用デバッグの初期設定

## デバッグ

要Cortex-Debug拡張

OpenOCDを先に立ち上げた状態でVSCodeのデバッグ実行

* Windows

```bash
~/pico/openocd-win/bin/openocd.exe -c "bindto 0.0.0.0" -f interface/picoprobe.cfg -f target/rp2040.cfg
```

* Ubuntu

```
~/pico/openocd-linux/bin/openocd -f interface/picoprobe.cfg -f target/rp2040.cfg
```