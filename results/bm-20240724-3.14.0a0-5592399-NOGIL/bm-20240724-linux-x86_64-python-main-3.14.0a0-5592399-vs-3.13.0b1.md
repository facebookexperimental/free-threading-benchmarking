# Results vs. 3.13.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 5592399
- commit date: 2024-07-24
- overall geometric mean: 1.36x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.25x slower
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 441 ms                                                                | 662 ms: 1.50x slower                                  |
| docutils       | 3.94 sec                                                              | 4.97 sec: 1.26x slower                                |
| html5lib       | 92.0 ms                                                               | 137 ms: 1.49x slower                                  |
| tornado_http   | 253 ms                                                                | 339 ms: 1.34x slower                                  |
| Geometric mean | (ref)                                                                 | 1.39x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|---------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg          | 1.43 sec                                                              | 1.17 sec: 1.23x faster                                |
| async_tree_io             | 1.39 sec                                                              | 1.27 sec: 1.09x faster                                |
| async_tree_memoization_tg | 692 ms                                                                | 652 ms: 1.06x faster                                  |
| asyncio_websockets        | 728 ms                                                                | 768 ms: 1.05x slower                                  |
| async_tree_cpu_io_mixed   | 898 ms                                                                | 959 ms: 1.07x slower                                  |
| asyncio_tcp               | 972 ms                                                                | 1.08 sec: 1.11x slower                                |
| async_tree_none           | 523 ms                                                                | 586 ms: 1.12x slower                                  |
| asyncio_tcp_ssl           | 2.83 sec                                                              | 3.42 sec: 1.21x slower                                |
| async_generators          | 588 ms                                                                | 721 ms: 1.23x slower                                  |
| coroutines                | 29.3 ms                                                               | 41.7 ms: 1.42x slower                                 |
| Geometric mean            | (ref)                                                                 | 1.05x slower                                          |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 256 ms                                                                | 241 ms: 1.06x faster                                  |
| float          | 115 ms                                                                | 211 ms: 1.83x slower                                  |
| nbody          | 126 ms                                                                | 278 ms: 2.21x slower                                  |
| Geometric mean | (ref)                                                                 | 1.56x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_compile  | 189 ms                                                                | 307 ms: 1.62x slower                                  |
| Geometric mean | (ref)                                                                 | 1.14x slower                                          |

Benchmark hidden because not significant (3): regex_dna, regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_list          | 7.48 us                                                               | 6.68 us: 1.12x faster                                 |
| pickle               | 15.2 us                                                               | 14.4 us: 1.06x faster                                 |
| unpickle_list        | 6.78 us                                                               | 7.97 us: 1.18x slower                                 |
| json_loads           | 37.9 us                                                               | 45.6 us: 1.20x slower                                 |
| json_dumps           | 13.9 ms                                                               | 19.0 ms: 1.36x slower                                 |
| xml_etree_generate   | 120 ms                                                                | 164 ms: 1.37x slower                                  |
| tomli_loads          | 2.84 sec                                                              | 4.32 sec: 1.52x slower                                |
| xml_etree_process    | 82.2 ms                                                               | 127 ms: 1.54x slower                                  |
| pickle_pure_python   | 428 us                                                                | 801 us: 1.87x slower                                  |
| unpickle_pure_python | 285 us                                                                | 547 us: 1.92x slower                                  |
| Geometric mean       | (ref)                                                                 | 1.23x slower                                          |

Benchmark hidden because not significant (4): xml_etree_parse, pickle_dict, unpickle, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup_no_site | 16.0 ms                                                               | 19.3 ms: 1.21x slower                                 |
| python_startup         | 23.5 ms                                                               | 29.1 ms: 1.24x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.22x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_text     | 31.6 ms                                                               | 53.7 ms: 1.70x slower                                 |
| genshi_xml      | 71.9 ms                                                               | 125 ms: 1.74x slower                                  |
| mako            | 16.7 ms                                                               | 31.1 ms: 1.87x slower                                 |
| django_template | 46.1 ms                                                               | 86.4 ms: 1.87x slower                                 |
| Geometric mean  | (ref)                                                                 | 1.79x slower                                          |

All benchmarks:
===============

| Benchmark                 | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240724-linux-x86_64-python-main-3.14.0a0-5592399 |
|---------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| telco                     | 229 ms                                                                | 13.8 ms: 16.54x faster                                |
| bench_mp_pool             | 19.7 ms                                                               | 14.4 ms: 1.36x faster                                 |
| create_gc_cycles          | 2.49 ms                                                               | 1.93 ms: 1.29x faster                                 |
| gc_traversal              | 5.80 ms                                                               | 4.51 ms: 1.29x faster                                 |
| async_tree_io_tg          | 1.43 sec                                                              | 1.17 sec: 1.23x faster                                |
| pickle_list               | 7.48 us                                                               | 6.68 us: 1.12x faster                                 |
| async_tree_io             | 1.39 sec                                                              | 1.27 sec: 1.09x faster                                |
| pidigits                  | 256 ms                                                                | 241 ms: 1.06x faster                                  |
| async_tree_memoization_tg | 692 ms                                                                | 652 ms: 1.06x faster                                  |
| pickle                    | 15.2 us                                                               | 14.4 us: 1.06x faster                                 |
| asyncio_websockets        | 728 ms                                                                | 768 ms: 1.05x slower                                  |
| async_tree_cpu_io_mixed   | 898 ms                                                                | 959 ms: 1.07x slower                                  |
| pathlib                   | 31.8 ms                                                               | 34.2 ms: 1.08x slower                                 |
| asyncio_tcp               | 972 ms                                                                | 1.08 sec: 1.11x slower                                |
| sqlite_synth              | 3.94 us                                                               | 4.39 us: 1.12x slower                                 |
| deepcopy                  | 498 us                                                                | 556 us: 1.12x slower                                  |
| async_tree_none           | 523 ms                                                                | 586 ms: 1.12x slower                                  |
| unpickle_list             | 6.78 us                                                               | 7.97 us: 1.18x slower                                 |
| json                      | 6.79 ms                                                               | 8.11 ms: 1.19x slower                                 |
| json_loads                | 37.9 us                                                               | 45.6 us: 1.20x slower                                 |
| python_startup_no_site    | 16.0 ms                                                               | 19.3 ms: 1.21x slower                                 |
| asyncio_tcp_ssl           | 2.83 sec                                                              | 3.42 sec: 1.21x slower                                |
| coverage                  | 121 ms                                                                | 148 ms: 1.22x slower                                  |
| async_generators          | 588 ms                                                                | 721 ms: 1.23x slower                                  |
| mdp                       | 4.01 sec                                                              | 4.96 sec: 1.24x slower                                |
| python_startup            | 23.5 ms                                                               | 29.1 ms: 1.24x slower                                 |
| docutils                  | 3.94 sec                                                              | 4.97 sec: 1.26x slower                                |
| meteor_contest            | 156 ms                                                                | 198 ms: 1.27x slower                                  |
| pylint                    | 466 ms                                                                | 592 ms: 1.27x slower                                  |
| generators                | 40.7 ms                                                               | 53.4 ms: 1.31x slower                                 |
| scimark_fft               | 469 ms                                                                | 616 ms: 1.31x slower                                  |
| pycparser                 | 1.71 sec                                                              | 2.25 sec: 1.32x slower                                |
| scimark_sparse_mat_mult   | 6.84 ms                                                               | 9.09 ms: 1.33x slower                                 |
| tornado_http              | 253 ms                                                                | 339 ms: 1.34x slower                                  |
| json_dumps                | 13.9 ms                                                               | 19.0 ms: 1.36x slower                                 |
| xml_etree_generate        | 120 ms                                                                | 164 ms: 1.37x slower                                  |
| dulwich_log               | 97.5 ms                                                               | 134 ms: 1.38x slower                                  |
| deepcopy_memo             | 50.9 us                                                               | 70.5 us: 1.39x slower                                 |
| bench_thread_pool         | 3.01 ms                                                               | 4.26 ms: 1.42x slower                                 |
| coroutines                | 29.3 ms                                                               | 41.7 ms: 1.42x slower                                 |
| fannkuch                  | 535 ms                                                                | 792 ms: 1.48x slower                                  |
| deepcopy_reduce           | 4.31 us                                                               | 6.40 us: 1.49x slower                                 |
| html5lib                  | 92.0 ms                                                               | 137 ms: 1.49x slower                                  |
| nqueens                   | 108 ms                                                                | 161 ms: 1.49x slower                                  |
| crypto_pyaes              | 102 ms                                                                | 152 ms: 1.50x slower                                  |
| 2to3                      | 441 ms                                                                | 662 ms: 1.50x slower                                  |
| sqlglot_normalize         | 150 ms                                                                | 227 ms: 1.51x slower                                  |
| tomli_loads               | 2.84 sec                                                              | 4.32 sec: 1.52x slower                                |
| sympy_integrate           | 28.7 ms                                                               | 44.1 ms: 1.54x slower                                 |
| xml_etree_process         | 82.2 ms                                                               | 127 ms: 1.54x slower                                  |
| richards                  | 68.8 ms                                                               | 107 ms: 1.55x slower                                  |
| bpe_tokeniser             | 6.53 sec                                                              | 10.2 sec: 1.57x slower                                |
| pyflate                   | 710 ms                                                                | 1.12 sec: 1.57x slower                                |
| sqlglot_optimize          | 77.9 ms                                                               | 123 ms: 1.58x slower                                  |
| typing_runtime_protocols  | 222 us                                                                | 354 us: 1.59x slower                                  |
| thrift                    | 1.09 ms                                                               | 1.74 ms: 1.61x slower                                 |
| regex_compile             | 189 ms                                                                | 307 ms: 1.62x slower                                  |
| spectral_norm             | 151 ms                                                                | 246 ms: 1.63x slower                                  |
| genshi_text               | 31.6 ms                                                               | 53.7 ms: 1.70x slower                                 |
| pprint_pformat            | 2.04 sec                                                              | 3.52 sec: 1.73x slower                                |
| richards_super            | 73.5 ms                                                               | 127 ms: 1.73x slower                                  |
| genshi_xml                | 71.9 ms                                                               | 125 ms: 1.74x slower                                  |
| comprehensions            | 22.6 us                                                               | 39.9 us: 1.76x slower                                 |
| pprint_safe_repr          | 991 ms                                                                | 1.75 sec: 1.77x slower                                |
| sympy_str                 | 376 ms                                                                | 679 ms: 1.80x slower                                  |
| logging_simple            | 9.16 us                                                               | 16.5 us: 1.81x slower                                 |
| float                     | 115 ms                                                                | 211 ms: 1.83x slower                                  |
| scimark_monte_carlo       | 89.0 ms                                                               | 164 ms: 1.85x slower                                  |
| mako                      | 16.7 ms                                                               | 31.1 ms: 1.87x slower                                 |
| django_template           | 46.1 ms                                                               | 86.4 ms: 1.87x slower                                 |
| pickle_pure_python        | 428 us                                                                | 801 us: 1.87x slower                                  |
| logging_format            | 9.36 us                                                               | 17.9 us: 1.91x slower                                 |
| hexiom                    | 8.42 ms                                                               | 16.1 ms: 1.91x slower                                 |
| unpickle_pure_python      | 285 us                                                                | 547 us: 1.92x slower                                  |
| logging_silent            | 137 ns                                                                | 266 ns: 1.95x slower                                  |
| sympy_expand              | 638 ms                                                                | 1.26 sec: 1.98x slower                                |
| scimark_sor               | 176 ms                                                                | 353 ms: 2.01x slower                                  |
| sqlglot_transpile         | 2.24 ms                                                               | 4.52 ms: 2.02x slower                                 |
| sqlglot_parse             | 1.92 ms                                                               | 4.03 ms: 2.10x slower                                 |
| scimark_lu                | 150 ms                                                                | 315 ms: 2.10x slower                                  |
| sympy_sum                 | 226 ms                                                                | 483 ms: 2.14x slower                                  |
| chaos                     | 81.5 ms                                                               | 176 ms: 2.15x slower                                  |
| go                        | 193 ms                                                                | 420 ms: 2.17x slower                                  |
| nbody                     | 126 ms                                                                | 278 ms: 2.21x slower                                  |
| raytrace                  | 351 ms                                                                | 803 ms: 2.29x slower                                  |
| deltablue                 | 4.55 ms                                                               | 11.8 ms: 2.59x slower                                 |
| unpack_sequence           | 54.6 ns                                                               | 194 ns: 3.55x slower                                  |
| Geometric mean            | (ref)                                                                 | 1.36x slower                                          |

Benchmark hidden because not significant (10): xml_etree_parse, async_tree_cpu_io_mixed_tg, async_tree_none_tg, async_tree_memoization, pickle_dict, unpickle, regex_dna, regex_v8, regex_effbot, xml_etree_iterparse
Ignored benchmarks (5) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.31x
- 95% likely to have a slowdown of 1.29x
- 99% likely to have a slowdown of 1.25x

# Memory
- memory change: 1.16x