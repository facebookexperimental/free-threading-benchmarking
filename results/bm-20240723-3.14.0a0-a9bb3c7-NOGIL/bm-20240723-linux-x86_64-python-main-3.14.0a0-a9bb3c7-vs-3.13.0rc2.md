# Results vs. 3.13.0rc2

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: a9bb3c7
- commit date: 2024-07-23
- overall geometric mean: 1.37x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 445 ms                                                       | 661 ms: 1.49x slower                                  |
| docutils       | 4.01 sec                                                     | 4.69 sec: 1.17x slower                                |
| html5lib       | 92.6 ms                                                      | 135 ms: 1.46x slower                                  |
| tornado_http   | 251 ms                                                       | 320 ms: 1.28x slower                                  |
| Geometric mean | (ref)                                                        | 1.34x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg           | 1.40 sec                                                     | 1.15 sec: 1.22x faster                                |
| async_tree_io              | 1.39 sec                                                     | 1.25 sec: 1.11x faster                                |
| asyncio_websockets         | 766 ms                                                       | 714 ms: 1.07x faster                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 632 ms: 1.06x faster                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 806 ms: 1.06x faster                                  |
| async_tree_none_tg         | 504 ms                                                       | 479 ms: 1.05x faster                                  |
| asyncio_tcp                | 948 ms                                                       | 1.05 sec: 1.10x slower                                |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 3.12 sec: 1.12x slower                                |
| async_generators           | 567 ms                                                       | 739 ms: 1.30x slower                                  |
| coroutines                 | 30.9 ms                                                      | 40.7 ms: 1.32x slower                                 |
| Geometric mean             | (ref)                                                        | 1.02x slower                                          |

Benchmark hidden because not significant (3): async_tree_none, async_tree_memoization, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| float          | 116 ms                                                       | 199 ms: 1.72x slower                                  |
| nbody          | 119 ms                                                       | 284 ms: 2.39x slower                                  |
| Geometric mean | (ref)                                                        | 1.58x slower                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_v8       | 32.8 ms                                                      | 35.5 ms: 1.08x slower                                 |
| regex_compile  | 182 ms                                                       | 287 ms: 1.57x slower                                  |
| Geometric mean | (ref)                                                        | 1.14x slower                                          |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_dict          | 47.2 us                                                      | 40.4 us: 1.17x faster                                 |
| xml_etree_iterparse  | 177 ms                                                       | 152 ms: 1.17x faster                                  |
| xml_etree_parse      | 231 ms                                                       | 203 ms: 1.14x faster                                  |
| pickle               | 15.1 us                                                      | 14.4 us: 1.05x faster                                 |
| pickle_list          | 6.86 us                                                      | 6.56 us: 1.05x faster                                 |
| unpickle_list        | 6.68 us                                                      | 7.37 us: 1.10x slower                                 |
| json_loads           | 34.3 us                                                      | 41.9 us: 1.22x slower                                 |
| json_dumps           | 14.1 ms                                                      | 18.2 ms: 1.29x slower                                 |
| xml_etree_generate   | 122 ms                                                       | 160 ms: 1.30x slower                                  |
| xml_etree_process    | 85.9 ms                                                      | 119 ms: 1.38x slower                                  |
| tomli_loads          | 2.78 sec                                                     | 4.17 sec: 1.50x slower                                |
| unpickle_pure_python | 290 us                                                       | 526 us: 1.81x slower                                  |
| pickle_pure_python   | 416 us                                                       | 792 us: 1.90x slower                                  |
| Geometric mean       | (ref)                                                        | 1.18x slower                                          |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 15.3 ms                                                      | 18.6 ms: 1.21x slower                                 |
| python_startup         | 22.4 ms                                                      | 27.3 ms: 1.22x slower                                 |
| Geometric mean         | (ref)                                                        | 1.22x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|-----------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 72.1 ms                                                      | 117 ms: 1.62x slower                                  |
| genshi_text     | 31.7 ms                                                      | 54.8 ms: 1.73x slower                                 |
| django_template | 44.3 ms                                                      | 80.7 ms: 1.82x slower                                 |
| mako            | 15.9 ms                                                      | 29.7 ms: 1.86x slower                                 |
| Geometric mean  | (ref)                                                        | 1.76x slower                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20240723-linux-x86_64-python-main-3.14.0a0-a9bb3c7 |
|----------------------------|:------------------------------------------------------------:|:-----------------------------------------------------:|
| bench_mp_pool              | 18.7 ms                                                      | 12.0 ms: 1.56x faster                                 |
| create_gc_cycles           | 2.41 ms                                                      | 1.77 ms: 1.36x faster                                 |
| gc_traversal               | 5.70 ms                                                      | 4.22 ms: 1.35x faster                                 |
| async_tree_io_tg           | 1.40 sec                                                     | 1.15 sec: 1.22x faster                                |
| pickle_dict                | 47.2 us                                                      | 40.4 us: 1.17x faster                                 |
| xml_etree_iterparse        | 177 ms                                                       | 152 ms: 1.17x faster                                  |
| xml_etree_parse            | 231 ms                                                       | 203 ms: 1.14x faster                                  |
| async_tree_io              | 1.39 sec                                                     | 1.25 sec: 1.11x faster                                |
| asyncio_websockets         | 766 ms                                                       | 714 ms: 1.07x faster                                  |
| async_tree_memoization_tg  | 670 ms                                                       | 632 ms: 1.06x faster                                  |
| async_tree_cpu_io_mixed_tg | 852 ms                                                       | 806 ms: 1.06x faster                                  |
| pickle                     | 15.1 us                                                      | 14.4 us: 1.05x faster                                 |
| async_tree_none_tg         | 504 ms                                                       | 479 ms: 1.05x faster                                  |
| pickle_list                | 6.86 us                                                      | 6.56 us: 1.05x faster                                 |
| pathlib                    | 29.9 ms                                                      | 31.7 ms: 1.06x slower                                 |
| regex_v8                   | 32.8 ms                                                      | 35.5 ms: 1.08x slower                                 |
| sqlite_synth               | 3.99 us                                                      | 4.31 us: 1.08x slower                                 |
| telco                      | 12.2 ms                                                      | 13.2 ms: 1.08x slower                                 |
| asyncio_tcp                | 948 ms                                                       | 1.05 sec: 1.10x slower                                |
| unpickle_list              | 6.68 us                                                      | 7.37 us: 1.10x slower                                 |
| asyncio_tcp_ssl            | 2.77 sec                                                     | 3.12 sec: 1.12x slower                                |
| docutils                   | 4.01 sec                                                     | 4.69 sec: 1.17x slower                                |
| pylint                     | 470 ms                                                       | 554 ms: 1.18x slower                                  |
| python_startup_no_site     | 15.3 ms                                                      | 18.6 ms: 1.21x slower                                 |
| python_startup             | 22.4 ms                                                      | 27.3 ms: 1.22x slower                                 |
| deepcopy                   | 498 us                                                       | 608 us: 1.22x slower                                  |
| json_loads                 | 34.3 us                                                      | 41.9 us: 1.22x slower                                 |
| json                       | 6.51 ms                                                      | 8.04 ms: 1.23x slower                                 |
| tornado_http               | 251 ms                                                       | 320 ms: 1.28x slower                                  |
| json_dumps                 | 14.1 ms                                                      | 18.2 ms: 1.29x slower                                 |
| bench_thread_pool          | 2.89 ms                                                      | 3.73 ms: 1.29x slower                                 |
| scimark_fft                | 473 ms                                                       | 616 ms: 1.30x slower                                  |
| meteor_contest             | 150 ms                                                       | 196 ms: 1.30x slower                                  |
| async_generators           | 567 ms                                                       | 739 ms: 1.30x slower                                  |
| xml_etree_generate         | 122 ms                                                       | 160 ms: 1.30x slower                                  |
| coroutines                 | 30.9 ms                                                      | 40.7 ms: 1.32x slower                                 |
| generators                 | 40.0 ms                                                      | 52.7 ms: 1.32x slower                                 |
| mdp                        | 3.80 sec                                                     | 5.07 sec: 1.34x slower                                |
| scimark_sparse_mat_mult    | 6.76 ms                                                      | 9.03 ms: 1.34x slower                                 |
| pycparser                  | 1.57 sec                                                     | 2.15 sec: 1.37x slower                                |
| nqueens                    | 112 ms                                                       | 153 ms: 1.37x slower                                  |
| deepcopy_memo              | 50.1 us                                                      | 69.3 us: 1.38x slower                                 |
| xml_etree_process          | 85.9 ms                                                      | 119 ms: 1.38x slower                                  |
| coverage                   | 107 ms                                                       | 149 ms: 1.39x slower                                  |
| sympy_integrate            | 30.2 ms                                                      | 43.4 ms: 1.43x slower                                 |
| dulwich_log                | 93.7 ms                                                      | 135 ms: 1.44x slower                                  |
| fannkuch                   | 547 ms                                                       | 794 ms: 1.45x slower                                  |
| html5lib                   | 92.6 ms                                                      | 135 ms: 1.46x slower                                  |
| deepcopy_reduce            | 4.10 us                                                      | 6.01 us: 1.47x slower                                 |
| 2to3                       | 445 ms                                                       | 661 ms: 1.49x slower                                  |
| typing_runtime_protocols   | 226 us                                                       | 337 us: 1.49x slower                                  |
| crypto_pyaes               | 100 ms                                                       | 150 ms: 1.49x slower                                  |
| tomli_loads                | 2.78 sec                                                     | 4.17 sec: 1.50x slower                                |
| richards                   | 65.5 ms                                                      | 99.0 ms: 1.51x slower                                 |
| bpe_tokeniser              | 6.28 sec                                                     | 9.73 sec: 1.55x slower                                |
| thrift                     | 1.10 ms                                                      | 1.71 ms: 1.56x slower                                 |
| spectral_norm              | 157 ms                                                       | 245 ms: 1.56x slower                                  |
| regex_compile              | 182 ms                                                       | 287 ms: 1.57x slower                                  |
| sqlglot_optimize           | 74.7 ms                                                      | 121 ms: 1.61x slower                                  |
| genshi_xml                 | 72.1 ms                                                      | 117 ms: 1.62x slower                                  |
| pyflate                    | 664 ms                                                       | 1.08 sec: 1.63x slower                                |
| richards_super             | 73.2 ms                                                      | 122 ms: 1.67x slower                                  |
| sqlglot_normalize          | 140 ms                                                       | 235 ms: 1.68x slower                                  |
| float                      | 116 ms                                                       | 199 ms: 1.72x slower                                  |
| pprint_safe_repr           | 987 ms                                                       | 1.71 sec: 1.73x slower                                |
| genshi_text                | 31.7 ms                                                      | 54.8 ms: 1.73x slower                                 |
| sympy_str                  | 379 ms                                                       | 664 ms: 1.75x slower                                  |
| pprint_pformat             | 1.94 sec                                                     | 3.50 sec: 1.80x slower                                |
| unpickle_pure_python       | 290 us                                                       | 526 us: 1.81x slower                                  |
| logging_simple             | 8.56 us                                                      | 15.5 us: 1.81x slower                                 |
| scimark_monte_carlo        | 90.6 ms                                                      | 165 ms: 1.82x slower                                  |
| logging_format             | 9.24 us                                                      | 16.8 us: 1.82x slower                                 |
| django_template            | 44.3 ms                                                      | 80.7 ms: 1.82x slower                                 |
| logging_silent             | 130 ns                                                       | 240 ns: 1.85x slower                                  |
| mako                       | 15.9 ms                                                      | 29.7 ms: 1.86x slower                                 |
| scimark_sor                | 179 ms                                                       | 337 ms: 1.89x slower                                  |
| comprehensions             | 22.2 us                                                      | 42.1 us: 1.89x slower                                 |
| pickle_pure_python         | 416 us                                                       | 792 us: 1.90x slower                                  |
| sqlglot_transpile          | 2.20 ms                                                      | 4.33 ms: 1.97x slower                                 |
| chaos                      | 83.6 ms                                                      | 165 ms: 1.97x slower                                  |
| hexiom                     | 8.11 ms                                                      | 16.5 ms: 2.03x slower                                 |
| go                         | 191 ms                                                       | 395 ms: 2.07x slower                                  |
| sympy_expand               | 601 ms                                                       | 1.27 sec: 2.11x slower                                |
| sqlglot_parse              | 1.76 ms                                                      | 3.77 ms: 2.15x slower                                 |
| sympy_sum                  | 210 ms                                                       | 460 ms: 2.19x slower                                  |
| scimark_lu                 | 146 ms                                                       | 326 ms: 2.23x slower                                  |
| raytrace                   | 344 ms                                                       | 784 ms: 2.28x slower                                  |
| nbody                      | 119 ms                                                       | 284 ms: 2.39x slower                                  |
| deltablue                  | 4.44 ms                                                      | 10.8 ms: 2.44x slower                                 |
| unpack_sequence            | 74.3 ns                                                      | 191 ns: 2.56x slower                                  |
| Geometric mean             | (ref)                                                        | 1.37x slower                                          |

Benchmark hidden because not significant (7): pidigits, regex_effbot, async_tree_none, regex_dna, async_tree_memoization, unpickle, async_tree_cpu_io_mixed
Ignored benchmarks (5) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.33x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.27x

# Memory
- memory change: 1.15x