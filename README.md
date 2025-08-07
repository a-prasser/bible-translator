# Towards a Decoder-Only Bible Translator and Text Generation

This project explores multilingual machine translation and alignment using the [eBible corpus](https://github.com/biblenlp/ebible), a collection of over 1,000 Bibles in different languages. It was developed as part of a Kaggle-based research project focused on leveraging religious texts for cross-lingual NLP applications.

## 📁 Dataset

The dataset is **not included in this repository** due to size constraints. It can be accessed and downloaded from the original GitHub source: [biblenlp/ebible](https://github.com/biblenlp/ebible). The corpus contains full Bible texts in over 1,000 languages.

## 🔍 Objective

- Explore the viability of multilingual Bible translation using modern AI techniques.
- Train a neural machine translation (NMT) model on the eBible corpus, which contains over 1000 Bibles in different languages.
- Investigate the impact of including religious text structure (books, chapters, verses) in translation models.
- Evaluate model performance on both high-resource and low-resource language pairs.
- Demonstrate that faith-based multilingual corpora can support cross-linguistic AI research, especially for underrepresented languages.
- Lay the groundwork for future research in faith-domain translation and culturally sensitive NLP applications.

## 🧠 Methodology

- **Dataset Source and Preparation**
  - Used the [eBible corpus](https://github.com/biblenlp/ebible), which provides Bible texts in over 100 languages with consistent book–chapter–verse alignment.
  - Extracted parallel sentence pairs by aligning verses across language pairs.
  - Filtered noisy or extremely short verses to improve training data quality.
- **Preprocessing**
  - Normalized Unicode text and removed punctuation inconsistencies.
  - Applied sentencepiece tokenization for efficient vocabulary sharing across languages.
- **Model Architecture**
  - Employed transformer-based sequence-to-sequence models using OpenNMT-py.
  - Trained both bilingual and multilingual models to compare translation quality across setups.
- **Training Strategy**
  - Used standard training settings: Adam optimizer, learning rate scheduling, label smoothing.
  - Trained multilingual models with language tags to specify target language.
  - Evaluated translation quality using BLEU scores on held-out validation data.
- **Experimnet Design**
  - Compared results between high-resource and low-resource language pairs.
  - Assessed benefits of multilingual training vs. bilingual baselines.
  - Focused on the role of shared verse alignment and Bible-specific linguistic structure.

## 📊 Results

- **BLEU Score Performance**
  - Achieved strong baseline BLEU scores across high-resource pairs (e.g., English–Spanish), validating the quality of the eBible dataset.
- **Impact of Multilingual Training**
  - Multilingual models outperformed bilingual models on low-resource pairs by leveraging cross-lingual transfer.
  - Demonstrated that combining related language families in training improved generalization and robustness.
- **Effect of Verse Alignment**
  - Structural alignment by book/chapter/verse proved critical to translation quality.
  - Verse-level granularity provided natural sentence-length units that improved training stability.
- **Translation Examples**
  - Qualitative examples revealed accurate conveyance of meaning, even across distant languages.
  - Minor errors in rare cases, typically involving idioms or less frequent vocabulary.
- **Scalability & Efficiency**
  - Demonstrated that meaningful Bible translation is possible even with modest computational resources.
  - Training times were manageable, and inference was fast on standard hardware.

