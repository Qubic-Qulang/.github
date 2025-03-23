![Banner](./qulang-banner-rounded.png)

---

<div align="center">
  Try the dApp and playground at [http://46.17.103.110:3000/](http://46.17.103.110:3000/) !  
  You can use a private seed such as `kexrupgtmbmwwzlcpqccemtgvolpzqezybmgaedaganynsnjijfyvcn`.
</div>

---

QuLang brings together AI builders across the _Qubic_ blockchain. Its goal is to enable decentralized inference of Large Language Models (LLMs) and AI Agents. Here's how it works:

- Users can top up their QuLang accounts through the smart contract (`procedure TopUp, 1`) and withdraw their balance using the same mechanism (`procedure Withdraw, 2`).

- Providers can register endpoints for LLM inference following the [Vercel AI SDK UI](https://sdk.vercel.ai/docs/ai-sdk-ui/overview) standard (an example is available in the [`example-openai-provider`](https://github.com/Qubic-Qulang/example-openai-provider) repository). The endpoints are stored in a centralized PostgreSQL database, while pricing (input token price, output token price) and burn rate parameters are managed by the smart contract (`procedure updateProvider, 3`).

- Inference transactions are validated through a main endpoint. Users with sufficient QuLang balances are debited an amount calculated by:

$$ D = n_{\text{input token}} \times p_{\text{input token}} + n_{\text{output token}} \times p_{\text{output token}} $$

The AI provider receives a credit of $D \times (1 - r_{\text{burn}})$, and the remaining amount $r_{\text{burn}} \times D$ is either burned or credited to the contract’s shares.

*Important note:* Some features, particularly security measures and exception handling, are not yet fully developed.

## Projects

### 1. core (Node and Smart Contract)

A fork of the Qubic node with our smart contract implementation.  
- **Code:** [https://github.com/Qubic-Qulang/core/blob/madrid-2025/src/contracts/HM25.h](https://github.com/Qubic-Qulang/core/blob/madrid-2025/src/contracts/HM25.h)  
- **Node endpoint:** [http://46.17.103.110:31841/](http://46.17.103.110:31841/)  
- **RPC endpoint:** [http://46.17.103.110/v1/tick-info](http://46.17.103.110/v1/tick-info)

### 2. qulang-app (Main dApp)

- **URL:** [http://46.17.103.110:3000/](http://46.17.103.110:3000/)  
- **Repository:** [https://github.com/Qubic-Qulang/qulang-app](https://github.com/Qubic-Qulang/qulang-app)

### 3. example-openai-provider

- **Endpoint instance:** [http://46.17.103.110:3001/](http://46.17.103.110:3001/)  
- **Repository:** [https://github.com/Qubic-Qulang/example-openai-provider](https://github.com/Qubic-Qulang/example-openai-provider)

This Next.js application demonstrates how AI providers can register with the QuLang marketplace. The API exposes model details (provider name, image, and description) via environment variables. It also includes a playground chatbot interface for easy testing and debugging of AI inference.
