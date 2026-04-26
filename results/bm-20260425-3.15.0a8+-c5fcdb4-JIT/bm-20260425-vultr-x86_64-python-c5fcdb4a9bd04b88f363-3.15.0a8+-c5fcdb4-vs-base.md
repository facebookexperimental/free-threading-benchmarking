# Results vs. base

- fork: python
- ref: c5fcdb4a9bd04b88f363
- machine: linux-x86_64
- commit hash: c5fcdb4
- commit date: 2026-04-25
- overall geometric mean: 1.097x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260425-3.15.0a8+-c5fcdb4/bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json | results/bm-20260425-3.15.0a8+-c5fcdb4-JIT/bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| docutils       | 2.46 sec                                                                                                          | 2.56 sec: 1.04x slower                                                                                                |
| html5lib       | 59.5 ms                                                                                                           | 61.0 ms: 1.02x slower                                                                                                 |
| sphinx         | 954 ms                                                                                                            | 962 ms: 1.01x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.02x slower                                                                                                          |

Benchmark hidden because not significant (1): 2to3

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260425-3.15.0a8+-c5fcdb4/bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json | results/bm-20260425-3.15.0a8+-c5fcdb4-JIT/bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_none            | 246 ms                                                                                                            | 222 ms: 1.11x faster                                                                                                  |
| async_tree_memoization     | 313 ms                                                                                                            | 286 ms: 1.09x faster                                                                                                  |
| async_tree_io              | 584 ms                                                                                                            | 538 ms: 1.09x faster                                                                                                  |
| async_tree_memoization_tg  | 303 ms                                                                                                            | 280 ms: 1.08x faster                                                                                                  |
| async_tree_io_tg           | 594 ms                                                                                                            | 551 ms: 1.08x faster                                                                                                  |
| async_tree_none_tg         | 248 ms                                                                                                            | 234 ms: 1.06x faster                                                                                                  |
| async_tree_cpu_io_mixed    | 495 ms                                                                                                            | 472 ms: 1.05x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 490 ms                                                                                                            | 469 ms: 1.05x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                            | 545 ms: 1.00x slower                                                                                                  |
| async_generators           | 346 ms                                                                                                            | 354 ms: 1.02x slower                                                                                                  |
| coroutines                 | 23.4 ms                                                                                                           | 24.3 ms: 1.04x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                             | 1.04x faster                                                                                                          |

Benchmark hidden because not significant (2): asyncio_tcp, asyncio_tcp_ssl

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260425-3.15.0a8+-c5fcdb4/bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json | results/bm-20260425-3.15.0a8+-c5fcdb4-JIT/bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| nbody          | 93.2 ms                                                                                                           | 67.8 ms: 1.38x faster                                                                                                 |
| float          | 70.1 ms                                                                                                           | 52.7 ms: 1.33x faster                                                                                                 |
| pidigits       | 185 ms                                                                                                            | 184 ms: 1.00x faster                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.22x faster                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260425-3.15.0a8+-c5fcdb4/bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json | results/bm-20260425-3.15.0a8+-c5fcdb4-JIT/bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_dna      | 177 ms                                                                                                            | 165 ms: 1.07x faster                                                                                                  |
| regex_effbot   | 2.73 ms                                                                                                           | 2.61 ms: 1.04x faster                                                                                                 |
| regex_compile  | 125 ms                                                                                                            | 121 ms: 1.03x faster                                                                                                  |
| regex_v8       | 21.9 ms                                                                                                           | 21.3 ms: 1.03x faster                                                                                                 |
| Geometric mean | (ref)                                                                                                             | 1.04x faster                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260425-3.15.0a8+-c5fcdb4/bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json | results/bm-20260425-3.15.0a8+-c5fcdb4-JIT/bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| unpickle_pure_python | 213 us                                                                                                            | 170 us: 1.25x faster                                                                                                  |
| tomli_loads          | 1.86 sec                                                                                                          | 1.50 sec: 1.24x faster                                                                                                |
| xml_etree_process    | 61.5 ms                                                                                                           | 53.0 ms: 1.16x faster                                                                                                 |
| pickle_pure_python   | 308 us                                                                                                            | 273 us: 1.13x faster                                                                                                  |
| xml_etree_generate   | 87.1 ms                                                                                                           | 79.0 ms: 1.10x faster                                                                                                 |
| json_dumps           | 9.61 ms                                                                                                           | 8.76 ms: 1.10x faster                                                                                                 |
| xml_etree_iterparse  | 84.4 ms                                                                                                           | 81.7 ms: 1.03x faster                                                                                                 |
| json_loads           | 27.7 us                                                                                                           | 27.0 us: 1.03x faster                                                                                                 |
| xml_etree_parse      | 132 ms                                                                                                            | 129 ms: 1.02x faster                                                                                                  |
| unpickle             | 14.9 us                                                                                                           | 14.7 us: 1.02x faster                                                                                                 |
| pickle_list          | 4.99 us                                                                                                           | 4.96 us: 1.01x faster                                                                                                 |
| pickle               | 12.6 us                                                                                                           | 12.7 us: 1.01x slower                                                                                                 |
| unpickle_list        | 5.17 us                                                                                                           | 5.25 us: 1.01x slower                                                                                                 |
| pickle_dict          | 30.4 us                                                                                                           | 31.1 us: 1.02x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                             | 1.07x faster                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260425-3.15.0a8+-c5fcdb4/bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json | results/bm-20260425-3.15.0a8+-c5fcdb4-JIT/bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup_no_site | 6.82 ms                                                                                                           | 6.85 ms: 1.00x slower                                                                                                 |
| python_startup         | 12.3 ms                                                                                                           | 12.4 ms: 1.01x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                             | 1.01x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260425-3.15.0a8+-c5fcdb4/bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json | results/bm-20260425-3.15.0a8+-c5fcdb4-JIT/bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| mako            | 12.2 ms                                                                                                           | 10.1 ms: 1.20x faster                                                                                                 |
| django_template | 35.8 ms                                                                                                           | 32.4 ms: 1.11x faster                                                                                                 |
| genshi_text     | 21.0 ms                                                                                                           | 19.3 ms: 1.09x faster                                                                                                 |
| genshi_xml      | 50.2 ms                                                                                                           | 49.6 ms: 1.01x faster                                                                                                 |
| Geometric mean  | (ref)                                                                                                             | 1.10x faster                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260425-3.15.0a8+-c5fcdb4/bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json | results/bm-20260425-3.15.0a8+-c5fcdb4-JIT/bm-20260425-vultr-x86_64-python-c5fcdb4a9bd04b88f363-3.15.0a8+-c5fcdb4.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| richards_super             | 48.2 ms                                                                                                           | 21.2 ms: 2.27x faster                                                                                                 |
| richards                   | 42.2 ms                                                                                                           | 18.9 ms: 2.23x faster                                                                                                 |
| bench_mp_pool              | 273 ms                                                                                                            | 184 ms: 1.48x faster                                                                                                  |
| scimark_sor                | 109 ms                                                                                                            | 76.2 ms: 1.43x faster                                                                                                 |
| scimark_lu                 | 110 ms                                                                                                            | 76.7 ms: 1.43x faster                                                                                                 |
| spectral_norm              | 93.6 ms                                                                                                           | 67.6 ms: 1.38x faster                                                                                                 |
| nbody                      | 93.2 ms                                                                                                           | 67.8 ms: 1.38x faster                                                                                                 |
| float                      | 70.1 ms                                                                                                           | 52.7 ms: 1.33x faster                                                                                                 |
| logging_silent             | 99.3 ns                                                                                                           | 75.8 ns: 1.31x faster                                                                                                 |
| scimark_monte_carlo        | 64.4 ms                                                                                                           | 50.4 ms: 1.28x faster                                                                                                 |
| scimark_fft                | 314 ms                                                                                                            | 246 ms: 1.27x faster                                                                                                  |
| unpickle_pure_python       | 213 us                                                                                                            | 170 us: 1.25x faster                                                                                                  |
| tomli_loads                | 1.86 sec                                                                                                          | 1.50 sec: 1.24x faster                                                                                                |
| deltablue                  | 3.27 ms                                                                                                           | 2.67 ms: 1.22x faster                                                                                                 |
| deepcopy_memo              | 26.9 us                                                                                                           | 22.3 us: 1.21x faster                                                                                                 |
| mako                       | 12.2 ms                                                                                                           | 10.1 ms: 1.20x faster                                                                                                 |
| pprint_pformat             | 1.48 sec                                                                                                          | 1.24 sec: 1.19x faster                                                                                                |
| pprint_safe_repr           | 725 ms                                                                                                            | 610 ms: 1.19x faster                                                                                                  |
| pyflate                    | 415 ms                                                                                                            | 353 ms: 1.18x faster                                                                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                                                                           | 3.76 ms: 1.17x faster                                                                                                 |
| xml_etree_process          | 61.5 ms                                                                                                           | 53.0 ms: 1.16x faster                                                                                                 |
| fannkuch                   | 383 ms                                                                                                            | 332 ms: 1.15x faster                                                                                                  |
| pickle_pure_python         | 308 us                                                                                                            | 273 us: 1.13x faster                                                                                                  |
| comprehensions             | 15.9 us                                                                                                           | 14.1 us: 1.13x faster                                                                                                 |
| nqueens                    | 74.6 ms                                                                                                           | 66.6 ms: 1.12x faster                                                                                                 |
| chaos                      | 54.2 ms                                                                                                           | 48.6 ms: 1.12x faster                                                                                                 |
| async_tree_none            | 246 ms                                                                                                            | 222 ms: 1.11x faster                                                                                                  |
| django_template            | 35.8 ms                                                                                                           | 32.4 ms: 1.11x faster                                                                                                 |
| xml_etree_generate         | 87.1 ms                                                                                                           | 79.0 ms: 1.10x faster                                                                                                 |
| logging_format             | 6.45 us                                                                                                           | 5.86 us: 1.10x faster                                                                                                 |
| json_dumps                 | 9.61 ms                                                                                                           | 8.76 ms: 1.10x faster                                                                                                 |
| async_tree_memoization     | 313 ms                                                                                                            | 286 ms: 1.09x faster                                                                                                  |
| logging_simple             | 5.75 us                                                                                                           | 5.26 us: 1.09x faster                                                                                                 |
| genshi_text                | 21.0 ms                                                                                                           | 19.3 ms: 1.09x faster                                                                                                 |
| typing_runtime_protocols   | 161 us                                                                                                            | 148 us: 1.09x faster                                                                                                  |
| telco                      | 158 ms                                                                                                            | 145 ms: 1.09x faster                                                                                                  |
| async_tree_io              | 584 ms                                                                                                            | 538 ms: 1.09x faster                                                                                                  |
| async_tree_memoization_tg  | 303 ms                                                                                                            | 280 ms: 1.08x faster                                                                                                  |
| async_tree_io_tg           | 594 ms                                                                                                            | 551 ms: 1.08x faster                                                                                                  |
| subparsers                 | 9.15 ms                                                                                                           | 8.50 ms: 1.08x faster                                                                                                 |
| regex_dna                  | 177 ms                                                                                                            | 165 ms: 1.07x faster                                                                                                  |
| async_tree_none_tg         | 248 ms                                                                                                            | 234 ms: 1.06x faster                                                                                                  |
| sqlglot_v2_parse           | 1.16 ms                                                                                                           | 1.09 ms: 1.06x faster                                                                                                 |
| crypto_pyaes               | 69.8 ms                                                                                                           | 65.8 ms: 1.06x faster                                                                                                 |
| bpe_tokeniser              | 4.11 sec                                                                                                          | 3.87 sec: 1.06x faster                                                                                                |
| sqlglot_v2_transpile       | 1.46 ms                                                                                                           | 1.38 ms: 1.06x faster                                                                                                 |
| sqlglot_v2_normalize       | 102 ms                                                                                                            | 96.9 ms: 1.05x faster                                                                                                 |
| deepcopy_reduce            | 2.58 us                                                                                                           | 2.45 us: 1.05x faster                                                                                                 |
| sqlite_synth               | 2.23 us                                                                                                           | 2.12 us: 1.05x faster                                                                                                 |
| async_tree_cpu_io_mixed    | 495 ms                                                                                                            | 472 ms: 1.05x faster                                                                                                  |
| connected_components       | 386 ms                                                                                                            | 369 ms: 1.05x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 490 ms                                                                                                            | 469 ms: 1.05x faster                                                                                                  |
| json                       | 5.06 ms                                                                                                           | 4.85 ms: 1.04x faster                                                                                                 |
| sqlglot_v2_optimize        | 51.3 ms                                                                                                           | 49.1 ms: 1.04x faster                                                                                                 |
| regex_effbot               | 2.73 ms                                                                                                           | 2.61 ms: 1.04x faster                                                                                                 |
| go                         | 104 ms                                                                                                            | 99.9 ms: 1.04x faster                                                                                                 |
| meteor_contest             | 101 ms                                                                                                            | 96.6 ms: 1.04x faster                                                                                                 |
| k_core                     | 1.88 sec                                                                                                          | 1.82 sec: 1.03x faster                                                                                                |
| sympy_expand               | 472 ms                                                                                                            | 457 ms: 1.03x faster                                                                                                  |
| pathlib                    | 17.6 ms                                                                                                           | 17.0 ms: 1.03x faster                                                                                                 |
| xml_etree_iterparse        | 84.4 ms                                                                                                           | 81.7 ms: 1.03x faster                                                                                                 |
| create_gc_cycles           | 1.94 ms                                                                                                           | 1.87 ms: 1.03x faster                                                                                                 |
| bench_thread_pool          | 1.33 ms                                                                                                           | 1.29 ms: 1.03x faster                                                                                                 |
| regex_compile              | 125 ms                                                                                                            | 121 ms: 1.03x faster                                                                                                  |
| regex_v8                   | 21.9 ms                                                                                                           | 21.3 ms: 1.03x faster                                                                                                 |
| json_loads                 | 27.7 us                                                                                                           | 27.0 us: 1.03x faster                                                                                                 |
| deepcopy                   | 231 us                                                                                                            | 225 us: 1.02x faster                                                                                                  |
| xml_etree_parse            | 132 ms                                                                                                            | 129 ms: 1.02x faster                                                                                                  |
| shortest_path              | 430 ms                                                                                                            | 421 ms: 1.02x faster                                                                                                  |
| unpickle                   | 14.9 us                                                                                                           | 14.7 us: 1.02x faster                                                                                                 |
| raytrace                   | 252 ms                                                                                                            | 248 ms: 1.02x faster                                                                                                  |
| coverage                   | 82.1 ms                                                                                                           | 81.1 ms: 1.01x faster                                                                                                 |
| genshi_xml                 | 50.2 ms                                                                                                           | 49.6 ms: 1.01x faster                                                                                                 |
| pickle_list                | 4.99 us                                                                                                           | 4.96 us: 1.01x faster                                                                                                 |
| gc_traversal               | 4.36 ms                                                                                                           | 4.33 ms: 1.01x faster                                                                                                 |
| pidigits                   | 185 ms                                                                                                            | 184 ms: 1.00x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                            | 545 ms: 1.00x slower                                                                                                  |
| python_startup_no_site     | 6.82 ms                                                                                                           | 6.85 ms: 1.00x slower                                                                                                 |
| python_startup             | 12.3 ms                                                                                                           | 12.4 ms: 1.01x slower                                                                                                 |
| pickle                     | 12.6 us                                                                                                           | 12.7 us: 1.01x slower                                                                                                 |
| thrift                     | 767 us                                                                                                            | 773 us: 1.01x slower                                                                                                  |
| sphinx                     | 954 ms                                                                                                            | 962 ms: 1.01x slower                                                                                                  |
| mdp                        | 1.16 sec                                                                                                          | 1.17 sec: 1.01x slower                                                                                                |
| hexiom                     | 5.63 ms                                                                                                           | 5.69 ms: 1.01x slower                                                                                                 |
| many_optionals             | 952 us                                                                                                            | 965 us: 1.01x slower                                                                                                  |
| unpickle_list              | 5.17 us                                                                                                           | 5.25 us: 1.01x slower                                                                                                 |
| generators                 | 28.4 ms                                                                                                           | 28.9 ms: 1.02x slower                                                                                                 |
| pickle_dict                | 30.4 us                                                                                                           | 31.1 us: 1.02x slower                                                                                                 |
| async_generators           | 346 ms                                                                                                            | 354 ms: 1.02x slower                                                                                                  |
| html5lib                   | 59.5 ms                                                                                                           | 61.0 ms: 1.02x slower                                                                                                 |
| pycparser                  | 1.08 sec                                                                                                          | 1.12 sec: 1.03x slower                                                                                                |
| dulwich_log                | 67.7 ms                                                                                                           | 69.8 ms: 1.03x slower                                                                                                 |
| docutils                   | 2.46 sec                                                                                                          | 2.56 sec: 1.04x slower                                                                                                |
| coroutines                 | 23.4 ms                                                                                                           | 24.3 ms: 1.04x slower                                                                                                 |
| sympy_integrate            | 19.0 ms                                                                                                           | 19.8 ms: 1.04x slower                                                                                                 |
| sympy_str                  | 274 ms                                                                                                            | 289 ms: 1.06x slower                                                                                                  |
| sympy_sum                  | 155 ms                                                                                                            | 167 ms: 1.07x slower                                                                                                  |
| unpack_sequence            | 45.5 ns                                                                                                           | 65.5 ns: 1.44x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                             | 1.09x faster                                                                                                          |

Benchmark hidden because not significant (4): pylint, asyncio_tcp, asyncio_tcp_ssl, 2to3

- Geometric mean (including insignificant results): 1.097x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.04x
- 95% likely to have a speedup of 1.04x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.03x