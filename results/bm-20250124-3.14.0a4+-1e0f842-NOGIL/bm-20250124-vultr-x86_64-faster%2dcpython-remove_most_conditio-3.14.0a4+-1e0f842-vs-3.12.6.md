# Results vs. 3.12.6

- fork: faster-cpython
- ref: remove_most_conditio
- machine: linux-x86_64
- commit hash: 1e0f842
- commit date: 2025-01-24
- overall geometric mean: 1.053x slower
- HPT reliability: 99.95%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 303 ms: 1.15x slower                                                             |
| docutils       | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                           |
| html5lib       | 63.6 ms                                                | 69.5 ms: 1.09x slower                                                            |
| Geometric mean | (ref)                                                  | 1.10x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 577 ms: 1.92x faster                                                             |
| async_tree_none_tg         | 446 ms                                                 | 249 ms: 1.79x faster                                                             |
| async_tree_io              | 1.08 sec                                               | 615 ms: 1.76x faster                                                             |
| async_tree_memoization_tg  | 560 ms                                                 | 319 ms: 1.75x faster                                                             |
| async_tree_none            | 464 ms                                                 | 285 ms: 1.63x faster                                                             |
| async_tree_memoization     | 555 ms                                                 | 352 ms: 1.58x faster                                                             |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 504 ms: 1.43x faster                                                             |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 535 ms: 1.34x faster                                                             |
| async_generators           | 384 ms                                                 | 368 ms: 1.05x faster                                                             |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.01x faster                                                            |
| Geometric mean             | (ref)                                                  | 1.44x faster                                                                     |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 75.6 ms: 1.07x faster                                                            |
| pidigits       | 184 ms                                                 | 190 ms: 1.03x slower                                                             |
| nbody          | 89.3 ms                                                | 131 ms: 1.47x slower                                                             |
| Geometric mean | (ref)                                                  | 1.12x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.85 ms: 1.11x faster                                                            |
| regex_compile  | 142 ms                                                 | 150 ms: 1.05x slower                                                             |
| regex_dna      | 168 ms                                                 | 187 ms: 1.12x slower                                                             |
| regex_v8       | 20.6 ms                                                | 23.4 ms: 1.13x slower                                                            |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 87.0 ms: 1.11x faster                                                            |
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                                             |
| tomli_loads          | 2.11 sec                                               | 2.35 sec: 1.11x slower                                                           |
| unpickle_pure_python | 221 us                                                 | 247 us: 1.12x slower                                                             |
| xml_etree_generate   | 85.2 ms                                                | 96.7 ms: 1.13x slower                                                            |
| json_loads           | 26.5 us                                                | 30.5 us: 1.15x slower                                                            |
| xml_etree_process    | 59.0 ms                                                | 69.4 ms: 1.18x slower                                                            |
| pickle_pure_python   | 308 us                                                 | 373 us: 1.21x slower                                                             |
| json_dumps           | 10.4 ms                                                | 13.0 ms: 1.25x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.52 ms: 1.33x slower                                                            |
| python_startup         | 9.93 ms                                                | 15.2 ms: 1.53x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.7 ms: 1.19x slower                                                            |
| genshi_text     | 22.8 ms                                                | 27.7 ms: 1.21x slower                                                            |
| django_template | 34.7 ms                                                | 44.4 ms: 1.28x slower                                                            |
| mako            | 11.0 ms                                                | 15.9 ms: 1.45x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.28x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 577 ms: 1.92x faster                                                             |
| async_tree_none_tg         | 446 ms                                                 | 249 ms: 1.79x faster                                                             |
| async_tree_io              | 1.08 sec                                               | 615 ms: 1.76x faster                                                             |
| async_tree_memoization_tg  | 560 ms                                                 | 319 ms: 1.75x faster                                                             |
| async_tree_none            | 464 ms                                                 | 285 ms: 1.63x faster                                                             |
| async_tree_memoization     | 555 ms                                                 | 352 ms: 1.58x faster                                                             |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 504 ms: 1.43x faster                                                             |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 535 ms: 1.34x faster                                                             |
| pathlib                    | 21.5 ms                                                | 19.2 ms: 1.12x faster                                                            |
| deepcopy                   | 352 us                                                 | 315 us: 1.12x faster                                                             |
| regex_effbot               | 3.17 ms                                                | 2.85 ms: 1.11x faster                                                            |
| xml_etree_iterparse        | 96.7 ms                                                | 87.0 ms: 1.11x faster                                                            |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                                             |
| sqlite_synth               | 2.20 us                                                | 2.04 us: 1.08x faster                                                            |
| float                      | 80.8 ms                                                | 75.6 ms: 1.07x faster                                                            |
| deepcopy_memo              | 40.3 us                                                | 38.0 us: 1.06x faster                                                            |
| gc_traversal               | 3.46 ms                                                | 3.29 ms: 1.05x faster                                                            |
| async_generators           | 384 ms                                                 | 368 ms: 1.05x faster                                                             |
| generators                 | 32.2 ms                                                | 31.3 ms: 1.03x faster                                                            |
| spectral_norm              | 110 ms                                                 | 107 ms: 1.03x faster                                                             |
| go                         | 139 ms                                                 | 137 ms: 1.02x faster                                                             |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.01x faster                                                            |
| bpe_tokeniser              | 4.74 sec                                               | 4.68 sec: 1.01x faster                                                           |
| scimark_sor                | 130 ms                                                 | 131 ms: 1.01x slower                                                             |
| pycparser                  | 1.17 sec                                               | 1.19 sec: 1.01x slower                                                           |
| logging_silent             | 109 ns                                                 | 112 ns: 1.03x slower                                                             |
| pidigits                   | 184 ms                                                 | 190 ms: 1.03x slower                                                             |
| dulwich_log                | 78.9 ms                                                | 82.0 ms: 1.04x slower                                                            |
| comprehensions             | 19.8 us                                                | 20.8 us: 1.05x slower                                                            |
| regex_compile              | 142 ms                                                 | 150 ms: 1.05x slower                                                             |
| json                       | 5.02 ms                                                | 5.28 ms: 1.05x slower                                                            |
| docutils                   | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                           |
| deepcopy_reduce            | 3.08 us                                                | 3.27 us: 1.06x slower                                                            |
| raytrace                   | 299 ms                                                 | 325 ms: 1.09x slower                                                             |
| html5lib                   | 63.6 ms                                                | 69.5 ms: 1.09x slower                                                            |
| pprint_safe_repr           | 743 ms                                                 | 814 ms: 1.10x slower                                                             |
| mdp                        | 2.42 sec                                               | 2.65 sec: 1.10x slower                                                           |
| scimark_fft                | 342 ms                                                 | 377 ms: 1.10x slower                                                             |
| chaos                      | 62.8 ms                                                | 69.4 ms: 1.10x slower                                                            |
| pyflate                    | 448 ms                                                 | 495 ms: 1.10x slower                                                             |
| pprint_pformat             | 1.52 sec                                               | 1.68 sec: 1.11x slower                                                           |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.1 ms: 1.11x slower                                                            |
| tomli_loads                | 2.11 sec                                               | 2.35 sec: 1.11x slower                                                           |
| regex_dna                  | 168 ms                                                 | 187 ms: 1.12x slower                                                             |
| unpickle_pure_python       | 221 us                                                 | 247 us: 1.12x slower                                                             |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                                             |
| sqlglot_normalize          | 107 ms                                                 | 120 ms: 1.12x slower                                                             |
| logging_simple             | 6.63 us                                                | 7.48 us: 1.13x slower                                                            |
| crypto_pyaes               | 76.6 ms                                                | 86.7 ms: 1.13x slower                                                            |
| xml_etree_generate         | 85.2 ms                                                | 96.7 ms: 1.13x slower                                                            |
| regex_v8                   | 20.6 ms                                                | 23.4 ms: 1.13x slower                                                            |
| sqlglot_parse              | 1.36 ms                                                | 1.54 ms: 1.14x slower                                                            |
| sqlglot_optimize           | 53.3 ms                                                | 60.7 ms: 1.14x slower                                                            |
| sqlalchemy_declarative     | 143 ms                                                 | 163 ms: 1.14x slower                                                             |
| sympy_str                  | 292 ms                                                 | 334 ms: 1.15x slower                                                             |
| sqlglot_transpile          | 1.67 ms                                                | 1.91 ms: 1.15x slower                                                            |
| 2to3                       | 264 ms                                                 | 303 ms: 1.15x slower                                                             |
| json_loads                 | 26.5 us                                                | 30.5 us: 1.15x slower                                                            |
| logging_format             | 7.35 us                                                | 8.55 us: 1.16x slower                                                            |
| sympy_expand               | 468 ms                                                 | 547 ms: 1.17x slower                                                             |
| hexiom                     | 6.17 ms                                                | 7.22 ms: 1.17x slower                                                            |
| sympy_integrate            | 20.5 ms                                                | 24.1 ms: 1.17x slower                                                            |
| thrift                     | 791 us                                                 | 929 us: 1.17x slower                                                             |
| xml_etree_process          | 59.0 ms                                                | 69.4 ms: 1.18x slower                                                            |
| scimark_monte_carlo        | 68.4 ms                                                | 81.0 ms: 1.18x slower                                                            |
| genshi_xml                 | 50.2 ms                                                | 59.7 ms: 1.19x slower                                                            |
| scimark_lu                 | 114 ms                                                 | 137 ms: 1.20x slower                                                             |
| nqueens                    | 80.1 ms                                                | 95.8 ms: 1.20x slower                                                            |
| richards                   | 45.9 ms                                                | 55.2 ms: 1.20x slower                                                            |
| genshi_text                | 22.8 ms                                                | 27.7 ms: 1.21x slower                                                            |
| pickle_pure_python         | 308 us                                                 | 373 us: 1.21x slower                                                             |
| create_gc_cycles           | 1.09 ms                                                | 1.33 ms: 1.22x slower                                                            |
| richards_super             | 51.9 ms                                                | 63.7 ms: 1.23x slower                                                            |
| typing_runtime_protocols   | 163 us                                                 | 202 us: 1.23x slower                                                             |
| json_dumps                 | 10.4 ms                                                | 13.0 ms: 1.25x slower                                                            |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.51 ms: 1.26x slower                                                            |
| meteor_contest             | 104 ms                                                 | 131 ms: 1.27x slower                                                             |
| django_template            | 34.7 ms                                                | 44.4 ms: 1.28x slower                                                            |
| fannkuch                   | 372 ms                                                 | 484 ms: 1.30x slower                                                             |
| telco                      | 6.53 ms                                                | 8.49 ms: 1.30x slower                                                            |
| python_startup_no_site     | 7.16 ms                                                | 9.52 ms: 1.33x slower                                                            |
| deltablue                  | 3.45 ms                                                | 4.63 ms: 1.34x slower                                                            |
| coverage                   | 71.4 ms                                                | 98.2 ms: 1.37x slower                                                            |
| mako                       | 11.0 ms                                                | 15.9 ms: 1.45x slower                                                            |
| nbody                      | 89.3 ms                                                | 131 ms: 1.47x slower                                                             |
| python_startup             | 9.93 ms                                                | 15.2 ms: 1.53x slower                                                            |
| bench_thread_pool          | 941 us                                                 | 3.31 ms: 3.51x slower                                                            |
| bench_mp_pool              | 10.8 ms                                                | 94.2 ms: 8.72x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.09x slower                                                                     |

Benchmark hidden because not significant (2): pylint, asyncio_websockets
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250124-3.14.0a4+-1e0f842-NOGIL/bm-20250124-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-1e0f842.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.053x slower

# HPT report

- Reliability score: 99.95% likely to be slow
- 90% likely to have a slowdown of 1.06x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.35x