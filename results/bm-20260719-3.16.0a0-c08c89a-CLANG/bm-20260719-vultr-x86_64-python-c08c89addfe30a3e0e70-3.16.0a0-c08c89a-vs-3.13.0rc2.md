# Results vs. 3.13.0rc2

- fork: python
- ref: c08c89addfe30a3e0e70
- machine: linux-x86_64
- commit hash: c08c89a
- commit date: 2026-07-19
- overall geometric mean: 1.063x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 254 ms: 1.02x faster                                                  |
| docutils       | 2.62 sec                                                     | 2.36 sec: 1.11x faster                                                |
| html5lib       | 67.0 ms                                                      | 57.5 ms: 1.17x faster                                                 |
| Geometric mean | (ref)                                                        | 1.10x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 666 ms                                                       | 521 ms: 1.28x faster                                                  |
| async_tree_none            | 354 ms                                                       | 280 ms: 1.26x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 366 ms: 1.26x faster                                                  |
| async_tree_io              | 876 ms                                                       | 707 ms: 1.24x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 761 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 545 ms: 1.17x faster                                                  |
| async_generators           | 377 ms                                                       | 323 ms: 1.17x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 357 ms: 1.16x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 293 ms: 1.15x faster                                                  |
| asyncio_tcp                | 505 ms                                                       | 440 ms: 1.15x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 22.8 ms: 1.04x faster                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.48 sec: 1.02x faster                                                |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.15x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 191 ms: 1.13x faster                                                  |
| float          | 77.5 ms                                                      | 71.6 ms: 1.08x faster                                                 |
| nbody          | 85.1 ms                                                      | 82.3 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                        | 1.08x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 22.9 ms: 1.01x slower                                                 |
| regex_effbot   | 3.08 ms                                                      | 3.25 ms: 1.06x slower                                                 |
| regex_compile  | 132 ms                                                       | 143 ms: 1.08x slower                                                  |
| regex_dna      | 180 ms                                                       | 196 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                        | 1.06x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 9.29 ms: 1.13x faster                                                 |
| unpickle_list        | 4.71 us                                                      | 4.25 us: 1.11x faster                                                 |
| tomli_loads          | 2.01 sec                                                     | 1.81 sec: 1.11x faster                                                |
| xml_etree_process    | 59.3 ms                                                      | 56.6 ms: 1.05x faster                                                 |
| pickle_dict          | 32.5 us                                                      | 31.2 us: 1.04x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 82.9 ms: 1.03x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 92.8 ms: 1.02x faster                                                 |
| unpickle_pure_python | 210 us                                                       | 208 us: 1.01x faster                                                  |
| json_loads           | 27.0 us                                                      | 26.8 us: 1.01x faster                                                 |
| pickle_pure_python   | 294 us                                                       | 299 us: 1.02x slower                                                  |
| pickle_list          | 4.93 us                                                      | 5.29 us: 1.07x slower                                                 |
| xml_etree_parse      | 136 ms                                                       | 159 ms: 1.17x slower                                                  |
| pickle               | 11.3 us                                                      | 13.7 us: 1.20x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.00x faster                                                          |

Benchmark hidden because not significant (1): unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 7.18 ms: 1.03x faster                                                 |
| python_startup         | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.05x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 32.7 ms: 1.04x faster                                                 |
| mako            | 11.3 ms                                                      | 12.0 ms: 1.06x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.01x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 111 ms: 2.87x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.07 sec: 2.21x faster                                                |
| deepcopy                   | 355 us                                                       | 217 us: 1.64x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 24.9 us: 1.57x faster                                                 |
| go                         | 141 ms                                                       | 101 ms: 1.40x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 112 us: 1.38x faster                                                  |
| scimark_sor                | 134 ms                                                       | 102 ms: 1.32x faster                                                  |
| spectral_norm              | 111 ms                                                       | 84.8 ms: 1.31x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.39 us: 1.30x faster                                                 |
| logging_silent             | 103 ns                                                       | 79.5 ns: 1.29x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 521 ms: 1.28x faster                                                  |
| async_tree_none            | 354 ms                                                       | 280 ms: 1.26x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 366 ms: 1.26x faster                                                  |
| scimark_fft                | 349 ms                                                       | 278 ms: 1.25x faster                                                  |
| async_tree_io              | 876 ms                                                       | 707 ms: 1.24x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 761 ms: 1.20x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 545 ms: 1.17x faster                                                  |
| richards                   | 45.2 ms                                                      | 38.7 ms: 1.17x faster                                                 |
| async_generators           | 377 ms                                                       | 323 ms: 1.17x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 57.5 ms: 1.17x faster                                                 |
| richards_super             | 51.6 ms                                                      | 44.5 ms: 1.16x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 357 ms: 1.16x faster                                                  |
| comprehensions             | 16.5 us                                                      | 14.3 us: 1.15x faster                                                 |
| async_tree_none_tg         | 336 ms                                                       | 293 ms: 1.15x faster                                                  |
| asyncio_tcp                | 505 ms                                                       | 440 ms: 1.15x faster                                                  |
| pyflate                    | 449 ms                                                       | 391 ms: 1.15x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 9.29 ms: 1.13x faster                                                 |
| pidigits                   | 217 ms                                                       | 191 ms: 1.13x faster                                                  |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.17 ms: 1.13x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 58.0 ms: 1.13x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 70.1 ms: 1.12x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 17.2 ms: 1.11x faster                                                 |
| chaos                      | 57.3 ms                                                      | 51.6 ms: 1.11x faster                                                 |
| unpickle_list              | 4.71 us                                                      | 4.25 us: 1.11x faster                                                 |
| docutils                   | 2.62 sec                                                     | 2.36 sec: 1.11x faster                                                |
| logging_simple             | 6.16 us                                                      | 5.56 us: 1.11x faster                                                 |
| tomli_loads                | 2.01 sec                                                     | 1.81 sec: 1.11x faster                                                |
| dulwich_log                | 74.8 ms                                                      | 67.6 ms: 1.11x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.42 ms: 1.11x faster                                                 |
| deltablue                  | 3.12 ms                                                      | 2.86 ms: 1.09x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 18.2 ms: 1.09x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.28 us: 1.09x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.09 sec: 1.09x faster                                                |
| unpack_sequence            | 44.8 ns                                                      | 41.4 ns: 1.08x faster                                                 |
| float                      | 77.5 ms                                                      | 71.6 ms: 1.08x faster                                                 |
| scimark_lu                 | 113 ms                                                       | 105 ms: 1.08x faster                                                  |
| thrift                     | 778 us                                                       | 728 us: 1.07x faster                                                  |
| raytrace                   | 253 ms                                                       | 238 ms: 1.06x faster                                                  |
| xml_etree_process          | 59.3 ms                                                      | 56.6 ms: 1.05x faster                                                 |
| sympy_str                  | 275 ms                                                       | 263 ms: 1.04x faster                                                  |
| pickle_dict                | 32.5 us                                                      | 31.2 us: 1.04x faster                                                 |
| django_template            | 34.1 ms                                                      | 32.7 ms: 1.04x faster                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.44 sec: 1.04x faster                                                |
| pprint_safe_repr           | 738 ms                                                       | 711 ms: 1.04x faster                                                  |
| sympy_sum                  | 156 ms                                                       | 150 ms: 1.04x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 22.8 ms: 1.04x faster                                                 |
| nbody                      | 85.1 ms                                                      | 82.3 ms: 1.03x faster                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 82.9 ms: 1.03x faster                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 7.18 ms: 1.03x faster                                                 |
| sympy_expand               | 457 ms                                                       | 444 ms: 1.03x faster                                                  |
| coverage                   | 83.0 ms                                                      | 80.6 ms: 1.03x faster                                                 |
| 2to3                       | 260 ms                                                       | 254 ms: 1.02x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 92.8 ms: 1.02x faster                                                 |
| asyncio_tcp_ssl            | 1.51 sec                                                     | 1.48 sec: 1.02x faster                                                |
| generators                 | 28.8 ms                                                      | 28.4 ms: 1.01x faster                                                 |
| unpickle_pure_python       | 210 us                                                       | 208 us: 1.01x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.19 us: 1.01x faster                                                 |
| json_loads                 | 27.0 us                                                      | 26.8 us: 1.01x faster                                                 |
| fannkuch                   | 370 ms                                                       | 368 ms: 1.01x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 22.9 ms: 1.01x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 299 us: 1.02x slower                                                  |
| meteor_contest             | 102 ms                                                       | 104 ms: 1.02x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.14 sec: 1.02x slower                                                |
| crypto_pyaes               | 67.9 ms                                                      | 69.6 ms: 1.03x slower                                                 |
| json                       | 4.93 ms                                                      | 5.15 ms: 1.04x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 544 ms: 1.05x slower                                                  |
| regex_effbot               | 3.08 ms                                                      | 3.25 ms: 1.06x slower                                                 |
| mako                       | 11.3 ms                                                      | 12.0 ms: 1.06x slower                                                 |
| pickle_list                | 4.93 us                                                      | 5.29 us: 1.07x slower                                                 |
| regex_compile              | 132 ms                                                       | 143 ms: 1.08x slower                                                  |
| regex_dna                  | 180 ms                                                       | 196 ms: 1.09x slower                                                  |
| python_startup             | 11.0 ms                                                      | 12.5 ms: 1.14x slower                                                 |
| xml_etree_parse            | 136 ms                                                       | 159 ms: 1.17x slower                                                  |
| pickle                     | 11.3 us                                                      | 13.7 us: 1.20x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.81 ms: 1.35x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.28 ms: 1.40x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 4.51 ms: 1.44x slower                                                 |
| telco                      | 7.82 ms                                                      | 154 ms: 19.64x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 354 ms: 32.21x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.02x faster                                                          |

Benchmark hidden because not significant (1): unpickle
Ignored benchmarks (12) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http
Ignored benchmarks (10) of results/bm-20260719-3.16.0a0-c08c89a-CLANG/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.063x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.16x