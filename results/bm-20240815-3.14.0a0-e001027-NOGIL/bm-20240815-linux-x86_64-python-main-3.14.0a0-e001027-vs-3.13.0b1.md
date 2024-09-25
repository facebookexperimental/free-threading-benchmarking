# Results vs. 3.13.0b1

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: e001027
- commit date: 2024-08-15
- overall geometric mean: 1.40x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.29x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| 2to3           | 441 ms                                                                | 698 ms: 1.58x slower                                  |
| docutils       | 3.94 sec                                                              | 5.02 sec: 1.27x slower                                |
| html5lib       | 92.0 ms                                                               | 149 ms: 1.62x slower                                  |
| tornado_http   | 253 ms                                                                | 429 ms: 1.70x slower                                  |
| Geometric mean | (ref)                                                                 | 1.53x slower                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|---------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| async_tree_io_tg          | 1.43 sec                                                              | 1.19 sec: 1.21x faster                                |
| async_tree_memoization_tg | 692 ms                                                                | 647 ms: 1.07x faster                                  |
| async_tree_cpu_io_mixed   | 898 ms                                                                | 974 ms: 1.08x slower                                  |
| asyncio_websockets        | 728 ms                                                                | 795 ms: 1.09x slower                                  |
| asyncio_tcp               | 972 ms                                                                | 1.12 sec: 1.15x slower                                |
| async_tree_none           | 523 ms                                                                | 614 ms: 1.18x slower                                  |
| asyncio_tcp_ssl           | 2.83 sec                                                              | 3.41 sec: 1.21x slower                                |
| async_generators          | 588 ms                                                                | 763 ms: 1.30x slower                                  |
| coroutines                | 29.3 ms                                                               | 43.6 ms: 1.49x slower                                 |
| Geometric mean            | (ref)                                                                 | 1.08x slower                                          |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_none_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pidigits       | 256 ms                                                                | 275 ms: 1.07x slower                                  |
| float          | 115 ms                                                                | 191 ms: 1.66x slower                                  |
| nbody          | 126 ms                                                                | 317 ms: 2.52x slower                                  |
| Geometric mean | (ref)                                                                 | 1.65x slower                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| regex_dna      | 284 ms                                                                | 297 ms: 1.05x slower                                  |
| regex_compile  | 189 ms                                                                | 303 ms: 1.60x slower                                  |
| Geometric mean | (ref)                                                                 | 1.14x slower                                          |

Benchmark hidden because not significant (2): regex_v8, regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|----------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| pickle_list          | 7.48 us                                                               | 6.74 us: 1.11x faster                                 |
| xml_etree_iterparse  | 163 ms                                                                | 177 ms: 1.09x slower                                  |
| xml_etree_parse      | 216 ms                                                                | 235 ms: 1.09x slower                                  |
| unpickle_list        | 6.78 us                                                               | 7.97 us: 1.18x slower                                 |
| json_loads           | 37.9 us                                                               | 48.4 us: 1.28x slower                                 |
| json_dumps           | 13.9 ms                                                               | 17.9 ms: 1.28x slower                                 |
| xml_etree_generate   | 120 ms                                                                | 180 ms: 1.50x slower                                  |
| tomli_loads          | 2.84 sec                                                              | 4.36 sec: 1.54x slower                                |
| xml_etree_process    | 82.2 ms                                                               | 133 ms: 1.62x slower                                  |
| unpickle_pure_python | 285 us                                                                | 574 us: 2.01x slower                                  |
| pickle_pure_python   | 428 us                                                                | 910 us: 2.13x slower                                  |
| Geometric mean       | (ref)                                                                 | 1.29x slower                                          |

Benchmark hidden because not significant (3): pickle_dict, pickle, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| python_startup         | 23.5 ms                                                               | 31.2 ms: 1.33x slower                                 |
| python_startup_no_site | 16.0 ms                                                               | 22.7 ms: 1.42x slower                                 |
| Geometric mean         | (ref)                                                                 | 1.37x slower                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|-----------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| genshi_xml      | 71.9 ms                                                               | 118 ms: 1.64x slower                                  |
| django_template | 46.1 ms                                                               | 80.8 ms: 1.75x slower                                 |
| mako            | 16.7 ms                                                               | 30.6 ms: 1.83x slower                                 |
| genshi_text     | 31.6 ms                                                               | 59.2 ms: 1.87x slower                                 |
| Geometric mean  | (ref)                                                                 | 1.77x slower                                          |

All benchmarks:
===============

| Benchmark                 | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240815-linux-x86_64-python-main-3.14.0a0-e001027 |
|---------------------------|:---------------------------------------------------------------------:|:-----------------------------------------------------:|
| telco                     | 229 ms                                                                | 14.1 ms: 16.20x faster                                |
| create_gc_cycles          | 2.49 ms                                                               | 1.95 ms: 1.28x faster                                 |
| async_tree_io_tg          | 1.43 sec                                                              | 1.19 sec: 1.21x faster                                |
| bench_mp_pool             | 19.7 ms                                                               | 17.0 ms: 1.16x faster                                 |
| gc_traversal              | 5.80 ms                                                               | 5.18 ms: 1.12x faster                                 |
| pickle_list               | 7.48 us                                                               | 6.74 us: 1.11x faster                                 |
| async_tree_memoization_tg | 692 ms                                                                | 647 ms: 1.07x faster                                  |
| regex_dna                 | 284 ms                                                                | 297 ms: 1.05x slower                                  |
| pidigits                  | 256 ms                                                                | 275 ms: 1.07x slower                                  |
| async_tree_cpu_io_mixed   | 898 ms                                                                | 974 ms: 1.08x slower                                  |
| xml_etree_iterparse       | 163 ms                                                                | 177 ms: 1.09x slower                                  |
| xml_etree_parse           | 216 ms                                                                | 235 ms: 1.09x slower                                  |
| asyncio_websockets        | 728 ms                                                                | 795 ms: 1.09x slower                                  |
| sqlite_synth              | 3.94 us                                                               | 4.35 us: 1.10x slower                                 |
| asyncio_tcp               | 972 ms                                                                | 1.12 sec: 1.15x slower                                |
| async_tree_none           | 523 ms                                                                | 614 ms: 1.18x slower                                  |
| unpickle_list             | 6.78 us                                                               | 7.97 us: 1.18x slower                                 |
| pathlib                   | 31.8 ms                                                               | 37.5 ms: 1.18x slower                                 |
| deepcopy                  | 498 us                                                                | 596 us: 1.20x slower                                  |
| asyncio_tcp_ssl           | 2.83 sec                                                              | 3.41 sec: 1.21x slower                                |
| pylint                    | 466 ms                                                                | 586 ms: 1.26x slower                                  |
| coverage                  | 121 ms                                                                | 152 ms: 1.26x slower                                  |
| docutils                  | 3.94 sec                                                              | 5.02 sec: 1.27x slower                                |
| json_loads                | 37.9 us                                                               | 48.4 us: 1.28x slower                                 |
| json_dumps                | 13.9 ms                                                               | 17.9 ms: 1.28x slower                                 |
| json                      | 6.79 ms                                                               | 8.77 ms: 1.29x slower                                 |
| pycparser                 | 1.71 sec                                                              | 2.21 sec: 1.29x slower                                |
| deepcopy_reduce           | 4.31 us                                                               | 5.58 us: 1.30x slower                                 |
| meteor_contest            | 156 ms                                                                | 203 ms: 1.30x slower                                  |
| async_generators          | 588 ms                                                                | 763 ms: 1.30x slower                                  |
| generators                | 40.7 ms                                                               | 53.0 ms: 1.30x slower                                 |
| mdp                       | 4.01 sec                                                              | 5.29 sec: 1.32x slower                                |
| python_startup            | 23.5 ms                                                               | 31.2 ms: 1.33x slower                                 |
| scimark_sparse_mat_mult   | 6.84 ms                                                               | 9.11 ms: 1.33x slower                                 |
| scimark_fft               | 469 ms                                                                | 642 ms: 1.37x slower                                  |
| deepcopy_memo             | 50.9 us                                                               | 70.9 us: 1.39x slower                                 |
| python_startup_no_site    | 16.0 ms                                                               | 22.7 ms: 1.42x slower                                 |
| fannkuch                  | 535 ms                                                                | 786 ms: 1.47x slower                                  |
| crypto_pyaes              | 102 ms                                                                | 150 ms: 1.47x slower                                  |
| coroutines                | 29.3 ms                                                               | 43.6 ms: 1.49x slower                                 |
| xml_etree_generate        | 120 ms                                                                | 180 ms: 1.50x slower                                  |
| tomli_loads               | 2.84 sec                                                              | 4.36 sec: 1.54x slower                                |
| bench_thread_pool         | 3.01 ms                                                               | 4.67 ms: 1.55x slower                                 |
| richards                  | 68.8 ms                                                               | 107 ms: 1.56x slower                                  |
| thrift                    | 1.09 ms                                                               | 1.70 ms: 1.56x slower                                 |
| bpe_tokeniser             | 6.53 sec                                                              | 10.3 sec: 1.58x slower                                |
| 2to3                      | 441 ms                                                                | 698 ms: 1.58x slower                                  |
| pyflate                   | 710 ms                                                                | 1.13 sec: 1.60x slower                                |
| sqlglot_normalize         | 150 ms                                                                | 240 ms: 1.60x slower                                  |
| regex_compile             | 189 ms                                                                | 303 ms: 1.60x slower                                  |
| typing_runtime_protocols  | 222 us                                                                | 355 us: 1.60x slower                                  |
| xml_etree_process         | 82.2 ms                                                               | 133 ms: 1.62x slower                                  |
| nqueens                   | 108 ms                                                                | 175 ms: 1.62x slower                                  |
| html5lib                  | 92.0 ms                                                               | 149 ms: 1.62x slower                                  |
| spectral_norm             | 151 ms                                                                | 245 ms: 1.62x slower                                  |
| logging_simple            | 9.16 us                                                               | 14.9 us: 1.63x slower                                 |
| genshi_xml                | 71.9 ms                                                               | 118 ms: 1.64x slower                                  |
| sqlglot_optimize          | 77.9 ms                                                               | 128 ms: 1.64x slower                                  |
| float                     | 115 ms                                                                | 191 ms: 1.66x slower                                  |
| sympy_integrate           | 28.7 ms                                                               | 48.4 ms: 1.68x slower                                 |
| tornado_http              | 253 ms                                                                | 429 ms: 1.70x slower                                  |
| comprehensions            | 22.6 us                                                               | 39.5 us: 1.74x slower                                 |
| django_template           | 46.1 ms                                                               | 80.8 ms: 1.75x slower                                 |
| pprint_pformat            | 2.04 sec                                                              | 3.57 sec: 1.76x slower                                |
| pprint_safe_repr          | 991 ms                                                                | 1.77 sec: 1.79x slower                                |
| mako                      | 16.7 ms                                                               | 30.6 ms: 1.83x slower                                 |
| richards_super            | 73.5 ms                                                               | 137 ms: 1.86x slower                                  |
| genshi_text               | 31.6 ms                                                               | 59.2 ms: 1.87x slower                                 |
| logging_format            | 9.36 us                                                               | 17.9 us: 1.91x slower                                 |
| scimark_monte_carlo       | 89.0 ms                                                               | 170 ms: 1.91x slower                                  |
| hexiom                    | 8.42 ms                                                               | 16.3 ms: 1.93x slower                                 |
| sympy_str                 | 376 ms                                                                | 730 ms: 1.94x slower                                  |
| logging_silent            | 137 ns                                                                | 267 ns: 1.95x slower                                  |
| sqlglot_parse             | 1.92 ms                                                               | 3.81 ms: 1.98x slower                                 |
| scimark_sor               | 176 ms                                                                | 354 ms: 2.01x slower                                  |
| unpickle_pure_python      | 285 us                                                                | 574 us: 2.01x slower                                  |
| sqlglot_transpile         | 2.24 ms                                                               | 4.53 ms: 2.02x slower                                 |
| sympy_expand              | 638 ms                                                                | 1.31 sec: 2.05x slower                                |
| pickle_pure_python        | 428 us                                                                | 910 us: 2.13x slower                                  |
| chaos                     | 81.5 ms                                                               | 175 ms: 2.15x slower                                  |
| scimark_lu                | 150 ms                                                                | 330 ms: 2.21x slower                                  |
| sympy_sum                 | 226 ms                                                                | 509 ms: 2.25x slower                                  |
| raytrace                  | 351 ms                                                                | 816 ms: 2.33x slower                                  |
| go                        | 193 ms                                                                | 452 ms: 2.34x slower                                  |
| deltablue                 | 4.55 ms                                                               | 11.3 ms: 2.48x slower                                 |
| nbody                     | 126 ms                                                                | 317 ms: 2.52x slower                                  |
| unpack_sequence           | 54.6 ns                                                               | 191 ns: 3.50x slower                                  |
| Geometric mean            | (ref)                                                                 | 1.40x slower                                          |

Benchmark hidden because not significant (9): async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_none_tg, async_tree_memoization, regex_v8, pickle_dict, regex_effbot, pickle, unpickle
Ignored benchmarks (6) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.33x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.29x

# Memory
- memory change: 1.15x