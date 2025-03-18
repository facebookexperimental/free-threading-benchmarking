# Results vs. base

- fork: mpage
- ref: load_fast_borrow_abs
- machine: linux-x86_64
- commit hash: 6c2f07d
- commit date: 2025-03-17
- overall geometric mean: 1.032x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 258 ms                                                                 | 249 ms: 1.04x faster                                                  |
| docutils       | 2.61 sec                                                               | 2.58 sec: 1.01x faster                                                |
| sphinx         | 1.00 sec                                                               | 985 ms: 1.02x faster                                                  |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_generators           | 340 ms                                                                 | 331 ms: 1.03x faster                                                  |
| async_tree_io_tg           | 628 ms                                                                 | 615 ms: 1.02x faster                                                  |
| async_tree_io              | 630 ms                                                                 | 618 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed    | 512 ms                                                                 | 503 ms: 1.02x faster                                                  |
| async_tree_memoization     | 327 ms                                                                 | 322 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                 | 491 ms: 1.01x faster                                                  |
| async_tree_none            | 274 ms                                                                 | 270 ms: 1.01x faster                                                  |
| coroutines                 | 23.1 ms                                                                | 22.8 ms: 1.01x faster                                                 |
| async_tree_none_tg         | 260 ms                                                                 | 257 ms: 1.01x faster                                                  |
| Geometric mean             | (ref)                                                                  | 1.01x faster                                                          |

Benchmark hidden because not significant (2): async_tree_memoization_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody          | 99.0 ms                                                                | 84.2 ms: 1.18x faster                                                 |
| float          | 74.5 ms                                                                | 69.3 ms: 1.07x faster                                                 |
| pidigits       | 206 ms                                                                 | 220 ms: 1.07x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 177 ms                                                                 | 167 ms: 1.06x faster                                                  |
| regex_compile  | 128 ms                                                                 | 124 ms: 1.03x faster                                                  |
| regex_v8       | 24.3 ms                                                                | 24.2 ms: 1.00x faster                                                 |
| regex_effbot   | 2.64 ms                                                                | 2.68 ms: 1.01x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x faster                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_pure_python   | 322 us                                                                 | 305 us: 1.06x faster                                                  |
| unpickle_pure_python | 223 us                                                                 | 215 us: 1.04x faster                                                  |
| json_loads           | 28.4 us                                                                | 27.4 us: 1.04x faster                                                 |
| tomli_loads          | 1.98 sec                                                               | 1.91 sec: 1.04x faster                                                |
| xml_etree_iterparse  | 93.6 ms                                                                | 91.2 ms: 1.03x faster                                                 |
| xml_etree_generate   | 85.7 ms                                                                | 83.7 ms: 1.02x faster                                                 |
| json_dumps           | 11.2 ms                                                                | 11.0 ms: 1.01x faster                                                 |
| xml_etree_process    | 59.7 ms                                                                | 59.3 ms: 1.01x faster                                                 |
| Geometric mean       | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 8.62 ms                                                                | 8.63 ms: 1.00x slower                                                 |
| python_startup         | 15.0 ms                                                                | 15.0 ms: 1.00x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 22.5 ms                                                                | 20.3 ms: 1.11x faster                                                 |
| genshi_xml      | 51.0 ms                                                                | 47.6 ms: 1.07x faster                                                 |
| django_template | 36.5 ms                                                                | 35.9 ms: 1.02x faster                                                 |
| mako            | 12.2 ms                                                                | 12.0 ms: 1.02x faster                                                 |
| Geometric mean  | (ref)                                                                  | 1.05x faster                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250317-vultr-x86_64-python-fd545d735d5f9c048f99-3.14.0a6+-fd545d7 | bm-20250317-vultr-x86_64-mpage-load_fast_borrow_abs-3.14.0a6+-6c2f07d |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| nbody                      | 99.0 ms                                                                | 84.2 ms: 1.18x faster                                                 |
| scimark_monte_carlo        | 67.1 ms                                                                | 60.6 ms: 1.11x faster                                                 |
| genshi_text                | 22.5 ms                                                                | 20.3 ms: 1.11x faster                                                 |
| scimark_sparse_mat_mult    | 4.84 ms                                                                | 4.39 ms: 1.10x faster                                                 |
| logging_silent             | 103 ns                                                                 | 94.5 ns: 1.09x faster                                                 |
| go                         | 116 ms                                                                 | 107 ms: 1.09x faster                                                  |
| raytrace                   | 271 ms                                                                 | 250 ms: 1.09x faster                                                  |
| scimark_sor                | 115 ms                                                                 | 106 ms: 1.08x faster                                                  |
| deepcopy                   | 266 us                                                                 | 247 us: 1.08x faster                                                  |
| float                      | 74.5 ms                                                                | 69.3 ms: 1.07x faster                                                 |
| deepcopy_memo              | 30.8 us                                                                | 28.6 us: 1.07x faster                                                 |
| deepcopy_reduce            | 2.74 us                                                                | 2.55 us: 1.07x faster                                                 |
| generators                 | 29.7 ms                                                                | 27.7 ms: 1.07x faster                                                 |
| genshi_xml                 | 51.0 ms                                                                | 47.6 ms: 1.07x faster                                                 |
| chaos                      | 59.0 ms                                                                | 55.0 ms: 1.07x faster                                                 |
| richards                   | 43.2 ms                                                                | 40.4 ms: 1.07x faster                                                 |
| pprint_pformat             | 1.52 sec                                                               | 1.42 sec: 1.07x faster                                                |
| nqueens                    | 83.8 ms                                                                | 78.8 ms: 1.06x faster                                                 |
| regex_dna                  | 177 ms                                                                 | 167 ms: 1.06x faster                                                  |
| sqlglot_parse              | 1.29 ms                                                                | 1.22 ms: 1.06x faster                                                 |
| richards_super             | 49.2 ms                                                                | 46.4 ms: 1.06x faster                                                 |
| fannkuch                   | 403 ms                                                                 | 380 ms: 1.06x faster                                                  |
| sqlglot_transpile          | 1.60 ms                                                                | 1.51 ms: 1.06x faster                                                 |
| scimark_lu                 | 117 ms                                                                 | 111 ms: 1.06x faster                                                  |
| pyflate                    | 427 ms                                                                 | 404 ms: 1.06x faster                                                  |
| pickle_pure_python         | 322 us                                                                 | 305 us: 1.06x faster                                                  |
| pprint_safe_repr           | 736 ms                                                                 | 697 ms: 1.06x faster                                                  |
| scimark_fft                | 329 ms                                                                 | 314 ms: 1.05x faster                                                  |
| hexiom                     | 6.10 ms                                                                | 5.82 ms: 1.05x faster                                                 |
| sqlglot_optimize           | 53.2 ms                                                                | 50.8 ms: 1.05x faster                                                 |
| json                       | 5.06 ms                                                                | 4.84 ms: 1.05x faster                                                 |
| sqlglot_normalize          | 106 ms                                                                 | 101 ms: 1.04x faster                                                  |
| pycparser                  | 1.15 sec                                                               | 1.10 sec: 1.04x faster                                                |
| unpickle_pure_python       | 223 us                                                                 | 215 us: 1.04x faster                                                  |
| meteor_contest             | 105 ms                                                                 | 101 ms: 1.04x faster                                                  |
| json_loads                 | 28.4 us                                                                | 27.4 us: 1.04x faster                                                 |
| 2to3                       | 258 ms                                                                 | 249 ms: 1.04x faster                                                  |
| tomli_loads                | 1.98 sec                                                               | 1.91 sec: 1.04x faster                                                |
| many_optionals             | 1.04 ms                                                                | 1.01 ms: 1.03x faster                                                 |
| subparsers                 | 22.9 ms                                                                | 22.2 ms: 1.03x faster                                                 |
| telco                      | 7.56 ms                                                                | 7.32 ms: 1.03x faster                                                 |
| regex_compile              | 128 ms                                                                 | 124 ms: 1.03x faster                                                  |
| sympy_expand               | 475 ms                                                                 | 462 ms: 1.03x faster                                                  |
| sympy_str                  | 280 ms                                                                 | 272 ms: 1.03x faster                                                  |
| logging_simple             | 6.14 us                                                                | 5.97 us: 1.03x faster                                                 |
| crypto_pyaes               | 71.8 ms                                                                | 69.8 ms: 1.03x faster                                                 |
| logging_format             | 6.83 us                                                                | 6.64 us: 1.03x faster                                                 |
| thrift                     | 748 us                                                                 | 728 us: 1.03x faster                                                  |
| async_generators           | 340 ms                                                                 | 331 ms: 1.03x faster                                                  |
| comprehensions             | 17.0 us                                                                | 16.6 us: 1.03x faster                                                 |
| xml_etree_iterparse        | 93.6 ms                                                                | 91.2 ms: 1.03x faster                                                 |
| xml_etree_generate         | 85.7 ms                                                                | 83.7 ms: 1.02x faster                                                 |
| bpe_tokeniser              | 4.37 sec                                                               | 4.28 sec: 1.02x faster                                                |
| async_tree_io_tg           | 628 ms                                                                 | 615 ms: 1.02x faster                                                  |
| sympy_integrate            | 20.1 ms                                                                | 19.7 ms: 1.02x faster                                                 |
| sphinx                     | 1.00 sec                                                               | 985 ms: 1.02x faster                                                  |
| async_tree_io              | 630 ms                                                                 | 618 ms: 1.02x faster                                                  |
| sympy_sum                  | 157 ms                                                                 | 154 ms: 1.02x faster                                                  |
| async_tree_cpu_io_mixed    | 512 ms                                                                 | 503 ms: 1.02x faster                                                  |
| async_tree_memoization     | 327 ms                                                                 | 322 ms: 1.02x faster                                                  |
| django_template            | 36.5 ms                                                                | 35.9 ms: 1.02x faster                                                 |
| mako                       | 12.2 ms                                                                | 12.0 ms: 1.02x faster                                                 |
| k_core                     | 2.07 sec                                                               | 2.04 sec: 1.01x faster                                                |
| shortest_path              | 443 ms                                                                 | 436 ms: 1.01x faster                                                  |
| async_tree_cpu_io_mixed_tg | 498 ms                                                                 | 491 ms: 1.01x faster                                                  |
| async_tree_none            | 274 ms                                                                 | 270 ms: 1.01x faster                                                  |
| json_dumps                 | 11.2 ms                                                                | 11.0 ms: 1.01x faster                                                 |
| coroutines                 | 23.1 ms                                                                | 22.8 ms: 1.01x faster                                                 |
| docutils                   | 2.61 sec                                                               | 2.58 sec: 1.01x faster                                                |
| dulwich_log                | 68.0 ms                                                                | 67.3 ms: 1.01x faster                                                 |
| sqlalchemy_declarative     | 131 ms                                                                 | 130 ms: 1.01x faster                                                  |
| async_tree_none_tg         | 260 ms                                                                 | 257 ms: 1.01x faster                                                  |
| bench_thread_pool          | 1.05 ms                                                                | 1.04 ms: 1.01x faster                                                 |
| connected_components       | 403 ms                                                                 | 400 ms: 1.01x faster                                                  |
| bench_mp_pool              | 88.4 ms                                                                | 87.9 ms: 1.01x faster                                                 |
| xml_etree_process          | 59.7 ms                                                                | 59.3 ms: 1.01x faster                                                 |
| regex_v8                   | 24.3 ms                                                                | 24.2 ms: 1.00x faster                                                 |
| python_startup_no_site     | 8.62 ms                                                                | 8.63 ms: 1.00x slower                                                 |
| python_startup             | 15.0 ms                                                                | 15.0 ms: 1.00x slower                                                 |
| sqlalchemy_imperative      | 19.5 ms                                                                | 19.7 ms: 1.01x slower                                                 |
| gc_traversal               | 4.16 ms                                                                | 4.21 ms: 1.01x slower                                                 |
| regex_effbot               | 2.64 ms                                                                | 2.68 ms: 1.01x slower                                                 |
| deltablue                  | 3.17 ms                                                                | 3.21 ms: 1.02x slower                                                 |
| spectral_norm              | 93.1 ms                                                                | 94.6 ms: 1.02x slower                                                 |
| mdp                        | 2.35 sec                                                               | 2.42 sec: 1.03x slower                                                |
| pidigits                   | 206 ms                                                                 | 220 ms: 1.07x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                          |

Benchmark hidden because not significant (9): pylint, sqlite_synth, xml_etree_parse, typing_runtime_protocols, pathlib, async_tree_memoization_tg, create_gc_cycles, asyncio_websockets, coverage

- Geometric mean (including insignificant results): 1.032x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.01x