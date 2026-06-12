# Satellite Image Classification — Siamese Triplet Network

Дипломна робота з класифікації супутникових знімків із використанням метричного навчання.

## Опис

Система знаходить інфраструктурні об'єкти на супутникових знімках:
кільцеві розв'язки, перехрестя, промзони, ліси, озера, мости, залізниці, стадіони, злітні смуги, житлову забудову.

Порівнюються три моделі:
- **Siamese Triplet Network** (наша) — ResNet-50 + Embedding Head + Triplet Loss
- ResNet-50 Baseline — pretrained ваги без fine-tuning
- MobileNetV3 Baseline — легка мобільна архітектура

## Результати

| Модель | mAP | Top-1 | Час мс/img |
|--------|-----|-------|------------|
| Siamese Triplet (наша) | **97.04%** | **97.40%** | 4.54 |
| ResNet-50 Baseline | 59.06% | 84.60% | 4.90 |
| MobileNetV3 Baseline | 58.45% | 88.00% | 5.57 |

## Запуск

1. Відкрийте `satellite_siamese_diploma_clean.ipynb` у Google Colab
2. Увімкніть GPU: `Середовище виконання → Змінити тип → T4 GPU`
3. Запустіть клітинки по порядку зверху вниз

## Датасет

[NWPU-RESISC45](https://huggingface.co/datasets/timm/resisc45) — 45 класів супутникових знімків, 700 зображень на клас.

## Вимоги
