# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: 7ab3ec6
- commit date: 2025-01-10
- overall geometric mean: 1.086x slower
- HPT reliability: 99.99%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 310 ms: 1.19x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.83 sec: 1.08x slower                                                |
| html5lib       | 67.0 ms                                                      | 72.1 ms: 1.08x slower                                                 |
| Geometric mean | (ref)                                                        | 1.12x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 589 ms: 1.55x faster                                                  |
| async_tree_io              | 876 ms                                                       | 604 ms: 1.45x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 240 ms: 1.40x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 481 ms: 1.33x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 350 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 523 ms: 1.27x faster                                                  |
| async_tree_none            | 354 ms                                                       | 286 ms: 1.24x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 516 ms: 1.01x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.1 ms: 1.02x slower                                                 |
| async_generators           | 377 ms                                                       | 426 ms: 1.13x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.23x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 194 ms: 1.12x faster                                                  |
| float          | 77.5 ms                                                      | 75.6 ms: 1.02x faster                                                 |
| nbody          | 85.1 ms                                                      | 130 ms: 1.53x slower                                                  |
| Geometric mean | (ref)                                                        | 1.10x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.93 ms: 1.05x faster                                                 |
| regex_dna      | 180 ms                                                       | 175 ms: 1.03x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 23.7 ms: 1.05x slower                                                 |
| regex_compile  | 132 ms                                                       | 149 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.1 ms: 1.09x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                  |
| json_loads           | 27.0 us                                                      | 28.3 us: 1.05x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 95.7 ms: 1.12x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 68.1 ms: 1.15x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 241 us: 1.15x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.32 sec: 1.16x slower                                                |
| json_dumps           | 10.5 ms                                                      | 12.8 ms: 1.22x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 364 us: 1.24x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.10x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.73 ms: 1.32x slower                                                 |
| python_startup         | 11.0 ms                                                      | 15.5 ms: 1.41x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.36x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 59.4 ms: 1.22x slower                                                 |
| django_template | 34.1 ms                                                      | 43.0 ms: 1.26x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 28.4 ms: 1.32x slower                                                 |
| mako            | 11.3 ms                                                      | 15.7 ms: 1.38x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 589 ms: 1.55x faster                                                  |
| async_tree_io              | 876 ms                                                       | 604 ms: 1.45x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 240 ms: 1.40x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 308 ms: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 481 ms: 1.33x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 350 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 523 ms: 1.27x faster                                                  |
| async_tree_none            | 354 ms                                                       | 286 ms: 1.24x faster                                                  |
| deepcopy                   | 355 us                                                       | 315 us: 1.13x faster                                                  |
| pidigits                   | 217 ms                                                       | 194 ms: 1.12x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.1 ms: 1.09x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.05 us: 1.08x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.93 ms: 1.05x faster                                                 |
| go                         | 141 ms                                                       | 136 ms: 1.03x faster                                                  |
| regex_dna                  | 180 ms                                                       | 175 ms: 1.03x faster                                                  |
| float                      | 77.5 ms                                                      | 75.6 ms: 1.02x faster                                                 |
| scimark_sor                | 134 ms                                                       | 133 ms: 1.01x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 516 ms: 1.01x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 19.1 ms: 1.01x faster                                                 |
| json                       | 4.93 ms                                                      | 4.96 ms: 1.01x slower                                                 |
| spectral_norm              | 111 ms                                                       | 112 ms: 1.01x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.1 ms: 1.02x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 3.22 ms: 1.02x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 23.7 ms: 1.05x slower                                                 |
| json_loads                 | 27.0 us                                                      | 28.3 us: 1.05x slower                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 3.32 us: 1.07x slower                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.74 sec: 1.07x slower                                                |
| generators                 | 28.8 ms                                                      | 30.8 ms: 1.07x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.20 sec: 1.07x slower                                                |
| pyflate                    | 449 ms                                                       | 482 ms: 1.07x slower                                                  |
| html5lib                   | 67.0 ms                                                      | 72.1 ms: 1.08x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.83 sec: 1.08x slower                                                |
| scimark_fft                | 349 ms                                                       | 381 ms: 1.09x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 82.0 ms: 1.10x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 819 ms: 1.11x slower                                                  |
| telco                      | 7.82 ms                                                      | 8.73 ms: 1.12x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 95.7 ms: 1.12x slower                                                 |
| regex_compile              | 132 ms                                                       | 149 ms: 1.12x slower                                                  |
| logging_silent             | 103 ns                                                       | 116 ns: 1.13x slower                                                  |
| async_generators           | 377 ms                                                       | 426 ms: 1.13x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.69 sec: 1.13x slower                                                |
| sqlglot_normalize          | 106 ms                                                       | 121 ms: 1.15x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.70 sec: 1.15x slower                                                |
| xml_etree_process          | 59.3 ms                                                      | 68.1 ms: 1.15x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 241 us: 1.15x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.32 sec: 1.16x slower                                                |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.52 ms: 1.17x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 61.9 ms: 1.17x slower                                                 |
| thrift                     | 778 us                                                       | 917 us: 1.18x slower                                                  |
| logging_simple             | 6.16 us                                                      | 7.28 us: 1.18x slower                                                 |
| 2to3                       | 260 ms                                                       | 310 ms: 1.19x slower                                                  |
| coverage                   | 83.0 ms                                                      | 99.2 ms: 1.20x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 186 ms: 1.20x slower                                                  |
| sympy_expand               | 457 ms                                                       | 549 ms: 1.20x slower                                                  |
| richards                   | 45.2 ms                                                      | 54.5 ms: 1.20x slower                                                 |
| logging_format             | 6.84 us                                                      | 8.31 us: 1.21x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 12.8 ms: 1.22x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 59.4 ms: 1.22x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 7.30 ms: 1.22x slower                                                 |
| sympy_str                  | 275 ms                                                       | 335 ms: 1.22x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 24.2 ms: 1.22x slower                                                 |
| chaos                      | 57.3 ms                                                      | 70.3 ms: 1.23x slower                                                 |
| sqlglot_transpile          | 1.56 ms                                                      | 1.92 ms: 1.23x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 97.0 ms: 1.23x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 364 us: 1.24x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 139 ms: 1.24x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 81.1 ms: 1.24x slower                                                 |
| richards_super             | 51.6 ms                                                      | 64.4 ms: 1.25x slower                                                 |
| comprehensions             | 16.5 us                                                      | 20.7 us: 1.26x slower                                                 |
| django_template            | 34.1 ms                                                      | 43.0 ms: 1.26x slower                                                 |
| sqlglot_parse              | 1.25 ms                                                      | 1.58 ms: 1.27x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 86.6 ms: 1.28x slower                                                 |
| raytrace                   | 253 ms                                                       | 323 ms: 1.28x slower                                                  |
| meteor_contest             | 102 ms                                                       | 131 ms: 1.28x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 199 us: 1.29x slower                                                  |
| fannkuch                   | 370 ms                                                       | 477 ms: 1.29x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 9.73 ms: 1.32x slower                                                 |
| genshi_text                | 21.5 ms                                                      | 28.4 ms: 1.32x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.37x slower                                                 |
| mako                       | 11.3 ms                                                      | 15.7 ms: 1.38x slower                                                 |
| python_startup             | 11.0 ms                                                      | 15.5 ms: 1.41x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 4.63 ms: 1.48x slower                                                 |
| nbody                      | 85.1 ms                                                      | 130 ms: 1.53x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.33 ms: 3.62x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 97.8 ms: 8.90x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.14x slower                                                          |

Benchmark hidden because not significant (2): deepcopy_memo, pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250110-3.14.0a3+-7ab3ec6-NOGIL/bm-20250110-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-7ab3ec6.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.086x slower

# HPT report

- Reliability score: 99.99% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.33x