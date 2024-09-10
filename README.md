# The Big Thick
Max 8 code for my Intro to Audio Tech I final project. The idea was to add different layers of my guitar tone on top of the original signal. That includes harmonizers, chorus, and reverb.

## Harmonizers
You can add a synthesized or pitch shifted signal on top of your original dry signal. Pitch tracking is monophonic and it isn't perfect, since I am using an object designed for sounds without percussive elements. If I ever want to make this project more usable I would make the input tracking more guitar friendly, but I haven't had a song need the sound enough for me to incorporate Max into my live set.

You can choose an interval, major or minor. If in dumb mode, the interval is always constant. If you choose a key, the interval changes to harmonize correctly with the scale. You can use choose what waveform to be synthesized over, or just use the guitar input pitch shifted. If shifted, you can choose the amount of delay to use to balance between latency and artifacts.

There is a filter section to remove treble from waveforms (or artifact heavy pitch shifting). The pitch reference is set based on the low E string on a guitar. Once you set the filter cutoff to taste, you can change the tracking. A setting of 0 means the cutoff stays constant. A setting of 1 means the cutoff moves proportionally with the note played. A setting of 2 increases the ratio between the note and the cutoff, allowing for brighter tones at the top of the playing range.

## Chorus
This is a basic chorus with speed and depth. It has two delay lines that are phase shifted to create stereo width.

## Reverb
This is a modification of the Schroeder reverb algorithm recommended by the [Spin Semiconductor knowledge base](https://www.spinsemi.com/knowledge_base/effects.html#Reverberation). The input is smeared with a delay line and the all-pass coefficients are modified over time with LFOs. You can cutoff high frequencies and add pitch shifted versions of the reverberated signal to the delay line.
