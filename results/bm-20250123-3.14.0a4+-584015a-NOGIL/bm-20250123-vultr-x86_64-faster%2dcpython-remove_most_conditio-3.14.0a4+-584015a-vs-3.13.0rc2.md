# Results vs. 3.13.0rc2

- fork: faster-cpython
- ref: remove_most_conditio
- machine: linux-x86_64
- commit hash: 584015a
- commit date: 2025-01-23
- overall geometric mean: 1.087x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.05x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 304 ms: 1.17x slower                                                             |
| docutils       | 2.62 sec                                                     | 2.87 sec: 1.10x slower                                                           |
| html5lib       | 67.0 ms                                                      | 70.2 ms: 1.05x slower                                                            |
| Geometric mean | (ref)                                                        | 1.10x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 582 ms: 1.57x faster                                                             |
| async_tree_io              | 876 ms                                                       | 614 ms: 1.43x faster                                                             |
| async_tree_none_tg         | 336 ms                                                       | 250 ms: 1.34x faster                                                             |
| async_tree_memoization     | 461 ms                                                       | 354 ms: 1.30x faster                                                             |
| async_tree_memoization_tg  | 414 ms                                                       | 321 ms: 1.29x faster                                                             |
| async_tree_none            | 354 ms                                                       | 289 ms: 1.22x faster                                                             |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 554 ms: 1.15x faster                                                             |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 584 ms: 1.14x faster                                                             |
| coroutines                 | 23.6 ms                                                      | 22.9 ms: 1.03x faster                                                            |
| async_generators           | 377 ms                                                       | 372 ms: 1.02x faster                                                             |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                             |
| Geometric mean             | (ref)                                                        | 1.22x faster                                                                     |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 74.7 ms: 1.04x faster                                                            |
| pidigits       | 217 ms                                                       | 215 ms: 1.01x faster                                                             |
| nbody          | 85.1 ms                                                      | 131 ms: 1.54x slower                                                             |
| Geometric mean | (ref)                                                        | 1.14x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.89 ms: 1.07x faster                                                            |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                             |
| regex_v8       | 22.7 ms                                                      | 23.9 ms: 1.05x slower                                                            |
| regex_compile  | 132 ms                                                       | 149 ms: 1.13x slower                                                             |
| Geometric mean | (ref)                                                        | 1.03x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 86.8 ms: 1.09x faster                                                            |
| xml_etree_parse      | 136 ms                                                       | 127 ms: 1.07x faster                                                             |
| json_loads           | 27.0 us                                                      | 30.4 us: 1.13x slower                                                            |
| xml_etree_generate   | 85.4 ms                                                      | 96.6 ms: 1.13x slower                                                            |
| tomli_loads          | 2.01 sec                                                     | 2.32 sec: 1.16x slower                                                           |
| xml_etree_process    | 59.3 ms                                                      | 69.0 ms: 1.16x slower                                                            |
| unpickle_pure_python | 210 us                                                       | 244 us: 1.16x slower                                                             |
| json_dumps           | 10.5 ms                                                      | 12.9 ms: 1.22x slower                                                            |
| pickle_pure_python   | 294 us                                                       | 370 us: 1.25x slower                                                             |
| Geometric mean       | (ref)                                                        | 1.11x slower                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.53 ms: 1.29x slower                                                            |
| python_startup         | 11.0 ms                                                      | 15.2 ms: 1.38x slower                                                            |
| Geometric mean         | (ref)                                                        | 1.33x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 59.2 ms: 1.21x slower                                                            |
| genshi_text     | 21.5 ms                                                      | 27.5 ms: 1.28x slower                                                            |
| django_template | 34.1 ms                                                      | 44.3 ms: 1.30x slower                                                            |
| mako            | 11.3 ms                                                      | 15.6 ms: 1.38x slower                                                            |
| Geometric mean  | (ref)                                                        | 1.29x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 582 ms: 1.57x faster                                                             |
| async_tree_io              | 876 ms                                                       | 614 ms: 1.43x faster                                                             |
| async_tree_none_tg         | 336 ms                                                       | 250 ms: 1.34x faster                                                             |
| async_tree_memoization     | 461 ms                                                       | 354 ms: 1.30x faster                                                             |
| async_tree_memoization_tg  | 414 ms                                                       | 321 ms: 1.29x faster                                                             |
| async_tree_none            | 354 ms                                                       | 289 ms: 1.22x faster                                                             |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 554 ms: 1.15x faster                                                             |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 584 ms: 1.14x faster                                                             |
| deepcopy                   | 355 us                                                       | 312 us: 1.14x faster                                                             |
| xml_etree_iterparse        | 94.9 ms                                                      | 86.8 ms: 1.09x faster                                                            |
| sqlite_synth               | 2.21 us                                                      | 2.05 us: 1.08x faster                                                            |
| xml_etree_parse            | 136 ms                                                       | 127 ms: 1.07x faster                                                             |
| regex_effbot               | 3.08 ms                                                      | 2.89 ms: 1.07x faster                                                            |
| go                         | 141 ms                                                       | 134 ms: 1.05x faster                                                             |
| float                      | 77.5 ms                                                      | 74.7 ms: 1.04x faster                                                            |
| pathlib                    | 19.2 ms                                                      | 18.6 ms: 1.03x faster                                                            |
| coroutines                 | 23.6 ms                                                      | 22.9 ms: 1.03x faster                                                            |
| deepcopy_memo              | 39.1 us                                                      | 38.4 us: 1.02x faster                                                            |
| scimark_sor                | 134 ms                                                       | 132 ms: 1.02x faster                                                             |
| async_generators           | 377 ms                                                       | 372 ms: 1.02x faster                                                             |
| pidigits                   | 217 ms                                                       | 215 ms: 1.01x faster                                                             |
| create_gc_cycles           | 1.34 ms                                                      | 1.33 ms: 1.01x faster                                                            |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                             |
| regex_dna                  | 180 ms                                                       | 182 ms: 1.01x slower                                                             |
| deepcopy_reduce            | 3.11 us                                                      | 3.19 us: 1.03x slower                                                            |
| gc_traversal               | 3.14 ms                                                      | 3.25 ms: 1.04x slower                                                            |
| html5lib                   | 67.0 ms                                                      | 70.2 ms: 1.05x slower                                                            |
| regex_v8                   | 22.7 ms                                                      | 23.9 ms: 1.05x slower                                                            |
| pycparser                  | 1.12 sec                                                     | 1.18 sec: 1.06x slower                                                           |
| bpe_tokeniser              | 4.45 sec                                                     | 4.71 sec: 1.06x slower                                                           |
| json                       | 4.93 ms                                                      | 5.28 ms: 1.07x slower                                                            |
| logging_silent             | 103 ns                                                       | 111 ns: 1.08x slower                                                             |
| generators                 | 28.8 ms                                                      | 31.1 ms: 1.08x slower                                                            |
| telco                      | 7.82 ms                                                      | 8.47 ms: 1.08x slower                                                            |
| dulwich_log                | 74.8 ms                                                      | 81.2 ms: 1.08x slower                                                            |
| pyflate                    | 449 ms                                                       | 487 ms: 1.09x slower                                                             |
| mdp                        | 2.36 sec                                                     | 2.58 sec: 1.10x slower                                                           |
| docutils                   | 2.62 sec                                                     | 2.87 sec: 1.10x slower                                                           |
| scimark_fft                | 349 ms                                                       | 385 ms: 1.10x slower                                                             |
| pprint_safe_repr           | 738 ms                                                       | 826 ms: 1.12x slower                                                             |
| json_loads                 | 27.0 us                                                      | 30.4 us: 1.13x slower                                                            |
| regex_compile              | 132 ms                                                       | 149 ms: 1.13x slower                                                             |
| xml_etree_generate         | 85.4 ms                                                      | 96.6 ms: 1.13x slower                                                            |
| pprint_pformat             | 1.50 sec                                                     | 1.71 sec: 1.14x slower                                                           |
| sqlglot_normalize          | 106 ms                                                       | 122 ms: 1.15x slower                                                             |
| tomli_loads                | 2.01 sec                                                     | 2.32 sec: 1.16x slower                                                           |
| xml_etree_process          | 59.3 ms                                                      | 69.0 ms: 1.16x slower                                                            |
| unpickle_pure_python       | 210 us                                                       | 244 us: 1.16x slower                                                             |
| sqlglot_optimize           | 52.7 ms                                                      | 61.3 ms: 1.16x slower                                                            |
| 2to3                       | 260 ms                                                       | 304 ms: 1.17x slower                                                             |
| thrift                     | 778 us                                                       | 916 us: 1.18x slower                                                             |
| logging_simple             | 6.16 us                                                      | 7.26 us: 1.18x slower                                                            |
| chaos                      | 57.3 ms                                                      | 67.8 ms: 1.18x slower                                                            |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.60 ms: 1.19x slower                                                            |
| coverage                   | 83.0 ms                                                      | 98.9 ms: 1.19x slower                                                            |
| hexiom                     | 5.99 ms                                                      | 7.14 ms: 1.19x slower                                                            |
| sympy_expand               | 457 ms                                                       | 548 ms: 1.20x slower                                                             |
| sympy_sum                  | 156 ms                                                       | 186 ms: 1.20x slower                                                             |
| genshi_xml                 | 48.8 ms                                                      | 59.2 ms: 1.21x slower                                                            |
| sympy_str                  | 275 ms                                                       | 334 ms: 1.22x slower                                                             |
| nqueens                    | 78.6 ms                                                      | 95.7 ms: 1.22x slower                                                            |
| scimark_monte_carlo        | 65.4 ms                                                      | 79.8 ms: 1.22x slower                                                            |
| scimark_lu                 | 113 ms                                                       | 138 ms: 1.22x slower                                                             |
| json_dumps                 | 10.5 ms                                                      | 12.9 ms: 1.22x slower                                                            |
| logging_format             | 6.84 us                                                      | 8.36 us: 1.22x slower                                                            |
| sympy_integrate            | 19.8 ms                                                      | 24.3 ms: 1.23x slower                                                            |
| sqlglot_transpile          | 1.56 ms                                                      | 1.93 ms: 1.24x slower                                                            |
| sqlglot_parse              | 1.25 ms                                                      | 1.55 ms: 1.24x slower                                                            |
| comprehensions             | 16.5 us                                                      | 20.4 us: 1.24x slower                                                            |
| pickle_pure_python         | 294 us                                                       | 370 us: 1.25x slower                                                             |
| raytrace                   | 253 ms                                                       | 321 ms: 1.27x slower                                                             |
| genshi_text                | 21.5 ms                                                      | 27.5 ms: 1.28x slower                                                            |
| crypto_pyaes               | 67.9 ms                                                      | 86.6 ms: 1.28x slower                                                            |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                             |
| fannkuch                   | 370 ms                                                       | 476 ms: 1.29x slower                                                             |
| python_startup_no_site     | 7.39 ms                                                      | 9.53 ms: 1.29x slower                                                            |
| django_template            | 34.1 ms                                                      | 44.3 ms: 1.30x slower                                                            |
| typing_runtime_protocols   | 155 us                                                       | 203 us: 1.31x slower                                                             |
| richards                   | 45.2 ms                                                      | 62.2 ms: 1.37x slower                                                            |
| mako                       | 11.3 ms                                                      | 15.6 ms: 1.38x slower                                                            |
| python_startup             | 11.0 ms                                                      | 15.2 ms: 1.38x slower                                                            |
| richards_super             | 51.6 ms                                                      | 71.6 ms: 1.39x slower                                                            |
| deltablue                  | 3.12 ms                                                      | 4.56 ms: 1.46x slower                                                            |
| nbody                      | 85.1 ms                                                      | 131 ms: 1.54x slower                                                             |
| bench_thread_pool          | 919 us                                                       | 3.30 ms: 3.59x slower                                                            |
| bench_mp_pool              | 11.0 ms                                                      | 94.2 ms: 8.57x slower                                                            |
| Geometric mean             | (ref)                                                        | 1.14x slower                                                                     |

Benchmark hidden because not significant (2): spectral_norm, pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250123-3.14.0a4+-584015a-NOGIL/bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.087x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.06x
- 99% likely to have a slowdown of 1.05x

# Memory
- memory change: 1.33x