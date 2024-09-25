# Results vs. 3.13.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 5f68511
- commit date: 2024-08-13
- overall geometric mean: 1.39x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.29x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 441 ms                                                                | 661 ms: 1.50x slower                                  |
| docutils       | 3.94 sec                                                              | 5.15 sec: 1.31x slower                                |
| html5lib       | 92.0 ms                                                               | 145 ms: 1.57x slower                                  |
| tornado_http   | 253 ms                                                                | 360 ms: 1.42x slower                                  |
| Geometric mean | (ref)                                                                 | 1.45x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|-------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg        | 1.43 sec                                                              | 1.17 sec: 1.23x faster                                |
| async_tree_io           | 1.39 sec                                                              | 1.30 sec: 1.07x faster                                |
| async_tree_cpu_io_mixed | 898 ms                                                                | 945 ms: 1.05x slower                                  |
| asyncio_websockets      | 728 ms                                                                | 788 ms: 1.08x slower                                  |
| async_tree_none         | 523 ms                                                                | 621 ms: 1.19x slower                                  |
| asyncio_tcp             | 972 ms                                                                | 1.17 sec: 1.20x slower                                |
| asyncio_tcp_ssl         | 2.83 sec                                                              | 3.55 sec: 1.26x slower                                |
| async_generators        | 588 ms                                                                | 744 ms: 1.27x slower                                  |
| coroutines              | 29.3 ms                                                               | 44.5 ms: 1.52x slower                                 |
| Geometric mean          | (ref)                                                                 | 1.08x slower                                          |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, async_tree_none_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 256 ms                                                                | 242 ms: 1.06x faster                                  |
| float          | 115 ms                                                                | 206 ms: 1.79x slower                                  |
| nbody          | 126 ms                                                                | 293 ms: 2.33x slower                                  |
| Geometric mean | (ref)                                                                 | 1.58x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 189 ms                                                                | 290 ms: 1.53x slower                                  |
| Geometric mean | (ref)                                                                 | 1.11x slower                                          |

Benchmark hidden because not significant (3): regex_v8, regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_list          | 7.48 us                                                               | 6.17 us: 1.21x faster                                 |
| pickle               | 15.2 us                                                               | 14.6 us: 1.04x faster                                 |
| json_loads           | 37.9 us                                                               | 43.2 us: 1.14x slower                                 |
| unpickle_list        | 6.78 us                                                               | 8.50 us: 1.25x slower                                 |
| xml_etree_generate   | 120 ms                                                                | 159 ms: 1.33x slower                                  |
| json_dumps           | 13.9 ms                                                               | 19.1 ms: 1.37x slower                                 |
| tomli_loads          | 2.84 sec                                                              | 4.26 sec: 1.50x slower                                |
| xml_etree_process    | 82.2 ms                                                               | 137 ms: 1.67x slower                                  |
| pickle_pure_python   | 428 us                                                                | 803 us: 1.88x slower                                  |
| unpickle_pure_python | 285 us                                                                | 619 us: 2.17x slower                                  |
| Geometric mean       | (ref)                                                                 | 1.25x slower                                          |

Benchmark hidden because not significant (4): pickle_dict, unpickle, xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.0 ms                                                               | 21.2 ms: 1.33x slower                                 |
| python_startup         | 23.5 ms                                                               | 31.5 ms: 1.34x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.33x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 71.9 ms                                                               | 117 ms: 1.62x slower                                  |
| genshi_text     | 31.6 ms                                                               | 55.9 ms: 1.77x slower                                 |
| django_template | 46.1 ms                                                               | 85.9 ms: 1.86x slower                                 |
| mako            | 16.7 ms                                                               | 32.0 ms: 1.92x slower                                 |
| Geometric mean  | (ref)                                                                 | 1.79x slower                                          |

All benchmarks:
===============

| Benchmark                | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240813-linux-x86_64-python-main-3.14.0a0-5f68511 |
|--------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| telco                    | 229 ms                                                                | 14.8 ms: 15.51x faster                                |
| create_gc_cycles         | 2.49 ms                                                               | 2.01 ms: 1.24x faster                                 |
| async_tree_io_tg         | 1.43 sec                                                              | 1.17 sec: 1.23x faster                                |
| pickle_list              | 7.48 us                                                               | 6.17 us: 1.21x faster                                 |
| bench_mp_pool            | 19.7 ms                                                               | 16.8 ms: 1.17x faster                                 |
| gc_traversal             | 5.80 ms                                                               | 5.42 ms: 1.07x faster                                 |
| async_tree_io            | 1.39 sec                                                              | 1.30 sec: 1.07x faster                                |
| pidigits                 | 256 ms                                                                | 242 ms: 1.06x faster                                  |
| pickle                   | 15.2 us                                                               | 14.6 us: 1.04x faster                                 |
| async_tree_cpu_io_mixed  | 898 ms                                                                | 945 ms: 1.05x slower                                  |
| asyncio_websockets       | 728 ms                                                                | 788 ms: 1.08x slower                                  |
| pathlib                  | 31.8 ms                                                               | 34.5 ms: 1.09x slower                                 |
| sqlite_synth             | 3.94 us                                                               | 4.38 us: 1.11x slower                                 |
| json_loads               | 37.9 us                                                               | 43.2 us: 1.14x slower                                 |
| deepcopy                 | 498 us                                                                | 571 us: 1.15x slower                                  |
| async_tree_none          | 523 ms                                                                | 621 ms: 1.19x slower                                  |
| asyncio_tcp              | 972 ms                                                                | 1.17 sec: 1.20x slower                                |
| coverage                 | 121 ms                                                                | 146 ms: 1.21x slower                                  |
| unpickle_list            | 6.78 us                                                               | 8.50 us: 1.25x slower                                 |
| asyncio_tcp_ssl          | 2.83 sec                                                              | 3.55 sec: 1.26x slower                                |
| json                     | 6.79 ms                                                               | 8.55 ms: 1.26x slower                                 |
| pylint                   | 466 ms                                                                | 588 ms: 1.26x slower                                  |
| async_generators         | 588 ms                                                                | 744 ms: 1.27x slower                                  |
| pycparser                | 1.71 sec                                                              | 2.18 sec: 1.28x slower                                |
| docutils                 | 3.94 sec                                                              | 5.15 sec: 1.31x slower                                |
| mdp                      | 4.01 sec                                                              | 5.24 sec: 1.31x slower                                |
| xml_etree_generate       | 120 ms                                                                | 159 ms: 1.33x slower                                  |
| python_startup_no_site   | 16.0 ms                                                               | 21.2 ms: 1.33x slower                                 |
| scimark_fft              | 469 ms                                                                | 628 ms: 1.34x slower                                  |
| python_startup           | 23.5 ms                                                               | 31.5 ms: 1.34x slower                                 |
| meteor_contest           | 156 ms                                                                | 210 ms: 1.34x slower                                  |
| json_dumps               | 13.9 ms                                                               | 19.1 ms: 1.37x slower                                 |
| scimark_sparse_mat_mult  | 6.84 ms                                                               | 9.62 ms: 1.41x slower                                 |
| tornado_http             | 253 ms                                                                | 360 ms: 1.42x slower                                  |
| deepcopy_reduce          | 4.31 us                                                               | 6.14 us: 1.42x slower                                 |
| deepcopy_memo            | 50.9 us                                                               | 72.7 us: 1.43x slower                                 |
| generators               | 40.7 ms                                                               | 58.3 ms: 1.43x slower                                 |
| 2to3                     | 441 ms                                                                | 661 ms: 1.50x slower                                  |
| tomli_loads              | 2.84 sec                                                              | 4.26 sec: 1.50x slower                                |
| fannkuch                 | 535 ms                                                                | 804 ms: 1.50x slower                                  |
| coroutines               | 29.3 ms                                                               | 44.5 ms: 1.52x slower                                 |
| regex_compile            | 189 ms                                                                | 290 ms: 1.53x slower                                  |
| sqlglot_normalize        | 150 ms                                                                | 231 ms: 1.54x slower                                  |
| crypto_pyaes             | 102 ms                                                                | 157 ms: 1.54x slower                                  |
| richards                 | 68.8 ms                                                               | 106 ms: 1.54x slower                                  |
| html5lib                 | 92.0 ms                                                               | 145 ms: 1.57x slower                                  |
| nqueens                  | 108 ms                                                                | 170 ms: 1.57x slower                                  |
| typing_runtime_protocols | 222 us                                                                | 350 us: 1.58x slower                                  |
| pyflate                  | 710 ms                                                                | 1.13 sec: 1.58x slower                                |
| thrift                   | 1.09 ms                                                               | 1.72 ms: 1.59x slower                                 |
| sqlglot_optimize         | 77.9 ms                                                               | 124 ms: 1.59x slower                                  |
| bench_thread_pool        | 3.01 ms                                                               | 4.83 ms: 1.61x slower                                 |
| bpe_tokeniser            | 6.53 sec                                                              | 10.6 sec: 1.62x slower                                |
| genshi_xml               | 71.9 ms                                                               | 117 ms: 1.62x slower                                  |
| logging_simple           | 9.16 us                                                               | 15.2 us: 1.66x slower                                 |
| xml_etree_process        | 82.2 ms                                                               | 137 ms: 1.67x slower                                  |
| spectral_norm            | 151 ms                                                                | 258 ms: 1.71x slower                                  |
| pprint_safe_repr         | 991 ms                                                                | 1.71 sec: 1.72x slower                                |
| pprint_pformat           | 2.04 sec                                                              | 3.54 sec: 1.74x slower                                |
| genshi_text              | 31.6 ms                                                               | 55.9 ms: 1.77x slower                                 |
| richards_super           | 73.5 ms                                                               | 131 ms: 1.78x slower                                  |
| comprehensions           | 22.6 us                                                               | 40.4 us: 1.79x slower                                 |
| float                    | 115 ms                                                                | 206 ms: 1.79x slower                                  |
| sympy_integrate          | 28.7 ms                                                               | 51.8 ms: 1.80x slower                                 |
| django_template          | 46.1 ms                                                               | 85.9 ms: 1.86x slower                                 |
| logging_format           | 9.36 us                                                               | 17.5 us: 1.87x slower                                 |
| pickle_pure_python       | 428 us                                                                | 803 us: 1.88x slower                                  |
| sympy_str                | 376 ms                                                                | 709 ms: 1.88x slower                                  |
| logging_silent           | 137 ns                                                                | 262 ns: 1.92x slower                                  |
| mako                     | 16.7 ms                                                               | 32.0 ms: 1.92x slower                                 |
| sqlglot_transpile        | 2.24 ms                                                               | 4.33 ms: 1.93x slower                                 |
| scimark_monte_carlo      | 89.0 ms                                                               | 174 ms: 1.96x slower                                  |
| hexiom                   | 8.42 ms                                                               | 16.8 ms: 1.99x slower                                 |
| sqlglot_parse            | 1.92 ms                                                               | 3.84 ms: 2.00x slower                                 |
| scimark_lu               | 150 ms                                                                | 305 ms: 2.04x slower                                  |
| sympy_expand             | 638 ms                                                                | 1.30 sec: 2.04x slower                                |
| scimark_sor              | 176 ms                                                                | 368 ms: 2.09x slower                                  |
| sympy_sum                | 226 ms                                                                | 479 ms: 2.12x slower                                  |
| chaos                    | 81.5 ms                                                               | 177 ms: 2.17x slower                                  |
| unpickle_pure_python     | 285 us                                                                | 619 us: 2.17x slower                                  |
| raytrace                 | 351 ms                                                                | 804 ms: 2.29x slower                                  |
| nbody                    | 126 ms                                                                | 293 ms: 2.33x slower                                  |
| go                       | 193 ms                                                                | 465 ms: 2.41x slower                                  |
| deltablue                | 4.55 ms                                                               | 12.0 ms: 2.64x slower                                 |
| unpack_sequence          | 54.6 ns                                                               | 180 ns: 3.30x slower                                  |
| Geometric mean           | (ref)                                                                 | 1.39x slower                                          |

Benchmark hidden because not significant (11): async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, pickle_dict, regex_v8, async_tree_none_tg, regex_effbot, unpickle, async_tree_memoization, regex_dna, xml_etree_parse, xml_etree_iterparse
Ignored benchmarks (6) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.33x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.29x

# Memory
- memory change: 1.15x