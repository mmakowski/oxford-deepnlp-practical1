`import gensim.models.Word2Vec` fails with

    Intel MKL FATAL ERROR: Cannot load libmkl_avx.so or libmkl_def.so.

Tried 

    LD_PRELOAD=~/anaconda3/envs/py3/lib/libmkl_core.so:~/anaconda3/envs/py3/lib/libmkl_avx.so python -c 'import gensim.models.Word2Vec' 2>&1 | grep -i error

This failed with

    python: symbol lookup error: /home/mmakowski/anaconda3/envs/py3/lib/libmkl_avx.so: undefined symbol: mkl_sparse_optimize_bsr_trsm_i8
