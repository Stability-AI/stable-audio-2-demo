⚠️ *Warning: This website may not function properly on Safari. For the best experience, please use Google Chrome.*

Our model can generate **variable-length and long-form stereo music at 44.1kHz**:

| Generated Stereo Music | Prompt |
| --------------- | ------ |
| <audio controls preload=False><source src="audio/berlin-techno-rave-drum-machine-kick-ARP-synthesizer-dark-moody-hypnotic-evolving-135-bpm.wav" type="audio/mpeg">Audio not supported by your browser.</audio> | Berlin techno, rave, drum machine, kick, ARP synthesizer, dark, moody, hypnotic, evolving, 135 BPM. Loop. |
| <audio controls preload=False><source src="audio/uplifting-acoustic-loop-120-bpm.wav" type="audio/mpeg">Audio not supported by your browser.</audio> | Uplifting acoustic loop. 120 BPM. |
| <audio controls preload=False><source src="audio/Disco, Driving Drum Machine, Synthesizer, Bass, Piano, Guitars, Instrumental, Clubby, Euphoric, Chicago, New York, 115 BPM.wav" type="audio/mpeg">Audio not supported by your browser.</audio> | Disco, Driving Drum Machine, Synthesizer, Bass, Piano, Guitars, Instrumental, Clubby, Euphoric, Chicago, New York, 115 BPM. |
| <audio controls preload=False><source src="audio/Calm meditation music to play in a spa lobby.wav" type="audio/mpeg">Audio not supported by your browser.</audio> | Calm meditation music to play in a spa lobby. |
| <audio controls preload=False><source src="audio/drum solo.wav" type="audio/mpeg">Audio not supported by your browser.</audio> | Drum solo. |

Differently from pervious state-of-the-art models, ours can generate **stereo sound effects at 44.1kHz**:

| Generated Stereo Sounds | Prompt |
| --------------- | ------ |
| <audio controls preload=False><source src="audio/door-slam-high-quality-stereo.wav" type="audio/mpeg">Audio not supported by your browser.</audio> | Door slam. High-quality, stereo. |
| <audio controls preload=False><source src="audio/sports-car-passing-by-high-quality-stereo.wav" type="audio/mpeg">Audio not supported by your browser.</audio> | Sports car passing by. High-quality, stereo. |
| <audio controls preload=False><source src="audio/motorbike-passing-by-high-quality-stereo.wav" type="audio/mpeg">Audio not supported by your browser.</audio> | Motorbike passing by. High-quality, stereo. |
| <audio controls preload=False><source src="audio/fireworks-high-quality-stereo.wav" type="audio/mpeg">Audio not supported by your browser.</audio> | Fireworks. High-quality, stereo. |
| <audio controls preload=False><source src="audio/reverberant-foot-steps-inside-a-large-rocky-cave-high-quality-stereo.wav" type="audio/mpeg">Audio not supported by your browser.</audio> | Reverberant footsteps inside a large rocky cave. High-quality, stereo. |

Note that all the examples in this website are generated with the same model that can generate both **variable-length music and sound effects** at 44.1kHz stereo. We append "high-quality, stereo" to our sound effects prompts because it is generally helpful.

## Long-form stereo music: comparison with state-of-the-art with MusicCaps prompts

**Prompt**: This song contains someone strumming a melody on a mandolin while more people are whistling along. Then a mandolin, an e-bass and an acoustic guitar are playing a short melody in a lower key before breaking into the next part along with flutes and percussions. This song may be played outside by musicians performing. 

| Our Model | MusicGen-large | MusicGen-stereo | AudioLDM2 | 
| *(stereo, 44.1kHz)* | *(mono, 32kHz)* | *(stereo, 32kHz)* | *(mono, 48kHz)* |
| ------ | -------------- | --------------- | --------- |
| <audio controls preload=False><source src="audio/ZTVMsW1h3bI_stableaudio.wav" type="audio/mpeg">Audio not supported by your browser.</audio> | <audio controls preload=False><source src="audio/ZTVMsW1h3bI_musicgenlarge.wav" type="audio/mpeg">Audio not supported by your browser.</audio> | <audio controls preload=False><source src="audio/ZTVMsW1h3bI_musicgenstereo.wav" type="audio/mpeg">Audio not supported by your browser.</audio> | <audio controls preload=False><source src="audio/ZTVMsW1h3bI_audioldm248k_stereo.wav" type="audio/mpeg">Audio not supported by your browser.</audio> |

**Prompt**: The commercial music features a groovy piano melody played over snare rolls in the first half of the loop. Right after, there is a drop that consists of a punchy "4 on the floor" kick pattern, shimmering hi hats, claps, groovy piano and wide synth lead melody. It sounds happy, fun, euphoric and exciting.

| Our Model | MusicGen-large | MusicGen-stereo | AudioLDM2 | 
| *(stereo, 44.1kHz)* | *(mono, 32kHz)* | *(stereo, 32kHz)* | *(mono, 48kHz)* |
| ------ | -------------- | --------------- | --------- |
| <audio controls preload=False><source src="audio/ZK5M3DZejzk_stableaudio.wav" type="audio/mpeg">Audio not supported by your browser.</audio> | <audio controls preload=False><source src="audio/ZK5M3DZejzk_musicgenlarge.wav" type="audio/mpeg">Audio not supported by your browser.</audio> | <audio controls preload=False><source src="audio/ZK5M3DZejzk_musicgenstereo.wav" type="audio/mpeg">Audio not supported by your browser.</audio> | <audio controls preload=False><source src="audio/ZK5M3DZejzk_audioldm248k_stereo.wav" type="audio/mpeg">Audio not supported by your browser.</audio> |

These prompts/audios were used for the qualitative study we report in our paper.

## Sound effects: comparison with state-of-the-art with AudioCaps prompts

**Prompt**: Clicking and sputtering then eventual revving of an idling engine.

| Model | Audiogen-medium | AudioLDM2 |
| *(stereo, 44.1kHz)* | *(mono, 32kHz)* | *(mono, 48kHz)* |
| ------ | -------------- | --------------- | 
| <audio controls preload=False><source src="audio/103136_stableaudio_audio.wav" type="audio/mpeg">Audio not supported by your browser.</audio> | <audio controls preload=False><source src="audio/103136_audiogen_stereo.wav" type="audio/mpeg">Audio not supported by your browser.</audio> | <audio controls preload=False><source src="audio/103136_audioldm248k_stereo.wav" type="audio/mpeg">Audio not supported by your browser.</audio> |

**Prompt**: Birds chirping loudly.

| Model | Audiogen-medium | AudioLDM2 |
| *(stereo, 44.1kHz)* | *(mono, 32kHz)* | *(mono, 48kHz)* |
| ------ | -------------- | --------------- | 
| <audio controls preload=False><source src="audio/37008_stableaudio_audio.wav" type="audio/mpeg">Audio not supported by your browser.</audio> | <audio controls preload=False><source src="audio/37008_audiogen_stereo.wav" type="audio/mpeg">Audio not supported by your browser.</audio> | <audio controls preload=False><source src="audio/37008_audioldm248k_stereo.wav" type="audio/mpeg">Audio not supported by your browser.</audio> |

These prompts/audios were used for the qualitative study we report in our paper. Note the (randomly) selected prompts from AudioCaps did not require substantial stereo movement, resulting in renders that are relatively non-spatial.

## Autoencoder: reconstructions

This comparison is useful to evaluate the audio fidelity capabilities of the autoencoder. On the left, we have the ground truth recording. On the right, we take the ground truth recording and end pass it through the autoencoder. Note that the autoencoder reconstruction is fairly transparent, very close to the ground truth.

| Ground truth | Autoencoder reconstruction |
|-|-|
| <audio controls preload=False><source src="audio/1197.flac" type="audio/mpeg">Your browser does not support the audio element.</audio> | <audio controls preload=False><source src="audio/1197_ae.wav" type="audio/mpeg">Your browser does not support the audio element.</audio> |
| <audio controls preload=False><source src="audio/1243.flac" type="audio/mpeg">Your browser does not support the audio element.</audio> | <audio controls preload=False><source src="audio/1243_ae.wav" type="audio/mpeg">Your browser does not support the audio element.</audio> |
| <audio controls preload=False><source src="audio/233076.flac" type="audio/mpeg">Your browser does not support the audio element.</audio> | <audio controls preload=False><source src="audio/233076_ae.wav" type="audio/mpeg">Your browser does not support the audio element.</audio> |
| <audio controls preload=False><source src="audio/451.flac" type="audio/mpeg">Your browser does not support the audio element.</audio> | <audio controls preload=False><source src="audio/451_ae.wav" type="audio/mpeg">Your browser does not support the audio element.</audio> |
| <audio controls preload=False><source src="audio/206251.flac" type="audio/mpeg">Your browser does not support the audio element.</audio> | <audio controls preload=False><source src="audio/206251_ae.wav" type="audio/mpeg">Your browser does not support the audio element.</audio> |
