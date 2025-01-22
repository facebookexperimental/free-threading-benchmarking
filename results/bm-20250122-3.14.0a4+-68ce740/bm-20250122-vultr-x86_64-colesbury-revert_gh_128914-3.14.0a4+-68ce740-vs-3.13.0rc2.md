# Results vs. 3.13.0rc2

- fork: colesbury
- ref: revert_gh_128914
- machine: linux-x86_64
- commit hash: 68ce740
- commit date: 2025-01-22
- overall geometric mean: 1.051x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.10x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 252 ms: 1.03x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.55 sec: 1.02x faster                                                |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 618 ms: 1.48x faster                                                  |
| async_tree_io              | 876 ms                                                       | 610 ms: 1.44x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 324 ms: 1.42x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 492 ms: 1.35x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 307 ms: 1.35x faster                                                  |
| async_tree_none            | 354 ms                                                       | 266 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 484 ms: 1.32x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 257 ms: 1.31x faster                                                  |
| async_generators           | 377 ms                                                       | 325 ms: 1.16x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 22.1 ms: 1.07x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                        | 1.29x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 72.4 ms: 1.07x faster                                                 |
| pidigits       | 217 ms                                                       | 207 ms: 1.05x faster                                                  |
| nbody          | 85.1 ms                                                      | 89.2 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                        | 1.02x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.72 ms: 1.13x faster                                                 |
| regex_compile  | 132 ms                                                       | 126 ms: 1.05x faster                                                  |
| regex_dna      | 180 ms                                                       | 174 ms: 1.04x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 23.8 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                        | 1.04x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 128 ms: 1.07x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.91 sec: 1.05x faster                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.4 ms: 1.04x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 84.4 ms: 1.01x faster                                                 |
| xml_etree_process    | 59.3 ms                                                      | 59.0 ms: 1.01x faster                                                 |
| json_loads           | 27.0 us                                                      | 27.9 us: 1.03x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 220 us: 1.05x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 313 us: 1.06x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 11.3 ms: 1.08x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.41 ms: 1.00x slower                                                 |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.15x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.7 ms: 1.01x slower                                                 |
| django_template | 34.1 ms                                                      | 35.5 ms: 1.04x slower                                                 |
| mako            | 11.3 ms                                                      | 12.0 ms: 1.05x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.02x slower                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 618 ms: 1.48x faster                                                  |
| async_tree_io              | 876 ms                                                       | 610 ms: 1.44x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 324 ms: 1.42x faster                                                  |
| deepcopy                   | 355 us                                                       | 259 us: 1.37x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 492 ms: 1.35x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 307 ms: 1.35x faster                                                  |
| async_tree_none            | 354 ms                                                       | 266 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 484 ms: 1.32x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 257 ms: 1.31x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 30.6 us: 1.28x faster                                                 |
| go                         | 141 ms                                                       | 115 ms: 1.22x faster                                                  |
| spectral_norm              | 111 ms                                                       | 93.8 ms: 1.18x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.64 us: 1.18x faster                                                 |
| async_generators           | 377 ms                                                       | 325 ms: 1.16x faster                                                  |
| scimark_sor                | 134 ms                                                       | 116 ms: 1.16x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.09 ms: 1.15x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.72 ms: 1.13x faster                                                 |
| pylint                     | 317 ms                                                       | 281 ms: 1.13x faster                                                  |
| scimark_fft                | 349 ms                                                       | 311 ms: 1.12x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.18 ms: 1.09x faster                                                 |
| float                      | 77.5 ms                                                      | 72.4 ms: 1.07x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 18.0 ms: 1.07x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 128 ms: 1.07x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 22.1 ms: 1.07x faster                                                 |
| thrift                     | 778 us                                                       | 733 us: 1.06x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.19 sec: 1.06x faster                                                |
| richards                   | 45.2 ms                                                      | 42.8 ms: 1.06x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.91 sec: 1.05x faster                                                |
| richards_super             | 51.6 ms                                                      | 49.1 ms: 1.05x faster                                                 |
| pyflate                    | 449 ms                                                       | 428 ms: 1.05x faster                                                  |
| pidigits                   | 217 ms                                                       | 207 ms: 1.05x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 705 ms: 1.05x faster                                                  |
| regex_compile              | 132 ms                                                       | 126 ms: 1.05x faster                                                  |
| coverage                   | 83.0 ms                                                      | 79.5 ms: 1.04x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.44 sec: 1.04x faster                                                |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.4 ms: 1.04x faster                                                 |
| regex_dna                  | 180 ms                                                       | 174 ms: 1.04x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.79 ms: 1.03x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 109 ms: 1.03x faster                                                  |
| 2to3                       | 260 ms                                                       | 252 ms: 1.03x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 63.7 ms: 1.03x faster                                                 |
| meteor_contest             | 102 ms                                                       | 99.1 ms: 1.03x faster                                                 |
| chaos                      | 57.3 ms                                                      | 55.9 ms: 1.02x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.55 sec: 1.02x faster                                                |
| sympy_sum                  | 156 ms                                                       | 153 ms: 1.02x faster                                                  |
| sqlglot_normalize          | 106 ms                                                       | 104 ms: 1.02x faster                                                  |
| mdp                        | 2.36 sec                                                     | 2.32 sec: 1.01x faster                                                |
| sqlglot_optimize           | 52.7 ms                                                      | 52.0 ms: 1.01x faster                                                 |
| sympy_str                  | 275 ms                                                       | 271 ms: 1.01x faster                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 84.4 ms: 1.01x faster                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 67.1 ms: 1.01x faster                                                 |
| fannkuch                   | 370 ms                                                       | 366 ms: 1.01x faster                                                  |
| pycparser                  | 1.12 sec                                                     | 1.11 sec: 1.01x faster                                                |
| sqlite_synth               | 2.21 us                                                      | 2.19 us: 1.01x faster                                                 |
| xml_etree_process          | 59.3 ms                                                      | 59.0 ms: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 517 ms: 1.01x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.7 ms: 1.01x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 78.2 ms: 1.01x faster                                                 |
| sqlglot_transpile          | 1.56 ms                                                      | 1.55 ms: 1.00x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.41 ms: 1.00x slower                                                 |
| genshi_text                | 21.5 ms                                                      | 21.7 ms: 1.01x slower                                                 |
| logging_format             | 6.84 us                                                      | 6.89 us: 1.01x slower                                                 |
| json                       | 4.93 ms                                                      | 4.98 ms: 1.01x slower                                                 |
| dulwich_log                | 74.8 ms                                                      | 75.6 ms: 1.01x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 156 us: 1.01x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.18 ms: 1.02x slower                                                 |
| comprehensions             | 16.5 us                                                      | 16.8 us: 1.02x slower                                                 |
| json_loads                 | 27.0 us                                                      | 27.9 us: 1.03x slower                                                 |
| logging_silent             | 103 ns                                                       | 106 ns: 1.04x slower                                                  |
| django_template            | 34.1 ms                                                      | 35.5 ms: 1.04x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 220 us: 1.05x slower                                                  |
| raytrace                   | 253 ms                                                       | 265 ms: 1.05x slower                                                  |
| nbody                      | 85.1 ms                                                      | 89.2 ms: 1.05x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 23.8 ms: 1.05x slower                                                 |
| mako                       | 11.3 ms                                                      | 12.0 ms: 1.05x slower                                                 |
| generators                 | 28.8 ms                                                      | 30.6 ms: 1.06x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 313 us: 1.06x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 11.3 ms: 1.08x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.03 ms: 1.13x slower                                                 |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.29 ms: 1.37x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.38x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 87.9 ms: 7.99x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.02x faster                                                          |

Benchmark hidden because not significant (4): sympy_expand, genshi_xml, logging_simple, sqlglot_parse
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250122-3.14.0a4+-68ce740/bm-20250122-vultr-x86_64-colesbury-revert_gh_128914-3.14.0a4+-68ce740.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.051x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.10x