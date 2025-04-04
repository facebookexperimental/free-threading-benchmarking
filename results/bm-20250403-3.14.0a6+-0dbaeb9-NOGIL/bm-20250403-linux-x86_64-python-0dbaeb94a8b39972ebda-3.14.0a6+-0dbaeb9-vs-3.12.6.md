# Results vs. 3.12.6

- fork: python
- ref: 0dbaeb94a8b39972ebda
- machine: linux-x86_64
- commit hash: 0dbaeb9
- commit date: 2025-04-03
- overall geometric mean: 1.010x faster
- HPT reliability: 88.91%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 527 ms: 1.15x slower                                                   |
| html5lib       | 88.9 ms                                                | 105 ms: 1.18x slower                                                   |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 710 ms: 2.72x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 789 ms: 2.34x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 319 ms: 2.21x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 431 ms: 2.16x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 475 ms: 2.05x faster                                                   |
| async_tree_none            | 741 ms                                                 | 383 ms: 1.94x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 646 ms: 1.70x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 691 ms: 1.56x faster                                                   |
| coroutines                 | 29.5 ms                                                | 35.2 ms: 1.19x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.67x faster                                                           |

Benchmark hidden because not significant (2): asyncio_websockets, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 96.0 ms: 1.28x faster                                                  |
| nbody          | 119 ms                                                 | 159 ms: 1.34x slower                                                   |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.39 ms: 1.17x faster                                                  |
| regex_v8       | 32.5 ms                                                | 29.6 ms: 1.10x faster                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (2): regex_compile, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse | 169 ms                                                 | 144 ms: 1.17x faster                                                   |
| xml_etree_parse     | 241 ms                                                 | 223 ms: 1.08x faster                                                   |
| xml_etree_generate  | 127 ms                                                 | 140 ms: 1.10x slower                                                   |
| xml_etree_process   | 83.7 ms                                                | 95.0 ms: 1.14x slower                                                  |
| json_dumps          | 14.3 ms                                                | 17.0 ms: 1.19x slower                                                  |
| json_loads          | 37.9 us                                                | 47.4 us: 1.25x slower                                                  |
| Geometric mean      | (ref)                                                  | 1.04x slower                                                           |

Benchmark hidden because not significant (3): pickle_pure_python, tomli_loads, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 26.2 ms: 1.49x slower                                                  |
| python_startup         | 23.7 ms                                                | 40.9 ms: 1.72x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.60x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 50.5 ms: 1.12x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 83.9 ms: 1.24x slower                                                  |
| genshi_text     | 30.2 ms                                                | 41.3 ms: 1.37x slower                                                  |
| mako            | 15.7 ms                                                | 25.7 ms: 1.63x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.33x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 710 ms: 2.72x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 789 ms: 2.34x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 319 ms: 2.21x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 431 ms: 2.16x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 475 ms: 2.05x faster                                                   |
| async_tree_none            | 741 ms                                                 | 383 ms: 1.94x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 646 ms: 1.70x faster                                                   |
| mdp                        | 3.97 sec                                               | 2.46 sec: 1.61x faster                                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 691 ms: 1.56x faster                                                   |
| gc_traversal               | 5.86 ms                                                | 4.15 ms: 1.41x faster                                                  |
| float                      | 123 ms                                                 | 96.0 ms: 1.28x faster                                                  |
| deepcopy                   | 468 us                                                 | 368 us: 1.27x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 42.8 us: 1.22x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.52 sec: 1.18x faster                                                 |
| xml_etree_iterparse        | 169 ms                                                 | 144 ms: 1.17x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.39 ms: 1.17x faster                                                  |
| regex_v8                   | 32.5 ms                                                | 29.6 ms: 1.10x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 223 ms: 1.08x faster                                                   |
| sqlite_synth               | 3.87 us                                                | 3.62 us: 1.07x faster                                                  |
| pathlib                    | 31.6 ms                                                | 29.7 ms: 1.07x faster                                                  |
| richards_super             | 72.8 ms                                                | 76.2 ms: 1.05x slower                                                  |
| json                       | 6.85 ms                                                | 7.22 ms: 1.05x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.03 sec: 1.06x slower                                                 |
| logging_simple             | 9.45 us                                                | 10.0 us: 1.06x slower                                                  |
| deepcopy_reduce            | 4.04 us                                                | 4.30 us: 1.07x slower                                                  |
| chaos                      | 84.9 ms                                                | 91.0 ms: 1.07x slower                                                  |
| comprehensions             | 27.1 us                                                | 29.1 us: 1.07x slower                                                  |
| generators                 | 41.1 ms                                                | 44.3 ms: 1.08x slower                                                  |
| richards                   | 60.3 ms                                                | 65.3 ms: 1.08x slower                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 105 ms: 1.09x slower                                                   |
| xml_etree_generate         | 127 ms                                                 | 140 ms: 1.10x slower                                                   |
| pprint_pformat             | 1.98 sec                                               | 2.21 sec: 1.12x slower                                                 |
| sympy_sum                  | 222 ms                                                 | 248 ms: 1.12x slower                                                   |
| django_template            | 44.9 ms                                                | 50.5 ms: 1.12x slower                                                  |
| deltablue                  | 4.27 ms                                                | 4.84 ms: 1.13x slower                                                  |
| xml_etree_process          | 83.7 ms                                                | 95.0 ms: 1.14x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 173 ms: 1.14x slower                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 7.70 ms: 1.15x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 259 us: 1.15x slower                                                   |
| 2to3                       | 456 ms                                                 | 527 ms: 1.15x slower                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 7.61 sec: 1.16x slower                                                 |
| dulwich_log                | 100 ms                                                 | 116 ms: 1.16x slower                                                   |
| logging_format             | 9.59 us                                                | 11.1 us: 1.16x slower                                                  |
| sympy_integrate            | 29.8 ms                                                | 34.6 ms: 1.16x slower                                                  |
| fannkuch                   | 540 ms                                                 | 636 ms: 1.18x slower                                                   |
| html5lib                   | 88.9 ms                                                | 105 ms: 1.18x slower                                                   |
| sympy_expand               | 582 ms                                                 | 689 ms: 1.18x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 17.0 ms: 1.19x slower                                                  |
| hexiom                     | 8.27 ms                                                | 9.86 ms: 1.19x slower                                                  |
| coroutines                 | 29.5 ms                                                | 35.2 ms: 1.19x slower                                                  |
| sympy_str                  | 385 ms                                                 | 466 ms: 1.21x slower                                                   |
| telco                      | 9.59 ms                                                | 11.7 ms: 1.22x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 83.9 ms: 1.24x slower                                                  |
| json_loads                 | 37.9 us                                                | 47.4 us: 1.25x slower                                                  |
| meteor_contest             | 146 ms                                                 | 185 ms: 1.26x slower                                                   |
| crypto_pyaes               | 107 ms                                                 | 138 ms: 1.29x slower                                                   |
| nbody                      | 119 ms                                                 | 159 ms: 1.34x slower                                                   |
| genshi_text                | 30.2 ms                                                | 41.3 ms: 1.37x slower                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 33.9 ms: 1.37x slower                                                  |
| python_startup_no_site     | 17.6 ms                                                | 26.2 ms: 1.49x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 2.97 ms: 1.53x slower                                                  |
| bench_thread_pool          | 3.48 ms                                                | 5.34 ms: 1.53x slower                                                  |
| mako                       | 15.7 ms                                                | 25.7 ms: 1.63x slower                                                  |
| coverage                   | 95.4 ms                                                | 158 ms: 1.66x slower                                                   |
| python_startup             | 23.7 ms                                                | 40.9 ms: 1.72x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 94.3 ms: 4.56x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (19): spectral_norm, logging_silent, scimark_fft, asyncio_websockets, go, async_generators, regex_compile, pylint, pidigits, raytrace, pickle_pure_python, tomli_loads, scimark_sor, unpickle_pure_python, pyflate, nqueens, regex_dna, docutils, sqlalchemy_declarative
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, thrift, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250403-3.14.0a6+-0dbaeb9-NOGIL/bm-20250403-linux-x86_64-python-0dbaeb94a8b39972ebda-3.14.0a6+-0dbaeb9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.010x faster

# HPT report

- Reliability score: 88.91% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x