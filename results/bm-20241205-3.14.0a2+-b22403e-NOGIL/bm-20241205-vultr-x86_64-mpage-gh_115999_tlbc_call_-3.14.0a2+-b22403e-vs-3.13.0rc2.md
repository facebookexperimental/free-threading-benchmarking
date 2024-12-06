# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: b22403e
- commit date: 2024-12-05
- overall geometric mean: 1.246x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.18x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 366 ms: 1.41x slower                                                  |
| docutils       | 2.62 sec                                                     | 3.08 sec: 1.18x slower                                                |
| html5lib       | 67.0 ms                                                      | 96.9 ms: 1.45x slower                                                 |
| Geometric mean | (ref)                                                        | 1.34x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 817 ms: 1.12x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 632 ms: 1.05x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 611 ms: 1.04x faster                                                  |
| async_tree_io              | 876 ms                                                       | 842 ms: 1.04x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.3 ms: 1.03x slower                                                 |
| async_tree_none_tg         | 336 ms                                                       | 352 ms: 1.05x slower                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 444 ms: 1.07x slower                                                  |
| async_tree_none            | 354 ms                                                       | 383 ms: 1.08x slower                                                  |
| async_generators           | 377 ms                                                       | 451 ms: 1.20x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.02x slower                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.20x faster                                                  |
| nbody          | 85.1 ms                                                      | 131 ms: 1.54x slower                                                  |
| float          | 77.5 ms                                                      | 139 ms: 1.79x slower                                                  |
| Geometric mean | (ref)                                                        | 1.32x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.84 ms: 1.08x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 25.0 ms: 1.10x slower                                                 |
| regex_compile  | 132 ms                                                       | 181 ms: 1.37x slower                                                  |
| Geometric mean | (ref)                                                        | 1.09x slower                                                          |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| xml_etree_iterparse  | 94.9 ms                                                      | 91.3 ms: 1.04x faster                                                 |
| json_loads           | 27.0 us                                                      | 28.5 us: 1.06x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 97.9 ms: 1.15x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 78.0 ms: 1.31x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 2.67 sec: 1.33x slower                                                |
| json_dumps           | 10.5 ms                                                      | 14.4 ms: 1.36x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 331 us: 1.58x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 504 us: 1.71x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.24x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                 |
| python_startup         | 11.0 ms                                                      | 17.5 ms: 1.59x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.49x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 63.4 ms: 1.30x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 31.5 ms: 1.46x slower                                                 |
| django_template | 34.1 ms                                                      | 50.3 ms: 1.47x slower                                                 |
| mako            | 11.3 ms                                                      | 17.7 ms: 1.56x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.44x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits                   | 217 ms                                                       | 181 ms: 1.20x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 817 ms: 1.12x faster                                                  |
| deepcopy                   | 355 us                                                       | 327 us: 1.09x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.84 ms: 1.08x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 632 ms: 1.05x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 611 ms: 1.04x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                  |
| async_tree_io              | 876 ms                                                       | 842 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.3 ms: 1.04x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 24.3 ms: 1.03x slower                                                 |
| deepcopy_memo              | 39.1 us                                                      | 40.5 us: 1.04x slower                                                 |
| json                       | 4.93 ms                                                      | 5.12 ms: 1.04x slower                                                 |
| sqlite_synth               | 2.21 us                                                      | 2.29 us: 1.04x slower                                                 |
| async_tree_none_tg         | 336 ms                                                       | 352 ms: 1.05x slower                                                  |
| json_loads                 | 27.0 us                                                      | 28.5 us: 1.06x slower                                                 |
| pathlib                    | 19.2 ms                                                      | 20.5 ms: 1.07x slower                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 444 ms: 1.07x slower                                                  |
| async_tree_none            | 354 ms                                                       | 383 ms: 1.08x slower                                                  |
| spectral_norm              | 111 ms                                                       | 122 ms: 1.10x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 25.0 ms: 1.10x slower                                                 |
| telco                      | 7.82 ms                                                      | 8.64 ms: 1.10x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 3.51 ms: 1.12x slower                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.97 sec: 1.12x slower                                                |
| deepcopy_reduce            | 3.11 us                                                      | 3.54 us: 1.14x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 97.9 ms: 1.15x slower                                                 |
| scimark_fft                | 349 ms                                                       | 405 ms: 1.16x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.77 sec: 1.17x slower                                                |
| docutils                   | 2.62 sec                                                     | 3.08 sec: 1.18x slower                                                |
| async_generators           | 377 ms                                                       | 451 ms: 1.20x slower                                                  |
| pylint                     | 317 ms                                                       | 380 ms: 1.20x slower                                                  |
| coverage                   | 83.0 ms                                                      | 101 ms: 1.21x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 96.7 ms: 1.23x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.96 ms: 1.27x slower                                                 |
| dulwich_log                | 74.8 ms                                                      | 95.4 ms: 1.28x slower                                                 |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                  |
| sqlglot_normalize          | 106 ms                                                       | 136 ms: 1.29x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 63.4 ms: 1.30x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 68.8 ms: 1.30x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 202 us: 1.31x slower                                                  |
| generators                 | 28.8 ms                                                      | 37.9 ms: 1.31x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 78.0 ms: 1.31x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 971 ms: 1.32x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.67 sec: 1.33x slower                                                |
| crypto_pyaes               | 67.9 ms                                                      | 90.7 ms: 1.34x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 2.01 sec: 1.34x slower                                                |
| fannkuch                   | 370 ms                                                       | 497 ms: 1.35x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 14.4 ms: 1.36x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.53 sec: 1.37x slower                                                |
| regex_compile              | 132 ms                                                       | 181 ms: 1.37x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.37x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                 |
| 2to3                       | 260 ms                                                       | 366 ms: 1.41x slower                                                  |
| html5lib                   | 67.0 ms                                                      | 96.9 ms: 1.45x slower                                                 |
| genshi_text                | 21.5 ms                                                      | 31.5 ms: 1.46x slower                                                 |
| django_template            | 34.1 ms                                                      | 50.3 ms: 1.47x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 29.4 ms: 1.49x slower                                                 |
| thrift                     | 778 us                                                       | 1.16 ms: 1.50x slower                                                 |
| nbody                      | 85.1 ms                                                      | 131 ms: 1.54x slower                                                  |
| pyflate                    | 449 ms                                                       | 695 ms: 1.55x slower                                                  |
| mako                       | 11.3 ms                                                      | 17.7 ms: 1.56x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 331 us: 1.58x slower                                                  |
| python_startup             | 11.0 ms                                                      | 17.5 ms: 1.59x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 184 ms: 1.63x slower                                                  |
| comprehensions             | 16.5 us                                                      | 26.9 us: 1.63x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 9.83 ms: 1.64x slower                                                 |
| richards_super             | 51.6 ms                                                      | 85.9 ms: 1.66x slower                                                 |
| richards                   | 45.2 ms                                                      | 76.6 ms: 1.69x slower                                                 |
| logging_simple             | 6.16 us                                                      | 10.5 us: 1.70x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 504 us: 1.71x slower                                                  |
| logging_format             | 6.84 us                                                      | 11.7 us: 1.71x slower                                                 |
| sympy_str                  | 275 ms                                                       | 475 ms: 1.73x slower                                                  |
| scimark_sor                | 134 ms                                                       | 234 ms: 1.74x slower                                                  |
| logging_silent             | 103 ns                                                       | 181 ns: 1.76x slower                                                  |
| float                      | 77.5 ms                                                      | 139 ms: 1.79x slower                                                  |
| chaos                      | 57.3 ms                                                      | 104 ms: 1.81x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 119 ms: 1.82x slower                                                  |
| go                         | 141 ms                                                       | 264 ms: 1.88x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 2.99 ms: 1.92x slower                                                 |
| sqlglot_parse              | 1.25 ms                                                      | 2.58 ms: 2.07x slower                                                 |
| sympy_expand               | 457 ms                                                       | 949 ms: 2.08x slower                                                  |
| raytrace                   | 253 ms                                                       | 549 ms: 2.17x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 348 ms: 2.24x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 7.86 ms: 2.52x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 3.36 ms: 3.65x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 109 ms: 9.92x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.38x slower                                                          |

Benchmark hidden because not significant (3): regex_dna, asyncio_websockets, async_tree_memoization
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241205-3.14.0a2+-b22403e-NOGIL/bm-20241205-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-b22403e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.246x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.23x
- 95% likely to have a slowdown of 1.21x
- 99% likely to have a slowdown of 1.18x

# Memory
- memory change: 1.32x