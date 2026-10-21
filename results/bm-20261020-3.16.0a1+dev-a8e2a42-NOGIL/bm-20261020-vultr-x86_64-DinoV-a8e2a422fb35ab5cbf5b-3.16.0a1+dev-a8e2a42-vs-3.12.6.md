# Results vs. 3.12.6

- fork: DinoV
- ref: a8e2a422fb35ab5cbf5b
- machine: linux-x86_64
- commit hash: a8e2a42
- commit date: 2026-10-20
- overall geometric mean: 1.040x slower
- HPT reliability: 87.86%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.39x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1+dev-a8e2a42 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 294 ms: 1.11x slower                                                     |
| docutils       | 2.64 sec                                               | 2.92 sec: 1.11x slower                                                   |
| html5lib       | 63.6 ms                                                | 65.4 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                  | 1.08x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1+dev-a8e2a42 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 724 ms: 1.53x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 716 ms: 1.51x faster                                                     |
| async_tree_memoization_tg  | 560 ms                                                 | 402 ms: 1.39x faster                                                     |
| async_tree_none            | 464 ms                                                 | 339 ms: 1.37x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 416 ms: 1.33x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 341 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 585 ms: 1.23x faster                                                     |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 601 ms: 1.19x faster                                                     |
| asyncio_websockets         | 517 ms                                                 | 502 ms: 1.03x faster                                                     |
| coroutines                 | 23.9 ms                                                | 25.7 ms: 1.07x slower                                                    |
| async_generators           | 384 ms                                                 | 416 ms: 1.08x slower                                                     |
| Geometric mean             | (ref)                                                  | 1.23x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1+dev-a8e2a42 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 188 ms: 1.02x slower                                                     |
| float          | 80.8 ms                                                | 84.9 ms: 1.05x slower                                                    |
| nbody          | 89.3 ms                                                | 118 ms: 1.32x slower                                                     |
| Geometric mean | (ref)                                                  | 1.12x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1+dev-a8e2a42 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.90 ms: 1.09x faster                                                    |
| regex_v8       | 20.6 ms                                                | 20.8 ms: 1.01x slower                                                    |
| regex_dna      | 168 ms                                                 | 184 ms: 1.10x slower                                                     |
| regex_compile  | 142 ms                                                 | 170 ms: 1.19x slower                                                     |
| Geometric mean | (ref)                                                  | 1.05x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1+dev-a8e2a42 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.95 sec: 1.08x faster                                                   |
| json_dumps           | 10.4 ms                                                | 10.2 ms: 1.02x faster                                                    |
| xml_etree_parse      | 139 ms                                                 | 145 ms: 1.04x slower                                                     |
| unpickle_pure_python | 221 us                                                 | 239 us: 1.08x slower                                                     |
| pickle_pure_python   | 308 us                                                 | 334 us: 1.09x slower                                                     |
| json_loads           | 26.5 us                                                | 30.2 us: 1.14x slower                                                    |
| xml_etree_generate   | 85.2 ms                                                | 103 ms: 1.21x slower                                                     |
| xml_etree_process    | 59.0 ms                                                | 76.8 ms: 1.30x slower                                                    |
| Geometric mean       | (ref)                                                  | 1.08x slower                                                             |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1+dev-a8e2a42 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 9.70 ms: 1.36x slower                                                    |
| python_startup         | 9.93 ms                                                | 14.5 ms: 1.46x slower                                                    |
| Geometric mean         | (ref)                                                  | 1.41x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1+dev-a8e2a42 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 34.7 ms                                                | 42.0 ms: 1.21x slower                                                    |
| mako            | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                    |
| Geometric mean  | (ref)                                                  | 1.33x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1+dev-a8e2a42 |
|----------------------------|:------------------------------------------------------:|:------------------------------------------------------------------------:|
| pylint                     | 319 ms                                                 | 133 ms: 2.40x faster                                                     |
| gc_traversal               | 3.46 ms                                                | 1.84 ms: 1.88x faster                                                    |
| mdp                        | 2.42 sec                                               | 1.30 sec: 1.86x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 724 ms: 1.53x faster                                                     |
| async_tree_io              | 1.08 sec                                               | 716 ms: 1.51x faster                                                     |
| bench_mp_pool              | 10.8 ms                                                | 7.17 ms: 1.51x faster                                                    |
| async_tree_memoization_tg  | 560 ms                                                 | 402 ms: 1.39x faster                                                     |
| async_tree_none            | 464 ms                                                 | 339 ms: 1.37x faster                                                     |
| async_tree_memoization     | 555 ms                                                 | 416 ms: 1.33x faster                                                     |
| deepcopy                   | 352 us                                                 | 269 us: 1.31x faster                                                     |
| async_tree_none_tg         | 446 ms                                                 | 341 ms: 1.31x faster                                                     |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 585 ms: 1.23x faster                                                     |
| deepcopy_memo              | 40.3 us                                                | 32.7 us: 1.23x faster                                                    |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 601 ms: 1.19x faster                                                     |
| pathlib                    | 21.5 ms                                                | 18.1 ms: 1.19x faster                                                    |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                     |
| sqlite_synth               | 2.20 us                                                | 1.94 us: 1.13x faster                                                    |
| typing_runtime_protocols   | 163 us                                                 | 146 us: 1.12x faster                                                     |
| spectral_norm              | 110 ms                                                 | 100 ms: 1.10x faster                                                     |
| scimark_sor                | 130 ms                                                 | 119 ms: 1.09x faster                                                     |
| dulwich_log                | 78.9 ms                                                | 72.3 ms: 1.09x faster                                                    |
| regex_effbot               | 3.17 ms                                                | 2.90 ms: 1.09x faster                                                    |
| comprehensions             | 19.8 us                                                | 18.3 us: 1.09x faster                                                    |
| tomli_loads                | 2.11 sec                                               | 1.95 sec: 1.08x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.42 sec: 1.07x faster                                                   |
| scimark_fft                | 342 ms                                                 | 324 ms: 1.06x faster                                                     |
| chaos                      | 62.8 ms                                                | 60.1 ms: 1.05x faster                                                    |
| deepcopy_reduce            | 3.08 us                                                | 2.96 us: 1.04x faster                                                    |
| asyncio_websockets         | 517 ms                                                 | 502 ms: 1.03x faster                                                     |
| logging_silent             | 109 ns                                                 | 106 ns: 1.03x faster                                                     |
| raytrace                   | 299 ms                                                 | 293 ms: 1.02x faster                                                     |
| json_dumps                 | 10.4 ms                                                | 10.2 ms: 1.02x faster                                                    |
| regex_v8                   | 20.6 ms                                                | 20.8 ms: 1.01x slower                                                    |
| pycparser                  | 1.17 sec                                               | 1.18 sec: 1.01x slower                                                   |
| pidigits                   | 184 ms                                                 | 188 ms: 1.02x slower                                                     |
| html5lib                   | 63.6 ms                                                | 65.4 ms: 1.03x slower                                                    |
| xml_etree_parse            | 139 ms                                                 | 145 ms: 1.04x slower                                                     |
| float                      | 80.8 ms                                                | 84.9 ms: 1.05x slower                                                    |
| json                       | 5.02 ms                                                | 5.37 ms: 1.07x slower                                                    |
| sympy_integrate            | 20.5 ms                                                | 22.0 ms: 1.07x slower                                                    |
| coroutines                 | 23.9 ms                                                | 25.7 ms: 1.07x slower                                                    |
| deltablue                  | 3.45 ms                                                | 3.70 ms: 1.07x slower                                                    |
| hexiom                     | 6.17 ms                                                | 6.62 ms: 1.07x slower                                                    |
| generators                 | 32.2 ms                                                | 34.8 ms: 1.08x slower                                                    |
| logging_simple             | 6.63 us                                                | 7.15 us: 1.08x slower                                                    |
| unpickle_pure_python       | 221 us                                                 | 239 us: 1.08x slower                                                     |
| async_generators           | 384 ms                                                 | 416 ms: 1.08x slower                                                     |
| pickle_pure_python         | 308 us                                                 | 334 us: 1.09x slower                                                     |
| logging_format             | 7.35 us                                                | 8.00 us: 1.09x slower                                                    |
| sympy_str                  | 292 ms                                                 | 319 ms: 1.09x slower                                                     |
| regex_dna                  | 168 ms                                                 | 184 ms: 1.10x slower                                                     |
| nqueens                    | 80.1 ms                                                | 87.9 ms: 1.10x slower                                                    |
| sympy_sum                  | 166 ms                                                 | 182 ms: 1.10x slower                                                     |
| pprint_safe_repr           | 743 ms                                                 | 818 ms: 1.10x slower                                                     |
| pprint_pformat             | 1.52 sec                                               | 1.68 sec: 1.10x slower                                                   |
| docutils                   | 2.64 sec                                               | 2.92 sec: 1.11x slower                                                   |
| 2to3                       | 264 ms                                                 | 294 ms: 1.11x slower                                                     |
| scimark_monte_carlo        | 68.4 ms                                                | 76.4 ms: 1.12x slower                                                    |
| scimark_lu                 | 114 ms                                                 | 130 ms: 1.14x slower                                                     |
| json_loads                 | 26.5 us                                                | 30.2 us: 1.14x slower                                                    |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 5.01 ms: 1.14x slower                                                    |
| sympy_expand               | 468 ms                                                 | 536 ms: 1.15x slower                                                     |
| richards                   | 45.9 ms                                                | 52.9 ms: 1.15x slower                                                    |
| crypto_pyaes               | 76.6 ms                                                | 88.6 ms: 1.16x slower                                                    |
| thrift                     | 791 us                                                 | 916 us: 1.16x slower                                                     |
| richards_super             | 51.9 ms                                                | 60.3 ms: 1.16x slower                                                    |
| regex_compile              | 142 ms                                                 | 170 ms: 1.19x slower                                                     |
| xml_etree_generate         | 85.2 ms                                                | 103 ms: 1.21x slower                                                     |
| meteor_contest             | 104 ms                                                 | 125 ms: 1.21x slower                                                     |
| django_template            | 34.7 ms                                                | 42.0 ms: 1.21x slower                                                    |
| create_gc_cycles           | 1.09 ms                                                | 1.35 ms: 1.23x slower                                                    |
| fannkuch                   | 372 ms                                                 | 460 ms: 1.24x slower                                                     |
| xml_etree_process          | 59.0 ms                                                | 76.8 ms: 1.30x slower                                                    |
| nbody                      | 89.3 ms                                                | 118 ms: 1.32x slower                                                     |
| python_startup_no_site     | 7.16 ms                                                | 9.70 ms: 1.36x slower                                                    |
| bench_thread_pool          | 941 us                                                 | 1.36 ms: 1.44x slower                                                    |
| mako                       | 11.0 ms                                                | 16.0 ms: 1.45x slower                                                    |
| python_startup             | 9.93 ms                                                | 14.5 ms: 1.46x slower                                                    |
| coverage                   | 71.4 ms                                                | 117 ms: 1.63x slower                                                     |
| telco                      | 6.53 ms                                                | 175 ms: 26.80x slower                                                    |
| Geometric mean             | (ref)                                                  | 1.04x slower                                                             |

Benchmark hidden because not significant (2): xml_etree_iterparse, pyflate
Ignored benchmarks (23) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, genshi_text, genshi_xml, gunicorn, mypy2, pickle, pickle_dict, pickle_list, sqlalchemy_declarative, sqlalchemy_imperative, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20261020-3.16.0a1+dev-a8e2a42-NOGIL/bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1+dev-a8e2a42.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.040x slower

# HPT report

- Reliability score: 87.86% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.39x