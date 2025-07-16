# Results vs. 3.12.6

- fork: python
- ref: cb59eaefeda5ff44ac0c
- machine: linux-x86_64
- commit hash: cb59eae
- commit date: 2025-07-15
- overall geometric mean: 1.024x slower
- HPT reliability: 94.90%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 283 ms: 1.07x slower                                                  |
| docutils       | 2.64 sec                                               | 2.69 sec: 1.02x slower                                                |
| html5lib       | 63.6 ms                                                | 65.8 ms: 1.03x slower                                                 |
| Geometric mean | (ref)                                                  | 1.04x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 527 ms: 2.11x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 286 ms: 1.95x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 229 ms: 1.95x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 556 ms: 1.95x faster                                                  |
| async_tree_none            | 464 ms                                                 | 259 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 480 ms: 1.51x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 506 ms: 1.41x faster                                                  |
| async_generators           | 384 ms                                                 | 371 ms: 1.04x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.1 ms: 1.15x faster                                                 |
| pidigits       | 184 ms                                                 | 195 ms: 1.06x slower                                                  |
| nbody          | 89.3 ms                                                | 124 ms: 1.39x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.90 ms: 1.09x faster                                                 |
| regex_compile  | 142 ms                                                 | 143 ms: 1.00x slower                                                  |
| regex_v8       | 20.6 ms                                                | 21.4 ms: 1.04x slower                                                 |
| regex_dna      | 168 ms                                                 | 180 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 96.7 ms                                                | 86.8 ms: 1.11x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.13 sec: 1.01x slower                                                |
| unpickle_pure_python | 221 us                                                 | 231 us: 1.05x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 340 us: 1.11x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 95.9 ms: 1.13x slower                                                 |
| json_loads           | 26.5 us                                                | 31.1 us: 1.17x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 69.3 ms: 1.18x slower                                                 |
| json_dumps           | 10.4 ms                                                | 12.2 ms: 1.18x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.37 ms: 1.31x slower                                                 |
| python_startup         | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                 |
| Geometric mean         | (ref)                                                  | 1.44x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 57.4 ms: 1.14x slower                                                 |
| django_template | 34.7 ms                                                | 40.1 ms: 1.16x slower                                                 |
| genshi_text     | 22.8 ms                                                | 26.7 ms: 1.17x slower                                                 |
| mako            | 11.0 ms                                                | 15.4 ms: 1.40x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.21x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 527 ms: 2.11x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 286 ms: 1.95x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 229 ms: 1.95x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 556 ms: 1.95x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.31 sec: 1.84x faster                                                |
| gc_traversal               | 3.46 ms                                                | 1.90 ms: 1.82x faster                                                 |
| async_tree_none            | 464 ms                                                 | 259 ms: 1.79x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 312 ms: 1.78x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 480 ms: 1.51x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 506 ms: 1.41x faster                                                  |
| deepcopy                   | 352 us                                                 | 293 us: 1.20x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 34.9 us: 1.15x faster                                                 |
| float                      | 80.8 ms                                                | 70.1 ms: 1.15x faster                                                 |
| go                         | 139 ms                                                 | 122 ms: 1.15x faster                                                  |
| pathlib                    | 21.5 ms                                                | 19.2 ms: 1.12x faster                                                 |
| comprehensions             | 19.8 us                                                | 17.8 us: 1.12x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 86.8 ms: 1.11x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 71.4 ms: 1.10x faster                                                 |
| regex_effbot               | 3.17 ms                                                | 2.90 ms: 1.09x faster                                                 |
| bpe_tokeniser              | 4.74 sec                                               | 4.39 sec: 1.08x faster                                                |
| sqlite_synth               | 2.20 us                                                | 2.07 us: 1.07x faster                                                 |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                                  |
| pylint                     | 319 ms                                                 | 307 ms: 1.04x faster                                                  |
| async_generators           | 384 ms                                                 | 371 ms: 1.04x faster                                                  |
| generators                 | 32.2 ms                                                | 31.2 ms: 1.03x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 3.00 us: 1.03x faster                                                 |
| scimark_sor                | 130 ms                                                 | 127 ms: 1.02x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.15 sec: 1.02x faster                                                |
| logging_silent             | 109 ns                                                 | 107 ns: 1.02x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 512 ms: 1.01x faster                                                  |
| regex_compile              | 142 ms                                                 | 143 ms: 1.00x slower                                                  |
| chaos                      | 62.8 ms                                                | 63.3 ms: 1.01x slower                                                 |
| tomli_loads                | 2.11 sec                                               | 2.13 sec: 1.01x slower                                                |
| raytrace                   | 299 ms                                                 | 305 ms: 1.02x slower                                                  |
| docutils                   | 2.64 sec                                               | 2.69 sec: 1.02x slower                                                |
| spectral_norm              | 110 ms                                                 | 113 ms: 1.02x slower                                                  |
| coroutines                 | 23.9 ms                                                | 24.7 ms: 1.03x slower                                                 |
| html5lib                   | 63.6 ms                                                | 65.8 ms: 1.03x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.4 ms: 1.04x slower                                                 |
| pyflate                    | 448 ms                                                 | 465 ms: 1.04x slower                                                  |
| hexiom                     | 6.17 ms                                                | 6.43 ms: 1.04x slower                                                 |
| pprint_safe_repr           | 743 ms                                                 | 777 ms: 1.05x slower                                                  |
| logging_simple             | 6.63 us                                                | 6.94 us: 1.05x slower                                                 |
| unpickle_pure_python       | 221 us                                                 | 231 us: 1.05x slower                                                  |
| deltablue                  | 3.45 ms                                                | 3.63 ms: 1.05x slower                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.60 sec: 1.06x slower                                                |
| json                       | 5.02 ms                                                | 5.33 ms: 1.06x slower                                                 |
| pidigits                   | 184 ms                                                 | 195 ms: 1.06x slower                                                  |
| scimark_fft                | 342 ms                                                 | 364 ms: 1.07x slower                                                  |
| sympy_str                  | 292 ms                                                 | 311 ms: 1.07x slower                                                  |
| sympy_integrate            | 20.5 ms                                                | 22.0 ms: 1.07x slower                                                 |
| regex_dna                  | 168 ms                                                 | 180 ms: 1.07x slower                                                  |
| 2to3                       | 264 ms                                                 | 283 ms: 1.07x slower                                                  |
| sympy_sum                  | 166 ms                                                 | 178 ms: 1.07x slower                                                  |
| logging_format             | 7.35 us                                                | 7.95 us: 1.08x slower                                                 |
| thrift                     | 791 us                                                 | 871 us: 1.10x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 340 us: 1.11x slower                                                  |
| nqueens                    | 80.1 ms                                                | 88.7 ms: 1.11x slower                                                 |
| sympy_expand               | 468 ms                                                 | 521 ms: 1.11x slower                                                  |
| crypto_pyaes               | 76.6 ms                                                | 85.8 ms: 1.12x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 95.9 ms: 1.13x slower                                                 |
| scimark_lu                 | 114 ms                                                 | 129 ms: 1.13x slower                                                  |
| richards                   | 45.9 ms                                                | 52.0 ms: 1.13x slower                                                 |
| meteor_contest             | 104 ms                                                 | 118 ms: 1.14x slower                                                  |
| genshi_xml                 | 50.2 ms                                                | 57.4 ms: 1.14x slower                                                 |
| richards_super             | 51.9 ms                                                | 59.3 ms: 1.14x slower                                                 |
| scimark_monte_carlo        | 68.4 ms                                                | 78.3 ms: 1.14x slower                                                 |
| django_template            | 34.7 ms                                                | 40.1 ms: 1.16x slower                                                 |
| typing_runtime_protocols   | 163 us                                                 | 191 us: 1.17x slower                                                  |
| json_loads                 | 26.5 us                                                | 31.1 us: 1.17x slower                                                 |
| genshi_text                | 22.8 ms                                                | 26.7 ms: 1.17x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 69.3 ms: 1.18x slower                                                 |
| json_dumps                 | 10.4 ms                                                | 12.2 ms: 1.18x slower                                                 |
| fannkuch                   | 372 ms                                                 | 454 ms: 1.22x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.53 ms: 1.26x slower                                                 |
| python_startup_no_site     | 7.16 ms                                                | 9.37 ms: 1.31x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.48 ms: 1.35x slower                                                 |
| nbody                      | 89.3 ms                                                | 124 ms: 1.39x slower                                                  |
| mako                       | 11.0 ms                                                | 15.4 ms: 1.40x slower                                                 |
| coverage                   | 71.4 ms                                                | 112 ms: 1.57x slower                                                  |
| python_startup             | 9.93 ms                                                | 15.8 ms: 1.59x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 3.15 ms: 3.35x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 108 ms: 10.03x slower                                                 |
| telco                      | 6.53 ms                                                | 174 ms: 26.69x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.07x slower                                                          |
Ignored benchmarks (21) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250715-3.15.0a0-cb59eae-NOGIL/bm-20250715-vultr-x86_64-python-cb59eaefeda5ff44ac0c-3.15.0a0-cb59eae.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.024x slower

# HPT report

- Reliability score: 94.90% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x