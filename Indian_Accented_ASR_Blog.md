
# Making Sense of Indian-Accented English: A Journey to Better Speech Recognition

## Introduction
Speech technologies like voice assistants, transcription tools, and captioning services rely on Automatic Speech Recognition (ASR) to turn spoken words into written text. ASR has improved dramatically in recent years, but many systems still struggle when people speak with different accents. Think about the vast linguistic diversity found in India: English is commonly spoken, but influenced by dozens of regional languages, leading to unique pronunciations, rhythms, and words not found in standard Englis...

This blog presents a project carried out as part of a graduate-level study at the University of Florida, under Dr. Grant’s mentorship. The goal was to enhance ASR performance for Indian-accented English—making the technology more inclusive and accurate. The journey started with traditional alignment methods and evolved to cutting-edge techniques, integrating special models that handle unfamiliar words and subtle accent differences. By the end, the hope is to show that advanced methods can bring ASR closer...
    


---

## What is ASR, and Why Are Accents Challenging?
Automatic Speech Recognition (ASR) is the technology that converts audio of spoken language into written text. Common examples include the voice assistant on your phone or automatic subtitles on videos. While ASR works well for “standard” English (like American or British accents), it can get confused by accents that differ in pronunciation patterns or vocabulary.

### Why Indian-Accented English?
Indian English often incorporates phonetic elements from native languages. Some sounds may be pronounced with a curled tongue (retroflex), certain vowel sounds might be shortened or lengthened differently, and local brand names or loanwords appear frequently. These variations can trip up ASR systems trained on more “standard” English.

**(Insert Image: A simple infographic showing a world map with a highlight on India and speech bubbles indicating different accents or phoneme symbols. This could visually represent linguistic diversity.)**
    


---

## The Svarah Dataset: A Starting Point
The project used a dataset called Svarah, containing about 9.6 hours of Indian-accented English speech from 117 speakers across 19 states. Each audio clip has a transcript and metadata like the speaker’s native language.

**Example: A Data Entry**

```
{
  "audio_filepath": "audio_files/speaker_03_clip_05.wav",
  "duration": 4.5,
  "text": "I would like to pay using Paytm",
  "gender": "male",
  "primary_language": "Hindi"
}
```

**(Insert Image: A screenshot of a waveform from an audio file in the dataset, with annotations showing speaker info or a snippet of metadata.)**

This dataset exposed how certain words—like “Paytm”—don’t exist in standard dictionaries, and how pronunciation patterns differ from what most ASR models expect.
    

