# neural-set-expansion

note:

There's a minor bug in the [pretrained model](http://nervana-modelzoo.s3.amazonaws.com/NLP/SetExp/enwiki-20171201_pretrained_set_expansion.txt) provided in the original implementation [page](http://nlp_architect.nervanasys.com/term_set_expansion.html).

`cat enwiki-20171201_pretrained_set_expansion.txt | grep -n 0.50.118487`

you will see that there's a invalid "number" at line 1066088, which may cause the model to fail.

Fix:

`sed -i.bak 's/0.50.118487/0.118487/g' enwiki-20171201_pretrained_set_expansion.txt`
