# Results vs. 3.13.0rc2

- fork: python
- ref: a6bc60da02ea37f33d5a
- machine: linux-x86_64
- commit hash: a6bc60d
- commit date: 2026-01-12
- overall geometric mean: 1.066x slower
- HPT reliability: 97.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.40x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 277 ms: 1.07x slower                                                   |
| docutils       | 2.62 sec                                                     | 2.74 sec: 1.05x slower                                                 |
| html5lib       | 67.0 ms                                                      | 64.4 ms: 1.04x faster                                                  |
| Geometric mean | (ref)                                                        | 1.02x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 593 ms: 1.54x faster                                                   |
| async_tree_io              | 876 ms                                                       | 611 ms: 1.43x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 353 ms: 1.31x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 262 ms: 1.29x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 324 ms: 1.28x faster                                                   |
| async_tree_none            | 354 ms                                                       | 288 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 556 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 532 ms: 1.20x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                   |
| async_generators           | 377 ms                                                       | 376 ms: 1.00x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.21x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 194 ms: 1.11x faster                                                   |
| float          | 77.5 ms                                                      | 75.1 ms: 1.03x faster                                                  |
| nbody          | 85.1 ms                                                      | 125 ms: 1.47x slower                                                   |
| Geometric mean | (ref)                                                        | 1.09x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.70 ms: 1.14x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 21.5 ms: 1.06x faster                                                  |
| regex_dna      | 180 ms                                                       | 173 ms: 1.04x faster                                                   |
| regex_compile  | 132 ms                                                       | 141 ms: 1.07x slower                                                   |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.1 ms: 1.08x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 2.00 sec: 1.00x faster                                                 |
| json_dumps           | 10.5 ms                                                      | 11.1 ms: 1.05x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 96.0 ms: 1.12x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 238 us: 1.13x slower                                                   |
| pickle_pure_python   | 294 us                                                       | 334 us: 1.13x slower                                                   |
| xml_etree_process    | 59.3 ms                                                      | 69.4 ms: 1.17x slower                                                  |
| json_loads           | 27.0 us                                                      | 32.3 us: 1.20x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.07x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.67 ms: 1.31x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.37x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 39.9 ms: 1.17x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 57.6 ms: 1.18x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 27.2 ms: 1.26x slower                                                  |
| mako            | 11.3 ms                                                      | 15.7 ms: 1.38x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.25x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.31 sec: 1.79x faster                                                 |
| gc_traversal               | 3.14 ms                                                      | 1.93 ms: 1.63x faster                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 7.04 ms: 1.56x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 593 ms: 1.54x faster                                                   |
| async_tree_io              | 876 ms                                                       | 611 ms: 1.43x faster                                                   |
| deepcopy                   | 355 us                                                       | 265 us: 1.34x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 353 ms: 1.31x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 262 ms: 1.29x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 324 ms: 1.28x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 30.8 us: 1.27x faster                                                  |
| async_tree_none            | 354 ms                                                       | 288 ms: 1.23x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 556 ms: 1.20x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 532 ms: 1.20x faster                                                   |
| go                         | 141 ms                                                       | 121 ms: 1.16x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 2.70 ms: 1.14x faster                                                  |
| pidigits                   | 217 ms                                                       | 194 ms: 1.11x faster                                                   |
| scimark_sor                | 134 ms                                                       | 123 ms: 1.09x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.1 ms: 1.08x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.06 us: 1.07x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.91 us: 1.07x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.2 ms: 1.06x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.5 ms: 1.06x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 70.9 ms: 1.05x faster                                                  |
| regex_dna                  | 180 ms                                                       | 173 ms: 1.04x faster                                                   |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| html5lib                   | 67.0 ms                                                      | 64.4 ms: 1.04x faster                                                  |
| float                      | 77.5 ms                                                      | 75.1 ms: 1.03x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                   |
| tomli_loads                | 2.01 sec                                                     | 2.00 sec: 1.00x faster                                                 |
| async_generators           | 377 ms                                                       | 376 ms: 1.00x faster                                                   |
| scimark_fft                | 349 ms                                                       | 353 ms: 1.01x slower                                                   |
| pycparser                  | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                                 |
| spectral_norm              | 111 ms                                                       | 113 ms: 1.02x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 24.2 ms: 1.03x slower                                                  |
| logging_silent             | 103 ns                                                       | 106 ns: 1.03x slower                                                   |
| pprint_safe_repr           | 738 ms                                                       | 768 ms: 1.04x slower                                                   |
| docutils                   | 2.62 sec                                                     | 2.74 sec: 1.05x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 11.1 ms: 1.05x slower                                                  |
| pyflate                    | 449 ms                                                       | 471 ms: 1.05x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 6.38 ms: 1.07x slower                                                  |
| regex_compile              | 132 ms                                                       | 141 ms: 1.07x slower                                                   |
| pprint_pformat             | 1.50 sec                                                     | 1.60 sec: 1.07x slower                                                 |
| 2to3                       | 260 ms                                                       | 277 ms: 1.07x slower                                                   |
| comprehensions             | 16.5 us                                                      | 17.9 us: 1.09x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 21.9 ms: 1.11x slower                                                  |
| json                       | 4.93 ms                                                      | 5.46 ms: 1.11x slower                                                  |
| logging_simple             | 6.16 us                                                      | 6.87 us: 1.12x slower                                                  |
| generators                 | 28.8 ms                                                      | 32.2 ms: 1.12x slower                                                  |
| chaos                      | 57.3 ms                                                      | 64.3 ms: 1.12x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 96.0 ms: 1.12x slower                                                  |
| logging_format             | 6.84 us                                                      | 7.71 us: 1.13x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.51 ms: 1.13x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 88.8 ms: 1.13x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 238 us: 1.13x slower                                                   |
| pickle_pure_python         | 294 us                                                       | 334 us: 1.13x slower                                                   |
| sympy_str                  | 275 ms                                                       | 313 ms: 1.14x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 178 ms: 1.14x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 3.61 ms: 1.16x slower                                                  |
| sympy_expand               | 457 ms                                                       | 528 ms: 1.16x slower                                                   |
| thrift                     | 778 us                                                       | 899 us: 1.16x slower                                                   |
| richards_super             | 51.6 ms                                                      | 60.1 ms: 1.16x slower                                                  |
| richards                   | 45.2 ms                                                      | 52.8 ms: 1.17x slower                                                  |
| django_template            | 34.1 ms                                                      | 39.9 ms: 1.17x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 132 ms: 1.17x slower                                                   |
| xml_etree_process          | 59.3 ms                                                      | 69.4 ms: 1.17x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 57.6 ms: 1.18x slower                                                  |
| meteor_contest             | 102 ms                                                       | 121 ms: 1.19x slower                                                   |
| json_loads                 | 27.0 us                                                      | 32.3 us: 1.20x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.64 ms: 1.20x slower                                                  |
| raytrace                   | 253 ms                                                       | 305 ms: 1.21x slower                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 79.5 ms: 1.22x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 194 us: 1.25x slower                                                   |
| fannkuch                   | 370 ms                                                       | 464 ms: 1.26x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 27.2 ms: 1.26x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 87.4 ms: 1.29x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 9.67 ms: 1.31x slower                                                  |
| coverage                   | 83.0 ms                                                      | 111 ms: 1.34x slower                                                   |
| mako                       | 11.3 ms                                                      | 15.7 ms: 1.38x slower                                                  |
| python_startup             | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                  |
| nbody                      | 85.1 ms                                                      | 125 ms: 1.47x slower                                                   |
| bench_thread_pool          | 919 us                                                       | 1.47 ms: 1.60x slower                                                  |
| telco                      | 7.82 ms                                                      | 177 ms: 22.62x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.07x slower                                                           |

Benchmark hidden because not significant (2): pylint, bpe_tokeniser
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260112-3.15.0a3+-a6bc60d-NOGIL/bm-20260112-vultr-x86_64-python-a6bc60da02ea37f33d5a-3.15.0a3+-a6bc60d.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.066x slower

# HPT report

- Reliability score: 97.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.40x