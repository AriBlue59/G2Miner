
# 高级计算机体系结构课程报告仓库

## 成员信息

| **成员**   | **学号**     | **邮箱**                                             |
| ---------------- | ------------------ | ---------------------------------------------------------- |
| **高英淇** | **24214306** | [gaoyq28@mail2.sysu.edu.cn](mailto:gaoyq28@mail2.sysu.edu.cn) |
| **郭嘉健** | **24214307** | [guojj59@mail2.sysu.edu.cn](mailto:guojj59@mail2.sysu.edu.cn) |

## How to use

`<OSDI-experiments-guide.md>` 是所复现仓库的官方指导

**为了复现'results/'中的内容，可执行以下命令**

```
$ make
```

### results/GuoJiajian

**Table 4**

```
$ bin/tc_gpu_base inputs/livej/graph      > lj-tc.log 2>&1
$ bin/tc_gpu_base inputs/orkut/graph      > ok-tc.log 2>&1
$ bin/tc_gpu_base inputs/twitter20/graph  > tw2-tc.log 2>&1
$ bin/tc_gpu_base inputs/twitter40/graph  > tw4-tc.log 2>&1
$ bin/tc_gpu_base inputs/friendster/graph > fr-tc.log 2>&1
$ bin/tc_gpu_base inputs/uk2007/graph     > uk-tc.log 2>&1
```

**Table 5**

```
# 4-cliques
$ bin/clique_gpu_base inputs/livej/graph      4 > lj-4-cliques.log 2>&1
$ bin/clique_gpu_base inputs/orkut/graph      4 > ok-4-cliques.log 2>&1
$ bin/clique_gpu_base inputs/twitter20/graph  4 > tw2-4-cliques.log 2>&1
$ bin/clique_gpu_base inputs/twitter40/graph  4 > tw4-4-cliques.log 2>&1
$ bin/clique_gpu_base inputs/friendster/graph 4 > fr-4-cliques.log 2>&1
$ # 5-cliques
$ bin/clique_gpu_base inputs/livej/graph      5 > lj-5-cliques.log 2>&1
$ bin/clique_gpu_base inputs/orkut/graph      5 > ok-5-cliques.log 2>&1
$ bin/clique_gpu_base inputs/friendster/graph 5 > fr-5-cliques.log 2>&1
```

**Table 6**

```
$ # diamond
$ bin/sgl_gpu_base inputs/livej/graph diamond        > lj-diamond.log 2>&1
$ bin/sgl_gpu_base inputs/orkut/graph diamond        > or-diamond.log 2>&1
$ bin/sgl_gpu_base inputs/twitter20/graph diamond    > tw2-diamond.log 2>&1
$ bin/sgl_gpu_base inputs/twitter40/graph diamond    > tw4-diamond.log 2>&1
$ bin/sgl_gpu_base inputs/friendster/graph diamond   > fr-diamond.log 2>&1
$ # rectangle
$ bin/sgl_gpu_base inputs/livej/graph rectangle      > lj-rectangle.log 2>&1
$ bin/sgl_gpu_base inputs/orkut/graph rectangle      > or-rectangle.log 2>&1
$ bin/sgl_gpu_base inputs/friendster/graph rectangle > fr-rectangle.log 2>&1
```

**Figure 9**

```
$ bin/tc_multigpu inputs/twitter40/graph 8 > tw4-tc-8gpu.log 2>&1
$ bin/sgl_multigpu inputs/friendster/graph rectangle 4 > fr-rectangle-4gpu.log 2>&1
$ bin/motif_multigpu inputs/twitter20/graph 3 6 > tw2-3-motifs-6gpu.log 2>&1
```

### results/GaoYingqi

**Table 7**

```
$ # 3-motifs
$ bin/motif_gpu_base inputs/livej/graph      3 > lj-3-motifs.log 2>&1
$ bin/motif_gpu_base inputs/orkut/graph      3 > ok-3-motifs.log 2>&1
$ bin/motif_gpu_base inputs/twitter20/graph  3 > tw2-3-motifs.log 2>&1
$ bin/motif_gpu_base inputs/twitter40/graph  3 > tw4-3-motifs.log 2>&1
$ bin/motif_gpu_base inputs/friendster/graph 3 > fr-3-motifs.log 2>&1
$ # 4-motifs
$ bin/motif_gpu_base inputs/livej/graph      4 > lj-4-motifs.log 2>&1
$ bin/motif_gpu_base inputs/orkut/graph      4 > ok-4-motifs.log 2>&1
$ bin/motif_gpu_base inputs/friendster/graph 4 > fr-4-motifs.log 2>&1
```

**Table 8**

```
$ # Mico
$./bin/fsm_gpu_base inputs/mico/graph 2 300  > mi-fsm-3-300.log 2>&1
$./bin/fsm_gpu_base inputs/mico/graph 2 500  > mi-fsm-3-500.log 2>&1
$./bin/fsm_gpu_base inputs/mico/graph 2 1000 > mi-fsm-3-1000.log 2>&1
$./bin/fsm_gpu_base inputs/mico/graph 2 5000 > mi-fsm-3-5000.log 2>&1
$ # Patent
$./bin/fsm_gpu_base inputs/patent_citations/graph 2 300  > pa-fsm-3-300.log 2>&1
$./bin/fsm_gpu_base inputs/patent_citations/graph 2 500  > pa-fsm-3-500.log 2>&1
$./bin/fsm_gpu_base inputs/patent_citations/graph 2 1000 > pa-fsm-3-1000.log 2>&1
$./bin/fsm_gpu_base inputs/patent_citations/graph 2 5000 > pa-fsm-3-5000.log 2>&1
$ # Youtube
$./bin/fsm_gpu_base inputs/youtube/graph 2 300  > yo-fsm-3-300.log 2>&1
$./bin/fsm_gpu_base inputs/youtube/graph 2 500  > yo-fsm-3-500.log 2>&1
$./bin/fsm_gpu_base inputs/youtube/graph 2 1000 > yo-fsm-3-1000.log 2>&1
$./bin/fsm_gpu_base inputs/youtube/graph 2 5000 > yo-fsm-3-5000.log 2>&1
```
