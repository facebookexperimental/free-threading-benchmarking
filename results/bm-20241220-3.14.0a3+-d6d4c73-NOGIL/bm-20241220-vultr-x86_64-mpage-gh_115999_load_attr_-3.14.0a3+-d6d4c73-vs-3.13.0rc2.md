# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: d6d4c73
- commit date: 2024-12-20
- overall geometric mean: 1.116x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 322 ms: 1.24x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.84 sec: 1.09x slower                                                |
| html5lib       | 67.0 ms                                                      | 71.4 ms: 1.07x slower                                                 |
| Geometric mean | (ref)                                                        | 1.13x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 586 ms: 1.56x faster                                                  |
| async_tree_io              | 876 ms                                                       | 604 ms: 1.45x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 241 ms: 1.40x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 484 ms: 1.32x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 350 ms: 1.32x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 315 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 518 ms: 1.29x faster                                                  |
| async_tree_none            | 354 ms                                                       | 284 ms: 1.25x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.0 ms: 1.02x slower                                                 |
| async_generators           | 377 ms                                                       | 420 ms: 1.11x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.24x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| float          | 77.5 ms                                                      | 81.9 ms: 1.06x slower                                                 |
| nbody          | 85.1 ms                                                      | 136 ms: 1.60x slower                                                  |
| Geometric mean | (ref)                                                        | 1.13x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.92 ms: 1.05x faster                                                 |
| regex_dna      | 180 ms                                                       | 177 ms: 1.02x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 24.3 ms: 1.07x slower                                                 |
| regex_compile  | 132 ms                                                       | 151 ms: 1.14x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.5 ms: 1.07x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| json_loads           | 27.0 us                                                      | 27.9 us: 1.03x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 96.8 ms: 1.13x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 68.6 ms: 1.16x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 247 us: 1.18x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.49 sec: 1.24x slower                                                |
| json_dumps           | 10.5 ms                                                      | 13.1 ms: 1.24x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 370 us: 1.26x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.12x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                 |
| python_startup         | 11.0 ms                                                      | 17.1 ms: 1.55x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.46x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 60.1 ms: 1.23x slower                                                 |
| django_template | 34.1 ms                                                      | 42.9 ms: 1.26x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 28.5 ms: 1.32x slower                                                 |
| mako            | 11.3 ms                                                      | 15.8 ms: 1.39x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.30x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 586 ms: 1.56x faster                                                  |
| async_tree_io              | 876 ms                                                       | 604 ms: 1.45x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 241 ms: 1.40x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 484 ms: 1.32x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 350 ms: 1.32x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 315 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 518 ms: 1.29x faster                                                  |
| async_tree_none            | 354 ms                                                       | 284 ms: 1.25x faster                                                  |
| pidigits                   | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| deepcopy                   | 355 us                                                       | 314 us: 1.13x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.5 ms: 1.07x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.07 us: 1.07x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.92 ms: 1.05x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                  |
| regex_dna                  | 180 ms                                                       | 177 ms: 1.02x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 38.7 us: 1.01x faster                                                 |
| json                       | 4.93 ms                                                      | 4.89 ms: 1.01x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.0 ms: 1.02x slower                                                 |
| go                         | 141 ms                                                       | 143 ms: 1.02x slower                                                  |
| spectral_norm              | 111 ms                                                       | 115 ms: 1.03x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.9 us: 1.03x slower                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 3.23 us: 1.04x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 3.29 ms: 1.05x slower                                                 |
| float                      | 77.5 ms                                                      | 81.9 ms: 1.06x slower                                                 |
| html5lib                   | 67.0 ms                                                      | 71.4 ms: 1.07x slower                                                 |
| regex_v8                   | 22.7 ms                                                      | 24.3 ms: 1.07x slower                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.79 sec: 1.08x slower                                                |
| telco                      | 7.82 ms                                                      | 8.47 ms: 1.08x slower                                                 |
| generators                 | 28.8 ms                                                      | 31.3 ms: 1.08x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.84 sec: 1.09x slower                                                |
| scimark_fft                | 349 ms                                                       | 380 ms: 1.09x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.22 sec: 1.09x slower                                                |
| pylint                     | 317 ms                                                       | 346 ms: 1.09x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 82.5 ms: 1.10x slower                                                 |
| mdp                        | 2.36 sec                                                     | 2.60 sec: 1.11x slower                                                |
| pyflate                    | 449 ms                                                       | 497 ms: 1.11x slower                                                  |
| async_generators           | 377 ms                                                       | 420 ms: 1.11x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 96.8 ms: 1.13x slower                                                 |
| logging_silent             | 103 ns                                                       | 116 ns: 1.13x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 841 ms: 1.14x slower                                                  |
| regex_compile              | 132 ms                                                       | 151 ms: 1.14x slower                                                  |
| sqlglot_normalize          | 106 ms                                                       | 121 ms: 1.14x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 68.6 ms: 1.16x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.74 sec: 1.16x slower                                                |
| sqlglot_optimize           | 52.7 ms                                                      | 61.4 ms: 1.16x slower                                                 |
| thrift                     | 778 us                                                       | 915 us: 1.18x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 247 us: 1.18x slower                                                  |
| coverage                   | 83.0 ms                                                      | 99.3 ms: 1.20x slower                                                 |
| scimark_sor                | 134 ms                                                       | 162 ms: 1.20x slower                                                  |
| logging_simple             | 6.16 us                                                      | 7.42 us: 1.20x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.69 ms: 1.21x slower                                                 |
| logging_format             | 6.84 us                                                      | 8.39 us: 1.23x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 60.1 ms: 1.23x slower                                                 |
| sqlglot_transpile          | 1.56 ms                                                      | 1.93 ms: 1.24x slower                                                 |
| 2to3                       | 260 ms                                                       | 322 ms: 1.24x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 97.5 ms: 1.24x slower                                                 |
| chaos                      | 57.3 ms                                                      | 71.1 ms: 1.24x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 2.49 sec: 1.24x slower                                                |
| json_dumps                 | 10.5 ms                                                      | 13.1 ms: 1.24x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 370 us: 1.26x slower                                                  |
| django_template            | 34.1 ms                                                      | 42.9 ms: 1.26x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 142 ms: 1.26x slower                                                  |
| richards                   | 45.2 ms                                                      | 56.9 ms: 1.26x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 7.62 ms: 1.27x slower                                                 |
| richards_super             | 51.6 ms                                                      | 65.9 ms: 1.28x slower                                                 |
| comprehensions             | 16.5 us                                                      | 21.0 us: 1.28x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 86.8 ms: 1.28x slower                                                 |
| raytrace                   | 253 ms                                                       | 323 ms: 1.28x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 1.60 ms: 1.28x slower                                                 |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 199 us: 1.29x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 84.5 ms: 1.29x slower                                                 |
| genshi_text                | 21.5 ms                                                      | 28.5 ms: 1.32x slower                                                 |
| fannkuch                   | 370 ms                                                       | 490 ms: 1.32x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.79 ms: 1.34x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 10.2 ms: 1.38x slower                                                 |
| mako                       | 11.3 ms                                                      | 15.8 ms: 1.39x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 28.9 ms: 1.46x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 4.84 ms: 1.55x slower                                                 |
| python_startup             | 11.0 ms                                                      | 17.1 ms: 1.55x slower                                                 |
| nbody                      | 85.1 ms                                                      | 136 ms: 1.60x slower                                                  |
| sympy_str                  | 275 ms                                                       | 459 ms: 1.67x slower                                                  |
| sympy_expand               | 457 ms                                                       | 929 ms: 2.03x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 343 ms: 2.20x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 3.34 ms: 3.63x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 105 ms: 9.59x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.17x slower                                                          |

Benchmark hidden because not significant (1): pathlib
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241220-3.14.0a3+-d6d4c73-NOGIL/bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.116x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.33x