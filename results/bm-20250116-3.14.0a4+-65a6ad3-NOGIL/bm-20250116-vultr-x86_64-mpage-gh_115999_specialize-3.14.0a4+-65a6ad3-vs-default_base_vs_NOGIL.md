# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 65a6ad3
- commit date: 2025-01-16
- overall geometric mean: 1.136x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 306 ms: 1.21x slower                                                  |
| docutils       | 2.58 sec                                                               | 2.83 sec: 1.10x slower                                                |
| sphinx         | 988 ms                                                                 | 1.12 sec: 1.14x slower                                                |
| Geometric mean | (ref)                                                                  | 1.15x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_none_tg         | 252 ms                                                                 | 240 ms: 1.05x faster                                                  |
| async_tree_io_tg           | 605 ms                                                                 | 583 ms: 1.04x faster                                                  |
| asyncio_websockets         | 523 ms                                                                 | 513 ms: 1.02x faster                                                  |
| async_tree_memoization_tg  | 302 ms                                                                 | 310 ms: 1.03x slower                                                  |
| async_tree_cpu_io_mixed_tg | 473 ms                                                                 | 499 ms: 1.06x slower                                                  |
| async_tree_memoization     | 327 ms                                                                 | 350 ms: 1.07x slower                                                  |
| async_tree_none            | 267 ms                                                                 | 286 ms: 1.07x slower                                                  |
| coroutines                 | 21.8 ms                                                                | 23.7 ms: 1.09x slower                                                 |
| async_tree_cpu_io_mixed    | 490 ms                                                                 | 540 ms: 1.10x slower                                                  |
| async_generators           | 324 ms                                                                 | 367 ms: 1.13x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.04x slower                                                          |

Benchmark hidden because not significant (1): async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 206 ms                                                                 | 209 ms: 1.01x slower                                                  |
| float          | 71.3 ms                                                                | 78.5 ms: 1.10x slower                                                 |
| nbody          | 85.8 ms                                                                | 135 ms: 1.57x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.21x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 23.8 ms                                                                | 23.4 ms: 1.02x faster                                                 |
| regex_effbot   | 2.84 ms                                                                | 2.82 ms: 1.01x faster                                                 |
| regex_dna      | 171 ms                                                                 | 183 ms: 1.07x slower                                                  |
| regex_compile  | 128 ms                                                                 | 152 ms: 1.19x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.9 ms                                                                | 87.0 ms: 1.04x faster                                                 |
| xml_etree_parse      | 130 ms                                                                 | 128 ms: 1.01x faster                                                  |
| json_loads           | 27.8 us                                                                | 30.7 us: 1.11x slower                                                 |
| xml_etree_generate   | 85.1 ms                                                                | 96.4 ms: 1.13x slower                                                 |
| json_dumps           | 11.4 ms                                                                | 13.0 ms: 1.14x slower                                                 |
| xml_etree_process    | 59.9 ms                                                                | 69.0 ms: 1.15x slower                                                 |
| unpickle_pure_python | 216 us                                                                 | 252 us: 1.17x slower                                                  |
| pickle_pure_python   | 308 us                                                                 | 377 us: 1.22x slower                                                  |
| tomli_loads          | 1.90 sec                                                               | 2.35 sec: 1.24x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 15.2 ms: 1.04x slower                                                 |
| python_startup_no_site | 7.45 ms                                                                | 9.54 ms: 1.28x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 35.7 ms                                                                | 43.0 ms: 1.20x slower                                                 |
| genshi_xml      | 49.4 ms                                                                | 60.4 ms: 1.22x slower                                                 |
| genshi_text     | 21.6 ms                                                                | 28.2 ms: 1.31x slower                                                 |
| mako            | 11.7 ms                                                                | 15.6 ms: 1.33x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.27x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250116-vultr-x86_64-python-211f41316b7f205d18eb-3.14.0a4+-211f413 | bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| create_gc_cycles           | 1.85 ms                                                                | 1.32 ms: 1.40x faster                                                 |
| gc_traversal               | 4.32 ms                                                                | 3.13 ms: 1.38x faster                                                 |
| sqlite_synth               | 2.22 us                                                                | 2.05 us: 1.09x faster                                                 |
| async_tree_none_tg         | 252 ms                                                                 | 240 ms: 1.05x faster                                                  |
| xml_etree_iterparse        | 90.9 ms                                                                | 87.0 ms: 1.04x faster                                                 |
| async_tree_io_tg           | 605 ms                                                                 | 583 ms: 1.04x faster                                                  |
| asyncio_websockets         | 523 ms                                                                 | 513 ms: 1.02x faster                                                  |
| regex_v8                   | 23.8 ms                                                                | 23.4 ms: 1.02x faster                                                 |
| xml_etree_parse            | 130 ms                                                                 | 128 ms: 1.01x faster                                                  |
| regex_effbot               | 2.84 ms                                                                | 2.82 ms: 1.01x faster                                                 |
| pidigits                   | 206 ms                                                                 | 209 ms: 1.01x slower                                                  |
| pathlib                    | 18.3 ms                                                                | 18.7 ms: 1.02x slower                                                 |
| async_tree_memoization_tg  | 302 ms                                                                 | 310 ms: 1.03x slower                                                  |
| python_startup             | 14.6 ms                                                                | 15.2 ms: 1.04x slower                                                 |
| async_tree_cpu_io_mixed_tg | 473 ms                                                                 | 499 ms: 1.06x slower                                                  |
| json                       | 5.02 ms                                                                | 5.33 ms: 1.06x slower                                                 |
| pycparser                  | 1.12 sec                                                               | 1.19 sec: 1.07x slower                                                |
| bench_mp_pool              | 88.5 ms                                                                | 94.7 ms: 1.07x slower                                                 |
| regex_dna                  | 171 ms                                                                 | 183 ms: 1.07x slower                                                  |
| async_tree_memoization     | 327 ms                                                                 | 350 ms: 1.07x slower                                                  |
| async_tree_none            | 267 ms                                                                 | 286 ms: 1.07x slower                                                  |
| dulwich_log                | 76.1 ms                                                                | 82.1 ms: 1.08x slower                                                 |
| coroutines                 | 21.8 ms                                                                | 23.7 ms: 1.09x slower                                                 |
| docutils                   | 2.58 sec                                                               | 2.83 sec: 1.10x slower                                                |
| async_tree_cpu_io_mixed    | 490 ms                                                                 | 540 ms: 1.10x slower                                                  |
| float                      | 71.3 ms                                                                | 78.5 ms: 1.10x slower                                                 |
| json_loads                 | 27.8 us                                                                | 30.7 us: 1.11x slower                                                 |
| bpe_tokeniser              | 4.22 sec                                                               | 4.74 sec: 1.12x slower                                                |
| mdp                        | 2.46 sec                                                               | 2.77 sec: 1.12x slower                                                |
| generators                 | 28.0 ms                                                                | 31.5 ms: 1.13x slower                                                 |
| k_core                     | 2.05 sec                                                               | 2.31 sec: 1.13x slower                                                |
| async_generators           | 324 ms                                                                 | 367 ms: 1.13x slower                                                  |
| xml_etree_generate         | 85.1 ms                                                                | 96.4 ms: 1.13x slower                                                 |
| pylint                     | 282 ms                                                                 | 319 ms: 1.13x slower                                                  |
| sphinx                     | 988 ms                                                                 | 1.12 sec: 1.14x slower                                                |
| json_dumps                 | 11.4 ms                                                                | 13.0 ms: 1.14x slower                                                 |
| many_optionals             | 1.02 ms                                                                | 1.18 ms: 1.15x slower                                                 |
| xml_etree_process          | 59.9 ms                                                                | 69.0 ms: 1.15x slower                                                 |
| subparsers                 | 21.9 ms                                                                | 25.3 ms: 1.15x slower                                                 |
| logging_silent             | 102 ns                                                                 | 118 ns: 1.15x slower                                                  |
| scimark_sor                | 115 ms                                                                 | 133 ms: 1.16x slower                                                  |
| sqlglot_normalize          | 105 ms                                                                 | 122 ms: 1.16x slower                                                  |
| telco                      | 7.33 ms                                                                | 8.52 ms: 1.16x slower                                                 |
| unpickle_pure_python       | 216 us                                                                 | 252 us: 1.17x slower                                                  |
| pprint_safe_repr           | 704 ms                                                                 | 828 ms: 1.18x slower                                                  |
| scimark_fft                | 328 ms                                                                 | 387 ms: 1.18x slower                                                  |
| pprint_pformat             | 1.44 sec                                                               | 1.70 sec: 1.18x slower                                                |
| sqlglot_optimize           | 52.4 ms                                                                | 62.1 ms: 1.19x slower                                                 |
| regex_compile              | 128 ms                                                                 | 152 ms: 1.19x slower                                                  |
| logging_simple             | 6.16 us                                                                | 7.37 us: 1.20x slower                                                 |
| sympy_expand               | 461 ms                                                                 | 552 ms: 1.20x slower                                                  |
| django_template            | 35.7 ms                                                                | 43.0 ms: 1.20x slower                                                 |
| scimark_lu                 | 115 ms                                                                 | 138 ms: 1.20x slower                                                  |
| 2to3                       | 253 ms                                                                 | 306 ms: 1.21x slower                                                  |
| go                         | 115 ms                                                                 | 139 ms: 1.21x slower                                                  |
| deepcopy                   | 259 us                                                                 | 316 us: 1.22x slower                                                  |
| spectral_norm              | 88.3 ms                                                                | 108 ms: 1.22x slower                                                  |
| pickle_pure_python         | 308 us                                                                 | 377 us: 1.22x slower                                                  |
| genshi_xml                 | 49.4 ms                                                                | 60.4 ms: 1.22x slower                                                 |
| sympy_integrate            | 19.8 ms                                                                | 24.3 ms: 1.22x slower                                                 |
| scimark_sparse_mat_mult    | 4.59 ms                                                                | 5.63 ms: 1.23x slower                                                 |
| sympy_sum                  | 153 ms                                                                 | 188 ms: 1.23x slower                                                  |
| logging_format             | 6.87 us                                                                | 8.43 us: 1.23x slower                                                 |
| pyflate                    | 409 ms                                                                 | 502 ms: 1.23x slower                                                  |
| coverage                   | 79.6 ms                                                                | 97.9 ms: 1.23x slower                                                 |
| sympy_str                  | 273 ms                                                                 | 336 ms: 1.23x slower                                                  |
| thrift                     | 741 us                                                                 | 914 us: 1.23x slower                                                  |
| tomli_loads                | 1.90 sec                                                               | 2.35 sec: 1.24x slower                                                |
| chaos                      | 55.6 ms                                                                | 68.7 ms: 1.24x slower                                                 |
| nqueens                    | 78.1 ms                                                                | 96.9 ms: 1.24x slower                                                 |
| sqlalchemy_imperative      | 19.5 ms                                                                | 24.2 ms: 1.24x slower                                                 |
| shortest_path              | 430 ms                                                                 | 536 ms: 1.25x slower                                                  |
| comprehensions             | 16.7 us                                                                | 20.9 us: 1.25x slower                                                 |
| connected_components       | 390 ms                                                                 | 488 ms: 1.25x slower                                                  |
| deepcopy_reduce            | 2.65 us                                                                | 3.33 us: 1.26x slower                                                 |
| raytrace                   | 261 ms                                                                 | 330 ms: 1.26x slower                                                  |
| sqlglot_transpile          | 1.55 ms                                                                | 1.96 ms: 1.27x slower                                                 |
| sqlalchemy_declarative     | 129 ms                                                                 | 164 ms: 1.28x slower                                                  |
| scimark_monte_carlo        | 64.4 ms                                                                | 82.2 ms: 1.28x slower                                                 |
| fannkuch                   | 375 ms                                                                 | 480 ms: 1.28x slower                                                  |
| python_startup_no_site     | 7.45 ms                                                                | 9.54 ms: 1.28x slower                                                 |
| sqlglot_parse              | 1.25 ms                                                                | 1.63 ms: 1.30x slower                                                 |
| hexiom                     | 5.73 ms                                                                | 7.44 ms: 1.30x slower                                                 |
| genshi_text                | 21.6 ms                                                                | 28.2 ms: 1.31x slower                                                 |
| typing_runtime_protocols   | 156 us                                                                 | 204 us: 1.31x slower                                                  |
| deepcopy_memo              | 29.9 us                                                                | 39.3 us: 1.32x slower                                                 |
| crypto_pyaes               | 66.6 ms                                                                | 88.3 ms: 1.33x slower                                                 |
| mako                       | 11.7 ms                                                                | 15.6 ms: 1.33x slower                                                 |
| meteor_contest             | 97.7 ms                                                                | 131 ms: 1.34x slower                                                  |
| richards                   | 42.0 ms                                                                | 57.3 ms: 1.36x slower                                                 |
| richards_super             | 48.1 ms                                                                | 66.9 ms: 1.39x slower                                                 |
| deltablue                  | 3.15 ms                                                                | 4.66 ms: 1.48x slower                                                 |
| nbody                      | 85.8 ms                                                                | 135 ms: 1.57x slower                                                  |
| bench_thread_pool          | 1.04 ms                                                                | 3.33 ms: 3.21x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.17x slower                                                          |

Benchmark hidden because not significant (1): async_tree_io
Ignored benchmarks (1) of results/bm-20250116-3.14.0a4+-65a6ad3-NOGIL/bm-20250116-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a4+-65a6ad3.json: html5lib

- Geometric mean (including insignificant results): 1.136x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.20x