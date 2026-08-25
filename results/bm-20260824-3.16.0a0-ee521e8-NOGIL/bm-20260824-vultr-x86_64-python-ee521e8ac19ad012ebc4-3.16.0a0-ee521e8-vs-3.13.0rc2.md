# Results vs. 3.13.0rc2

- fork: python
- ref: ee521e8ac19ad012ebc4
- machine: linux-x86_64
- commit hash: ee521e8
- commit date: 2026-08-24
- overall geometric mean: 1.074x slower
- HPT reliability: 98.34%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 295 ms: 1.14x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.92 sec: 1.12x slower                                                |
| html5lib       | 67.0 ms                                                      | 67.8 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                        | 1.09x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 693 ms: 1.32x faster                                                  |
| async_tree_io              | 876 ms                                                       | 701 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 599 ms: 1.11x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 416 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 581 ms: 1.10x faster                                                  |
| async_tree_none            | 354 ms                                                       | 339 ms: 1.04x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 399 ms: 1.04x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 25.1 ms: 1.06x slower                                                 |
| async_generators           | 377 ms                                                       | 414 ms: 1.10x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.07x faster                                                          |

Benchmark hidden because not significant (1): async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 180 ms: 1.21x faster                                                  |
| float          | 77.5 ms                                                      | 84.3 ms: 1.09x slower                                                 |
| nbody          | 85.1 ms                                                      | 124 ms: 1.45x slower                                                  |
| Geometric mean | (ref)                                                        | 1.09x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 21.3 ms: 1.06x faster                                                 |
| regex_effbot   | 3.08 ms                                                      | 3.01 ms: 1.02x faster                                                 |
| regex_dna      | 180 ms                                                       | 188 ms: 1.04x slower                                                  |
| regex_compile  | 132 ms                                                       | 169 ms: 1.28x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| json_dumps           | 10.5 ms                                                      | 10.0 ms: 1.05x faster                                                 |
| tomli_loads          | 2.01 sec                                                     | 1.97 sec: 1.02x faster                                                |
| xml_etree_iterparse  | 94.9 ms                                                      | 96.5 ms: 1.02x slower                                                 |
| xml_etree_parse      | 136 ms                                                       | 140 ms: 1.03x slower                                                  |
| unpickle_pure_python | 210 us                                                       | 238 us: 1.13x slower                                                  |
| json_loads           | 27.0 us                                                      | 30.7 us: 1.14x slower                                                 |
| pickle_pure_python   | 294 us                                                       | 336 us: 1.14x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 102 ms: 1.20x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 76.0 ms: 1.28x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.91 ms: 1.34x slower                                                 |
| python_startup         | 11.0 ms                                                      | 16.1 ms: 1.46x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.40x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 40.9 ms: 1.20x slower                                                 |
| mako            | 11.3 ms                                                      | 15.8 ms: 1.39x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 131 ms: 2.43x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.31 sec: 1.80x faster                                                |
| gc_traversal               | 3.14 ms                                                      | 1.78 ms: 1.76x faster                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 6.69 ms: 1.64x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 693 ms: 1.32x faster                                                  |
| deepcopy                   | 355 us                                                       | 271 us: 1.31x faster                                                  |
| async_tree_io              | 876 ms                                                       | 701 ms: 1.25x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 31.8 us: 1.23x faster                                                 |
| pidigits                   | 217 ms                                                       | 180 ms: 1.21x faster                                                  |
| go                         | 141 ms                                                       | 120 ms: 1.18x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 1.94 us: 1.14x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 599 ms: 1.11x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 416 ms: 1.11x faster                                                  |
| scimark_sor                | 134 ms                                                       | 122 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 581 ms: 1.10x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.9 ms: 1.07x faster                                                 |
| regex_v8                   | 22.7 ms                                                      | 21.3 ms: 1.06x faster                                                 |
| typing_runtime_protocols   | 155 us                                                       | 146 us: 1.06x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 71.0 ms: 1.05x faster                                                 |
| spectral_norm              | 111 ms                                                       | 105 ms: 1.05x faster                                                  |
| json_dumps                 | 10.5 ms                                                      | 10.0 ms: 1.05x faster                                                 |
| async_tree_none            | 354 ms                                                       | 339 ms: 1.04x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 399 ms: 1.04x faster                                                  |
| deepcopy_reduce            | 3.11 us                                                      | 3.01 us: 1.03x faster                                                 |
| regex_effbot               | 3.08 ms                                                      | 3.01 ms: 1.02x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.35 sec: 1.02x faster                                                |
| tomli_loads                | 2.01 sec                                                     | 1.97 sec: 1.02x faster                                                |
| asyncio_websockets         | 520 ms                                                       | 512 ms: 1.02x faster                                                  |
| scimark_fft                | 349 ms                                                       | 347 ms: 1.01x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 67.8 ms: 1.01x slower                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 96.5 ms: 1.02x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.37 ms: 1.02x slower                                                 |
| pyflate                    | 449 ms                                                       | 461 ms: 1.03x slower                                                  |
| xml_etree_parse            | 136 ms                                                       | 140 ms: 1.03x slower                                                  |
| regex_dna                  | 180 ms                                                       | 188 ms: 1.04x slower                                                  |
| logging_silent             | 103 ns                                                       | 107 ns: 1.05x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.18 sec: 1.05x slower                                                |
| chaos                      | 57.3 ms                                                      | 60.5 ms: 1.06x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 25.1 ms: 1.06x slower                                                 |
| comprehensions             | 16.5 us                                                      | 17.8 us: 1.08x slower                                                 |
| float                      | 77.5 ms                                                      | 84.3 ms: 1.09x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 6.57 ms: 1.10x slower                                                 |
| json                       | 4.93 ms                                                      | 5.40 ms: 1.10x slower                                                 |
| async_generators           | 377 ms                                                       | 414 ms: 1.10x slower                                                  |
| sympy_integrate            | 19.8 ms                                                      | 21.8 ms: 1.10x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 820 ms: 1.11x slower                                                  |
| docutils                   | 2.62 sec                                                     | 2.92 sec: 1.12x slower                                                |
| nqueens                    | 78.6 ms                                                      | 88.2 ms: 1.12x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.32 ms: 1.13x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 238 us: 1.13x slower                                                  |
| pprint_pformat             | 1.50 sec                                                     | 1.69 sec: 1.13x slower                                                |
| 2to3                       | 260 ms                                                       | 295 ms: 1.14x slower                                                  |
| json_loads                 | 27.0 us                                                      | 30.7 us: 1.14x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 336 us: 1.14x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 130 ms: 1.16x slower                                                  |
| logging_simple             | 6.16 us                                                      | 7.12 us: 1.16x slower                                                 |
| sympy_str                  | 275 ms                                                       | 318 ms: 1.16x slower                                                  |
| generators                 | 28.8 ms                                                      | 33.5 ms: 1.16x slower                                                 |
| raytrace                   | 253 ms                                                       | 294 ms: 1.16x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 181 ms: 1.16x slower                                                  |
| richards                   | 45.2 ms                                                      | 52.9 ms: 1.17x slower                                                 |
| richards_super             | 51.6 ms                                                      | 60.8 ms: 1.18x slower                                                 |
| sympy_expand               | 457 ms                                                       | 540 ms: 1.18x slower                                                  |
| logging_format             | 6.84 us                                                      | 8.11 us: 1.19x slower                                                 |
| deltablue                  | 3.12 ms                                                      | 3.71 ms: 1.19x slower                                                 |
| thrift                     | 778 us                                                       | 928 us: 1.19x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 78.1 ms: 1.19x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 102 ms: 1.20x slower                                                  |
| django_template            | 34.1 ms                                                      | 40.9 ms: 1.20x slower                                                 |
| fannkuch                   | 370 ms                                                       | 462 ms: 1.25x slower                                                  |
| meteor_contest             | 102 ms                                                       | 128 ms: 1.26x slower                                                  |
| regex_compile              | 132 ms                                                       | 169 ms: 1.28x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 76.0 ms: 1.28x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 88.5 ms: 1.30x slower                                                 |
| python_startup_no_site     | 7.39 ms                                                      | 9.91 ms: 1.34x slower                                                 |
| mako                       | 11.3 ms                                                      | 15.8 ms: 1.39x slower                                                 |
| coverage                   | 83.0 ms                                                      | 116 ms: 1.40x slower                                                  |
| nbody                      | 85.1 ms                                                      | 124 ms: 1.45x slower                                                  |
| python_startup             | 11.0 ms                                                      | 16.1 ms: 1.46x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.48 ms: 1.61x slower                                                 |
| telco                      | 7.82 ms                                                      | 174 ms: 22.30x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.08x slower                                                          |

Benchmark hidden because not significant (1): async_tree_none_tg
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260824-3.16.0a0-ee521e8-NOGIL/bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.074x slower

# HPT report

- Reliability score: 98.34% likely to be slow
- 90% likely to have a slowdown of 1.02x
- 95% likely to have a slowdown of 1.01x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x