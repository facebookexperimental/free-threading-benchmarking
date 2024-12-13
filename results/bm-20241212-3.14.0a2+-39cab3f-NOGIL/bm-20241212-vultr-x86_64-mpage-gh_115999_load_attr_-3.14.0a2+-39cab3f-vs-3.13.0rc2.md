# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 39cab3f
- commit date: 2024-12-12
- overall geometric mean: 1.164x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 342 ms: 1.32x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.87 sec: 1.10x slower                                                |
| html5lib       | 67.0 ms                                                      | 78.3 ms: 1.17x slower                                                 |
| Geometric mean | (ref)                                                        | 1.19x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 637 ms: 1.43x faster                                                  |
| async_tree_io              | 876 ms                                                       | 662 ms: 1.32x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 272 ms: 1.24x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 377 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 524 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 550 ms: 1.21x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 346 ms: 1.20x faster                                                  |
| async_tree_none            | 354 ms                                                       | 309 ms: 1.14x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.6 ms: 1.05x slower                                                 |
| async_generators           | 377 ms                                                       | 423 ms: 1.12x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.16x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| float          | 77.5 ms                                                      | 109 ms: 1.40x slower                                                  |
| nbody          | 85.1 ms                                                      | 132 ms: 1.55x slower                                                  |
| Geometric mean | (ref)                                                        | 1.23x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.85 ms: 1.08x faster                                                 |
| regex_dna      | 180 ms                                                       | 178 ms: 1.01x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 24.0 ms: 1.06x slower                                                 |
| regex_compile  | 132 ms                                                       | 161 ms: 1.22x slower                                                  |
| Geometric mean | (ref)                                                        | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.2 ms: 1.08x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| json_loads           | 27.0 us                                                      | 28.0 us: 1.04x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 97.1 ms: 1.14x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 257 us: 1.23x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 13.2 ms: 1.25x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 370 us: 1.26x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.60 sec: 1.30x slower                                                |
| xml_etree_process    | 59.3 ms                                                      | 77.4 ms: 1.30x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.15x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 14.2 ms: 1.92x slower                                                 |
| python_startup         | 11.0 ms                                                      | 23.6 ms: 2.15x slower                                                 |
| Geometric mean         | (ref)                                                        | 2.03x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 61.1 ms: 1.25x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 27.9 ms: 1.30x slower                                                 |
| django_template | 34.1 ms                                                      | 44.3 ms: 1.30x slower                                                 |
| mako            | 11.3 ms                                                      | 15.6 ms: 1.38x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.31x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 637 ms: 1.43x faster                                                  |
| async_tree_io              | 876 ms                                                       | 662 ms: 1.32x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 272 ms: 1.24x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 377 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 524 ms: 1.22x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 550 ms: 1.21x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 346 ms: 1.20x faster                                                  |
| pidigits                   | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| async_tree_none            | 354 ms                                                       | 309 ms: 1.14x faster                                                  |
| deepcopy                   | 355 us                                                       | 315 us: 1.13x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.85 ms: 1.08x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.2 ms: 1.08x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.13 us: 1.04x faster                                                 |
| deepcopy_memo              | 39.1 us                                                      | 38.5 us: 1.02x faster                                                 |
| regex_dna                  | 180 ms                                                       | 178 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 19.4 ms: 1.01x slower                                                 |
| json_loads                 | 27.0 us                                                      | 28.0 us: 1.04x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 3.27 ms: 1.04x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 24.6 ms: 1.05x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 24.0 ms: 1.06x slower                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 3.36 us: 1.08x slower                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.81 sec: 1.08x slower                                                |
| generators                 | 28.8 ms                                                      | 31.2 ms: 1.08x slower                                                 |
| logging_silent             | 103 ns                                                       | 112 ns: 1.09x slower                                                  |
| spectral_norm              | 111 ms                                                       | 121 ms: 1.09x slower                                                  |
| docutils                   | 2.62 sec                                                     | 2.87 sec: 1.10x slower                                                |
| pylint                     | 317 ms                                                       | 352 ms: 1.11x slower                                                  |
| telco                      | 7.82 ms                                                      | 8.74 ms: 1.12x slower                                                 |
| async_generators           | 377 ms                                                       | 423 ms: 1.12x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 97.1 ms: 1.14x slower                                                 |
| scimark_fft                | 349 ms                                                       | 397 ms: 1.14x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 85.8 ms: 1.15x slower                                                 |
| sqlglot_normalize          | 106 ms                                                       | 122 ms: 1.16x slower                                                  |
| html5lib                   | 67.0 ms                                                      | 78.3 ms: 1.17x slower                                                 |
| mdp                        | 2.36 sec                                                     | 2.77 sec: 1.18x slower                                                |
| coverage                   | 83.0 ms                                                      | 98.3 ms: 1.18x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.34 sec: 1.20x slower                                                |
| sqlglot_optimize           | 52.7 ms                                                      | 63.1 ms: 1.20x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 882 ms: 1.20x slower                                                  |
| go                         | 141 ms                                                       | 170 ms: 1.21x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.70 ms: 1.21x slower                                                 |
| regex_compile              | 132 ms                                                       | 161 ms: 1.22x slower                                                  |
| pyflate                    | 449 ms                                                       | 547 ms: 1.22x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.83 sec: 1.22x slower                                                |
| unpickle_pure_python       | 210 us                                                       | 257 us: 1.23x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 98.1 ms: 1.25x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 61.1 ms: 1.25x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 13.2 ms: 1.25x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 370 us: 1.26x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 86.6 ms: 1.28x slower                                                 |
| comprehensions             | 16.5 us                                                      | 21.0 us: 1.28x slower                                                 |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.60 sec: 1.30x slower                                                |
| genshi_text                | 21.5 ms                                                      | 27.9 ms: 1.30x slower                                                 |
| django_template            | 34.1 ms                                                      | 44.3 ms: 1.30x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 77.4 ms: 1.30x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 7.84 ms: 1.31x slower                                                 |
| 2to3                       | 260 ms                                                       | 342 ms: 1.32x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 206 us: 1.33x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.78 ms: 1.33x slower                                                 |
| logging_simple             | 6.16 us                                                      | 8.23 us: 1.34x slower                                                 |
| fannkuch                   | 370 ms                                                       | 498 ms: 1.35x slower                                                  |
| scimark_sor                | 134 ms                                                       | 181 ms: 1.35x slower                                                  |
| thrift                     | 778 us                                                       | 1.05 ms: 1.35x slower                                                 |
| logging_format             | 6.84 us                                                      | 9.40 us: 1.37x slower                                                 |
| mako                       | 11.3 ms                                                      | 15.6 ms: 1.38x slower                                                 |
| chaos                      | 57.3 ms                                                      | 80.4 ms: 1.40x slower                                                 |
| float                      | 77.5 ms                                                      | 109 ms: 1.40x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 2.21 ms: 1.42x slower                                                 |
| richards                   | 45.2 ms                                                      | 65.3 ms: 1.44x slower                                                 |
| richards_super             | 51.6 ms                                                      | 74.7 ms: 1.45x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 28.7 ms: 1.45x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 164 ms: 1.45x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 95.6 ms: 1.46x slower                                                 |
| raytrace                   | 253 ms                                                       | 381 ms: 1.51x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.89 ms: 1.51x slower                                                 |
| nbody                      | 85.1 ms                                                      | 132 ms: 1.55x slower                                                  |
| sympy_str                  | 275 ms                                                       | 460 ms: 1.68x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 5.43 ms: 1.74x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 14.2 ms: 1.92x slower                                                 |
| sympy_expand               | 457 ms                                                       | 933 ms: 2.04x slower                                                  |
| python_startup             | 11.0 ms                                                      | 23.6 ms: 2.15x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 343 ms: 2.20x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.43 ms: 3.73x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 116 ms: 10.52x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.24x slower                                                          |

Benchmark hidden because not significant (1): json
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241212-3.14.0a2+-39cab3f-NOGIL/bm-20241212-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a2+-39cab3f.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.164x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.32x