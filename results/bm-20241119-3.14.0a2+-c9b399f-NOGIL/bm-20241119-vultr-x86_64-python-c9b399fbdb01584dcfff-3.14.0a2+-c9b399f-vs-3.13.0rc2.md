# Results vs. 3.13.0rc2

- fork: python
- ref: c9b399fbdb01584dcfff
- machine: linux-x86_64
- commit hash: c9b399f
- commit date: 2024-11-19
- overall geometric mean: 1.56x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.40x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 414 ms: 1.59x slower                                                   |
| docutils       | 2.62 sec                                                     | 3.37 sec: 1.29x slower                                                 |
| html5lib       | 67.0 ms                                                      | 106 ms: 1.59x slower                                                   |
| Geometric mean | (ref)                                                        | 1.48x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_tcp      | 505 ms                                                       | 584 ms: 1.16x slower                                                   |
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.83 sec: 1.21x slower                                                 |
| coroutines       | 23.6 ms                                                      | 31.1 ms: 1.32x slower                                                  |
| async_generators | 377 ms                                                       | 504 ms: 1.33x slower                                                   |
| Geometric mean   | (ref)                                                        | 1.20x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 187 ms: 1.16x faster                                                   |
| float          | 77.5 ms                                                      | 151 ms: 1.95x slower                                                   |
| nbody          | 85.1 ms                                                      | 199 ms: 2.34x slower                                                   |
| Geometric mean | (ref)                                                        | 1.58x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.86 ms: 1.08x faster                                                  |
| regex_dna      | 180 ms                                                       | 187 ms: 1.04x slower                                                   |
| regex_v8       | 22.7 ms                                                      | 25.0 ms: 1.10x slower                                                  |
| regex_compile  | 132 ms                                                       | 228 ms: 1.73x slower                                                   |
| Geometric mean | (ref)                                                        | 1.16x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_dict          | 32.5 us                                                      | 31.7 us: 1.03x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 133 ms: 1.03x faster                                                   |
| unpickle             | 14.3 us                                                      | 15.0 us: 1.04x slower                                                  |
| pickle_list          | 4.93 us                                                      | 5.15 us: 1.04x slower                                                  |
| pickle               | 11.3 us                                                      | 12.0 us: 1.06x slower                                                  |
| json_loads           | 27.0 us                                                      | 28.5 us: 1.06x slower                                                  |
| unpickle_list        | 4.71 us                                                      | 5.09 us: 1.08x slower                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 110 ms: 1.15x slower                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 114 ms: 1.33x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 15.4 ms: 1.46x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 93.8 ms: 1.58x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 3.21 sec: 1.60x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 427 us: 2.03x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 623 us: 2.12x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.28x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.41x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 82.8 ms: 1.70x slower                                                  |
| mako            | 11.3 ms                                                      | 21.0 ms: 1.85x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 40.8 ms: 1.89x slower                                                  |
| django_template | 34.1 ms                                                      | 65.2 ms: 1.91x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.84x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 3.14 ms                                                      | 2.39 ms: 1.32x faster                                                  |
| create_gc_cycles         | 1.34 ms                                                      | 1.14 ms: 1.18x faster                                                  |
| pidigits                 | 217 ms                                                       | 187 ms: 1.16x faster                                                   |
| regex_effbot             | 3.08 ms                                                      | 2.86 ms: 1.08x faster                                                  |
| pickle_dict              | 32.5 us                                                      | 31.7 us: 1.03x faster                                                  |
| xml_etree_parse          | 136 ms                                                       | 133 ms: 1.03x faster                                                   |
| regex_dna                | 180 ms                                                       | 187 ms: 1.04x slower                                                   |
| unpickle                 | 14.3 us                                                      | 15.0 us: 1.04x slower                                                  |
| pickle_list              | 4.93 us                                                      | 5.15 us: 1.04x slower                                                  |
| pickle                   | 11.3 us                                                      | 12.0 us: 1.06x slower                                                  |
| json_loads               | 27.0 us                                                      | 28.5 us: 1.06x slower                                                  |
| json                     | 4.93 ms                                                      | 5.30 ms: 1.08x slower                                                  |
| unpickle_list            | 4.71 us                                                      | 5.09 us: 1.08x slower                                                  |
| regex_v8                 | 22.7 ms                                                      | 25.0 ms: 1.10x slower                                                  |
| sqlite_synth             | 2.21 us                                                      | 2.45 us: 1.11x slower                                                  |
| pathlib                  | 19.2 ms                                                      | 22.1 ms: 1.15x slower                                                  |
| xml_etree_iterparse      | 94.9 ms                                                      | 110 ms: 1.15x slower                                                   |
| asyncio_tcp              | 505 ms                                                       | 584 ms: 1.16x slower                                                   |
| scimark_fft              | 349 ms                                                       | 408 ms: 1.17x slower                                                   |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.83 sec: 1.21x slower                                                 |
| telco                    | 7.82 ms                                                      | 9.58 ms: 1.22x slower                                                  |
| deepcopy                 | 355 us                                                       | 436 us: 1.23x slower                                                   |
| coverage                 | 83.0 ms                                                      | 102 ms: 1.23x slower                                                   |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 5.93 ms: 1.26x slower                                                  |
| docutils                 | 2.62 sec                                                     | 3.37 sec: 1.29x slower                                                 |
| mdp                      | 2.36 sec                                                     | 3.06 sec: 1.30x slower                                                 |
| coroutines               | 23.6 ms                                                      | 31.1 ms: 1.32x slower                                                  |
| xml_etree_generate       | 85.4 ms                                                      | 114 ms: 1.33x slower                                                   |
| pylint                   | 317 ms                                                       | 422 ms: 1.33x slower                                                   |
| async_generators         | 377 ms                                                       | 504 ms: 1.33x slower                                                   |
| meteor_contest           | 102 ms                                                       | 140 ms: 1.38x slower                                                   |
| python_startup_no_site   | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                  |
| deepcopy_memo            | 39.1 us                                                      | 54.2 us: 1.39x slower                                                  |
| bpe_tokeniser            | 4.45 sec                                                     | 6.17 sec: 1.39x slower                                                 |
| dulwich_log              | 74.8 ms                                                      | 104 ms: 1.39x slower                                                   |
| spectral_norm            | 111 ms                                                       | 158 ms: 1.43x slower                                                   |
| python_startup           | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                  |
| generators               | 28.8 ms                                                      | 41.5 ms: 1.44x slower                                                  |
| json_dumps               | 10.5 ms                                                      | 15.4 ms: 1.46x slower                                                  |
| deepcopy_reduce          | 3.11 us                                                      | 4.55 us: 1.46x slower                                                  |
| nqueens                  | 78.6 ms                                                      | 116 ms: 1.47x slower                                                   |
| fannkuch                 | 370 ms                                                       | 563 ms: 1.52x slower                                                   |
| pycparser                | 1.12 sec                                                     | 1.71 sec: 1.53x slower                                                 |
| xml_etree_process        | 59.3 ms                                                      | 93.8 ms: 1.58x slower                                                  |
| html5lib                 | 67.0 ms                                                      | 106 ms: 1.59x slower                                                   |
| crypto_pyaes             | 67.9 ms                                                      | 108 ms: 1.59x slower                                                   |
| 2to3                     | 260 ms                                                       | 414 ms: 1.59x slower                                                   |
| tomli_loads              | 2.01 sec                                                     | 3.21 sec: 1.60x slower                                                 |
| typing_runtime_protocols | 155 us                                                       | 253 us: 1.64x slower                                                   |
| thrift                   | 778 us                                                       | 1.29 ms: 1.65x slower                                                  |
| sympy_integrate          | 19.8 ms                                                      | 33.2 ms: 1.67x slower                                                  |
| genshi_xml               | 48.8 ms                                                      | 82.8 ms: 1.70x slower                                                  |
| sqlglot_normalize        | 106 ms                                                       | 182 ms: 1.72x slower                                                   |
| regex_compile            | 132 ms                                                       | 228 ms: 1.73x slower                                                   |
| sqlglot_optimize         | 52.7 ms                                                      | 91.2 ms: 1.73x slower                                                  |
| pyflate                  | 449 ms                                                       | 778 ms: 1.73x slower                                                   |
| pprint_safe_repr         | 738 ms                                                       | 1.32 sec: 1.80x slower                                                 |
| pprint_pformat           | 1.50 sec                                                     | 2.76 sec: 1.84x slower                                                 |
| mako                     | 11.3 ms                                                      | 21.0 ms: 1.85x slower                                                  |
| comprehensions           | 16.5 us                                                      | 30.9 us: 1.88x slower                                                  |
| genshi_text              | 21.5 ms                                                      | 40.8 ms: 1.89x slower                                                  |
| django_template          | 34.1 ms                                                      | 65.2 ms: 1.91x slower                                                  |
| scimark_monte_carlo      | 65.4 ms                                                      | 125 ms: 1.92x slower                                                   |
| float                    | 77.5 ms                                                      | 151 ms: 1.95x slower                                                   |
| sympy_str                | 275 ms                                                       | 541 ms: 1.97x slower                                                   |
| logging_simple           | 6.16 us                                                      | 12.1 us: 1.97x slower                                                  |
| richards                 | 45.2 ms                                                      | 89.7 ms: 1.98x slower                                                  |
| logging_format           | 6.84 us                                                      | 13.6 us: 1.99x slower                                                  |
| scimark_sor              | 134 ms                                                       | 271 ms: 2.02x slower                                                   |
| unpickle_pure_python     | 210 us                                                       | 427 us: 2.03x slower                                                   |
| logging_silent           | 103 ns                                                       | 213 ns: 2.07x slower                                                   |
| hexiom                   | 5.99 ms                                                      | 12.5 ms: 2.08x slower                                                  |
| richards_super           | 51.6 ms                                                      | 109 ms: 2.10x slower                                                   |
| go                       | 141 ms                                                       | 297 ms: 2.11x slower                                                   |
| pickle_pure_python       | 294 us                                                       | 623 us: 2.12x slower                                                   |
| sqlglot_transpile        | 1.56 ms                                                      | 3.30 ms: 2.12x slower                                                  |
| chaos                    | 57.3 ms                                                      | 122 ms: 2.13x slower                                                   |
| scimark_lu               | 113 ms                                                       | 245 ms: 2.17x slower                                                   |
| sqlglot_parse            | 1.25 ms                                                      | 2.85 ms: 2.28x slower                                                  |
| sympy_expand             | 457 ms                                                       | 1.06 sec: 2.31x slower                                                 |
| nbody                    | 85.1 ms                                                      | 199 ms: 2.34x slower                                                   |
| sympy_sum                | 156 ms                                                       | 381 ms: 2.45x slower                                                   |
| raytrace                 | 253 ms                                                       | 631 ms: 2.50x slower                                                   |
| deltablue                | 3.12 ms                                                      | 9.02 ms: 2.89x slower                                                  |
| unpack_sequence          | 44.8 ns                                                      | 147 ns: 3.29x slower                                                   |
| bench_thread_pool        | 919 us                                                       | 3.49 ms: 3.80x slower                                                  |
| bench_mp_pool            | 11.0 ms                                                      | 72.6 ms: 6.60x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.56x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.47x
- 95% likely to have a slowdown of 1.45x
- 99% likely to have a slowdown of 1.40x

# Memory
- memory change: 1.21x