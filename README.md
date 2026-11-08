<div align="center">

# Vaibhav Binwal

### RISC-V open-source contributor · Systems engineer · IIT Jodhpur

*I work where the ISA meets the metal: auditing processor RTL against the spec, fixing trap handling in the official compliance suite, and building kernel-bypass systems that I measure against real baselines.*

[![Portfolio](https://img.shields.io/badge/Portfolio-vaibhav805.github.io-C85A32?style=for-the-badge&logo=googlechrome&logoColor=white)](https://vaibhav805.github.io)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-vaibhav--binwal-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/vaibhav-binwal-93670236a/)
[![Email](https://img.shields.io/badge/Email-binwalvaibhav%40gmail.com-1C1B1A?style=for-the-badge&logo=gmail&logoColor=white)](mailto:binwalvaibhav@gmail.com)

</div>

---

### 🔭 Right now

- **LFX Mentorship Fall 2026 (interview stage):** hardware-enforced **CFI** (Zicfiss shadow stack, Zicfilp landing pads) in the **Sargantana** RISC-V core
- **B.Tech major project:** a RISC-V SoC with a custom **systolic-array coprocessor** for genomic sequence alignment, driven through custom ISA extensions over RoCC/AXI-DMA and verified with Spike and Verilator

---

### 🧩 RISC-V open source

| Project | Contribution | Status |
|---|---|---|
| [**bsc-loca/sargantana**](https://github.com/bsc-loca/sargantana) | Audited the FP instruction decoder against the ISA spec and found **6 legality bugs**: Q-format encodings not trapping, and reserved `rs2` fields accepted on FSQRT, FCVT, FMV and FCLASS | 6 issues raised · fixes in progress |
| [**riscv/riscv-arch-test**](https://github.com/riscv/riscv-arch-test) | [#1727](https://github.com/riscv/riscv-arch-test/issues/1727): a secondary trap clobbered `mcause` in failure diagnostics · [#1753](https://github.com/riscv/riscv-arch-test/issues/1753): `ExceptionsS` aborted on misaligned load/store | ✅ 2 merged |
| [**OpenMathLib/OpenBLAS**](https://github.com/OpenMathLib/OpenBLAS/pull/5819) | Found that the RVV kernels were never selected by the build, so `RISCV64_GENERIC` silently produced scalar code. Fixed the kernel routing and validated **724 RVV instrs**, **42/42 DGEMM** cases, BLAS L1–L3 and LAPACK | ✅ merged (#5819) |
| HAL Transitional Libraries | LFX Spring: riscv64 cross-compile and validation pipeline, plus `hal/simd.h` with RVV, AVX2+FMA, SSE2 and scalar backends | LFX |

---

### ⚡ Systems projects

<table>
<tr>
<td width="50%" valign="top">

#### [ZeroKV](https://github.com/Vaibhav805/ZeroKV)
`Rust` `RDMA` `libibverbs` `RoCE`

A key-value store where a **GET never wakes the server**: one-sided RDMA READs straight into remote memory, plus HERD-style writes.

- **4 µs p50** GET vs 7 µs for Redis
- **88× lower** worst-case latency
- **126K ops/s** on 8 threads with lock-free seqlock reads and 0 mismatches
- **0.10 µs p50** with the client cache (Zipf-1.2)

</td>
<td width="50%" valign="top">

#### [Sentinel-X](https://github.com/Vaibhav805/sentinel-x)
`C` `eBPF/XDP` `Python` `XGBoost`

DDoS mitigation that **drops packets before any `sk_buff` is allocated**, with an ML control plane that rewrites the rules live.

- **45.3M packets** processed
- **96.51%** drop accuracy, **0.31%** false positives
- **0.066 ms** p99 verdict latency under flood
- **~5.2 MB** total kernel map footprint

</td>
</tr>
<tr>
<td colspan="2" valign="top">

#### Onitro
`C++` `AVX2` `OpenMP` `CMake`

A vectorised Monte Carlo derivatives pricing engine (group project). I own the fixed-income module and the European/Asian option engine: antithetic and control variates, per-option PCG32 RNG streams, and SIMD isolated behind a CMake-controlled macro.

</td>
</tr>
</table>

---

### 🛠️ Toolbox

**Hardware & ISA**
![RISC-V](https://img.shields.io/badge/RISC--V-283272?style=flat-square&logo=riscv&logoColor=white)
![SystemVerilog](https://img.shields.io/badge/SystemVerilog-C85A32?style=flat-square)
![Verilator](https://img.shields.io/badge/Verilator-6E8A6B?style=flat-square)
![Spike](https://img.shields.io/badge/Spike-4F6C88?style=flat-square)
![FPGA](https://img.shields.io/badge/FPGA-C79A3E?style=flat-square)

**Languages**
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Rust](https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Assembly](https://img.shields.io/badge/RISC--V_asm-555555?style=flat-square)

**Systems**
![eBPF](https://img.shields.io/badge/eBPF%2FXDP-FF6600?style=flat-square&logo=ebpf&logoColor=white)
![RDMA](https://img.shields.io/badge/RDMA-1C1B1A?style=flat-square)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![CMake](https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake&logoColor=white)
![QEMU](https://img.shields.io/badge/QEMU-FF6600?style=flat-square&logo=qemu&logoColor=white)

---

<div align="center">

**[→ Full portfolio with interactive charts](https://vaibhav805.github.io)**

</div>
