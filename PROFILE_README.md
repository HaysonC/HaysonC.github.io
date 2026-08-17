# Hayson Cheung

Founding machine learning engineer in San Francisco, where I work on diffusion, flow, and language models for spatial intelligence — generating and reasoning about the physical world in 3D. Engineering Science (Robotics) at the **[University of Toronto](https://www.engineering.utoronto.ca/)**, 2024–2028, and an undergraduate researcher there.

I'm interested in **physical and spatial intelligence** and **robotics**, particularly the **energy-based and probabilistic models** that make long-horizon planning possible — and in the **efficient model and systems design** that makes any of it cheap enough to actually run.

[hayson.me](https://hayson.me) · [Scholar](https://scholar.google.com/citations?user=S-SivN8AAAAJ) · [LinkedIn](https://www.linkedin.com/in/hayson-cheung-3688a5241/) · [Email](mailto:hayson.cheung@mail.utoronto.ca) · [Notes](https://github.com/HaysonC/skulenotes)

## Selected research

**[Per-Token Compute Budgeting in a 26B MoE Router](https://github.com/HaysonC/gemma4-optimization)** · technical report, 2026
A light per-layer budget head decides *how many* of the top-8 routed experts a token needs rather than *which*. Distilled against a frozen Gemma 4 26B-A4B, it cuts 8 active experts to 2.5 on WikiText (5.8 in chat) at router KL ≈ 0.05 — a near-lossless **69% reduction** in active routed-expert compute. → [code](https://github.com/HaysonC/gemma4-optimization)

**[REACT: A Conditioning Framework for User-Adaptive sEMG Hand Pose Estimation](https://arxiv.org/abs/2605.30127)** · ICRA Workshop, 2026
Surface EMG decoders degrade across users because electrode placement and anatomy shift the input distribution. Conditioning a pose backbone on a learned per-user embedding absorbs that shift, beating the state of the art on **all three EMG2POSE splits** from **under 45 seconds** of calibration and with no retraining at deployment. → [arXiv](https://arxiv.org/abs/2605.30127)

**[PIVONet: A Physically-Informed Variational Neural ODE Model for Efficient Advection-Diffusion Fluid Simulation](https://arxiv.org/abs/2601.03397)** · arXiv, 2026
A neural surrogate for flows where advection and diffusion both matter. Splitting the dynamics into a deterministic neural ODE and a variational stochastic controller keeps the mean field physically consistent while still modelling the noise — worth an **80–96% accuracy gain** over the purely deterministic baseline across flow regimes. → [arXiv](https://arxiv.org/abs/2601.03397) · [code](https://github.com/HaysonC/PIVONet)

**[SAMUeL: Efficient Vocal-Conditioned Music Generation via Soft Alignment Attention and Latent Diffusion](https://arxiv.org/abs/2507.19991)** · IEEE/WIC WI-IAT, 2025
Accompaniment has to track a vocal line locally while staying coherent globally. A soft alignment attention that reweights local against global temporal dependence as a function of the diffusion timestep gets both out of a 15M-parameter latent diffusion model: **220× fewer parameters and 52× faster inference** at competitive quality. → [arXiv](https://arxiv.org/abs/2507.19991) · [code](https://github.com/HaysonC/SAMUeL-GEN)

## Projects

**Amortized Manifold Planning by Energy Descent in Chess and Go** · *in progress*
Tree search buys depth at exponential cost. The alternative here is to learn the value landscape as an energy over a continuous manifold of positions, so a plan comes from gradient descent on that energy instead of from expanding a frontier — branching becomes a fixed number of refinement steps, and those steps batch on a GPU where a search serializes. Beats Stockfish at **3000 Elo** without exponential-scale search.

**World Models as a Proxy for Robotics** · *ongoing*
An end-to-end Dreamer-style world model for an SO-101 arm: teleoperated data collection, latent dynamics learning, and policy training done entirely in imagined rollouts, for closed-loop visuomotor control.

**3D Generation with Extra Modalities**
A training-free way to steer 3D generation models with text and geometric constraints at inference time, plus a distributed inference and networking stack running at **>2× lower latency** than the official implementation.

Earlier things I still like: [NEAT-PongBot](https://github.com/HaysonC/NEAT-PongBot) (neuroevolution playing Pong and Smash Bros), [LegoFIKS](https://devpost.com/software/legofiks) (photo → 3D model → step-by-step LEGO build instructions, and the first thing that got me into 3D generation), an [LSTM encoder–decoder translator](https://github.com/HaysonC/Encoder-DecoderLSTMTranslator), and [real-time pendulum tracking](https://github.com/HaysonC/PHY180-Pendulum) from first-year physics.
