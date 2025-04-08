# Results vs. base

- fork: mpage
- ref: experiment_noinline
- machine: linux-x86_64
- commit hash: 521fae6
- commit date: 2025-04-07
- overall geometric mean: 1.040x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.03x faster
- Memory change: 1.01x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 247 ms: 1.03x faster                                                 |
| docutils       | 2.58 sec                                                               | 2.53 sec: 1.02x faster                                               |
| sphinx         | 1000 ms                                                                | 977 ms: 1.02x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_generators           | 337 ms                                                                 | 321 ms: 1.05x faster                                                 |
| async_tree_none            | 282 ms                                                                 | 270 ms: 1.04x faster                                                 |
| async_tree_none_tg         | 265 ms                                                                 | 255 ms: 1.04x faster                                                 |
| coroutines                 | 24.5 ms                                                                | 23.6 ms: 1.04x faster                                                |
| async_tree_io_tg           | 631 ms                                                                 | 609 ms: 1.04x faster                                                 |
| async_tree_memoization_tg  | 324 ms                                                                 | 313 ms: 1.04x faster                                                 |
| async_tree_memoization     | 321 ms                                                                 | 311 ms: 1.03x faster                                                 |
| async_tree_io              | 632 ms                                                                 | 612 ms: 1.03x faster                                                 |
| async_tree_cpu_io_mixed    | 503 ms                                                                 | 493 ms: 1.02x faster                                                 |
| async_tree_cpu_io_mixed_tg | 499 ms                                                                 | 491 ms: 1.02x faster                                                 |
| Geometric mean             | (ref)                                                                  | 1.03x faster                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| nbody          | 92.6 ms                                                                | 84.2 ms: 1.10x faster                                                |
| float          | 71.4 ms                                                                | 68.4 ms: 1.04x faster                                                |
| pidigits       | 190 ms                                                                 | 190 ms: 1.00x faster                                                 |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 2.84 ms                                                                | 2.61 ms: 1.09x faster                                                |
| regex_dna      | 181 ms                                                                 | 166 ms: 1.09x faster                                                 |
| regex_compile  | 130 ms                                                                 | 123 ms: 1.06x faster                                                 |
| regex_v8       | 22.1 ms                                                                | 21.8 ms: 1.01x faster                                                |
| Geometric mean | (ref)                                                                  | 1.06x faster                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_pure_python   | 322 us                                                                 | 300 us: 1.07x faster                                                 |
| unpickle_pure_python | 222 us                                                                 | 207 us: 1.07x faster                                                 |
| tomli_loads          | 1.99 sec                                                               | 1.87 sec: 1.07x faster                                               |
| xml_etree_process    | 60.6 ms                                                                | 58.9 ms: 1.03x faster                                                |
| xml_etree_iterparse  | 93.7 ms                                                                | 91.5 ms: 1.02x faster                                                |
| xml_etree_generate   | 85.1 ms                                                                | 83.2 ms: 1.02x faster                                                |
| json_loads           | 27.7 us                                                                | 27.3 us: 1.02x faster                                                |
| json_dumps           | 11.2 ms                                                                | 11.3 ms: 1.01x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.03x faster                                                         |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup | 15.1 ms                                                                | 15.1 ms: 1.00x faster                                                |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                         |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_text     | 22.0 ms                                                                | 20.7 ms: 1.06x faster                                                |
| django_template | 36.6 ms                                                                | 34.7 ms: 1.05x faster                                                |
| mako            | 12.2 ms                                                                | 11.7 ms: 1.05x faster                                                |
| genshi_xml      | 50.5 ms                                                                | 48.3 ms: 1.05x faster                                                |
| Geometric mean  | (ref)                                                                  | 1.05x faster                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20250407-vultr-x86_64-python-f0dcb29d3affbbe1ec25-3.14.0a6+-f0dcb29 | bm-20250407-vultr-x86_64-mpage-experiment_noinline-3.14.0a6+-521fae6 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| richards                   | 44.5 ms                                                                | 40.3 ms: 1.10x faster                                                |
| nbody                      | 92.6 ms                                                                | 84.2 ms: 1.10x faster                                                |
| richards_super             | 50.3 ms                                                                | 46.2 ms: 1.09x faster                                                |
| regex_effbot               | 2.84 ms                                                                | 2.61 ms: 1.09x faster                                                |
| logging_silent             | 101 ns                                                                 | 92.5 ns: 1.09x faster                                                |
| regex_dna                  | 181 ms                                                                 | 166 ms: 1.09x faster                                                 |
| hexiom                     | 6.12 ms                                                                | 5.66 ms: 1.08x faster                                                |
| pickle_pure_python         | 322 us                                                                 | 300 us: 1.07x faster                                                 |
| unpickle_pure_python       | 222 us                                                                 | 207 us: 1.07x faster                                                 |
| nqueens                    | 80.8 ms                                                                | 75.5 ms: 1.07x faster                                                |
| go                         | 114 ms                                                                 | 107 ms: 1.07x faster                                                 |
| generators                 | 29.2 ms                                                                | 27.4 ms: 1.07x faster                                                |
| spectral_norm              | 98.0 ms                                                                | 91.8 ms: 1.07x faster                                                |
| tomli_loads                | 1.99 sec                                                               | 1.87 sec: 1.07x faster                                               |
| pycparser                  | 1.17 sec                                                               | 1.10 sec: 1.06x faster                                               |
| scimark_monte_carlo        | 63.8 ms                                                                | 60.0 ms: 1.06x faster                                                |
| genshi_text                | 22.0 ms                                                                | 20.7 ms: 1.06x faster                                                |
| comprehensions             | 17.3 us                                                                | 16.3 us: 1.06x faster                                                |
| scimark_sor                | 115 ms                                                                 | 108 ms: 1.06x faster                                                 |
| chaos                      | 55.9 ms                                                                | 52.7 ms: 1.06x faster                                                |
| pprint_pformat             | 1.49 sec                                                               | 1.41 sec: 1.06x faster                                               |
| gc_traversal               | 4.26 ms                                                                | 4.03 ms: 1.06x faster                                                |
| sqlglot_v2_parse           | 1.28 ms                                                                | 1.21 ms: 1.06x faster                                                |
| sqlglot_v2_transpile       | 1.59 ms                                                                | 1.50 ms: 1.06x faster                                                |
| fannkuch                   | 396 ms                                                                 | 374 ms: 1.06x faster                                                 |
| regex_compile              | 130 ms                                                                 | 123 ms: 1.06x faster                                                 |
| sqlglot_v2_normalize       | 106 ms                                                                 | 100 ms: 1.06x faster                                                 |
| raytrace                   | 260 ms                                                                 | 246 ms: 1.06x faster                                                 |
| pprint_safe_repr           | 732 ms                                                                 | 695 ms: 1.05x faster                                                 |
| django_template            | 36.6 ms                                                                | 34.7 ms: 1.05x faster                                                |
| deltablue                  | 3.36 ms                                                                | 3.19 ms: 1.05x faster                                                |
| scimark_lu                 | 117 ms                                                                 | 111 ms: 1.05x faster                                                 |
| async_generators           | 337 ms                                                                 | 321 ms: 1.05x faster                                                 |
| deepcopy                   | 262 us                                                                 | 250 us: 1.05x faster                                                 |
| deepcopy_memo              | 29.7 us                                                                | 28.3 us: 1.05x faster                                                |
| logging_format             | 6.92 us                                                                | 6.60 us: 1.05x faster                                                |
| mako                       | 12.2 ms                                                                | 11.7 ms: 1.05x faster                                                |
| logging_simple             | 6.24 us                                                                | 5.97 us: 1.05x faster                                                |
| genshi_xml                 | 50.5 ms                                                                | 48.3 ms: 1.05x faster                                                |
| typing_runtime_protocols   | 162 us                                                                 | 155 us: 1.04x faster                                                 |
| async_tree_none            | 282 ms                                                                 | 270 ms: 1.04x faster                                                 |
| deepcopy_reduce            | 2.69 us                                                                | 2.58 us: 1.04x faster                                                |
| float                      | 71.4 ms                                                                | 68.4 ms: 1.04x faster                                                |
| sqlglot_v2_optimize        | 52.5 ms                                                                | 50.4 ms: 1.04x faster                                                |
| sympy_str                  | 281 ms                                                                 | 270 ms: 1.04x faster                                                 |
| crypto_pyaes               | 69.7 ms                                                                | 67.0 ms: 1.04x faster                                                |
| mdp                        | 1.18 sec                                                               | 1.14 sec: 1.04x faster                                               |
| async_tree_none_tg         | 265 ms                                                                 | 255 ms: 1.04x faster                                                 |
| coroutines                 | 24.5 ms                                                                | 23.6 ms: 1.04x faster                                                |
| scimark_fft                | 321 ms                                                                 | 309 ms: 1.04x faster                                                 |
| bpe_tokeniser              | 4.35 sec                                                               | 4.20 sec: 1.04x faster                                               |
| sqlalchemy_imperative      | 20.6 ms                                                                | 19.8 ms: 1.04x faster                                                |
| sympy_sum                  | 159 ms                                                                 | 153 ms: 1.04x faster                                                 |
| async_tree_io_tg           | 631 ms                                                                 | 609 ms: 1.04x faster                                                 |
| pyflate                    | 420 ms                                                                 | 405 ms: 1.04x faster                                                 |
| async_tree_memoization_tg  | 324 ms                                                                 | 313 ms: 1.04x faster                                                 |
| telco                      | 7.29 ms                                                                | 7.04 ms: 1.03x faster                                                |
| sympy_integrate            | 19.6 ms                                                                | 18.9 ms: 1.03x faster                                                |
| 2to3                       | 255 ms                                                                 | 247 ms: 1.03x faster                                                 |
| async_tree_memoization     | 321 ms                                                                 | 311 ms: 1.03x faster                                                 |
| async_tree_io              | 632 ms                                                                 | 612 ms: 1.03x faster                                                 |
| pylint                     | 287 ms                                                                 | 278 ms: 1.03x faster                                                 |
| xml_etree_process          | 60.6 ms                                                                | 58.9 ms: 1.03x faster                                                |
| sympy_expand               | 471 ms                                                                 | 458 ms: 1.03x faster                                                 |
| dulwich_log                | 68.9 ms                                                                | 67.1 ms: 1.03x faster                                                |
| meteor_contest             | 101 ms                                                                 | 98.0 ms: 1.03x faster                                                |
| sqlalchemy_declarative     | 132 ms                                                                 | 129 ms: 1.02x faster                                                 |
| xml_etree_iterparse        | 93.7 ms                                                                | 91.5 ms: 1.02x faster                                                |
| xml_etree_generate         | 85.1 ms                                                                | 83.2 ms: 1.02x faster                                                |
| many_optionals             | 1.04 ms                                                                | 1.02 ms: 1.02x faster                                                |
| sphinx                     | 1000 ms                                                                | 977 ms: 1.02x faster                                                 |
| docutils                   | 2.58 sec                                                               | 2.53 sec: 1.02x faster                                               |
| k_core                     | 2.06 sec                                                               | 2.02 sec: 1.02x faster                                               |
| async_tree_cpu_io_mixed    | 503 ms                                                                 | 493 ms: 1.02x faster                                                 |
| json_loads                 | 27.7 us                                                                | 27.3 us: 1.02x faster                                                |
| async_tree_cpu_io_mixed_tg | 499 ms                                                                 | 491 ms: 1.02x faster                                                 |
| subparsers                 | 22.5 ms                                                                | 22.2 ms: 1.02x faster                                                |
| pathlib                    | 19.7 ms                                                                | 19.4 ms: 1.01x faster                                                |
| regex_v8                   | 22.1 ms                                                                | 21.8 ms: 1.01x faster                                                |
| connected_components       | 399 ms                                                                 | 394 ms: 1.01x faster                                                 |
| bench_thread_pool          | 1.06 ms                                                                | 1.05 ms: 1.01x faster                                                |
| shortest_path              | 441 ms                                                                 | 437 ms: 1.01x faster                                                 |
| bench_mp_pool              | 88.9 ms                                                                | 88.3 ms: 1.01x faster                                                |
| python_startup             | 15.1 ms                                                                | 15.1 ms: 1.00x faster                                                |
| pidigits                   | 190 ms                                                                 | 190 ms: 1.00x faster                                                 |
| json_dumps                 | 11.2 ms                                                                | 11.3 ms: 1.01x slower                                                |
| scimark_sparse_mat_mult    | 4.40 ms                                                                | 4.44 ms: 1.01x slower                                                |
| coverage                   | 79.9 ms                                                                | 81.4 ms: 1.02x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                         |

Benchmark hidden because not significant (6): json, sqlite_synth, python_startup_no_site, create_gc_cycles, xml_etree_parse, asyncio_websockets

- Geometric mean (including insignificant results): 1.040x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.03x
- 99% likely to have a speedup of 1.03x

# Memory
- memory change: 1.01x