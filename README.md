<p align="center">
 <img width="100px" src="public/vercel.png" align="center" alt="Deploy Python(+FastAPI) project on Vercel" />
 <h2 align="center"> LLM API 反向代理 </h2>

<p align="center">
  <a href="https://github.com/ultrasev/llmproxy-vercel/issues">
    <img alt="Issues" src="https://img.shields.io/github/issues/ultrasev/llmproxy-vercel?style=flat&color=336791" />
  </a>
  <a href="https://github.com/ultrasev/llmproxy-vercel/pulls">
    <img alt="GitHub pull requests" src="https://img.shields.io/github/issues-pr/ultrasev/llmproxy-vercel?style=flat&color=336791" />
  </a>
  <br />
</p>

众所周知，Google, Groq, Cerebras（使用了 Amazon cloudfront） 等供应商在部分国家及地区（e.g, 中国香港）不提供服务。

本项目旨在提供一个反向代理服务，解决在部分国家或地区无法直接访问的问题。

# 支持功能

- 支持供应商：Groq、Google、OpenAI
- 支持流式输出
- 兼容 OpenAI API 规范

注：大陆不可直接访问 vercel.app 域名。如想直接访问，可参考之前作者的另一个项目[llmproxy](https://github.com/ultrasev/llmproxy)，通过 cloudflare worker 部署 LLM API 反向代理。

# 示例

```python
from openai import AsyncOpenAI

```

# Vercel 一键部署

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/ultrasev/llmproxy-vercel/tree/master/llmproxy&demo-title=PythonDeployment&demo-description=Deploy&demo-url=https://llmproxy.vercel.app/&demo-image=https://vercel.com/button)

# Local Development

```bash
pip3 install -r requirements.txt
pip3 install uvicorn
uvicorn main:app --host 0.0.0.0 --port 8000 --reload
```

# License

Copyright © 2024 [ultrasev](https://github.com/ultrasev).<br />
This project is [MIT](LICENSE) licensed.
