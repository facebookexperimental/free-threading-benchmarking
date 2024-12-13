# Results vs. base

- fork: nascheme
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: d6ea4f1
- commit date: 2024-12-13
- overall geometric mean: 1.001x faster
- HPT reliability: 99.56%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 255 ms: 1.01x slower                                                     |
| docutils       | 2.53 sec                                                               | 2.55 sec: 1.01x slower                                                   |
| sphinx         | 980 ms                                                                 | 988 ms: 1.01x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_cpu_io_mixed    | 567 ms                                                                 | 498 ms: 1.14x faster                                                     |
| async_tree_cpu_io_mixed_tg | 547 ms                                                                 | 481 ms: 1.14x faster                                                     |
| async_tree_io              | 625 ms                                                                 | 618 ms: 1.01x faster                                                     |
| asyncio_websockets         | 523 ms                                                                 | 523 ms: 1.00x slower                                                     |
| async_generators           | 359 ms                                                                 | 362 ms: 1.01x slower                                                     |
| coroutines                 | 21.3 ms                                                                | 23.2 ms: 1.09x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.02x faster                                                             |

Benchmark hidden because not significant (5): async_tree_none, async_tree_memoization, async_tree_memoization_tg, async_tree_io_tg, async_tree_none_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 216 ms                                                                 | 185 ms: 1.17x faster                                                     |
| float          | 77.2 ms                                                                | 76.1 ms: 1.01x faster                                                    |
| nbody          | 89.4 ms                                                                | 91.8 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.05x faster                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 24.5 ms                                                                | 24.7 ms: 1.01x slower                                                    |
| regex_dna      | 172 ms                                                                 | 174 ms: 1.01x slower                                                     |
| regex_compile  | 127 ms                                                                 | 129 ms: 1.01x slower                                                     |
| regex_effbot   | 2.68 ms                                                                | 2.72 ms: 1.01x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.01x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 26.5 us                                                                | 26.1 us: 1.01x faster                                                    |
| pickle_pure_python   | 314 us                                                                 | 310 us: 1.01x faster                                                     |
| xml_etree_iterparse  | 90.2 ms                                                                | 90.5 ms: 1.00x slower                                                    |
| json_dumps           | 11.3 ms                                                                | 11.4 ms: 1.01x slower                                                    |
| xml_etree_generate   | 82.9 ms                                                                | 83.7 ms: 1.01x slower                                                    |
| xml_etree_process    | 57.8 ms                                                                | 58.4 ms: 1.01x slower                                                    |
| unpickle_pure_python | 208 us                                                                 | 212 us: 1.02x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (2): xml_etree_parse, tomli_loads

Benchmarks with tag 'startup':
==============================

| Benchmark      | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup | 14.6 ms                                                                | 14.6 ms: 1.00x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (1): python_startup_no_site

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 49.3 ms                                                                | 49.7 ms: 1.01x slower                                                    |
| django_template | 34.6 ms                                                                | 35.0 ms: 1.01x slower                                                    |
| mako            | 11.4 ms                                                                | 11.7 ms: 1.03x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (1): genshi_text

All benchmarks:
===============

| Benchmark                  | bm-20241211-vultr-x86_64-python-bc262de06b10a2d119c2-3.14.0a2+-bc262de | bm-20241213-vultr-x86_64-nascheme-gh_115999_specialize-3.14.0a2+-d6ea4f1 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits                   | 216 ms                                                                 | 185 ms: 1.17x faster                                                     |
| async_tree_cpu_io_mixed    | 567 ms                                                                 | 498 ms: 1.14x faster                                                     |
| async_tree_cpu_io_mixed_tg | 547 ms                                                                 | 481 ms: 1.14x faster                                                     |
| gc_traversal               | 4.62 ms                                                                | 4.18 ms: 1.10x faster                                                    |
| crypto_pyaes               | 68.0 ms                                                                | 65.6 ms: 1.04x faster                                                    |
| logging_format             | 6.78 us                                                                | 6.61 us: 1.03x faster                                                    |
| telco                      | 7.26 ms                                                                | 7.11 ms: 1.02x faster                                                    |
| deepcopy_reduce            | 2.60 us                                                                | 2.56 us: 1.02x faster                                                    |
| nqueens                    | 78.8 ms                                                                | 77.7 ms: 1.01x faster                                                    |
| float                      | 77.2 ms                                                                | 76.1 ms: 1.01x faster                                                    |
| json_loads                 | 26.5 us                                                                | 26.1 us: 1.01x faster                                                    |
| richards                   | 45.3 ms                                                                | 44.7 ms: 1.01x faster                                                    |
| pickle_pure_python         | 314 us                                                                 | 310 us: 1.01x faster                                                     |
| async_tree_io              | 625 ms                                                                 | 618 ms: 1.01x faster                                                     |
| pprint_pformat             | 1.45 sec                                                               | 1.44 sec: 1.01x faster                                                   |
| pyflate                    | 439 ms                                                                 | 435 ms: 1.01x faster                                                     |
| logging_silent             | 106 ns                                                                 | 105 ns: 1.01x faster                                                     |
| comprehensions             | 17.0 us                                                                | 16.8 us: 1.01x faster                                                    |
| richards_super             | 51.3 ms                                                                | 50.9 ms: 1.01x faster                                                    |
| logging_simple             | 5.95 us                                                                | 5.91 us: 1.01x faster                                                    |
| pprint_safe_repr           | 708 ms                                                                 | 703 ms: 1.01x faster                                                     |
| python_startup             | 14.6 ms                                                                | 14.6 ms: 1.00x slower                                                    |
| asyncio_websockets         | 523 ms                                                                 | 523 ms: 1.00x slower                                                     |
| xml_etree_iterparse        | 90.2 ms                                                                | 90.5 ms: 1.00x slower                                                    |
| bench_thread_pool          | 1.03 ms                                                                | 1.03 ms: 1.00x slower                                                    |
| sqlglot_transpile          | 1.57 ms                                                                | 1.58 ms: 1.00x slower                                                    |
| chaos                      | 57.5 ms                                                                | 57.8 ms: 1.01x slower                                                    |
| shortest_path              | 439 ms                                                                 | 441 ms: 1.01x slower                                                     |
| regex_v8                   | 24.5 ms                                                                | 24.7 ms: 1.01x slower                                                    |
| sympy_str                  | 268 ms                                                                 | 269 ms: 1.01x slower                                                     |
| sympy_integrate            | 19.6 ms                                                                | 19.7 ms: 1.01x slower                                                    |
| raytrace                   | 259 ms                                                                 | 260 ms: 1.01x slower                                                     |
| dulwich_log                | 74.8 ms                                                                | 75.3 ms: 1.01x slower                                                    |
| 2to3                       | 253 ms                                                                 | 255 ms: 1.01x slower                                                     |
| json_dumps                 | 11.3 ms                                                                | 11.4 ms: 1.01x slower                                                    |
| async_generators           | 359 ms                                                                 | 362 ms: 1.01x slower                                                     |
| docutils                   | 2.53 sec                                                               | 2.55 sec: 1.01x slower                                                   |
| sphinx                     | 980 ms                                                                 | 988 ms: 1.01x slower                                                     |
| genshi_xml                 | 49.3 ms                                                                | 49.7 ms: 1.01x slower                                                    |
| subparsers                 | 21.5 ms                                                                | 21.7 ms: 1.01x slower                                                    |
| xml_etree_generate         | 82.9 ms                                                                | 83.7 ms: 1.01x slower                                                    |
| sqlglot_normalize          | 103 ms                                                                 | 104 ms: 1.01x slower                                                     |
| connected_components       | 398 ms                                                                 | 402 ms: 1.01x slower                                                     |
| sympy_expand               | 451 ms                                                                 | 455 ms: 1.01x slower                                                     |
| django_template            | 34.6 ms                                                                | 35.0 ms: 1.01x slower                                                    |
| scimark_sparse_mat_mult    | 4.37 ms                                                                | 4.42 ms: 1.01x slower                                                    |
| many_optionals             | 1.01 ms                                                                | 1.02 ms: 1.01x slower                                                    |
| regex_dna                  | 172 ms                                                                 | 174 ms: 1.01x slower                                                     |
| deepcopy                   | 252 us                                                                 | 255 us: 1.01x slower                                                     |
| xml_etree_process          | 57.8 ms                                                                | 58.4 ms: 1.01x slower                                                    |
| regex_compile              | 127 ms                                                                 | 129 ms: 1.01x slower                                                     |
| generators                 | 26.6 ms                                                                | 27.0 ms: 1.01x slower                                                    |
| sqlglot_optimize           | 51.7 ms                                                                | 52.4 ms: 1.01x slower                                                    |
| pycparser                  | 1.12 sec                                                               | 1.13 sec: 1.01x slower                                                   |
| regex_effbot               | 2.68 ms                                                                | 2.72 ms: 1.01x slower                                                    |
| go                         | 117 ms                                                                 | 119 ms: 1.02x slower                                                     |
| unpickle_pure_python       | 208 us                                                                 | 212 us: 1.02x slower                                                     |
| bpe_tokeniser              | 4.23 sec                                                               | 4.31 sec: 1.02x slower                                                   |
| scimark_fft                | 323 ms                                                                 | 330 ms: 1.02x slower                                                     |
| scimark_lu                 | 107 ms                                                                 | 110 ms: 1.02x slower                                                     |
| mako                       | 11.4 ms                                                                | 11.7 ms: 1.03x slower                                                    |
| nbody                      | 89.4 ms                                                                | 91.8 ms: 1.03x slower                                                    |
| coverage                   | 78.1 ms                                                                | 80.3 ms: 1.03x slower                                                    |
| sqlalchemy_declarative     | 126 ms                                                                 | 130 ms: 1.03x slower                                                     |
| sqlalchemy_imperative      | 18.8 ms                                                                | 19.5 ms: 1.03x slower                                                    |
| mdp                        | 2.34 sec                                                               | 2.47 sec: 1.05x slower                                                   |
| coroutines                 | 21.3 ms                                                                | 23.2 ms: 1.09x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (28): async_tree_none, async_tree_memoization, json, pathlib, sqlite_synth, deltablue, bench_mp_pool, create_gc_cycles, xml_etree_parse, async_tree_memoization_tg, hexiom, async_tree_io_tg, genshi_text, tomli_loads, meteor_contest, scimark_monte_carlo, python_startup_no_site, async_tree_none_tg, scimark_sor, spectral_norm, deepcopy_memo, sqlglot_parse, fannkuch, sympy_sum, thrift, typing_runtime_protocols, k_core, pylint

- Geometric mean (including insignificant results): 1.001x faster

# HPT report

- Reliability score: 99.56% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x