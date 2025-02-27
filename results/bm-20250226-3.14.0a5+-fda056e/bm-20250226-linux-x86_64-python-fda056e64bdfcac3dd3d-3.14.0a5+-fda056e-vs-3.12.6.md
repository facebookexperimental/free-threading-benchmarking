# Results vs. 3.12.6

- fork: python
- ref: fda056e64bdfcac3dd3d
- machine: linux-x86_64
- commit hash: fda056e
- commit date: 2025-02-26
- overall geometric mean: 1.116x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.14x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 434 ms: 1.05x faster                                                   |
| docutils       | 4.00 sec                                               | 3.68 sec: 1.08x faster                                                 |
| html5lib       | 88.9 ms                                                | 84.0 ms: 1.06x faster                                                  |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.85 sec                                               | 842 ms: 2.20x faster                                                   |
| async_tree_io_tg           | 1.93 sec                                               | 887 ms: 2.18x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 476 ms: 2.05x faster                                                   |
| async_tree_none            | 741 ms                                                 | 379 ms: 1.96x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 485 ms: 1.92x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 434 ms: 1.62x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 680 ms: 1.62x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 687 ms: 1.57x faster                                                   |
| async_generators           | 589 ms                                                 | 504 ms: 1.17x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 725 ms: 1.03x faster                                                   |
| coroutines                 | 29.5 ms                                                | 30.8 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.60x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 98.7 ms: 1.25x faster                                                  |
| pidigits       | 250 ms                                                 | 229 ms: 1.09x faster                                                   |
| Geometric mean | (ref)                                                  | 1.10x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.03 ms: 1.27x faster                                                  |
| regex_compile  | 187 ms                                                 | 160 ms: 1.16x faster                                                   |
| Geometric mean | (ref)                                                  | 1.11x faster                                                           |

Benchmark hidden because not significant (2): regex_v8, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads         | 2.88 sec                                               | 2.57 sec: 1.12x faster                                                 |
| xml_etree_generate  | 127 ms                                                 | 116 ms: 1.10x faster                                                   |
| xml_etree_parse     | 241 ms                                                 | 222 ms: 1.09x faster                                                   |
| xml_etree_iterparse | 169 ms                                                 | 157 ms: 1.08x faster                                                   |
| json_dumps          | 14.3 ms                                                | 15.1 ms: 1.05x slower                                                  |
| Geometric mean      | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (4): pickle_pure_python, json_loads, xml_etree_process, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 15.8 ms: 1.12x faster                                                  |
| python_startup         | 23.7 ms                                                | 27.4 ms: 1.16x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.02x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 30.2 ms                                                | 27.2 ms: 1.11x faster                                                  |
| mako            | 15.7 ms                                                | 15.0 ms: 1.05x faster                                                  |
| django_template | 44.9 ms                                                | 48.4 ms: 1.08x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.85 sec                                               | 842 ms: 2.20x faster                                                   |
| async_tree_io_tg           | 1.93 sec                                               | 887 ms: 2.18x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 476 ms: 2.05x faster                                                   |
| async_tree_none            | 741 ms                                                 | 379 ms: 1.96x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 485 ms: 1.92x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 434 ms: 1.62x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 680 ms: 1.62x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 687 ms: 1.57x faster                                                   |
| deepcopy_memo              | 52.4 us                                                | 36.8 us: 1.42x faster                                                  |
| deepcopy                   | 468 us                                                 | 329 us: 1.42x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.03 ms: 1.27x faster                                                  |
| float                      | 123 ms                                                 | 98.7 ms: 1.25x faster                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 175 ms: 1.24x faster                                                   |
| spectral_norm              | 156 ms                                                 | 127 ms: 1.23x faster                                                   |
| comprehensions             | 27.1 us                                                | 22.1 us: 1.22x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.47 sec: 1.22x faster                                                 |
| scimark_fft                | 500 ms                                                 | 418 ms: 1.20x faster                                                   |
| pylint                     | 465 ms                                                 | 389 ms: 1.20x faster                                                   |
| sqlalchemy_imperative      | 24.7 ms                                                | 20.8 ms: 1.19x faster                                                  |
| sqlglot_normalize          | 157 ms                                                 | 132 ms: 1.19x faster                                                   |
| go                         | 172 ms                                                 | 145 ms: 1.18x faster                                                   |
| pyflate                    | 727 ms                                                 | 616 ms: 1.18x faster                                                   |
| raytrace                   | 408 ms                                                 | 347 ms: 1.17x faster                                                   |
| async_generators           | 589 ms                                                 | 504 ms: 1.17x faster                                                   |
| regex_compile              | 187 ms                                                 | 160 ms: 1.16x faster                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 83.2 ms: 1.16x faster                                                  |
| logging_simple             | 9.45 us                                                | 8.22 us: 1.15x faster                                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.57 us: 1.13x faster                                                  |
| tomli_loads                | 2.88 sec                                               | 2.57 sec: 1.12x faster                                                 |
| sympy_sum                  | 222 ms                                                 | 198 ms: 1.12x faster                                                   |
| python_startup_no_site     | 17.6 ms                                                | 15.8 ms: 1.12x faster                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 5.93 sec: 1.11x faster                                                 |
| genshi_text                | 30.2 ms                                                | 27.2 ms: 1.11x faster                                                  |
| crypto_pyaes               | 107 ms                                                 | 97.3 ms: 1.10x faster                                                  |
| sympy_str                  | 385 ms                                                 | 349 ms: 1.10x faster                                                   |
| nqueens                    | 117 ms                                                 | 106 ms: 1.10x faster                                                   |
| xml_etree_generate         | 127 ms                                                 | 116 ms: 1.10x faster                                                   |
| richards_super             | 72.8 ms                                                | 66.6 ms: 1.09x faster                                                  |
| mdp                        | 3.97 sec                                               | 3.64 sec: 1.09x faster                                                 |
| pidigits                   | 250 ms                                                 | 229 ms: 1.09x faster                                                   |
| bench_thread_pool          | 3.48 ms                                                | 3.20 ms: 1.09x faster                                                  |
| xml_etree_parse            | 241 ms                                                 | 222 ms: 1.09x faster                                                   |
| docutils                   | 4.00 sec                                               | 3.68 sec: 1.08x faster                                                 |
| sympy_integrate            | 29.8 ms                                                | 27.5 ms: 1.08x faster                                                  |
| meteor_contest             | 146 ms                                                 | 135 ms: 1.08x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 157 ms: 1.08x faster                                                   |
| chaos                      | 84.9 ms                                                | 78.9 ms: 1.07x faster                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.25 ms: 1.07x faster                                                  |
| sqlglot_optimize           | 76.0 ms                                                | 71.2 ms: 1.07x faster                                                  |
| thrift                     | 1.06 ms                                                | 998 us: 1.06x faster                                                   |
| fannkuch                   | 540 ms                                                 | 509 ms: 1.06x faster                                                   |
| pprint_pformat             | 1.98 sec                                               | 1.87 sec: 1.06x faster                                                 |
| sqlite_synth               | 3.87 us                                                | 3.66 us: 1.06x faster                                                  |
| html5lib                   | 88.9 ms                                                | 84.0 ms: 1.06x faster                                                  |
| typing_runtime_protocols   | 224 us                                                 | 213 us: 1.05x faster                                                   |
| 2to3                       | 456 ms                                                 | 434 ms: 1.05x faster                                                   |
| pathlib                    | 31.6 ms                                                | 30.1 ms: 1.05x faster                                                  |
| richards                   | 60.3 ms                                                | 57.7 ms: 1.05x faster                                                  |
| mako                       | 15.7 ms                                                | 15.0 ms: 1.05x faster                                                  |
| scimark_sor                | 167 ms                                                 | 160 ms: 1.04x faster                                                   |
| generators                 | 41.1 ms                                                | 39.6 ms: 1.04x faster                                                  |
| asyncio_websockets         | 748 ms                                                 | 725 ms: 1.03x faster                                                   |
| coroutines                 | 29.5 ms                                                | 30.8 ms: 1.05x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 15.1 ms: 1.05x slower                                                  |
| django_template            | 44.9 ms                                                | 48.4 ms: 1.08x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 168 ms: 1.10x slower                                                   |
| telco                      | 9.59 ms                                                | 11.0 ms: 1.15x slower                                                  |
| json                       | 6.85 ms                                                | 7.89 ms: 1.15x slower                                                  |
| python_startup             | 23.7 ms                                                | 27.4 ms: 1.16x slower                                                  |
| coverage                   | 95.4 ms                                                | 114 ms: 1.20x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 8.25 ms: 1.41x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 4.00 ms: 2.06x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 94.4 ms: 4.56x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.09x faster                                                           |

Benchmark hidden because not significant (17): sqlglot_transpile, regex_v8, dulwich_log, logging_silent, pickle_pure_python, pprint_safe_repr, deltablue, json_loads, sqlglot_parse, xml_etree_process, genshi_xml, hexiom, nbody, logging_format, unpickle_pure_python, regex_dna, sympy_expand
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250226-3.14.0a5+-fda056e/bm-20250226-linux-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.116x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.07x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.14x