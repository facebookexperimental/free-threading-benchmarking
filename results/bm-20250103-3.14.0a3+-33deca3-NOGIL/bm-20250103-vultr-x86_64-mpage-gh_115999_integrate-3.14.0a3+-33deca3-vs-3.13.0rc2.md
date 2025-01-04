# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_integrate
- machine: linux-x86_64
- commit hash: 33deca3
- commit date: 2025-01-03
- overall geometric mean: 1.089x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.33x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 312 ms: 1.20x slower                                                 |
| docutils       | 2.62 sec                                                     | 2.84 sec: 1.08x slower                                               |
| html5lib       | 67.0 ms                                                      | 72.9 ms: 1.09x slower                                                |
| Geometric mean | (ref)                                                        | 1.12x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 587 ms: 1.56x faster                                                 |
| async_tree_io              | 876 ms                                                       | 600 ms: 1.46x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 234 ms: 1.44x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 306 ms: 1.36x faster                                                 |
| async_tree_memoization     | 461 ms                                                       | 344 ms: 1.34x faster                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 478 ms: 1.33x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 512 ms: 1.30x faster                                                 |
| async_tree_none            | 354 ms                                                       | 278 ms: 1.27x faster                                                 |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.02x faster                                                |
| async_generators           | 377 ms                                                       | 419 ms: 1.11x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.25x faster                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 191 ms: 1.13x faster                                                 |
| float          | 77.5 ms                                                      | 79.1 ms: 1.02x slower                                                |
| nbody          | 85.1 ms                                                      | 132 ms: 1.55x slower                                                 |
| Geometric mean | (ref)                                                        | 1.12x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.72 ms: 1.13x faster                                                |
| regex_dna      | 180 ms                                                       | 179 ms: 1.01x faster                                                 |
| regex_v8       | 22.7 ms                                                      | 23.8 ms: 1.05x slower                                                |
| regex_compile  | 132 ms                                                       | 151 ms: 1.14x slower                                                 |
| Geometric mean | (ref)                                                        | 1.01x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.9 ms: 1.08x faster                                                |
| xml_etree_parse      | 136 ms                                                       | 130 ms: 1.05x faster                                                 |
| json_loads           | 27.0 us                                                      | 27.5 us: 1.02x slower                                                |
| xml_etree_generate   | 85.4 ms                                                      | 96.9 ms: 1.13x slower                                                |
| tomli_loads          | 2.01 sec                                                     | 2.33 sec: 1.16x slower                                               |
| xml_etree_process    | 59.3 ms                                                      | 69.0 ms: 1.16x slower                                                |
| unpickle_pure_python | 210 us                                                       | 249 us: 1.18x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 13.0 ms: 1.23x slower                                                |
| pickle_pure_python   | 294 us                                                       | 373 us: 1.27x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.11x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.71 ms: 1.31x slower                                                |
| python_startup         | 11.0 ms                                                      | 15.5 ms: 1.41x slower                                                |
| Geometric mean         | (ref)                                                        | 1.36x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|-----------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 61.2 ms: 1.25x slower                                                |
| django_template | 34.1 ms                                                      | 43.5 ms: 1.28x slower                                                |
| genshi_text     | 21.5 ms                                                      | 28.5 ms: 1.32x slower                                                |
| mako            | 11.3 ms                                                      | 15.8 ms: 1.39x slower                                                |
| Geometric mean  | (ref)                                                        | 1.31x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------------------|:------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 587 ms: 1.56x faster                                                 |
| async_tree_io              | 876 ms                                                       | 600 ms: 1.46x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 234 ms: 1.44x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 306 ms: 1.36x faster                                                 |
| async_tree_memoization     | 461 ms                                                       | 344 ms: 1.34x faster                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 478 ms: 1.33x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 512 ms: 1.30x faster                                                 |
| async_tree_none            | 354 ms                                                       | 278 ms: 1.27x faster                                                 |
| pidigits                   | 217 ms                                                       | 191 ms: 1.13x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.72 ms: 1.13x faster                                                |
| deepcopy                   | 355 us                                                       | 318 us: 1.12x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.9 ms: 1.08x faster                                                |
| sqlite_synth               | 2.21 us                                                      | 2.06 us: 1.07x faster                                                |
| xml_etree_parse            | 136 ms                                                       | 130 ms: 1.05x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 18.7 ms: 1.03x faster                                                |
| json                       | 4.93 ms                                                      | 4.84 ms: 1.02x faster                                                |
| coroutines                 | 23.6 ms                                                      | 23.2 ms: 1.02x faster                                                |
| spectral_norm              | 111 ms                                                       | 110 ms: 1.01x faster                                                 |
| deepcopy_memo              | 39.1 us                                                      | 38.7 us: 1.01x faster                                                |
| regex_dna                  | 180 ms                                                       | 179 ms: 1.01x faster                                                 |
| go                         | 141 ms                                                       | 140 ms: 1.01x faster                                                 |
| scimark_sor                | 134 ms                                                       | 136 ms: 1.01x slower                                                 |
| json_loads                 | 27.0 us                                                      | 27.5 us: 1.02x slower                                                |
| float                      | 77.5 ms                                                      | 79.1 ms: 1.02x slower                                                |
| regex_v8                   | 22.7 ms                                                      | 23.8 ms: 1.05x slower                                                |
| gc_traversal               | 3.14 ms                                                      | 3.30 ms: 1.05x slower                                                |
| bpe_tokeniser              | 4.45 sec                                                     | 4.76 sec: 1.07x slower                                               |
| deepcopy_reduce            | 3.11 us                                                      | 3.34 us: 1.07x slower                                                |
| pycparser                  | 1.12 sec                                                     | 1.21 sec: 1.08x slower                                               |
| docutils                   | 2.62 sec                                                     | 2.84 sec: 1.08x slower                                               |
| html5lib                   | 67.0 ms                                                      | 72.9 ms: 1.09x slower                                                |
| pyflate                    | 449 ms                                                       | 488 ms: 1.09x slower                                                 |
| scimark_fft                | 349 ms                                                       | 382 ms: 1.09x slower                                                 |
| dulwich_log                | 74.8 ms                                                      | 81.8 ms: 1.09x slower                                                |
| generators                 | 28.8 ms                                                      | 31.6 ms: 1.10x slower                                                |
| mdp                        | 2.36 sec                                                     | 2.60 sec: 1.10x slower                                               |
| async_generators           | 377 ms                                                       | 419 ms: 1.11x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 819 ms: 1.11x slower                                                 |
| telco                      | 7.82 ms                                                      | 8.73 ms: 1.12x slower                                                |
| pprint_pformat             | 1.50 sec                                                     | 1.70 sec: 1.13x slower                                               |
| xml_etree_generate         | 85.4 ms                                                      | 96.9 ms: 1.13x slower                                                |
| regex_compile              | 132 ms                                                       | 151 ms: 1.14x slower                                                 |
| logging_silent             | 103 ns                                                       | 117 ns: 1.14x slower                                                 |
| sqlglot_normalize          | 106 ms                                                       | 122 ms: 1.16x slower                                                 |
| tomli_loads                | 2.01 sec                                                     | 2.33 sec: 1.16x slower                                               |
| xml_etree_process          | 59.3 ms                                                      | 69.0 ms: 1.16x slower                                                |
| unpickle_pure_python       | 210 us                                                       | 249 us: 1.18x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 62.5 ms: 1.19x slower                                                |
| thrift                     | 778 us                                                       | 926 us: 1.19x slower                                                 |
| coverage                   | 83.0 ms                                                      | 98.8 ms: 1.19x slower                                                |
| sympy_sum                  | 156 ms                                                       | 186 ms: 1.19x slower                                                 |
| logging_simple             | 6.16 us                                                      | 7.35 us: 1.19x slower                                                |
| 2to3                       | 260 ms                                                       | 312 ms: 1.20x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.67 ms: 1.21x slower                                                |
| logging_format             | 6.84 us                                                      | 8.29 us: 1.21x slower                                                |
| sympy_expand               | 457 ms                                                       | 554 ms: 1.21x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 24.3 ms: 1.22x slower                                                |
| sympy_str                  | 275 ms                                                       | 336 ms: 1.22x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 13.0 ms: 1.23x slower                                                |
| richards                   | 45.2 ms                                                      | 56.0 ms: 1.24x slower                                                |
| nqueens                    | 78.6 ms                                                      | 97.6 ms: 1.24x slower                                                |
| chaos                      | 57.3 ms                                                      | 71.3 ms: 1.24x slower                                                |
| sqlglot_transpile          | 1.56 ms                                                      | 1.94 ms: 1.25x slower                                                |
| hexiom                     | 5.99 ms                                                      | 7.51 ms: 1.25x slower                                                |
| genshi_xml                 | 48.8 ms                                                      | 61.2 ms: 1.25x slower                                                |
| scimark_monte_carlo        | 65.4 ms                                                      | 82.3 ms: 1.26x slower                                                |
| meteor_contest             | 102 ms                                                       | 128 ms: 1.26x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 142 ms: 1.26x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 373 us: 1.27x slower                                                 |
| richards_super             | 51.6 ms                                                      | 65.4 ms: 1.27x slower                                                |
| django_template            | 34.1 ms                                                      | 43.5 ms: 1.28x slower                                                |
| crypto_pyaes               | 67.9 ms                                                      | 86.7 ms: 1.28x slower                                                |
| comprehensions             | 16.5 us                                                      | 21.0 us: 1.28x slower                                                |
| sqlglot_parse              | 1.25 ms                                                      | 1.60 ms: 1.28x slower                                                |
| typing_runtime_protocols   | 155 us                                                       | 199 us: 1.29x slower                                                 |
| fannkuch                   | 370 ms                                                       | 480 ms: 1.30x slower                                                 |
| raytrace                   | 253 ms                                                       | 331 ms: 1.31x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 9.71 ms: 1.31x slower                                                |
| genshi_text                | 21.5 ms                                                      | 28.5 ms: 1.32x slower                                                |
| create_gc_cycles           | 1.34 ms                                                      | 1.80 ms: 1.35x slower                                                |
| mako                       | 11.3 ms                                                      | 15.8 ms: 1.39x slower                                                |
| python_startup             | 11.0 ms                                                      | 15.5 ms: 1.41x slower                                                |
| deltablue                  | 3.12 ms                                                      | 4.80 ms: 1.54x slower                                                |
| nbody                      | 85.1 ms                                                      | 132 ms: 1.55x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 3.34 ms: 3.63x slower                                                |
| bench_mp_pool              | 11.0 ms                                                      | 97.8 ms: 8.90x slower                                                |
| Geometric mean             | (ref)                                                        | 1.14x slower                                                         |

Benchmark hidden because not significant (2): asyncio_websockets, pylint
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20250103-3.14.0a3+-33deca3-NOGIL/bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.089x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.33x