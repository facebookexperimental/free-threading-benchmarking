# Results vs. 3.12.6

- fork: mpage
- ref: gh_115999_integrate
- machine: linux-x86_64
- commit hash: b7e9a16
- commit date: 2024-12-13
- overall geometric mean: 1.043x slower
- HPT reliability: 99.95%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 531 ms: 1.16x slower                                                 |
| docutils       | 4.00 sec                                               | 4.14 sec: 1.04x slower                                               |
| html5lib       | 88.9 ms                                                | 101 ms: 1.14x slower                                                 |
| Geometric mean | (ref)                                                  | 1.11x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 764 ms: 2.53x faster                                                 |
| async_tree_none_tg         | 704 ms                                                 | 315 ms: 2.24x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 828 ms: 2.23x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 462 ms: 2.01x faster                                                 |
| async_tree_none            | 741 ms                                                 | 406 ms: 1.83x faster                                                 |
| async_tree_memoization     | 977 ms                                                 | 536 ms: 1.82x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 637 ms: 1.73x faster                                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 718 ms: 1.50x faster                                                 |
| coroutines                 | 29.5 ms                                                | 31.9 ms: 1.08x slower                                                |
| Geometric mean             | (ref)                                                  | 1.62x faster                                                         |

Benchmark hidden because not significant (2): asyncio_websockets, async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| float          | 123 ms                                                 | 110 ms: 1.12x faster                                                 |
| nbody          | 119 ms                                                 | 174 ms: 1.46x slower                                                 |
| Geometric mean | (ref)                                                  | 1.08x slower                                                         |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.15 ms: 1.24x faster                                                |
| regex_compile  | 187 ms                                                 | 209 ms: 1.12x slower                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                         |

Benchmark hidden because not significant (2): regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 135 ms: 1.26x faster                                                 |
| xml_etree_parse      | 241 ms                                                 | 209 ms: 1.15x faster                                                 |
| tomli_loads          | 2.88 sec                                               | 3.02 sec: 1.05x slower                                               |
| unpickle_pure_python | 300 us                                                 | 328 us: 1.09x slower                                                 |
| pickle_pure_python   | 436 us                                                 | 486 us: 1.12x slower                                                 |
| xml_etree_process    | 83.7 ms                                                | 97.6 ms: 1.17x slower                                                |
| json_dumps           | 14.3 ms                                                | 16.9 ms: 1.18x slower                                                |
| Geometric mean       | (ref)                                                  | 1.02x slower                                                         |

Benchmark hidden because not significant (2): json_loads, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 19.9 ms: 1.13x slower                                                |
| python_startup         | 23.7 ms                                                | 31.4 ms: 1.33x slower                                                |
| Geometric mean         | (ref)                                                  | 1.23x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|-----------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 51.7 ms: 1.15x slower                                                |
| genshi_text     | 30.2 ms                                                | 36.3 ms: 1.20x slower                                                |
| genshi_xml      | 67.6 ms                                                | 81.5 ms: 1.21x slower                                                |
| mako            | 15.7 ms                                                | 23.7 ms: 1.51x slower                                                |
| Geometric mean  | (ref)                                                  | 1.26x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 764 ms: 2.53x faster                                                 |
| async_tree_none_tg         | 704 ms                                                 | 315 ms: 2.24x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 828 ms: 2.23x faster                                                 |
| async_tree_memoization_tg  | 930 ms                                                 | 462 ms: 2.01x faster                                                 |
| async_tree_none            | 741 ms                                                 | 406 ms: 1.83x faster                                                 |
| async_tree_memoization     | 977 ms                                                 | 536 ms: 1.82x faster                                                 |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 637 ms: 1.73x faster                                                 |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 718 ms: 1.50x faster                                                 |
| xml_etree_iterparse        | 169 ms                                                 | 135 ms: 1.26x faster                                                 |
| regex_effbot               | 5.13 ms                                                | 4.15 ms: 1.24x faster                                                |
| xml_etree_parse            | 241 ms                                                 | 209 ms: 1.15x faster                                                 |
| deepcopy                   | 468 us                                                 | 415 us: 1.13x faster                                                 |
| float                      | 123 ms                                                 | 110 ms: 1.12x faster                                                 |
| pathlib                    | 31.6 ms                                                | 28.4 ms: 1.11x faster                                                |
| pycparser                  | 1.79 sec                                               | 1.70 sec: 1.06x faster                                               |
| sqlite_synth               | 3.87 us                                                | 3.71 us: 1.04x faster                                                |
| generators                 | 41.1 ms                                                | 42.5 ms: 1.03x slower                                                |
| docutils                   | 4.00 sec                                               | 4.14 sec: 1.04x slower                                               |
| mdp                        | 3.97 sec                                               | 4.13 sec: 1.04x slower                                               |
| tomli_loads                | 2.88 sec                                               | 3.02 sec: 1.05x slower                                               |
| deepcopy_reduce            | 4.04 us                                                | 4.24 us: 1.05x slower                                                |
| sqlglot_optimize           | 76.0 ms                                                | 80.2 ms: 1.06x slower                                                |
| dulwich_log                | 100 ms                                                 | 107 ms: 1.06x slower                                                 |
| raytrace                   | 408 ms                                                 | 435 ms: 1.07x slower                                                 |
| scimark_fft                | 500 ms                                                 | 535 ms: 1.07x slower                                                 |
| logging_silent             | 139 ns                                                 | 149 ns: 1.07x slower                                                 |
| nqueens                    | 117 ms                                                 | 125 ms: 1.07x slower                                                 |
| go                         | 172 ms                                                 | 185 ms: 1.07x slower                                                 |
| coroutines                 | 29.5 ms                                                | 31.9 ms: 1.08x slower                                                |
| unpickle_pure_python       | 300 us                                                 | 328 us: 1.09x slower                                                 |
| sqlalchemy_declarative     | 218 ms                                                 | 240 ms: 1.10x slower                                                 |
| bpe_tokeniser              | 6.59 sec                                               | 7.32 sec: 1.11x slower                                               |
| pickle_pure_python         | 436 us                                                 | 486 us: 1.12x slower                                                 |
| scimark_sor                | 167 ms                                                 | 186 ms: 1.12x slower                                                 |
| regex_compile              | 187 ms                                                 | 209 ms: 1.12x slower                                                 |
| crypto_pyaes               | 107 ms                                                 | 121 ms: 1.13x slower                                                 |
| python_startup_no_site     | 17.6 ms                                                | 19.9 ms: 1.13x slower                                                |
| scimark_monte_carlo        | 96.4 ms                                                | 110 ms: 1.14x slower                                                 |
| html5lib                   | 88.9 ms                                                | 101 ms: 1.14x slower                                                 |
| sqlglot_transpile          | 2.34 ms                                                | 2.66 ms: 1.14x slower                                                |
| meteor_contest             | 146 ms                                                 | 167 ms: 1.14x slower                                                 |
| logging_format             | 9.59 us                                                | 11.0 us: 1.15x slower                                                |
| django_template            | 44.9 ms                                                | 51.7 ms: 1.15x slower                                                |
| gc_traversal               | 5.86 ms                                                | 6.76 ms: 1.15x slower                                                |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 7.75 ms: 1.16x slower                                                |
| 2to3                       | 456 ms                                                 | 531 ms: 1.16x slower                                                 |
| xml_etree_process          | 83.7 ms                                                | 97.6 ms: 1.17x slower                                                |
| pprint_pformat             | 1.98 sec                                               | 2.31 sec: 1.17x slower                                               |
| pprint_safe_repr           | 967 ms                                                 | 1.13 sec: 1.17x slower                                               |
| richards_super             | 72.8 ms                                                | 85.5 ms: 1.17x slower                                                |
| fannkuch                   | 540 ms                                                 | 636 ms: 1.18x slower                                                 |
| json_dumps                 | 14.3 ms                                                | 16.9 ms: 1.18x slower                                                |
| richards                   | 60.3 ms                                                | 71.8 ms: 1.19x slower                                                |
| genshi_text                | 30.2 ms                                                | 36.3 ms: 1.20x slower                                                |
| genshi_xml                 | 67.6 ms                                                | 81.5 ms: 1.21x slower                                                |
| typing_runtime_protocols   | 224 us                                                 | 273 us: 1.22x slower                                                 |
| chaos                      | 84.9 ms                                                | 105 ms: 1.24x slower                                                 |
| hexiom                     | 8.27 ms                                                | 10.2 ms: 1.24x slower                                                |
| thrift                     | 1.06 ms                                                | 1.33 ms: 1.26x slower                                                |
| sqlglot_parse              | 1.79 ms                                                | 2.27 ms: 1.27x slower                                                |
| sympy_integrate            | 29.8 ms                                                | 38.0 ms: 1.28x slower                                                |
| telco                      | 9.59 ms                                                | 12.5 ms: 1.31x slower                                                |
| python_startup             | 23.7 ms                                                | 31.4 ms: 1.33x slower                                                |
| coverage                   | 95.4 ms                                                | 126 ms: 1.33x slower                                                 |
| sqlalchemy_imperative      | 24.7 ms                                                | 32.9 ms: 1.33x slower                                                |
| scimark_lu                 | 152 ms                                                 | 203 ms: 1.33x slower                                                 |
| nbody                      | 119 ms                                                 | 174 ms: 1.46x slower                                                 |
| sympy_str                  | 385 ms                                                 | 565 ms: 1.47x slower                                                 |
| deltablue                  | 4.27 ms                                                | 6.28 ms: 1.47x slower                                                |
| mako                       | 15.7 ms                                                | 23.7 ms: 1.51x slower                                                |
| create_gc_cycles           | 1.94 ms                                                | 3.26 ms: 1.68x slower                                                |
| sympy_sum                  | 222 ms                                                 | 395 ms: 1.78x slower                                                 |
| sympy_expand               | 582 ms                                                 | 1.08 sec: 1.85x slower                                               |
| bench_mp_pool              | 20.7 ms                                                | 88.8 ms: 4.29x slower                                                |
| Geometric mean             | (ref)                                                  | 1.06x slower                                                         |

Benchmark hidden because not significant (16): json_loads, logging_simple, pidigits, comprehensions, asyncio_websockets, spectral_norm, sqlglot_normalize, json, deepcopy_memo, regex_v8, regex_dna, pyflate, async_generators, xml_etree_generate, bench_thread_pool, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241213-3.14.0a2+-b7e9a16-NOGIL/bm-20241213-linux-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.043x slower

# HPT report

- Reliability score: 99.95% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.03x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.34x