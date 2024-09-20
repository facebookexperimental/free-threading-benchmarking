# Results vs. 3.13.0b1

- fork: python
- ref: v3.13.0rc2
- machine: linux-x86_64
- commit hash: ec61006
- commit date: 2024-09-06
- overall geometric mean: 1.36x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x slower
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| 2to3           | 441 ms                                                                | 648 ms: 1.47x slower                                         |
| chameleon      | 9.58 ms                                                               | 18.1 ms: 1.89x slower                                        |
| docutils       | 3.94 sec                                                              | 4.93 sec: 1.25x slower                                       |
| html5lib       | 92.0 ms                                                               | 147 ms: 1.59x slower                                         |
| tornado_http   | 253 ms                                                                | 356 ms: 1.41x slower                                         |
| Geometric mean | (ref)                                                                 | 1.51x slower                                                 |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| async_tree_io_tg           | 1.43 sec                                                              | 1.17 sec: 1.23x faster                                       |
| async_tree_io              | 1.39 sec                                                              | 1.29 sec: 1.07x faster                                       |
| async_tree_memoization_tg  | 692 ms                                                                | 729 ms: 1.05x slower                                         |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 938 ms: 1.07x slower                                         |
| asyncio_websockets         | 728 ms                                                                | 780 ms: 1.07x slower                                         |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 988 ms: 1.10x slower                                         |
| async_tree_none_tg         | 526 ms                                                                | 583 ms: 1.11x slower                                         |
| asyncio_tcp_ssl            | 2.83 sec                                                              | 3.29 sec: 1.17x slower                                       |
| asyncio_tcp                | 972 ms                                                                | 1.17 sec: 1.20x slower                                       |
| async_generators           | 588 ms                                                                | 718 ms: 1.22x slower                                         |
| async_tree_none            | 523 ms                                                                | 654 ms: 1.25x slower                                         |
| coroutines                 | 29.3 ms                                                               | 42.2 ms: 1.44x slower                                        |
| Geometric mean             | (ref)                                                                 | 1.10x slower                                                 |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| float          | 115 ms                                                                | 193 ms: 1.67x slower                                         |
| nbody          | 126 ms                                                                | 267 ms: 2.13x slower                                         |
| Geometric mean | (ref)                                                                 | 1.51x slower                                                 |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| regex_dna      | 284 ms                                                                | 312 ms: 1.10x slower                                         |
| regex_effbot   | 4.63 ms                                                               | 5.22 ms: 1.13x slower                                        |
| regex_compile  | 189 ms                                                                | 271 ms: 1.43x slower                                         |
| Geometric mean | (ref)                                                                 | 1.14x slower                                                 |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| xml_etree_parse      | 216 ms                                                                | 200 ms: 1.08x faster                                         |
| pickle_dict          | 46.5 us                                                               | 43.3 us: 1.07x faster                                        |
| pickle_list          | 7.48 us                                                               | 6.97 us: 1.07x faster                                        |
| pickle               | 15.2 us                                                               | 14.4 us: 1.06x faster                                        |
| json_loads           | 37.9 us                                                               | 42.7 us: 1.13x slower                                        |
| xml_etree_generate   | 120 ms                                                                | 153 ms: 1.28x slower                                         |
| json_dumps           | 13.9 ms                                                               | 18.0 ms: 1.29x slower                                        |
| tomli_loads          | 2.84 sec                                                              | 4.19 sec: 1.48x slower                                       |
| xml_etree_process    | 82.2 ms                                                               | 126 ms: 1.54x slower                                         |
| unpickle_pure_python | 285 us                                                                | 515 us: 1.80x slower                                         |
| pickle_pure_python   | 428 us                                                                | 872 us: 2.04x slower                                         |
| Geometric mean       | (ref)                                                                 | 1.19x slower                                                 |

Benchmark hidden because not significant (3): unpickle, xml_etree_iterparse, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| python_startup_no_site | 16.0 ms                                                               | 21.9 ms: 1.37x slower                                        |
| python_startup         | 23.5 ms                                                               | 33.8 ms: 1.44x slower                                        |
| Geometric mean         | (ref)                                                                 | 1.40x slower                                                 |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|-----------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| genshi_xml      | 71.9 ms                                                               | 118 ms: 1.65x slower                                         |
| django_template | 46.1 ms                                                               | 76.1 ms: 1.65x slower                                        |
| genshi_text     | 31.6 ms                                                               | 54.3 ms: 1.72x slower                                        |
| mako            | 16.7 ms                                                               | 29.9 ms: 1.79x slower                                        |
| Geometric mean  | (ref)                                                                 | 1.70x slower                                                 |

All benchmarks:
===============

| Benchmark                  | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240906-linux-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 |
|----------------------------|:---------------------------------------------------------------------:|:------------------------------------------------------------:|
| telco                      | 229 ms                                                                | 14.3 ms: 16.06x faster                                       |
| bench_mp_pool              | 19.7 ms                                                               | 13.3 ms: 1.48x faster                                        |
| create_gc_cycles           | 2.49 ms                                                               | 1.91 ms: 1.30x faster                                        |
| gc_traversal               | 5.80 ms                                                               | 4.47 ms: 1.30x faster                                        |
| async_tree_io_tg           | 1.43 sec                                                              | 1.17 sec: 1.23x faster                                       |
| xml_etree_parse            | 216 ms                                                                | 200 ms: 1.08x faster                                         |
| pickle_dict                | 46.5 us                                                               | 43.3 us: 1.07x faster                                        |
| pickle_list                | 7.48 us                                                               | 6.97 us: 1.07x faster                                        |
| async_tree_io              | 1.39 sec                                                              | 1.29 sec: 1.07x faster                                       |
| pickle                     | 15.2 us                                                               | 14.4 us: 1.06x faster                                        |
| async_tree_memoization_tg  | 692 ms                                                                | 729 ms: 1.05x slower                                         |
| async_tree_cpu_io_mixed_tg | 878 ms                                                                | 938 ms: 1.07x slower                                         |
| asyncio_websockets         | 728 ms                                                                | 780 ms: 1.07x slower                                         |
| sqlite_synth               | 3.94 us                                                               | 4.31 us: 1.09x slower                                        |
| async_tree_cpu_io_mixed    | 898 ms                                                                | 988 ms: 1.10x slower                                         |
| regex_dna                  | 284 ms                                                                | 312 ms: 1.10x slower                                         |
| async_tree_none_tg         | 526 ms                                                                | 583 ms: 1.11x slower                                         |
| regex_effbot               | 4.63 ms                                                               | 5.22 ms: 1.13x slower                                        |
| json_loads                 | 37.9 us                                                               | 42.7 us: 1.13x slower                                        |
| pathlib                    | 31.8 ms                                                               | 36.1 ms: 1.14x slower                                        |
| asyncio_tcp_ssl            | 2.83 sec                                                              | 3.29 sec: 1.17x slower                                       |
| json                       | 6.79 ms                                                               | 7.98 ms: 1.17x slower                                        |
| asyncio_tcp                | 972 ms                                                                | 1.17 sec: 1.20x slower                                       |
| mdp                        | 4.01 sec                                                              | 4.87 sec: 1.22x slower                                       |
| async_generators           | 588 ms                                                                | 718 ms: 1.22x slower                                         |
| coverage                   | 121 ms                                                                | 148 ms: 1.23x slower                                         |
| scimark_sparse_mat_mult    | 6.84 ms                                                               | 8.40 ms: 1.23x slower                                        |
| pylint                     | 466 ms                                                                | 576 ms: 1.24x slower                                         |
| pycparser                  | 1.71 sec                                                              | 2.13 sec: 1.25x slower                                       |
| async_tree_none            | 523 ms                                                                | 654 ms: 1.25x slower                                         |
| docutils                   | 3.94 sec                                                              | 4.93 sec: 1.25x slower                                       |
| meteor_contest             | 156 ms                                                                | 198 ms: 1.27x slower                                         |
| xml_etree_generate         | 120 ms                                                                | 153 ms: 1.28x slower                                         |
| bench_thread_pool          | 3.01 ms                                                               | 3.85 ms: 1.28x slower                                        |
| scimark_fft                | 469 ms                                                                | 604 ms: 1.29x slower                                         |
| json_dumps                 | 13.9 ms                                                               | 18.0 ms: 1.29x slower                                        |
| dulwich_log                | 97.5 ms                                                               | 128 ms: 1.31x slower                                         |
| generators                 | 40.7 ms                                                               | 54.0 ms: 1.33x slower                                        |
| aiohttp                    | 2.24 ms                                                               | 2.97 ms: 1.33x slower                                        |
| gunicorn                   | 1.89 ms                                                               | 2.53 ms: 1.34x slower                                        |
| python_startup_no_site     | 16.0 ms                                                               | 21.9 ms: 1.37x slower                                        |
| fannkuch                   | 535 ms                                                                | 738 ms: 1.38x slower                                         |
| crypto_pyaes               | 102 ms                                                                | 142 ms: 1.39x slower                                         |
| nqueens                    | 108 ms                                                                | 151 ms: 1.40x slower                                         |
| tornado_http               | 253 ms                                                                | 356 ms: 1.41x slower                                         |
| regex_compile              | 189 ms                                                                | 271 ms: 1.43x slower                                         |
| python_startup             | 23.5 ms                                                               | 33.8 ms: 1.44x slower                                        |
| coroutines                 | 29.3 ms                                                               | 42.2 ms: 1.44x slower                                        |
| pyflate                    | 710 ms                                                                | 1.03 sec: 1.45x slower                                       |
| 2to3                       | 441 ms                                                                | 648 ms: 1.47x slower                                         |
| tomli_loads                | 2.84 sec                                                              | 4.19 sec: 1.48x slower                                       |
| typing_runtime_protocols   | 222 us                                                                | 329 us: 1.48x slower                                         |
| deepcopy                   | 498 us                                                                | 744 us: 1.49x slower                                         |
| sqlglot_normalize          | 150 ms                                                                | 225 ms: 1.50x slower                                         |
| sympy_integrate            | 28.7 ms                                                               | 43.4 ms: 1.51x slower                                        |
| thrift                     | 1.09 ms                                                               | 1.65 ms: 1.52x slower                                        |
| bpe_tokeniser              | 6.53 sec                                                              | 9.94 sec: 1.52x slower                                       |
| spectral_norm              | 151 ms                                                                | 231 ms: 1.53x slower                                         |
| xml_etree_process          | 82.2 ms                                                               | 126 ms: 1.54x slower                                         |
| sqlglot_optimize           | 77.9 ms                                                               | 122 ms: 1.56x slower                                         |
| richards                   | 68.8 ms                                                               | 108 ms: 1.57x slower                                         |
| html5lib                   | 92.0 ms                                                               | 147 ms: 1.59x slower                                         |
| comprehensions             | 22.6 us                                                               | 36.9 us: 1.63x slower                                        |
| deepcopy_reduce            | 4.31 us                                                               | 7.05 us: 1.64x slower                                        |
| genshi_xml                 | 71.9 ms                                                               | 118 ms: 1.65x slower                                         |
| django_template            | 46.1 ms                                                               | 76.1 ms: 1.65x slower                                        |
| deepcopy_memo              | 50.9 us                                                               | 84.2 us: 1.65x slower                                        |
| float                      | 115 ms                                                                | 193 ms: 1.67x slower                                         |
| pprint_pformat             | 2.04 sec                                                              | 3.42 sec: 1.68x slower                                       |
| genshi_text                | 31.6 ms                                                               | 54.3 ms: 1.72x slower                                        |
| pprint_safe_repr           | 991 ms                                                                | 1.74 sec: 1.75x slower                                       |
| logging_simple             | 9.16 us                                                               | 16.1 us: 1.76x slower                                        |
| sympy_str                  | 376 ms                                                                | 664 ms: 1.76x slower                                         |
| richards_super             | 73.5 ms                                                               | 130 ms: 1.77x slower                                         |
| mako                       | 16.7 ms                                                               | 29.9 ms: 1.79x slower                                        |
| unpickle_pure_python       | 285 us                                                                | 515 us: 1.80x slower                                         |
| logging_format             | 9.36 us                                                               | 17.6 us: 1.88x slower                                        |
| scimark_monte_carlo        | 89.0 ms                                                               | 167 ms: 1.88x slower                                         |
| chameleon                  | 9.58 ms                                                               | 18.1 ms: 1.89x slower                                        |
| sqlglot_transpile          | 2.24 ms                                                               | 4.25 ms: 1.90x slower                                        |
| logging_silent             | 137 ns                                                                | 262 ns: 1.91x slower                                         |
| hexiom                     | 8.42 ms                                                               | 16.3 ms: 1.94x slower                                        |
| sympy_expand               | 638 ms                                                                | 1.24 sec: 1.95x slower                                       |
| scimark_sor                | 176 ms                                                                | 345 ms: 1.96x slower                                         |
| sqlglot_parse              | 1.92 ms                                                               | 3.76 ms: 1.96x slower                                        |
| pickle_pure_python         | 428 us                                                                | 872 us: 2.04x slower                                         |
| sympy_sum                  | 226 ms                                                                | 466 ms: 2.06x slower                                         |
| chaos                      | 81.5 ms                                                               | 168 ms: 2.06x slower                                         |
| go                         | 193 ms                                                                | 401 ms: 2.08x slower                                         |
| scimark_lu                 | 150 ms                                                                | 313 ms: 2.09x slower                                         |
| raytrace                   | 351 ms                                                                | 740 ms: 2.11x slower                                         |
| flaskblogging              | 8.08 ms                                                               | 17.1 ms: 2.12x slower                                        |
| nbody                      | 126 ms                                                                | 267 ms: 2.13x slower                                         |
| deltablue                  | 4.55 ms                                                               | 10.7 ms: 2.35x slower                                        |
| unpack_sequence            | 54.6 ns                                                               | 193 ns: 3.53x slower                                         |
| Geometric mean             | (ref)                                                                 | 1.36x slower                                                 |

Benchmark hidden because not significant (6): regex_v8, unpickle, pidigits, xml_etree_iterparse, async_tree_memoization, unpickle_list
Ignored benchmarks (1) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: dask

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.30x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.24x

# Memory
- memory change: 1.14x