# Results vs. 3.13.0rc2

- fork: python
- ref: acefff95eab3db6b7cf8
- machine: linux-x86_64
- commit hash: acefff9
- commit date: 2026-05-17
- overall geometric mean: 1.074x slower
- HPT reliability: 99.75%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.62 sec                                                     | 2.97 sec: 1.13x slower                                                |
| html5lib       | 67.0 ms                                                      | 68.3 ms: 1.02x slower                                                 |
| Geometric mean | (ref)                                                        | 1.07x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 689 ms: 1.33x faster                                                  |
| async_tree_io              | 876 ms                                                       | 716 ms: 1.22x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 422 ms: 1.09x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 399 ms: 1.04x faster                                                  |
| async_tree_none            | 354 ms                                                       | 343 ms: 1.03x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 326 ms: 1.03x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 509 ms: 1.02x faster                                                  |
| async_generators           | 377 ms                                                       | 387 ms: 1.03x slower                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 690 ms: 1.04x slower                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 670 ms: 1.05x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.9 ms: 1.06x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 224 ms: 1.04x slower                                                  |
| float          | 77.5 ms                                                      | 87.4 ms: 1.13x slower                                                 |
| nbody          | 85.1 ms                                                      | 126 ms: 1.48x slower                                                  |
| Geometric mean | (ref)                                                        | 1.20x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 20.6 ms: 1.10x faster                                                 |
| regex_effbot   | 3.08 ms                                                      | 2.95 ms: 1.05x faster                                                 |
| regex_dna      | 180 ms                                                       | 175 ms: 1.03x faster                                                  |
| regex_compile  | 132 ms                                                       | 145 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                        | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.99 sec: 1.01x faster                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 95.3 ms: 1.00x slower                                                 |
| xml_etree_parse      | 136 ms                                                       | 140 ms: 1.03x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 10.9 ms: 1.04x slower                                                 |
| json_loads           | 27.0 us                                                      | 31.1 us: 1.15x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 242 us: 1.15x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 344 us: 1.17x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 102 ms: 1.19x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 75.7 ms: 1.28x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.11x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 40.1 ms: 1.18x slower                                                 |
| mako            | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 133 ms: 2.39x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.33 sec: 1.77x faster                                                |
| gc_traversal               | 3.14 ms                                                      | 1.90 ms: 1.65x faster                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 6.97 ms: 1.58x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 689 ms: 1.33x faster                                                  |
| deepcopy                   | 355 us                                                       | 270 us: 1.31x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 31.3 us: 1.25x faster                                                 |
| async_tree_io              | 876 ms                                                       | 716 ms: 1.22x faster                                                  |
| go                         | 141 ms                                                       | 123 ms: 1.14x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 1.95 us: 1.13x faster                                                 |
| scimark_sor                | 134 ms                                                       | 121 ms: 1.11x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 20.6 ms: 1.10x faster                                                 |
| async_tree_memoization     | 461 ms                                                       | 422 ms: 1.09x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 144 us: 1.07x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 18.0 ms: 1.06x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.96 us: 1.05x faster                                                 |
| dulwich_log                | 74.8 ms                                                      | 71.5 ms: 1.05x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.95 ms: 1.05x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 399 ms: 1.04x faster                                                  |
| async_tree_none            | 354 ms                                                       | 343 ms: 1.03x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 326 ms: 1.03x faster                                                  |
| regex_dna                  | 180 ms                                                       | 175 ms: 1.03x faster                                                  |
| spectral_norm              | 111 ms                                                       | 108 ms: 1.03x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 509 ms: 1.02x faster                                                  |
| scimark_fft                | 349 ms                                                       | 344 ms: 1.01x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.99 sec: 1.01x faster                                                |
| bpe_tokeniser              | 4.45 sec                                                     | 4.43 sec: 1.00x faster                                                |
| xml_etree_iterparse        | 94.9 ms                                                      | 95.3 ms: 1.00x slower                                                 |
| html5lib                   | 67.0 ms                                                      | 68.3 ms: 1.02x slower                                                 |
| async_generators           | 377 ms                                                       | 387 ms: 1.03x slower                                                  |
| xml_etree_parse            | 136 ms                                                       | 140 ms: 1.03x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 10.9 ms: 1.04x slower                                                 |
| pidigits                   | 217 ms                                                       | 224 ms: 1.04x slower                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 690 ms: 1.04x slower                                                  |
| logging_silent             | 103 ns                                                       | 106 ns: 1.04x slower                                                  |
| pyflate                    | 449 ms                                                       | 467 ms: 1.04x slower                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 670 ms: 1.05x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.18 sec: 1.05x slower                                                |
| coroutines                 | 23.6 ms                                                      | 24.9 ms: 1.06x slower                                                 |
| comprehensions             | 16.5 us                                                      | 17.5 us: 1.07x slower                                                 |
| json                       | 4.93 ms                                                      | 5.34 ms: 1.08x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 6.55 ms: 1.09x slower                                                 |
| regex_compile              | 132 ms                                                       | 145 ms: 1.09x slower                                                  |
| chaos                      | 57.3 ms                                                      | 63.1 ms: 1.10x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.49 ms: 1.11x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 822 ms: 1.11x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 22.3 ms: 1.12x slower                                                 |
| logging_simple             | 6.16 us                                                      | 6.95 us: 1.13x slower                                                 |
| float                      | 77.5 ms                                                      | 87.4 ms: 1.13x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 88.7 ms: 1.13x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.97 sec: 1.13x slower                                                |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.34 ms: 1.13x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.70 sec: 1.14x slower                                                |
| scimark_lu                 | 113 ms                                                       | 128 ms: 1.14x slower                                                  |
| logging_format             | 6.84 us                                                      | 7.84 us: 1.15x slower                                                 |
| json_loads                 | 27.0 us                                                      | 31.1 us: 1.15x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 242 us: 1.15x slower                                                  |
| generators                 | 28.8 ms                                                      | 33.5 ms: 1.16x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 181 ms: 1.17x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 344 us: 1.17x slower                                                  |
| richards_super             | 51.6 ms                                                      | 60.3 ms: 1.17x slower                                                 |
| richards                   | 45.2 ms                                                      | 52.9 ms: 1.17x slower                                                 |
| sympy_str                  | 275 ms                                                       | 321 ms: 1.17x slower                                                  |
| sympy_expand               | 457 ms                                                       | 536 ms: 1.17x slower                                                  |
| thrift                     | 778 us                                                       | 913 us: 1.17x slower                                                  |
| django_template            | 34.1 ms                                                      | 40.1 ms: 1.18x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.70 ms: 1.18x slower                                                 |
| raytrace                   | 253 ms                                                       | 301 ms: 1.19x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 102 ms: 1.19x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 79.3 ms: 1.21x slower                                                 |
| fannkuch                   | 370 ms                                                       | 459 ms: 1.24x slower                                                  |
| meteor_contest             | 102 ms                                                       | 129 ms: 1.27x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 75.7 ms: 1.28x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 89.3 ms: 1.32x slower                                                 |
| coverage                   | 83.0 ms                                                      | 115 ms: 1.38x slower                                                  |
| mako                       | 11.3 ms                                                      | 16.0 ms: 1.41x slower                                                 |
| nbody                      | 85.1 ms                                                      | 126 ms: 1.48x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.47 ms: 1.60x slower                                                 |
| telco                      | 7.82 ms                                                      | 178 ms: 22.71x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.08x slower                                                          |
Ignored benchmarks (23) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260517-3.16.0a0-acefff9-NOGIL/bm-20260517-vultr-x86_64-python-acefff95eab3db6b7cf8-3.16.0a0-acefff9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.074x slower

# HPT report

- Reliability score: 99.75% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.02x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.39x