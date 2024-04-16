⚠️ *Warning: This website may not function properly on Safari. For the best experience, please use Google Chrome.*

Audio-based generative models for music have seen great strides recently, but so far have not managed to produce full-length music tracks with coherent musical structure. We show that by training a generative model on long temporal contexts it is possible to produce long-form music of up to 4m\,45s. Our model consists of a diffusion-transformer operating on a highly downsampled continuous latent representation {(latent rate of 21.5\,Hz)}. It obtains state-of-the-art generations according to metrics on audio quality and prompt alignment, and subjective tests reveal that it produces full-length music with coherent structure.

## Comparison with state-of-the-art (song describer dataset prompts)

**Prompt**: An uplifting jazz song that makes your head shake. 

| Our Model (stereo, 44.1kHz) | MusicGen-large-stereo (stereo, 32kHz) | 
| --------- | ---------------------- | 
| <audio controls preload=False><source src="audio/1001_sa2.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> | <audio controls preload=False><source src="audio/1001_musicgen.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> |

**Prompt**: One cannot avoid moving the feet and neck listening to this fast and loopy brazilian tune.

| Our Model | MusicGen-large-stereo  | 
| --------- | ---------------------- | 
| <audio controls preload=False><source src="audio/94_sa2.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> | <audio controls preload=False><source src="audio/94_musicgen.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> |

**Prompt**: Ambiental song that evokes calm with a progression of stereo electronic elements.

| Our Model | MusicGen-large-stereo  | 
| --------- | ---------------------- | 
| <audio controls preload=False><source src="audio/906_sa2.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> | <audio controls preload=False><source src="audio/906_musicgen.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> |

**Prompt**: This song starts with a ukulele and builds up with percussion using claps and an acoustic guitar that plays the same rhythm as the ukulele with melody played on a xylophone and has a very upbeat feel to it.

| Our Model (stereo, 44.1kHz) | MusicGen-large-stereo (stereo, 32kHz) | Ground-truth (stereo, 44.1kHz) | 
| --------- | -------------- | --------------- | 
| <audio controls preload=False><source src="audio/1069_sa2.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> | <audio controls preload=False><source src="audio/1969_musicgen.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> | <audio controls preload=False><source src="audio/1069.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> |

**Prompt**: Calming instrumental music primarily on piano can be used for relaxing.

| Our Model | MusicGen-large-stereo | Ground-truth | 
| --------- | -------------- | --------------- | 
| <audio controls preload=False><source src="audio/1091_sa2.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> | <audio controls preload=False><source src="audio/1091_musicgen.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> | <audio controls preload=False><source src="audio/1091.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> |

**Prompt**: A dance music club banger, with a heavy kick, subtle supporting percussion like tabla and bongos, prominent pop synth lines, and a repetitive hook.

| Our Model | MusicGen-large-stereo | Ground-truth | 
| --------- | -------------- | --------------- | 
| <audio controls preload=False><source src="audio/3_sa2.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> | <audio controls preload=False><source src="audio/3_musicgen.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> | <audio controls preload=False><source src="audio/3.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> |

These prompts/audios were used for the qualitative study we report in our paper.

## Additional creative capabilities

**Audio-to-audio**
 With diffusion models is possible to perform some degree of style-transfer by initializing the noise with audio during sampling. This capability can be used to modify the aesthetics of an existing recording based on a given text prompt, whilst maintaining the reference audio's structure (e.g., a beatbox recording could be style-transfered to produce realistic-sounding drums). As a result, our model can be influenced by not only text prompts but also audio inputs, enhancing its controllability and expressiveness. We noted that when initialized with voice recordings (such as beatbox or onomatopoeias), there is a sensation of control akin to an instrument.

| Input audio | Output audio | Prompt |
| ----------- | ------------ | ------ |
|<audio controls preload=False><source src="audio/input_bass.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>|<audio controls preload=False><source src="audio/bass.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>| Bass guitar|
|<audio controls preload=False><source src="audio/input_vibraphone.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>|<audio controls preload=False><source src="audio/vibraphone.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>| format: solo, instruments: vibraphone |
|<audio controls preload=False><source src="audio/input_707.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>|<audio controls preload=False><source src="audio/707.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>| Genre: UK Bass, Instruments: 707 Drum Machine, Strings, 808 bass stabs, Beautiful Synths |
|<audio controls preload=False><source src="audio/input_whistle.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>|<audio controls preload=False><source src="audio/whistle.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>| Guitar |
|<audio controls preload=False><source src="audio/input_hum.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>|<audio controls preload=False><source src="audio/hum.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>| Drums |

**Vocal music**
The training dataset contains a subset of music with vocals. Our focus is on the generation of instrumental music, so we do not provide any conditioning based on lyrics. As a result, when the model is prompted for vocals, the model's generations contains vocal-like melodies without intelligible words. Whilst not a substitute for intelligible vocals, these sounds have an artistic and textural value of their own.

|<audio controls preload=False><source src="audio/vocals1.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>|<audio controls preload=False><source src="audio/vocals2.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>|
|<audio controls preload=False><source src="audio/vocals3.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>|<audio controls preload=False><source src="audio/vocals4.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>|
|<audio controls preload=False><source src="audio/vocals5.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>|<audio controls preload=False><source src="audio/vocals6.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>|

**Short-form audio generation**
The training set does not exclusively contain long-form music. It also contains shorter sounds like sound effects or instrument samples. As a consequence, our model is also capable of producing such sounds when prompted appropriately.

| Generation by our model | Prompt |
| ----------------------- | ------ |
|<audio controls preload=False><source src="audio/dog.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>| Dog barking |
|<audio controls preload=False><source src="audio/ringtone.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>| Ringtone |
|<audio controls preload=False><source src="audio/waves.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>| Waves |
|<audio controls preload=False><source src="audio/helicopter.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>| Helicopter passing by from left to right |
|<audio controls preload=False><source src="audio/chicken.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>| Fowl, chicken, rooster, crowing, cock-a-doodle-doo |

## Memorization analysis

Recent works examined the potential of generative models to memorize training data, especially for repeated elements in the training set. Further, musicLM conducted a memorization analysis to address concerns on the potential misappropriation of creative content. Adhering to principles of responsible model development, we also run a comprehensive study on memorization. 

Considering the increased probability of memorizing repeated music within the dataset, we start by studying if our training set contains repeated data. We embed all our training data using the LAION-CLAP audio encoder to select audios that are close in this space based on a manually set threshold. The threshold is set such that the selected audios correspond to exact replicas. With this process, we identify 5566 repeated audios in our training set.

We compare our model's generations against the training set in LAION-CLAP space. Generations are from 5566 prompts within the repeated training data (in-distribution), and 586 prompts from the Song Describer Dataset (no-singing, out-of-distribution). We then identify the top-50 generated music that is closest to the training data and listen. 

We extensively listened to potential memorization candidates, and **could not find memorization**. Those are the most interesting candidates from (repeated) training data prompts:

| Generation by our model | Closest #1 | Closest #2 | Closest #3 | Prompt |
| ----------------------- | ---------- | ---------- | ---------- | ------ |
| <audio controls preload=False><source src="audio/427105.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> | <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.427160">427160</a>| <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.427105">427105</a>| <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.140843">140843</a>| Birds chirping, forest birds, tropical, africa wild life, singing birds, sound effects. |
| <audio controls preload=False><source src="audio/978535.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> | <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.978924">978924</a>| <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.979616">979616</a>| <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.978717">978717</a>| Totally rad 8-bit melodies and intense arps create that fearless throwback vibe. |
| <audio controls preload=False><source src="audio/972457.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> | <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.979544">979544</a>| <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.979695">979695</a>| <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.979670">979670</a>| Totally rad 8-bit melodies and intense arps create that strong-willed throwback vibe. |
| <audio controls preload=False><source src="audio/978661.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> | <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.972466">972466</a>| <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.972983">972983</a>| <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.973055">973055</a>| Pleasant strings create desire in this adamant scoring cue. |

We found a fair ammount of 8-bit/chiptunes that were repeated in the training dataset. Still, our model does not memorize them.

We even selected additional outstanding generations from Song Describer Dataset prompts, and **could not find memorization**. Those are the most interesting memorization candidates:

| Generation by our model | Closest #1 | Closest #2 | Closest #3 | Prompt |
| ----------------------- | ---------- | ---------- | ---------- | ------ |
| <audio controls preload=False><source src="audio/94_original.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> | <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.796563">796563</a>| <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.1083119">1083119</a>| <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.634461">634461</a>| One cannot avoid moving the feet and neck listening to this fast and loopy brazilian tune. |
| <audio controls preload=False><source src="audio/1001_original.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> | <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.279428">279428</a>| <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.1082095">1082095</a>| <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.326758">326758</a>| An uplifting jazz song that makes your head shake. |
| <audio controls preload=False><source src="audio/1091_original.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> | <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.1024058">1024058</a>| <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.1023046">1023046</a>| <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.788950">788950</a>| Calming instrumental music primarily on piano can be used for relaxing. |
| <audio controls preload=False><source src="audio/1069_original.mp3" type="audio/mpeg">Audio not supported by your browser.</audio> | <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.470048">470048</a>| <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.470047">470047</a>| <a href="https://www.audiosparx.com/sa/summary/play.cfm/crumb.31/crumc.0/sound_iid.696082">696082</a>| This song starts with a ukulele and builds up with percussion using claps and an acoustic guitar that plays the same rhythm as the ukulele with melody played on a xylophone and has a very upbeat feel to it. |

## Autoencoder: reconstructions

This comparison is useful to evaluate the audio fidelity capabilities of the autoencoder. On the left, we have the ground truth recording. On the right, we take the ground truth recording and end pass it through the autoencoder. Note that the autoencoder reconstruction is fairly transparent, very close to the ground truth.

| Ground truth | Autoencoder reconstruction |
| ------------ | -------------------------- |
|<audio controls preload=False><source src="audio/226.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>|<audio controls preload=False><source src="audio/226.wav" type="audio/mpeg">Audio not supported by your browser.</audio><br>|
|<audio controls preload=False><source src="audio/3112.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>|<audio controls preload=False><source src="audio/3112.wav" type="audio/mpeg">Audio not supported by your browser.</audio><br>|
|<audio controls preload=False><source src="audio/3453.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>|<audio controls preload=False><source src="audio/3453.wav" type="audio/mpeg">Audio not supported by your browser.</audio><br>|
|<audio controls preload=False><source src="audio/4880.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>|<audio controls preload=False><source src="audio/4880.wav" type="audio/mpeg">Audio not supported by your browser.</audio><br>|
|<audio controls preload=False><source src="audio/4883.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>|<audio controls preload=False><source src="audio/4883.wav" type="audio/mpeg">Audio not supported by your browser.</audio><br>|
|<audio controls preload=False><source src="audio/5084.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>|<audio controls preload=False><source src="audio/5084.wav" type="audio/mpeg">Audio not supported by your browser.</audio><br>|
|<audio controls preload=False><source src="audio/5089.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>|<audio controls preload=False><source src="audio/5089.wav" type="audio/mpeg">Audio not supported by your browser.</audio><br>|
|<audio controls preload=False><source src="audio/5339.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>|<audio controls preload=False><source src="audio/5339.wav" type="audio/mpeg">Audio not supported by your browser.</audio><br>|
|<audio controls preload=False><source src="audio/5340.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>|<audio controls preload=False><source src="audio/5340.wav" type="audio/mpeg">Audio not supported by your browser.</audio><br>|
|<audio controls preload=False><source src="audio/5341.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>|<audio controls preload=False><source src="audio/5341.wav" type="audio/mpeg">Audio not supported by your browser.</audio><br>|
|<audio controls preload=False><source src="audio/5343.mp3" type="audio/mpeg">Audio not supported by your browser.</audio><br>|<audio controls preload=False><source src="audio/5343.wav" type="audio/mpeg">Audio not supported by your browser.</audio><br>|


