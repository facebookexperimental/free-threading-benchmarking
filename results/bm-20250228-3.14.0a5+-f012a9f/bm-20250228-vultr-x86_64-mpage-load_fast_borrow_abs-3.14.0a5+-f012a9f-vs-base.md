# Results vs. base

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: f012a9f
- commit date: 2025-02-28
- overall geometric mean: 1.009x faster
- HPT reliability: 99.29%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 247 ms                                                                 | 248 ms: 1.00x slower                                                  |
| docutils       | 2.51 sec                                                               | 2.52 sec: 1.01x slower                                                |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_generators           | 320 ms                                                                 | 318 ms: 1.01x faster                                                  |
| async_tree_none            | 259 ms                                                                 | 263 ms: 1.02x slower                                                  |
| coroutines                 | 21.3 ms                                                                | 21.6 ms: 1.02x slower                                                 |
| async_tree_none_tg         | 253 ms                                                                 | 257 ms: 1.02x slower                                                  |
| async_tree_cpu_io_mixed    | 485 ms                                                                 | 498 ms: 1.03x slower                                                  |
| async_tree_cpu_io_mixed_tg | 472 ms                                                                 | 490 ms: 1.04x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (5): asyncio_websockets, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 84.2 ms                                                                | 87.3 ms: 1.04x slower                                                 |
| pidigits       | 187 ms                                                                 | 200 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                          |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.84 ms                                                                | 2.70 ms: 1.05x faster                                                 |
| regex_v8       | 24.7 ms                                                                | 23.5 ms: 1.05x faster                                                 |
| regex_dna      | 177 ms                                                                 | 174 ms: 1.02x faster                                                  |
| regex_compile  | 123 ms                                                                 | 124 ms: 1.01x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_process    | 57.7 ms                                                                | 57.1 ms: 1.01x faster                                                 |
| xml_etree_generate   | 82.8 ms                                                                | 82.3 ms: 1.01x faster                                                 |
| tomli_loads          | 1.87 sec                                                               | 1.86 sec: 1.01x faster                                                |
| unpickle_pure_python | 208 us                                                                 | 208 us: 1.00x slower                                                  |
| json_dumps           | 11.0 ms                                                                | 11.0 ms: 1.00x slower                                                 |
| xml_etree_parse      | 128 ms                                                                 | 129 ms: 1.00x slower                                                  |
| json_loads           | 28.4 us                                                                | 28.8 us: 1.01x slower                                                 |
| pickle_pure_python   | 297 us                                                                 | 302 us: 1.02x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.52 ms                                                                | 7.50 ms: 1.00x faster                                                 |
| python_startup         | 14.8 ms                                                                | 14.8 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 33.1 ms                                                                | 33.3 ms: 1.01x slower                                                 |
| genshi_text     | 20.3 ms                                                                | 20.5 ms: 1.01x slower                                                 |
| mako            | 11.3 ms                                                                | 11.6 ms: 1.02x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                          |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                  | bm-20250228-vultr-x86_64-python-75f38af7810af1c3ca56-3.14.0a5+-75f38af | bm-20250228-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a5+-f012a9f |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| sqlglot_normalize          | 277 ms                                                                 | 102 ms: 2.72x faster                                                  |
| scimark_sparse_mat_mult    | 4.38 ms                                                                | 4.11 ms: 1.07x faster                                                 |
| regex_effbot               | 2.84 ms                                                                | 2.70 ms: 1.05x faster                                                 |
| regex_v8                   | 24.7 ms                                                                | 23.5 ms: 1.05x faster                                                 |
| scimark_lu                 | 111 ms                                                                 | 106 ms: 1.05x faster                                                  |
| pprint_pformat             | 1.39 sec                                                               | 1.36 sec: 1.02x faster                                                |
| connected_components       | 392 ms                                                                 | 385 ms: 1.02x faster                                                  |
| deepcopy_reduce            | 2.57 us                                                                | 2.53 us: 1.02x faster                                                 |
| logging_simple             | 5.94 us                                                                | 5.85 us: 1.02x faster                                                 |
| regex_dna                  | 177 ms                                                                 | 174 ms: 1.02x faster                                                  |
| sqlglot_parse              | 1.24 ms                                                                | 1.22 ms: 1.01x faster                                                 |
| hexiom                     | 5.69 ms                                                                | 5.62 ms: 1.01x faster                                                 |
| pprint_safe_repr           | 680 ms                                                                 | 672 ms: 1.01x faster                                                  |
| sqlglot_transpile          | 1.53 ms                                                                | 1.52 ms: 1.01x faster                                                 |
| xml_etree_process          | 57.7 ms                                                                | 57.1 ms: 1.01x faster                                                 |
| async_generators           | 320 ms                                                                 | 318 ms: 1.01x faster                                                  |
| meteor_contest             | 99.4 ms                                                                | 98.7 ms: 1.01x faster                                                 |
| xml_etree_generate         | 82.8 ms                                                                | 82.3 ms: 1.01x faster                                                 |
| bpe_tokeniser              | 4.15 sec                                                               | 4.12 sec: 1.01x faster                                                |
| tomli_loads                | 1.87 sec                                                               | 1.86 sec: 1.01x faster                                                |
| gc_traversal               | 4.45 ms                                                                | 4.44 ms: 1.00x faster                                                 |
| python_startup_no_site     | 7.52 ms                                                                | 7.50 ms: 1.00x faster                                                 |
| python_startup             | 14.8 ms                                                                | 14.8 ms: 1.00x slower                                                 |
| bench_thread_pool          | 1.03 ms                                                                | 1.03 ms: 1.00x slower                                                 |
| pycparser                  | 1.09 sec                                                               | 1.10 sec: 1.00x slower                                                |
| unpickle_pure_python       | 208 us                                                                 | 208 us: 1.00x slower                                                  |
| scimark_fft                | 309 ms                                                                 | 310 ms: 1.00x slower                                                  |
| dulwich_log                | 74.8 ms                                                                | 75.1 ms: 1.00x slower                                                 |
| json_dumps                 | 11.0 ms                                                                | 11.0 ms: 1.00x slower                                                 |
| xml_etree_parse            | 128 ms                                                                 | 129 ms: 1.00x slower                                                  |
| 2to3                       | 247 ms                                                                 | 248 ms: 1.00x slower                                                  |
| sqlglot_optimize           | 50.6 ms                                                                | 50.8 ms: 1.00x slower                                                 |
| deepcopy_memo              | 28.7 us                                                                | 28.8 us: 1.00x slower                                                 |
| logging_silent             | 102 ns                                                                 | 103 ns: 1.00x slower                                                  |
| raytrace                   | 254 ms                                                                 | 255 ms: 1.01x slower                                                  |
| scimark_monte_carlo        | 62.5 ms                                                                | 62.9 ms: 1.01x slower                                                 |
| comprehensions             | 15.9 us                                                                | 15.9 us: 1.01x slower                                                 |
| coverage                   | 79.0 ms                                                                | 79.4 ms: 1.01x slower                                                 |
| docutils                   | 2.51 sec                                                               | 2.52 sec: 1.01x slower                                                |
| sympy_integrate            | 19.3 ms                                                                | 19.4 ms: 1.01x slower                                                 |
| scimark_sor                | 110 ms                                                                 | 111 ms: 1.01x slower                                                  |
| chaos                      | 53.7 ms                                                                | 54.1 ms: 1.01x slower                                                 |
| sqlalchemy_declarative     | 125 ms                                                                 | 126 ms: 1.01x slower                                                  |
| django_template            | 33.1 ms                                                                | 33.3 ms: 1.01x slower                                                 |
| sympy_sum                  | 150 ms                                                                 | 151 ms: 1.01x slower                                                  |
| subparsers                 | 21.5 ms                                                                | 21.7 ms: 1.01x slower                                                 |
| go                         | 110 ms                                                                 | 111 ms: 1.01x slower                                                  |
| regex_compile              | 123 ms                                                                 | 124 ms: 1.01x slower                                                  |
| genshi_text                | 20.3 ms                                                                | 20.5 ms: 1.01x slower                                                 |
| richards_super             | 47.1 ms                                                                | 47.6 ms: 1.01x slower                                                 |
| generators                 | 26.9 ms                                                                | 27.2 ms: 1.01x slower                                                 |
| telco                      | 7.27 ms                                                                | 7.36 ms: 1.01x slower                                                 |
| richards                   | 41.2 ms                                                                | 41.7 ms: 1.01x slower                                                 |
| many_optionals             | 999 us                                                                 | 1.01 ms: 1.01x slower                                                 |
| json_loads                 | 28.4 us                                                                | 28.8 us: 1.01x slower                                                 |
| crypto_pyaes               | 65.6 ms                                                                | 66.5 ms: 1.01x slower                                                 |
| deltablue                  | 3.01 ms                                                                | 3.06 ms: 1.01x slower                                                 |
| async_tree_none            | 259 ms                                                                 | 263 ms: 1.02x slower                                                  |
| coroutines                 | 21.3 ms                                                                | 21.6 ms: 1.02x slower                                                 |
| async_tree_none_tg         | 253 ms                                                                 | 257 ms: 1.02x slower                                                  |
| pickle_pure_python         | 297 us                                                                 | 302 us: 1.02x slower                                                  |
| pathlib                    | 18.8 ms                                                                | 19.2 ms: 1.02x slower                                                 |
| mako                       | 11.3 ms                                                                | 11.6 ms: 1.02x slower                                                 |
| sqlalchemy_imperative      | 18.9 ms                                                                | 19.3 ms: 1.02x slower                                                 |
| thrift                     | 705 us                                                                 | 722 us: 1.02x slower                                                  |
| async_tree_cpu_io_mixed    | 485 ms                                                                 | 498 ms: 1.03x slower                                                  |
| spectral_norm              | 88.6 ms                                                                | 91.2 ms: 1.03x slower                                                 |
| nbody                      | 84.2 ms                                                                | 87.3 ms: 1.04x slower                                                 |
| async_tree_cpu_io_mixed_tg | 472 ms                                                                 | 490 ms: 1.04x slower                                                  |
| pidigits                   | 187 ms                                                                 | 200 ms: 1.07x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (25): k_core, typing_runtime_protocols, bench_mp_pool, float, shortest_path, pyflate, genshi_xml, sphinx, sympy_expand, asyncio_websockets, json, async_tree_io, logging_format, nqueens, deepcopy, create_gc_cycles, fannkuch, mdp, async_tree_io_tg, sympy_str, xml_etree_iterparse, async_tree_memoization, sqlite_synth, pylint, async_tree_memoization_tg

- Geometric mean (including insignificant results): 1.009x faster

# HPT report

- Reliability score: 99.29% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x