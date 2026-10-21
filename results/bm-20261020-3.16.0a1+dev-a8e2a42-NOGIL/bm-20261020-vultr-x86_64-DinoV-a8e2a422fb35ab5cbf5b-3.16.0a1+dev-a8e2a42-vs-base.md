# Results vs. base

- fork: DinoV
- ref: a8e2a422fb35ab5cbf5b
- machine: linux-x86_64
- commit hash: a8e2a42
- commit date: 2026-10-20
- overall geometric mean: 1.002x slower
- HPT reliability: 94.81%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.03x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20261020-vultr-x86_64-python-f5bd07700ecd0f02cc42-3.16.0a1+dev-f5bd077 | bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1+dev-a8e2a42 |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 291 ms                                                                    | 294 ms: 1.01x slower                                                     |
| docutils       | 2.90 sec                                                                  | 2.92 sec: 1.01x slower                                                   |
| html5lib       | 65.0 ms                                                                   | 65.4 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                     | 1.01x slower                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20261020-vultr-x86_64-python-f5bd07700ecd0f02cc42-3.16.0a1+dev-f5bd077 | bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1+dev-a8e2a42 |
|----------------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_memoization     | 429 ms                                                                    | 416 ms: 1.03x faster                                                     |
| async_tree_none            | 344 ms                                                                    | 339 ms: 1.02x faster                                                     |
| asyncio_websockets         | 509 ms                                                                    | 502 ms: 1.01x faster                                                     |
| coroutines                 | 25.8 ms                                                                   | 25.7 ms: 1.01x faster                                                    |
| async_generators           | 419 ms                                                                    | 416 ms: 1.01x faster                                                     |
| async_tree_io              | 719 ms                                                                    | 716 ms: 1.00x faster                                                     |
| async_tree_cpu_io_mixed_tg | 580 ms                                                                    | 585 ms: 1.01x slower                                                     |
| async_tree_none_tg         | 334 ms                                                                    | 341 ms: 1.02x slower                                                     |
| async_tree_io_tg           | 707 ms                                                                    | 724 ms: 1.02x slower                                                     |
| Geometric mean             | (ref)                                                                     | 1.00x faster                                                             |

Benchmark hidden because not significant (2): async_tree_memoization_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20261020-vultr-x86_64-python-f5bd07700ecd0f02cc42-3.16.0a1+dev-f5bd077 | bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1+dev-a8e2a42 |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 187 ms                                                                    | 188 ms: 1.01x slower                                                     |
| float          | 83.8 ms                                                                   | 84.9 ms: 1.01x slower                                                    |
| nbody          | 115 ms                                                                    | 118 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                     | 1.01x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20261020-vultr-x86_64-python-f5bd07700ecd0f02cc42-3.16.0a1+dev-f5bd077 | bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1+dev-a8e2a42 |
|----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 21.4 ms                                                                   | 20.8 ms: 1.03x faster                                                    |
| regex_effbot   | 2.96 ms                                                                   | 2.90 ms: 1.02x faster                                                    |
| regex_dna      | 185 ms                                                                    | 184 ms: 1.01x faster                                                     |
| Geometric mean | (ref)                                                                     | 1.01x faster                                                             |

Benchmark hidden because not significant (1): regex_compile

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20261020-vultr-x86_64-python-f5bd07700ecd0f02cc42-3.16.0a1+dev-f5bd077 | bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1+dev-a8e2a42 |
|----------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 30.3 us                                                                   | 30.2 us: 1.01x faster                                                    |
| unpickle_pure_python | 238 us                                                                    | 239 us: 1.00x slower                                                     |
| tomli_loads          | 1.94 sec                                                                  | 1.95 sec: 1.00x slower                                                   |
| xml_etree_iterparse  | 95.9 ms                                                                   | 96.7 ms: 1.01x slower                                                    |
| xml_etree_generate   | 101 ms                                                                    | 103 ms: 1.02x slower                                                     |
| xml_etree_process    | 75.5 ms                                                                   | 76.8 ms: 1.02x slower                                                    |
| json_dumps           | 10.0 ms                                                                   | 10.2 ms: 1.02x slower                                                    |
| xml_etree_parse      | 141 ms                                                                    | 145 ms: 1.02x slower                                                     |
| Geometric mean       | (ref)                                                                     | 1.01x slower                                                             |

Benchmark hidden because not significant (1): pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20261020-vultr-x86_64-python-f5bd07700ecd0f02cc42-3.16.0a1+dev-f5bd077 | bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1+dev-a8e2a42 |
|------------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.5 ms                                                                   | 14.5 ms: 1.00x slower                                                    |
| python_startup_no_site | 9.57 ms                                                                   | 9.70 ms: 1.01x slower                                                    |
| Geometric mean         | (ref)                                                                     | 1.01x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20261020-vultr-x86_64-python-f5bd07700ecd0f02cc42-3.16.0a1+dev-f5bd077 | bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1+dev-a8e2a42 |
|-----------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 41.8 ms                                                                   | 42.0 ms: 1.01x slower                                                    |
| mako            | 15.8 ms                                                                   | 16.0 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                                     | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20261020-vultr-x86_64-python-f5bd07700ecd0f02cc42-3.16.0a1+dev-f5bd077 | bm-20261020-vultr-x86_64-DinoV-a8e2a422fb35ab5cbf5b-3.16.0a1+dev-a8e2a42 |
|----------------------------|:-------------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| bench_thread_pool          | 1.63 ms                                                                   | 1.36 ms: 1.20x faster                                                    |
| spectral_norm              | 105 ms                                                                    | 100 ms: 1.05x faster                                                     |
| scimark_sparse_mat_mult    | 5.19 ms                                                                   | 5.01 ms: 1.04x faster                                                    |
| async_tree_memoization     | 429 ms                                                                    | 416 ms: 1.03x faster                                                     |
| regex_v8                   | 21.4 ms                                                                   | 20.8 ms: 1.03x faster                                                    |
| logging_format             | 8.19 us                                                                   | 8.00 us: 1.02x faster                                                    |
| fannkuch                   | 470 ms                                                                    | 460 ms: 1.02x faster                                                     |
| logging_silent             | 108 ns                                                                    | 106 ns: 1.02x faster                                                     |
| coverage                   | 119 ms                                                                    | 117 ms: 1.02x faster                                                     |
| regex_effbot               | 2.96 ms                                                                   | 2.90 ms: 1.02x faster                                                    |
| scimark_sor                | 121 ms                                                                    | 119 ms: 1.02x faster                                                     |
| deltablue                  | 3.76 ms                                                                   | 3.70 ms: 1.02x faster                                                    |
| async_tree_none            | 344 ms                                                                    | 339 ms: 1.02x faster                                                     |
| mdp                        | 1.32 sec                                                                  | 1.30 sec: 1.01x faster                                                   |
| asyncio_websockets         | 509 ms                                                                    | 502 ms: 1.01x faster                                                     |
| pprint_pformat             | 1.69 sec                                                                  | 1.68 sec: 1.01x faster                                                   |
| scimark_fft                | 327 ms                                                                    | 324 ms: 1.01x faster                                                     |
| scimark_lu                 | 131 ms                                                                    | 130 ms: 1.01x faster                                                     |
| richards_super             | 60.9 ms                                                                   | 60.3 ms: 1.01x faster                                                    |
| json                       | 5.41 ms                                                                   | 5.37 ms: 1.01x faster                                                    |
| regex_dna                  | 185 ms                                                                    | 184 ms: 1.01x faster                                                     |
| coroutines                 | 25.8 ms                                                                   | 25.7 ms: 1.01x faster                                                    |
| deepcopy_memo              | 32.9 us                                                                   | 32.7 us: 1.01x faster                                                    |
| richards                   | 53.2 ms                                                                   | 52.9 ms: 1.01x faster                                                    |
| async_generators           | 419 ms                                                                    | 416 ms: 1.01x faster                                                     |
| json_loads                 | 30.3 us                                                                   | 30.2 us: 1.01x faster                                                    |
| async_tree_io              | 719 ms                                                                    | 716 ms: 1.00x faster                                                     |
| python_startup             | 14.5 ms                                                                   | 14.5 ms: 1.00x slower                                                    |
| unpickle_pure_python       | 238 us                                                                    | 239 us: 1.00x slower                                                     |
| comprehensions             | 18.2 us                                                                   | 18.3 us: 1.00x slower                                                    |
| scimark_monte_carlo        | 76.1 ms                                                                   | 76.4 ms: 1.00x slower                                                    |
| tomli_loads                | 1.94 sec                                                                  | 1.95 sec: 1.00x slower                                                   |
| pidigits                   | 187 ms                                                                    | 188 ms: 1.01x slower                                                     |
| meteor_contest             | 124 ms                                                                    | 125 ms: 1.01x slower                                                     |
| deepcopy                   | 267 us                                                                    | 269 us: 1.01x slower                                                     |
| deepcopy_reduce            | 2.94 us                                                                   | 2.96 us: 1.01x slower                                                    |
| html5lib                   | 65.0 ms                                                                   | 65.4 ms: 1.01x slower                                                    |
| nqueens                    | 87.3 ms                                                                   | 87.9 ms: 1.01x slower                                                    |
| django_template            | 41.8 ms                                                                   | 42.0 ms: 1.01x slower                                                    |
| sqlglot_v2_normalize       | 113 ms                                                                    | 114 ms: 1.01x slower                                                     |
| 2to3                       | 291 ms                                                                    | 294 ms: 1.01x slower                                                     |
| docutils                   | 2.90 sec                                                                  | 2.92 sec: 1.01x slower                                                   |
| k_core                     | 2.25 sec                                                                  | 2.27 sec: 1.01x slower                                                   |
| xml_etree_iterparse        | 95.9 ms                                                                   | 96.7 ms: 1.01x slower                                                    |
| chaos                      | 59.6 ms                                                                   | 60.1 ms: 1.01x slower                                                    |
| pyflate                    | 444 ms                                                                    | 448 ms: 1.01x slower                                                     |
| async_tree_cpu_io_mixed_tg | 580 ms                                                                    | 585 ms: 1.01x slower                                                     |
| mako                       | 15.8 ms                                                                   | 16.0 ms: 1.01x slower                                                    |
| float                      | 83.8 ms                                                                   | 84.9 ms: 1.01x slower                                                    |
| crypto_pyaes               | 87.4 ms                                                                   | 88.6 ms: 1.01x slower                                                    |
| python_startup_no_site     | 9.57 ms                                                                   | 9.70 ms: 1.01x slower                                                    |
| connected_components       | 486 ms                                                                    | 493 ms: 1.01x slower                                                     |
| xml_etree_generate         | 101 ms                                                                    | 103 ms: 1.02x slower                                                     |
| xml_etree_process          | 75.5 ms                                                                   | 76.8 ms: 1.02x slower                                                    |
| json_dumps                 | 10.0 ms                                                                   | 10.2 ms: 1.02x slower                                                    |
| async_tree_none_tg         | 334 ms                                                                    | 341 ms: 1.02x slower                                                     |
| xml_etree_parse            | 141 ms                                                                    | 145 ms: 1.02x slower                                                     |
| nbody                      | 115 ms                                                                    | 118 ms: 1.02x slower                                                     |
| async_tree_io_tg           | 707 ms                                                                    | 724 ms: 1.02x slower                                                     |
| create_gc_cycles           | 1.32 ms                                                                   | 1.35 ms: 1.02x slower                                                    |
| dulwich_log                | 70.3 ms                                                                   | 72.3 ms: 1.03x slower                                                    |
| gc_traversal               | 1.77 ms                                                                   | 1.84 ms: 1.04x slower                                                    |
| pycparser                  | 1.13 sec                                                                  | 1.18 sec: 1.05x slower                                                   |
| generators                 | 33.1 ms                                                                   | 34.8 ms: 1.05x slower                                                    |
| bench_mp_pool              | 6.70 ms                                                                   | 7.17 ms: 1.07x slower                                                    |
| Geometric mean             | (ref)                                                                     | 1.00x slower                                                             |

Benchmark hidden because not significant (27): typing_runtime_protocols, sqlglot_v2_transpile, hexiom, async_tree_memoization_tg, logging_simple, thrift, pathlib, regex_compile, sqlite_synth, telco, raytrace, sqlglot_v2_parse, sympy_str, shortest_path, sympy_integrate, bpe_tokeniser, pickle_pure_python, pprint_safe_repr, many_optionals, go, sympy_expand, subparsers, sympy_sum, sphinx, async_tree_cpu_io_mixed, sqlglot_v2_optimize, pylint

- Geometric mean (including insignificant results): 1.002x slower

# HPT report

- Reliability score: 94.81% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.03x