# Results vs. 3.13.0rc2

- fork: corona10
- ref: gh_115999_BINARY_SUB
- machine: linux-x86_64
- commit hash: 3aa9426
- commit date: 2024-12-17
- overall geometric mean: 1.250x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.20x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 368 ms: 1.42x slower                                                     |
| docutils       | 2.62 sec                                                     | 3.11 sec: 1.19x slower                                                   |
| html5lib       | 67.0 ms                                                      | 98.4 ms: 1.47x slower                                                    |
| Geometric mean | (ref)                                                        | 1.35x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 827 ms: 1.10x faster                                                     |
| async_tree_io              | 876 ms                                                       | 849 ms: 1.03x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 622 ms: 1.02x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 651 ms: 1.02x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                     |
| async_tree_none_tg         | 336 ms                                                       | 358 ms: 1.06x slower                                                     |
| coroutines                 | 23.6 ms                                                      | 25.2 ms: 1.07x slower                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 445 ms: 1.07x slower                                                     |
| async_tree_none            | 354 ms                                                       | 389 ms: 1.10x slower                                                     |
| async_generators           | 377 ms                                                       | 461 ms: 1.22x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                             |

Benchmark hidden because not significant (1): async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.20x faster                                                     |
| nbody          | 85.1 ms                                                      | 132 ms: 1.56x slower                                                     |
| float          | 77.5 ms                                                      | 141 ms: 1.82x slower                                                     |
| Geometric mean | (ref)                                                        | 1.33x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.90 ms: 1.06x faster                                                    |
| regex_dna      | 180 ms                                                       | 177 ms: 1.02x faster                                                     |
| regex_v8       | 22.7 ms                                                      | 24.8 ms: 1.09x slower                                                    |
| regex_compile  | 132 ms                                                       | 179 ms: 1.35x slower                                                     |
| Geometric mean | (ref)                                                        | 1.08x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 91.9 ms: 1.03x faster                                                    |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.03x faster                                                     |
| json_loads           | 27.0 us                                                      | 28.7 us: 1.06x slower                                                    |
| xml_etree_generate   | 85.4 ms                                                      | 98.0 ms: 1.15x slower                                                    |
| xml_etree_process    | 59.3 ms                                                      | 78.2 ms: 1.32x slower                                                    |
| tomli_loads          | 2.01 sec                                                     | 2.69 sec: 1.34x slower                                                   |
| json_dumps           | 10.5 ms                                                      | 14.2 ms: 1.35x slower                                                    |
| unpickle_pure_python | 210 us                                                       | 333 us: 1.59x slower                                                     |
| pickle_pure_python   | 294 us                                                       | 517 us: 1.76x slower                                                     |
| Geometric mean       | (ref)                                                        | 1.25x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                    |
| python_startup         | 11.0 ms                                                      | 17.5 ms: 1.59x slower                                                    |
| Geometric mean         | (ref)                                                        | 1.49x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 64.7 ms: 1.33x slower                                                    |
| genshi_text     | 21.5 ms                                                      | 32.2 ms: 1.49x slower                                                    |
| django_template | 34.1 ms                                                      | 51.4 ms: 1.50x slower                                                    |
| mako            | 11.3 ms                                                      | 17.8 ms: 1.57x slower                                                    |
| Geometric mean  | (ref)                                                        | 1.47x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                   | 217 ms                                                       | 181 ms: 1.20x faster                                                     |
| async_tree_io_tg           | 913 ms                                                       | 827 ms: 1.10x faster                                                     |
| deepcopy                   | 355 us                                                       | 331 us: 1.07x faster                                                     |
| regex_effbot               | 3.08 ms                                                      | 2.90 ms: 1.06x faster                                                    |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.9 ms: 1.03x faster                                                    |
| async_tree_io              | 876 ms                                                       | 849 ms: 1.03x faster                                                     |
| xml_etree_parse            | 136 ms                                                       | 132 ms: 1.03x faster                                                     |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 622 ms: 1.02x faster                                                     |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 651 ms: 1.02x faster                                                     |
| regex_dna                  | 180 ms                                                       | 177 ms: 1.02x faster                                                     |
| asyncio_websockets         | 520 ms                                                       | 518 ms: 1.00x faster                                                     |
| deepcopy_memo              | 39.1 us                                                      | 39.9 us: 1.02x slower                                                    |
| sqlite_synth               | 2.21 us                                                      | 2.27 us: 1.03x slower                                                    |
| json                       | 4.93 ms                                                      | 5.09 ms: 1.03x slower                                                    |
| pathlib                    | 19.2 ms                                                      | 19.8 ms: 1.03x slower                                                    |
| json_loads                 | 27.0 us                                                      | 28.7 us: 1.06x slower                                                    |
| async_tree_none_tg         | 336 ms                                                       | 358 ms: 1.06x slower                                                     |
| coroutines                 | 23.6 ms                                                      | 25.2 ms: 1.07x slower                                                    |
| async_tree_memoization_tg  | 414 ms                                                       | 445 ms: 1.07x slower                                                     |
| regex_v8                   | 22.7 ms                                                      | 24.8 ms: 1.09x slower                                                    |
| async_tree_none            | 354 ms                                                       | 389 ms: 1.10x slower                                                     |
| telco                      | 7.82 ms                                                      | 8.67 ms: 1.11x slower                                                    |
| gc_traversal               | 3.14 ms                                                      | 3.52 ms: 1.12x slower                                                    |
| bpe_tokeniser              | 4.45 sec                                                     | 5.02 sec: 1.13x slower                                                   |
| spectral_norm              | 111 ms                                                       | 126 ms: 1.13x slower                                                     |
| deepcopy_reduce            | 3.11 us                                                      | 3.53 us: 1.13x slower                                                    |
| xml_etree_generate         | 85.4 ms                                                      | 98.0 ms: 1.15x slower                                                    |
| scimark_fft                | 349 ms                                                       | 414 ms: 1.18x slower                                                     |
| docutils                   | 2.62 sec                                                     | 3.11 sec: 1.19x slower                                                   |
| pylint                     | 317 ms                                                       | 382 ms: 1.20x slower                                                     |
| mdp                        | 2.36 sec                                                     | 2.84 sec: 1.20x slower                                                   |
| async_generators           | 377 ms                                                       | 461 ms: 1.22x slower                                                     |
| coverage                   | 83.0 ms                                                      | 103 ms: 1.25x slower                                                     |
| nqueens                    | 78.6 ms                                                      | 98.0 ms: 1.25x slower                                                    |
| dulwich_log                | 74.8 ms                                                      | 95.7 ms: 1.28x slower                                                    |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                     |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 6.10 ms: 1.30x slower                                                    |
| sqlglot_normalize          | 106 ms                                                       | 138 ms: 1.30x slower                                                     |
| sqlglot_optimize           | 52.7 ms                                                      | 69.2 ms: 1.31x slower                                                    |
| xml_etree_process          | 59.3 ms                                                      | 78.2 ms: 1.32x slower                                                    |
| genshi_xml                 | 48.8 ms                                                      | 64.7 ms: 1.33x slower                                                    |
| pprint_safe_repr           | 738 ms                                                       | 981 ms: 1.33x slower                                                     |
| typing_runtime_protocols   | 155 us                                                       | 207 us: 1.34x slower                                                     |
| tomli_loads                | 2.01 sec                                                     | 2.69 sec: 1.34x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 14.2 ms: 1.35x slower                                                    |
| generators                 | 28.8 ms                                                      | 38.8 ms: 1.35x slower                                                    |
| regex_compile              | 132 ms                                                       | 179 ms: 1.35x slower                                                     |
| pprint_pformat             | 1.50 sec                                                     | 2.04 sec: 1.36x slower                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 92.6 ms: 1.36x slower                                                    |
| pycparser                  | 1.12 sec                                                     | 1.53 sec: 1.37x slower                                                   |
| create_gc_cycles           | 1.34 ms                                                      | 1.84 ms: 1.38x slower                                                    |
| scimark_lu                 | 113 ms                                                       | 155 ms: 1.38x slower                                                     |
| fannkuch                   | 370 ms                                                       | 512 ms: 1.38x slower                                                     |
| python_startup_no_site     | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                    |
| 2to3                       | 260 ms                                                       | 368 ms: 1.42x slower                                                     |
| html5lib                   | 67.0 ms                                                      | 98.4 ms: 1.47x slower                                                    |
| thrift                     | 778 us                                                       | 1.15 ms: 1.48x slower                                                    |
| sympy_integrate            | 19.8 ms                                                      | 29.5 ms: 1.49x slower                                                    |
| genshi_text                | 21.5 ms                                                      | 32.2 ms: 1.49x slower                                                    |
| django_template            | 34.1 ms                                                      | 51.4 ms: 1.50x slower                                                    |
| pyflate                    | 449 ms                                                       | 696 ms: 1.55x slower                                                     |
| nbody                      | 85.1 ms                                                      | 132 ms: 1.56x slower                                                     |
| mako                       | 11.3 ms                                                      | 17.8 ms: 1.57x slower                                                    |
| unpickle_pure_python       | 210 us                                                       | 333 us: 1.59x slower                                                     |
| python_startup             | 11.0 ms                                                      | 17.5 ms: 1.59x slower                                                    |
| hexiom                     | 5.99 ms                                                      | 9.71 ms: 1.62x slower                                                    |
| comprehensions             | 16.5 us                                                      | 27.2 us: 1.65x slower                                                    |
| scimark_sor                | 134 ms                                                       | 224 ms: 1.67x slower                                                     |
| richards_super             | 51.6 ms                                                      | 86.3 ms: 1.67x slower                                                    |
| richards                   | 45.2 ms                                                      | 76.4 ms: 1.69x slower                                                    |
| sympy_str                  | 275 ms                                                       | 477 ms: 1.74x slower                                                     |
| logging_simple             | 6.16 us                                                      | 10.7 us: 1.74x slower                                                    |
| logging_format             | 6.84 us                                                      | 12.0 us: 1.75x slower                                                    |
| pickle_pure_python         | 294 us                                                       | 517 us: 1.76x slower                                                     |
| logging_silent             | 103 ns                                                       | 184 ns: 1.79x slower                                                     |
| scimark_monte_carlo        | 65.4 ms                                                      | 118 ms: 1.81x slower                                                     |
| float                      | 77.5 ms                                                      | 141 ms: 1.82x slower                                                     |
| chaos                      | 57.3 ms                                                      | 104 ms: 1.82x slower                                                     |
| go                         | 141 ms                                                       | 269 ms: 1.91x slower                                                     |
| sqlglot_transpile          | 1.56 ms                                                      | 3.02 ms: 1.93x slower                                                    |
| sqlglot_parse              | 1.25 ms                                                      | 2.60 ms: 2.08x slower                                                    |
| sympy_expand               | 457 ms                                                       | 956 ms: 2.09x slower                                                     |
| raytrace                   | 253 ms                                                       | 548 ms: 2.17x slower                                                     |
| sympy_sum                  | 156 ms                                                       | 350 ms: 2.25x slower                                                     |
| deltablue                  | 3.12 ms                                                      | 7.94 ms: 2.54x slower                                                    |
| bench_thread_pool          | 919 us                                                       | 3.43 ms: 3.73x slower                                                    |
| bench_mp_pool              | 11.0 ms                                                      | 109 ms: 9.89x slower                                                     |
| Geometric mean             | (ref)                                                        | 1.38x slower                                                             |

Benchmark hidden because not significant (1): async_tree_memoization
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241217-3.14.0a2+-3aa9426-NOGIL/bm-20241217-vultr-x86_64-corona10-gh_115999_BINARY_SUB-3.14.0a2+-3aa9426.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.250x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.24x
- 95% likely to have a slowdown of 1.23x
- 99% likely to have a slowdown of 1.20x

# Memory
- memory change: 1.32x