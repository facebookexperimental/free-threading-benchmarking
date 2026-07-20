# Results vs. 3.13.0rc2

- fork: python
- ref: c08c89addfe30a3e0e70
- machine: linux-x86_64
- commit hash: c08c89a
- commit date: 2026-07-19
- overall geometric mean: 1.074x slower
- HPT reliability: 99.15%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.35x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 295 ms: 1.13x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.97 sec: 1.14x slower                                                |
| Geometric mean | (ref)                                                        | 1.09x slower                                                          |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 685 ms: 1.33x faster                                                  |
| async_tree_io              | 876 ms                                                       | 706 ms: 1.24x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 416 ms: 1.11x faster                                                  |
| asyncio_tcp                | 505 ms                                                       | 464 ms: 1.09x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 391 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 630 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 609 ms: 1.05x faster                                                  |
| async_tree_none            | 354 ms                                                       | 338 ms: 1.05x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 323 ms: 1.04x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 513 ms: 1.01x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.0 ms: 1.02x slower                                                 |
| async_generators           | 377 ms                                                       | 388 ms: 1.03x slower                                                  |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.71 sec: 1.13x slower                                                |
| Geometric mean             | (ref)                                                        | 1.06x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 205 ms: 1.06x faster                                                  |
| float          | 77.5 ms                                                      | 85.3 ms: 1.10x slower                                                 |
| nbody          | 85.1 ms                                                      | 127 ms: 1.49x slower                                                  |
| Geometric mean | (ref)                                                        | 1.16x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 20.3 ms: 1.12x faster                                                 |
| regex_effbot   | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                                 |
| regex_dna      | 180 ms                                                       | 178 ms: 1.01x faster                                                  |
| regex_compile  | 132 ms                                                       | 169 ms: 1.28x slower                                                  |
| Geometric mean | (ref)                                                        | 1.01x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.95 sec: 1.03x faster                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 95.9 ms: 1.01x slower                                                 |
| json_dumps           | 10.5 ms                                                      | 10.7 ms: 1.02x slower                                                 |
| pickle_dict          | 32.5 us                                                      | 33.1 us: 1.02x slower                                                 |
| xml_etree_parse      | 136 ms                                                       | 141 ms: 1.03x slower                                                  |
| pickle_list          | 4.93 us                                                      | 5.51 us: 1.12x slower                                                 |
| json_loads           | 27.0 us                                                      | 30.3 us: 1.12x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 239 us: 1.14x slower                                                  |
| pickle               | 11.3 us                                                      | 13.1 us: 1.16x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 342 us: 1.16x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 102 ms: 1.19x slower                                                  |
| unpickle             | 14.3 us                                                      | 17.2 us: 1.20x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 75.0 ms: 1.26x slower                                                 |
| unpickle_list        | 4.71 us                                                      | 5.96 us: 1.27x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.12x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.32 ms: 1.26x slower                                                 |
| python_startup         | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.34x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 40.4 ms: 1.18x slower                                                 |
| mako            | 11.3 ms                                                      | 15.7 ms: 1.39x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.28x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 132 ms: 2.41x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.30 sec: 1.81x faster                                                |
| gc_traversal               | 3.14 ms                                                      | 1.78 ms: 1.76x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 685 ms: 1.33x faster                                                  |
| deepcopy                   | 355 us                                                       | 279 us: 1.27x faster                                                  |
| async_tree_io              | 876 ms                                                       | 706 ms: 1.24x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 31.7 us: 1.23x faster                                                 |
| go                         | 141 ms                                                       | 121 ms: 1.17x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 1.95 us: 1.13x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 20.3 ms: 1.12x faster                                                 |
| async_tree_memoization     | 461 ms                                                       | 416 ms: 1.11x faster                                                  |
| scimark_sor                | 134 ms                                                       | 123 ms: 1.09x faster                                                  |
| asyncio_tcp                | 505 ms                                                       | 464 ms: 1.09x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.8 ms: 1.08x faster                                                 |
| typing_runtime_protocols   | 155 us                                                       | 144 us: 1.07x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.88 ms: 1.07x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 391 ms: 1.06x faster                                                  |
| pidigits                   | 217 ms                                                       | 205 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 630 ms: 1.06x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 609 ms: 1.05x faster                                                  |
| async_tree_none            | 354 ms                                                       | 338 ms: 1.05x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 71.7 ms: 1.04x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 323 ms: 1.04x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.00 us: 1.04x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.95 sec: 1.03x faster                                                |
| spectral_norm              | 111 ms                                                       | 109 ms: 1.02x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 513 ms: 1.01x faster                                                  |
| regex_dna                  | 180 ms                                                       | 178 ms: 1.01x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.40 sec: 1.01x faster                                                |
| xml_etree_iterparse        | 94.9 ms                                                      | 95.9 ms: 1.01x slower                                                 |
| scimark_fft                | 349 ms                                                       | 354 ms: 1.01x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 10.7 ms: 1.02x slower                                                 |
| pickle_dict                | 32.5 us                                                      | 33.1 us: 1.02x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 24.0 ms: 1.02x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                                |
| async_generators           | 377 ms                                                       | 388 ms: 1.03x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.38 ms: 1.03x slower                                                 |
| xml_etree_parse            | 136 ms                                                       | 141 ms: 1.03x slower                                                  |
| unpack_sequence            | 44.8 ns                                                      | 46.4 ns: 1.04x slower                                                 |
| pyflate                    | 449 ms                                                       | 464 ms: 1.04x slower                                                  |
| logging_silent             | 103 ns                                                       | 108 ns: 1.06x slower                                                  |
| json                       | 4.93 ms                                                      | 5.36 ms: 1.09x slower                                                 |
| chaos                      | 57.3 ms                                                      | 62.6 ms: 1.09x slower                                                 |
| comprehensions             | 16.5 us                                                      | 18.0 us: 1.09x slower                                                 |
| float                      | 77.5 ms                                                      | 85.3 ms: 1.10x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 6.60 ms: 1.10x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 817 ms: 1.11x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 22.0 ms: 1.11x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 87.4 ms: 1.11x slower                                                 |
| pickle_list                | 4.93 us                                                      | 5.51 us: 1.12x slower                                                 |
| json_loads                 | 27.0 us                                                      | 30.3 us: 1.12x slower                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.71 sec: 1.13x slower                                                |
| pprint_pformat             | 1.50 sec                                                     | 1.69 sec: 1.13x slower                                                |
| 2to3                       | 260 ms                                                       | 295 ms: 1.13x slower                                                  |
| logging_simple             | 6.16 us                                                      | 7.00 us: 1.14x slower                                                 |
| docutils                   | 2.62 sec                                                     | 2.97 sec: 1.14x slower                                                |
| unpickle_pure_python       | 210 us                                                       | 239 us: 1.14x slower                                                  |
| sympy_str                  | 275 ms                                                       | 314 ms: 1.14x slower                                                  |
| generators                 | 28.8 ms                                                      | 33.0 ms: 1.15x slower                                                 |
| sympy_expand               | 457 ms                                                       | 526 ms: 1.15x slower                                                  |
| pickle                     | 11.3 us                                                      | 13.1 us: 1.16x slower                                                 |
| sympy_sum                  | 156 ms                                                       | 180 ms: 1.16x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 342 us: 1.16x slower                                                  |
| richards_super             | 51.6 ms                                                      | 60.0 ms: 1.16x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 131 ms: 1.16x slower                                                  |
| thrift                     | 778 us                                                       | 909 us: 1.17x slower                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.50 ms: 1.17x slower                                                 |
| logging_format             | 6.84 us                                                      | 8.01 us: 1.17x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.69 ms: 1.18x slower                                                 |
| django_template            | 34.1 ms                                                      | 40.4 ms: 1.18x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 102 ms: 1.19x slower                                                  |
| richards                   | 45.2 ms                                                      | 54.0 ms: 1.19x slower                                                 |
| unpickle                   | 14.3 us                                                      | 17.2 us: 1.20x slower                                                 |
| raytrace                   | 253 ms                                                       | 304 ms: 1.20x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 78.9 ms: 1.21x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 13.3 ms: 1.21x slower                                                 |
| meteor_contest             | 102 ms                                                       | 125 ms: 1.23x slower                                                  |
| fannkuch                   | 370 ms                                                       | 465 ms: 1.26x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 9.32 ms: 1.26x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 75.0 ms: 1.26x slower                                                 |
| unpickle_list              | 4.71 us                                                      | 5.96 us: 1.27x slower                                                 |
| regex_compile              | 132 ms                                                       | 169 ms: 1.28x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 89.7 ms: 1.32x slower                                                 |
| coverage                   | 83.0 ms                                                      | 114 ms: 1.37x slower                                                  |
| mako                       | 11.3 ms                                                      | 15.7 ms: 1.39x slower                                                 |
| python_startup             | 11.0 ms                                                      | 15.7 ms: 1.43x slower                                                 |
| nbody                      | 85.1 ms                                                      | 127 ms: 1.49x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.50 ms: 1.63x slower                                                 |
| telco                      | 7.82 ms                                                      | 175 ms: 22.41x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.09x slower                                                          |

Benchmark hidden because not significant (1): html5lib
Ignored benchmarks (12) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260719-3.16.0a0-c08c89a-NOGIL/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.074x slower

# HPT report

- Reliability score: 99.15% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.35x