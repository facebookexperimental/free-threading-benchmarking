# Results vs. 3.13.0rc2

- fork: Fidget-Spinner
- ref: jit_ft
- machine: linux-x86_64
- commit hash: 00ae7b5
- commit date: 2025-12-18
- overall geometric mean: 1.030x slower
- HPT reliability: 58.36%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.43x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 281 ms: 1.08x slower                                               |
| docutils       | 2.62 sec                                                     | 2.88 sec: 1.10x slower                                             |
| html5lib       | 67.0 ms                                                      | 70.6 ms: 1.05x slower                                              |
| Geometric mean | (ref)                                                        | 1.08x slower                                                       |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 615 ms: 1.48x faster                                               |
| async_tree_io              | 876 ms                                                       | 635 ms: 1.38x faster                                               |
| async_tree_memoization     | 461 ms                                                       | 357 ms: 1.29x faster                                               |
| async_tree_memoization_tg  | 414 ms                                                       | 331 ms: 1.25x faster                                               |
| async_tree_none_tg         | 336 ms                                                       | 269 ms: 1.25x faster                                               |
| async_tree_none            | 354 ms                                                       | 291 ms: 1.22x faster                                               |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 548 ms: 1.21x faster                                               |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 526 ms: 1.21x faster                                               |
| asyncio_websockets         | 520 ms                                                       | 510 ms: 1.02x faster                                               |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                              |
| async_generators           | 377 ms                                                       | 399 ms: 1.06x slower                                               |
| Geometric mean             | (ref)                                                        | 1.19x faster                                                       |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| float          | 77.5 ms                                                      | 58.6 ms: 1.32x faster                                              |
| pidigits       | 217 ms                                                       | 199 ms: 1.09x faster                                               |
| nbody          | 85.1 ms                                                      | 93.9 ms: 1.10x slower                                              |
| Geometric mean | (ref)                                                        | 1.09x faster                                                       |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                              |
| regex_v8       | 22.7 ms                                                      | 21.5 ms: 1.06x faster                                              |
| regex_dna      | 180 ms                                                       | 176 ms: 1.02x faster                                               |
| regex_compile  | 132 ms                                                       | 144 ms: 1.09x slower                                               |
| Geometric mean | (ref)                                                        | 1.02x faster                                                       |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|----------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 87.0 ms: 1.09x faster                                              |
| xml_etree_parse      | 136 ms                                                       | 131 ms: 1.04x faster                                               |
| unpickle_pure_python | 210 us                                                       | 204 us: 1.03x faster                                               |
| json_dumps           | 10.5 ms                                                      | 10.7 ms: 1.02x slower                                              |
| xml_etree_generate   | 85.4 ms                                                      | 89.8 ms: 1.05x slower                                              |
| xml_etree_process    | 59.3 ms                                                      | 63.1 ms: 1.06x slower                                              |
| pickle_pure_python   | 294 us                                                       | 314 us: 1.07x slower                                               |
| tomli_loads          | 2.01 sec                                                     | 2.17 sec: 1.08x slower                                             |
| json_loads           | 27.0 us                                                      | 32.8 us: 1.21x slower                                              |
| Geometric mean       | (ref)                                                        | 1.04x slower                                                       |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.63 ms: 1.30x slower                                              |
| python_startup         | 11.0 ms                                                      | 16.0 ms: 1.45x slower                                              |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                       |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|-----------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 40.3 ms: 1.18x slower                                              |
| genshi_text     | 21.5 ms                                                      | 27.6 ms: 1.28x slower                                              |
| mako            | 11.3 ms                                                      | 14.9 ms: 1.32x slower                                              |
| genshi_xml      | 48.8 ms                                                      | 68.8 ms: 1.41x slower                                              |
| Geometric mean  | (ref)                                                        | 1.30x slower                                                       |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5 |
|----------------------------|:------------------------------------------------------------:|:------------------------------------------------------------------:|
| richards                   | 45.2 ms                                                      | 20.3 ms: 2.22x faster                                              |
| richards_super             | 51.6 ms                                                      | 25.8 ms: 2.00x faster                                              |
| gc_traversal               | 3.14 ms                                                      | 1.94 ms: 1.62x faster                                              |
| bench_mp_pool              | 11.0 ms                                                      | 7.15 ms: 1.54x faster                                              |
| mdp                        | 2.36 sec                                                     | 1.55 sec: 1.52x faster                                             |
| async_tree_io_tg           | 913 ms                                                       | 615 ms: 1.48x faster                                               |
| async_tree_io              | 876 ms                                                       | 635 ms: 1.38x faster                                               |
| deepcopy_memo              | 39.1 us                                                      | 28.5 us: 1.37x faster                                              |
| go                         | 141 ms                                                       | 104 ms: 1.35x faster                                               |
| float                      | 77.5 ms                                                      | 58.6 ms: 1.32x faster                                              |
| async_tree_memoization     | 461 ms                                                       | 357 ms: 1.29x faster                                               |
| deepcopy                   | 355 us                                                       | 283 us: 1.25x faster                                               |
| async_tree_memoization_tg  | 414 ms                                                       | 331 ms: 1.25x faster                                               |
| async_tree_none_tg         | 336 ms                                                       | 269 ms: 1.25x faster                                               |
| logging_silent             | 103 ns                                                       | 82.6 ns: 1.24x faster                                              |
| async_tree_none            | 354 ms                                                       | 291 ms: 1.22x faster                                               |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 548 ms: 1.21x faster                                               |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 526 ms: 1.21x faster                                               |
| scimark_fft                | 349 ms                                                       | 296 ms: 1.18x faster                                               |
| scimark_sor                | 134 ms                                                       | 114 ms: 1.18x faster                                               |
| spectral_norm              | 111 ms                                                       | 100 ms: 1.11x faster                                               |
| bpe_tokeniser              | 4.45 sec                                                     | 4.03 sec: 1.10x faster                                             |
| pyflate                    | 449 ms                                                       | 408 ms: 1.10x faster                                               |
| sqlite_synth               | 2.21 us                                                      | 2.01 us: 1.10x faster                                              |
| xml_etree_iterparse        | 94.9 ms                                                      | 87.0 ms: 1.09x faster                                              |
| pidigits                   | 217 ms                                                       | 199 ms: 1.09x faster                                               |
| regex_effbot               | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                              |
| regex_v8                   | 22.7 ms                                                      | 21.5 ms: 1.06x faster                                              |
| deepcopy_reduce            | 3.11 us                                                      | 2.95 us: 1.05x faster                                              |
| pathlib                    | 19.2 ms                                                      | 18.3 ms: 1.05x faster                                              |
| pprint_safe_repr           | 738 ms                                                       | 706 ms: 1.04x faster                                               |
| xml_etree_parse            | 136 ms                                                       | 131 ms: 1.04x faster                                               |
| unpickle_pure_python       | 210 us                                                       | 204 us: 1.03x faster                                               |
| deltablue                  | 3.12 ms                                                      | 3.05 ms: 1.02x faster                                              |
| regex_dna                  | 180 ms                                                       | 176 ms: 1.02x faster                                               |
| asyncio_websockets         | 520 ms                                                       | 510 ms: 1.02x faster                                               |
| json_dumps                 | 10.5 ms                                                      | 10.7 ms: 1.02x slower                                              |
| pycparser                  | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                             |
| dulwich_log                | 74.8 ms                                                      | 77.3 ms: 1.03x slower                                              |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.04x slower                                              |
| chaos                      | 57.3 ms                                                      | 59.5 ms: 1.04x slower                                              |
| scimark_monte_carlo        | 65.4 ms                                                      | 67.9 ms: 1.04x slower                                              |
| xml_etree_generate         | 85.4 ms                                                      | 89.8 ms: 1.05x slower                                              |
| html5lib                   | 67.0 ms                                                      | 70.6 ms: 1.05x slower                                              |
| async_generators           | 377 ms                                                       | 399 ms: 1.06x slower                                               |
| xml_etree_process          | 59.3 ms                                                      | 63.1 ms: 1.06x slower                                              |
| pickle_pure_python         | 294 us                                                       | 314 us: 1.07x slower                                               |
| tomli_loads                | 2.01 sec                                                     | 2.17 sec: 1.08x slower                                             |
| 2to3                       | 260 ms                                                       | 281 ms: 1.08x slower                                               |
| regex_compile              | 132 ms                                                       | 144 ms: 1.09x slower                                               |
| json                       | 4.93 ms                                                      | 5.39 ms: 1.09x slower                                              |
| docutils                   | 2.62 sec                                                     | 2.88 sec: 1.10x slower                                             |
| nbody                      | 85.1 ms                                                      | 93.9 ms: 1.10x slower                                              |
| comprehensions             | 16.5 us                                                      | 18.2 us: 1.11x slower                                              |
| generators                 | 28.8 ms                                                      | 31.9 ms: 1.11x slower                                              |
| scimark_lu                 | 113 ms                                                       | 125 ms: 1.11x slower                                               |
| create_gc_cycles           | 1.34 ms                                                      | 1.49 ms: 1.11x slower                                              |
| hexiom                     | 5.99 ms                                                      | 6.72 ms: 1.12x slower                                              |
| thrift                     | 778 us                                                       | 875 us: 1.12x slower                                               |
| fannkuch                   | 370 ms                                                       | 417 ms: 1.13x slower                                               |
| logging_simple             | 6.16 us                                                      | 7.00 us: 1.14x slower                                              |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.44 ms: 1.16x slower                                              |
| sympy_integrate            | 19.8 ms                                                      | 23.0 ms: 1.16x slower                                              |
| logging_format             | 6.84 us                                                      | 7.96 us: 1.16x slower                                              |
| meteor_contest             | 102 ms                                                       | 119 ms: 1.17x slower                                               |
| django_template            | 34.1 ms                                                      | 40.3 ms: 1.18x slower                                              |
| raytrace                   | 253 ms                                                       | 302 ms: 1.20x slower                                               |
| json_loads                 | 27.0 us                                                      | 32.8 us: 1.21x slower                                              |
| nqueens                    | 78.6 ms                                                      | 95.9 ms: 1.22x slower                                              |
| crypto_pyaes               | 67.9 ms                                                      | 83.6 ms: 1.23x slower                                              |
| sympy_sum                  | 156 ms                                                       | 193 ms: 1.24x slower                                               |
| sympy_expand               | 457 ms                                                       | 575 ms: 1.26x slower                                               |
| typing_runtime_protocols   | 155 us                                                       | 196 us: 1.26x slower                                               |
| genshi_text                | 21.5 ms                                                      | 27.6 ms: 1.28x slower                                              |
| sympy_str                  | 275 ms                                                       | 354 ms: 1.29x slower                                               |
| python_startup_no_site     | 7.39 ms                                                      | 9.63 ms: 1.30x slower                                              |
| mako                       | 11.3 ms                                                      | 14.9 ms: 1.32x slower                                              |
| coverage                   | 83.0 ms                                                      | 113 ms: 1.36x slower                                               |
| genshi_xml                 | 48.8 ms                                                      | 68.8 ms: 1.41x slower                                              |
| python_startup             | 11.0 ms                                                      | 16.0 ms: 1.45x slower                                              |
| bench_thread_pool          | 919 us                                                       | 1.48 ms: 1.62x slower                                              |
| telco                      | 7.82 ms                                                      | 179 ms: 22.89x slower                                              |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                       |

Benchmark hidden because not significant (2): pprint_pformat, pylint
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20251218-3.15.0a3+-00ae7b5-JIT,NOGIL/bm-20251218-vultr-x86_64-Fidget%2dSpinner-jit_ft-3.15.0a3+-00ae7b5.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.030x slower

# HPT report

- Reliability score: 58.36% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.43x