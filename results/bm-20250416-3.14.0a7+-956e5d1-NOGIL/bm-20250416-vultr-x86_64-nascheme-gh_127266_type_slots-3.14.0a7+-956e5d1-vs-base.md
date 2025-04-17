# Results vs. base

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: 956e5d1
- commit date: 2025-04-16
- overall geometric mean: 1.003x faster
- HPT reliability: 99.48%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| docutils       | 2.68 sec                                                               | 2.69 sec: 1.00x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (3): 2to3, html5lib, sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| coroutines                 | 22.6 ms                                                                | 21.8 ms: 1.04x faster                                                    |
| async_generators           | 364 ms                                                                 | 361 ms: 1.01x faster                                                     |
| async_tree_io_tg           | 520 ms                                                                 | 516 ms: 1.01x faster                                                     |
| async_tree_io              | 544 ms                                                                 | 539 ms: 1.01x faster                                                     |
| async_tree_cpu_io_mixed    | 494 ms                                                                 | 540 ms: 1.09x slower                                                     |
| async_tree_cpu_io_mixed_tg | 467 ms                                                                 | 516 ms: 1.10x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (5): async_tree_none, async_tree_memoization_tg, async_tree_memoization, async_tree_none_tg, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| nbody          | 111 ms                                                                 | 109 ms: 1.02x faster                                                     |
| float          | 67.2 ms                                                                | 67.3 ms: 1.00x slower                                                    |
| pidigits       | 191 ms                                                                 | 235 ms: 1.23x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna      | 187 ms                                                                 | 177 ms: 1.05x faster                                                     |
| regex_effbot   | 2.84 ms                                                                | 2.75 ms: 1.03x faster                                                    |
| regex_v8       | 21.0 ms                                                                | 20.3 ms: 1.03x faster                                                    |
| regex_compile  | 142 ms                                                                 | 143 ms: 1.00x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.03x faster                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| json_loads           | 30.7 us                                                                | 29.8 us: 1.03x faster                                                    |
| json_dumps           | 12.7 ms                                                                | 12.5 ms: 1.01x faster                                                    |
| tomli_loads          | 2.10 sec                                                               | 2.08 sec: 1.01x faster                                                   |
| xml_etree_generate   | 92.9 ms                                                                | 92.2 ms: 1.01x faster                                                    |
| xml_etree_parse      | 129 ms                                                                 | 128 ms: 1.01x faster                                                     |
| unpickle_pure_python | 227 us                                                                 | 227 us: 1.00x slower                                                     |
| xml_etree_iterparse  | 86.9 ms                                                                | 87.4 ms: 1.01x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (2): xml_etree_process, pickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup_no_site | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                    |
| python_startup         | 15.9 ms                                                                | 15.8 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 15.3 ms                                                                | 15.0 ms: 1.02x faster                                                    |
| genshi_xml      | 55.2 ms                                                                | 54.3 ms: 1.02x faster                                                    |
| genshi_text     | 26.0 ms                                                                | 25.6 ms: 1.02x faster                                                    |
| django_template | 39.7 ms                                                                | 39.9 ms: 1.01x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x faster                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_dna                  | 187 ms                                                                 | 177 ms: 1.05x faster                                                     |
| scimark_sparse_mat_mult    | 5.15 ms                                                                | 4.90 ms: 1.05x faster                                                    |
| json                       | 5.29 ms                                                                | 5.03 ms: 1.05x faster                                                    |
| scimark_fft                | 348 ms                                                                 | 334 ms: 1.04x faster                                                     |
| pyflate                    | 473 ms                                                                 | 455 ms: 1.04x faster                                                     |
| coroutines                 | 22.6 ms                                                                | 21.8 ms: 1.04x faster                                                    |
| regex_effbot               | 2.84 ms                                                                | 2.75 ms: 1.03x faster                                                    |
| regex_v8                   | 21.0 ms                                                                | 20.3 ms: 1.03x faster                                                    |
| json_loads                 | 30.7 us                                                                | 29.8 us: 1.03x faster                                                    |
| generators                 | 31.9 ms                                                                | 31.1 ms: 1.02x faster                                                    |
| telco                      | 8.37 ms                                                                | 8.18 ms: 1.02x faster                                                    |
| spectral_norm              | 105 ms                                                                 | 103 ms: 1.02x faster                                                     |
| nbody                      | 111 ms                                                                 | 109 ms: 1.02x faster                                                     |
| mako                       | 15.3 ms                                                                | 15.0 ms: 1.02x faster                                                    |
| scimark_sor                | 122 ms                                                                 | 119 ms: 1.02x faster                                                     |
| sympy_expand               | 525 ms                                                                 | 516 ms: 1.02x faster                                                     |
| chaos                      | 60.9 ms                                                                | 59.8 ms: 1.02x faster                                                    |
| genshi_xml                 | 55.2 ms                                                                | 54.3 ms: 1.02x faster                                                    |
| genshi_text                | 26.0 ms                                                                | 25.6 ms: 1.02x faster                                                    |
| deltablue                  | 3.56 ms                                                                | 3.50 ms: 1.02x faster                                                    |
| json_dumps                 | 12.7 ms                                                                | 12.5 ms: 1.01x faster                                                    |
| logging_format             | 7.80 us                                                                | 7.68 us: 1.01x faster                                                    |
| nqueens                    | 87.0 ms                                                                | 86.0 ms: 1.01x faster                                                    |
| sqlite_synth               | 2.00 us                                                                | 1.98 us: 1.01x faster                                                    |
| scimark_monte_carlo        | 73.8 ms                                                                | 73.1 ms: 1.01x faster                                                    |
| sympy_sum                  | 179 ms                                                                 | 177 ms: 1.01x faster                                                     |
| async_generators           | 364 ms                                                                 | 361 ms: 1.01x faster                                                     |
| tomli_loads                | 2.10 sec                                                               | 2.08 sec: 1.01x faster                                                   |
| subparsers                 | 24.4 ms                                                                | 24.2 ms: 1.01x faster                                                    |
| go                         | 124 ms                                                                 | 123 ms: 1.01x faster                                                     |
| async_tree_io_tg           | 520 ms                                                                 | 516 ms: 1.01x faster                                                     |
| bpe_tokeniser              | 4.47 sec                                                               | 4.44 sec: 1.01x faster                                                   |
| async_tree_io              | 544 ms                                                                 | 539 ms: 1.01x faster                                                     |
| mdp                        | 1.31 sec                                                               | 1.30 sec: 1.01x faster                                                   |
| raytrace                   | 289 ms                                                                 | 287 ms: 1.01x faster                                                     |
| fannkuch                   | 457 ms                                                                 | 454 ms: 1.01x faster                                                     |
| xml_etree_generate         | 92.9 ms                                                                | 92.2 ms: 1.01x faster                                                    |
| deepcopy                   | 291 us                                                                 | 290 us: 1.01x faster                                                     |
| xml_etree_parse            | 129 ms                                                                 | 128 ms: 1.01x faster                                                     |
| python_startup_no_site     | 11.2 ms                                                                | 11.1 ms: 1.01x faster                                                    |
| bench_mp_pool              | 95.7 ms                                                                | 95.2 ms: 1.01x faster                                                    |
| crypto_pyaes               | 82.3 ms                                                                | 81.9 ms: 1.00x faster                                                    |
| hexiom                     | 6.63 ms                                                                | 6.60 ms: 1.00x faster                                                    |
| deepcopy_reduce            | 2.96 us                                                                | 2.95 us: 1.00x faster                                                    |
| python_startup             | 15.9 ms                                                                | 15.8 ms: 1.00x faster                                                    |
| unpickle_pure_python       | 227 us                                                                 | 227 us: 1.00x slower                                                     |
| regex_compile              | 142 ms                                                                 | 143 ms: 1.00x slower                                                     |
| pprint_pformat             | 1.57 sec                                                               | 1.57 sec: 1.00x slower                                                   |
| float                      | 67.2 ms                                                                | 67.3 ms: 1.00x slower                                                    |
| comprehensions             | 19.3 us                                                                | 19.4 us: 1.00x slower                                                    |
| k_core                     | 2.22 sec                                                               | 2.23 sec: 1.00x slower                                                   |
| docutils                   | 2.68 sec                                                               | 2.69 sec: 1.00x slower                                                   |
| gc_traversal               | 1.79 ms                                                                | 1.79 ms: 1.00x slower                                                    |
| django_template            | 39.7 ms                                                                | 39.9 ms: 1.01x slower                                                    |
| xml_etree_iterparse        | 86.9 ms                                                                | 87.4 ms: 1.01x slower                                                    |
| create_gc_cycles           | 1.36 ms                                                                | 1.37 ms: 1.01x slower                                                    |
| coverage                   | 107 ms                                                                 | 108 ms: 1.01x slower                                                     |
| scimark_lu                 | 130 ms                                                                 | 131 ms: 1.01x slower                                                     |
| dulwich_log                | 70.4 ms                                                                | 71.1 ms: 1.01x slower                                                    |
| sqlglot_v2_optimize        | 57.0 ms                                                                | 57.6 ms: 1.01x slower                                                    |
| many_optionals             | 1.10 ms                                                                | 1.11 ms: 1.01x slower                                                    |
| sqlglot_v2_normalize       | 112 ms                                                                 | 113 ms: 1.01x slower                                                     |
| pathlib                    | 19.1 ms                                                                | 19.4 ms: 1.02x slower                                                    |
| logging_silent             | 100 ns                                                                 | 103 ns: 1.03x slower                                                     |
| async_tree_cpu_io_mixed    | 494 ms                                                                 | 540 ms: 1.09x slower                                                     |
| async_tree_cpu_io_mixed_tg | 467 ms                                                                 | 516 ms: 1.10x slower                                                     |
| pidigits                   | 191 ms                                                                 | 235 ms: 1.23x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (28): async_tree_none, typing_runtime_protocols, async_tree_memoization_tg, logging_simple, sympy_str, async_tree_memoization, richards, deepcopy_memo, sympy_integrate, richards_super, html5lib, async_tree_none_tg, sqlalchemy_declarative, pprint_safe_repr, xml_etree_process, pylint, sphinx, sqlglot_v2_transpile, connected_components, 2to3, sqlglot_v2_parse, bench_thread_pool, asyncio_websockets, shortest_path, pycparser, pickle_pure_python, meteor_contest, sqlalchemy_imperative

- Geometric mean (including insignificant results): 1.003x faster

# HPT report

- Reliability score: 99.48% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.00x