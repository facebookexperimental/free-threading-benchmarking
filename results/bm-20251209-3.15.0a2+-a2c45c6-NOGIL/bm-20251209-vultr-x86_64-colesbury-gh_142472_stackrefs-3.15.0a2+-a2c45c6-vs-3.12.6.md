# Results vs. 3.12.6

- fork: colesbury
- ref: gh_142472_stackrefs
- machine: linux-x86_64
- commit hash: a2c45c6
- commit date: 2025-12-09
- overall geometric mean: 1.027x slower
- HPT reliability: 82.89%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 277 ms: 1.05x slower                                                     |
| docutils       | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                   |
| html5lib       | 63.6 ms                                                | 65.9 ms: 1.04x slower                                                    |
| Geometric mean | (ref)                                                  | 1.04x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 611 ms: 1.82x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 623 ms: 1.74x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 329 ms: 1.70x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 269 ms: 1.66x faster                                                     |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 355 ms: 1.56x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 540 ms: 1.34x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 560 ms: 1.28x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 510 ms: 1.01x faster                                                     |
| async_generators           | 384 ms                                                 | 380 ms: 1.01x faster                                                     |
| Geometric mean             | (ref)                                                  | 1.40x faster                                                             |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.3 ms: 1.12x faster                                                    |
| pidigits       | 184 ms                                                 | 215 ms: 1.17x slower                                                     |
| nbody          | 89.3 ms                                                | 121 ms: 1.36x slower                                                     |
| Geometric mean | (ref)                                                  | 1.12x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.87 ms: 1.10x faster                                                    |
| regex_compile  | 142 ms                                                 | 141 ms: 1.01x faster                                                     |
| regex_v8       | 20.6 ms                                                | 22.1 ms: 1.07x slower                                                    |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                                     |
| Geometric mean | (ref)                                                  | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 133 ms: 1.04x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 93.5 ms: 1.03x faster                                                    |
| json_dumps           | 10.4 ms                                                | 10.7 ms: 1.04x slower                                                    |
| unpickle_pure_python | 221 us                                                 | 233 us: 1.06x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 330 us: 1.07x slower                                                     |
| tomli_loads          | 2.11 sec                                               | 2.29 sec: 1.08x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 95.3 ms: 1.12x slower                                                    |
| xml_etree_process    | 59.0 ms                                                | 68.1 ms: 1.16x slower                                                    |
| json_loads           | 26.5 us                                                | 31.9 us: 1.20x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.70 ms: 1.36x slower                                                    |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.47x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 56.9 ms: 1.13x slower                                                    |
| genshi_text     | 22.8 ms                                                | 26.3 ms: 1.15x slower                                                    |
| django_template | 34.7 ms                                                | 40.4 ms: 1.16x slower                                                    |
| mako            | 11.0 ms                                                | 15.5 ms: 1.41x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.21x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| mdp                        | 2.42 sec                                               | 1.30 sec: 1.86x faster                                                   |
| gc_traversal               | 3.46 ms                                                | 1.90 ms: 1.82x faster                                                    |
| async_tree_io_tg           | 1.11 sec                                               | 611 ms: 1.82x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 623 ms: 1.74x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 329 ms: 1.70x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 269 ms: 1.66x faster                                                     |
| async_tree_none            | 464 ms                                                 | 287 ms: 1.62x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 355 ms: 1.56x faster                                                     |
| bench_mp_pool              | 10.8 ms                                                | 7.30 ms: 1.48x faster                                                    |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 540 ms: 1.34x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 30.3 us: 1.33x faster                                                    |
| deepcopy                   | 352 us                                                 | 272 us: 1.29x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 560 ms: 1.28x faster                                                     |
| pathlib                    | 21.5 ms                                                | 17.7 ms: 1.22x faster                                                    |
| go                         | 139 ms                                                 | 118 ms: 1.18x faster                                                     |
| comprehensions             | 19.8 us                                                | 17.4 us: 1.14x faster                                                    |
| float                      | 80.8 ms                                                | 72.3 ms: 1.12x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.87 ms: 1.10x faster                                                    |
| bpe_tokeniser              | 4.74 sec                                               | 4.30 sec: 1.10x faster                                                   |
| dulwich_log                | 78.9 ms                                                | 71.9 ms: 1.10x faster                                                    |
| scimark_sor                | 130 ms                                                 | 120 ms: 1.09x faster                                                     |
| generators                 | 32.2 ms                                                | 30.3 ms: 1.06x faster                                                    |
| deepcopy_reduce            | 3.08 us                                                | 2.90 us: 1.06x faster                                                    |
| logging_silent             | 109 ns                                                 | 103 ns: 1.06x faster                                                     |
| pylint                     | 319 ms                                                 | 302 ms: 1.06x faster                                                     |
| sqlite_synth               | 2.20 us                                                | 2.09 us: 1.05x faster                                                    |
| xml_etree_parse            | 139 ms                                                 | 133 ms: 1.04x faster                                                     |
| pycparser                  | 1.17 sec                                               | 1.13 sec: 1.04x faster                                                   |
| xml_etree_iterparse        | 96.7 ms                                                | 93.5 ms: 1.03x faster                                                    |
| spectral_norm              | 110 ms                                                 | 108 ms: 1.02x faster                                                     |
| chaos                      | 62.8 ms                                                | 61.7 ms: 1.02x faster                                                    |
| asyncio_websockets         | 517 ms                                                 | 510 ms: 1.01x faster                                                     |
| raytrace                   | 299 ms                                                 | 296 ms: 1.01x faster                                                     |
| async_generators           | 384 ms                                                 | 380 ms: 1.01x faster                                                     |
| regex_compile              | 142 ms                                                 | 141 ms: 1.01x faster                                                     |
| pyflate                    | 448 ms                                                 | 451 ms: 1.01x slower                                                     |
| scimark_fft                | 342 ms                                                 | 344 ms: 1.01x slower                                                     |
| hexiom                     | 6.17 ms                                                | 6.23 ms: 1.01x slower                                                    |
| logging_simple             | 6.63 us                                                | 6.77 us: 1.02x slower                                                    |
| docutils                   | 2.64 sec                                               | 2.70 sec: 1.02x slower                                                   |
| pprint_safe_repr           | 743 ms                                                 | 767 ms: 1.03x slower                                                     |
| html5lib                   | 63.6 ms                                                | 65.9 ms: 1.04x slower                                                    |
| json_dumps                 | 10.4 ms                                                | 10.7 ms: 1.04x slower                                                    |
| pprint_pformat             | 1.52 sec                                               | 1.59 sec: 1.05x slower                                                   |
| sympy_str                  | 292 ms                                                 | 306 ms: 1.05x slower                                                     |
| sympy_integrate            | 20.5 ms                                                | 21.6 ms: 1.05x slower                                                    |
| 2to3                       | 264 ms                                                 | 277 ms: 1.05x slower                                                     |
| logging_format             | 7.35 us                                                | 7.76 us: 1.06x slower                                                    |
| unpickle_pure_python       | 221 us                                                 | 233 us: 1.06x slower                                                     |
| sympy_sum                  | 166 ms                                                 | 176 ms: 1.06x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 330 us: 1.07x slower                                                     |
| regex_v8                   | 20.6 ms                                                | 22.1 ms: 1.07x slower                                                    |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                                     |
| json                       | 5.02 ms                                                | 5.45 ms: 1.08x slower                                                    |
| tomli_loads                | 2.11 sec                                               | 2.29 sec: 1.08x slower                                                   |
| nqueens                    | 80.1 ms                                                | 87.5 ms: 1.09x slower                                                    |
| thrift                     | 791 us                                                 | 865 us: 1.09x slower                                                     |
| deltablue                  | 3.45 ms                                                | 3.77 ms: 1.09x slower                                                    |
| sympy_expand               | 468 ms                                                 | 520 ms: 1.11x slower                                                     |
| richards                   | 45.9 ms                                                | 51.1 ms: 1.11x slower                                                    |
| crypto_pyaes               | 76.6 ms                                                | 85.3 ms: 1.11x slower                                                    |
| xml_etree_generate         | 85.2 ms                                                | 95.3 ms: 1.12x slower                                                    |
| scimark_monte_carlo        | 68.4 ms                                                | 76.7 ms: 1.12x slower                                                    |
| scimark_lu                 | 114 ms                                                 | 128 ms: 1.13x slower                                                     |
| richards_super             | 51.9 ms                                                | 58.6 ms: 1.13x slower                                                    |
| genshi_xml                 | 50.2 ms                                                | 56.9 ms: 1.13x slower                                                    |
| meteor_contest             | 104 ms                                                 | 119 ms: 1.15x slower                                                     |
| genshi_text                | 22.8 ms                                                | 26.3 ms: 1.15x slower                                                    |
| xml_etree_process          | 59.0 ms                                                | 68.1 ms: 1.16x slower                                                    |
| typing_runtime_protocols   | 163 us                                                 | 190 us: 1.16x slower                                                     |
| django_template            | 34.7 ms                                                | 40.4 ms: 1.16x slower                                                    |
| pidigits                   | 184 ms                                                 | 215 ms: 1.17x slower                                                     |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.25 ms: 1.19x slower                                                    |
| json_loads                 | 26.5 us                                                | 31.9 us: 1.20x slower                                                    |
| fannkuch                   | 372 ms                                                 | 456 ms: 1.22x slower                                                     |
| create_gc_cycles           | 1.09 ms                                                | 1.48 ms: 1.35x slower                                                    |
| python_startup_no_site     | 7.16 ms                                                | 9.70 ms: 1.36x slower                                                    |
| nbody                      | 89.3 ms                                                | 121 ms: 1.36x slower                                                     |
| mako                       | 11.0 ms                                                | 15.5 ms: 1.41x slower                                                    |
| coverage                   | 71.4 ms                                                | 111 ms: 1.56x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 1.47 ms: 1.57x slower                                                    |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                    |
| telco                      | 6.53 ms                                                | 175 ms: 26.78x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                             |

Benchmark hidden because not significant (1): coroutines
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251209-3.15.0a2+-a2c45c6-NOGIL/bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.027x slower

# HPT report

- Reliability score: 82.89% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x