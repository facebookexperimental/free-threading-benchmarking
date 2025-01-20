# Results vs. base

- fork: python
- ref: bca35f0e782848ae2acd
- machine: linux-x86_64
- commit hash: bca35f0
- commit date: 2025-01-20
- overall geometric mean: 1.127x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250120-3.14.0a4+-bca35f0/bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json | results/bm-20250120-3.14.0a4+-bca35f0-NOGIL/bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 514 ms                                                                                                            | 558 ms: 1.08x slower                                                                                                    |
| html5lib       | 81.4 ms                                                                                                           | 107 ms: 1.32x slower                                                                                                    |
| sphinx         | 1.45 sec                                                                                                          | 1.62 sec: 1.11x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.12x slower                                                                                                            |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | results/bm-20250120-3.14.0a4+-bca35f0/bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json | results/bm-20250120-3.14.0a4+-bca35f0-NOGIL/bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json |
|-------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| async_tree_none_tg      | 398 ms                                                                                                            | 342 ms: 1.17x faster                                                                                                    |
| async_tree_io_tg        | 867 ms                                                                                                            | 758 ms: 1.14x faster                                                                                                    |
| async_tree_memoization  | 563 ms                                                                                                            | 534 ms: 1.05x faster                                                                                                    |
| async_generators        | 535 ms                                                                                                            | 573 ms: 1.07x slower                                                                                                    |
| coroutines              | 30.7 ms                                                                                                           | 34.2 ms: 1.12x slower                                                                                                   |
| async_tree_cpu_io_mixed | 711 ms                                                                                                            | 810 ms: 1.14x slower                                                                                                    |
| Geometric mean          | (ref)                                                                                                             | 1.01x slower                                                                                                            |

Benchmark hidden because not significant (5): async_tree_io, async_tree_memoization_tg, async_tree_none, asyncio_websockets, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250120-3.14.0a4+-bca35f0/bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json | results/bm-20250120-3.14.0a4+-bca35f0-NOGIL/bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 225 ms                                                                                                            | 240 ms: 1.07x slower                                                                                                    |
| float          | 106 ms                                                                                                            | 119 ms: 1.12x slower                                                                                                    |
| nbody          | 126 ms                                                                                                            | 185 ms: 1.46x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.20x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250120-3.14.0a4+-bca35f0/bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json | results/bm-20250120-3.14.0a4+-bca35f0-NOGIL/bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_effbot   | 4.52 ms                                                                                                           | 4.06 ms: 1.11x faster                                                                                                   |
| regex_compile  | 166 ms                                                                                                            | 204 ms: 1.23x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.01x slower                                                                                                            |

Benchmark hidden because not significant (2): regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250120-3.14.0a4+-bca35f0/bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json | results/bm-20250120-3.14.0a4+-bca35f0-NOGIL/bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| unpickle_pure_python | 300 us                                                                                                            | 343 us: 1.14x slower                                                                                                    |
| json_loads           | 39.5 us                                                                                                           | 46.7 us: 1.18x slower                                                                                                   |
| tomli_loads          | 2.58 sec                                                                                                          | 3.11 sec: 1.20x slower                                                                                                  |
| xml_etree_generate   | 112 ms                                                                                                            | 138 ms: 1.23x slower                                                                                                    |
| xml_etree_process    | 82.9 ms                                                                                                           | 102 ms: 1.24x slower                                                                                                    |
| xml_etree_parse      | 188 ms                                                                                                            | 243 ms: 1.30x slower                                                                                                    |
| json_dumps           | 15.1 ms                                                                                                           | 22.5 ms: 1.49x slower                                                                                                   |
| Geometric mean       | (ref)                                                                                                             | 1.19x slower                                                                                                            |

Benchmark hidden because not significant (2): xml_etree_iterparse, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250120-3.14.0a4+-bca35f0/bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json | results/bm-20250120-3.14.0a4+-bca35f0-NOGIL/bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 30.7 ms                                                                                                           | 34.2 ms: 1.11x slower                                                                                                   |
| python_startup_no_site | 17.2 ms                                                                                                           | 22.0 ms: 1.28x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.19x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250120-3.14.0a4+-bca35f0/bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json | results/bm-20250120-3.14.0a4+-bca35f0-NOGIL/bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 70.8 ms                                                                                                           | 87.3 ms: 1.23x slower                                                                                                   |
| django_template | 50.2 ms                                                                                                           | 64.6 ms: 1.29x slower                                                                                                   |
| genshi_text     | 28.8 ms                                                                                                           | 40.5 ms: 1.40x slower                                                                                                   |
| mako            | 16.2 ms                                                                                                           | 25.0 ms: 1.55x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.36x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                | results/bm-20250120-3.14.0a4+-bca35f0/bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json | results/bm-20250120-3.14.0a4+-bca35f0-NOGIL/bm-20250120-linux-x86_64-python-bca35f0e782848ae2acd-3.14.0a4+-bca35f0.json |
|--------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| create_gc_cycles         | 4.60 ms                                                                                                           | 2.83 ms: 1.62x faster                                                                                                   |
| async_tree_none_tg       | 398 ms                                                                                                            | 342 ms: 1.17x faster                                                                                                    |
| async_tree_io_tg         | 867 ms                                                                                                            | 758 ms: 1.14x faster                                                                                                    |
| regex_effbot             | 4.52 ms                                                                                                           | 4.06 ms: 1.11x faster                                                                                                   |
| bench_mp_pool            | 100 ms                                                                                                            | 94.1 ms: 1.06x faster                                                                                                   |
| pycparser                | 1.68 sec                                                                                                          | 1.58 sec: 1.06x faster                                                                                                  |
| async_tree_memoization   | 563 ms                                                                                                            | 534 ms: 1.05x faster                                                                                                    |
| deepcopy_reduce          | 3.95 us                                                                                                           | 4.14 us: 1.05x slower                                                                                                   |
| logging_silent           | 139 ns                                                                                                            | 147 ns: 1.06x slower                                                                                                    |
| coverage                 | 134 ms                                                                                                            | 141 ms: 1.06x slower                                                                                                    |
| sqlite_synth             | 4.03 us                                                                                                           | 4.28 us: 1.06x slower                                                                                                   |
| meteor_contest           | 164 ms                                                                                                            | 175 ms: 1.07x slower                                                                                                    |
| pidigits                 | 225 ms                                                                                                            | 240 ms: 1.07x slower                                                                                                    |
| comprehensions           | 25.2 us                                                                                                           | 26.9 us: 1.07x slower                                                                                                   |
| async_generators         | 535 ms                                                                                                            | 573 ms: 1.07x slower                                                                                                    |
| dulwich_log              | 102 ms                                                                                                            | 109 ms: 1.07x slower                                                                                                    |
| sqlglot_optimize         | 76.1 ms                                                                                                           | 82.3 ms: 1.08x slower                                                                                                   |
| 2to3                     | 514 ms                                                                                                            | 558 ms: 1.08x slower                                                                                                    |
| sqlglot_normalize        | 156 ms                                                                                                            | 170 ms: 1.09x slower                                                                                                    |
| many_optionals           | 1.25 ms                                                                                                           | 1.39 ms: 1.11x slower                                                                                                   |
| sphinx                   | 1.45 sec                                                                                                          | 1.62 sec: 1.11x slower                                                                                                  |
| python_startup           | 30.7 ms                                                                                                           | 34.2 ms: 1.11x slower                                                                                                   |
| scimark_lu               | 158 ms                                                                                                            | 176 ms: 1.12x slower                                                                                                    |
| float                    | 106 ms                                                                                                            | 119 ms: 1.12x slower                                                                                                    |
| coroutines               | 30.7 ms                                                                                                           | 34.2 ms: 1.12x slower                                                                                                   |
| crypto_pyaes             | 107 ms                                                                                                            | 121 ms: 1.12x slower                                                                                                    |
| sympy_expand             | 604 ms                                                                                                            | 682 ms: 1.13x slower                                                                                                    |
| fannkuch                 | 577 ms                                                                                                            | 652 ms: 1.13x slower                                                                                                    |
| connected_components     | 824 ms                                                                                                            | 937 ms: 1.14x slower                                                                                                    |
| async_tree_cpu_io_mixed  | 711 ms                                                                                                            | 810 ms: 1.14x slower                                                                                                    |
| unpickle_pure_python     | 300 us                                                                                                            | 343 us: 1.14x slower                                                                                                    |
| pylint                   | 405 ms                                                                                                            | 467 ms: 1.15x slower                                                                                                    |
| go                       | 163 ms                                                                                                            | 188 ms: 1.15x slower                                                                                                    |
| shortest_path            | 917 ms                                                                                                            | 1.06 sec: 1.15x slower                                                                                                  |
| scimark_sor              | 161 ms                                                                                                            | 189 ms: 1.17x slower                                                                                                    |
| spectral_norm            | 136 ms                                                                                                            | 160 ms: 1.17x slower                                                                                                    |
| pprint_safe_repr         | 940 ms                                                                                                            | 1.10 sec: 1.18x slower                                                                                                  |
| mdp                      | 3.54 sec                                                                                                          | 4.17 sec: 1.18x slower                                                                                                  |
| json_loads               | 39.5 us                                                                                                           | 46.7 us: 1.18x slower                                                                                                   |
| pprint_pformat           | 1.89 sec                                                                                                          | 2.25 sec: 1.19x slower                                                                                                  |
| tomli_loads              | 2.58 sec                                                                                                          | 3.11 sec: 1.20x slower                                                                                                  |
| sqlalchemy_declarative   | 188 ms                                                                                                            | 227 ms: 1.20x slower                                                                                                    |
| sympy_sum                | 219 ms                                                                                                            | 264 ms: 1.21x slower                                                                                                    |
| deepcopy_memo            | 44.4 us                                                                                                           | 53.7 us: 1.21x slower                                                                                                   |
| scimark_fft              | 460 ms                                                                                                            | 559 ms: 1.21x slower                                                                                                    |
| subparsers               | 35.0 ms                                                                                                           | 42.8 ms: 1.22x slower                                                                                                   |
| regex_compile            | 166 ms                                                                                                            | 204 ms: 1.23x slower                                                                                                    |
| xml_etree_generate       | 112 ms                                                                                                            | 138 ms: 1.23x slower                                                                                                    |
| genshi_xml               | 70.8 ms                                                                                                           | 87.3 ms: 1.23x slower                                                                                                   |
| xml_etree_process        | 82.9 ms                                                                                                           | 102 ms: 1.24x slower                                                                                                    |
| logging_format           | 9.85 us                                                                                                           | 12.2 us: 1.24x slower                                                                                                   |
| nqueens                  | 104 ms                                                                                                            | 130 ms: 1.25x slower                                                                                                    |
| sympy_integrate          | 30.1 ms                                                                                                           | 37.9 ms: 1.26x slower                                                                                                   |
| sqlglot_transpile        | 2.22 ms                                                                                                           | 2.80 ms: 1.26x slower                                                                                                   |
| bench_thread_pool        | 3.96 ms                                                                                                           | 5.00 ms: 1.26x slower                                                                                                   |
| sqlalchemy_imperative    | 24.9 ms                                                                                                           | 31.8 ms: 1.27x slower                                                                                                   |
| generators               | 39.3 ms                                                                                                           | 50.2 ms: 1.28x slower                                                                                                   |
| python_startup_no_site   | 17.2 ms                                                                                                           | 22.0 ms: 1.28x slower                                                                                                   |
| sqlglot_parse            | 1.82 ms                                                                                                           | 2.34 ms: 1.29x slower                                                                                                   |
| django_template          | 50.2 ms                                                                                                           | 64.6 ms: 1.29x slower                                                                                                   |
| telco                    | 10.8 ms                                                                                                           | 13.9 ms: 1.29x slower                                                                                                   |
| xml_etree_parse          | 188 ms                                                                                                            | 243 ms: 1.30x slower                                                                                                    |
| sympy_str                | 396 ms                                                                                                            | 516 ms: 1.30x slower                                                                                                    |
| html5lib                 | 81.4 ms                                                                                                           | 107 ms: 1.32x slower                                                                                                    |
| hexiom                   | 8.64 ms                                                                                                           | 11.5 ms: 1.33x slower                                                                                                   |
| pyflate                  | 604 ms                                                                                                            | 807 ms: 1.34x slower                                                                                                    |
| bpe_tokeniser            | 5.80 sec                                                                                                          | 7.77 sec: 1.34x slower                                                                                                  |
| richards_super           | 66.7 ms                                                                                                           | 92.3 ms: 1.38x slower                                                                                                   |
| scimark_monte_carlo      | 84.8 ms                                                                                                           | 118 ms: 1.39x slower                                                                                                    |
| raytrace                 | 346 ms                                                                                                            | 484 ms: 1.40x slower                                                                                                    |
| logging_simple           | 8.56 us                                                                                                           | 12.0 us: 1.40x slower                                                                                                   |
| genshi_text              | 28.8 ms                                                                                                           | 40.5 ms: 1.40x slower                                                                                                   |
| scimark_sparse_mat_mult  | 6.06 ms                                                                                                           | 8.51 ms: 1.40x slower                                                                                                   |
| thrift                   | 1.08 ms                                                                                                           | 1.55 ms: 1.43x slower                                                                                                   |
| deltablue                | 5.14 ms                                                                                                           | 7.35 ms: 1.43x slower                                                                                                   |
| nbody                    | 126 ms                                                                                                            | 185 ms: 1.46x slower                                                                                                    |
| json_dumps               | 15.1 ms                                                                                                           | 22.5 ms: 1.49x slower                                                                                                   |
| richards                 | 54.3 ms                                                                                                           | 81.5 ms: 1.50x slower                                                                                                   |
| typing_runtime_protocols | 206 us                                                                                                            | 315 us: 1.53x slower                                                                                                    |
| mako                     | 16.2 ms                                                                                                           | 25.0 ms: 1.55x slower                                                                                                   |
| Geometric mean           | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmark hidden because not significant (16): regex_v8, gc_traversal, xml_etree_iterparse, pathlib, pickle_pure_python, async_tree_io, docutils, json, regex_dna, async_tree_memoization_tg, async_tree_none, chaos, k_core, asyncio_websockets, async_tree_cpu_io_mixed_tg, deepcopy

- Geometric mean (including insignificant results): 1.127x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.19x