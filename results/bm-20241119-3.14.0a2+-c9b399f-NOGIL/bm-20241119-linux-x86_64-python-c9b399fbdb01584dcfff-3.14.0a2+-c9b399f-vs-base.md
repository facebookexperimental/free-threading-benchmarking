# Results vs. base

- fork: python
- ref: c9b399fbdb01584dcfff
- machine: linux-x86_64
- commit hash: c9b399f
- commit date: 2024-11-19
- overall geometric mean: 1.43x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.35x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20241119-3.14.0a2+-c9b399f/bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f.json | results/bm-20241119-3.14.0a2+-c9b399f-NOGIL/bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 410 ms                                                                                                            | 648 ms: 1.58x slower                                                                                                    |
| docutils       | 3.66 sec                                                                                                          | 4.60 sec: 1.26x slower                                                                                                  |
| html5lib       | 90.1 ms                                                                                                           | 147 ms: 1.63x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.48x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | results/bm-20241119-3.14.0a2+-c9b399f/bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f.json | results/bm-20241119-3.14.0a2+-c9b399f-NOGIL/bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f.json |
|------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| asyncio_tcp      | 901 ms                                                                                                            | 1.03 sec: 1.15x slower                                                                                                  |
| async_generators | 586 ms                                                                                                            | 679 ms: 1.16x slower                                                                                                    |
| asyncio_tcp_ssl  | 2.73 sec                                                                                                          | 3.21 sec: 1.18x slower                                                                                                  |
| coroutines       | 31.6 ms                                                                                                           | 40.9 ms: 1.29x slower                                                                                                   |
| Geometric mean   | (ref)                                                                                                             | 1.15x slower                                                                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20241119-3.14.0a2+-c9b399f/bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f.json | results/bm-20241119-3.14.0a2+-c9b399f-NOGIL/bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| float          | 119 ms                                                                                                            | 201 ms: 1.69x slower                                                                                                    |
| nbody          | 123 ms                                                                                                            | 257 ms: 2.08x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.53x slower                                                                                                            |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20241119-3.14.0a2+-c9b399f/bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f.json | results/bm-20241119-3.14.0a2+-c9b399f-NOGIL/bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_compile  | 180 ms                                                                                                            | 287 ms: 1.60x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.13x slower                                                                                                            |

Benchmark hidden because not significant (3): regex_effbot, regex_dna, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20241119-3.14.0a2+-c9b399f/bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f.json | results/bm-20241119-3.14.0a2+-c9b399f-NOGIL/bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pickle               | 17.5 us                                                                                                           | 15.7 us: 1.12x faster                                                                                                   |
| pickle_list          | 7.49 us                                                                                                           | 6.85 us: 1.09x faster                                                                                                   |
| json_loads           | 38.7 us                                                                                                           | 40.7 us: 1.05x slower                                                                                                   |
| xml_etree_iterparse  | 155 ms                                                                                                            | 167 ms: 1.08x slower                                                                                                    |
| unpickle_list        | 7.03 us                                                                                                           | 7.70 us: 1.10x slower                                                                                                   |
| unpickle             | 18.9 us                                                                                                           | 21.4 us: 1.13x slower                                                                                                   |
| json_dumps           | 15.5 ms                                                                                                           | 19.5 ms: 1.26x slower                                                                                                   |
| xml_etree_generate   | 119 ms                                                                                                            | 164 ms: 1.38x slower                                                                                                    |
| xml_etree_process    | 82.2 ms                                                                                                           | 126 ms: 1.53x slower                                                                                                    |
| tomli_loads          | 2.62 sec                                                                                                          | 4.09 sec: 1.56x slower                                                                                                  |
| unpickle_pure_python | 295 us                                                                                                            | 524 us: 1.78x slower                                                                                                    |
| pickle_pure_python   | 436 us                                                                                                            | 776 us: 1.78x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.21x slower                                                                                                            |

Benchmark hidden because not significant (2): xml_etree_parse, pickle_dict

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20241119-3.14.0a2+-c9b399f/bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f.json | results/bm-20241119-3.14.0a2+-c9b399f-NOGIL/bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 14.0 ms                                                                                                           | 18.8 ms: 1.34x slower                                                                                                   |
| python_startup         | 19.9 ms                                                                                                           | 29.5 ms: 1.49x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.41x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20241119-3.14.0a2+-c9b399f/bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f.json | results/bm-20241119-3.14.0a2+-c9b399f-NOGIL/bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 71.6 ms                                                                                                           | 112 ms: 1.56x slower                                                                                                    |
| django_template | 46.7 ms                                                                                                           | 79.0 ms: 1.69x slower                                                                                                   |
| genshi_text     | 28.7 ms                                                                                                           | 50.2 ms: 1.75x slower                                                                                                   |
| mako            | 16.7 ms                                                                                                           | 30.4 ms: 1.81x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.70x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                | results/bm-20241119-3.14.0a2+-c9b399f/bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f.json | results/bm-20241119-3.14.0a2+-c9b399f-NOGIL/bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f.json |
|--------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| create_gc_cycles         | 2.34 ms                                                                                                           | 1.83 ms: 1.28x faster                                                                                                   |
| gc_traversal             | 5.16 ms                                                                                                           | 4.04 ms: 1.28x faster                                                                                                   |
| pickle                   | 17.5 us                                                                                                           | 15.7 us: 1.12x faster                                                                                                   |
| pickle_list              | 7.49 us                                                                                                           | 6.85 us: 1.09x faster                                                                                                   |
| bench_mp_pool            | 68.3 ms                                                                                                           | 63.7 ms: 1.07x faster                                                                                                   |
| json_loads               | 38.7 us                                                                                                           | 40.7 us: 1.05x slower                                                                                                   |
| sqlite_synth             | 3.84 us                                                                                                           | 4.11 us: 1.07x slower                                                                                                   |
| xml_etree_iterparse      | 155 ms                                                                                                            | 167 ms: 1.08x slower                                                                                                    |
| json                     | 6.96 ms                                                                                                           | 7.53 ms: 1.08x slower                                                                                                   |
| unpickle_list            | 7.03 us                                                                                                           | 7.70 us: 1.10x slower                                                                                                   |
| bench_thread_pool        | 2.99 ms                                                                                                           | 3.34 ms: 1.12x slower                                                                                                   |
| scimark_fft              | 485 ms                                                                                                            | 545 ms: 1.12x slower                                                                                                    |
| unpickle                 | 18.9 us                                                                                                           | 21.4 us: 1.13x slower                                                                                                   |
| asyncio_tcp              | 901 ms                                                                                                            | 1.03 sec: 1.15x slower                                                                                                  |
| async_generators         | 586 ms                                                                                                            | 679 ms: 1.16x slower                                                                                                    |
| asyncio_tcp_ssl          | 2.73 sec                                                                                                          | 3.21 sec: 1.18x slower                                                                                                  |
| telco                    | 10.6 ms                                                                                                           | 13.1 ms: 1.24x slower                                                                                                   |
| meteor_contest           | 152 ms                                                                                                            | 191 ms: 1.25x slower                                                                                                    |
| json_dumps               | 15.5 ms                                                                                                           | 19.5 ms: 1.26x slower                                                                                                   |
| pathlib                  | 27.5 ms                                                                                                           | 34.6 ms: 1.26x slower                                                                                                   |
| docutils                 | 3.66 sec                                                                                                          | 4.60 sec: 1.26x slower                                                                                                  |
| scimark_sparse_mat_mult  | 6.63 ms                                                                                                           | 8.36 ms: 1.26x slower                                                                                                   |
| pylint                   | 462 ms                                                                                                            | 589 ms: 1.27x slower                                                                                                    |
| coverage                 | 113 ms                                                                                                            | 147 ms: 1.29x slower                                                                                                    |
| coroutines               | 31.6 ms                                                                                                           | 40.9 ms: 1.29x slower                                                                                                   |
| dulwich_log              | 99.4 ms                                                                                                           | 130 ms: 1.31x slower                                                                                                    |
| pycparser                | 1.62 sec                                                                                                          | 2.13 sec: 1.32x slower                                                                                                  |
| python_startup_no_site   | 14.0 ms                                                                                                           | 18.8 ms: 1.34x slower                                                                                                   |
| mdp                      | 3.55 sec                                                                                                          | 4.79 sec: 1.35x slower                                                                                                  |
| generators               | 39.4 ms                                                                                                           | 53.5 ms: 1.36x slower                                                                                                   |
| xml_etree_generate       | 119 ms                                                                                                            | 164 ms: 1.38x slower                                                                                                    |
| nqueens                  | 110 ms                                                                                                            | 153 ms: 1.39x slower                                                                                                    |
| spectral_norm            | 150 ms                                                                                                            | 209 ms: 1.39x slower                                                                                                    |
| fannkuch                 | 518 ms                                                                                                            | 759 ms: 1.46x slower                                                                                                    |
| bpe_tokeniser            | 5.93 sec                                                                                                          | 8.77 sec: 1.48x slower                                                                                                  |
| python_startup           | 19.9 ms                                                                                                           | 29.5 ms: 1.49x slower                                                                                                   |
| crypto_pyaes             | 98.1 ms                                                                                                           | 146 ms: 1.49x slower                                                                                                    |
| thrift                   | 1.10 ms                                                                                                           | 1.65 ms: 1.50x slower                                                                                                   |
| sympy_integrate          | 28.6 ms                                                                                                           | 43.3 ms: 1.51x slower                                                                                                   |
| deepcopy_reduce          | 3.76 us                                                                                                           | 5.74 us: 1.53x slower                                                                                                   |
| xml_etree_process        | 82.2 ms                                                                                                           | 126 ms: 1.53x slower                                                                                                    |
| sqlglot_optimize         | 75.8 ms                                                                                                           | 117 ms: 1.55x slower                                                                                                    |
| tomli_loads              | 2.62 sec                                                                                                          | 4.09 sec: 1.56x slower                                                                                                  |
| genshi_xml               | 71.6 ms                                                                                                           | 112 ms: 1.56x slower                                                                                                    |
| pyflate                  | 663 ms                                                                                                            | 1.04 sec: 1.57x slower                                                                                                  |
| 2to3                     | 410 ms                                                                                                            | 648 ms: 1.58x slower                                                                                                    |
| comprehensions           | 22.5 us                                                                                                           | 35.7 us: 1.59x slower                                                                                                   |
| regex_compile            | 180 ms                                                                                                            | 287 ms: 1.60x slower                                                                                                    |
| deepcopy                 | 352 us                                                                                                            | 564 us: 1.60x slower                                                                                                    |
| html5lib                 | 90.1 ms                                                                                                           | 147 ms: 1.63x slower                                                                                                    |
| typing_runtime_protocols | 216 us                                                                                                            | 353 us: 1.63x slower                                                                                                    |
| logging_silent           | 150 ns                                                                                                            | 246 ns: 1.64x slower                                                                                                    |
| richards                 | 64.8 ms                                                                                                           | 107 ms: 1.65x slower                                                                                                    |
| deepcopy_memo            | 41.4 us                                                                                                           | 69.9 us: 1.69x slower                                                                                                   |
| django_template          | 46.7 ms                                                                                                           | 79.0 ms: 1.69x slower                                                                                                   |
| float                    | 119 ms                                                                                                            | 201 ms: 1.69x slower                                                                                                    |
| logging_simple           | 8.87 us                                                                                                           | 15.1 us: 1.70x slower                                                                                                   |
| logging_format           | 9.73 us                                                                                                           | 16.6 us: 1.71x slower                                                                                                   |
| chaos                    | 89.2 ms                                                                                                           | 153 ms: 1.71x slower                                                                                                    |
| sqlglot_normalize        | 134 ms                                                                                                            | 232 ms: 1.73x slower                                                                                                    |
| richards_super           | 73.3 ms                                                                                                           | 128 ms: 1.75x slower                                                                                                    |
| scimark_monte_carlo      | 87.9 ms                                                                                                           | 154 ms: 1.75x slower                                                                                                    |
| genshi_text              | 28.7 ms                                                                                                           | 50.2 ms: 1.75x slower                                                                                                   |
| pprint_pformat           | 1.92 sec                                                                                                          | 3.37 sec: 1.75x slower                                                                                                  |
| pprint_safe_repr         | 936 ms                                                                                                            | 1.64 sec: 1.76x slower                                                                                                  |
| unpickle_pure_python     | 295 us                                                                                                            | 524 us: 1.78x slower                                                                                                    |
| pickle_pure_python       | 436 us                                                                                                            | 776 us: 1.78x slower                                                                                                    |
| sqlglot_transpile        | 2.34 ms                                                                                                           | 4.23 ms: 1.81x slower                                                                                                   |
| mako                     | 16.7 ms                                                                                                           | 30.4 ms: 1.81x slower                                                                                                   |
| hexiom                   | 8.93 ms                                                                                                           | 16.3 ms: 1.83x slower                                                                                                   |
| scimark_lu               | 157 ms                                                                                                            | 290 ms: 1.85x slower                                                                                                    |
| sympy_str                | 353 ms                                                                                                            | 662 ms: 1.87x slower                                                                                                    |
| sympy_expand             | 641 ms                                                                                                            | 1.21 sec: 1.89x slower                                                                                                  |
| scimark_sor              | 177 ms                                                                                                            | 334 ms: 1.89x slower                                                                                                    |
| go                       | 173 ms                                                                                                            | 336 ms: 1.95x slower                                                                                                    |
| raytrace                 | 376 ms                                                                                                            | 741 ms: 1.97x slower                                                                                                    |
| nbody                    | 123 ms                                                                                                            | 257 ms: 2.08x slower                                                                                                    |
| sqlglot_parse            | 1.79 ms                                                                                                           | 3.82 ms: 2.13x slower                                                                                                   |
| deltablue                | 4.90 ms                                                                                                           | 11.3 ms: 2.30x slower                                                                                                   |
| sympy_sum                | 205 ms                                                                                                            | 482 ms: 2.36x slower                                                                                                    |
| unpack_sequence          | 65.7 ns                                                                                                           | 209 ns: 3.18x slower                                                                                                    |
| Geometric mean           | (ref)                                                                                                             | 1.43x slower                                                                                                            |

Benchmark hidden because not significant (7): regex_effbot, xml_etree_parse, asyncio_websockets, pickle_dict, pidigits, regex_dna, regex_v8

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.40x
- 95% likely to have a slowdown of 1.37x
- 99% likely to have a slowdown of 1.35x

# Memory
- memory change: 1.18x