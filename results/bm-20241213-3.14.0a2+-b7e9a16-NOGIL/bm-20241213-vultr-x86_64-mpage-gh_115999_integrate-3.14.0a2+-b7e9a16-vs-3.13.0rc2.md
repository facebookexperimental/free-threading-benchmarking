# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_integrate
- machine: linux-x86_64
- commit hash: b7e9a16
- commit date: 2024-12-13
- overall geometric mean: 1.114x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 318 ms: 1.23x slower                                                 |
| docutils       | 2.62 sec                                                     | 2.84 sec: 1.09x slower                                               |
| html5lib       | 67.0 ms                                                      | 75.3 ms: 1.12x slower                                                |
| Geometric mean | (ref)                                                        | 1.14x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 591 ms: 1.55x faster                                                 |
| async_tree_io              | 876 ms                                                       | 604 ms: 1.45x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 239 ms: 1.41x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 309 ms: 1.34x faster                                                 |
| async_tree_memoization     | 461 ms                                                       | 347 ms: 1.33x faster                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 481 ms: 1.33x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 514 ms: 1.30x faster                                                 |
| async_tree_none            | 354 ms                                                       | 283 ms: 1.25x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 23.1 ms: 1.02x faster                                                |
| async_generators           | 377 ms                                                       | 422 ms: 1.12x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.24x faster                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.20x faster                                                 |
| float          | 77.5 ms                                                      | 83.0 ms: 1.07x slower                                                |
| nbody          | 85.1 ms                                                      | 133 ms: 1.56x slower                                                 |
| Geometric mean | (ref)                                                        | 1.12x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.86 ms: 1.08x faster                                                |
| regex_dna      | 180 ms                                                       | 176 ms: 1.02x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 24.0 ms: 1.06x slower                                                |
| regex_compile  | 132 ms                                                       | 151 ms: 1.14x slower                                                 |
| Geometric mean | (ref)                                                        | 1.02x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.1 ms: 1.08x faster                                                |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                 |
| json_loads           | 27.0 us                                                      | 27.8 us: 1.03x slower                                                |
| xml_etree_generate   | 85.4 ms                                                      | 96.4 ms: 1.13x slower                                                |
| xml_etree_process    | 59.3 ms                                                      | 68.6 ms: 1.16x slower                                                |
| tomli_loads          | 2.01 sec                                                     | 2.34 sec: 1.17x slower                                               |
| unpickle_pure_python | 210 us                                                       | 248 us: 1.18x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 365 us: 1.24x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 13.2 ms: 1.26x slower                                                |
| Geometric mean       | (ref)                                                        | 1.11x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                |
| python_startup         | 11.0 ms                                                      | 17.0 ms: 1.55x slower                                                |
| Geometric mean         | (ref)                                                        | 1.46x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 59.6 ms: 1.22x slower                                                |
| django_template | 34.1 ms                                                      | 43.4 ms: 1.27x slower                                                |
| genshi_text     | 21.5 ms                                                      | 28.1 ms: 1.31x slower                                                |
| mako            | 11.3 ms                                                      | 15.6 ms: 1.38x slower                                                |
| Geometric mean  | (ref)                                                        | 1.29x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 591 ms: 1.55x faster                                                 |
| async_tree_io              | 876 ms                                                       | 604 ms: 1.45x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 239 ms: 1.41x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 309 ms: 1.34x faster                                                 |
| async_tree_memoization     | 461 ms                                                       | 347 ms: 1.33x faster                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 481 ms: 1.33x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 514 ms: 1.30x faster                                                 |
| async_tree_none            | 354 ms                                                       | 283 ms: 1.25x faster                                                 |
| pidigits                   | 217 ms                                                       | 181 ms: 1.20x faster                                                 |
| deepcopy                   | 355 us                                                       | 315 us: 1.13x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.04 us: 1.08x faster                                                |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.1 ms: 1.08x faster                                                |
| regex_effbot               | 3.08 ms                                                      | 2.86 ms: 1.08x faster                                                |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                 |
| spectral_norm              | 111 ms                                                       | 108 ms: 1.02x faster                                                 |
| regex_dna                  | 180 ms                                                       | 176 ms: 1.02x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 23.1 ms: 1.02x faster                                                |
| pathlib                    | 19.2 ms                                                      | 18.9 ms: 1.02x faster                                                |
| go                         | 141 ms                                                       | 142 ms: 1.01x slower                                                 |
| json_loads                 | 27.0 us                                                      | 27.8 us: 1.03x slower                                                |
| gc_traversal               | 3.14 ms                                                      | 3.29 ms: 1.05x slower                                                |
| deepcopy_reduce            | 3.11 us                                                      | 3.28 us: 1.06x slower                                                |
| regex_v8                   | 22.7 ms                                                      | 24.0 ms: 1.06x slower                                                |
| scimark_fft                | 349 ms                                                       | 371 ms: 1.06x slower                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.74 sec: 1.07x slower                                               |
| float                      | 77.5 ms                                                      | 83.0 ms: 1.07x slower                                                |
| telco                      | 7.82 ms                                                      | 8.46 ms: 1.08x slower                                                |
| pylint                     | 317 ms                                                       | 343 ms: 1.08x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.84 sec: 1.09x slower                                               |
| pycparser                  | 1.12 sec                                                     | 1.22 sec: 1.10x slower                                               |
| generators                 | 28.8 ms                                                      | 31.6 ms: 1.10x slower                                                |
| dulwich_log                | 74.8 ms                                                      | 82.2 ms: 1.10x slower                                                |
| scimark_sor                | 134 ms                                                       | 149 ms: 1.10x slower                                                 |
| pyflate                    | 449 ms                                                       | 498 ms: 1.11x slower                                                 |
| async_generators           | 377 ms                                                       | 422 ms: 1.12x slower                                                 |
| html5lib                   | 67.0 ms                                                      | 75.3 ms: 1.12x slower                                                |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.31 ms: 1.13x slower                                                |
| xml_etree_generate         | 85.4 ms                                                      | 96.4 ms: 1.13x slower                                                |
| logging_silent             | 103 ns                                                       | 117 ns: 1.14x slower                                                 |
| regex_compile              | 132 ms                                                       | 151 ms: 1.14x slower                                                 |
| sqlglot_normalize          | 106 ms                                                       | 122 ms: 1.15x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 68.6 ms: 1.16x slower                                                |
| pprint_safe_repr           | 738 ms                                                       | 854 ms: 1.16x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 61.2 ms: 1.16x slower                                                |
| tomli_loads                | 2.01 sec                                                     | 2.34 sec: 1.17x slower                                               |
| mdp                        | 2.36 sec                                                     | 2.76 sec: 1.17x slower                                               |
| pprint_pformat             | 1.50 sec                                                     | 1.76 sec: 1.18x slower                                               |
| thrift                     | 778 us                                                       | 915 us: 1.18x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 248 us: 1.18x slower                                                 |
| logging_simple             | 6.16 us                                                      | 7.29 us: 1.18x slower                                                |
| coverage                   | 83.0 ms                                                      | 98.7 ms: 1.19x slower                                                |
| logging_format             | 6.84 us                                                      | 8.27 us: 1.21x slower                                                |
| genshi_xml                 | 48.8 ms                                                      | 59.6 ms: 1.22x slower                                                |
| 2to3                       | 260 ms                                                       | 318 ms: 1.23x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 96.5 ms: 1.23x slower                                                |
| pickle_pure_python         | 294 us                                                       | 365 us: 1.24x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 81.2 ms: 1.24x slower                                                |
| chaos                      | 57.3 ms                                                      | 71.2 ms: 1.24x slower                                                |
| sqlglot_transpile          | 1.56 ms                                                      | 1.94 ms: 1.25x slower                                                |
| json_dumps                 | 10.5 ms                                                      | 13.2 ms: 1.26x slower                                                |
| richards                   | 45.2 ms                                                      | 56.8 ms: 1.26x slower                                                |
| django_template            | 34.1 ms                                                      | 43.4 ms: 1.27x slower                                                |
| crypto_pyaes               | 67.9 ms                                                      | 86.4 ms: 1.27x slower                                                |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 7.65 ms: 1.28x slower                                                |
| richards_super             | 51.6 ms                                                      | 66.1 ms: 1.28x slower                                                |
| typing_runtime_protocols   | 155 us                                                       | 200 us: 1.29x slower                                                 |
| sqlglot_parse              | 1.25 ms                                                      | 1.62 ms: 1.29x slower                                                |
| fannkuch                   | 370 ms                                                       | 480 ms: 1.30x slower                                                 |
| comprehensions             | 16.5 us                                                      | 21.5 us: 1.30x slower                                                |
| genshi_text                | 21.5 ms                                                      | 28.1 ms: 1.31x slower                                                |
| raytrace                   | 253 ms                                                       | 331 ms: 1.31x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.80 ms: 1.35x slower                                                |
| mako                       | 11.3 ms                                                      | 15.6 ms: 1.38x slower                                                |
| python_startup_no_site     | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                |
| scimark_lu                 | 113 ms                                                       | 161 ms: 1.43x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 28.4 ms: 1.43x slower                                                |
| deltablue                  | 3.12 ms                                                      | 4.72 ms: 1.51x slower                                                |
| python_startup             | 11.0 ms                                                      | 17.0 ms: 1.55x slower                                                |
| nbody                      | 85.1 ms                                                      | 133 ms: 1.56x slower                                                 |
| sympy_str                  | 275 ms                                                       | 458 ms: 1.67x slower                                                 |
| sympy_expand               | 457 ms                                                       | 927 ms: 2.03x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 340 ms: 2.19x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 3.33 ms: 3.63x slower                                                |
| bench_mp_pool              | 11.0 ms                                                      | 105 ms: 9.58x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.17x slower                                                         |

Benchmark hidden because not significant (3): asyncio_websockets, deepcopy_memo, json
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241213-3.14.0a2+-b7e9a16-NOGIL/bm-20241213-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a2+-b7e9a16.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.114x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.10x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.33x