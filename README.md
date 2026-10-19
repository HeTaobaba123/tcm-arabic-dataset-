# TCM Arabic Dataset — Traditional Chinese Medicine in Arabic & Chinese

> The first open **Arabic–Chinese Traditional Chinese Medicine (TCM) dataset**: 1,029 herbs, 409 classical formulas, 499 acupoints, 129 classical texts, and 50 PubMed-cited clinical evidence entries — each with **Arabic names, Arabic descriptions, and unique Arabic-medicine cultural relations**.

[![License: CC0 1.0](https://img.shields.io/badge/License-CC0%201.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
[![Data: JSON](https://img.shields.io/badge/format-JSON-blue.svg)]()
[![Languages](https://img.shields.io/badge/lang-Arabic%20%7C%20Chinese%20%7C%20Pinyin-green.svg)]()

Built and maintained by **[TCMHub](https://aicatalogx.com)** — the first comprehensive Arabic platform for Traditional Chinese Medicine (الطب الصيني التقليدي).

---

## 📦 What's inside

| File | Records | Description |
|---|---|---|
| `tcm-herbs.ar-zh.json` | 1,029 | Chinese herbs — Arabic/Chinese names, pinyin, Latin name, nature/flavor (性味), meridians (归经), functions, dosage, contraindications, and **`arabRelation`** (Arabic common name + cultural notes) |
| `tcm-formulas.ar-zh.json` | 409 | Classical formulas (方剂) — source text, century, category, functions, indications, constituent herbs |
| `tcm-acupoints.ar-zh.json` | 499 | Acupuncture points (穴位) — code, meridian, Arabic location, indications, needling method |
| `tcm-classics.ar-zh.json` | 129 | Classical TCM texts (经典) — Arabic/Chinese title, dynasty, author, excerpts |
| `tcm-evidence-pubmed.ar.json` | 50 | Clinical evidence — condition, intervention, finding, PubMed citation (PMID + URL), evidence level |

**Total: 2,116 structured records**, all Arabic-Chinese bilingual.

---

## 🌟 Unique feature: `arabRelation`

Unlike any existing TCM dataset, each herb carries an `arabRelation` object documenting the herb's place in **Arabic/Gulf medicine and culture** — the Arabic common name, culinary and traditional-medicine usage across the Arab world, and historical notes on the China–Arab medicine exchange along the Silk Road.

This makes the dataset uniquely valuable for:
- Arabic NLP / health-tech / chatbot projects
- Cross-cultural medical history research
- Arabic-language health content platforms
- Machine translation (zh↔ar medical domain)

---

## 📖 Schema

### `tcm-herbs.ar-zh.json`
```json
{
  "id": "H001",
  "nameAr": "الزنجبيل",
  "nameZh": "生姜",
  "pinyin": "Sheng Jiang",
  "latinName": "Zingiberis Rhizoma Recens",
  "xing": "温",
  "wei": "辛",
  "guijing": ["肺", "脾", "胃"],
  "gongxiao": "تبديد البرودة الخارجية، تدفئة المعدة...",
  "jinji": "يمنع للحوامل بكميات كبيرة...",
  "yongfa": "يغلى 3-10 غرام...",
  "arabRelation": {
    "commonArabicName": "زنجبيل",
    "culturalNotes": "الزنجبيل من أهم التوابل في المطبخ العربي..."
  }
}
```

### `tcm-formulas.ar-zh.json`
```json
{
  "id": "F001",
  "nameAr": "...", "nameZh": "麻黄汤", "pinyin": "Mahuang Tang",
  "sourceText": "伤寒论", "century": "3rd", "category": "解表剂",
  "functions": "...", "indications": "...", "herbs": ["H..."]
}
```

### `tcm-acupoints.ar-zh.json`
```json
{
  "id": "A001", "nameAr": "...", "nameZh": "...", "pinyin": "...",
  "code": "LI4", "meridian": "手阳明大肠经",
  "locationAr": "...", "indications": "...", "method": "...", "contraindications": "..."
}
```

### `tcm-evidence-pubmed.ar.json`
```json
{
  "conditionAr": "...", "interventionAr": "...", "findingAr": "...",
  "citation": "...", "year": 2020, "pmid": "...", "pubmedUrl": "...", "levelAr": "..."
}
```

---

## 🚀 Usage

```python
import json

herbs = json.load(open('tcm-herbs.ar-zh.json', encoding='utf-8'))
for h in herbs:
    print(h['nameZh'], '→', h['nameAr'], '|', h['latinName'])
```

The data is clean, UTF-8 encoded, and ready for:
- **Health chatbots & LLM fine-tuning** (Arabic medical domain)
- **Search / knowledge-graph** applications
- **Academic research** on China–Arab medical exchange
- **Translation memory** for zh↔ar medical content

---

## 🌐 Live application

This dataset powers **[TCMHub.com](https://aicatalogx.com)** — browse all herbs, formulas, acupoints and classical texts in full Arabic, with an AI TCM health advisor.

- Website: https://aicatalogx.com
- Arabic: https://aicatalogx.com/ar

---

## 📄 License

**CC0 1.0 Universal (Public Domain Dedication)** — free for any use, commercial or not, no attribution required (though a link back to [TCMHub](https://aicatalogx.com) is appreciated).

## ⚠️ Disclaimer

This dataset is for **educational and research purposes only**. It is not medical advice, diagnosis, or treatment. Always consult a qualified physician before using any herbal or TCM information.

## 🤝 Contributing

Spotted an error or want to contribute more Arabic TCM data? Open an issue or PR. Translations, corrections, and additional records are welcome.

---

*Keywords: Traditional Chinese Medicine, TCM, Arabic, الطب الصيني, الأعشاب الصينية, Chinese herbs, acupuncture, acupoints, herbal formulas, medical dataset, Arabic NLP, health data, China-Arab, bilingual medical corpus*
