# Results vs. 3.12.6

- fork: python
- ref: 1c3bb200da77f9df30af
- machine: linux-x86_64
- commit hash: 1c3bb20
- commit date: 2025-01-28
- overall geometric mean: 1.100x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 550 ms: 1.21x slower                                                   |
| html5lib       | 88.9 ms                                                | 114 ms: 1.28x slower                                                   |
| Geometric mean | (ref)                                                  | 1.16x slower                                                           |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 859 ms: 2.25x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 897 ms: 2.06x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 351 ms: 2.01x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 563 ms: 1.74x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 542 ms: 1.72x faster                                                   |
| async_tree_none            | 741 ms                                                 | 448 ms: 1.65x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 697 ms: 1.58x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 794 ms: 1.36x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 776 ms: 1.04x slower                                                   |
| async_generators           | 589 ms                                                 | 618 ms: 1.05x slower                                                   |
| coroutines                 | 29.5 ms                                                | 34.9 ms: 1.18x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.48x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 110 ms: 1.12x faster                                                   |
| pidigits       | 250 ms                                                 | 241 ms: 1.04x faster                                                   |
| nbody          | 119 ms                                                 | 183 ms: 1.54x slower                                                   |
| Geometric mean | (ref)                                                  | 1.10x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.75 ms: 1.08x faster                                                  |
| regex_dna      | 278 ms                                                 | 293 ms: 1.05x slower                                                   |
| regex_v8       | 32.5 ms                                                | 37.5 ms: 1.15x slower                                                  |
| regex_compile  | 187 ms                                                 | 225 ms: 1.21x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.88 sec                                               | 3.15 sec: 1.09x slower                                                 |
| xml_etree_generate   | 127 ms                                                 | 140 ms: 1.10x slower                                                   |
| json_loads           | 37.9 us                                                | 43.1 us: 1.14x slower                                                  |
| pickle_pure_python   | 436 us                                                 | 505 us: 1.16x slower                                                   |
| unpickle_pure_python | 300 us                                                 | 376 us: 1.25x slower                                                   |
| xml_etree_process    | 83.7 ms                                                | 107 ms: 1.28x slower                                                   |
| json_dumps           | 14.3 ms                                                | 19.7 ms: 1.38x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.14x slower                                                           |

Benchmark hidden because not significant (2): xml_etree_iterparse, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 21.7 ms: 1.24x slower                                                  |
| python_startup         | 23.7 ms                                                | 31.9 ms: 1.35x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.29x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 30.2 ms                                                | 37.8 ms: 1.25x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 92.3 ms: 1.37x slower                                                  |
| django_template | 44.9 ms                                                | 62.4 ms: 1.39x slower                                                  |
| mako            | 15.7 ms                                                | 25.0 ms: 1.59x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.39x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 859 ms: 2.25x faster                                                   |
| async_tree_io              | 1.85 sec                                               | 897 ms: 2.06x faster                                                   |
| async_tree_none_tg         | 704 ms                                                 | 351 ms: 2.01x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 563 ms: 1.74x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 542 ms: 1.72x faster                                                   |
| async_tree_none            | 741 ms                                                 | 448 ms: 1.65x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 697 ms: 1.58x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 794 ms: 1.36x faster                                                   |
| float                      | 123 ms                                                 | 110 ms: 1.12x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.75 ms: 1.08x faster                                                  |
| pycparser                  | 1.79 sec                                               | 1.69 sec: 1.06x faster                                                 |
| sqlite_synth               | 3.87 us                                                | 3.65 us: 1.06x faster                                                  |
| pidigits                   | 250 ms                                                 | 241 ms: 1.04x faster                                                   |
| asyncio_websockets         | 748 ms                                                 | 776 ms: 1.04x slower                                                   |
| async_generators           | 589 ms                                                 | 618 ms: 1.05x slower                                                   |
| regex_dna                  | 278 ms                                                 | 293 ms: 1.05x slower                                                   |
| nqueens                    | 117 ms                                                 | 124 ms: 1.06x slower                                                   |
| mdp                        | 3.97 sec                                               | 4.26 sec: 1.07x slower                                                 |
| sympy_integrate            | 29.8 ms                                                | 31.9 ms: 1.07x slower                                                  |
| spectral_norm              | 156 ms                                                 | 170 ms: 1.09x slower                                                   |
| tomli_loads                | 2.88 sec                                               | 3.15 sec: 1.09x slower                                                 |
| xml_etree_generate         | 127 ms                                                 | 140 ms: 1.10x slower                                                   |
| deepcopy_memo              | 52.4 us                                                | 57.6 us: 1.10x slower                                                  |
| generators                 | 41.1 ms                                                | 45.6 ms: 1.11x slower                                                  |
| deepcopy                   | 468 us                                                 | 520 us: 1.11x slower                                                   |
| bench_thread_pool          | 3.48 ms                                                | 3.88 ms: 1.12x slower                                                  |
| json_loads                 | 37.9 us                                                | 43.1 us: 1.14x slower                                                  |
| sqlglot_optimize           | 76.0 ms                                                | 86.8 ms: 1.14x slower                                                  |
| crypto_pyaes               | 107 ms                                                 | 123 ms: 1.15x slower                                                   |
| comprehensions             | 27.1 us                                                | 31.2 us: 1.15x slower                                                  |
| regex_v8                   | 32.5 ms                                                | 37.5 ms: 1.15x slower                                                  |
| pyflate                    | 727 ms                                                 | 840 ms: 1.15x slower                                                   |
| pickle_pure_python         | 436 us                                                 | 505 us: 1.16x slower                                                   |
| scimark_fft                | 500 ms                                                 | 580 ms: 1.16x slower                                                   |
| dulwich_log                | 100 ms                                                 | 118 ms: 1.18x slower                                                   |
| coroutines                 | 29.5 ms                                                | 34.9 ms: 1.18x slower                                                  |
| logging_silent             | 139 ns                                                 | 165 ns: 1.18x slower                                                   |
| scimark_sor                | 167 ms                                                 | 197 ms: 1.18x slower                                                   |
| sqlglot_normalize          | 157 ms                                                 | 186 ms: 1.18x slower                                                   |
| scimark_lu                 | 152 ms                                                 | 181 ms: 1.19x slower                                                   |
| sqlalchemy_declarative     | 218 ms                                                 | 258 ms: 1.19x slower                                                   |
| pprint_pformat             | 1.98 sec                                               | 2.35 sec: 1.19x slower                                                 |
| 2to3                       | 456 ms                                                 | 550 ms: 1.21x slower                                                   |
| regex_compile              | 187 ms                                                 | 225 ms: 1.21x slower                                                   |
| bpe_tokeniser              | 6.59 sec                                               | 7.96 sec: 1.21x slower                                                 |
| raytrace                   | 408 ms                                                 | 493 ms: 1.21x slower                                                   |
| sqlglot_transpile          | 2.34 ms                                                | 2.83 ms: 1.21x slower                                                  |
| logging_format             | 9.59 us                                                | 11.8 us: 1.23x slower                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 30.5 ms: 1.23x slower                                                  |
| python_startup_no_site     | 17.6 ms                                                | 21.7 ms: 1.24x slower                                                  |
| scimark_monte_carlo        | 96.4 ms                                                | 119 ms: 1.24x slower                                                   |
| fannkuch                   | 540 ms                                                 | 673 ms: 1.25x slower                                                   |
| pprint_safe_repr           | 967 ms                                                 | 1.21 sec: 1.25x slower                                                 |
| genshi_text                | 30.2 ms                                                | 37.8 ms: 1.25x slower                                                  |
| chaos                      | 84.9 ms                                                | 106 ms: 1.25x slower                                                   |
| unpickle_pure_python       | 300 us                                                 | 376 us: 1.25x slower                                                   |
| logging_simple             | 9.45 us                                                | 11.8 us: 1.25x slower                                                  |
| deepcopy_reduce            | 4.04 us                                                | 5.06 us: 1.25x slower                                                  |
| sympy_str                  | 385 ms                                                 | 483 ms: 1.25x slower                                                   |
| richards_super             | 72.8 ms                                                | 91.4 ms: 1.26x slower                                                  |
| html5lib                   | 88.9 ms                                                | 114 ms: 1.28x slower                                                   |
| xml_etree_process          | 83.7 ms                                                | 107 ms: 1.28x slower                                                   |
| json                       | 6.85 ms                                                | 8.76 ms: 1.28x slower                                                  |
| thrift                     | 1.06 ms                                                | 1.37 ms: 1.29x slower                                                  |
| richards                   | 60.3 ms                                                | 80.5 ms: 1.33x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 8.94 ms: 1.34x slower                                                  |
| python_startup             | 23.7 ms                                                | 31.9 ms: 1.35x slower                                                  |
| go                         | 172 ms                                                 | 232 ms: 1.35x slower                                                   |
| sympy_sum                  | 222 ms                                                 | 299 ms: 1.35x slower                                                   |
| genshi_xml                 | 67.6 ms                                                | 92.3 ms: 1.37x slower                                                  |
| sqlglot_parse              | 1.79 ms                                                | 2.44 ms: 1.37x slower                                                  |
| sympy_expand               | 582 ms                                                 | 798 ms: 1.37x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 19.7 ms: 1.38x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 310 us: 1.38x slower                                                   |
| telco                      | 9.59 ms                                                | 13.3 ms: 1.39x slower                                                  |
| django_template            | 44.9 ms                                                | 62.4 ms: 1.39x slower                                                  |
| meteor_contest             | 146 ms                                                 | 206 ms: 1.41x slower                                                   |
| coverage                   | 95.4 ms                                                | 139 ms: 1.46x slower                                                   |
| hexiom                     | 8.27 ms                                                | 12.4 ms: 1.50x slower                                                  |
| nbody                      | 119 ms                                                 | 183 ms: 1.54x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 9.07 ms: 1.55x slower                                                  |
| deltablue                  | 4.27 ms                                                | 6.71 ms: 1.57x slower                                                  |
| mako                       | 15.7 ms                                                | 25.0 ms: 1.59x slower                                                  |
| create_gc_cycles           | 1.94 ms                                                | 3.19 ms: 1.65x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 95.7 ms: 4.62x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.14x slower                                                           |

Benchmark hidden because not significant (5): xml_etree_iterparse, xml_etree_parse, pathlib, docutils, pylint
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250128-3.14.0a4+-1c3bb20-NOGIL/bm-20250128-linux-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.100x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.35x