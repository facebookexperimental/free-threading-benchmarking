# Results vs. 3.12.6

- fork: python
- ref: 10ee2d9d3bcde27c75f1
- machine: linux-x86_64
- commit hash: 10ee2d9
- commit date: 2025-01-30
- overall geometric mean: 1.051x slower
- HPT reliability: 99.93%
- HPT 99th percentile: 1.03x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 555 ms: 1.22x slower                                                   |
| html5lib       | 88.9 ms                                                | 99.8 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 837 ms: 2.31x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 845 ms: 2.19x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 442 ms: 2.10x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 376 ms: 1.87x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 549 ms: 1.78x faster                                                   |
| async_tree_none            | 741 ms                                                 | 431 ms: 1.72x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 701 ms: 1.57x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 708 ms: 1.52x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 703 ms: 1.06x faster                                                   |
| coroutines                 | 29.5 ms                                                | 32.1 ms: 1.09x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.57x faster                                                           |

Benchmark hidden because not significant (1): async_generators

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 109 ms: 1.13x faster                                                   |
| nbody          | 119 ms                                                 | 186 ms: 1.56x slower                                                   |
| Geometric mean | (ref)                                                  | 1.10x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 278 ms                                                 | 293 ms: 1.05x slower                                                   |
| regex_compile  | 187 ms                                                 | 214 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (2): regex_effbot, regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 144 ms: 1.18x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 216 ms: 1.12x faster                                                   |
| pickle_pure_python   | 436 us                                                 | 464 us: 1.07x slower                                                   |
| tomli_loads          | 2.88 sec                                               | 3.09 sec: 1.07x slower                                                 |
| xml_etree_generate   | 127 ms                                                 | 145 ms: 1.14x slower                                                   |
| json_dumps           | 14.3 ms                                                | 16.6 ms: 1.16x slower                                                  |
| unpickle_pure_python | 300 us                                                 | 364 us: 1.22x slower                                                   |
| json_loads           | 37.9 us                                                | 46.9 us: 1.24x slower                                                  |
| xml_etree_process    | 83.7 ms                                                | 105 ms: 1.25x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.09x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 21.4 ms: 1.22x slower                                                  |
| python_startup         | 23.7 ms                                                | 33.7 ms: 1.42x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.31x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 56.2 ms: 1.25x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 86.5 ms: 1.28x slower                                                  |
| genshi_text     | 30.2 ms                                                | 39.8 ms: 1.32x slower                                                  |
| mako            | 15.7 ms                                                | 24.3 ms: 1.54x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.34x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 837 ms: 2.31x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 845 ms: 2.19x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 442 ms: 2.10x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 376 ms: 1.87x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 549 ms: 1.78x faster                                                   |
| async_tree_none            | 741 ms                                                 | 431 ms: 1.72x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 701 ms: 1.57x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 708 ms: 1.52x faster                                                   |
| gc_traversal               | 5.86 ms                                                | 4.01 ms: 1.46x faster                                                  |
| xml_etree_iterparse        | 169 ms                                                 | 144 ms: 1.18x faster                                                   |
| deepcopy                   | 468 us                                                 | 413 us: 1.13x faster                                                   |
| float                      | 123 ms                                                 | 109 ms: 1.13x faster                                                   |
| pycparser                  | 1.79 sec                                               | 1.60 sec: 1.12x faster                                                 |
| xml_etree_parse            | 241 ms                                                 | 216 ms: 1.12x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 703 ms: 1.06x faster                                                   |
| comprehensions             | 27.1 us                                                | 25.8 us: 1.05x faster                                                  |
| regex_dna                  | 278 ms                                                 | 293 ms: 1.05x slower                                                   |
| generators                 | 41.1 ms                                                | 43.6 ms: 1.06x slower                                                  |
| pickle_pure_python         | 436 us                                                 | 464 us: 1.07x slower                                                   |
| tomli_loads                | 2.88 sec                                               | 3.09 sec: 1.07x slower                                                 |
| logging_format             | 9.59 us                                                | 10.3 us: 1.07x slower                                                  |
| mdp                        | 3.97 sec                                               | 4.27 sec: 1.08x slower                                                 |
| pyflate                    | 727 ms                                                 | 782 ms: 1.08x slower                                                   |
| coroutines                 | 29.5 ms                                                | 32.1 ms: 1.09x slower                                                  |
| sqlalchemy_declarative     | 218 ms                                                 | 242 ms: 1.11x slower                                                   |
| scimark_fft                | 500 ms                                                 | 558 ms: 1.12x slower                                                   |
| sympy_str                  | 385 ms                                                 | 431 ms: 1.12x slower                                                   |
| html5lib                   | 88.9 ms                                                | 99.8 ms: 1.12x slower                                                  |
| raytrace                   | 408 ms                                                 | 461 ms: 1.13x slower                                                   |
| pprint_safe_repr           | 967 ms                                                 | 1.09 sec: 1.13x slower                                                 |
| bpe_tokeniser              | 6.59 sec                                               | 7.48 sec: 1.14x slower                                                 |
| xml_etree_generate         | 127 ms                                                 | 145 ms: 1.14x slower                                                   |
| go                         | 172 ms                                                 | 197 ms: 1.14x slower                                                   |
| regex_compile              | 187 ms                                                 | 214 ms: 1.15x slower                                                   |
| bench_thread_pool          | 3.48 ms                                                | 3.99 ms: 1.15x slower                                                  |
| logging_simple             | 9.45 us                                                | 10.9 us: 1.15x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.22 ms: 1.15x slower                                                  |
| chaos                      | 84.9 ms                                                | 97.6 ms: 1.15x slower                                                  |
| json_dumps                 | 14.3 ms                                                | 16.6 ms: 1.16x slower                                                  |
| sympy_sum                  | 222 ms                                                 | 257 ms: 1.16x slower                                                   |
| sqlglot_optimize           | 76.0 ms                                                | 88.7 ms: 1.17x slower                                                  |
| pprint_pformat             | 1.98 sec                                               | 2.31 sec: 1.17x slower                                                 |
| scimark_sor                | 167 ms                                                 | 196 ms: 1.18x slower                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 113 ms: 1.18x slower                                                   |
| scimark_lu                 | 152 ms                                                 | 182 ms: 1.19x slower                                                   |
| richards_super             | 72.8 ms                                                | 87.3 ms: 1.20x slower                                                  |
| hexiom                     | 8.27 ms                                                | 10.0 ms: 1.21x slower                                                  |
| sympy_integrate            | 29.8 ms                                                | 36.1 ms: 1.21x slower                                                  |
| 2to3                       | 456 ms                                                 | 555 ms: 1.22x slower                                                   |
| unpickle_pure_python       | 300 us                                                 | 364 us: 1.22x slower                                                   |
| python_startup_no_site     | 17.6 ms                                                | 21.4 ms: 1.22x slower                                                  |
| sympy_expand               | 582 ms                                                 | 709 ms: 1.22x slower                                                   |
| crypto_pyaes               | 107 ms                                                 | 132 ms: 1.23x slower                                                   |
| json_loads                 | 37.9 us                                                | 46.9 us: 1.24x slower                                                  |
| json                       | 6.85 ms                                                | 8.48 ms: 1.24x slower                                                  |
| logging_silent             | 139 ns                                                 | 173 ns: 1.24x slower                                                   |
| sqlglot_transpile          | 2.34 ms                                                | 2.91 ms: 1.24x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 2.23 ms: 1.25x slower                                                  |
| django_template            | 44.9 ms                                                | 56.2 ms: 1.25x slower                                                  |
| richards                   | 60.3 ms                                                | 75.7 ms: 1.25x slower                                                  |
| xml_etree_process          | 83.7 ms                                                | 105 ms: 1.25x slower                                                   |
| telco                      | 9.59 ms                                                | 12.1 ms: 1.26x slower                                                  |
| genshi_xml                 | 67.6 ms                                                | 86.5 ms: 1.28x slower                                                  |
| fannkuch                   | 540 ms                                                 | 710 ms: 1.31x slower                                                   |
| genshi_text                | 30.2 ms                                                | 39.8 ms: 1.32x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 301 us: 1.34x slower                                                   |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 9.20 ms: 1.37x slower                                                  |
| meteor_contest             | 146 ms                                                 | 206 ms: 1.41x slower                                                   |
| python_startup             | 23.7 ms                                                | 33.7 ms: 1.42x slower                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 36.4 ms: 1.47x slower                                                  |
| mako                       | 15.7 ms                                                | 24.3 ms: 1.54x slower                                                  |
| nbody                      | 119 ms                                                 | 186 ms: 1.56x slower                                                   |
| deltablue                  | 4.27 ms                                                | 6.68 ms: 1.56x slower                                                  |
| coverage                   | 95.4 ms                                                | 151 ms: 1.58x slower                                                   |
| create_gc_cycles           | 1.94 ms                                                | 3.12 ms: 1.61x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 94.9 ms: 4.59x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.08x slower                                                           |

Benchmark hidden because not significant (14): regex_effbot, pidigits, pathlib, async_generators, sqlite_synth, pylint, regex_v8, deepcopy_memo, deepcopy_reduce, docutils, spectral_norm, nqueens, sqlglot_normalize, dulwich_log
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250130-3.14.0a4+-10ee2d9-NOGIL/bm-20250130-linux-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.051x slower

# HPT report

- Reliability score: 99.93% likely to be slow
- 90% likely to have a slowdown of 1.05x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.03x

# Memory
- memory change: 1.35x