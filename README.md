# Poker44-gen11lgbm2

Minimal release repository for model gen11lgbm2.

This repo is a standalone miner variant, extracted analogously to gen10heur releases,
but wired to the LightGBM profile/model artifacts used by gen8lgbm and with
a final 50/50 bot-human rebalance step.

## Quick start

```bash
git clone https://github.com/tomkaba/Poker44-gen11lgbm2.git
cd Poker44-gen11lgbm2
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
pip install -e .
```

## Run Miner

```bash
python neurons/miner.py
```

or legacy wrapper:

```bash
./start_miner.sh HOTKEY_ID[,HOTKEY_ID2,...]
```

## Implementation

- Scorer: score_chunks_gen11lgbm2_rebalanced() in poker44/miner_heuristics.py
- Artifacts:
  - models/benchmark_lgbm_profile.json
  - models/benchmark_lgbm_model.pkl
- Entry point: neurons/miner.py

Manifest implementation SHA256 is computed from:

- neurons/miner.py
- poker44/miner_heuristics.py
- models/benchmark_lgbm_profile.json
- models/benchmark_lgbm_model.pkl
