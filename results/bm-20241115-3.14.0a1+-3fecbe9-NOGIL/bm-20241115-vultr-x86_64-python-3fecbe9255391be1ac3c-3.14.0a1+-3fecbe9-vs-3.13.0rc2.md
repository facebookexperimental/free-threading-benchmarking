# Results vs. 3.13.0rc2

- fork: python
- ref: 3fecbe9255391be1ac3c
- machine: linux-x86_64
- commit hash: 3fecbe9
- commit date: 2024-11-15
- overall geometric mean: 1.57x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.40x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 415 ms: 1.60x slower                                                   |
| docutils       | 2.62 sec                                                     | 3.39 sec: 1.29x slower                                                 |
| html5lib       | 67.0 ms                                                      | 107 ms: 1.59x slower                                                   |
| Geometric mean | (ref)                                                        | 1.49x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_tcp      | 505 ms                                                       | 583 ms: 1.15x slower                                                   |
| asyncio_tcp_ssl  | 1.51 sec                                                     | 1.82 sec: 1.20x slower                                                 |
| async_generators | 377 ms                                                       | 497 ms: 1.32x slower                                                   |
| coroutines       | 23.6 ms                                                      | 31.7 ms: 1.35x slower                                                  |
| Geometric mean   | (ref)                                                        | 1.20x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 183 ms: 1.18x faster                                                   |
| float          | 77.5 ms                                                      | 152 ms: 1.96x slower                                                   |
| nbody          | 85.1 ms                                                      | 198 ms: 2.32x slower                                                   |
| Geometric mean | (ref)                                                        | 1.57x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.98 ms: 1.03x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 24.6 ms: 1.08x slower                                                  |
| regex_compile  | 132 ms                                                       | 227 ms: 1.72x slower                                                   |
| Geometric mean | (ref)                                                        | 1.16x slower                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 133 ms: 1.03x faster                                                   |
| pickle_list          | 4.93 us                                                      | 5.11 us: 1.04x slower                                                  |
| unpickle_list        | 4.71 us                                                      | 4.94 us: 1.05x slower                                                  |
| json_loads           | 27.0 us                                                      | 28.8 us: 1.07x slower                                                  |
| pickle               | 11.3 us                                                      | 12.7 us: 1.12x slower                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 109 ms: 1.15x slower                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 114 ms: 1.34x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 15.3 ms: 1.45x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 93.6 ms: 1.58x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 3.25 sec: 1.62x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 420 us: 2.00x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 618 us: 2.10x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.28x slower                                                           |

Benchmark hidden because not significant (2): pickle_dict, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.41x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 82.4 ms: 1.69x slower                                                  |
| mako            | 11.3 ms                                                      | 20.8 ms: 1.83x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 40.7 ms: 1.89x slower                                                  |
| django_template | 34.1 ms                                                      | 65.4 ms: 1.92x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.83x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241115-vultr-x86_64-python-3fecbe9255391be1ac3c-3.14.0a1+-3fecbe9 |
|--------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 3.14 ms                                                      | 2.47 ms: 1.27x faster                                                  |
| create_gc_cycles         | 1.34 ms                                                      | 1.13 ms: 1.18x faster                                                  |
| pidigits                 | 217 ms                                                       | 183 ms: 1.18x faster                                                   |
| regex_effbot             | 3.08 ms                                                      | 2.98 ms: 1.03x faster                                                  |
| xml_etree_parse          | 136 ms                                                       | 133 ms: 1.03x faster                                                   |
| pickle_list              | 4.93 us                                                      | 5.11 us: 1.04x slower                                                  |
| unpickle_list            | 4.71 us                                                      | 4.94 us: 1.05x slower                                                  |
| json_loads               | 27.0 us                                                      | 28.8 us: 1.07x slower                                                  |
| json                     | 4.93 ms                                                      | 5.30 ms: 1.07x slower                                                  |
| regex_v8                 | 22.7 ms                                                      | 24.6 ms: 1.08x slower                                                  |
| pickle                   | 11.3 us                                                      | 12.7 us: 1.12x slower                                                  |
| sqlite_synth             | 2.21 us                                                      | 2.47 us: 1.12x slower                                                  |
| xml_etree_iterparse      | 94.9 ms                                                      | 109 ms: 1.15x slower                                                   |
| asyncio_tcp              | 505 ms                                                       | 583 ms: 1.15x slower                                                   |
| pathlib                  | 19.2 ms                                                      | 22.1 ms: 1.15x slower                                                  |
| telco                    | 7.82 ms                                                      | 9.23 ms: 1.18x slower                                                  |
| scimark_fft              | 349 ms                                                       | 416 ms: 1.19x slower                                                   |
| asyncio_tcp_ssl          | 1.51 sec                                                     | 1.82 sec: 1.20x slower                                                 |
| deepcopy                 | 355 us                                                       | 435 us: 1.22x slower                                                   |
| coverage                 | 83.0 ms                                                      | 104 ms: 1.25x slower                                                   |
| scimark_sparse_mat_mult  | 4.71 ms                                                      | 5.94 ms: 1.26x slower                                                  |
| docutils                 | 2.62 sec                                                     | 3.39 sec: 1.29x slower                                                 |
| async_generators         | 377 ms                                                       | 497 ms: 1.32x slower                                                   |
| pylint                   | 317 ms                                                       | 420 ms: 1.33x slower                                                   |
| xml_etree_generate       | 85.4 ms                                                      | 114 ms: 1.34x slower                                                   |
| coroutines               | 23.6 ms                                                      | 31.7 ms: 1.35x slower                                                  |
| meteor_contest           | 102 ms                                                       | 138 ms: 1.36x slower                                                   |
| deepcopy_memo            | 39.1 us                                                      | 53.6 us: 1.37x slower                                                  |
| mdp                      | 2.36 sec                                                     | 3.24 sec: 1.38x slower                                                 |
| bpe_tokeniser            | 4.45 sec                                                     | 6.12 sec: 1.38x slower                                                 |
| python_startup_no_site   | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                  |
| dulwich_log              | 74.8 ms                                                      | 105 ms: 1.40x slower                                                   |
| generators               | 28.8 ms                                                      | 41.1 ms: 1.43x slower                                                  |
| python_startup           | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                  |
| json_dumps               | 10.5 ms                                                      | 15.3 ms: 1.45x slower                                                  |
| spectral_norm            | 111 ms                                                       | 162 ms: 1.46x slower                                                   |
| deepcopy_reduce          | 3.11 us                                                      | 4.57 us: 1.47x slower                                                  |
| nqueens                  | 78.6 ms                                                      | 116 ms: 1.48x slower                                                   |
| fannkuch                 | 370 ms                                                       | 564 ms: 1.53x slower                                                   |
| pycparser                | 1.12 sec                                                     | 1.75 sec: 1.57x slower                                                 |
| xml_etree_process        | 59.3 ms                                                      | 93.6 ms: 1.58x slower                                                  |
| crypto_pyaes             | 67.9 ms                                                      | 108 ms: 1.59x slower                                                   |
| html5lib                 | 67.0 ms                                                      | 107 ms: 1.59x slower                                                   |
| 2to3                     | 260 ms                                                       | 415 ms: 1.60x slower                                                   |
| tomli_loads              | 2.01 sec                                                     | 3.25 sec: 1.62x slower                                                 |
| thrift                   | 778 us                                                       | 1.26 ms: 1.63x slower                                                  |
| typing_runtime_protocols | 155 us                                                       | 253 us: 1.64x slower                                                   |
| sympy_integrate          | 19.8 ms                                                      | 33.2 ms: 1.68x slower                                                  |
| genshi_xml               | 48.8 ms                                                      | 82.4 ms: 1.69x slower                                                  |
| regex_compile            | 132 ms                                                       | 227 ms: 1.72x slower                                                   |
| pyflate                  | 449 ms                                                       | 772 ms: 1.72x slower                                                   |
| sqlglot_optimize         | 52.7 ms                                                      | 91.4 ms: 1.73x slower                                                  |
| sqlglot_normalize        | 106 ms                                                       | 184 ms: 1.74x slower                                                   |
| pprint_safe_repr         | 738 ms                                                       | 1.34 sec: 1.81x slower                                                 |
| mako                     | 11.3 ms                                                      | 20.8 ms: 1.83x slower                                                  |
| pprint_pformat           | 1.50 sec                                                     | 2.75 sec: 1.83x slower                                                 |
| comprehensions           | 16.5 us                                                      | 30.8 us: 1.87x slower                                                  |
| genshi_text              | 21.5 ms                                                      | 40.7 ms: 1.89x slower                                                  |
| django_template          | 34.1 ms                                                      | 65.4 ms: 1.92x slower                                                  |
| scimark_monte_carlo      | 65.4 ms                                                      | 126 ms: 1.93x slower                                                   |
| float                    | 77.5 ms                                                      | 152 ms: 1.96x slower                                                   |
| sympy_str                | 275 ms                                                       | 541 ms: 1.97x slower                                                   |
| logging_simple           | 6.16 us                                                      | 12.3 us: 1.99x slower                                                  |
| unpickle_pure_python     | 210 us                                                       | 420 us: 2.00x slower                                                   |
| logging_format           | 6.84 us                                                      | 13.7 us: 2.00x slower                                                  |
| scimark_sor              | 134 ms                                                       | 270 ms: 2.01x slower                                                   |
| richards                 | 45.2 ms                                                      | 93.2 ms: 2.06x slower                                                  |
| logging_silent           | 103 ns                                                       | 213 ns: 2.07x slower                                                   |
| hexiom                   | 5.99 ms                                                      | 12.5 ms: 2.09x slower                                                  |
| go                       | 141 ms                                                       | 295 ms: 2.09x slower                                                   |
| pickle_pure_python       | 294 us                                                       | 618 us: 2.10x slower                                                   |
| richards_super           | 51.6 ms                                                      | 109 ms: 2.10x slower                                                   |
| chaos                    | 57.3 ms                                                      | 122 ms: 2.12x slower                                                   |
| sqlglot_transpile        | 1.56 ms                                                      | 3.35 ms: 2.15x slower                                                  |
| scimark_lu               | 113 ms                                                       | 247 ms: 2.19x slower                                                   |
| sympy_expand             | 457 ms                                                       | 1.06 sec: 2.32x slower                                                 |
| sqlglot_parse            | 1.25 ms                                                      | 2.90 ms: 2.32x slower                                                  |
| nbody                    | 85.1 ms                                                      | 198 ms: 2.32x slower                                                   |
| sympy_sum                | 156 ms                                                       | 381 ms: 2.45x slower                                                   |
| raytrace                 | 253 ms                                                       | 621 ms: 2.46x slower                                                   |
| deltablue                | 3.12 ms                                                      | 9.08 ms: 2.91x slower                                                  |
| unpack_sequence          | 44.8 ns                                                      | 144 ns: 3.22x slower                                                   |
| bench_thread_pool        | 919 us                                                       | 3.49 ms: 3.80x slower                                                  |
| bench_mp_pool            | 11.0 ms                                                      | 72.5 ms: 6.60x slower                                                  |
| Geometric mean           | (ref)                                                        | 1.57x slower                                                           |

Benchmark hidden because not significant (4): pickle_dict, asyncio_websockets, regex_dna, unpickle
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.47x
- 95% likely to have a slowdown of 1.45x
- 99% likely to have a slowdown of 1.40x

# Memory
- memory change: 1.21x