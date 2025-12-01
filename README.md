# XMRig

**High-performance Monero (XMR) CPU & GPU miner**  
RandomX • kHeavyHash • GhostRider • Argon2 • CPU-optimized for maximum hashrate

## Supported Algorithms & Dev Fee

| Algorithm     | Dev Fee | Example Coins                  |
|---------------|---------|--------------------------------|
| randomx       | 1.00%   | Monero (XMR), ArQmA            |
| rx/0          | 1.00%   | Monero variant                 |
| rx/arq         | 1.00%   | ArQmA                          |
| rx/sfx        | 1.00%   | Safexcoin                      |
| rx/wow        | 1.00%   | Wownero                         |
| kheavyhash    | 1.00%   | Ravencoin (RVN)                |
| ghostrider    | 1.00%   | Raptoreum (RTM)                |
| argon2id_chukwa| 1.00%   | Chukwa                          |
| cn/r         | 1.00%   | Masari (MSR)                   |
| cn/2          | 1.00%   | Monero Classic                 |
| cn/gpu        | 1.00%   | Monero (GPU)                   |

All fees: 1% (60-second rounds) · Open-source & donation-based

## Features
- Highest RandomX hashrate on modern CPUs (Intel/AMD/ARM)
- Full OpenCL/CUDA/OpenMP support for AMD/NVIDIA/Intel GPUs
- Advanced CPU affinity & huge pages optimization
- Low-latency stratum protocol & failover pools
- Built-in HTTPS/TLS support for secure connections
- JSON API & web console for monitoring
- Benchmark mode & hashrate benchmarking
- Configurable threads, intensity, & memory modes
- Watchdog & health checks for 24/7 operation
- Cross-platform: Windows · Linux · macOS · FreeBSD · Android
- ARM support (Raspberry Pi, mobile devices)

## Supported Hardware

**CPU**  
Intel Core i3/i5/i7/i9 · Xeon · AMD Ryzen · EPYC · Threadripper  
ARM: Apple M1/M2/M3 · Raspberry Pi 4/5 · Qualcomm Snapdragon

**GPU**  
AMD RX 5000–9000 · Vega · Polaris  
NVIDIA GTX 10xx–RTX 50xx (CUDA)  
Intel Arc A-series (OpenCL)

## Quick Start

**Basic RandomX (Monero)**
```bash
./xmrig -o pool.supportxmr.com:443 -u YOUR_MONERO_WALLET -p worker1 --tls --coin monero



{
    "algo": "rx/0",
    "coin": "monero",
    "pools": [
        {
            "url": "pool.example.com:3333",
            "user": "YOUR_WALLET_ADDRESS",
            "pass": "rig1",
            "tls": false
        }
    ],
    "cpu": { "enabled": true, "max-threads-hint": 100 },
    "opencl": { "enabled": true },
    "cuda": { "enabled": true }
}
