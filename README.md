<p align="center">
  <img src="https://raw.githubusercontent.com/hidra0x/hidra0x/main/assets/banner.svg" width="100%" alt="hidra0x — iOS kernel research">
</p>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=21&pause=900&color=FF9F43&center=true&vCenter=true&width=950&lines=iOS+kernel+research+on+A12+%2F+18.7.2;Building+HIDRA+%E2%80%94+data-only+jailbreak+research;MOON+Probe+%E2%80%94+open-source+AppleJPEGDriver+PoC;Aurora+TV+%E2%80%94+lightweight+Android+TV+launcher" alt="Typing SVG">
</p>

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=hidra0x&label=PROFILE+VIEWS&color=FF4D4D&style=for-the-badge" alt="profile views">
  <img src="https://img.shields.io/github/followers/hidra0x?label=FOLLOWERS&style=for-the-badge&color=FF9F43&labelColor=0D1117" alt="followers">
  <img src="https://img.shields.io/badge/STATUS-RESEARCH-FF9F43?style=for-the-badge&labelColor=0D1117" alt="status">
  <img src="https://img.shields.io/badge/TARGET-iOS%2018.7.2%20%2F%20A12-58A6FF?style=for-the-badge&labelColor=0D1117" alt="target">
</p>

## `$ whoami`

<p align="center">
  <img src="https://raw.githubusercontent.com/hidra0x/hidra0x/main/assets/terminal.svg" width="92%" alt="hidra0x terminal">
</p>

```yaml
name: hidra0x
role: iOS kernel research
target: iPhone XR · A12 / T8020 · iOS 18.7.2
focus: AppleJPEGDriver CVE-2026-20687 → controlled free → double-free/write
strategy: data-only kernel control · no text patching · no fake PAC pointers
status: S0–S3 done · S4 in progress · no public build
```

I break things on a spare iPhone, read XNU at night, and write down every
panic. The goal is not another crash — it is **kernel control** through data,
not through a forged function pointer.

## `$ ls ~/projects`

<table>
  <tr>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/hidra0x/hidra">HIDRA</a></h3>
      <p>A12 / iOS 18.7.2 jailbreak research. Kernel entry via AppleJPEGDriver, then a data-only path to kernel r/w.</p>
      <p><code>S0–S3 done</code> · <code>S4 in progress</code></p>
    </td>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/hidra0x/hidgate-poc/tree/main/PoC/applejpeg">MOON Probe</a></h3>
      <p>Open-source AppleJPEGDriver PoC: userclient, 0x58 ABI, deferred UAF, runnable IPA.</p>
      <p><code>v0.1</code> · <code>unsigned IPA</code></p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/hidra0x/hidgate-poc">hidgate-poc</a></h3>
      <p>Kernel UAF research on 18.7.2/A12: IOHID crash-only, AppleJPEG controlled free, panic analysis, test matrix.</p>
      <p><code>research</code> · <code>18.7.2</code></p>
    </td>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/hidra0x/aurora-tv">Aurora TV</a></h3>
      <p>Lightweight Android TV launcher for Telefunken / Android 5–14. No ads, no trackers, no Google Play Services.</p>
      <p><code>v1.4.0</code> · <code>Kotlin</code></p>
    </td>
  </tr>
</table>

## `$ cat /now`

- **RE:** `AppleJPEGDriver 7.6.9`, `IOUserClient2022`, queue / power paths.
- **Hunting:** a double-free or write primitive from the stale `JpegRequest` queue node (S4).
- **Strategy:** data-only — `proc`, `ucred`, `csflags`, AMFI/MACF; no kernel text patching, no page tables unless required.
- **Next:** KASLR leak after a write primitive; then PAC/PPL/KTRR-safe bootstrap.

## `$ ./stack`

<p align="center">
  <img src="https://skillicons.dev/icons?i=apple,c,kotlin,android,py,bash,git,github,linux&theme=dark" alt="stack">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/arm64e-PAC-FF4D4D?style=flat-square&labelColor=0D1117" alt="arm64e">
  <img src="https://img.shields.io/badge/XNU-kernel-FF9F43?style=flat-square&labelColor=0D1117" alt="XNU">
  <img src="https://img.shields.io/badge/IOKit-userclients-58A6FF?style=flat-square&labelColor=0D1117" alt="IOKit">
  <img src="https://img.shields.io/badge/IOSurface-KVA-27C93F?style=flat-square&labelColor=0D1117" alt="IOSurface">
</p>

## `$ ./metrics`

<p align="center">
  <img src="https://raw.githubusercontent.com/hidra0x/hidra0x/main/assets/metrics.svg" width="92%" alt="hidra0x metrics">
</p>

<p align="center">
  <img src="https://img.shields.io/github/stars/hidra0x/hidra?style=for-the-badge&label=STARS&color=FF9F43&labelColor=0D1117" alt="stars">
  <img src="https://img.shields.io/github/forks/hidra0x/hidra?style=for-the-badge&label=FORKS&color=58A6FF&labelColor=0D1117" alt="forks">
  <img src="https://img.shields.io/github/last-commit/hidra0x/hidra?style=for-the-badge&label=LAST%20COMMIT&color=27C93F&labelColor=0D1117" alt="last commit">
</p>

## `$ ./snake`

<p align="center">
  <img src="https://raw.githubusercontent.com/hidra0x/hidra0x/output/github-contribution-grid-snake-dark.svg" alt="Contribution snake">
</p>

## `$ contact`

<p align="center">
  <a href="https://github.com/hidra0x"><img src="https://img.shields.io/badge/GitHub-hidra0x-0D1117?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"></a>
  <a href="https://github.com/hidra0x/hidra"><img src="https://img.shields.io/badge/HIDRA-research-FF4D4D?style=for-the-badge&labelColor=0D1117" alt="HIDRA"></a>
  <a href="https://github.com/hidra0x/hidgate-poc/releases/tag/moon-poc-v0.1"><img src="https://img.shields.io/badge/MOON-Probe-FF9F43?style=for-the-badge&labelColor=0D1117" alt="MOON"></a>
</p>

<p align="center">
  <i>«Паника — это не конец. Это доказательство, что мы уже в ядре.»</i>
</p>

<p align="center">
  <b>CRASH → CONTROL → JAILBREAK</b>
</p>
