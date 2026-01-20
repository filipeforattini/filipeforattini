<div align="center">

# Hey, I'm Filipe Forattini

### Building tools that developers actually want to use.

[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)

**AI Enthusiast** — Building the future with my favorites:

[![Claude](https://img.shields.io/badge/Claude_Opus_&_Sonnet-191919?style=flat-square&logo=anthropic&logoColor=white)](https://anthropic.com)
[![GPT](https://img.shields.io/badge/GPT_5.2-412991?style=flat-square&logo=openai&logoColor=white)](https://openai.com)
[![Gemini](https://img.shields.io/badge/Gemini_3-4285F4?style=flat-square&logo=google&logoColor=white)](https://deepmind.google)

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&color=8B5CF6&center=true&vCenter=true&width=435&lines=Zero+dependencies.+Maximum+power.;MCP-ready+for+AI+assistants.;Open+source.+Free+forever." alt="Typing SVG" />

---

<img src="https://github-readme-stats.vercel.app/api?username=filipeforattini&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=8B5CF6&icon_color=8B5CF6" alt="GitHub Stats" />

<img src="https://github-readme-activity-graph.vercel.app/graph?username=filipeforattini&theme=tokyo-night&hide_border=true&bg_color=0D1117&color=8B5CF6&line=8B5CF6&point=FF6B6B" alt="Activity Graph" />

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=filipeforattini&layout=compact&theme=tokyonight&hide_border=true&bg_color=0D1117&title_color=8B5CF6" alt="Top Languages" />

![Profile Views](https://komarev.com/ghpvc/?username=filipeforattini&color=8B5CF6&style=flat-square)

</div>

---

## Quick Nav

| Project | What it does |
|:--------|:-------------|
| [**s3db.js**](#s3dbjs) | Document database on S3 with ORM-like API |
| [**recker**](#recker) | Multi-protocol SDK (HTTP, WS, DNS, WHOIS, FTP...) |
| [**tuiuiu.js**](#tuiuiujs) | Terminal UI framework with 50+ components |
| [**genetics-ai.js**](#genetics-aijs) | Evolve neural networks with genetic algorithms |
| [**raffel**](#raffel) | Multi-protocol API server (Express-like DX) |
| [**vaulter**](#vaulter) | Encrypted secrets manager with K8s/Terraform export |
| [**cli-args-parser**](#cli-args-parser) | Zero-dep CLI argument parser |
| [**redblue**](#redblue) | Security toolkit in Rust (30+ tools, 2.7MB) |

---

## s3db.js

**Transform AWS S3 into a fully functional document database.**

[![npm](https://img.shields.io/npm/v/s3db.js?style=flat-square)](https://www.npmjs.com/package/s3db.js)
[![downloads](https://img.shields.io/npm/dm/s3db.js?style=flat-square)](https://www.npmjs.com/package/s3db.js)
[![GitHub](https://img.shields.io/github/stars/forattini-dev/s3db.js?style=flat-square)](https://github.com/forattini-dev/s3db.js)

ORM-like interface. Field-level encryption (AES-256-GCM). Streaming API. 30+ field types. 12 plugins. MCP server included. Pay only for S3 storage.

```javascript
const db = new S3db({ uri: 's3://key:secret@bucket?region=us-east-1' })

const users = await db.createResource({
  name: 'users',
  attributes: {
    email: 'email|required|unique',
    password: 'secret|required',
    role: 'enum:admin,user|default:user'
  }
})

await users.insert({ email: 'dev@example.com', password: 'secure123' })
const admins = await users.query({ role: 'admin' })
```

---

## recker

**Multi-Protocol SDK for the AI Era.**

[![npm](https://img.shields.io/npm/v/recker?style=flat-square)](https://www.npmjs.com/package/recker)
[![downloads](https://img.shields.io/npm/dm/recker?style=flat-square)](https://www.npmjs.com/package/recker)
[![GitHub](https://img.shields.io/github/stars/forattini-dev/recker?style=flat-square)](https://github.com/forattini-dev/recker)

9 protocols unified: HTTP, WebSocket, DNS, WHOIS, RDAP, FTP, SFTP, Telnet, HLS. 48 API presets (OpenAI, Anthropic, Stripe, GitHub...). 65 MCP tools. 4200+ tests.

```javascript
import { get, post, whois, dns, ftp } from 'recker'

// HTTP with automatic retry, cache, auth
const users = await get('https://api.example.com/users').json()

// Multi-protocol in the same codebase
const domainInfo = await whois('github.com')
const records = await dns('google.com', { type: 'MX' })
const files = await ftp('ftp://server.com').list('/pub')

// AI-native
import { anthropic } from 'recker'
const response = await anthropic.chat('Explain recursion')
```

---

## tuiuiu.js

**Terminal UI Framework. Zero Dependencies. Pure Node.js.**

[![npm](https://img.shields.io/npm/v/tuiuiu.js?style=flat-square)](https://www.npmjs.com/package/tuiuiu.js)
[![downloads](https://img.shields.io/npm/dm/tuiuiu.js?style=flat-square)](https://www.npmjs.com/package/tuiuiu.js)
[![GitHub](https://img.shields.io/github/stars/forattini-dev/tuiuiu.js?style=flat-square)](https://github.com/forattini-dev/tuiuiu.js)

Signal-based reactivity. Flexbox layout engine. Full mouse support. 50+ components. 11 themes. 5300+ tests. MCP server included.

```javascript
import { render, Box, Text, Button, createSignal } from 'tuiuiu.js'

const [count, setCount] = createSignal(0)

render(() =>
  Box({ padding: 2, border: 'rounded', flexDirection: 'column' },
    Text({ color: 'cyan', bold: true }, `Count: ${count()}`),
    Button({
      onClick: () => setCount(c => c + 1),
      variant: 'primary'
    }, 'Increment')
  )
)
```

---

## genetics-ai.js

**Evolve neural networks with genetic algorithms. No training data needed.**

[![npm](https://img.shields.io/npm/v/genetics-ai.js?style=flat-square)](https://www.npmjs.com/package/genetics-ai.js)
[![GitHub](https://img.shields.io/github/stars/forattini-dev/genetics-ai.js?style=flat-square)](https://github.com/forattini-dev/genetics-ai.js)

NEAT speciation. Multi-objective (NSGA-II). Novelty search. Hill climbing. 262 tests. ~8k brain ticks/second. Built-in profiler and visualizer.

```javascript
import { Generation, Individual } from 'genetics-ai.js'

class Creature extends Individual {
  fitness() {
    return this.distance  // Further = better
  }
}

const gen = new Generation({ size: 100, individualClass: Creature })
gen.fillRandom()

for (let i = 0; i < 100; i++) {
  await gen.tickAsync()
  gen.population.sort((a, b) => b.fitness() - a.fitness())
  gen.population.slice(-30).forEach(ind => ind.dead = true)
  gen = await gen.nextAsync()  // Evolution!
}
```

---

## raffel

**Build APIs Like Express. Scale Like Nothing Else.**

[![npm](https://img.shields.io/npm/v/raffel?style=flat-square)](https://www.npmjs.com/package/raffel)
[![GitHub](https://img.shields.io/github/stars/forattini-dev/raffel?style=flat-square)](https://github.com/forattini-dev/raffel)

Write once, expose everywhere. Same handler works over HTTP, WebSocket, JSON-RPC, gRPC, and GraphQL. Zero extra code.

```javascript
import { createServer } from 'raffel'

const app = createServer({
  port: 3000,
  websocket: { path: '/ws' },
  jsonrpc: { path: '/rpc' }
})

app.get('/users/:id', async ({ id }) => {
  return db.users.findById(id)
})

app.post('/users', async (body) => {
  return db.users.create(body)
})

await app.start()
// Same handlers now work via HTTP, WebSocket, and JSON-RPC
```

---

## vaulter

**Stop committing .env files.**

[![npm](https://img.shields.io/npm/v/vaulter?style=flat-square)](https://www.npmjs.com/package/vaulter)
[![GitHub](https://img.shields.io/github/stars/forattini-dev/vaulter?style=flat-square)](https://github.com/forattini-dev/vaulter)

Encrypted storage (AES-256-GCM). Multi-backend (S3, MinIO, R2). Monorepo support. Export to K8s, Helm, Terraform, Docker. 30 MCP tools.

```bash
# Initialize and store secrets
vaulter init --backend s3://my-bucket/secrets
vaulter set DATABASE_URL="postgres://prod:5432/db" -e prd
vaulter set API_KEY="sk-live-xxx" -e prd --tags sensitive

# Export to any format
vaulter export k8s-secret -e prd | kubectl apply -f -
vaulter export helm-values -e prd > values.yaml
vaulter export tfvars -e prd > terraform.tfvars
```

---

## cli-args-parser

**Zero-dependency CLI argument parser.**

[![npm](https://img.shields.io/npm/v/cli-args-parser?style=flat-square)](https://www.npmjs.com/package/cli-args-parser)
[![deps](https://img.shields.io/badge/dependencies-0-success?style=flat-square)](https://www.npmjs.com/package/cli-args-parser)
[![GitHub](https://img.shields.io/github/stars/forattini-dev/cli-args-parser?style=flat-square)](https://github.com/forattini-dev/cli-args-parser)

Expressive syntax: `key=value`, `key:=typed`, `Key:Meta`. Nested subcommands. Custom validation. Shell completion. 431 tests.

```javascript
import { parse } from 'cli-args-parser'

parse(['user=filipe', 'age:=30', 'admin:=true', '--verbose', '-f'])
// {
//   data: { user: 'filipe', age: 30, admin: true },
//   flags: { verbose: true, f: true }
// }
```

---

## redblue

**The Ultimate Security Arsenal in a Single Binary.**

[![Rust](https://img.shields.io/badge/rust-1.70+-orange?style=flat-square)](https://www.rust-lang.org)
[![size](https://img.shields.io/badge/binary-2.7MB-green?style=flat-square)](https://github.com/forattini-dev/redblue/releases)
[![GitHub](https://img.shields.io/github/stars/forattini-dev/redblue?style=flat-square)](https://github.com/forattini-dev/redblue)

30+ security tools. Zero dependencies. 100% Rust. Port scanning, subdomain enumeration, web fuzzing, CVE lookup, secrets detection, encrypted vault, multi-modal database (tables + graphs + vectors).

```bash
# Network reconnaissance
rb network scan ports 192.168.1.0/24 --type syn --top-ports 1000
rb network scan services 10.0.0.1 -p 80,443,8080

# Domain intelligence
rb recon domain subdomains example.com --recursive
rb recon domain tech-stack example.com

# Web security
rb web fuzz http://target.com/FUZZ -w wordlist.txt --threads 50
rb web crawl http://target.com --depth 3

# Vulnerability intelligence
rb intel vuln search nginx 1.18.0
rb intel vuln details CVE-2021-44228

# Crypto & secrets
rb crypto vault create secrets.vault
rb crypto vault encrypt data.json -o data.enc
```

---

<div align="center">

## The Philosophy

**Zero Dependencies** · **TypeScript-First** · **MCP-Ready** · **Production-Ready**

No supply chain attacks. Full type safety. AI assistants can use my tools natively. Not toys—used in real systems.

---

### Let's Connect

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/filipeforattini)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/filipeforattini)

*All projects are MIT licensed. Open source. Free forever.*

</div>
