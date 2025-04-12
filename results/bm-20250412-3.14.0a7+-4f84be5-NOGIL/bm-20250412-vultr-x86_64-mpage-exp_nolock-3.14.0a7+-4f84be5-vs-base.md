# Results vs. base

- fork: mpage
- ref: exp_nolock
- machine: linux-x86_64
- commit hash: 4f84be5
- commit date: 2025-04-12
- overall geometric mean: 1.007x slower
- HPT reliability: 99.67%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250412-vultr-x86_64-python-9634085af3670b1eb654-3.14.0a7+-9634085 | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| 2to3           | 280 ms                                                                 | 280 ms: 1.00x faster                                        |
| html5lib       | 65.3 ms                                                                | 64.7 ms: 1.01x faster                                       |
| sphinx         | 1.06 sec                                                               | 1.06 sec: 1.00x slower                                      |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                |

Benchmark hidden because not significant (1): docutils

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250412-vultr-x86_64-python-9634085af3670b1eb654-3.14.0a7+-9634085 | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| async_generators           | 363 ms                                                                 | 361 ms: 1.00x faster                                        |
| async_tree_io              | 543 ms                                                                 | 547 ms: 1.01x slower                                        |
| coroutines                 | 22.8 ms                                                                | 23.1 ms: 1.01x slower                                       |
| async_tree_cpu_io_mixed    | 500 ms                                                                 | 550 ms: 1.10x slower                                        |
| async_tree_cpu_io_mixed_tg | 474 ms                                                                 | 523 ms: 1.10x slower                                        |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                |

Benchmark hidden because not significant (6): async_tree_memoization_tg, asyncio_websockets, async_tree_none_tg, async_tree_memoization, async_tree_none, async_tree_io_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250412-vultr-x86_64-python-9634085af3670b1eb654-3.14.0a7+-9634085 | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| pidigits       | 219 ms                                                                 | 203 ms: 1.08x faster                                        |
| float          | 67.2 ms                                                                | 67.5 ms: 1.01x slower                                       |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250412-vultr-x86_64-python-9634085af3670b1eb654-3.14.0a7+-9634085 | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| regex_v8       | 21.3 ms                                                                | 21.1 ms: 1.01x faster                                       |
| regex_compile  | 143 ms                                                                 | 143 ms: 1.01x slower                                        |
| regex_effbot   | 2.74 ms                                                                | 2.80 ms: 1.02x slower                                       |
| regex_dna      | 175 ms                                                                 | 184 ms: 1.05x slower                                        |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250412-vultr-x86_64-python-9634085af3670b1eb654-3.14.0a7+-9634085 | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| json_loads           | 30.9 us                                                                | 30.6 us: 1.01x faster                                       |
| xml_etree_generate   | 93.1 ms                                                                | 93.0 ms: 1.00x faster                                       |
| xml_etree_process    | 66.1 ms                                                                | 66.4 ms: 1.00x slower                                       |
| xml_etree_iterparse  | 86.3 ms                                                                | 87.0 ms: 1.01x slower                                       |
| json_dumps           | 12.6 ms                                                                | 12.7 ms: 1.01x slower                                       |
| pickle_pure_python   | 325 us                                                                 | 329 us: 1.01x slower                                        |
| tomli_loads          | 2.06 sec                                                               | 2.10 sec: 1.02x slower                                      |
| unpickle_pure_python | 224 us                                                                 | 229 us: 1.02x slower                                        |
| Geometric mean       | (ref)                                                                  | 1.01x slower                                                |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250412-vultr-x86_64-python-9634085af3670b1eb654-3.14.0a7+-9634085 | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| python_startup         | 15.9 ms                                                                | 15.8 ms: 1.00x faster                                       |
| python_startup_no_site | 11.2 ms                                                                | 11.1 ms: 1.00x faster                                       |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250412-vultr-x86_64-python-9634085af3670b1eb654-3.14.0a7+-9634085 | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| django_template | 40.6 ms                                                                | 39.5 ms: 1.03x faster                                       |
| mako            | 15.2 ms                                                                | 15.5 ms: 1.02x slower                                       |
| Geometric mean  | (ref)                                                                  | 1.00x faster                                                |

Benchmark hidden because not significant (2): genshi_text, genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20250412-vultr-x86_64-python-9634085af3670b1eb654-3.14.0a7+-9634085 | bm-20250412-vultr-x86_64-mpage-exp_nolock-3.14.0a7+-4f84be5 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------:|
| pidigits                   | 219 ms                                                                 | 203 ms: 1.08x faster                                        |
| django_template            | 40.6 ms                                                                | 39.5 ms: 1.03x faster                                       |
| pycparser                  | 1.13 sec                                                               | 1.11 sec: 1.01x faster                                      |
| create_gc_cycles           | 1.35 ms                                                                | 1.33 ms: 1.01x faster                                       |
| coverage                   | 110 ms                                                                 | 109 ms: 1.01x faster                                        |
| json                       | 5.27 ms                                                                | 5.21 ms: 1.01x faster                                       |
| deepcopy                   | 289 us                                                                 | 286 us: 1.01x faster                                        |
| json_loads                 | 30.9 us                                                                | 30.6 us: 1.01x faster                                       |
| regex_v8                   | 21.3 ms                                                                | 21.1 ms: 1.01x faster                                       |
| sqlglot_v2_normalize       | 113 ms                                                                 | 112 ms: 1.01x faster                                        |
| gc_traversal               | 1.78 ms                                                                | 1.77 ms: 1.01x faster                                       |
| html5lib                   | 65.3 ms                                                                | 64.7 ms: 1.01x faster                                       |
| sqlalchemy_declarative     | 154 ms                                                                 | 153 ms: 1.01x faster                                        |
| async_generators           | 363 ms                                                                 | 361 ms: 1.00x faster                                        |
| python_startup             | 15.9 ms                                                                | 15.8 ms: 1.00x faster                                       |
| sympy_str                  | 319 ms                                                                 | 317 ms: 1.00x faster                                        |
| pprint_safe_repr           | 772 ms                                                                 | 769 ms: 1.00x faster                                        |
| python_startup_no_site     | 11.2 ms                                                                | 11.1 ms: 1.00x faster                                       |
| xml_etree_generate         | 93.1 ms                                                                | 93.0 ms: 1.00x faster                                       |
| 2to3                       | 280 ms                                                                 | 280 ms: 1.00x faster                                        |
| bench_thread_pool          | 3.13 ms                                                                | 3.13 ms: 1.00x slower                                       |
| comprehensions             | 19.4 us                                                                | 19.5 us: 1.00x slower                                       |
| mdp                        | 1.30 sec                                                               | 1.31 sec: 1.00x slower                                      |
| xml_etree_process          | 66.1 ms                                                                | 66.4 ms: 1.00x slower                                       |
| sphinx                     | 1.06 sec                                                               | 1.06 sec: 1.00x slower                                      |
| float                      | 67.2 ms                                                                | 67.5 ms: 1.01x slower                                       |
| bpe_tokeniser              | 4.47 sec                                                               | 4.49 sec: 1.01x slower                                      |
| deepcopy_reduce            | 2.95 us                                                                | 2.97 us: 1.01x slower                                       |
| regex_compile              | 143 ms                                                                 | 143 ms: 1.01x slower                                        |
| sqlglot_v2_parse           | 1.45 ms                                                                | 1.46 ms: 1.01x slower                                       |
| connected_components       | 479 ms                                                                 | 482 ms: 1.01x slower                                        |
| async_tree_io              | 543 ms                                                                 | 547 ms: 1.01x slower                                        |
| many_optionals             | 1.10 ms                                                                | 1.11 ms: 1.01x slower                                       |
| xml_etree_iterparse        | 86.3 ms                                                                | 87.0 ms: 1.01x slower                                       |
| raytrace                   | 286 ms                                                                 | 288 ms: 1.01x slower                                        |
| hexiom                     | 6.61 ms                                                                | 6.68 ms: 1.01x slower                                       |
| fannkuch                   | 451 ms                                                                 | 455 ms: 1.01x slower                                        |
| json_dumps                 | 12.6 ms                                                                | 12.7 ms: 1.01x slower                                       |
| coroutines                 | 22.8 ms                                                                | 23.1 ms: 1.01x slower                                       |
| telco                      | 8.33 ms                                                                | 8.44 ms: 1.01x slower                                       |
| scimark_lu                 | 126 ms                                                                 | 128 ms: 1.01x slower                                        |
| logging_silent             | 104 ns                                                                 | 105 ns: 1.01x slower                                        |
| pickle_pure_python         | 325 us                                                                 | 329 us: 1.01x slower                                        |
| spectral_norm              | 101 ms                                                                 | 102 ms: 1.01x slower                                        |
| logging_simple             | 6.93 us                                                                | 7.03 us: 1.01x slower                                       |
| crypto_pyaes               | 81.5 ms                                                                | 82.7 ms: 1.01x slower                                       |
| meteor_contest             | 128 ms                                                                 | 130 ms: 1.02x slower                                        |
| deepcopy_memo              | 34.5 us                                                                | 35.1 us: 1.02x slower                                       |
| scimark_fft                | 337 ms                                                                 | 343 ms: 1.02x slower                                        |
| subparsers                 | 24.2 ms                                                                | 24.7 ms: 1.02x slower                                       |
| tomli_loads                | 2.06 sec                                                               | 2.10 sec: 1.02x slower                                      |
| scimark_sparse_mat_mult    | 4.93 ms                                                                | 5.02 ms: 1.02x slower                                       |
| richards                   | 49.7 ms                                                                | 50.7 ms: 1.02x slower                                       |
| unpickle_pure_python       | 224 us                                                                 | 229 us: 1.02x slower                                        |
| chaos                      | 60.4 ms                                                                | 61.7 ms: 1.02x slower                                       |
| deltablue                  | 3.51 ms                                                                | 3.58 ms: 1.02x slower                                       |
| generators                 | 30.9 ms                                                                | 31.6 ms: 1.02x slower                                       |
| mako                       | 15.2 ms                                                                | 15.5 ms: 1.02x slower                                       |
| pyflate                    | 458 ms                                                                 | 470 ms: 1.02x slower                                        |
| scimark_monte_carlo        | 72.8 ms                                                                | 74.5 ms: 1.02x slower                                       |
| regex_effbot               | 2.74 ms                                                                | 2.80 ms: 1.02x slower                                       |
| richards_super             | 57.6 ms                                                                | 59.1 ms: 1.03x slower                                       |
| go                         | 123 ms                                                                 | 126 ms: 1.03x slower                                        |
| scimark_sor                | 118 ms                                                                 | 123 ms: 1.04x slower                                        |
| regex_dna                  | 175 ms                                                                 | 184 ms: 1.05x slower                                        |
| async_tree_cpu_io_mixed    | 500 ms                                                                 | 550 ms: 1.10x slower                                        |
| async_tree_cpu_io_mixed_tg | 474 ms                                                                 | 523 ms: 1.10x slower                                        |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                |

Benchmark hidden because not significant (28): pylint, async_tree_memoization_tg, genshi_text, typing_runtime_protocols, genshi_xml, asyncio_websockets, pprint_pformat, async_tree_none_tg, k_core, docutils, async_tree_memoization, bench_mp_pool, sympy_sum, async_tree_none, xml_etree_parse, nqueens, dulwich_log, sympy_expand, sympy_integrate, shortest_path, pathlib, sqlalchemy_imperative, sqlite_synth, nbody, async_tree_io_tg, sqlglot_v2_optimize, logging_format, sqlglot_v2_transpile

- Geometric mean (including insignificant results): 1.007x slower

# HPT report

- Reliability score: 99.67% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x