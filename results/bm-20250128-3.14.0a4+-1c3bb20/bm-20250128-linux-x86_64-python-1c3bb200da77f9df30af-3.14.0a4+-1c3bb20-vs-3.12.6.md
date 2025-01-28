# Results vs. 3.12.6

- fork: python
- ref: 1c3bb200da77f9df30af
- machine: linux-x86_64
- commit hash: 1c3bb20
- commit date: 2025-01-28
- overall geometric mean: 1.074x faster
- HPT reliability: 99.96%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.13x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 489 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (2): docutils, html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 969 ms: 2.00x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 954 ms: 1.94x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 509 ms: 1.92x faster                                                   |
| async_tree_none            | 741 ms                                                 | 392 ms: 1.89x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 494 ms: 1.88x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 407 ms: 1.73x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 708 ms: 1.55x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 738 ms: 1.46x faster                                                   |
| async_generators           | 589 ms                                                 | 537 ms: 1.10x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 722 ms: 1.04x faster                                                   |
| coroutines                 | 29.5 ms                                                | 34.9 ms: 1.18x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.52x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 110 ms: 1.12x faster                                                   |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmark hidden because not significant (2): nbody, pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.11 ms: 1.25x faster                                                  |
| regex_compile  | 187 ms                                                 | 173 ms: 1.08x faster                                                   |
| regex_v8       | 32.5 ms                                                | 39.6 ms: 1.22x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse     | 241 ms                                                 | 213 ms: 1.13x faster                                                   |
| xml_etree_iterparse | 169 ms                                                 | 157 ms: 1.08x faster                                                   |
| xml_etree_generate  | 127 ms                                                 | 119 ms: 1.07x faster                                                   |
| tomli_loads         | 2.88 sec                                               | 2.73 sec: 1.05x faster                                                 |
| pickle_pure_python  | 436 us                                                 | 467 us: 1.07x slower                                                   |
| Geometric mean      | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (4): unpickle_pure_python, json_loads, xml_etree_process, json_dumps

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 16.3 ms: 1.08x faster                                                  |
| python_startup         | 23.7 ms                                                | 27.4 ms: 1.15x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 30.2 ms                                                | 27.4 ms: 1.10x faster                                                  |
| django_template | 44.9 ms                                                | 46.8 ms: 1.04x slower                                                  |
| mako            | 15.7 ms                                                | 17.9 ms: 1.14x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 969 ms: 2.00x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 954 ms: 1.94x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 509 ms: 1.92x faster                                                   |
| async_tree_none            | 741 ms                                                 | 392 ms: 1.89x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 494 ms: 1.88x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 407 ms: 1.73x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 708 ms: 1.55x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 738 ms: 1.46x faster                                                   |
| deepcopy                   | 468 us                                                 | 327 us: 1.43x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.11 ms: 1.25x faster                                                  |
| deepcopy_memo              | 52.4 us                                                | 43.0 us: 1.22x faster                                                  |
| pylint                     | 465 ms                                                 | 393 ms: 1.18x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.54 sec: 1.16x faster                                                 |
| sympy_sum                  | 222 ms                                                 | 191 ms: 1.16x faster                                                   |
| logging_simple             | 9.45 us                                                | 8.14 us: 1.16x faster                                                  |
| spectral_norm              | 156 ms                                                 | 135 ms: 1.15x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 213 ms: 1.13x faster                                                   |
| comprehensions             | 27.1 us                                                | 24.1 us: 1.13x faster                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 194 ms: 1.12x faster                                                   |
| pyflate                    | 727 ms                                                 | 649 ms: 1.12x faster                                                   |
| float                      | 123 ms                                                 | 110 ms: 1.12x faster                                                   |
| pathlib                    | 31.6 ms                                                | 28.6 ms: 1.11x faster                                                  |
| chaos                      | 84.9 ms                                                | 76.8 ms: 1.11x faster                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 6.06 ms: 1.10x faster                                                  |
| genshi_text                | 30.2 ms                                                | 27.4 ms: 1.10x faster                                                  |
| deepcopy_reduce            | 4.04 us                                                | 3.67 us: 1.10x faster                                                  |
| async_generators           | 589 ms                                                 | 537 ms: 1.10x faster                                                   |
| typing_runtime_protocols   | 224 us                                                 | 205 us: 1.10x faster                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 6.02 sec: 1.09x faster                                                 |
| scimark_sor                | 167 ms                                                 | 153 ms: 1.09x faster                                                   |
| thrift                     | 1.06 ms                                                | 975 us: 1.09x faster                                                   |
| crypto_pyaes               | 107 ms                                                 | 98.8 ms: 1.09x faster                                                  |
| nqueens                    | 117 ms                                                 | 108 ms: 1.08x faster                                                   |
| python_startup_no_site     | 17.6 ms                                                | 16.3 ms: 1.08x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 157 ms: 1.08x faster                                                   |
| dulwich_log                | 100 ms                                                 | 93.1 ms: 1.08x faster                                                  |
| regex_compile              | 187 ms                                                 | 173 ms: 1.08x faster                                                   |
| xml_etree_generate         | 127 ms                                                 | 119 ms: 1.07x faster                                                   |
| go                         | 172 ms                                                 | 162 ms: 1.06x faster                                                   |
| fannkuch                   | 540 ms                                                 | 509 ms: 1.06x faster                                                   |
| mdp                        | 3.97 sec                                               | 3.74 sec: 1.06x faster                                                 |
| tomli_loads                | 2.88 sec                                               | 2.73 sec: 1.05x faster                                                 |
| sqlglot_parse              | 1.79 ms                                                | 1.71 ms: 1.04x faster                                                  |
| pprint_safe_repr           | 967 ms                                                 | 927 ms: 1.04x faster                                                   |
| pprint_pformat             | 1.98 sec                                               | 1.90 sec: 1.04x faster                                                 |
| asyncio_websockets         | 748 ms                                                 | 722 ms: 1.04x faster                                                   |
| django_template            | 44.9 ms                                                | 46.8 ms: 1.04x slower                                                  |
| meteor_contest             | 146 ms                                                 | 154 ms: 1.05x slower                                                   |
| logging_silent             | 139 ns                                                 | 148 ns: 1.06x slower                                                   |
| deltablue                  | 4.27 ms                                                | 4.54 ms: 1.06x slower                                                  |
| 2to3                       | 456 ms                                                 | 489 ms: 1.07x slower                                                   |
| pickle_pure_python         | 436 us                                                 | 467 us: 1.07x slower                                                   |
| json                       | 6.85 ms                                                | 7.35 ms: 1.07x slower                                                  |
| sympy_str                  | 385 ms                                                 | 419 ms: 1.09x slower                                                   |
| generators                 | 41.1 ms                                                | 44.8 ms: 1.09x slower                                                  |
| sqlite_synth               | 3.87 us                                                | 4.28 us: 1.10x slower                                                  |
| scimark_lu                 | 152 ms                                                 | 172 ms: 1.13x slower                                                   |
| mako                       | 15.7 ms                                                | 17.9 ms: 1.14x slower                                                  |
| python_startup             | 23.7 ms                                                | 27.4 ms: 1.15x slower                                                  |
| sympy_expand               | 582 ms                                                 | 678 ms: 1.17x slower                                                   |
| coroutines                 | 29.5 ms                                                | 34.9 ms: 1.18x slower                                                  |
| regex_v8                   | 32.5 ms                                                | 39.6 ms: 1.22x slower                                                  |
| coverage                   | 95.4 ms                                                | 128 ms: 1.34x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 8.80 ms: 1.50x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 4.45 ms: 2.30x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 97.1 ms: 4.69x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.04x faster                                                           |

Benchmark hidden because not significant (24): logging_format, unpickle_pure_python, sqlglot_normalize, raytrace, json_loads, genshi_xml, nbody, richards_super, pidigits, html5lib, scimark_fft, xml_etree_process, sympy_integrate, docutils, sqlalchemy_imperative, scimark_monte_carlo, json_dumps, regex_dna, telco, hexiom, sqlglot_optimize, sqlglot_transpile, richards, bench_thread_pool
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250128-3.14.0a4+-1c3bb20/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.074x faster

# HPT report

- Reliability score: 99.96% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.13x