# 手指几何负片生成器 - 自托管版

## 文件清单（压缩包内）

| 文件 | 说明 | 状态 |
|------|------|------|
| `hand-negative.html` | 主程序（已改好相对路径） | ✅ 已就绪 |
| `vision_bundle.mjs` | MediaPipe JS 模块 | ✅ 已就绪 |
| `wasm/vision_wasm_internal.js` | WASM 加载器 | ✅ 已就绪 |
| `wasm/vision_wasm_internal.wasm` | WASM 二进制（9MB） | ✅ 已就绪 |
| `model-helper.html` | 模型下载器（帮你下 .task） | ✅ 已就绪 |
| `hand_landmarker.task` | 手部模型 | ⚠️ 需下载 |

## 你的仓库最终结构

```
hand-negative.html
vision_bundle.mjs
hand_landmarker.task         ← 唯一还缺的
wasm/
  vision_wasm_internal.js
  vision_wasm_internal.wasm
model-helper.html            ← 用完可删
```

## 操作步骤

### Step 1: 上传已有文件到 GitHub
把除 `hand_landmarker.task` 外的所有文件上传到仓库：
- hand-negative.html
- vision_bundle.mjs
- wasm/ 整个文件夹
- model-helper.html（临时用）

### Step 2: 下载 hand_landmarker.task
打开 model-helper.html（Safari + VPN），它会自动尝试 3 个镜像地址下载。
如果 3 个都失败 → 用电脑开 VPN 下载 → 传到手机。

### Step 3: 上传 .task 到仓库根目录

### Step 4: 测试
等 1-2 分钟，打开：
`https://你的用户名.github.io/hand-negative/hand-negative.html`

状态栏应显示：
1. `Step 1/2: 加载 WASM 模块…` → `✓ WASM loaded`
2. `Step 2/2: 加载手部模型…` → `✓ Model loaded`
3. `✅ 模型就绪！请选择视频`
