# DeepBeat

Deep learning driven hip-hop beat generation for my [AAR
project](https://github.com/nicholaschiang/aar).

## Instructions

First, create a [virtual environment](https://virtualenv.pypa.io/en/stable/) and
install our dependencies by running:

```
$ virtualenv -p python3 .venv
$ source .venv/bin/activate
$ make dev
```

Then, run on CPU with command:

```
$ python generator.py [# of epochs]
```

Or, run on GPU with command:

```
$ THEANO_FLAGS=mode=FAST_RUN,device=gpu,floatX=float32 python generator.py
  [# of epochs]
```

Note: running Keras/Theano on GPU is formally supported for only NVIDIA cards
(CUDA backend).

Note: `preprocess.py` must be modified to work with other MIDI files (the
relevant "melody" MIDI part needs to be selected). The ability to handle this
natively is a planned feature.

## Credits

This project was forked from Ji-Sung Kim's
[**deepjazz** project](https://github.com/jisungk/deepjazz) who used a lot of
the preprocessing code (with permission) from Evan Chow's [**jazzml**
project](https://github.com/evancchow/jazzml). Public examples from the [Keras
documentation](https://github.com/fchollet/keras) were also referenced.
