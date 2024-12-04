# Results vs. 3.13.0rc2

- fork: mpage
- ref: measure_gc_changes
- machine: linux-x86_64
- commit hash: 0f5d11c
- commit date: 2024-12-04
- overall geometric mean: 1.279x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.23x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 376 ms: 1.45x slower                                                |
| docutils       | 2.62 sec                                                     | 3.19 sec: 1.22x slower                                              |
| html5lib       | 67.0 ms                                                      | 98.9 ms: 1.48x slower                                               |
| Geometric mean | (ref)                                                        | 1.38x slower                                                        |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|---------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| async_tree_io_tg          | 913 ms                                                       | 865 ms: 1.06x faster                                                |
| async_tree_memoization    | 461 ms                                                       | 493 ms: 1.07x slower                                                |
| async_tree_none_tg        | 336 ms                                                       | 366 ms: 1.09x slower                                                |
| async_tree_memoization_tg | 414 ms                                                       | 461 ms: 1.11x slower                                                |
| async_tree_none           | 354 ms                                                       | 400 ms: 1.13x slower                                                |
| coroutines                | 23.6 ms                                                      | 28.4 ms: 1.21x slower                                               |
| async_generators          | 377 ms                                                       | 467 ms: 1.24x slower                                                |
| Geometric mean            | (ref)                                                        | 1.07x slower                                                        |

Benchmark hidden because not significant (4): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, asyncio_websockets, async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.17x faster                                                |
| nbody          | 85.1 ms                                                      | 128 ms: 1.50x slower                                                |
| float          | 77.5 ms                                                      | 143 ms: 1.85x slower                                                |
| Geometric mean | (ref)                                                        | 1.33x slower                                                        |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.67 ms: 1.15x faster                                               |
| regex_dna      | 180 ms                                                       | 175 ms: 1.03x faster                                                |
| regex_v8       | 22.7 ms                                                      | 23.8 ms: 1.05x slower                                               |
| regex_compile  | 132 ms                                                       | 191 ms: 1.45x slower                                                |
| Geometric mean | (ref)                                                        | 1.06x slower                                                        |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|----------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                |
| json_loads           | 27.0 us                                                      | 28.1 us: 1.04x slower                                               |
| xml_etree_generate   | 85.4 ms                                                      | 103 ms: 1.20x slower                                                |
| json_dumps           | 10.5 ms                                                      | 14.5 ms: 1.37x slower                                               |
| xml_etree_process    | 59.3 ms                                                      | 82.3 ms: 1.39x slower                                               |
| tomli_loads          | 2.01 sec                                                     | 2.81 sec: 1.40x slower                                              |
| unpickle_pure_python | 210 us                                                       | 379 us: 1.81x slower                                                |
| pickle_pure_python   | 294 us                                                       | 556 us: 1.89x slower                                                |
| Geometric mean       | (ref)                                                        | 1.30x slower                                                        |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                               |
| python_startup         | 11.0 ms                                                      | 17.4 ms: 1.59x slower                                               |
| Geometric mean         | (ref)                                                        | 1.48x slower                                                        |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|-----------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 66.7 ms: 1.37x slower                                               |
| genshi_text     | 21.5 ms                                                      | 33.5 ms: 1.56x slower                                               |
| django_template | 34.1 ms                                                      | 55.2 ms: 1.62x slower                                               |
| mako            | 11.3 ms                                                      | 19.6 ms: 1.73x slower                                               |
| Geometric mean  | (ref)                                                        | 1.56x slower                                                        |

All benchmarks:
===============

| Benchmark                 | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c |
|---------------------------|:------------------------------------------------------------:|:-------------------------------------------------------------------:|
| pidigits                  | 217 ms                                                       | 184 ms: 1.17x faster                                                |
| regex_effbot              | 3.08 ms                                                      | 2.67 ms: 1.15x faster                                               |
| async_tree_io_tg          | 913 ms                                                       | 865 ms: 1.06x faster                                                |
| xml_etree_parse           | 136 ms                                                       | 130 ms: 1.05x faster                                                |
| regex_dna                 | 180 ms                                                       | 175 ms: 1.03x faster                                                |
| deepcopy                  | 355 us                                                       | 353 us: 1.01x faster                                                |
| json                      | 4.93 ms                                                      | 5.06 ms: 1.03x slower                                               |
| json_loads                | 27.0 us                                                      | 28.1 us: 1.04x slower                                               |
| sqlite_synth              | 2.21 us                                                      | 2.30 us: 1.04x slower                                               |
| regex_v8                  | 22.7 ms                                                      | 23.8 ms: 1.05x slower                                               |
| gc_traversal              | 3.14 ms                                                      | 3.30 ms: 1.05x slower                                               |
| async_tree_memoization    | 461 ms                                                       | 493 ms: 1.07x slower                                                |
| pathlib                   | 19.2 ms                                                      | 20.7 ms: 1.08x slower                                               |
| async_tree_none_tg        | 336 ms                                                       | 366 ms: 1.09x slower                                                |
| async_tree_memoization_tg | 414 ms                                                       | 461 ms: 1.11x slower                                                |
| telco                     | 7.82 ms                                                      | 8.79 ms: 1.12x slower                                               |
| async_tree_none           | 354 ms                                                       | 400 ms: 1.13x slower                                                |
| scimark_fft               | 349 ms                                                       | 401 ms: 1.15x slower                                                |
| deepcopy_memo             | 39.1 us                                                      | 44.9 us: 1.15x slower                                               |
| deepcopy_reduce           | 3.11 us                                                      | 3.74 us: 1.20x slower                                               |
| xml_etree_generate        | 85.4 ms                                                      | 103 ms: 1.20x slower                                                |
| coverage                  | 83.0 ms                                                      | 99.7 ms: 1.20x slower                                               |
| spectral_norm             | 111 ms                                                       | 134 ms: 1.20x slower                                                |
| coroutines                | 23.6 ms                                                      | 28.4 ms: 1.21x slower                                               |
| docutils                  | 2.62 sec                                                     | 3.19 sec: 1.22x slower                                              |
| bpe_tokeniser             | 4.45 sec                                                     | 5.47 sec: 1.23x slower                                              |
| scimark_sparse_mat_mult   | 4.71 ms                                                      | 5.82 ms: 1.24x slower                                               |
| async_generators          | 377 ms                                                       | 467 ms: 1.24x slower                                                |
| pylint                    | 317 ms                                                       | 393 ms: 1.24x slower                                                |
| mdp                       | 2.36 sec                                                     | 3.03 sec: 1.29x slower                                              |
| nqueens                   | 78.6 ms                                                      | 103 ms: 1.31x slower                                                |
| dulwich_log               | 74.8 ms                                                      | 98.9 ms: 1.32x slower                                               |
| meteor_contest            | 102 ms                                                       | 135 ms: 1.33x slower                                                |
| generators                | 28.8 ms                                                      | 38.4 ms: 1.33x slower                                               |
| create_gc_cycles          | 1.34 ms                                                      | 1.82 ms: 1.36x slower                                               |
| genshi_xml                | 48.8 ms                                                      | 66.7 ms: 1.37x slower                                               |
| typing_runtime_protocols  | 155 us                                                       | 212 us: 1.37x slower                                                |
| json_dumps                | 10.5 ms                                                      | 14.5 ms: 1.37x slower                                               |
| fannkuch                  | 370 ms                                                       | 511 ms: 1.38x slower                                                |
| python_startup_no_site    | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                               |
| xml_etree_process         | 59.3 ms                                                      | 82.3 ms: 1.39x slower                                               |
| tomli_loads               | 2.01 sec                                                     | 2.81 sec: 1.40x slower                                              |
| crypto_pyaes              | 67.9 ms                                                      | 95.4 ms: 1.40x slower                                               |
| sqlglot_normalize         | 106 ms                                                       | 151 ms: 1.43x slower                                                |
| sqlglot_optimize          | 52.7 ms                                                      | 75.4 ms: 1.43x slower                                               |
| pycparser                 | 1.12 sec                                                     | 1.61 sec: 1.44x slower                                              |
| regex_compile             | 132 ms                                                       | 191 ms: 1.45x slower                                                |
| 2to3                      | 260 ms                                                       | 376 ms: 1.45x slower                                                |
| pprint_safe_repr          | 738 ms                                                       | 1.07 sec: 1.45x slower                                              |
| html5lib                  | 67.0 ms                                                      | 98.9 ms: 1.48x slower                                               |
| pprint_pformat            | 1.50 sec                                                     | 2.24 sec: 1.49x slower                                              |
| nbody                     | 85.1 ms                                                      | 128 ms: 1.50x slower                                                |
| sympy_integrate           | 19.8 ms                                                      | 30.8 ms: 1.55x slower                                               |
| genshi_text               | 21.5 ms                                                      | 33.5 ms: 1.56x slower                                               |
| thrift                    | 778 us                                                       | 1.22 ms: 1.57x slower                                               |
| python_startup            | 11.0 ms                                                      | 17.4 ms: 1.59x slower                                               |
| django_template           | 34.1 ms                                                      | 55.2 ms: 1.62x slower                                               |
| pyflate                   | 449 ms                                                       | 726 ms: 1.62x slower                                                |
| scimark_lu                | 113 ms                                                       | 194 ms: 1.72x slower                                                |
| mako                      | 11.3 ms                                                      | 19.6 ms: 1.73x slower                                               |
| comprehensions            | 16.5 us                                                      | 28.9 us: 1.76x slower                                               |
| sympy_str                 | 275 ms                                                       | 495 ms: 1.80x slower                                                |
| hexiom                    | 5.99 ms                                                      | 10.8 ms: 1.80x slower                                               |
| unpickle_pure_python      | 210 us                                                       | 379 us: 1.81x slower                                                |
| scimark_sor               | 134 ms                                                       | 245 ms: 1.83x slower                                                |
| richards                  | 45.2 ms                                                      | 82.6 ms: 1.83x slower                                               |
| logging_simple            | 6.16 us                                                      | 11.3 us: 1.83x slower                                               |
| logging_format            | 6.84 us                                                      | 12.6 us: 1.84x slower                                               |
| float                     | 77.5 ms                                                      | 143 ms: 1.85x slower                                                |
| scimark_monte_carlo       | 65.4 ms                                                      | 122 ms: 1.87x slower                                                |
| pickle_pure_python        | 294 us                                                       | 556 us: 1.89x slower                                                |
| richards_super            | 51.6 ms                                                      | 99.1 ms: 1.92x slower                                               |
| logging_silent            | 103 ns                                                       | 197 ns: 1.92x slower                                                |
| chaos                     | 57.3 ms                                                      | 112 ms: 1.95x slower                                                |
| sqlglot_transpile         | 1.56 ms                                                      | 3.08 ms: 1.98x slower                                               |
| go                        | 141 ms                                                       | 281 ms: 2.00x slower                                                |
| sqlglot_parse             | 1.25 ms                                                      | 2.66 ms: 2.13x slower                                               |
| sympy_expand              | 457 ms                                                       | 987 ms: 2.16x slower                                                |
| sympy_sum                 | 156 ms                                                       | 359 ms: 2.31x slower                                                |
| raytrace                  | 253 ms                                                       | 602 ms: 2.38x slower                                                |
| deltablue                 | 3.12 ms                                                      | 8.76 ms: 2.80x slower                                               |
| bench_thread_pool         | 919 us                                                       | 3.38 ms: 3.68x slower                                               |
| bench_mp_pool             | 11.0 ms                                                      | 110 ms: 9.97x slower                                                |
| Geometric mean            | (ref)                                                        | 1.44x slower                                                        |

Benchmark hidden because not significant (5): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, asyncio_websockets, xml_etree_iterparse, async_tree_io
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241204-3.14.0a2+-0f5d11c-NOGIL/bm-20241204-vultr-x86_64-mpage-measure_gc_changes-3.14.0a2+-0f5d11c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.279x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.29x
- 95% likely to have a slowdown of 1.27x
- 99% likely to have a slowdown of 1.23x

# Memory
- memory change: 1.32x