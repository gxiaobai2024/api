AI  [https://github.com/copilot/    ](https://github.com/copilot/)
ai   https://www.deepseek.com/
https://vgo.pub/  **下载高清视频
**
azure 注册：https://azure.microsoft.com/
azure AI 平台：https://ai.azure.com/
CherryStudio：https://cherry-ai.com/
火山引擎：https://www.volcengine.com
硅基流动：https://www.siliconflow.com/zh/home
OpenWeb UI:  https://github.com/open-webui/open-webui
秘塔AI搜索：https://metaso.cn/
Perplexity搜索： https://www.perplexity.ai/
https://grok.dairoot.cn/
https://grok.dairoot.cn/admin
https://aistudio.google.com/prompts/new_chat?pli=1




(免费AI
直接使用站点
https://chat.bestip.one
支持deepseek-r1 o1 o3-mini-high 等
模型名字后面带有search的启用了联网功能
免费接口
```
https://ai.bestip.one
sk-LWaFHAG2PGwWZeBHmn0RkrTlsjZ9m78f2DuYWkxqWZkeZuY4
```
https://next.bestip.one
openwebui 界面更美观 支持联网插件
https://chat.bestip.one
支持deepseek-r1 o1 o3-mini-high 等
模型名字后面带有search的启用了联网功能
免费接口
```
https://ai.bestip.one
sk-LWaFHAG2PGwWZeBHmn0RkrTlsjZ9m78f2DuYWkxqWZkeZuY4
```)
grokAI            https://grok.com/
v2rayN 最新版点击这里(https://github.com/2dust/v2rayN/releases)

cloudflare点击这里(https://dash.cloudflare.com/)

部署代码：点击这里(https://github.com/yonggekkk/Cloudflare_vless_trojan)
CM大佬项目: https://github.com/cmliu/edgetunnel
3K大佬项目: https://github.com/6Kmfi6HP/EDtunnel
勇哥大佬项目:[ https://github.com/yonggekkk/Cloudfla...](https://github.com/yonggekkk/Cloudflare_vless_trojan)

uuid生成：点击这里(https://1024tools.com/uuid)

workers win专用ip优选：点击这里(https://jdssl.top/wp-content/uploads/2023/07/works%E4%B8%93%E7%94%A8ip%E4%BC%98%E9%80%89.zip)

ip查看：点击这里(https://whatismyipaddress.com/)

cf ip优选；点击这里(https://stock.hostmonit.com/CloudFlareYes)

网络测速：点击这里(https://www.speedtest.net/result/14952074175)


一、准备工作
域名

建议你先拥有一个免费的二级域名（如 L53 等服务商）或自有付费域名。
域名需在 Cloudflare 完成解析、指向。
Cloudflare 账号

在 Cloudflare Dashboard 里添加你的域名，并确保状态为 Active。
Workers 功能无需付费，可免费使用一定额度的请求数。
BPB 面板项目
- 原项目的 GitHub 地址及其混淆版脚本。 - 建议先 Star 一下作者的仓库，以表示对开源项目的支持。

可选：IP 优选脚本

若要获得更佳速度，可借助自己编写或第三方的脚本优选最适合你网络环境的 Cloudflare IP。
安全 & 合法使用

Cloudflare 不允许用于 “反代” 的行为。如要继续，请做好隐藏或更改 回退域名，避免被他人投诉。
本文只作技术交流，请遵守当地法律法规。
二、创建 Workers 并部署 BPB 脚本
新建 Workers

进入 Cloudflare 后台，左侧菜单找到「Workers & Pages」。
点 Create a Service，选择「Hello World」模板，命名项目（如 test）。
创建完毕后，默认会部署一个 “Hello World” 示例。
删除默认代码 & 粘贴混淆脚本

点击「Edit code」，清空默认示例内容。
到 BPB 项目仓库中找到 https://github.com/bia-pain-bache/BPB-Worker-Panel/blob/main/_worker.js 文件下的 混淆版脚本；复制其中所有内容。
在 Cloudflare 编辑器里粘贴覆盖 → 点击「Save and deploy」。
自定义域名

返回 Workers → Settings → Custom Domains / Routes。
添加你在 Cloudflare 绑定的域名前缀（如 panel.yourdomain.com 或 pp.yourdomain.example）。
若页面提示「已绑定成功」，则说明可通过该域名访问 Workers。
三、配置变量 (Variables) & KV 存储
当你访问该 Workers 时，若出现报错提示 “需要 UUID / Trojan 密码 / KV 命名空间” 等信息，可按以下步骤设置：

添加 Variables (UUID / Trojan 密码 / 回退域名)

进入 Workers → Settings → Variables → Environment Variables。
分别设置：
UUID：大写，值为你想要的 UUID（可在 uuidgenerator.net 或其他工具生成）。
TR_PASS ：大写 / 小写以项目作者说明为准，值为你设置的 Trojan 密码。
（可选）FALLBACK：默认为其他域名可能会带来风险；建议改成 example.com 或任意无业务的公共域名，降低被投诉 / 封号概率。
创建并绑定 KV 命名空间

在 Cloudflare Dashboard 左侧找到「KV」或「存储」。
新建一个命名空间（如 test），保存后回到 Workers → Settings → KV Namespace。
绑定小写 kv （或项目提示的名称）到你新建的命名空间 test。
再次部署并刷新页面，测试若能正常访问，则说明 KV 绑定成功。
四、访问 BPBM 面板 & 修改默认设置
面板路径

默认情况下，若你的域名是 panel.yourdomain.com，则面板访问地址为 https://panel.yourdomain.com/panel。
第一次打开会要求设置面板登录密码，请牢记。
初始化面板

登录后，会看到一个类似管理后台的界面，能对「Trojan / VLess / 」等协议进行开启 / 关闭、查看订阅链接等。
建议勾选常用协议（如 Trojan / VLess / ），然后点击「保存 & 部署订阅」。
安全注意事项

参照上文，最好添加 FALLBACK 变量，让默认访问跳到 example.com 而非原项目的回退域名，以防止潜在的 Cloudflare 违规举报。
若想进一步强化安全，可使用自定义伪装路径、在订阅配置里改域名等方式减少可检测性。
五、添加 IP 优选 & 提升速度
BPB 面板默认会提供 70+ 节点规则，但未必适合你的网络。你可以：

使用官方 IP 或 FOFA 搜索

优选官方 Cloudflare IP：选取与当地线路更匹配的 IP，减少中转延迟。
或在 FOFA 搜索合适的 Cloudflare 节点（排除 asn="13335" 等），并测试延迟。
脚本优选

# mac 或者Linux
curl -L -O jhb.ovh/jb/gfip.sh
bash gfip.sh
# Windows
powershell -ExecutionPolicy Bypass -Command "Invoke-WebRequest -Uri 'https://joeyblog.net/jb/gfip.ps1' -OutFile 'gfip.ps1'; & './gfip.ps1'"
将优选出来的 IP（多条用英文逗号分隔）填入面板的「IP 填写区」，保存后自动生成新订阅。
在客户端导入新订阅
复制面板给出的订阅链接。
打开 V2RayN / Clash 等工具，「添加订阅」并刷新。
测试可用性和速度，如 Speedtest、YouTube 4K 等。若满意即可长期使用，若不理想则重复优选步骤。
六、常见问题 & 说明
为什么要改回退域名 (FALLBACK)？
默认回退不安全，可能被 Cloudflare 投诉，导致账号封禁。改为 example.com 类公共域名，可尽量规避。
绑定 KV 一直报错？
确保命名空间名称写对，如小写的 kv，在面板或混淆脚本里须与之对应。
免费套餐是否稳定？
Cloudflare 免费 Workers 有请求数 / CPU 时间等限制，普通个人使用够用，如流量极大需考虑付费或其他替代。
免费域名到期怎么办？
一般是 3 ~ 12 个月免费期，需及时在注册商后台续期；或更换其他域名。
七、结语
至此，你已拥有一个使用 BPB 面板 管理的 Cloudflare Workers 节点：

BPBM 面板：可视化开启多协议、查看订阅、测试流量情况。
自定义反代回退：保护 Cloudflare 账号安全，降低被官方警告 / 封号的概率。
KV 存储：用来持久化你的面板数据、账号配置等。
IP 优选：进一步改善连接速度与稳定性，让 0 成本节点也能流畅看 YouTube。
最后声明：


openclash转换订阅网址：点击这里https://sub-web.netlify.app/()

免费域名注册：点击这里(https://www.youtube.com/watch?v=oL421WyF6KY&t=59s)
  全球主流国家城市的节点   https://openproxylist.com/
