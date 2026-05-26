# Results vs. 3.13.0rc2

- fork: python
- ref: 43c60ec2fddd316a4a6b
- machine: linux-x86_64
- commit hash: 43c60ec
- commit date: 2026-05-24
- overall geometric mean: 1.027x faster
- HPT reliability: 99.37%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.16x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.62 sec                                                     | 2.40 sec: 1.09x faster                                                |
| html5lib       | 67.0 ms                                                      | 60.2 ms: 1.11x faster                                                 |
| Geometric mean | (ref)                                                        | 1.10x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 666 ms                                                       | 542 ms: 1.23x faster                                                  |
| async_tree_io              | 876 ms                                                       | 715 ms: 1.23x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 749 ms: 1.22x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 379 ms: 1.22x faster                                                  |
| async_tree_none            | 354 ms                                                       | 294 ms: 1.21x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 553 ms: 1.15x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 365 ms: 1.14x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 296 ms: 1.14x faster                                                  |
| async_generators           | 377 ms                                                       | 343 ms: 1.10x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.03x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.14x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| float          | 77.5 ms                                                      | 75.1 ms: 1.03x faster                                                 |
| nbody          | 85.1 ms                                                      | 93.6 ms: 1.10x slower                                                 |
| Geometric mean | (ref)                                                        | 1.03x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.83 ms: 1.09x faster                                                 |
| regex_compile  | 132 ms                                                       | 125 ms: 1.06x faster                                                  |
| regex_v8       | 22.7 ms                                                      | 21.5 ms: 1.05x faster                                                 |
| regex_dna      | 180 ms                                                       | 182 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                        | 1.05x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.01 sec                                                     | 1.83 sec: 1.10x faster                                                |
| json_dumps           | 10.5 ms                                                      | 10.0 ms: 1.05x faster                                                 |
| xml_etree_iterparse  | 94.9 ms                                                      | 90.3 ms: 1.05x faster                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 87.1 ms: 1.02x slower                                                 |
| json_loads           | 27.0 us                                                      | 27.6 us: 1.02x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 215 us: 1.03x slower                                                  |
| xml_etree_process    | 59.3 ms                                                      | 61.5 ms: 1.04x slower                                                 |
| xml_etree_parse      | 136 ms                                                       | 143 ms: 1.05x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 318 us: 1.08x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.00x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.1 ms                                                      | 36.1 ms: 1.06x slower                                                 |
| mako            | 11.3 ms                                                      | 12.0 ms: 1.06x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.06x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 317 ms                                                       | 114 ms: 2.79x faster                                                  |
| mdp                        | 2.36 sec                                                     | 1.14 sec: 2.06x faster                                                |
| deepcopy                   | 355 us                                                       | 237 us: 1.50x faster                                                  |
| deepcopy_memo              | 39.1 us                                                      | 27.4 us: 1.42x faster                                                 |
| typing_runtime_protocols   | 155 us                                                       | 119 us: 1.30x faster                                                  |
| go                         | 141 ms                                                       | 108 ms: 1.30x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 542 ms: 1.23x faster                                                  |
| async_tree_io              | 876 ms                                                       | 715 ms: 1.23x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 749 ms: 1.22x faster                                                  |
| async_tree_memoization     | 461 ms                                                       | 379 ms: 1.22x faster                                                  |
| async_tree_none            | 354 ms                                                       | 294 ms: 1.21x faster                                                  |
| spectral_norm              | 111 ms                                                       | 93.1 ms: 1.19x faster                                                 |
| deepcopy_reduce            | 3.11 us                                                      | 2.62 us: 1.19x faster                                                 |
| scimark_sor                | 134 ms                                                       | 113 ms: 1.19x faster                                                  |
| pidigits                   | 217 ms                                                       | 184 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 553 ms: 1.15x faster                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 365 ms: 1.14x faster                                                  |
| async_tree_none_tg         | 336 ms                                                       | 296 ms: 1.14x faster                                                  |
| html5lib                   | 67.0 ms                                                      | 60.2 ms: 1.11x faster                                                 |
| async_generators           | 377 ms                                                       | 343 ms: 1.10x faster                                                  |
| tomli_loads                | 2.01 sec                                                     | 1.83 sec: 1.10x faster                                                |
| scimark_fft                | 349 ms                                                       | 320 ms: 1.09x faster                                                  |
| pyflate                    | 449 ms                                                       | 411 ms: 1.09x faster                                                  |
| docutils                   | 2.62 sec                                                     | 2.40 sec: 1.09x faster                                                |
| regex_effbot               | 3.08 ms                                                      | 2.83 ms: 1.09x faster                                                 |
| dulwich_log                | 74.8 ms                                                      | 69.0 ms: 1.08x faster                                                 |
| pathlib                    | 19.2 ms                                                      | 17.9 ms: 1.07x faster                                                 |
| nqueens                    | 78.6 ms                                                      | 74.0 ms: 1.06x faster                                                 |
| regex_compile              | 132 ms                                                       | 125 ms: 1.06x faster                                                  |
| bpe_tokeniser              | 4.45 sec                                                     | 4.20 sec: 1.06x faster                                                |
| regex_v8                   | 22.7 ms                                                      | 21.5 ms: 1.05x faster                                                 |
| json_dumps                 | 10.5 ms                                                      | 10.0 ms: 1.05x faster                                                 |
| generators                 | 28.8 ms                                                      | 27.4 ms: 1.05x faster                                                 |
| xml_etree_iterparse        | 94.9 ms                                                      | 90.3 ms: 1.05x faster                                                 |
| richards                   | 45.2 ms                                                      | 43.5 ms: 1.04x faster                                                 |
| logging_simple             | 6.16 us                                                      | 5.93 us: 1.04x faster                                                 |
| richards_super             | 51.6 ms                                                      | 49.7 ms: 1.04x faster                                                 |
| logging_silent             | 103 ns                                                       | 98.9 ns: 1.04x faster                                                 |
| sympy_integrate            | 19.8 ms                                                      | 19.2 ms: 1.03x faster                                                 |
| float                      | 77.5 ms                                                      | 75.1 ms: 1.03x faster                                                 |
| comprehensions             | 16.5 us                                                      | 16.0 us: 1.03x faster                                                 |
| meteor_contest             | 102 ms                                                       | 99.3 ms: 1.02x faster                                                 |
| hexiom                     | 5.99 ms                                                      | 5.87 ms: 1.02x faster                                                 |
| chaos                      | 57.3 ms                                                      | 56.3 ms: 1.02x faster                                                 |
| logging_format             | 6.84 us                                                      | 6.73 us: 1.02x faster                                                 |
| scimark_monte_carlo        | 65.4 ms                                                      | 64.6 ms: 1.01x faster                                                 |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 4.67 ms: 1.01x faster                                                 |
| sympy_sum                  | 156 ms                                                       | 156 ms: 1.01x slower                                                  |
| regex_dna                  | 180 ms                                                       | 182 ms: 1.01x slower                                                  |
| sympy_str                  | 275 ms                                                       | 277 ms: 1.01x slower                                                  |
| pprint_safe_repr           | 738 ms                                                       | 744 ms: 1.01x slower                                                  |
| coverage                   | 83.0 ms                                                      | 84.0 ms: 1.01x slower                                                 |
| pprint_pformat             | 1.50 sec                                                     | 1.51 sec: 1.01x slower                                                |
| sqlite_synth               | 2.21 us                                                      | 2.24 us: 1.02x slower                                                 |
| scimark_lu                 | 113 ms                                                       | 115 ms: 1.02x slower                                                  |
| crypto_pyaes               | 67.9 ms                                                      | 69.1 ms: 1.02x slower                                                 |
| xml_etree_generate         | 85.4 ms                                                      | 87.1 ms: 1.02x slower                                                 |
| json_loads                 | 27.0 us                                                      | 27.6 us: 1.02x slower                                                 |
| fannkuch                   | 370 ms                                                       | 378 ms: 1.02x slower                                                  |
| unpickle_pure_python       | 210 us                                                       | 215 us: 1.03x slower                                                  |
| thrift                     | 778 us                                                       | 801 us: 1.03x slower                                                  |
| coroutines                 | 23.6 ms                                                      | 24.4 ms: 1.03x slower                                                 |
| raytrace                   | 253 ms                                                       | 262 ms: 1.04x slower                                                  |
| xml_etree_process          | 59.3 ms                                                      | 61.5 ms: 1.04x slower                                                 |
| json                       | 4.93 ms                                                      | 5.15 ms: 1.04x slower                                                 |
| asyncio_websockets         | 520 ms                                                       | 545 ms: 1.05x slower                                                  |
| xml_etree_parse            | 136 ms                                                       | 143 ms: 1.05x slower                                                  |
| sympy_expand               | 457 ms                                                       | 479 ms: 1.05x slower                                                  |
| django_template            | 34.1 ms                                                      | 36.1 ms: 1.06x slower                                                 |
| mako                       | 11.3 ms                                                      | 12.0 ms: 1.06x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.18 sec: 1.06x slower                                                |
| pickle_pure_python         | 294 us                                                       | 318 us: 1.08x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 3.39 ms: 1.08x slower                                                 |
| nbody                      | 85.1 ms                                                      | 93.6 ms: 1.10x slower                                                 |
| gc_traversal               | 3.14 ms                                                      | 3.84 ms: 1.22x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.81 ms: 1.36x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 1.33 ms: 1.45x slower                                                 |
| telco                      | 7.82 ms                                                      | 161 ms: 20.55x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 246 ms: 22.42x slower                                                 |
| Geometric mean             | (ref)                                                        | 1.02x slower                                                          |
Ignored benchmarks (23) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260524-3.16.0a0-43c60ec/bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.027x faster

# HPT report

- Reliability score: 99.37% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.16x