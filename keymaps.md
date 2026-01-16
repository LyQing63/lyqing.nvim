# Mars.nvim 键位映射大全 (Keymaps)

以下是 Mars.nvim 配置中所有的快捷键映射，按功能分类。
所有的 `<leader>` 键默认为 **空格键 (Space)**。

## 1. 全局基础映射 (Global)
*文件来源: `lua/mars/keymaps.lua`*

| 键位 | 模式 | 功能 | 中文解释 |
| :--- | :--- | :--- | :--- |
| `<Esc>` | Normal | `:nohlsearch` | 清除搜索高亮 |
| `<leader>q` | Normal | `vim.diagnostic.setloclist` | 打开诊断列表 (Quickfix) |
| `tn` | Normal | `:tabnew` | 新建标签页 |
| `tj` | Normal | `:tabnext` | 下一个标签页 |
| `tk` | Normal | `:tabprevious` | 上一个标签页 |
| `tc` | Normal | `:tabclose` | 关闭当前标签页 |
| `;` | Normal | `:` | 使用分号代替冒号进入命令模式 |
| `jk` | Insert | `<Esc>` | 在输入模式下按 `jk` 快速退出到普通模式 |
| `jk` | Terminal | `<C-\><C-n>` | 在终端模式下退出到普通模式 |
| `<Esc><Esc>` | Terminal | `<C-\><C-n>` | 在终端模式下退出到普通模式 |

## 2. 文件与窗口导航 (Navigation)
*文件来源: `init.lua`, `plugins/telescope.lua`, `plugins/neo-tree.lua`, `plugins/leap.lua`*

| 键位 | 模式 | 功能 | 中文解释 |
| :--- | :--- | :--- | :--- |
| **Telescope (模糊搜索)** | | | |
| `<C-p>` | Normal | Find files | 查找文件 (同 `<leader>sf`) |
| `<leader>sf` | Normal | Find files | 查找文件 |
| `<leader>sg` | Normal | Live grep | 全局搜索关键字 (grep) |
| `<leader>sw` | Normal | Grep string | 搜索当前光标下的单词 |
| `<leader>sb` | Normal | Buffers | 查找已打开的缓冲区 |
| `<leader>sh` | Normal | Help tags | 查找帮助文档 |
| `<leader>sk` | Normal | Keymaps | 查找快捷键 |
| `<leader>sd` | Normal | Diagnostics | 查找项目诊断信息 |
| `<leader>sr` | Normal | Resume | 恢复上一次搜索 |
| `<leader>s.` | Normal | Old files | 查找最近打开的文件 |
| `<leader>/` | Normal | Current buffer fuzzy | 在当前文件中模糊搜索 |
| `<leader>s/` | Normal | Grep in open files | 在所有打开的文件中搜索 |
| `<leader>sn` | Normal | Neovim files | 查找 Neovim 配置文件 |
| **Neo-tree (文件浏览器)** | | | |
| `<C-e>` | Normal | Toggle Neo-tree | 打开/关闭文件浏览器 |
| `z` | Neo-tree | Grug-far replace | 在当前目录进行全局替换 |
| **Leap (快速跳转)** | | | |
| `e` | N/V/O | Leap forward/backward | 屏幕内快速双向跳转 |
| `E` | Normal | Leap from window | 跨窗口跳转 |
| **Tmux Navigator (窗口切换)** | | | |
| `<C-h>` | Normal | Navigate Left | 切换到左侧窗口 (支持 Vim/Tmux) |
| `<C-j>` | Normal | Navigate Down | 切换到下方窗口 (支持 Vim/Tmux) |
| `<C-k>` | Normal | Navigate Up | 切换到上方窗口 (支持 Vim/Tmux) |
| `<C-l>` | Normal | Navigate Right | 切换到右侧窗口 (支持 Vim/Tmux) |

## 3. 代码智能与 LSP (Code Intelligence)
*文件来源: `plugins/lsp.lua`, `init.lua`*

| 键位 | 模式 | 功能 | 中文解释 |
| :--- | :--- | :--- | :--- |
| `grn` | Normal | Rename | 重命名变量/函数 |
| `gra` | N/X | Code Action | 代码操作 (快速修复) |
| `grr` | Normal | References | 查找引用 |
| `gri` | Normal | Implementation | 查找实现 |
| `grd` | Normal | Definition | 跳转到定义 (当前窗口) |
| `grv` | Normal | Definition (vsplit) | 跳转到定义 (垂直分屏) |
| `grD` | Normal | Declaration | 跳转到声明 |
| `grt` | Normal | Type Definition | 跳转到类型定义 |
| `gO` | Normal | Document Symbols | 查找当前文件符号 (函数/变量等) |
| `gW` | Normal | Workspace Symbols | 查找工作区符号 |
| `L` | Normal | Line Diagnostics | 显示当前行的诊断浮窗 |
| `<leader>yd` | Normal | Yank Diagnostic | 复制当前行的诊断信息和位置 |
| `<leader>th` | Normal | Toggle Inlay Hints | 切换内联提示 (类型提示等) |
| `<leader>f` | Normal | Format | 格式化当前文件 |
| **自动补全 (Blink.cmp)** | | | |
| `<C-s>` | Insert | Show signature | 显示/隐藏函数签名帮助 |
| `<C-l>` | Insert | Show docs | 显示/隐藏文档 |
| `<C-j>` | Insert | Select next | 选择下一个补全项 |
| `<C-k>` | Insert | Select prev | 选择上一个补全项 |
| `<CR>` | Insert | Accept | 接受选中的补全项 |

## 4. Git 版本控制 (Git)
*文件来源: `plugins/gitsigns.lua`, `init.lua`*

| 键位 | 模式 | 功能 | 中文解释 |
| :--- | :--- | :--- | :--- |
| `<leader>ng` | Normal | Neogit | 打开 Neogit (Git 客户端界面) |
| `]c` | Normal | Next Hunk | 跳转到下一个变更块 |
| `[c` | Normal | Prev Hunk | 跳转到上一个变更块 |
| `<leader>hs` | N/V | Stage Hunk | 暂存当前块 |
| `<leader>hr` | N/V | Reset Hunk | 重置当前块 (放弃更改) |
| `<leader>hS` | Normal | Stage Buffer | 暂存当前文件所有更改 |
| `<leader>hu` | Normal | Undo Stage Hunk | 撤销暂存当前块 |
| `<leader>hR` | Normal | Reset Buffer | 重置当前文件所有更改 |
| `<leader>hp` | Normal | Preview Hunk | 预览当前块 |
| `<leader>hb` | Normal | Blame Line | 显示当前行的 Git Blame |
| `<leader>hd` | Normal | Diff Index | 与索引(暂存区)对比差异 |
| `<leader>hD` | Normal | Diff Commit | 与上一次提交对比差异 |
| `<leader>tb` | Normal | Toggle Blame | 切换行内 Blame 显示 |
| `<leader>tD` | Normal | Toggle Deleted | 切换显示已删除的内容 |

## 5. 调试 (Debugging)
*文件来源: `plugins/debug.lua`*

| 键位 | 模式 | 功能 | 中文解释 |
| :--- | :--- | :--- | :--- |
| `<F5>` | Normal | Continue | 开始调试 / 继续运行 |
| `<F1>` | Normal | Step Into | 单步进入 |
| `<F2>` | Normal | Step Over | 单步跳过 |
| `<F3>` | Normal | Step Out | 单步跳出 |
| `<F7>` | Normal | Toggle UI | 切换调试界面 |
| `<leader>b` | Normal | Toggle Breakpoint | 切换断点 |
| `<leader>B` | Normal | Set Condition BP | 设置条件断点 |

## 6. AI 助手 (OpenCode)
*文件来源: `plugins/ai.lua`*

| 键位 | 模式 | 功能 | 中文解释 |
| :--- | :--- | :--- | :--- |
| `<C-a>` | N/X | Ask | 向 AI 提问 (选中代码或当前位置) |
| `<C-x>` | N/X | Select Action | 选择 AI 操作菜单 |
| `<C-.>` | N/X | Toggle | 切换 AI 聊天窗口 |
| `go` | N/X | Add to Context | 将选中范围添加到 AI 上下文 |
| `goo` | Normal | Add Line | 将当前行添加到 AI 上下文 |

## 7. 其他工具 (Others)
*文件来源: `init.lua`*

| 键位 | 模式 | 功能 | 中文解释 |
| :--- | :--- | :--- | :--- |
| `<leader>gs` | Normal | Grug Far | 打开全局查找替换窗口 |

## 8. 代码折叠 (Folding)
*文件来源: `lua/mars/options.lua` (启用 Treesitter 折叠)*

| 键位 | 模式 | 功能 | 中文解释 |
| :--- | :--- | :--- | :--- |
| `za` | Normal | Toggle Fold | 切换折叠/展开 (当前代码块) |
| `zM` | Normal | Close All | 折叠所有代码 (概览模式) |
| `zR` | Normal | Open All | 展开所有代码 |
| `zo` | Normal | Open Fold | 展开当前折叠 |
| `zc` | Normal | Close Fold | 折叠当前代码块 |
