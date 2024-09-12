# Results vs. 3.13.0b1

- fork: python
- ref: b2afe2aae487ebf89897
- machine: linux-x86_64
- commit hash: b2afe2a
- commit date: 2024-09-12
- overall geometric mean: 1.38x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 441 ms                                                                | 721 ms: 1.63x slower                                                  |
| docutils       | 3.94 sec                                                              | 5.09 sec: 1.29x slower                                                |
| html5lib       | 92.0 ms                                                               | 141 ms: 1.53x slower                                                  |
| tornado_http   | 253 ms                                                                | 369 ms: 1.46x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.47x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|---------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg          | 1.43 sec                                                              | 1.26 sec: 1.14x faster                                                |
| async_tree_none_tg        | 526 ms                                                                | 491 ms: 1.07x faster                                                  |
| async_tree_memoization_tg | 692 ms                                                                | 649 ms: 1.07x faster                                                  |
| asyncio_websockets        | 728 ms                                                                | 792 ms: 1.09x slower                                                  |
| asyncio_tcp_ssl           | 2.83 sec                                                              | 3.12 sec: 1.10x slower                                                |
| asyncio_tcp               | 972 ms                                                                | 1.19 sec: 1.22x slower                                                |
| async_generators          | 588 ms                                                                | 726 ms: 1.24x slower                                                  |
| async_tree_none           | 523 ms                                                                | 647 ms: 1.24x slower                                                  |
| coroutines                | 29.3 ms                                                               | 44.1 ms: 1.50x slower                                                 |
| Geometric mean            | (ref)                                                                 | 1.08x slower                                                          |

Benchmark hidden because not significant (4): async_tree_memoization, async_tree_io, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 115 ms                                                                | 202 ms: 1.75x slower                                                  |
| nbody          | 126 ms                                                                | 286 ms: 2.28x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.59x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 4.63 ms                                                               | 4.89 ms: 1.06x slower                                                 |
| regex_compile  | 189 ms                                                                | 301 ms: 1.59x slower                                                  |
| Geometric mean | (ref)                                                                 | 1.14x slower                                                          |

Benchmark hidden because not significant (2): regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|----------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_list          | 7.48 us                                                               | 6.85 us: 1.09x faster                                                 |
| pickle               | 15.2 us                                                               | 14.5 us: 1.05x faster                                                 |
| xml_etree_parse      | 216 ms                                                                | 229 ms: 1.06x slower                                                  |
| unpickle             | 22.2 us                                                               | 24.2 us: 1.09x slower                                                 |
| json_loads           | 37.9 us                                                               | 42.8 us: 1.13x slower                                                 |
| unpickle_list        | 6.78 us                                                               | 7.76 us: 1.14x slower                                                 |
| json_dumps           | 13.9 ms                                                               | 18.0 ms: 1.29x slower                                                 |
| xml_etree_generate   | 120 ms                                                                | 165 ms: 1.38x slower                                                  |
| tomli_loads          | 2.84 sec                                                              | 4.26 sec: 1.50x slower                                                |
| xml_etree_process    | 82.2 ms                                                               | 128 ms: 1.56x slower                                                  |
| pickle_pure_python   | 428 us                                                                | 835 us: 1.95x slower                                                  |
| unpickle_pure_python | 285 us                                                                | 581 us: 2.04x slower                                                  |
| Geometric mean       | (ref)                                                                 | 1.25x slower                                                          |

Benchmark hidden because not significant (2): pickle_dict, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 16.0 ms                                                               | 23.8 ms: 1.49x slower                                                 |
| python_startup         | 23.5 ms                                                               | 35.1 ms: 1.49x slower                                                 |
| Geometric mean         | (ref)                                                                 | 1.49x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|-----------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 71.9 ms                                                               | 114 ms: 1.59x slower                                                  |
| django_template | 46.1 ms                                                               | 82.9 ms: 1.80x slower                                                 |
| mako            | 16.7 ms                                                               | 30.3 ms: 1.82x slower                                                 |
| genshi_text     | 31.6 ms                                                               | 61.0 ms: 1.93x slower                                                 |
| Geometric mean  | (ref)                                                                 | 1.78x slower                                                          |

All benchmarks:
===============

| Benchmark                 | bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289 | bm-20240912-linux-x86_64-python-b2afe2aae487ebf89897-3.14.0a0-b2afe2a |
|---------------------------|:---------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| telco                     | 229 ms                                                                | 14.6 ms: 15.70x faster                                                |
| create_gc_cycles          | 2.49 ms                                                               | 1.83 ms: 1.36x faster                                                 |
| gc_traversal              | 5.80 ms                                                               | 4.51 ms: 1.29x faster                                                 |
| bench_mp_pool             | 19.7 ms                                                               | 16.5 ms: 1.20x faster                                                 |
| async_tree_io_tg          | 1.43 sec                                                              | 1.26 sec: 1.14x faster                                                |
| pickle_list               | 7.48 us                                                               | 6.85 us: 1.09x faster                                                 |
| async_tree_none_tg        | 526 ms                                                                | 491 ms: 1.07x faster                                                  |
| async_tree_memoization_tg | 692 ms                                                                | 649 ms: 1.07x faster                                                  |
| pickle                    | 15.2 us                                                               | 14.5 us: 1.05x faster                                                 |
| regex_effbot              | 4.63 ms                                                               | 4.89 ms: 1.06x slower                                                 |
| xml_etree_parse           | 216 ms                                                                | 229 ms: 1.06x slower                                                  |
| asyncio_websockets        | 728 ms                                                                | 792 ms: 1.09x slower                                                  |
| unpickle                  | 22.2 us                                                               | 24.2 us: 1.09x slower                                                 |
| asyncio_tcp_ssl           | 2.83 sec                                                              | 3.12 sec: 1.10x slower                                                |
| sqlite_synth              | 3.94 us                                                               | 4.43 us: 1.13x slower                                                 |
| json_loads                | 37.9 us                                                               | 42.8 us: 1.13x slower                                                 |
| pathlib                   | 31.8 ms                                                               | 36.3 ms: 1.14x slower                                                 |
| unpickle_list             | 6.78 us                                                               | 7.76 us: 1.14x slower                                                 |
| deepcopy                  | 498 us                                                                | 595 us: 1.19x slower                                                  |
| json                      | 6.79 ms                                                               | 8.13 ms: 1.20x slower                                                 |
| asyncio_tcp               | 972 ms                                                                | 1.19 sec: 1.22x slower                                                |
| async_generators          | 588 ms                                                                | 726 ms: 1.24x slower                                                  |
| async_tree_none           | 523 ms                                                                | 647 ms: 1.24x slower                                                  |
| meteor_contest            | 156 ms                                                                | 199 ms: 1.28x slower                                                  |
| coverage                  | 121 ms                                                                | 154 ms: 1.28x slower                                                  |
| dulwich_log               | 97.5 ms                                                               | 125 ms: 1.29x slower                                                  |
| docutils                  | 3.94 sec                                                              | 5.09 sec: 1.29x slower                                                |
| mdp                       | 4.01 sec                                                              | 5.18 sec: 1.29x slower                                                |
| json_dumps                | 13.9 ms                                                               | 18.0 ms: 1.29x slower                                                 |
| deepcopy_reduce           | 4.31 us                                                               | 5.61 us: 1.30x slower                                                 |
| scimark_sparse_mat_mult   | 6.84 ms                                                               | 8.99 ms: 1.31x slower                                                 |
| pylint                    | 466 ms                                                                | 627 ms: 1.35x slower                                                  |
| scimark_fft               | 469 ms                                                                | 636 ms: 1.35x slower                                                  |
| generators                | 40.7 ms                                                               | 56.1 ms: 1.38x slower                                                 |
| xml_etree_generate        | 120 ms                                                                | 165 ms: 1.38x slower                                                  |
| deepcopy_memo             | 50.9 us                                                               | 71.2 us: 1.40x slower                                                 |
| bench_thread_pool         | 3.01 ms                                                               | 4.27 ms: 1.42x slower                                                 |
| pycparser                 | 1.71 sec                                                              | 2.43 sec: 1.42x slower                                                |
| tornado_http              | 253 ms                                                                | 369 ms: 1.46x slower                                                  |
| fannkuch                  | 535 ms                                                                | 786 ms: 1.47x slower                                                  |
| thrift                    | 1.09 ms                                                               | 1.61 ms: 1.49x slower                                                 |
| pyflate                   | 710 ms                                                                | 1.06 sec: 1.49x slower                                                |
| python_startup_no_site    | 16.0 ms                                                               | 23.8 ms: 1.49x slower                                                 |
| python_startup            | 23.5 ms                                                               | 35.1 ms: 1.49x slower                                                 |
| tomli_loads               | 2.84 sec                                                              | 4.26 sec: 1.50x slower                                                |
| coroutines                | 29.3 ms                                                               | 44.1 ms: 1.50x slower                                                 |
| crypto_pyaes              | 102 ms                                                                | 153 ms: 1.50x slower                                                  |
| typing_runtime_protocols  | 222 us                                                                | 334 us: 1.51x slower                                                  |
| html5lib                  | 92.0 ms                                                               | 141 ms: 1.53x slower                                                  |
| richards                  | 68.8 ms                                                               | 107 ms: 1.56x slower                                                  |
| sympy_integrate           | 28.7 ms                                                               | 44.8 ms: 1.56x slower                                                 |
| xml_etree_process         | 82.2 ms                                                               | 128 ms: 1.56x slower                                                  |
| genshi_xml                | 71.9 ms                                                               | 114 ms: 1.59x slower                                                  |
| regex_compile             | 189 ms                                                                | 301 ms: 1.59x slower                                                  |
| bpe_tokeniser             | 6.53 sec                                                              | 10.4 sec: 1.59x slower                                                |
| sqlglot_normalize         | 150 ms                                                                | 245 ms: 1.63x slower                                                  |
| nqueens                   | 108 ms                                                                | 177 ms: 1.63x slower                                                  |
| 2to3                      | 441 ms                                                                | 721 ms: 1.63x slower                                                  |
| pprint_safe_repr          | 991 ms                                                                | 1.70 sec: 1.72x slower                                                |
| sqlglot_optimize          | 77.9 ms                                                               | 134 ms: 1.72x slower                                                  |
| spectral_norm             | 151 ms                                                                | 260 ms: 1.72x slower                                                  |
| float                     | 115 ms                                                                | 202 ms: 1.75x slower                                                  |
| pprint_pformat            | 2.04 sec                                                              | 3.58 sec: 1.76x slower                                                |
| comprehensions            | 22.6 us                                                               | 40.4 us: 1.78x slower                                                 |
| django_template           | 46.1 ms                                                               | 82.9 ms: 1.80x slower                                                 |
| logging_simple            | 9.16 us                                                               | 16.7 us: 1.82x slower                                                 |
| mako                      | 16.7 ms                                                               | 30.3 ms: 1.82x slower                                                 |
| scimark_monte_carlo       | 89.0 ms                                                               | 164 ms: 1.84x slower                                                  |
| richards_super            | 73.5 ms                                                               | 137 ms: 1.86x slower                                                  |
| go                        | 193 ms                                                                | 363 ms: 1.88x slower                                                  |
| logging_format            | 9.36 us                                                               | 17.9 us: 1.91x slower                                                 |
| sympy_str                 | 376 ms                                                                | 721 ms: 1.91x slower                                                  |
| logging_silent            | 137 ns                                                                | 262 ns: 1.92x slower                                                  |
| genshi_text               | 31.6 ms                                                               | 61.0 ms: 1.93x slower                                                 |
| pickle_pure_python        | 428 us                                                                | 835 us: 1.95x slower                                                  |
| sqlglot_parse             | 1.92 ms                                                               | 3.75 ms: 1.96x slower                                                 |
| hexiom                    | 8.42 ms                                                               | 16.9 ms: 2.00x slower                                                 |
| scimark_lu                | 150 ms                                                                | 302 ms: 2.01x slower                                                  |
| sympy_sum                 | 226 ms                                                                | 460 ms: 2.03x slower                                                  |
| unpickle_pure_python      | 285 us                                                                | 581 us: 2.04x slower                                                  |
| sympy_expand              | 638 ms                                                                | 1.31 sec: 2.06x slower                                                |
| sqlglot_transpile         | 2.24 ms                                                               | 4.66 ms: 2.08x slower                                                 |
| scimark_sor               | 176 ms                                                                | 367 ms: 2.08x slower                                                  |
| chaos                     | 81.5 ms                                                               | 172 ms: 2.11x slower                                                  |
| raytrace                  | 351 ms                                                                | 764 ms: 2.18x slower                                                  |
| nbody                     | 126 ms                                                                | 286 ms: 2.28x slower                                                  |
| deltablue                 | 4.55 ms                                                               | 11.4 ms: 2.50x slower                                                 |
| unpack_sequence           | 54.6 ns                                                               | 220 ns: 4.02x slower                                                  |
| Geometric mean            | (ref)                                                                 | 1.38x slower                                                          |

Benchmark hidden because not significant (9): async_tree_memoization, async_tree_io, regex_v8, pickle_dict, pidigits, async_tree_cpu_io_mixed, regex_dna, async_tree_cpu_io_mixed_tg, xml_etree_iterparse
Ignored benchmarks (5) of results/bm-20240508-3.13.0b1-2268289/bm-20240508-linux-x86_64-python-2268289a47c6e3c9a220-3.13.0b1-2268289.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.35x
- 95% likely to have a slowdown of 1.32x
- 99% likely to have a slowdown of 1.27x

# Memory
- memory change: 1.15x