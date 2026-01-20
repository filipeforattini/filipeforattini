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

</div>

---

## What I'm Building

I create **zero-dependency**, **production-ready** libraries that solve real problems. No bloat. No unnecessary abstractions. Just tools that work.

<table>
<tr>
<td width="50%" valign="top">

### [**s3db.js**](https://github.com/forattini-dev/s3db.js)
**Document Database on S3**

Transform AWS S3 into a fully functional document database. ORM-like interface, field-level encryption, streaming API, and 30+ field types. Pay only for storage.

[![npm](https://img.shields.io/npm/v/s3db.js?color=brightgreen&style=flat-square)](https://www.npmjs.com/package/s3db.js)
[![npm downloads](https://img.shields.io/npm/dm/s3db.js?color=blue&style=flat-square)](https://www.npmjs.com/package/s3db.js)

```javascript
const users = await db.createResource({
  name: 'users',
  attributes: {
    email: 'email|required|unique',
    password: 'secret|required'
  }
});
await users.insert({ email: 'hi@me.com', password: 'x' });
```

</td>
<td width="50%" valign="top">

### [**recker**](https://github.com/forattini-dev/recker)
**Multi-Protocol SDK for the AI Era**

9 protocols unified: HTTP, WebSocket, DNS, WHOIS, RDAP, FTP, SFTP, Telnet, HLS. AI-native with OpenAI, Anthropic, Google built-in. 48 API presets. MCP server with 65 tools.

[![npm](https://img.shields.io/npm/v/recker?color=F5A623&style=flat-square)](https://www.npmjs.com/package/recker)
[![npm downloads](https://img.shields.io/npm/dm/recker?color=34C759&style=flat-square)](https://www.npmjs.com/package/recker)

```javascript
import { get, whois, dns } from 'recker';

const users = await get('https://api.com/users').json();
const info = await whois('github.com');
const ips = await dns('google.com');
```

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [**tuiuiu.js**](https://github.com/forattini-dev/tuiuiu.js)
**Terminal UI Framework**

Build beautiful, reactive terminal apps. Signal-based reactivity, Flexbox layout, full mouse support. 50+ components. Zero dependencies. Pure Node.js.

[![npm](https://img.shields.io/npm/v/tuiuiu.js?color=F5A623&style=flat-square)](https://www.npmjs.com/package/tuiuiu.js)
[![npm downloads](https://img.shields.io/npm/dm/tuiuiu.js?color=34C759&style=flat-square)](https://www.npmjs.com/package/tuiuiu.js)

```javascript
import { render, Box, Text, useState } from 'tuiuiu.js';

function App() {
  const [count, setCount] = useState(0);
  return Box({ padding: 1 },
    Text({ color: 'cyan' }, `Count: ${count()}`)
  );
}
```

</td>
<td width="50%" valign="top">

### [**raffel**](https://github.com/forattini-dev/raffel)
**Build APIs Like Express. Scale Like Nothing Else.**

Write once, expose everywhere. Same handler works over HTTP, WebSocket, JSON-RPC, gRPC, and GraphQL. Zero extra code. Express-like DX.

[![npm](https://img.shields.io/npm/v/raffel?color=8b5cf6&style=flat-square)](https://www.npmjs.com/package/raffel)

```javascript
const app = createServer({ port: 3000 })

app.get('/users/:id', async ({ id }) => {
  return db.users.findById(id)
})

// Works: HTTP, WebSocket, JSON-RPC, gRPC
await app.start()
```

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [**vaulter**](https://github.com/forattini-dev/vaulter)
**Environment & Secrets Manager**

Stop committing `.env` files. Encrypted storage (AES-256-GCM), multi-backend (S3, MinIO, R2), monorepo support. Export to K8s, Helm, Terraform, Docker. MCP server with 30 tools.

[![npm](https://img.shields.io/npm/v/vaulter?color=F5A623&style=flat-square)](https://www.npmjs.com/package/vaulter)

```bash
vaulter init
vaulter var set DATABASE_URL="postgres://..." -e prd
vaulter export k8s-secret -e prd | kubectl apply -f -
```

</td>
<td width="50%" valign="top">

### [**cli-args-parser**](https://github.com/forattini-dev/cli-args-parser)
**Expressive CLI Argument Parser**

Zero dependencies. Expressive `key=value`, `key:=typed`, `Key:Meta` syntax. Nested subcommands. Custom validation. Shell completion. 431 tests.

[![npm](https://img.shields.io/npm/v/cli-args-parser?color=F5A623&style=flat-square)](https://www.npmjs.com/package/cli-args-parser)
[![Zero Dependencies](https://img.shields.io/badge/deps-0-success?style=flat-square)](https://www.npmjs.com/package/cli-args-parser)

```javascript
parse(['name=Filipe', 'age:=35', '--verbose'])
// { data: { name: 'Filipe', age: 35 }, flags: { verbose: true } }
```

</td>
</tr>
<tr>
<td colspan="2" valign="top">

### [**redblue**](https://github.com/forattini-dev/redblue)
**The Ultimate Security Arsenal in a Single Binary**

30+ security tools in one 2.7MB binary. Zero dependencies. 100% Rust. Port scanning, subdomain enumeration, web fuzzing, vulnerability intelligence, secrets detection, encrypted vault, and a multi-modal database (tables + graphs + vectors).

[![Rust](https://img.shields.io/badge/rust-1.70%2B-orange?style=flat-square)](https://www.rust-lang.org)
[![Size](https://img.shields.io/badge/size-2.7MB-green?style=flat-square)](https://github.com/forattini-dev/redblue/releases)

```bash
rb network scan ports 192.168.1.1 --type syn    # SYN scan
rb recon domain subdomains example.com          # Subdomain enum
rb web fuzz http://target.com/FUZZ -w words.txt # Web fuzzing
rb intel vuln search nginx 1.18.0               # CVE lookup
rb crypto vault encrypt secrets.txt             # AES-256-GCM vault
```

</td>
</tr>
</table>

---

## The Philosophy

Every library I build follows these principles:

| Principle | Why |
|:----------|:----|
| **Zero Dependencies** | No supply chain attacks. No version conflicts. No bloat. |
| **TypeScript-First** | Full type safety. Great IDE support. Self-documenting APIs. |
| **MCP-Ready** | AI assistants (Claude, Cursor) can use my tools natively. |
| **Production-Ready** | Not toys. Used in real systems. Thoroughly tested. |

---

## By the Numbers

| Metric | Value |
|:-------|:------|
| **s3db.js** | 60+ examples, 12 plugins, MCP server |
| **recker** | 9 protocols, 48 presets, 65 MCP tools, 4200+ tests |
| **tuiuiu.js** | 50+ components, 11 themes, 5300+ tests |
| **redblue** | 30+ tools, multi-modal DB, 2.7MB binary |
| **vaulter** | 30 MCP tools, exports to 8 formats |

---

<div align="center">

### Let's Connect

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/filipeforattini)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/filipeforattini)

---

*All projects are MIT licensed. Open source. Free forever.*

</div>
