# Number-Plate-Recognition

Run the code by executing following steps

```shellscript
$ cd darknet && make
```
```shellscript
$ bash get-networks.sh
```
```shellscript
$ bash run.sh -i samples/test -o /tmp/output -c /tmp/output/results.csv
```
The following command can be used to train the network from scratch

```shellscript
$ mkdir models
$ python create-model.py eccv models/eccv-model-scratch
$ python train-detector.py --model models/eccv-model-scratch --name my-trained-model --train-dir samples/train-detector --output-dir models/my-trained-model/ -op Adam -lr .001 -its 300000 -bs 64
```
