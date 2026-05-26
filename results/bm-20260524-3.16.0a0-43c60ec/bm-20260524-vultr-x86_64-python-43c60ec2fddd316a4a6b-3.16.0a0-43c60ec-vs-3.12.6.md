# Results vs. 3.12.6

- fork: python
- ref: 43c60ec2fddd316a4a6b
- machine: linux-x86_64
- commit hash: 43c60ec
- commit date: 2026-05-24
- overall geometric mean: 1.065x faster
- HPT reliability: 99.99%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| docutils       | 2.64 sec                                               | 2.40 sec: 1.10x faster                                                |
| html5lib       | 63.6 ms                                                | 60.2 ms: 1.06x faster                                                 |
| Geometric mean | (ref)                                                  | 1.08x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none            | 464 ms                                                 | 294 ms: 1.58x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 365 ms: 1.53x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 715 ms: 1.52x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 296 ms: 1.51x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 749 ms: 1.48x faster                                                  |
| async_tree_memoization     | 555 ms                                                 | 379 ms: 1.47x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 542 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 553 ms: 1.31x faster                                                  |
| async_generators           | 384 ms                                                 | 343 ms: 1.12x faster                                                  |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                 |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.32x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 75.1 ms: 1.08x faster                                                 |
| nbody          | 89.3 ms                                                | 93.6 ms: 1.05x slower                                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 125 ms: 1.14x faster                                                  |
| regex_effbot   | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                 |
| regex_v8       | 20.6 ms                                                | 21.5 ms: 1.05x slower                                                 |
| regex_dna      | 168 ms                                                 | 182 ms: 1.08x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.83 sec: 1.15x faster                                                |
| xml_etree_iterparse  | 96.7 ms                                                | 90.3 ms: 1.07x faster                                                 |
| json_dumps           | 10.4 ms                                                | 10.0 ms: 1.03x faster                                                 |
| unpickle_pure_python | 221 us                                                 | 215 us: 1.02x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 87.1 ms: 1.02x slower                                                 |
| xml_etree_parse      | 139 ms                                                 | 143 ms: 1.03x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 318 us: 1.03x slower                                                  |
| json_loads           | 26.5 us                                                | 27.6 us: 1.04x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 61.5 ms: 1.04x slower                                                 |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 36.1 ms: 1.04x slower                                                 |
| mako            | 11.0 ms                                                | 12.0 ms: 1.09x slower                                                 |
| Geometric mean  | (ref)                                                  | 1.06x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 114 ms: 2.80x faster                                                  |
| mdp                        | 2.42 sec                                               | 1.14 sec: 2.12x faster                                                |
| async_tree_none            | 464 ms                                                 | 294 ms: 1.58x faster                                                  |
| async_tree_memoization_tg  | 560 ms                                                 | 365 ms: 1.53x faster                                                  |
| async_tree_io              | 1.08 sec                                               | 715 ms: 1.52x faster                                                  |
| async_tree_none_tg         | 446 ms                                                 | 296 ms: 1.51x faster                                                  |
| deepcopy                   | 352 us                                                 | 237 us: 1.49x faster                                                  |
| async_tree_io_tg           | 1.11 sec                                               | 749 ms: 1.48x faster                                                  |
| deepcopy_memo              | 40.3 us                                                | 27.4 us: 1.47x faster                                                 |
| async_tree_memoization     | 555 ms                                                 | 379 ms: 1.47x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 119 us: 1.37x faster                                                  |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 542 ms: 1.32x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 553 ms: 1.31x faster                                                  |
| go                         | 139 ms                                                 | 108 ms: 1.28x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.0 us: 1.24x faster                                                 |
| pathlib                    | 21.5 ms                                                | 17.9 ms: 1.21x faster                                                 |
| spectral_norm              | 110 ms                                                 | 93.1 ms: 1.18x faster                                                 |
| generators                 | 32.2 ms                                                | 27.4 ms: 1.18x faster                                                 |
| deepcopy_reduce            | 3.08 us                                                | 2.62 us: 1.17x faster                                                 |
| tomli_loads                | 2.11 sec                                               | 1.83 sec: 1.15x faster                                                |
| scimark_sor                | 130 ms                                                 | 113 ms: 1.15x faster                                                  |
| dulwich_log                | 78.9 ms                                                | 69.0 ms: 1.14x faster                                                 |
| raytrace                   | 299 ms                                                 | 262 ms: 1.14x faster                                                  |
| regex_compile              | 142 ms                                                 | 125 ms: 1.14x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.20 sec: 1.13x faster                                                |
| async_generators           | 384 ms                                                 | 343 ms: 1.12x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.83 ms: 1.12x faster                                                 |
| logging_simple             | 6.63 us                                                | 5.93 us: 1.12x faster                                                 |
| chaos                      | 62.8 ms                                                | 56.3 ms: 1.12x faster                                                 |
| crypto_pyaes               | 76.6 ms                                                | 69.1 ms: 1.11x faster                                                 |
| logging_silent             | 109 ns                                                 | 98.9 ns: 1.10x faster                                                 |
| docutils                   | 2.64 sec                                               | 2.40 sec: 1.10x faster                                                |
| logging_format             | 7.35 us                                                | 6.73 us: 1.09x faster                                                 |
| pyflate                    | 448 ms                                                 | 411 ms: 1.09x faster                                                  |
| nqueens                    | 80.1 ms                                                | 74.0 ms: 1.08x faster                                                 |
| float                      | 80.8 ms                                                | 75.1 ms: 1.08x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 90.3 ms: 1.07x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.2 ms: 1.07x faster                                                 |
| scimark_fft                | 342 ms                                                 | 320 ms: 1.07x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 156 ms: 1.06x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 64.6 ms: 1.06x faster                                                 |
| html5lib                   | 63.6 ms                                                | 60.2 ms: 1.06x faster                                                 |
| richards                   | 45.9 ms                                                | 43.5 ms: 1.06x faster                                                 |
| sympy_str                  | 292 ms                                                 | 277 ms: 1.05x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.87 ms: 1.05x faster                                                 |
| richards_super             | 51.9 ms                                                | 49.7 ms: 1.04x faster                                                 |
| meteor_contest             | 104 ms                                                 | 99.3 ms: 1.04x faster                                                 |
| json_dumps                 | 10.4 ms                                                | 10.0 ms: 1.03x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 215 us: 1.02x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.39 ms: 1.02x faster                                                 |
| scimark_lu                 | 114 ms                                                 | 115 ms: 1.00x slower                                                  |
| thrift                     | 791 us                                                 | 801 us: 1.01x slower                                                  |
| pycparser                  | 1.17 sec                                               | 1.18 sec: 1.01x slower                                                |
| fannkuch                   | 372 ms                                                 | 378 ms: 1.02x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.24 us: 1.02x slower                                                 |
| coroutines                 | 23.9 ms                                                | 24.4 ms: 1.02x slower                                                 |
| xml_etree_generate         | 85.2 ms                                                | 87.1 ms: 1.02x slower                                                 |
| json                       | 5.02 ms                                                | 5.15 ms: 1.02x slower                                                 |
| sympy_expand               | 468 ms                                                 | 479 ms: 1.02x slower                                                  |
| xml_etree_parse            | 139 ms                                                 | 143 ms: 1.03x slower                                                  |
| pickle_pure_python         | 308 us                                                 | 318 us: 1.03x slower                                                  |
| django_template            | 34.7 ms                                                | 36.1 ms: 1.04x slower                                                 |
| json_loads                 | 26.5 us                                                | 27.6 us: 1.04x slower                                                 |
| xml_etree_process          | 59.0 ms                                                | 61.5 ms: 1.04x slower                                                 |
| regex_v8                   | 20.6 ms                                                | 21.5 ms: 1.05x slower                                                 |
| nbody                      | 89.3 ms                                                | 93.6 ms: 1.05x slower                                                 |
| asyncio_websockets         | 517 ms                                                 | 545 ms: 1.05x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.67 ms: 1.06x slower                                                 |
| regex_dna                  | 168 ms                                                 | 182 ms: 1.08x slower                                                  |
| mako                       | 11.0 ms                                                | 12.0 ms: 1.09x slower                                                 |
| gc_traversal               | 3.46 ms                                                | 3.84 ms: 1.11x slower                                                 |
| coverage                   | 71.4 ms                                                | 84.0 ms: 1.18x slower                                                 |
| bench_thread_pool          | 941 us                                                 | 1.33 ms: 1.42x slower                                                 |
| create_gc_cycles           | 1.09 ms                                                | 1.81 ms: 1.66x slower                                                 |
| bench_mp_pool              | 10.8 ms                                                | 246 ms: 22.82x slower                                                 |
| telco                      | 6.53 ms                                                | 161 ms: 24.64x slower                                                 |
| Geometric mean             | (ref)                                                  | 1.02x faster                                                          |

Benchmark hidden because not significant (3): pprint_pformat, pidigits, pprint_safe_repr
Ignored benchmarks (26) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: 2to3, aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, python_startup, python_startup_no_site, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20260524-3.16.0a0-43c60ec/bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.065x faster

# HPT report

- Reliability score: 99.99% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.18x