# Results vs. 3.13.0rc2

- fork: python
- ref: 0efd679a6ce3b57ec3c5
- machine: linux-x86_64
- commit hash: 0efd679
- commit date: 2026-04-28
- overall geometric mean: 1.050x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 259 ms: 1.00x faster                                                   |
| docutils       | 2.62 sec                                                     | 2.48 sec: 1.06x faster                                                 |
| html5lib       | 67.0 ms                                                      | 60.9 ms: 1.10x faster                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 575 ms: 1.59x faster                                                   |
| async_tree_io              | 876 ms                                                       | 576 ms: 1.52x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 305 ms: 1.51x faster                                                   |
| async_tree_none            | 354 ms                                                       | 251 ms: 1.41x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 298 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 484 ms: 1.38x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 250 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 485 ms: 1.32x faster                                                   |
| async_generators           | 377 ms                                                       | 340 ms: 1.11x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                  |
| asyncio_websockets         | 520 ms                                                       | 543 ms: 1.04x slower                                                   |
| Geometric mean             | (ref)                                                        | 1.30x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                   |
| float          | 77.5 ms                                                      | 70.8 ms: 1.09x faster                                                  |
| nbody          | 85.1 ms                                                      | 95.7 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.81 ms: 1.10x faster                                                  |
| regex_compile  | 132 ms                                                       | 125 ms: 1.06x faster                                                   |
| regex_v8       | 22.7 ms                                                      | 22.4 ms: 1.01x faster                                                  |
| regex_dna      | 180 ms                                                       | 183 ms: 1.02x slower                                                   |
| Geometric mean | (ref)                                                        | 1.04x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 84.4 ms: 1.12x faster                                                  |
| tomli_loads          | 2.01 sec                                                     | 1.84 sec: 1.09x faster                                                 |
| json_dumps           | 10.5 ms                                                      | 9.69 ms: 1.09x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 84.0 ms: 1.02x faster                                                  |
| unpickle_pure_python | 210 us                                                       | 212 us: 1.01x slower                                                   |
| xml_etree_process    | 59.3 ms                                                      | 60.2 ms: 1.02x slower                                                  |
| json_loads           | 27.0 us                                                      | 27.4 us: 1.02x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 314 us: 1.07x slower                                                   |
| Geometric mean       | (ref)                                                        | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 6.80 ms: 1.09x faster                                                  |
| python_startup         | 11.0 ms                                                      | 12.3 ms: 1.12x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.02x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 21.5 ms                                                      | 21.8 ms: 1.01x slower                                                  |
| genshi_xml      | 48.8 ms                                                      | 50.8 ms: 1.04x slower                                                  |
| django_template | 34.1 ms                                                      | 36.3 ms: 1.06x slower                                                  |
| mako            | 11.3 ms                                                      | 12.2 ms: 1.08x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.05x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679 |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 116 ms: 2.73x faster                                                   |
| mdp                        | 2.36 sec                                                     | 1.15 sec: 2.04x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 575 ms: 1.59x faster                                                   |
| async_tree_io              | 876 ms                                                       | 576 ms: 1.52x faster                                                   |
| deepcopy                   | 355 us                                                       | 234 us: 1.52x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 305 ms: 1.51x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 26.8 us: 1.46x faster                                                  |
| async_tree_none            | 354 ms                                                       | 251 ms: 1.41x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 298 ms: 1.39x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 484 ms: 1.38x faster                                                   |
| go                         | 141 ms                                                       | 104 ms: 1.35x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 250 ms: 1.35x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 485 ms: 1.32x faster                                                   |
| scimark_sor                | 134 ms                                                       | 108 ms: 1.24x faster                                                   |
| deepcopy_reduce            | 3.11 us                                                      | 2.55 us: 1.22x faster                                                  |
| spectral_norm              | 111 ms                                                       | 91.4 ms: 1.21x faster                                                  |
| pidigits                   | 217 ms                                                       | 184 ms: 1.18x faster                                                   |
| scimark_fft                | 349 ms                                                       | 302 ms: 1.16x faster                                                   |
| xml_etree_iterparse        | 94.9 ms                                                      | 84.4 ms: 1.12x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.3 ms: 1.11x faster                                                  |
| async_generators           | 377 ms                                                       | 340 ms: 1.11x faster                                                   |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.25 ms: 1.11x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 60.9 ms: 1.10x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 68.3 ms: 1.10x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.81 ms: 1.10x faster                                                  |
| float                      | 77.5 ms                                                      | 70.8 ms: 1.09x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.84 sec: 1.09x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 9.69 ms: 1.09x faster                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 6.80 ms: 1.09x faster                                                  |
| pyflate                    | 449 ms                                                       | 413 ms: 1.08x faster                                                   |
| bpe_tokeniser              | 4.45 sec                                                     | 4.13 sec: 1.08x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.60 ms: 1.07x faster                                                  |
| richards_super             | 51.6 ms                                                      | 48.8 ms: 1.06x faster                                                  |
| regex_compile              | 132 ms                                                       | 125 ms: 1.06x faster                                                   |
| docutils                   | 2.62 sec                                                     | 2.48 sec: 1.06x faster                                                 |
| richards                   | 45.2 ms                                                      | 42.9 ms: 1.05x faster                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 62.2 ms: 1.05x faster                                                  |
| chaos                      | 57.3 ms                                                      | 54.6 ms: 1.05x faster                                                  |
| logging_simple             | 6.16 us                                                      | 5.91 us: 1.04x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                                   |
| scimark_lu                 | 113 ms                                                       | 108 ms: 1.04x faster                                                   |
| logging_format             | 6.84 us                                                      | 6.65 us: 1.03x faster                                                  |
| sympy_integrate            | 19.8 ms                                                      | 19.3 ms: 1.03x faster                                                  |
| logging_silent             | 103 ns                                                       | 99.9 ns: 1.03x faster                                                  |
| comprehensions             | 16.5 us                                                      | 16.0 us: 1.03x faster                                                  |
| nqueens                    | 78.6 ms                                                      | 76.7 ms: 1.03x faster                                                  |
| coverage                   | 83.0 ms                                                      | 81.1 ms: 1.02x faster                                                  |
| generators                 | 28.8 ms                                                      | 28.2 ms: 1.02x faster                                                  |
| pprint_safe_repr           | 738 ms                                                       | 724 ms: 1.02x faster                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 84.0 ms: 1.02x faster                                                  |
| meteor_contest             | 102 ms                                                       | 99.9 ms: 1.02x faster                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.47 sec: 1.02x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 22.4 ms: 1.01x faster                                                  |
| 2to3                       | 260 ms                                                       | 259 ms: 1.00x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.7 ms: 1.01x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 212 us: 1.01x slower                                                   |
| genshi_text                | 21.5 ms                                                      | 21.8 ms: 1.01x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 60.2 ms: 1.02x slower                                                  |
| json_loads                 | 27.0 us                                                      | 27.4 us: 1.02x slower                                                  |
| regex_dna                  | 180 ms                                                       | 183 ms: 1.02x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 158 ms: 1.02x slower                                                   |
| sympy_str                  | 275 ms                                                       | 280 ms: 1.02x slower                                                   |
| sqlite_synth               | 2.21 us                                                      | 2.27 us: 1.03x slower                                                  |
| json                       | 4.93 ms                                                      | 5.08 ms: 1.03x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 70.4 ms: 1.04x slower                                                  |
| fannkuch                   | 370 ms                                                       | 384 ms: 1.04x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 50.8 ms: 1.04x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 161 us: 1.04x slower                                                   |
| asyncio_websockets         | 520 ms                                                       | 543 ms: 1.04x slower                                                   |
| django_template            | 34.1 ms                                                      | 36.3 ms: 1.06x slower                                                  |
| sympy_expand               | 457 ms                                                       | 486 ms: 1.06x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 3.34 ms: 1.07x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 314 us: 1.07x slower                                                   |
| mako                       | 11.3 ms                                                      | 12.2 ms: 1.08x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.3 ms: 1.12x slower                                                  |
| nbody                      | 85.1 ms                                                      | 95.7 ms: 1.12x slower                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.91 ms: 1.25x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.76 ms: 1.32x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.32 ms: 1.43x slower                                                  |
| telco                      | 7.82 ms                                                      | 161 ms: 20.60x slower                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 296 ms: 26.90x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.01x faster                                                           |

Benchmark hidden because not significant (3): thrift, raytrace, pycparser
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260428-3.15.0a8+-0efd679/bm-20260428-vultr-x86_64-python-0efd679a6ce3b57ec3c5-3.15.0a8+-0efd679.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.050x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.15x