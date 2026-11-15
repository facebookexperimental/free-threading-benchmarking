# Results vs. 3.12.6

- fork: python
- ref: edd6f7692ad1bb30ba48
- machine: linux-x86_64
- commit hash: edd6f76
- commit date: 2026-11-14
- overall geometric mean: 1.029x slower
- HPT reliability: 80.76%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.32x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 290 ms: 1.10x slower                                                      |
| docutils       | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                    |
| html5lib       | 63.6 ms                                                | 67.2 ms: 1.06x slower                                                     |
| Geometric mean | (ref)                                                  | 1.07x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 699 ms: 1.59x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 720 ms: 1.50x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 397 ms: 1.41x faster                                                      |
| async_tree_none            | 464 ms                                                 | 340 ms: 1.37x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 411 ms: 1.35x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 333 ms: 1.34x faster                                                      |
| async_generators           | 384 ms                                                 | 294 ms: 1.31x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 564 ms: 1.28x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 575 ms: 1.24x faster                                                      |
| asyncio_tcp                | 519 ms                                                 | 454 ms: 1.14x faster                                                      |
| asyncio_websockets         | 517 ms                                                 | 502 ms: 1.03x faster                                                      |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.57 sec: 1.04x slower                                                    |
| coroutines                 | 23.9 ms                                                | 26.0 ms: 1.08x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.25x faster                                                              |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 84.3 ms: 1.04x slower                                                     |
| pidigits       | 184 ms                                                 | 192 ms: 1.04x slower                                                      |
| nbody          | 89.3 ms                                                | 117 ms: 1.31x slower                                                      |
| Geometric mean | (ref)                                                  | 1.13x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                     |
| regex_v8       | 20.6 ms                                                | 19.9 ms: 1.03x faster                                                     |
| regex_dna      | 168 ms                                                 | 169 ms: 1.01x slower                                                      |
| regex_compile  | 142 ms                                                 | 171 ms: 1.20x slower                                                      |
| Geometric mean | (ref)                                                  | 1.01x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.99 sec: 1.06x faster                                                    |
| json_dumps           | 10.4 ms                                                | 10.2 ms: 1.01x faster                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 96.4 ms: 1.00x faster                                                     |
| xml_etree_parse      | 139 ms                                                 | 143 ms: 1.03x slower                                                      |
| unpickle_pure_python | 221 us                                                 | 242 us: 1.10x slower                                                      |
| pickle_dict          | 31.8 us                                                | 35.5 us: 1.12x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 347 us: 1.13x slower                                                      |
| pickle               | 10.9 us                                                | 12.6 us: 1.15x slower                                                     |
| xml_etree_generate   | 85.2 ms                                                | 98.4 ms: 1.15x slower                                                     |
| json_loads           | 26.5 us                                                | 30.9 us: 1.17x slower                                                     |
| pickle_list          | 4.77 us                                                | 5.60 us: 1.17x slower                                                     |
| unpickle             | 14.1 us                                                | 16.7 us: 1.19x slower                                                     |
| unpickle_list        | 4.67 us                                                | 5.69 us: 1.22x slower                                                     |
| xml_etree_process    | 59.0 ms                                                | 75.2 ms: 1.27x slower                                                     |
| Geometric mean       | (ref)                                                  | 1.11x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.87 ms: 1.24x slower                                                     |
| python_startup         | 9.93 ms                                                | 13.4 ms: 1.35x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.29x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 41.5 ms: 1.20x slower                                                     |
| mako            | 11.0 ms                                                | 16.1 ms: 1.46x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.32x slower                                                              |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76 |
|----------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 116 ms: 2.74x faster                                                      |
| gc_traversal               | 3.46 ms                                                | 1.81 ms: 1.91x faster                                                     |
| mdp                        | 2.42 sec                                               | 1.29 sec: 1.87x faster                                                    |
| bench_mp_pool              | 10.8 ms                                                | 6.65 ms: 1.62x faster                                                     |
| async_tree_io_tg           | 1.11 sec                                               | 699 ms: 1.59x faster                                                      |
| async_tree_io              | 1.08 sec                                               | 720 ms: 1.50x faster                                                      |
| async_tree_memoization_tg  | 560 ms                                                 | 397 ms: 1.41x faster                                                      |
| async_tree_none            | 464 ms                                                 | 340 ms: 1.37x faster                                                      |
| async_tree_memoization     | 555 ms                                                 | 411 ms: 1.35x faster                                                      |
| async_tree_none_tg         | 446 ms                                                 | 333 ms: 1.34x faster                                                      |
| deepcopy                   | 352 us                                                 | 268 us: 1.32x faster                                                      |
| async_generators           | 384 ms                                                 | 294 ms: 1.31x faster                                                      |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 564 ms: 1.28x faster                                                      |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 575 ms: 1.24x faster                                                      |
| deepcopy_memo              | 40.3 us                                                | 33.3 us: 1.21x faster                                                     |
| typing_runtime_protocols   | 163 us                                                 | 136 us: 1.20x faster                                                      |
| pathlib                    | 21.5 ms                                                | 18.2 ms: 1.18x faster                                                     |
| go                         | 139 ms                                                 | 121 ms: 1.15x faster                                                      |
| asyncio_tcp                | 519 ms                                                 | 454 ms: 1.14x faster                                                      |
| regex_effbot               | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                     |
| bpe_tokeniser              | 4.74 sec                                               | 4.26 sec: 1.11x faster                                                    |
| comprehensions             | 19.8 us                                                | 17.9 us: 1.11x faster                                                     |
| dulwich_log                | 78.9 ms                                                | 71.5 ms: 1.10x faster                                                     |
| sqlite_synth               | 2.20 us                                                | 2.03 us: 1.09x faster                                                     |
| scimark_sor                | 130 ms                                                 | 121 ms: 1.07x faster                                                      |
| spectral_norm              | 110 ms                                                 | 104 ms: 1.06x faster                                                      |
| tomli_loads                | 2.11 sec                                               | 1.99 sec: 1.06x faster                                                    |
| deepcopy_reduce            | 3.08 us                                                | 2.95 us: 1.04x faster                                                     |
| unpack_sequence            | 52.1 ns                                                | 49.9 ns: 1.04x faster                                                     |
| regex_v8                   | 20.6 ms                                                | 19.9 ms: 1.03x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 502 ms: 1.03x faster                                                      |
| chaos                      | 62.8 ms                                                | 61.5 ms: 1.02x faster                                                     |
| scimark_fft                | 342 ms                                                 | 335 ms: 1.02x faster                                                      |
| json_dumps                 | 10.4 ms                                                | 10.2 ms: 1.01x faster                                                     |
| raytrace                   | 299 ms                                                 | 296 ms: 1.01x faster                                                      |
| xml_etree_iterparse        | 96.7 ms                                                | 96.4 ms: 1.00x faster                                                     |
| pycparser                  | 1.17 sec                                               | 1.17 sec: 1.00x slower                                                    |
| pyflate                    | 448 ms                                                 | 451 ms: 1.01x slower                                                      |
| regex_dna                  | 168 ms                                                 | 169 ms: 1.01x slower                                                      |
| logging_silent             | 109 ns                                                 | 112 ns: 1.03x slower                                                      |
| xml_etree_parse            | 139 ms                                                 | 143 ms: 1.03x slower                                                      |
| asyncio_tcp_ssl            | 1.51 sec                                               | 1.57 sec: 1.04x slower                                                    |
| float                      | 80.8 ms                                                | 84.3 ms: 1.04x slower                                                     |
| pidigits                   | 184 ms                                                 | 192 ms: 1.04x slower                                                      |
| generators                 | 32.2 ms                                                | 33.8 ms: 1.05x slower                                                     |
| html5lib                   | 63.6 ms                                                | 67.2 ms: 1.06x slower                                                     |
| logging_simple             | 6.63 us                                                | 7.02 us: 1.06x slower                                                     |
| docutils                   | 2.64 sec                                               | 2.80 sec: 1.06x slower                                                    |
| hexiom                     | 6.17 ms                                                | 6.56 ms: 1.06x slower                                                     |
| sympy_integrate            | 20.5 ms                                                | 21.9 ms: 1.07x slower                                                     |
| deltablue                  | 3.45 ms                                                | 3.69 ms: 1.07x slower                                                     |
| json                       | 5.02 ms                                                | 5.45 ms: 1.08x slower                                                     |
| coroutines                 | 23.9 ms                                                | 26.0 ms: 1.08x slower                                                     |
| nqueens                    | 80.1 ms                                                | 87.4 ms: 1.09x slower                                                     |
| unpickle_pure_python       | 221 us                                                 | 242 us: 1.10x slower                                                      |
| 2to3                       | 264 ms                                                 | 290 ms: 1.10x slower                                                      |
| logging_format             | 7.35 us                                                | 8.09 us: 1.10x slower                                                     |
| sympy_str                  | 292 ms                                                 | 321 ms: 1.10x slower                                                      |
| sympy_sum                  | 166 ms                                                 | 183 ms: 1.10x slower                                                      |
| pprint_safe_repr           | 743 ms                                                 | 824 ms: 1.11x slower                                                      |
| pprint_pformat             | 1.52 sec                                               | 1.70 sec: 1.12x slower                                                    |
| pickle_dict                | 31.8 us                                                | 35.5 us: 1.12x slower                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 77.1 ms: 1.13x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 347 us: 1.13x slower                                                      |
| crypto_pyaes               | 76.6 ms                                                | 87.9 ms: 1.15x slower                                                     |
| pickle                     | 10.9 us                                                | 12.6 us: 1.15x slower                                                     |
| sympy_expand               | 468 ms                                                 | 537 ms: 1.15x slower                                                      |
| scimark_lu                 | 114 ms                                                 | 131 ms: 1.15x slower                                                      |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.07 ms: 1.15x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 98.4 ms: 1.15x slower                                                     |
| richards                   | 45.9 ms                                                | 53.1 ms: 1.16x slower                                                     |
| thrift                     | 791 us                                                 | 921 us: 1.16x slower                                                      |
| json_loads                 | 26.5 us                                                | 30.9 us: 1.17x slower                                                     |
| richards_super             | 51.9 ms                                                | 60.7 ms: 1.17x slower                                                     |
| pickle_list                | 4.77 us                                                | 5.60 us: 1.17x slower                                                     |
| unpickle                   | 14.1 us                                                | 16.7 us: 1.19x slower                                                     |
| django_template            | 34.7 ms                                                | 41.5 ms: 1.20x slower                                                     |
| regex_compile              | 142 ms                                                 | 171 ms: 1.20x slower                                                      |
| meteor_contest             | 104 ms                                                 | 126 ms: 1.21x slower                                                      |
| create_gc_cycles           | 1.09 ms                                                | 1.33 ms: 1.22x slower                                                     |
| unpickle_list              | 4.67 us                                                | 5.69 us: 1.22x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 8.87 ms: 1.24x slower                                                     |
| fannkuch                   | 372 ms                                                 | 471 ms: 1.26x slower                                                      |
| xml_etree_process          | 59.0 ms                                                | 75.2 ms: 1.27x slower                                                     |
| nbody                      | 89.3 ms                                                | 117 ms: 1.31x slower                                                      |
| python_startup             | 9.93 ms                                                | 13.4 ms: 1.35x slower                                                     |
| mako                       | 11.0 ms                                                | 16.1 ms: 1.46x slower                                                     |
| bench_thread_pool          | 941 us                                                 | 1.41 ms: 1.50x slower                                                     |
| coverage                   | 71.4 ms                                                | 119 ms: 1.66x slower                                                      |
| telco                      | 6.53 ms                                                | 175 ms: 26.74x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.03x slower                                                              |
Ignored benchmarks (15) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20261114-3.16.0a2+dev-edd6f76-NOGIL/bm-20261114-vultr-x86_64-python-edd6f7692ad1bb30ba48-3.16.0a2+dev-edd6f76.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.029x slower

# HPT report

- Reliability score: 80.76% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.32x