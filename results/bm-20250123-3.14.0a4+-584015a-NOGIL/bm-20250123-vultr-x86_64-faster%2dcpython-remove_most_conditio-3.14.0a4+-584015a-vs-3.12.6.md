# Results vs. 3.12.6

- fork: faster-cpython
- ref: remove_most_conditio
- machine: linux-x86_64
- commit hash: 584015a
- commit date: 2025-01-23
- overall geometric mean: 1.057x slower
- HPT reliability: 99.97%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 304 ms: 1.15x slower                                                             |
| docutils       | 2.64 sec                                               | 2.87 sec: 1.09x slower                                                           |
| html5lib       | 63.6 ms                                                | 70.2 ms: 1.10x slower                                                            |
| Geometric mean | (ref)                                                  | 1.11x slower                                                                     |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 582 ms: 1.91x faster                                                             |
| async_tree_none_tg         | 446 ms                                                 | 250 ms: 1.78x faster                                                             |
| async_tree_io              | 1.08 sec                                               | 614 ms: 1.76x faster                                                             |
| async_tree_memoization_tg  | 560 ms                                                 | 321 ms: 1.74x faster                                                             |
| async_tree_none            | 464 ms                                                 | 289 ms: 1.61x faster                                                             |
| async_tree_memoization     | 555 ms                                                 | 354 ms: 1.57x faster                                                             |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 554 ms: 1.30x faster                                                             |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 584 ms: 1.23x faster                                                             |
| coroutines                 | 23.9 ms                                                | 22.9 ms: 1.05x faster                                                            |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                                             |
| Geometric mean             | (ref)                                                  | 1.41x faster                                                                     |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 74.7 ms: 1.08x faster                                                            |
| pidigits       | 184 ms                                                 | 215 ms: 1.16x slower                                                             |
| nbody          | 89.3 ms                                                | 131 ms: 1.47x slower                                                             |
| Geometric mean | (ref)                                                  | 1.17x slower                                                                     |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.89 ms: 1.10x faster                                                            |
| regex_compile  | 142 ms                                                 | 149 ms: 1.05x slower                                                             |
| regex_dna      | 168 ms                                                 | 182 ms: 1.08x slower                                                             |
| regex_v8       | 20.6 ms                                                | 23.9 ms: 1.16x slower                                                            |
| Geometric mean | (ref)                                                  | 1.05x slower                                                                     |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 86.8 ms: 1.11x faster                                                            |
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                                             |
| tomli_loads          | 2.11 sec                                               | 2.32 sec: 1.10x slower                                                           |
| unpickle_pure_python | 221 us                                                 | 244 us: 1.11x slower                                                             |
| xml_etree_generate   | 85.2 ms                                                | 96.6 ms: 1.13x slower                                                            |
| json_loads           | 26.5 us                                                | 30.4 us: 1.15x slower                                                            |
| xml_etree_process    | 59.0 ms                                                | 69.0 ms: 1.17x slower                                                            |
| pickle_pure_python   | 308 us                                                 | 370 us: 1.20x slower                                                             |
| json_dumps           | 10.4 ms                                                | 12.9 ms: 1.24x slower                                                            |
| Geometric mean       | (ref)                                                  | 1.10x slower                                                                     |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.53 ms: 1.33x slower                                                            |
| python_startup         | 9.93 ms                                                | 15.2 ms: 1.53x slower                                                            |
| Geometric mean         | (ref)                                                  | 1.43x slower                                                                     |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 59.2 ms: 1.18x slower                                                            |
| genshi_text     | 22.8 ms                                                | 27.5 ms: 1.20x slower                                                            |
| django_template | 34.7 ms                                                | 44.3 ms: 1.28x slower                                                            |
| mako            | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                            |
| Geometric mean  | (ref)                                                  | 1.27x slower                                                                     |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 582 ms: 1.91x faster                                                             |
| async_tree_none_tg         | 446 ms                                                 | 250 ms: 1.78x faster                                                             |
| async_tree_io              | 1.08 sec                                               | 614 ms: 1.76x faster                                                             |
| async_tree_memoization_tg  | 560 ms                                                 | 321 ms: 1.74x faster                                                             |
| async_tree_none            | 464 ms                                                 | 289 ms: 1.61x faster                                                             |
| async_tree_memoization     | 555 ms                                                 | 354 ms: 1.57x faster                                                             |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 554 ms: 1.30x faster                                                             |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 584 ms: 1.23x faster                                                             |
| pathlib                    | 21.5 ms                                                | 18.6 ms: 1.16x faster                                                            |
| deepcopy                   | 352 us                                                 | 312 us: 1.13x faster                                                             |
| xml_etree_iterparse        | 96.7 ms                                                | 86.8 ms: 1.11x faster                                                            |
| regex_effbot               | 3.17 ms                                                | 2.89 ms: 1.10x faster                                                            |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                                             |
| float                      | 80.8 ms                                                | 74.7 ms: 1.08x faster                                                            |
| sqlite_synth               | 2.20 us                                                | 2.05 us: 1.08x faster                                                            |
| gc_traversal               | 3.46 ms                                                | 3.25 ms: 1.06x faster                                                            |
| deepcopy_memo              | 40.3 us                                                | 38.4 us: 1.05x faster                                                            |
| coroutines                 | 23.9 ms                                                | 22.9 ms: 1.05x faster                                                            |
| go                         | 139 ms                                                 | 134 ms: 1.04x faster                                                             |
| generators                 | 32.2 ms                                                | 31.1 ms: 1.04x faster                                                            |
| async_generators           | 384 ms                                                 | 372 ms: 1.03x faster                                                             |
| bpe_tokeniser              | 4.74 sec                                               | 4.71 sec: 1.01x faster                                                           |
| spectral_norm              | 110 ms                                                 | 111 ms: 1.01x slower                                                             |
| pycparser                  | 1.17 sec                                               | 1.18 sec: 1.01x slower                                                           |
| logging_silent             | 109 ns                                                 | 111 ns: 1.02x slower                                                             |
| scimark_sor                | 130 ms                                                 | 132 ms: 1.02x slower                                                             |
| dulwich_log                | 78.9 ms                                                | 81.2 ms: 1.03x slower                                                            |
| comprehensions             | 19.8 us                                                | 20.4 us: 1.03x slower                                                            |
| deepcopy_reduce            | 3.08 us                                                | 3.19 us: 1.04x slower                                                            |
| regex_compile              | 142 ms                                                 | 149 ms: 1.05x slower                                                             |
| json                       | 5.02 ms                                                | 5.28 ms: 1.05x slower                                                            |
| mdp                        | 2.42 sec                                               | 2.58 sec: 1.07x slower                                                           |
| raytrace                   | 299 ms                                                 | 321 ms: 1.07x slower                                                             |
| chaos                      | 62.8 ms                                                | 67.8 ms: 1.08x slower                                                            |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.08x slower                                                             |
| docutils                   | 2.64 sec                                               | 2.87 sec: 1.09x slower                                                           |
| pyflate                    | 448 ms                                                 | 487 ms: 1.09x slower                                                             |
| logging_simple             | 6.63 us                                                | 7.26 us: 1.09x slower                                                            |
| tomli_loads                | 2.11 sec                                               | 2.32 sec: 1.10x slower                                                           |
| html5lib                   | 63.6 ms                                                | 70.2 ms: 1.10x slower                                                            |
| unpickle_pure_python       | 221 us                                                 | 244 us: 1.11x slower                                                             |
| sqlalchemy_imperative      | 21.8 ms                                                | 24.2 ms: 1.11x slower                                                            |
| pprint_safe_repr           | 743 ms                                                 | 826 ms: 1.11x slower                                                             |
| pprint_pformat             | 1.52 sec                                               | 1.71 sec: 1.12x slower                                                           |
| sympy_sum                  | 166 ms                                                 | 186 ms: 1.12x slower                                                             |
| scimark_fft                | 342 ms                                                 | 385 ms: 1.13x slower                                                             |
| crypto_pyaes               | 76.6 ms                                                | 86.6 ms: 1.13x slower                                                            |
| xml_etree_generate         | 85.2 ms                                                | 96.6 ms: 1.13x slower                                                            |
| logging_format             | 7.35 us                                                | 8.36 us: 1.14x slower                                                            |
| sqlglot_parse              | 1.36 ms                                                | 1.55 ms: 1.14x slower                                                            |
| sqlalchemy_declarative     | 143 ms                                                 | 163 ms: 1.14x slower                                                             |
| sqlglot_normalize          | 107 ms                                                 | 122 ms: 1.14x slower                                                             |
| json_loads                 | 26.5 us                                                | 30.4 us: 1.15x slower                                                            |
| sympy_str                  | 292 ms                                                 | 334 ms: 1.15x slower                                                             |
| sqlglot_optimize           | 53.3 ms                                                | 61.3 ms: 1.15x slower                                                            |
| sqlglot_transpile          | 1.67 ms                                                | 1.93 ms: 1.15x slower                                                            |
| 2to3                       | 264 ms                                                 | 304 ms: 1.15x slower                                                             |
| thrift                     | 791 us                                                 | 916 us: 1.16x slower                                                             |
| hexiom                     | 6.17 ms                                                | 7.14 ms: 1.16x slower                                                            |
| regex_v8                   | 20.6 ms                                                | 23.9 ms: 1.16x slower                                                            |
| pidigits                   | 184 ms                                                 | 215 ms: 1.16x slower                                                             |
| scimark_monte_carlo        | 68.4 ms                                                | 79.8 ms: 1.17x slower                                                            |
| xml_etree_process          | 59.0 ms                                                | 69.0 ms: 1.17x slower                                                            |
| sympy_expand               | 468 ms                                                 | 548 ms: 1.17x slower                                                             |
| genshi_xml                 | 50.2 ms                                                | 59.2 ms: 1.18x slower                                                            |
| sympy_integrate            | 20.5 ms                                                | 24.3 ms: 1.18x slower                                                            |
| nqueens                    | 80.1 ms                                                | 95.7 ms: 1.20x slower                                                            |
| pickle_pure_python         | 308 us                                                 | 370 us: 1.20x slower                                                             |
| genshi_text                | 22.8 ms                                                | 27.5 ms: 1.20x slower                                                            |
| scimark_lu                 | 114 ms                                                 | 138 ms: 1.21x slower                                                             |
| create_gc_cycles           | 1.09 ms                                                | 1.33 ms: 1.22x slower                                                            |
| json_dumps                 | 10.4 ms                                                | 12.9 ms: 1.24x slower                                                            |
| typing_runtime_protocols   | 163 us                                                 | 203 us: 1.24x slower                                                             |
| meteor_contest             | 104 ms                                                 | 130 ms: 1.26x slower                                                             |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.60 ms: 1.28x slower                                                            |
| django_template            | 34.7 ms                                                | 44.3 ms: 1.28x slower                                                            |
| fannkuch                   | 372 ms                                                 | 476 ms: 1.28x slower                                                             |
| telco                      | 6.53 ms                                                | 8.47 ms: 1.30x slower                                                            |
| deltablue                  | 3.45 ms                                                | 4.56 ms: 1.32x slower                                                            |
| python_startup_no_site     | 7.16 ms                                                | 9.53 ms: 1.33x slower                                                            |
| richards                   | 45.9 ms                                                | 62.2 ms: 1.35x slower                                                            |
| richards_super             | 51.9 ms                                                | 71.6 ms: 1.38x slower                                                            |
| coverage                   | 71.4 ms                                                | 98.9 ms: 1.38x slower                                                            |
| mako                       | 11.0 ms                                                | 15.6 ms: 1.42x slower                                                            |
| nbody                      | 89.3 ms                                                | 131 ms: 1.47x slower                                                             |
| python_startup             | 9.93 ms                                                | 15.2 ms: 1.53x slower                                                            |
| bench_thread_pool          | 941 us                                                 | 3.30 ms: 3.50x slower                                                            |
| bench_mp_pool              | 10.8 ms                                                | 94.2 ms: 8.72x slower                                                            |
| Geometric mean             | (ref)                                                  | 1.10x slower                                                                     |

Benchmark hidden because not significant (2): asyncio_websockets, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250123-3.14.0a4+-584015a-NOGIL/bm-20250123-vultr-x86_64-faster%2dcpython-remove_most_conditio-3.14.0a4+-584015a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.057x slower

# HPT report

- Reliability score: 99.97% likely to be slow
- 90% likely to have a slowdown of 1.07x
- 95% likely to have a slowdown of 1.05x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.35x