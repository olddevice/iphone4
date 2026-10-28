工具链（Linux → iOS armv7 交叉）


| 组件 | 路径 / 版本 | 说明 |
|---|---|---|
| clang / clang++ | `./ios-toolchain/llvmroot2/usr/lib/llvm-18/bin/clang`（18.1.x） | 编译 ObjC++ / C++17 |
| 链接器 ld64 | `./ios-toolchain/cctools-port/cctools/ld64/src/ld/ld`（Apple ld64 956.6） | 真机 Mach‑O 链接 |
| SDK | `./ios-toolchain/sdkdl/iPhoneOS9.3.sdk` | 用 9.3 SDK 编译、部署到 7.1.2 |
| Stub 库 | `./ios-toolchain/stubs`（libSystem.B.dylib 等）、`./ios-toolchain/stubs-fw` | 解决链接期缺失符号 |
| 签名 | `./ios-toolchain/ldid` | fake‑sign entitlements |
| USB 中继 | `./ios-toolchain/usbmux_relay 2222 22` | USB → TCP，本地 2222 映射设备 ssh:22（密码 `alpine`） |
| 便捷壳 | `./ios-toolchain/dssh`、`./ios-toolchain/dscp` | `ssh -p 2222 root@127.0.0.1` 封装 |
