# Results vs. 3.12.6

- fork: python
- ref: 910a92babf40b7b34baa
- machine: linux-x86_64
- commit hash: 910a92b
- commit date: 2026-11-16
- overall geometric mean: 1.026x slower
- HPT reliability: 60.89%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 290 ms: 1.10x slower                                                      |
| docutils       | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                    |
| html5lib       | 63.6 ms                                                | 64.6 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                  | 1.06x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 698 ms: 1.59x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 722 ms: 1.50x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 398 ms: 1.41x faster                                                      |
| async_tree_none            | 464 ms                                                 | 341 ms: 1.36x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 414 ms: 1.34x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 334 ms: 1.34x faster                                                      |
| async_generators           | 384 ms                                                 | 293 ms: 1.31x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 571 ms: 1.27x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 583 ms: 1.23x faster                                                      |
| asyncio_websockets         | 517 ms                                                 | 502 ms: 1.03x faster                                                      |
| coroutines                 | 23.9 ms                                                | 26.2 ms: 1.09x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.28x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 184 ms: 1.00x faster                                                      |
| float          | 80.8 ms                                                | 84.9 ms: 1.05x slower                                                     |
| nbody          | 89.3 ms                                                | 117 ms: 1.31x slower                                                      |
| Geometric mean | (ref)                                                  | 1.11x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.90 ms: 1.09x faster                                                     |
| regex_v8       | 20.6 ms                                                | 20.3 ms: 1.02x faster                                                     |
| regex_dna      | 168 ms                                                 | 172 ms: 1.02x slower                                                      |
| regex_compile  | 142 ms                                                 | 169 ms: 1.19x slower                                                      |
| Geometric mean | (ref)                                                  | 1.02x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.98 sec: 1.06x faster                                                    |
| json_dumps           | 10.4 ms                                                | 10.1 ms: 1.03x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 96.3 ms: 1.00x faster                                                     |
| xml_etree_parse      | 139 ms                                                 | 143 ms: 1.03x slower                                                      |
| unpickle_pure_python | 221 us                                                 | 241 us: 1.09x slower                                                      |
| pickle_pure_python   | 308 us                                                 | 345 us: 1.12x slower                                                      |
| xml_etree_generate   | 85.2 ms                                                | 98.3 ms: 1.15x slower                                                     |
| json_loads           | 26.5 us                                                | 31.3 us: 1.18x slower                                                     |
| xml_etree_process    | 59.0 ms                                                | 75.4 ms: 1.28x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.88 ms: 1.24x slower                                                     |
| python_startup         | 9.93 ms                                                | 13.4 ms: 1.35x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.29x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 41.7 ms: 1.20x slower                                                     |
| mako            | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.31x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 115 ms: 2.76x faster                                                      |
| gc_traversal               | 3.46 ms                                                | 1.79 ms: 1.93x faster                                                     |
| mdp                        | 2.42 sec                                               | 1.29 sec: 1.88x faster                                                    |
| bench_mp_pool              | 10.8 ms                                                | 6.66 ms: 1.62x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 698 ms: 1.59x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 722 ms: 1.50x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 398 ms: 1.41x faster                                                      |
| async_tree_none            | 464 ms                                                 | 341 ms: 1.36x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 414 ms: 1.34x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 334 ms: 1.34x faster                                                      |
| deepcopy                   | 352 us                                                 | 265 us: 1.33x faster                                                      |
| async_generators           | 384 ms                                                 | 293 ms: 1.31x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 571 ms: 1.27x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 583 ms: 1.23x faster                                                      |
| deepcopy_memo              | 40.3 us                                                | 32.9 us: 1.22x faster                                                     |
| pathlib                    | 21.5 ms                                                | 18.1 ms: 1.19x faster                                                     |
| typing_runtime_protocols   | 163 us                                                 | 137 us: 1.19x faster                                                      |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                      |
| bpe_tokeniser              | 4.74 sec                                               | 4.23 sec: 1.12x faster                                                    |
| comprehensions             | 19.8 us                                                | 17.8 us: 1.11x faster                                                     |
| dulwich_log                | 78.9 ms                                                | 70.9 ms: 1.11x faster                                                     |
| regex_effbot               | 3.17 ms                                                | 2.90 ms: 1.09x faster                                                     |
| scimark_sor                | 130 ms                                                 | 119 ms: 1.09x faster                                                      |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.08x faster                                                     |
| spectral_norm              | 110 ms                                                 | 103 ms: 1.07x faster                                                      |
| tomli_loads                | 2.11 sec                                               | 1.98 sec: 1.06x faster                                                    |
| deepcopy_reduce            | 3.08 us                                                | 2.96 us: 1.04x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 502 ms: 1.03x faster                                                      |
| pyflate                    | 448 ms                                                 | 436 ms: 1.03x faster                                                      |
| chaos                      | 62.8 ms                                                | 61.2 ms: 1.03x faster                                                     |
| json_dumps                 | 10.4 ms                                                | 10.1 ms: 1.03x faster                                                     |
| regex_v8                   | 20.6 ms                                                | 20.3 ms: 1.02x faster                                                     |
| scimark_fft                | 342 ms                                                 | 337 ms: 1.01x faster                                                      |
| raytrace                   | 299 ms                                                 | 295 ms: 1.01x faster                                                      |
| pycparser                  | 1.17 sec                                               | 1.16 sec: 1.00x faster                                                    |
| xml_etree_iterparse        | 96.7 ms                                                | 96.3 ms: 1.00x faster                                                     |
| pidigits                   | 184 ms                                                 | 184 ms: 1.00x faster                                                      |
| html5lib                   | 63.6 ms                                                | 64.6 ms: 1.02x slower                                                     |
| regex_dna                  | 168 ms                                                 | 172 ms: 1.02x slower                                                      |
| xml_etree_parse            | 139 ms                                                 | 143 ms: 1.03x slower                                                      |
| logging_simple             | 6.63 us                                                | 6.94 us: 1.05x slower                                                     |
| generators                 | 32.2 ms                                                | 33.9 ms: 1.05x slower                                                     |
| hexiom                     | 6.17 ms                                                | 6.48 ms: 1.05x slower                                                     |
| float                      | 80.8 ms                                                | 84.9 ms: 1.05x slower                                                     |
| docutils                   | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 21.9 ms: 1.07x slower                                                     |
| deltablue                  | 3.45 ms                                                | 3.71 ms: 1.08x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 800 ms: 1.08x slower                                                      |
| nqueens                    | 80.1 ms                                                | 86.7 ms: 1.08x slower                                                     |
| logging_format             | 7.35 us                                                | 7.98 us: 1.09x slower                                                     |
| pprint_pformat             | 1.52 sec                                               | 1.65 sec: 1.09x slower                                                    |
| json                       | 5.02 ms                                                | 5.47 ms: 1.09x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 241 us: 1.09x slower                                                      |
| coroutines                 | 23.9 ms                                                | 26.2 ms: 1.09x slower                                                     |
| sympy_sum                  | 166 ms                                                 | 182 ms: 1.10x slower                                                      |
| sympy_str                  | 292 ms                                                 | 320 ms: 1.10x slower                                                      |
| 2to3                       | 264 ms                                                 | 290 ms: 1.10x slower                                                      |
| pickle_pure_python         | 308 us                                                 | 345 us: 1.12x slower                                                      |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.97 ms: 1.13x slower                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 77.7 ms: 1.13x slower                                                     |
| sympy_expand               | 468 ms                                                 | 534 ms: 1.14x slower                                                      |
| crypto_pyaes               | 76.6 ms                                                | 87.7 ms: 1.15x slower                                                     |
| scimark_lu                 | 114 ms                                                 | 131 ms: 1.15x slower                                                      |
| xml_etree_generate         | 85.2 ms                                                | 98.3 ms: 1.15x slower                                                     |
| richards                   | 45.9 ms                                                | 53.3 ms: 1.16x slower                                                     |
| richards_super             | 51.9 ms                                                | 60.7 ms: 1.17x slower                                                     |
| json_loads                 | 26.5 us                                                | 31.3 us: 1.18x slower                                                     |
| regex_compile              | 142 ms                                                 | 169 ms: 1.19x slower                                                      |
| thrift                     | 791 us                                                 | 947 us: 1.20x slower                                                      |
| django_template            | 34.7 ms                                                | 41.7 ms: 1.20x slower                                                     |
| meteor_contest             | 104 ms                                                 | 125 ms: 1.21x slower                                                      |
| create_gc_cycles           | 1.09 ms                                                | 1.33 ms: 1.22x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 8.88 ms: 1.24x slower                                                     |
| fannkuch                   | 372 ms                                                 | 468 ms: 1.26x slower                                                      |
| xml_etree_process          | 59.0 ms                                                | 75.4 ms: 1.28x slower                                                     |
| nbody                      | 89.3 ms                                                | 117 ms: 1.31x slower                                                      |
| python_startup             | 9.93 ms                                                | 13.4 ms: 1.35x slower                                                     |
| mako                       | 11.0 ms                                                | 15.7 ms: 1.43x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 1.42 ms: 1.51x slower                                                     |
| coverage                   | 71.4 ms                                                | 118 ms: 1.66x slower                                                      |
| telco                      | 6.53 ms                                                | 176 ms: 26.90x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.02x slower                                                              |

Benchmark hidden because not significant (1): logging_silent
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261116-3.16.0a2+dev-910a92b-NOGIL/bm-20261116-vultr-x86_64-python-910a92babf40b7b34baa-3.16.0a2+dev-910a92b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.026x slower

# HPT report

- Reliability score: 60.89% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.31x