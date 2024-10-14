# Video Scene Graph Generation

### Docker Image

```bash
docker pull baekkop/vsgg
### After a container is made, start and attach the container.
cd /workspace/VSGG
```

### Train

```bash
python TEATGT_train.py --mode predcls --datasize large --data_path /DATA/PATH --lr 1e-5 --warmup 3 --nepoch 30 --lap_node_id --lap_node_id_k 50 --type_id --save_path /SAVE/PATH --use_ctl_loss --use_cons_str_loss --use_cons_sem_loss
```

### Test

```bash
python TEATGT_test.py --mode predcls --datasize mini --data_path /DATA/PATH --model_path /MODEL/PATH --output_path /OUTPUT/PATH --lap_node_id --lap_node_id_k 50 --type_id
```

### Evaluate

```bash
python TEATGT_evaluate.py --mode predcls --datasize mini --data_path /DATA/PATH --model_path /MODEL/PATHmodels/ --output_path /OUTPUT/PATH --lap_node_id --lap_node_id_k 50 --type_id
```

### Reference Link
- Tokenized Graph Transformer Reference: https://arxiv.org/abs/2207.02505
- Action Genome Dataset Reference: https://openaccess.thecvf.com/content_CVPR_2020/papers/Ji_Action_Genome_Actions_As_Compositions_of_Spatio-Temporal_Scene_Graphs_CVPR_2020_paper.pdf
- Unbiased Video Scene Graph Generation Reference: https://openaccess.thecvf.com/content/CVPR2023/papers/Nag_Unbiased_Scene_Graph_Generation_in_Videos_CVPR_2023_paper.pdf
