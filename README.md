# σ-VAE for Stochastic Video Generation. 
This repo contains the application of σ-VAE to the paper on [Stochastic Video Generation with a Learned Prior](https://arxiv.org/abs/1802.07687). See the σ-VAE [project page](https://orybkin.github.io/sigma-vae/) for more info and alternative implementations!

In this implementation, we add a learned shared decoder variance. This method is very easy to implement, and it allows to achieve good results without tuning the heuristic weight beta since the decoder variance balances the objective. To train the σ-VAE, run this command that sets beta=1, learn_beta=1: 

```
python train_svg_lp.py --dataset smmnist --num_digits 2 --g_dim 128 --z_dim 10 --beta 1 --learn_beta=1 --data_root /path/to/data/ --log_dir /logs/will/be/saved/here/
```

See the original SVG code for more examples.
