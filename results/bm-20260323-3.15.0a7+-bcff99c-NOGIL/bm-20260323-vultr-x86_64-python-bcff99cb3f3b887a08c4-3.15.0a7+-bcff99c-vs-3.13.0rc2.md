# Results vs. 3.13.0rc2

- fork: python
- ref: bcff99cb3f3b887a08c4
- machine: linux-x86_64
- commit hash: bcff99c
- commit date: 2026-03-23
- overall geometric mean: 1.062x slower
- HPT reliability: 94.05%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.43x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 283 ms: 1.09x slower                                                   |
| docutils       | 2.62 sec                                                     | 2.66 sec: 1.02x slower                                                 |
| html5lib       | 67.0 ms                                                      | 65.7 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                        | 1.03x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 602 ms: 1.52x faster                                                   |
| async_tree_io              | 876 ms                                                       | 612 ms: 1.43x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 350 ms: 1.32x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 259 ms: 1.30x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 320 ms: 1.29x faster                                                   |
| async_tree_none            | 354 ms                                                       | 284 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 522 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 547 ms: 1.22x faster                                                   |
| asyncio_websockets         | 520 ms                                                       | 513 ms: 1.01x faster                                                   |
| async_generators           | 377 ms                                                       | 372 ms: 1.01x faster                                                   |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.01x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.22x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 187 ms: 1.16x faster                                                   |
| float          | 77.5 ms                                                      | 73.3 ms: 1.06x faster                                                  |
| nbody          | 85.1 ms                                                      | 122 ms: 1.44x slower                                                   |
| Geometric mean | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 21.8 ms: 1.04x faster                                                  |
| regex_effbot   | 3.08 ms                                                      | 3.00 ms: 1.03x faster                                                  |
| regex_dna      | 180 ms                                                       | 186 ms: 1.03x slower                                                   |
| regex_compile  | 132 ms                                                       | 142 ms: 1.08x slower                                                   |
| Geometric mean | (ref)                                                        | 1.01x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 88.0 ms: 1.08x faster                                                  |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.04x faster                                                   |
| tomli_loads          | 2.01 sec                                                     | 1.97 sec: 1.02x faster                                                 |
| json_dumps           | 10.5 ms                                                      | 10.9 ms: 1.03x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 236 us: 1.12x slower                                                   |
| xml_etree_generate   | 85.4 ms                                                      | 96.5 ms: 1.13x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 335 us: 1.14x slower                                                   |
| xml_etree_process    | 59.3 ms                                                      | 68.2 ms: 1.15x slower                                                  |
| json_loads           | 27.0 us                                                      | 31.3 us: 1.16x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.06x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.77 ms: 1.32x slower                                                  |
| python_startup         | 11.0 ms                                                      | 15.9 ms: 1.45x slower                                                  |
| Geometric mean         | (ref)                                                        | 1.38x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|-----------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 55.4 ms: 1.14x slower                                                  |
| django_template | 34.1 ms                                                      | 39.9 ms: 1.17x slower                                                  |
| genshi_text     | 21.5 ms                                                      | 26.2 ms: 1.21x slower                                                  |
| mako            | 11.3 ms                                                      | 15.5 ms: 1.37x slower                                                  |
| Geometric mean  | (ref)                                                        | 1.22x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c |
|----------------------------|:------------------------------------------------------------:|:----------------------------------------------------------------------:|
| mdp                        | 2.36 sec                                                     | 1.31 sec: 1.80x faster                                                 |
| gc_traversal               | 3.14 ms                                                      | 1.92 ms: 1.63x faster                                                  |
| bench_mp_pool              | 11.0 ms                                                      | 7.02 ms: 1.57x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 602 ms: 1.52x faster                                                   |
| async_tree_io              | 876 ms                                                       | 612 ms: 1.43x faster                                                   |
| deepcopy                   | 355 us                                                       | 268 us: 1.33x faster                                                   |
| async_tree_memoization     | 461 ms                                                       | 350 ms: 1.32x faster                                                   |
| async_tree_none_tg         | 336 ms                                                       | 259 ms: 1.30x faster                                                   |
| async_tree_memoization_tg  | 414 ms                                                       | 320 ms: 1.29x faster                                                   |
| deepcopy_memo              | 39.1 us                                                      | 31.3 us: 1.25x faster                                                  |
| async_tree_none            | 354 ms                                                       | 284 ms: 1.25x faster                                                   |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 522 ms: 1.22x faster                                                   |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 547 ms: 1.22x faster                                                   |
| go                         | 141 ms                                                       | 119 ms: 1.18x faster                                                   |
| pidigits                   | 217 ms                                                       | 187 ms: 1.16x faster                                                   |
| sqlite_synth               | 2.21 us                                                      | 1.92 us: 1.15x faster                                                  |
| scimark_sor                | 134 ms                                                       | 121 ms: 1.11x faster                                                   |
| pathlib                    | 19.2 ms                                                      | 17.7 ms: 1.09x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 88.0 ms: 1.08x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 69.5 ms: 1.08x faster                                                  |
| pylint                     | 317 ms                                                       | 300 ms: 1.06x faster                                                   |
| float                      | 77.5 ms                                                      | 73.3 ms: 1.06x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 2.95 us: 1.05x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 21.8 ms: 1.04x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 132 ms: 1.04x faster                                                   |
| regex_effbot               | 3.08 ms                                                      | 3.00 ms: 1.03x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.97 sec: 1.02x faster                                                 |
| html5lib                   | 67.0 ms                                                      | 65.7 ms: 1.02x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.36 sec: 1.02x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 513 ms: 1.01x faster                                                   |
| async_generators           | 377 ms                                                       | 372 ms: 1.01x faster                                                   |
| scimark_fft                | 349 ms                                                       | 354 ms: 1.01x slower                                                   |
| spectral_norm              | 111 ms                                                       | 112 ms: 1.01x slower                                                   |
| coroutines                 | 23.6 ms                                                      | 23.9 ms: 1.01x slower                                                  |
| docutils                   | 2.62 sec                                                     | 2.66 sec: 1.02x slower                                                 |
| logging_silent             | 103 ns                                                       | 104 ns: 1.02x slower                                                   |
| regex_dna                  | 180 ms                                                       | 186 ms: 1.03x slower                                                   |
| json_dumps                 | 10.5 ms                                                      | 10.9 ms: 1.03x slower                                                  |
| pyflate                    | 449 ms                                                       | 466 ms: 1.04x slower                                                   |
| chaos                      | 57.3 ms                                                      | 61.7 ms: 1.08x slower                                                  |
| regex_compile              | 132 ms                                                       | 142 ms: 1.08x slower                                                   |
| hexiom                     | 5.99 ms                                                      | 6.48 ms: 1.08x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 801 ms: 1.09x slower                                                   |
| 2to3                       | 260 ms                                                       | 283 ms: 1.09x slower                                                   |
| sympy_integrate            | 19.8 ms                                                      | 21.6 ms: 1.09x slower                                                  |
| nqueens                    | 78.6 ms                                                      | 86.4 ms: 1.10x slower                                                  |
| json                       | 4.93 ms                                                      | 5.44 ms: 1.10x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.66 sec: 1.11x slower                                                 |
| logging_simple             | 6.16 us                                                      | 6.84 us: 1.11x slower                                                  |
| generators                 | 28.8 ms                                                      | 32.0 ms: 1.11x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.49 ms: 1.11x slower                                                  |
| comprehensions             | 16.5 us                                                      | 18.4 us: 1.12x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 236 us: 1.12x slower                                                   |
| deltablue                  | 3.12 ms                                                      | 3.51 ms: 1.12x slower                                                  |
| sympy_str                  | 275 ms                                                       | 310 ms: 1.13x slower                                                   |
| sympy_expand               | 457 ms                                                       | 516 ms: 1.13x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                      | 96.5 ms: 1.13x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 128 ms: 1.13x slower                                                   |
| genshi_xml                 | 48.8 ms                                                      | 55.4 ms: 1.14x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 335 us: 1.14x slower                                                   |
| sympy_sum                  | 156 ms                                                       | 178 ms: 1.15x slower                                                   |
| xml_etree_process          | 59.3 ms                                                      | 68.2 ms: 1.15x slower                                                  |
| richards_super             | 51.6 ms                                                      | 59.5 ms: 1.15x slower                                                  |
| json_loads                 | 27.0 us                                                      | 31.3 us: 1.16x slower                                                  |
| logging_format             | 6.84 us                                                      | 7.94 us: 1.16x slower                                                  |
| django_template            | 34.1 ms                                                      | 39.9 ms: 1.17x slower                                                  |
| thrift                     | 778 us                                                       | 911 us: 1.17x slower                                                   |
| richards                   | 45.2 ms                                                      | 53.2 ms: 1.18x slower                                                  |
| raytrace                   | 253 ms                                                       | 302 ms: 1.20x slower                                                   |
| scimark_monte_carlo        | 65.4 ms                                                      | 78.9 ms: 1.21x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.69 ms: 1.21x slower                                                  |
| genshi_text                | 21.5 ms                                                      | 26.2 ms: 1.21x slower                                                  |
| meteor_contest             | 102 ms                                                       | 126 ms: 1.24x slower                                                   |
| fannkuch                   | 370 ms                                                       | 460 ms: 1.24x slower                                                   |
| typing_runtime_protocols   | 155 us                                                       | 193 us: 1.25x slower                                                   |
| crypto_pyaes               | 67.9 ms                                                      | 87.7 ms: 1.29x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 9.77 ms: 1.32x slower                                                  |
| coverage                   | 83.0 ms                                                      | 113 ms: 1.36x slower                                                   |
| mako                       | 11.3 ms                                                      | 15.5 ms: 1.37x slower                                                  |
| nbody                      | 85.1 ms                                                      | 122 ms: 1.44x slower                                                   |
| python_startup             | 11.0 ms                                                      | 15.9 ms: 1.45x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.49 ms: 1.62x slower                                                  |
| telco                      | 7.82 ms                                                      | 172 ms: 22.03x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.06x slower                                                           |

Benchmark hidden because not significant (1): pycparser
Ignored benchmarks (18) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260323-3.15.0a7+-bcff99c-NOGIL/bm-20260323-vultr-x86_64-python-bcff99cb3f3b887a08c4-3.15.0a7+-bcff99c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.062x slower

# HPT report

- Reliability score: 94.05% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.43x