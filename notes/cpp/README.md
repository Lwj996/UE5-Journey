# C++ Notes

UE 方言 C++ 笔记（第 3 个月开始建）。

## 预期目录

- `01-ue-cpp-vs-standard.md` — UE C++ 与标准 C++ 的区别
- `02-uclass-uproperty-ufunction.md` — 三大宏详解
- `03-containers.md` — `TArray` / `TMap` / `TSet` / `FString`
- `04-uobject-gc.md` — UObject 与垃圾回收
- `05-pointers.md` — 指针类型区分（`TWeakObjectPtr` 等）
- `06-delegates.md` — 单播 / 多播 / 动态 Delegate
- `07-bp-cpp-interop.md` — C++ 与蓝图交互
- `08-structs.md` — `USTRUCT`
- `09-subsystems.md` — GameInstance/World/LocalPlayer Subsystem
- `10-modules.md` — UE 模块与 `.Build.cs`

## 前端转 C++ 的心理建设

| JS 习惯 | UE C++ 陷阱 |
|---------|------------|
| 变量自由类型 | 类型必须显式声明 |
| GC 自动 | 必须 `UPROPERTY()` 告诉 UE 这个指针要被 GC 追踪 |
| `null` 检查宽松 | 解引用空指针立即崩溃 |
| `console.log` 到处打 | 用 `UE_LOG` 宏 + 分级（Log/Warning/Error） |
| async/await | 用 Delegate 或 Tick 轮询 |
| 模块化 `import` | `#include` + `.Build.cs` 中加模块依赖 |

**别怕** — UE C++ 比标准 C++ 简单得多，你前端的工程化思维会帮你很多。
