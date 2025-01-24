# Results vs. 3.13.0rc2

- fork: faster-cpython
- ref: remove_most_conditio
- machine: linux-x86_64
- commit hash: 1e0f842
- commit date: 2025-01-24
- overall geometric mean: 1.083x slower
- HPT reliability: 99.98%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 303 ms: 1.17x slower                                                             |
| docutils       | 2.62 sec                                                     | 2.80 sec: 1.07x slower                                                           |
| html5lib       | 67.0 ms                                                      | 69.5 ms: 1.04x slower                                                            |
| Geometric mean | (ref)                                                        | 1.09x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 577 ms: 1.58x faster                                                             |
| async_tree_io              | 876 ms                                                       | 615 ms: 1.43x faster                                                             |
| async_tree_none_tg         | 336 ms                                                       | 249 ms: 1.35x faster                                                             |
| async_tree_memoization     | 461 ms                                                       | 352 ms: 1.31x faster                                                             |
| async_tree_memoization_tg  | 414 ms                                                       | 319 ms: 1.30x faster                                                             |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 504 ms: 1.27x faster                                                             |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 535 ms: 1.25x faster                                                             |
| async_tree_none            | 354 ms                                                       | 285 ms: 1.24x faster                                                             |
| async_generators           | 377 ms                                                       | 368 ms: 1.03x faster                                                             |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                             |
| Geometric mean             | (ref)                                                        | 1.24x faster                                                                     |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 190 ms: 1.14x faster                                                             |
| float          | 77.5 ms                                                      | 75.6 ms: 1.02x faster                                                            |
| nbody          | 85.1 ms                                                      | 131 ms: 1.54x slower                                                             |
| Geometric mean | (ref)                                                        | 1.10x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.85 ms: 1.08x faster                                                            |
| regex_v8       | 22.7 ms                                                      | 23.4 ms: 1.03x slower                                                            |
| regex_dna      | 180 ms                                                       | 187 ms: 1.04x slower                                                             |
| regex_compile  | 132 ms                                                       | 150 ms: 1.13x slower                                                             |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.0 ms: 1.09x faster                                                            |
| xml_etree_parse      | 136 ms                                                       | 127 ms: 1.07x faster                                                             |
| json_loads           | 27.0 us                                                      | 30.5 us: 1.13x slower                                                            |
| xml_etree_generate   | 85.4 ms                                                      | 96.7 ms: 1.13x slower                                                            |
| xml_etree_process    | 59.3 ms                                                      | 69.4 ms: 1.17x slower                                                            |
| tomli_loads          | 2.01 sec                                                     | 2.35 sec: 1.17x slower                                                           |
| unpickle_pure_python | 210 us                                                       | 247 us: 1.18x slower                                                             |
| json_dumps           | 10.5 ms                                                      | 13.0 ms: 1.23x slower                                                            |
| pickle_pure_python   | 294 us                                                       | 373 us: 1.27x slower                                                             |
| Geometric mean       | (ref)                                                        | 1.12x slower                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.52 ms: 1.29x slower                                                            |
| python_startup         | 11.0 ms                                                      | 15.2 ms: 1.38x slower                                                            |
| Geometric mean         | (ref)                                                        | 1.33x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 59.7 ms: 1.22x slower                                                            |
| genshi_text     | 21.5 ms                                                      | 27.7 ms: 1.28x slower                                                            |
| django_template | 34.1 ms                                                      | 44.4 ms: 1.30x slower                                                            |
| mako            | 11.3 ms                                                      | 15.9 ms: 1.40x slower                                                            |
| Geometric mean  | (ref)                                                        | 1.30x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 577 ms: 1.58x faster                                                             |
| async_tree_io              | 876 ms                                                       | 615 ms: 1.43x faster                                                             |
| async_tree_none_tg         | 336 ms                                                       | 249 ms: 1.35x faster                                                             |
| async_tree_memoization     | 461 ms                                                       | 352 ms: 1.31x faster                                                             |
| async_tree_memoization_tg  | 414 ms                                                       | 319 ms: 1.30x faster                                                             |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 504 ms: 1.27x faster                                                             |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 535 ms: 1.25x faster                                                             |
| async_tree_none            | 354 ms                                                       | 285 ms: 1.24x faster                                                             |
| pidigits                   | 217 ms                                                       | 190 ms: 1.14x faster                                                             |
| deepcopy                   | 355 us                                                       | 315 us: 1.13x faster                                                             |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.0 ms: 1.09x faster                                                            |
| regex_effbot               | 3.08 ms                                                      | 2.85 ms: 1.08x faster                                                            |
| sqlite_synth               | 2.21 us                                                      | 2.04 us: 1.08x faster                                                            |
| xml_etree_parse            | 136 ms                                                       | 127 ms: 1.07x faster                                                             |
| spectral_norm              | 111 ms                                                       | 107 ms: 1.03x faster                                                             |
| go                         | 141 ms                                                       | 137 ms: 1.03x faster                                                             |
| deepcopy_memo              | 39.1 us                                                      | 38.0 us: 1.03x faster                                                            |
| async_generators           | 377 ms                                                       | 368 ms: 1.03x faster                                                             |
| scimark_sor                | 134 ms                                                       | 131 ms: 1.02x faster                                                             |
| float                      | 77.5 ms                                                      | 75.6 ms: 1.02x faster                                                            |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                             |
| regex_v8                   | 22.7 ms                                                      | 23.4 ms: 1.03x slower                                                            |
| html5lib                   | 67.0 ms                                                      | 69.5 ms: 1.04x slower                                                            |
| regex_dna                  | 180 ms                                                       | 187 ms: 1.04x slower                                                             |
| gc_traversal               | 3.14 ms                                                      | 3.29 ms: 1.05x slower                                                            |
| bpe_tokeniser              | 4.45 sec                                                     | 4.68 sec: 1.05x slower                                                           |
| deepcopy_reduce            | 3.11 us                                                      | 3.27 us: 1.05x slower                                                            |
| pycparser                  | 1.12 sec                                                     | 1.19 sec: 1.06x slower                                                           |
| docutils                   | 2.62 sec                                                     | 2.80 sec: 1.07x slower                                                           |
| json                       | 4.93 ms                                                      | 5.28 ms: 1.07x slower                                                            |
| scimark_fft                | 349 ms                                                       | 377 ms: 1.08x slower                                                             |
| telco                      | 7.82 ms                                                      | 8.49 ms: 1.08x slower                                                            |
| generators                 | 28.8 ms                                                      | 31.3 ms: 1.09x slower                                                            |
| logging_silent             | 103 ns                                                       | 112 ns: 1.09x slower                                                             |
| dulwich_log                | 74.8 ms                                                      | 82.0 ms: 1.10x slower                                                            |
| pyflate                    | 449 ms                                                       | 495 ms: 1.10x slower                                                             |
| pprint_safe_repr           | 738 ms                                                       | 814 ms: 1.10x slower                                                             |
| pprint_pformat             | 1.50 sec                                                     | 1.68 sec: 1.12x slower                                                           |
| mdp                        | 2.36 sec                                                     | 2.65 sec: 1.13x slower                                                           |
| json_loads                 | 27.0 us                                                      | 30.5 us: 1.13x slower                                                            |
| xml_etree_generate         | 85.4 ms                                                      | 96.7 ms: 1.13x slower                                                            |
| regex_compile              | 132 ms                                                       | 150 ms: 1.13x slower                                                             |
| sqlglot_normalize          | 106 ms                                                       | 120 ms: 1.13x slower                                                             |
| sqlglot_optimize           | 52.7 ms                                                      | 60.7 ms: 1.15x slower                                                            |
| 2to3                       | 260 ms                                                       | 303 ms: 1.17x slower                                                             |
| xml_etree_process          | 59.3 ms                                                      | 69.4 ms: 1.17x slower                                                            |
| tomli_loads                | 2.01 sec                                                     | 2.35 sec: 1.17x slower                                                           |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.51 ms: 1.17x slower                                                            |
| unpickle_pure_python       | 210 us                                                       | 247 us: 1.18x slower                                                             |
| coverage                   | 83.0 ms                                                      | 98.2 ms: 1.18x slower                                                            |
| thrift                     | 778 us                                                       | 929 us: 1.19x slower                                                             |
| sympy_expand               | 457 ms                                                       | 547 ms: 1.20x slower                                                             |
| sympy_sum                  | 156 ms                                                       | 186 ms: 1.20x slower                                                             |
| hexiom                     | 5.99 ms                                                      | 7.22 ms: 1.21x slower                                                            |
| chaos                      | 57.3 ms                                                      | 69.4 ms: 1.21x slower                                                            |
| scimark_lu                 | 113 ms                                                       | 137 ms: 1.21x slower                                                             |
| logging_simple             | 6.16 us                                                      | 7.48 us: 1.21x slower                                                            |
| sympy_str                  | 275 ms                                                       | 334 ms: 1.22x slower                                                             |
| sympy_integrate            | 19.8 ms                                                      | 24.1 ms: 1.22x slower                                                            |
| nqueens                    | 78.6 ms                                                      | 95.8 ms: 1.22x slower                                                            |
| richards                   | 45.2 ms                                                      | 55.2 ms: 1.22x slower                                                            |
| genshi_xml                 | 48.8 ms                                                      | 59.7 ms: 1.22x slower                                                            |
| sqlglot_transpile          | 1.56 ms                                                      | 1.91 ms: 1.23x slower                                                            |
| json_dumps                 | 10.5 ms                                                      | 13.0 ms: 1.23x slower                                                            |
| richards_super             | 51.6 ms                                                      | 63.7 ms: 1.23x slower                                                            |
| sqlglot_parse              | 1.25 ms                                                      | 1.54 ms: 1.23x slower                                                            |
| scimark_monte_carlo        | 65.4 ms                                                      | 81.0 ms: 1.24x slower                                                            |
| logging_format             | 6.84 us                                                      | 8.55 us: 1.25x slower                                                            |
| comprehensions             | 16.5 us                                                      | 20.8 us: 1.26x slower                                                            |
| pickle_pure_python         | 294 us                                                       | 373 us: 1.27x slower                                                             |
| crypto_pyaes               | 67.9 ms                                                      | 86.7 ms: 1.28x slower                                                            |
| genshi_text                | 21.5 ms                                                      | 27.7 ms: 1.28x slower                                                            |
| python_startup_no_site     | 7.39 ms                                                      | 9.52 ms: 1.29x slower                                                            |
| raytrace                   | 253 ms                                                       | 325 ms: 1.29x slower                                                             |
| meteor_contest             | 102 ms                                                       | 131 ms: 1.29x slower                                                             |
| django_template            | 34.1 ms                                                      | 44.4 ms: 1.30x slower                                                            |
| typing_runtime_protocols   | 155 us                                                       | 202 us: 1.30x slower                                                             |
| fannkuch                   | 370 ms                                                       | 484 ms: 1.31x slower                                                             |
| python_startup             | 11.0 ms                                                      | 15.2 ms: 1.38x slower                                                            |
| mako                       | 11.3 ms                                                      | 15.9 ms: 1.40x slower                                                            |
| deltablue                  | 3.12 ms                                                      | 4.63 ms: 1.48x slower                                                            |
| nbody                      | 85.1 ms                                                      | 131 ms: 1.54x slower                                                             |
| bench_thread_pool          | 919 us                                                       | 3.31 ms: 3.60x slower                                                            |
| bench_mp_pool              | 11.0 ms                                                      | 94.2 ms: 8.56x slower                                                            |
| Geometric mean             | (ref)                                                        | 1.13x slower                                                                     |

Benchmark hidden because not significant (4): create_gc_cycles, pylint, pathlib, coroutines
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250124-3.14.0a4+-1e0f842-NOGIL/bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.083x slower

# HPT report

- Reliability score: 99.98% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.33x