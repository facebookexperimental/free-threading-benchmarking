# Results vs. 3.13.0rc2

- fork: python
- ref: 1f9d20bbd4fed601e7ca
- machine: linux-x86_64
- commit hash: 1f9d20b
- commit date: 2026-07-20
- overall geometric mean: 1.069x slower
- HPT reliability: 97.64%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.36x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 294 ms: 1.13x slower                                                  |
| docutils       | 2.62 sec                                                     | 2.96 sec: 1.13x slower                                                |
| html5lib       | 67.0 ms                                                      | 65.0 ms: 1.03x faster                                                 |
| Geometric mean | (ref)                                                        | 1.07x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 683 ms: 1.34x faster                                                  |
| async_tree_io              | 876 ms                                                       | 699 ms: 1.25x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 597 ms: 1.12x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 418 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 578 ms: 1.10x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 394 ms: 1.05x faster                                                  |
| async_tree_none            | 354 ms                                                       | 339 ms: 1.04x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 324 ms: 1.04x faster                                                  |
| asyncio_websockets         | 520 ms                                                       | 515 ms: 1.01x faster                                                  |
| async_generators           | 377 ms                                                       | 385 ms: 1.02x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 25.1 ms: 1.06x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.08x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 180 ms: 1.20x faster                                                  |
| float          | 77.5 ms                                                      | 86.4 ms: 1.12x slower                                                 |
| nbody          | 85.1 ms                                                      | 127 ms: 1.49x slower                                                  |
| Geometric mean | (ref)                                                        | 1.11x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 22.7 ms                                                      | 20.7 ms: 1.10x faster                                                 |
| regex_effbot   | 3.08 ms                                                      | 3.03 ms: 1.02x faster                                                 |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                  |
| regex_compile  | 132 ms                                                       | 168 ms: 1.27x slower                                                  |
| Geometric mean | (ref)                                                        | 1.03x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.94 sec: 1.04x faster                                                |
| json_dumps           | 10.5 ms                                                      | 10.6 ms: 1.01x slower                                                 |
| xml_etree_parse      | 136 ms                                                       | 140 ms: 1.03x slower                                                  |
| json_loads           | 27.0 us                                                      | 30.3 us: 1.12x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 238 us: 1.13x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 341 us: 1.16x slower                                                  |
| xml_etree_generate   | 85.4 ms                                                      | 101 ms: 1.18x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 74.7 ms: 1.26x slower                                                 |
| Geometric mean       | (ref)                                                        | 1.09x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 9.29 ms: 1.26x slower                                                 |
| python_startup         | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.34x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 40.7 ms: 1.19x slower                                                 |
| mako            | 11.3 ms                                                      | 16.1 ms: 1.42x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.30x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 130 ms: 2.43x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.30 sec: 1.81x faster                                                |
| gc_traversal               | 3.14 ms                                                      | 1.77 ms: 1.77x faster                                                 |
| async_tree_io_tg           | 913 ms                                                       | 683 ms: 1.34x faster                                                  |
| deepcopy                   | 355 us                                                       | 270 us: 1.32x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 30.9 us: 1.26x faster                                                 |
| async_tree_io              | 876 ms                                                       | 699 ms: 1.25x faster                                                  |
| pidigits                   | 217 ms                                                       | 180 ms: 1.20x faster                                                  |
| go                         | 141 ms                                                       | 120 ms: 1.17x faster                                                  |
| sqlite_synth               | 2.21 us                                                      | 1.97 us: 1.12x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 597 ms: 1.12x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 418 ms: 1.10x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 578 ms: 1.10x faster                                                  |
| regex_v8                   | 22.7 ms                                                      | 20.7 ms: 1.10x faster                                                 |
| scimark_sor                | 134 ms                                                       | 124 ms: 1.08x faster                                                  |
| typing_runtime_protocols   | 155 us                                                       | 144 us: 1.07x faster                                                  |
| pathlib                    | 19.2 ms                                                      | 17.9 ms: 1.07x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.92 us: 1.07x faster                                                 |
| async_tree_memoization_tg  | 414 ms                                                       | 394 ms: 1.05x faster                                                  |
| dulwich_log                | 74.8 ms                                                      | 71.3 ms: 1.05x faster                                                 |
| async_tree_none            | 354 ms                                                       | 339 ms: 1.04x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 324 ms: 1.04x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.94 sec: 1.04x faster                                                |
| html5lib                   | 67.0 ms                                                      | 65.0 ms: 1.03x faster                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.35 sec: 1.02x faster                                                |
| regex_effbot               | 3.08 ms                                                      | 3.03 ms: 1.02x faster                                                 |
| asyncio_websockets         | 520 ms                                                       | 515 ms: 1.01x faster                                                  |
| logging_silent             | 103 ns                                                       | 103 ns: 1.01x slower                                                  |
| json_dumps                 | 10.5 ms                                                      | 10.6 ms: 1.01x slower                                                 |
| regex_dna                  | 180 ms                                                       | 182 ms: 1.01x slower                                                  |
| async_generators           | 377 ms                                                       | 385 ms: 1.02x slower                                                  |
| create_gc_cycles           | 1.34 ms                                                      | 1.37 ms: 1.03x slower                                                 |
| xml_etree_parse            | 136 ms                                                       | 140 ms: 1.03x slower                                                  |
| pyflate                    | 449 ms                                                       | 462 ms: 1.03x slower                                                  |
| pycparser                  | 1.12 sec                                                     | 1.17 sec: 1.04x slower                                                |
| coroutines                 | 23.6 ms                                                      | 25.1 ms: 1.06x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 799 ms: 1.08x slower                                                  |
| chaos                      | 57.3 ms                                                      | 62.2 ms: 1.09x slower                                                 |
| json                       | 4.93 ms                                                      | 5.37 ms: 1.09x slower                                                 |
| hexiom                     | 5.99 ms                                                      | 6.55 ms: 1.09x slower                                                 |
| comprehensions             | 16.5 us                                                      | 18.0 us: 1.10x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 21.9 ms: 1.10x slower                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.20 ms: 1.11x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.65 sec: 1.11x slower                                                |
| nqueens                    | 78.6 ms                                                      | 87.5 ms: 1.11x slower                                                 |
| float                      | 77.5 ms                                                      | 86.4 ms: 1.12x slower                                                 |
| json_loads                 | 27.0 us                                                      | 30.3 us: 1.12x slower                                                 |
| sympy_str                  | 275 ms                                                       | 310 ms: 1.13x slower                                                  |
| docutils                   | 2.62 sec                                                     | 2.96 sec: 1.13x slower                                                |
| logging_simple             | 6.16 us                                                      | 6.96 us: 1.13x slower                                                 |
| 2to3                       | 260 ms                                                       | 294 ms: 1.13x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 238 us: 1.13x slower                                                  |
| sympy_expand               | 457 ms                                                       | 521 ms: 1.14x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 128 ms: 1.14x slower                                                  |
| pickle_pure_python         | 294 us                                                       | 341 us: 1.16x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 180 ms: 1.16x slower                                                  |
| logging_format             | 6.84 us                                                      | 7.92 us: 1.16x slower                                                 |
| richards_super             | 51.6 ms                                                      | 60.0 ms: 1.16x slower                                                 |
| generators                 | 28.8 ms                                                      | 33.5 ms: 1.16x slower                                                 |
| thrift                     | 778 us                                                       | 910 us: 1.17x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 101 ms: 1.18x slower                                                  |
| raytrace                   | 253 ms                                                       | 300 ms: 1.19x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.72 ms: 1.19x slower                                                 |
| richards                   | 45.2 ms                                                      | 53.9 ms: 1.19x slower                                                 |
| django_template            | 34.1 ms                                                      | 40.7 ms: 1.19x slower                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 79.1 ms: 1.21x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 13.3 ms: 1.21x slower                                                 |
| meteor_contest             | 102 ms                                                       | 124 ms: 1.22x slower                                                  |
| fannkuch                   | 370 ms                                                       | 458 ms: 1.24x slower                                                  |
| python_startup_no_site     | 7.39 ms                                                      | 9.29 ms: 1.26x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 74.7 ms: 1.26x slower                                                 |
| regex_compile              | 132 ms                                                       | 168 ms: 1.27x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 89.9 ms: 1.32x slower                                                 |
| coverage                   | 83.0 ms                                                      | 115 ms: 1.38x slower                                                  |
| mako                       | 11.3 ms                                                      | 16.1 ms: 1.42x slower                                                 |
| python_startup             | 11.0 ms                                                      | 15.6 ms: 1.42x slower                                                 |
| nbody                      | 85.1 ms                                                      | 127 ms: 1.49x slower                                                  |
| bench_thread_pool          | 919 us                                                       | 1.49 ms: 1.62x slower                                                 |
| telco                      | 7.82 ms                                                      | 174 ms: 22.29x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.08x slower                                                          |

Benchmark hidden because not significant (3): scimark_fft, xml_etree_iterparse, spectral_norm
Ignored benchmarks (20) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260720-3.16.0a0-1f9d20b-NOGIL/bm-20260720-vultr-x86_64-python-1f9d20bbd4fed601e7ca-3.16.0a0-1f9d20b.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.069x slower

# HPT report

- Reliability score: 97.64% likely to be slow
- 90% likely to have a slowdown of 1.01x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.36x