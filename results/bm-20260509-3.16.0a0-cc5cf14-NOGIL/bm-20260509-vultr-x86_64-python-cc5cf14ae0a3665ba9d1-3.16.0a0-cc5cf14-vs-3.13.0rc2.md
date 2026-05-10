# Results vs. 3.13.0rc2

- fork: python
- ref: cc5cf14ae0a3665ba9d1
- machine: linux-x86_64
- commit hash: cc5cf14
- commit date: 2026-05-09
- overall geometric mean: 1.073x slower
- HPT reliability: 96.41%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.38x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.62 sec                                                     | 2.96 sec: 1.13x slower                                                |
| html5lib       | 67.0 ms                                                      | 70.0 ms: 1.04x slower                                                 |
| Geometric mean | (ref)                                                        | 1.09x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 691 ms: 1.32x faster                                                  |
| async_tree_io              | 876 ms                                                       | 709 ms: 1.24x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 584 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 573 ms: 1.11x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 419 ms: 1.10x faster                                                  |
| asyncio_tcp                | 505 ms                                                       | 463 ms: 1.09x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 393 ms: 1.05x faster                                                  |
| async_tree_none            | 354 ms                                                       | 340 ms: 1.04x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 325 ms: 1.04x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 509 ms: 1.02x faster                                                  |
| async_generators           | 377 ms                                                       | 387 ms: 1.03x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 25.0 ms: 1.06x slower                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.68 sec: 1.11x slower                                                |
| Geometric mean             | (ref)                                                        | 1.07x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 194 ms: 1.12x faster                                                  |
| float          | 77.5 ms                                                      | 88.6 ms: 1.14x slower                                                 |
| nbody          | 85.1 ms                                                      | 124 ms: 1.46x slower                                                  |
| Geometric mean | (ref)                                                        | 1.14x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 20.2 ms: 1.13x faster                                                 |
| regex_effbot   | 3.08 ms                                                      | 2.94 ms: 1.05x faster                                                 |
| regex_dna      | 180 ms                                                       | 172 ms: 1.05x faster                                                  |
| regex_compile  | 132 ms                                                       | 145 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.97 sec: 1.02x faster                                                |
| pickle_list          | 4.93 us                                                      | 4.84 us: 1.02x faster                                                 |
| pickle_dict          | 32.5 us                                                      | 32.4 us: 1.01x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 95.4 ms: 1.00x slower                                                 |
| xml_etree_parse      | 136 ms                                                       | 140 ms: 1.03x slower                                                  |
| json_dumps           | 10.5 ms                                                      | 10.9 ms: 1.04x slower                                                 |
| pickle               | 11.3 us                                                      | 12.6 us: 1.11x slower                                                 |
| json_loads           | 27.0 us                                                      | 30.8 us: 1.14x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 247 us: 1.18x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 347 us: 1.18x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 101 ms: 1.18x slower                                                  |
| unpickle             | 14.3 us                                                      | 17.0 us: 1.18x slower                                                 |
| unpickle_list        | 4.71 us                                                      | 5.89 us: 1.25x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 74.9 ms: 1.26x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.10x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 39.6 ms: 1.16x slower                                                 |
| mako            | 11.3 ms                                                      | 15.9 ms: 1.40x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.28x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 132 ms: 2.40x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.33 sec: 1.77x faster                                                |
| gc_traversal               | 3.14 ms                                                      | 1.89 ms: 1.67x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 691 ms: 1.32x faster                                                  |
| deepcopy                   | 355 us                                                       | 272 us: 1.30x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 31.4 us: 1.24x faster                                                 |
| async_tree_io              | 876 ms                                                       | 709 ms: 1.24x faster                                                  |
| go                         | 141 ms                                                       | 123 ms: 1.14x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 584 ms: 1.14x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 20.2 ms: 1.13x faster                                                 |
| sqlite_synth               | 2.21 us                                                      | 1.96 us: 1.12x faster                                                 |
| pidigits                   | 217 ms                                                       | 194 ms: 1.12x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 573 ms: 1.11x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 419 ms: 1.10x faster                                                  |
| asyncio_tcp                | 505 ms                                                       | 463 ms: 1.09x faster                                                  |
| scimark_sor                | 134 ms                                                       | 123 ms: 1.09x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 393 ms: 1.05x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 71.1 ms: 1.05x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 2.94 ms: 1.05x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 18.3 ms: 1.05x faster                                                 |
| regex_dna                  | 180 ms                                                       | 172 ms: 1.05x faster                                                  |
| async_tree_none            | 354 ms                                                       | 340 ms: 1.04x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 325 ms: 1.04x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.01 us: 1.03x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 509 ms: 1.02x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.97 sec: 1.02x faster                                                |
| pickle_list                | 4.93 us                                                      | 4.84 us: 1.02x faster                                                 |
| spectral_norm              | 111 ms                                                       | 109 ms: 1.01x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.40 sec: 1.01x faster                                                |
| scimark_fft                | 349 ms                                                       | 347 ms: 1.01x faster                                                  |
| pickle_dict                | 32.5 us                                                      | 32.4 us: 1.01x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 95.4 ms: 1.00x slower                                                 |
| async_generators           | 377 ms                                                       | 387 ms: 1.03x slower                                                  |
| xml_etree_parse            | 136 ms                                                       | 140 ms: 1.03x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 10.9 ms: 1.04x slower                                                 |
| pyflate                    | 449 ms                                                       | 466 ms: 1.04x slower                                                  |
| html5lib                   | 67.0 ms                                                      | 70.0 ms: 1.04x slower                                                 |
| logging_silent             | 103 ns                                                       | 108 ns: 1.05x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.18 sec: 1.06x slower                                                |
| coroutines                 | 23.6 ms                                                      | 25.0 ms: 1.06x slower                                                 |
| comprehensions             | 16.5 us                                                      | 17.5 us: 1.07x slower                                                 |
| json                       | 4.93 ms                                                      | 5.36 ms: 1.09x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 6.55 ms: 1.09x slower                                                 |
| regex_compile              | 132 ms                                                       | 145 ms: 1.09x slower                                                  |
| chaos                      | 57.3 ms                                                      | 62.9 ms: 1.10x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 818 ms: 1.11x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.49 ms: 1.11x slower                                                 |
| generators                 | 28.8 ms                                                      | 32.1 ms: 1.11x slower                                                 |
| pickle                     | 11.3 us                                                      | 12.6 us: 1.11x slower                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.68 sec: 1.11x slower                                                |
| sympy_integrate            | 19.8 ms                                                      | 22.2 ms: 1.12x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 88.3 ms: 1.12x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.96 sec: 1.13x slower                                                |
| pprint_pformat             | 1.50 sec                                                     | 1.70 sec: 1.14x slower                                                |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.36 ms: 1.14x slower                                                 |
| json_loads                 | 27.0 us                                                      | 30.8 us: 1.14x slower                                                 |
| float                      | 77.5 ms                                                      | 88.6 ms: 1.14x slower                                                 |
| logging_simple             | 6.16 us                                                      | 7.07 us: 1.15x slower                                                 |
| sympy_str                  | 275 ms                                                       | 316 ms: 1.15x slower                                                  |
| unpack_sequence            | 44.8 ns                                                      | 51.5 ns: 1.15x slower                                                 |
| richards_super             | 51.6 ms                                                      | 59.6 ms: 1.15x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 130 ms: 1.16x slower                                                  |
| logging_format             | 6.84 us                                                      | 7.92 us: 1.16x slower                                                 |
| richards                   | 45.2 ms                                                      | 52.4 ms: 1.16x slower                                                 |
| django_template            | 34.1 ms                                                      | 39.6 ms: 1.16x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 181 ms: 1.16x slower                                                  |
| sympy_expand               | 457 ms                                                       | 536 ms: 1.17x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 247 us: 1.18x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 347 us: 1.18x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 101 ms: 1.18x slower                                                  |
| unpickle                   | 14.3 us                                                      | 17.0 us: 1.18x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.77 ms: 1.21x slower                                                 |
| thrift                     | 778 us                                                       | 939 us: 1.21x slower                                                  |
| raytrace                   | 253 ms                                                       | 306 ms: 1.21x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 79.5 ms: 1.22x slower                                                 |
| unpickle_list              | 4.71 us                                                      | 5.89 us: 1.25x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 74.9 ms: 1.26x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 13.9 ms: 1.26x slower                                                 |
| meteor_contest             | 102 ms                                                       | 129 ms: 1.27x slower                                                  |
| fannkuch                   | 370 ms                                                       | 469 ms: 1.27x slower                                                  |
| typing_runtime_protocols   | 155 us                                                       | 201 us: 1.30x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 89.8 ms: 1.32x slower                                                 |
| coverage                   | 83.0 ms                                                      | 115 ms: 1.39x slower                                                  |
| mako                       | 11.3 ms                                                      | 15.9 ms: 1.40x slower                                                 |
| nbody                      | 85.1 ms                                                      | 124 ms: 1.46x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.47 ms: 1.60x slower                                                 |
| telco                      | 7.82 ms                                                      | 177 ms: 22.58x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.08x slower                                                          |
Ignored benchmarks (15) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260509-3.16.0a0-cc5cf14-NOGIL/bm-20260509-vultr-x86_64-python-cc5cf14ae0a3665ba9d1-3.16.0a0-cc5cf14.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.073x slower

# HPT report

- Reliability score: 96.41% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.38x