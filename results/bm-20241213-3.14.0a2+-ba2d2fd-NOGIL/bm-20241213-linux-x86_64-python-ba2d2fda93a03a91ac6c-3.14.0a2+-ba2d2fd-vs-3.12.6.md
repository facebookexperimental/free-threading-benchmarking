# Results vs. 3.12.6

- fork: python
- ref: ba2d2fda93a03a91ac6c
- machine: linux-x86_64
- commit hash: ba2d2fd
- commit date: 2024-12-13
- overall geometric mean: 1.173x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 595 ms: 1.30x slower                                                   |
| docutils       | 4.00 sec                                               | 4.43 sec: 1.11x slower                                                 |
| html5lib       | 88.9 ms                                                | 124 ms: 1.39x slower                                                   |
| Geometric mean | (ref)                                                  | 1.26x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.06 sec: 1.82x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 1.14 sec: 1.63x faster                                                 |
| async_tree_none_tg         | 704 ms                                                 | 440 ms: 1.60x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 634 ms: 1.47x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 683 ms: 1.43x faster                                                   |
| async_tree_none            | 741 ms                                                 | 533 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 799 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 866 ms: 1.25x faster                                                   |
| async_generators           | 589 ms                                                 | 653 ms: 1.11x slower                                                   |
| coroutines                 | 29.5 ms                                                | 33.6 ms: 1.14x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.30x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 242 ms: 1.03x faster                                                   |
| float          | 123 ms                                                 | 181 ms: 1.47x slower                                                   |
| nbody          | 119 ms                                                 | 181 ms: 1.52x slower                                                   |
| Geometric mean | (ref)                                                  | 1.29x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.47 ms: 1.15x faster                                                  |
| regex_dna      | 278 ms                                                 | 302 ms: 1.08x slower                                                   |
| regex_compile  | 187 ms                                                 | 231 ms: 1.24x slower                                                   |
| Geometric mean | (ref)                                                  | 1.05x slower                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 169 ms                                                 | 137 ms: 1.24x faster                                                   |
| xml_etree_parse      | 241 ms                                                 | 206 ms: 1.17x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 3.50 sec: 1.21x slower                                                 |
| json_dumps           | 14.3 ms                                                | 18.1 ms: 1.27x slower                                                  |
| xml_etree_process    | 83.7 ms                                                | 107 ms: 1.28x slower                                                   |
| unpickle_pure_python | 300 us                                                 | 406 us: 1.36x slower                                                   |
| pickle_pure_python   | 436 us                                                 | 664 us: 1.52x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.12x slower                                                           |

Benchmark hidden because not significant (2): xml_etree_generate, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 20.8 ms: 1.18x slower                                                  |
| python_startup         | 23.7 ms                                                | 34.6 ms: 1.46x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.31x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 88.3 ms: 1.31x slower                                                  |
| genshi_text     | 30.2 ms                                                | 42.1 ms: 1.39x slower                                                  |
| django_template | 44.9 ms                                                | 63.3 ms: 1.41x slower                                                  |
| mako            | 15.7 ms                                                | 27.5 ms: 1.75x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.45x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.93 sec                                               | 1.06 sec: 1.82x faster                                                 |
| async_tree_io              | 1.85 sec                                               | 1.14 sec: 1.63x faster                                                 |
| async_tree_none_tg         | 704 ms                                                 | 440 ms: 1.60x faster                                                   |
| async_tree_memoization_tg  | 930 ms                                                 | 634 ms: 1.47x faster                                                   |
| async_tree_memoization     | 977 ms                                                 | 683 ms: 1.43x faster                                                   |
| async_tree_none            | 741 ms                                                 | 533 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed_tg | 1.10 sec                                               | 799 ms: 1.38x faster                                                   |
| async_tree_cpu_io_mixed    | 1.08 sec                                               | 866 ms: 1.25x faster                                                   |
| xml_etree_iterparse        | 169 ms                                                 | 137 ms: 1.24x faster                                                   |
| xml_etree_parse            | 241 ms                                                 | 206 ms: 1.17x faster                                                   |
| regex_effbot               | 5.13 ms                                                | 4.47 ms: 1.15x faster                                                  |
| pidigits                   | 250 ms                                                 | 242 ms: 1.03x faster                                                   |
| sqlite_synth               | 3.87 us                                                | 4.08 us: 1.05x slower                                                  |
| nqueens                    | 117 ms                                                 | 123 ms: 1.06x slower                                                   |
| regex_dna                  | 278 ms                                                 | 302 ms: 1.08x slower                                                   |
| pycparser                  | 1.79 sec                                               | 1.97 sec: 1.10x slower                                                 |
| docutils                   | 4.00 sec                                               | 4.43 sec: 1.11x slower                                                 |
| async_generators           | 589 ms                                                 | 653 ms: 1.11x slower                                                   |
| sqlglot_normalize          | 157 ms                                                 | 174 ms: 1.11x slower                                                   |
| deepcopy_reduce            | 4.04 us                                                | 4.54 us: 1.12x slower                                                  |
| pylint                     | 465 ms                                                 | 524 ms: 1.13x slower                                                   |
| mdp                        | 3.97 sec                                               | 4.48 sec: 1.13x slower                                                 |
| spectral_norm              | 156 ms                                                 | 176 ms: 1.13x slower                                                   |
| gc_traversal               | 5.86 ms                                                | 6.65 ms: 1.14x slower                                                  |
| coroutines                 | 29.5 ms                                                | 33.6 ms: 1.14x slower                                                  |
| crypto_pyaes               | 107 ms                                                 | 123 ms: 1.14x slower                                                   |
| scimark_fft                | 500 ms                                                 | 574 ms: 1.15x slower                                                   |
| dulwich_log                | 100 ms                                                 | 115 ms: 1.15x slower                                                   |
| bench_thread_pool          | 3.48 ms                                                | 4.04 ms: 1.16x slower                                                  |
| scimark_sparse_mat_mult    | 6.70 ms                                                | 7.85 ms: 1.17x slower                                                  |
| python_startup_no_site     | 17.6 ms                                                | 20.8 ms: 1.18x slower                                                  |
| bpe_tokeniser              | 6.59 sec                                               | 7.82 sec: 1.19x slower                                                 |
| sqlglot_optimize           | 76.0 ms                                                | 91.1 ms: 1.20x slower                                                  |
| typing_runtime_protocols   | 224 us                                                 | 272 us: 1.21x slower                                                   |
| tomli_loads                | 2.88 sec                                               | 3.50 sec: 1.21x slower                                                 |
| sqlalchemy_declarative     | 218 ms                                                 | 267 ms: 1.23x slower                                                   |
| meteor_contest             | 146 ms                                                 | 180 ms: 1.23x slower                                                   |
| regex_compile              | 187 ms                                                 | 231 ms: 1.24x slower                                                   |
| fannkuch                   | 540 ms                                                 | 672 ms: 1.24x slower                                                   |
| comprehensions             | 27.1 us                                                | 34.1 us: 1.26x slower                                                  |
| pyflate                    | 727 ms                                                 | 916 ms: 1.26x slower                                                   |
| json_dumps                 | 14.3 ms                                                | 18.1 ms: 1.27x slower                                                  |
| xml_etree_process          | 83.7 ms                                                | 107 ms: 1.28x slower                                                   |
| generators                 | 41.1 ms                                                | 52.9 ms: 1.29x slower                                                  |
| 2to3                       | 456 ms                                                 | 595 ms: 1.30x slower                                                   |
| genshi_xml                 | 67.6 ms                                                | 88.3 ms: 1.31x slower                                                  |
| telco                      | 9.59 ms                                                | 12.7 ms: 1.33x slower                                                  |
| pprint_safe_repr           | 967 ms                                                 | 1.29 sec: 1.34x slower                                                 |
| pprint_pformat             | 1.98 sec                                               | 2.65 sec: 1.34x slower                                                 |
| sympy_integrate            | 29.8 ms                                                | 39.9 ms: 1.34x slower                                                  |
| unpickle_pure_python       | 300 us                                                 | 406 us: 1.36x slower                                                   |
| logging_simple             | 9.45 us                                                | 13.1 us: 1.39x slower                                                  |
| html5lib                   | 88.9 ms                                                | 124 ms: 1.39x slower                                                   |
| genshi_text                | 30.2 ms                                                | 42.1 ms: 1.39x slower                                                  |
| django_template            | 44.9 ms                                                | 63.3 ms: 1.41x slower                                                  |
| richards_super             | 72.8 ms                                                | 104 ms: 1.42x slower                                                   |
| chaos                      | 84.9 ms                                                | 121 ms: 1.43x slower                                                   |
| scimark_lu                 | 152 ms                                                 | 221 ms: 1.45x slower                                                   |
| logging_format             | 9.59 us                                                | 14.0 us: 1.46x slower                                                  |
| python_startup             | 23.7 ms                                                | 34.6 ms: 1.46x slower                                                  |
| coverage                   | 95.4 ms                                                | 140 ms: 1.47x slower                                                   |
| float                      | 123 ms                                                 | 181 ms: 1.47x slower                                                   |
| scimark_monte_carlo        | 96.4 ms                                                | 143 ms: 1.48x slower                                                   |
| thrift                     | 1.06 ms                                                | 1.58 ms: 1.49x slower                                                  |
| sqlalchemy_imperative      | 24.7 ms                                                | 37.3 ms: 1.51x slower                                                  |
| richards                   | 60.3 ms                                                | 91.1 ms: 1.51x slower                                                  |
| nbody                      | 119 ms                                                 | 181 ms: 1.52x slower                                                   |
| pickle_pure_python         | 436 us                                                 | 664 us: 1.52x slower                                                   |
| sympy_str                  | 385 ms                                                 | 598 ms: 1.55x slower                                                   |
| logging_silent             | 139 ns                                                 | 218 ns: 1.57x slower                                                   |
| raytrace                   | 408 ms                                                 | 645 ms: 1.58x slower                                                   |
| hexiom                     | 8.27 ms                                                | 13.3 ms: 1.60x slower                                                  |
| sqlglot_transpile          | 2.34 ms                                                | 3.79 ms: 1.62x slower                                                  |
| mako                       | 15.7 ms                                                | 27.5 ms: 1.75x slower                                                  |
| scimark_sor                | 167 ms                                                 | 297 ms: 1.78x slower                                                   |
| sqlglot_parse              | 1.79 ms                                                | 3.25 ms: 1.81x slower                                                  |
| go                         | 172 ms                                                 | 314 ms: 1.82x slower                                                   |
| create_gc_cycles           | 1.94 ms                                                | 3.66 ms: 1.89x slower                                                  |
| sympy_sum                  | 222 ms                                                 | 424 ms: 1.91x slower                                                   |
| sympy_expand               | 582 ms                                                 | 1.16 sec: 2.00x slower                                                 |
| deltablue                  | 4.27 ms                                                | 11.1 ms: 2.61x slower                                                  |
| bench_mp_pool              | 20.7 ms                                                | 94.3 ms: 4.56x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.23x slower                                                           |

Benchmark hidden because not significant (8): pathlib, deepcopy_memo, deepcopy, xml_etree_generate, asyncio_websockets, json_loads, json, regex_v8
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241213-3.14.0a2+-ba2d2fd-NOGIL/bm-20241213-linux-x86_64-python-ba2d2fda93a03a91ac6c-3.14.0a2+-ba2d2fd.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.173x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.15x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.34x