# Results vs. 3.13.0rc2

- fork: python
- ref: a7d5a6cc179e2eabd780
- machine: linux-x86_64
- commit hash: a7d5a6c
- commit date: 2026-05-23
- overall geometric mean: 1.066x slower
- HPT reliability: 95.50%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.62 sec                                                     | 2.96 sec: 1.13x slower                                                |
| html5lib       | 67.0 ms                                                      | 68.1 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                        | 1.07x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 691 ms: 1.32x faster                                                  |
| async_tree_io              | 876 ms                                                       | 708 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 592 ms: 1.12x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 576 ms: 1.11x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 423 ms: 1.09x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 396 ms: 1.04x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 510 ms: 1.02x faster                                                  |
| async_tree_none            | 354 ms                                                       | 348 ms: 1.02x faster                                                  |
| async_generators           | 377 ms                                                       | 388 ms: 1.03x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.7 ms: 1.05x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.08x faster                                                          |

Benchmark hidden because not significant (1): async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 188 ms: 1.15x faster                                                  |
| float          | 77.5 ms                                                      | 88.6 ms: 1.14x slower                                                 |
| nbody          | 85.1 ms                                                      | 127 ms: 1.49x slower                                                  |
| Geometric mean | (ref)                                                        | 1.14x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 20.3 ms: 1.12x faster                                                 |
| regex_effbot   | 3.08 ms                                                      | 2.94 ms: 1.05x faster                                                 |
| regex_dna      | 180 ms                                                       | 175 ms: 1.03x faster                                                  |
| regex_compile  | 132 ms                                                       | 144 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.92 sec: 1.04x faster                                                |
| xml_etree_parse      | 136 ms                                                       | 140 ms: 1.02x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 11.1 ms: 1.05x slower                                                 |
| json_loads           | 27.0 us                                                      | 31.1 us: 1.15x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 243 us: 1.15x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 343 us: 1.17x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 102 ms: 1.20x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 75.6 ms: 1.27x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.10x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 40.6 ms: 1.19x slower                                                 |
| mako            | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.30x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 132 ms: 2.39x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.32 sec: 1.78x faster                                                |
| gc_traversal               | 3.14 ms                                                      | 1.94 ms: 1.62x faster                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 6.98 ms: 1.58x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 691 ms: 1.32x faster                                                  |
| deepcopy                   | 355 us                                                       | 271 us: 1.31x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 31.3 us: 1.25x faster                                                 |
| async_tree_io              | 876 ms                                                       | 708 ms: 1.24x faster                                                  |
| go                         | 141 ms                                                       | 122 ms: 1.15x faster                                                  |
| pidigits                   | 217 ms                                                       | 188 ms: 1.15x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 1.95 us: 1.13x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 592 ms: 1.12x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 20.3 ms: 1.12x faster                                                 |
| scimark_sor                | 134 ms                                                       | 121 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 576 ms: 1.11x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 423 ms: 1.09x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 144 us: 1.08x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.1 ms: 1.06x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.97 us: 1.05x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.94 ms: 1.05x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 396 ms: 1.04x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.92 sec: 1.04x faster                                                |
| dulwich_log                | 74.8 ms                                                      | 72.0 ms: 1.04x faster                                                 |
| spectral_norm              | 111 ms                                                       | 108 ms: 1.03x faster                                                  |
| regex_dna                  | 180 ms                                                       | 175 ms: 1.03x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 510 ms: 1.02x faster                                                  |
| async_tree_none            | 354 ms                                                       | 348 ms: 1.02x faster                                                  |
| scimark_fft                | 349 ms                                                       | 343 ms: 1.02x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.39 sec: 1.01x faster                                                |
| logging_silent             | 103 ns                                                       | 102 ns: 1.00x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 68.1 ms: 1.02x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                                |
| xml_etree_parse            | 136 ms                                                       | 140 ms: 1.02x slower                                                  |
| async_generators           | 377 ms                                                       | 388 ms: 1.03x slower                                                  |
| pyflate                    | 449 ms                                                       | 464 ms: 1.03x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.7 ms: 1.05x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 11.1 ms: 1.05x slower                                                 |
| comprehensions             | 16.5 us                                                      | 17.6 us: 1.07x slower                                                 |
| chaos                      | 57.3 ms                                                      | 61.9 ms: 1.08x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 6.51 ms: 1.09x slower                                                 |
| json                       | 4.93 ms                                                      | 5.36 ms: 1.09x slower                                                 |
| regex_compile              | 132 ms                                                       | 144 ms: 1.09x slower                                                  |
| logging_simple             | 6.16 us                                                      | 6.73 us: 1.09x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 812 ms: 1.10x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 22.0 ms: 1.11x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 87.5 ms: 1.11x slower                                                 |
| logging_format             | 6.84 us                                                      | 7.66 us: 1.12x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.67 sec: 1.12x slower                                                |
| generators                 | 28.8 ms                                                      | 32.5 ms: 1.13x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.96 sec: 1.13x slower                                                |
| scimark_lu                 | 113 ms                                                       | 128 ms: 1.14x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.53 ms: 1.14x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.38 ms: 1.14x slower                                                 |
| float                      | 77.5 ms                                                      | 88.6 ms: 1.14x slower                                                 |
| json_loads                 | 27.0 us                                                      | 31.1 us: 1.15x slower                                                 |
| sympy_str                  | 275 ms                                                       | 317 ms: 1.15x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 243 us: 1.15x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 180 ms: 1.16x slower                                                  |
| richards                   | 45.2 ms                                                      | 52.6 ms: 1.16x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 343 us: 1.17x slower                                                  |
| richards_super             | 51.6 ms                                                      | 60.2 ms: 1.17x slower                                                 |
| thrift                     | 778 us                                                       | 911 us: 1.17x slower                                                  |
| sympy_expand               | 457 ms                                                       | 535 ms: 1.17x slower                                                  |
| raytrace                   | 253 ms                                                       | 299 ms: 1.19x slower                                                  |
| django_template            | 34.1 ms                                                      | 40.6 ms: 1.19x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.73 ms: 1.20x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 102 ms: 1.20x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 79.7 ms: 1.22x slower                                                 |
| meteor_contest             | 102 ms                                                       | 126 ms: 1.24x slower                                                  |
| fannkuch                   | 370 ms                                                       | 467 ms: 1.26x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 75.6 ms: 1.27x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 89.9 ms: 1.32x slower                                                 |
| coverage                   | 83.0 ms                                                      | 115 ms: 1.39x slower                                                  |
| mako                       | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                                 |
| nbody                      | 85.1 ms                                                      | 127 ms: 1.49x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.48 ms: 1.61x slower                                                 |
| telco                      | 7.82 ms                                                      | 174 ms: 22.28x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.07x slower                                                          |

Benchmark hidden because not significant (2): async_tree_none_tg, xml_etree_iterparse
Ignored benchmarks (23) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260523-3.16.0a0-a7d5a6c-NOGIL/bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.066x slower

# HPT report

- Reliability score: 95.50% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.39x