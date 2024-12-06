# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: b22403e
- commit date: 2024-12-05
- overall geometric mean: 1.027x faster
- HPT reliability: 83.21%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.09x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 258 ms: 1.01x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                |
| Geometric mean | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 618 ms: 1.48x faster                                                  |
| async_tree_io              | 876 ms                                                       | 624 ms: 1.40x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 338 ms: 1.37x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 498 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 312 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 260 ms: 1.29x faster                                                  |
| async_tree_none            | 354 ms                                                       | 276 ms: 1.28x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 22.3 ms: 1.06x faster                                                 |
| async_generators           | 377 ms                                                       | 368 ms: 1.03x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.25x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 185 ms: 1.17x faster                                                  |
| float          | 77.5 ms                                                      | 78.7 ms: 1.02x slower                                                 |
| nbody          | 85.1 ms                                                      | 94.5 ms: 1.11x slower                                                 |
| Geometric mean | (ref)                                                        | 1.01x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.81 ms: 1.10x faster                                                 |
| regex_dna      | 180 ms                                                       | 168 ms: 1.07x faster                                                  |
| regex_compile  | 132 ms                                                       | 130 ms: 1.01x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 23.7 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_loads           | 27.0 us                                                      | 25.2 us: 1.07x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 129 ms: 1.06x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.9 ms: 1.03x faster                                                 |
| xml_etree_process    | 59.3 ms                                                      | 60.0 ms: 1.01x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 86.9 ms: 1.02x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 216 us: 1.03x slower                                                  |
| tomli_loads          | 2.01 sec                                                     | 2.11 sec: 1.05x slower                                                |
| pickle_pure_python   | 294 us                                                       | 313 us: 1.06x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 11.3 ms: 1.08x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.01x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.47 ms: 1.01x slower                                                 |
| python_startup         | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 22.0 ms: 1.02x slower                                                 |
| mako            | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                 |
| genshi_xml      | 48.8 ms                                                      | 50.5 ms: 1.03x slower                                                 |
| django_template | 34.1 ms                                                      | 35.4 ms: 1.04x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.03x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 618 ms: 1.48x faster                                                  |
| async_tree_io              | 876 ms                                                       | 624 ms: 1.40x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 338 ms: 1.37x faster                                                  |
| deepcopy                   | 355 us                                                       | 263 us: 1.35x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 498 ms: 1.34x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 312 ms: 1.33x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 483 ms: 1.32x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 260 ms: 1.29x faster                                                  |
| async_tree_none            | 354 ms                                                       | 276 ms: 1.28x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 30.9 us: 1.27x faster                                                 |
| go                         | 141 ms                                                       | 119 ms: 1.18x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.65 us: 1.17x faster                                                 |
| pidigits                   | 217 ms                                                       | 185 ms: 1.17x faster                                                  |
| pylint                     | 317 ms                                                       | 284 ms: 1.12x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.81 ms: 1.10x faster                                                 |
| json                       | 4.93 ms                                                      | 4.58 ms: 1.08x faster                                                 |
| json_loads                 | 27.0 us                                                      | 25.2 us: 1.07x faster                                                 |
| regex_dna                  | 180 ms                                                       | 168 ms: 1.07x faster                                                  |
| telco                      | 7.82 ms                                                      | 7.34 ms: 1.07x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 22.3 ms: 1.06x faster                                                 |
| xml_etree_parse            | 136 ms                                                       | 129 ms: 1.06x faster                                                  |
| thrift                     | 778 us                                                       | 738 us: 1.05x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.2 ms: 1.05x faster                                                 |
| coverage                   | 83.0 ms                                                      | 79.5 ms: 1.04x faster                                                 |
| scimark_fft                | 349 ms                                                       | 337 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.9 ms: 1.03x faster                                                 |
| pprint_safe_repr           | 738 ms                                                       | 718 ms: 1.03x faster                                                  |
| async_generators           | 377 ms                                                       | 368 ms: 1.03x faster                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 66.3 ms: 1.02x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.46 sec: 1.02x faster                                                |
| bpe_tokeniser              | 4.45 sec                                                     | 4.35 sec: 1.02x faster                                                |
| docutils                   | 2.62 sec                                                     | 2.56 sec: 1.02x faster                                                |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.62 ms: 1.02x faster                                                 |
| regex_compile              | 132 ms                                                       | 130 ms: 1.01x faster                                                  |
| spectral_norm              | 111 ms                                                       | 110 ms: 1.01x faster                                                  |
| 2to3                       | 260 ms                                                       | 258 ms: 1.01x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 155 ms: 1.00x faster                                                  |
| hexiom                     | 5.99 ms                                                      | 5.98 ms: 1.00x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 523 ms: 1.00x slower                                                  |
| generators                 | 28.8 ms                                                      | 29.0 ms: 1.01x slower                                                 |
| sympy_str                  | 275 ms                                                       | 276 ms: 1.01x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.13 sec: 1.01x slower                                                |
| python_startup_no_site     | 7.39 ms                                                      | 7.47 ms: 1.01x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 60.0 ms: 1.01x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 20.1 ms: 1.01x slower                                                 |
| dulwich_log                | 74.8 ms                                                      | 75.9 ms: 1.01x slower                                                 |
| float                      | 77.5 ms                                                      | 78.7 ms: 1.02x slower                                                 |
| sympy_expand               | 457 ms                                                       | 465 ms: 1.02x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 86.9 ms: 1.02x slower                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.25 us: 1.02x slower                                                 |
| genshi_text                | 21.5 ms                                                      | 22.0 ms: 1.02x slower                                                 |
| sqlglot_normalize          | 106 ms                                                       | 108 ms: 1.02x slower                                                  |
| logging_format             | 6.84 us                                                      | 6.99 us: 1.02x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 53.9 ms: 1.02x slower                                                 |
| chaos                      | 57.3 ms                                                      | 58.7 ms: 1.03x slower                                                 |
| richards_super             | 51.6 ms                                                      | 53.0 ms: 1.03x slower                                                 |
| richards                   | 45.2 ms                                                      | 46.5 ms: 1.03x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 216 us: 1.03x slower                                                  |
| mako                       | 11.3 ms                                                      | 11.7 ms: 1.03x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 81.0 ms: 1.03x slower                                                 |
| sqlglot_transpile          | 1.56 ms                                                      | 1.61 ms: 1.03x slower                                                 |
| genshi_xml                 | 48.8 ms                                                      | 50.5 ms: 1.03x slower                                                 |
| sqlglot_parse              | 1.25 ms                                                      | 1.29 ms: 1.04x slower                                                 |
| django_template            | 34.1 ms                                                      | 35.4 ms: 1.04x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 161 us: 1.04x slower                                                  |
| fannkuch                   | 370 ms                                                       | 385 ms: 1.04x slower                                                  |
| logging_silent             | 103 ns                                                       | 107 ns: 1.04x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 23.7 ms: 1.04x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.27 ms: 1.05x slower                                                 |
| raytrace                   | 253 ms                                                       | 266 ms: 1.05x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.11 sec: 1.05x slower                                                |
| pickle_pure_python         | 294 us                                                       | 313 us: 1.06x slower                                                  |
| comprehensions             | 16.5 us                                                      | 17.6 us: 1.07x slower                                                 |
| mdp                        | 2.36 sec                                                     | 2.54 sec: 1.08x slower                                                |
| json_dumps                 | 10.5 ms                                                      | 11.3 ms: 1.08x slower                                                 |
| nbody                      | 85.1 ms                                                      | 94.5 ms: 1.11x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.02 ms: 1.11x slower                                                 |
| python_startup             | 11.0 ms                                                      | 14.6 ms: 1.33x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.29 ms: 1.37x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.85 ms: 1.39x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 88.8 ms: 8.07x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.00x faster                                                          |

Benchmark hidden because not significant (6): scimark_sor, scimark_lu, scimark_monte_carlo, logging_simple, pyflate, meteor_contest
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241205-3.14.0a2+-b22403e/bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.027x faster

# HPT report

- Reliability score: 83.21% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.09x