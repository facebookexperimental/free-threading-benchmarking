# Results vs. base

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: 956e5d1
- commit date: 2025-04-16
- overall geometric mean: 1.005x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 1.00x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 247 ms                                                                 | 246 ms: 1.01x faster                                                     |
| docutils       | 2.54 sec                                                               | 2.53 sec: 1.01x faster                                                   |
| Geometric mean | (ref)                                                                  | 1.00x faster                                                             |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_generators           | 327 ms                                                                 | 325 ms: 1.01x faster                                                     |
| async_tree_none            | 268 ms                                                                 | 270 ms: 1.01x slower                                                     |
| async_tree_cpu_io_mixed    | 500 ms                                                                 | 507 ms: 1.01x slower                                                     |
| async_tree_none_tg         | 253 ms                                                                 | 257 ms: 1.01x slower                                                     |
| async_tree_cpu_io_mixed_tg | 497 ms                                                                 | 505 ms: 1.02x slower                                                     |
| async_tree_io              | 600 ms                                                                 | 611 ms: 1.02x slower                                                     |
| coroutines                 | 23.2 ms                                                                | 23.7 ms: 1.02x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (4): asyncio_websockets, async_tree_memoization, async_tree_io_tg, async_tree_memoization_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 198 ms                                                                 | 202 ms: 1.02x slower                                                     |
| float          | 69.0 ms                                                                | 70.7 ms: 1.03x slower                                                    |
| nbody          | 85.2 ms                                                                | 88.1 ms: 1.03x slower                                                    |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 22.0 ms                                                                | 21.4 ms: 1.03x faster                                                    |
| regex_effbot   | 2.77 ms                                                                | 2.71 ms: 1.02x faster                                                    |
| regex_compile  | 121 ms                                                                 | 123 ms: 1.02x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.01x faster                                                             |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|---------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pickle_pure_python  | 308 us                                                                 | 302 us: 1.02x faster                                                     |
| xml_etree_iterparse | 93.0 ms                                                                | 92.3 ms: 1.01x faster                                                    |
| tomli_loads         | 1.90 sec                                                               | 1.90 sec: 1.00x slower                                                   |
| json_loads          | 28.5 us                                                                | 28.7 us: 1.01x slower                                                    |
| xml_etree_process   | 59.1 ms                                                                | 59.7 ms: 1.01x slower                                                    |
| xml_etree_generate  | 83.3 ms                                                                | 84.6 ms: 1.02x slower                                                    |
| Geometric mean      | (ref)                                                                  | 1.00x slower                                                             |

Benchmark hidden because not significant (3): json_dumps, unpickle_pure_python, xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 15.1 ms                                                                | 15.0 ms: 1.00x faster                                                    |
| python_startup_no_site | 8.64 ms                                                                | 8.62 ms: 1.00x faster                                                    |
| Geometric mean         | (ref)                                                                  | 1.00x faster                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| mako            | 12.1 ms                                                                | 11.9 ms: 1.01x faster                                                    |
| genshi_text     | 20.3 ms                                                                | 20.5 ms: 1.01x slower                                                    |
| genshi_xml      | 47.7 ms                                                                | 48.7 ms: 1.02x slower                                                    |
| django_template | 34.5 ms                                                                | 35.4 ms: 1.02x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.01x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 4.72 ms                                                                | 4.29 ms: 1.10x faster                                                    |
| generators                 | 28.4 ms                                                                | 27.5 ms: 1.03x faster                                                    |
| regex_v8                   | 22.0 ms                                                                | 21.4 ms: 1.03x faster                                                    |
| regex_effbot               | 2.77 ms                                                                | 2.71 ms: 1.02x faster                                                    |
| pickle_pure_python         | 308 us                                                                 | 302 us: 1.02x faster                                                     |
| coverage                   | 81.7 ms                                                                | 80.5 ms: 1.01x faster                                                    |
| mako                       | 12.1 ms                                                                | 11.9 ms: 1.01x faster                                                    |
| pyflate                    | 401 ms                                                                 | 397 ms: 1.01x faster                                                     |
| pycparser                  | 1.11 sec                                                               | 1.10 sec: 1.01x faster                                                   |
| async_generators           | 327 ms                                                                 | 325 ms: 1.01x faster                                                     |
| xml_etree_iterparse        | 93.0 ms                                                                | 92.3 ms: 1.01x faster                                                    |
| docutils                   | 2.54 sec                                                               | 2.53 sec: 1.01x faster                                                   |
| 2to3                       | 247 ms                                                                 | 246 ms: 1.01x faster                                                     |
| sqlglot_v2_transpile       | 1.51 ms                                                                | 1.50 ms: 1.00x faster                                                    |
| raytrace                   | 248 ms                                                                 | 247 ms: 1.00x faster                                                     |
| python_startup             | 15.1 ms                                                                | 15.0 ms: 1.00x faster                                                    |
| python_startup_no_site     | 8.64 ms                                                                | 8.62 ms: 1.00x faster                                                    |
| bpe_tokeniser              | 4.22 sec                                                               | 4.23 sec: 1.00x slower                                                   |
| richards_super             | 46.3 ms                                                                | 46.4 ms: 1.00x slower                                                    |
| crypto_pyaes               | 67.7 ms                                                                | 68.0 ms: 1.00x slower                                                    |
| tomli_loads                | 1.90 sec                                                               | 1.90 sec: 1.00x slower                                                   |
| sympy_sum                  | 153 ms                                                                 | 154 ms: 1.00x slower                                                     |
| bench_thread_pool          | 1.05 ms                                                                | 1.05 ms: 1.00x slower                                                    |
| sqlglot_v2_normalize       | 98.8 ms                                                                | 99.3 ms: 1.01x slower                                                    |
| mdp                        | 1.13 sec                                                               | 1.13 sec: 1.01x slower                                                   |
| json_loads                 | 28.5 us                                                                | 28.7 us: 1.01x slower                                                    |
| sympy_integrate            | 18.7 ms                                                                | 18.8 ms: 1.01x slower                                                    |
| sqlalchemy_declarative     | 129 ms                                                                 | 130 ms: 1.01x slower                                                     |
| async_tree_none            | 268 ms                                                                 | 270 ms: 1.01x slower                                                     |
| many_optionals             | 1.00 ms                                                                | 1.01 ms: 1.01x slower                                                    |
| pathlib                    | 19.0 ms                                                                | 19.1 ms: 1.01x slower                                                    |
| genshi_text                | 20.3 ms                                                                | 20.5 ms: 1.01x slower                                                    |
| xml_etree_process          | 59.1 ms                                                                | 59.7 ms: 1.01x slower                                                    |
| logging_simple             | 5.92 us                                                                | 5.98 us: 1.01x slower                                                    |
| nqueens                    | 75.8 ms                                                                | 76.7 ms: 1.01x slower                                                    |
| json                       | 5.01 ms                                                                | 5.07 ms: 1.01x slower                                                    |
| go                         | 105 ms                                                                 | 106 ms: 1.01x slower                                                     |
| deepcopy_memo              | 28.8 us                                                                | 29.1 us: 1.01x slower                                                    |
| sympy_expand               | 449 ms                                                                 | 454 ms: 1.01x slower                                                     |
| fannkuch                   | 372 ms                                                                 | 377 ms: 1.01x slower                                                     |
| async_tree_cpu_io_mixed    | 500 ms                                                                 | 507 ms: 1.01x slower                                                     |
| hexiom                     | 5.65 ms                                                                | 5.73 ms: 1.01x slower                                                    |
| async_tree_none_tg         | 253 ms                                                                 | 257 ms: 1.01x slower                                                     |
| typing_runtime_protocols   | 153 us                                                                 | 156 us: 1.01x slower                                                     |
| xml_etree_generate         | 83.3 ms                                                                | 84.6 ms: 1.02x slower                                                    |
| deepcopy_reduce            | 2.56 us                                                                | 2.60 us: 1.02x slower                                                    |
| async_tree_cpu_io_mixed_tg | 497 ms                                                                 | 505 ms: 1.02x slower                                                     |
| subparsers                 | 21.7 ms                                                                | 22.1 ms: 1.02x slower                                                    |
| regex_compile              | 121 ms                                                                 | 123 ms: 1.02x slower                                                     |
| async_tree_io              | 600 ms                                                                 | 611 ms: 1.02x slower                                                     |
| coroutines                 | 23.2 ms                                                                | 23.7 ms: 1.02x slower                                                    |
| chaos                      | 53.0 ms                                                                | 54.0 ms: 1.02x slower                                                    |
| sqlite_synth               | 2.20 us                                                                | 2.24 us: 1.02x slower                                                    |
| scimark_lu                 | 113 ms                                                                 | 115 ms: 1.02x slower                                                     |
| genshi_xml                 | 47.7 ms                                                                | 48.7 ms: 1.02x slower                                                    |
| pidigits                   | 198 ms                                                                 | 202 ms: 1.02x slower                                                     |
| logging_format             | 6.58 us                                                                | 6.73 us: 1.02x slower                                                    |
| deepcopy                   | 246 us                                                                 | 252 us: 1.02x slower                                                     |
| django_template            | 34.5 ms                                                                | 35.4 ms: 1.02x slower                                                    |
| float                      | 69.0 ms                                                                | 70.7 ms: 1.03x slower                                                    |
| scimark_monte_carlo        | 59.8 ms                                                                | 61.5 ms: 1.03x slower                                                    |
| scimark_sparse_mat_mult    | 4.36 ms                                                                | 4.49 ms: 1.03x slower                                                    |
| nbody                      | 85.2 ms                                                                | 88.1 ms: 1.03x slower                                                    |
| spectral_norm              | 92.5 ms                                                                | 95.7 ms: 1.03x slower                                                    |
| logging_silent             | 93.0 ns                                                                | 96.9 ns: 1.04x slower                                                    |
| scimark_fft                | 310 ms                                                                 | 325 ms: 1.05x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.01x slower                                                             |

Benchmark hidden because not significant (28): create_gc_cycles, richards, pprint_safe_repr, json_dumps, pprint_pformat, comprehensions, meteor_contest, unpickle_pure_python, sqlglot_v2_parse, regex_dna, sqlglot_v2_optimize, shortest_path, asyncio_websockets, scimark_sor, sphinx, bench_mp_pool, sqlalchemy_imperative, connected_components, telco, deltablue, sympy_str, dulwich_log, xml_etree_parse, k_core, pylint, async_tree_memoization, async_tree_io_tg, async_tree_memoization_tg

- Geometric mean (including insignificant results): 1.005x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 1.00x