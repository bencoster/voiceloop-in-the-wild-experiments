VoiceLoop In the Wild experiments.

This is an attempt to reproduce the In the Wild experiments for VoiceLoop https://ytaigman.github.io/loop/

We have collected 8000 audio samples of around 3 seconds each from YouTube videos of Donald Trump, Barack Obama, Hillary Clinton and Bill Clinton. There are around 2000 samples for each speaker along with the automated caption text.

We have an open issue with the authors of VoiceLoop asking for guidance https://github.com/facebookresearch/loop/issues/58

So far we have tried to train with the following parameters:

python train.py --expName politicians --noise 4 --seq-len 100 --nspk 4 --epochs 90 --data data/politicians/

python train.py --expName politicians_step2 --noise 2 --seq-len 1000 --nspk 4 --epochs 90 --data data/politicians/ --checkpoints checkpoints/politicians/bestmodel.pth

python train.py --expName politicians_step3 --noise 1 --seq-len 1000 --nspk 4 --epochs 90 --data data/politicians/ --checkpoint checkpoints/politicians_step2/bestmodel.pth

We haven't been successful yet.

We'll soon add more datasets.
