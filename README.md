## Benjamin Tung

MS Electrical & Computer Engineering @ UCLA — Integrated Circuit Design
BSEE, Arizona State, 2026 · Exchange year in EE at National Taiwan University

Previously: **NXP Semiconductors** (3D chiplet packaging) · **Samsung Austin Semiconductor** (2 summers)

[LinkedIn](https://www.linkedin.com/in/benjamin-tung-b5165420a/) — happy to send supporting material for anything here.

---

### FPGA / Digital Design

| Project | Description |
|---|---|
| **[flappy-bird](https://github.com/bentung12/flappy-bird)** | Flappy Bird in SystemVerilog, rendered to VGA. Each pixel's color computed on demand at 25 MHz. |
| **[risc_v-microprocessor](https://github.com/bentung12/risc_v-microprocessor)** | 5-stage pipelined RISC-V core in Chisel. Forwarding, hazard detection, branches resolved in ID to halve the mispredict penalty. |
| **[simple-microprocessor](https://github.com/bentung12/simple-microprocessor)** | 12-bit CPU with an ISA I designed, plus a debug mux and slow clock for single-stepping on the board. |
| **[alarm-clock](https://github.com/bentung12/alarm-clock)** | 24-hour clock built from one parameterized counter module at six different moduli. |

![Flappy Bird Demo](https://github.com/bentung12/flappy-bird/blob/main/flappy_bird.gif)

---

### Research — Analog In-Memory Computing Under Radiation

Senior capstone. Marinella group, ASU, in collaboration with Sandia National Labs.

**Problem:** Analog in-memory computing can do matrix multiplication using a memory array, making neural network inference far more energy-efficient than traditional methods. However, these cells store weights as trapped charge, and radiation can knock that charge loose. This results in weights drifting and accuracy collapses, particularly in high radiation applications such as satellites.

**Solution**

- Modeled SONOS charge-trap arrays under total ionizing dose in [CrossSim](https://github.com/bentung12/cross-sim/tree/pytorch), Sandia's analog accelerator simulator
- Built a runtime calibration factor that cancels drift by measuring the array's response to a known input
- Built a training method that folds that correction into the training loop instead of applying it afterward
- Brought up the SONOS evaluation board and ran trained weights on real hardware

**Result:** held ResNet-32 accuracy to **~13× the radiation dose** the uncorrected model tolerated, with no accuracy loss on an unirradiated chip.

My code: [tiny_imagenet](https://github.com/bentung12/cross-sim/tree/pytorch/applications/dnn/torch/tiny_imagenet) · [tiny_imagenet_radiation](https://github.com/bentung12/cross-sim/tree/pytorch/applications/dnn/torch/tiny_imagenet_radiation)

---

### Other

**[inkjet-printing](https://github.com/bentung12/inkjet-printing)** — MATLAB model solving for the deflection voltage that places each ink droplet, then reconstructing the printed image from the voltage waveform.