# Llama-3.3-70B Training Monitor Log

## Run Details
- **Model**: Llama-3.3-70B-Instruct (QLoRA 4-bit NF4, r=512)
- **Cluster**: train-flex-2026_03_20_01_12_28-h4zx (Nebius H100:8)
- **Job ID**: 10
- **WandB**: https://wandb.ai/slingshot-ai/Ash%20Models/runs/8r69qjra

---

## 2026-03-24 — Step 2040 / 8089 (25.2%)

**Status: HEALTHY — All systems nominal**

### Training Metrics (last 5 logged steps)

| Step | Loss | Grad Norm | LR | Token Acc | Epoch |
|------|------|-----------|----|-----------|-------|
| 2020 | 1.1233 | 0.393 | 8.91e-5 | 66.2% | 0.25 |
| 2025 | 1.1063 | 0.418 | 8.90e-5 | 66.4% | 0.25 |
| 2030 | 1.1169 | 0.434 | 8.90e-5 | 66.2% | 0.25 |
| 2035 | 1.1057 | 0.401 | 8.89e-5 | 66.6% | 0.25 |
| 2040 | 1.1128 | 0.383 | 8.89e-5 | 66.1% | 0.25 |

### GPU Utilization

All 8x H100 GPUs at 100% compute utilization, 94-96% VRAM, temps 56-70°C.

### Notes
- Loss trending down from ~1.13 (step 1685) to ~1.11 (step 2040)
- Still tracking ~0.11-0.13 ahead of a4 baseline at same % through training
- Step time stable at ~158-159s/step
- ETA: ~267 hours remaining (~April 4, 2026)
- Checkpoint-2000 should have been saved
- Autostop configured at 10 minutes — monitor cluster availability
