# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: 956e5d1
- commit date: 2025-04-16
- overall geometric mean: 1.080x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 247 ms                                                                 | 280 ms: 1.13x slower                                                     |
| docutils       | 2.54 sec                                                               | 2.69 sec: 1.06x slower                                                   |
| sphinx         | 975 ms                                                                 | 1.06 sec: 1.09x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 601 ms                                                                 | 516 ms: 1.16x faster                                                     |
| async_tree_none_tg         | 253 ms                                                                 | 223 ms: 1.13x faster                                                     |
| async_tree_io              | 600 ms                                                                 | 539 ms: 1.11x faster                                                     |
| async_tree_memoization_tg  | 311 ms                                                                 | 282 ms: 1.11x faster                                                     |
| coroutines                 | 23.2 ms                                                                | 21.8 ms: 1.07x faster                                                    |
| async_tree_none            | 268 ms                                                                 | 253 ms: 1.06x faster                                                     |
| async_tree_cpu_io_mixed_tg | 497 ms                                                                 | 516 ms: 1.04x slower                                                     |
| async_tree_cpu_io_mixed    | 500 ms                                                                 | 540 ms: 1.08x slower                                                     |
| async_generators           | 327 ms                                                                 | 361 ms: 1.10x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                             |

Benchmark hidden because not significant (2): async_tree_memoization, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 69.0 ms                                                                | 67.3 ms: 1.02x faster                                                    |
| pidigits       | 198 ms                                                                 | 235 ms: 1.19x slower                                                     |
| nbody          | 85.2 ms                                                                | 109 ms: 1.28x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 22.0 ms                                                                | 20.3 ms: 1.09x faster                                                    |
| regex_effbot   | 2.77 ms                                                                | 2.75 ms: 1.01x faster                                                    |
| regex_dna      | 174 ms                                                                 | 177 ms: 1.02x slower                                                     |
| regex_compile  | 121 ms                                                                 | 143 ms: 1.18x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.0 ms                                                                | 87.4 ms: 1.06x faster                                                    |
| xml_etree_parse      | 131 ms                                                                 | 128 ms: 1.02x faster                                                     |
| json_loads           | 28.5 us                                                                | 29.8 us: 1.05x slower                                                    |
| pickle_pure_python   | 308 us                                                                 | 325 us: 1.06x slower                                                     |
| unpickle_pure_python | 209 us                                                                 | 227 us: 1.09x slower                                                     |
| json_dumps           | 11.4 ms                                                                | 12.5 ms: 1.10x slower                                                    |
| tomli_loads          | 1.90 sec                                                               | 2.08 sec: 1.10x slower                                                   |
| xml_etree_generate   | 83.3 ms                                                                | 92.2 ms: 1.11x slower                                                    |
| xml_etree_process    | 59.1 ms                                                                | 66.0 ms: 1.12x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.06x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 15.1 ms                                                                | 15.8 ms: 1.05x slower                                                    |
| python_startup_no_site | 8.64 ms                                                                | 11.1 ms: 1.29x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 47.7 ms                                                                | 54.3 ms: 1.14x slower                                                    |
| django_template | 34.5 ms                                                                | 39.9 ms: 1.15x slower                                                    |
| mako            | 12.1 ms                                                                | 15.0 ms: 1.25x slower                                                    |
| genshi_text     | 20.3 ms                                                                | 25.6 ms: 1.26x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.20x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20250417-vultr-x86_64-python-39ee468e092eed659bfc-3.14.0a7+-39ee468 | bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 4.72 ms                                                                | 1.79 ms: 2.63x faster                                                    |
| create_gc_cycles           | 1.85 ms                                                                | 1.37 ms: 1.35x faster                                                    |
| async_tree_io_tg           | 601 ms                                                                 | 516 ms: 1.16x faster                                                     |
| async_tree_none_tg         | 253 ms                                                                 | 223 ms: 1.13x faster                                                     |
| async_tree_io              | 600 ms                                                                 | 539 ms: 1.11x faster                                                     |
| sqlite_synth               | 2.20 us                                                                | 1.98 us: 1.11x faster                                                    |
| async_tree_memoization_tg  | 311 ms                                                                 | 282 ms: 1.11x faster                                                     |
| regex_v8                   | 22.0 ms                                                                | 20.3 ms: 1.09x faster                                                    |
| coroutines                 | 23.2 ms                                                                | 21.8 ms: 1.07x faster                                                    |
| xml_etree_iterparse        | 93.0 ms                                                                | 87.4 ms: 1.06x faster                                                    |
| async_tree_none            | 268 ms                                                                 | 253 ms: 1.06x faster                                                     |
| float                      | 69.0 ms                                                                | 67.3 ms: 1.02x faster                                                    |
| xml_etree_parse            | 131 ms                                                                 | 128 ms: 1.02x faster                                                     |
| regex_effbot               | 2.77 ms                                                                | 2.75 ms: 1.01x faster                                                    |
| pycparser                  | 1.11 sec                                                               | 1.13 sec: 1.02x slower                                                   |
| regex_dna                  | 174 ms                                                                 | 177 ms: 1.02x slower                                                     |
| pathlib                    | 19.0 ms                                                                | 19.4 ms: 1.02x slower                                                    |
| async_tree_cpu_io_mixed_tg | 497 ms                                                                 | 516 ms: 1.04x slower                                                     |
| json_loads                 | 28.5 us                                                                | 29.8 us: 1.05x slower                                                    |
| python_startup             | 15.1 ms                                                                | 15.8 ms: 1.05x slower                                                    |
| bpe_tokeniser              | 4.22 sec                                                               | 4.44 sec: 1.05x slower                                                   |
| dulwich_log                | 67.5 ms                                                                | 71.1 ms: 1.05x slower                                                    |
| pickle_pure_python         | 308 us                                                                 | 325 us: 1.06x slower                                                     |
| docutils                   | 2.54 sec                                                               | 2.69 sec: 1.06x slower                                                   |
| scimark_fft                | 310 ms                                                                 | 334 ms: 1.07x slower                                                     |
| async_tree_cpu_io_mixed    | 500 ms                                                                 | 540 ms: 1.08x slower                                                     |
| pprint_safe_repr           | 703 ms                                                                 | 763 ms: 1.09x slower                                                     |
| bench_mp_pool              | 87.6 ms                                                                | 95.2 ms: 1.09x slower                                                    |
| sphinx                     | 975 ms                                                                 | 1.06 sec: 1.09x slower                                                   |
| unpickle_pure_python       | 209 us                                                                 | 227 us: 1.09x slower                                                     |
| deltablue                  | 3.21 ms                                                                | 3.50 ms: 1.09x slower                                                    |
| json_dumps                 | 11.4 ms                                                                | 12.5 ms: 1.10x slower                                                    |
| pylint                     | 278 ms                                                                 | 304 ms: 1.10x slower                                                     |
| generators                 | 28.4 ms                                                                | 31.1 ms: 1.10x slower                                                    |
| tomli_loads                | 1.90 sec                                                               | 2.08 sec: 1.10x slower                                                   |
| pprint_pformat             | 1.43 sec                                                               | 1.57 sec: 1.10x slower                                                   |
| async_generators           | 327 ms                                                                 | 361 ms: 1.10x slower                                                     |
| scimark_sor                | 108 ms                                                                 | 119 ms: 1.10x slower                                                     |
| k_core                     | 2.02 sec                                                               | 2.23 sec: 1.10x slower                                                   |
| xml_etree_generate         | 83.3 ms                                                                | 92.2 ms: 1.11x slower                                                    |
| many_optionals             | 1.00 ms                                                                | 1.11 ms: 1.11x slower                                                    |
| logging_silent             | 93.0 ns                                                                | 103 ns: 1.11x slower                                                     |
| spectral_norm              | 92.5 ms                                                                | 103 ms: 1.11x slower                                                     |
| subparsers                 | 21.7 ms                                                                | 24.2 ms: 1.11x slower                                                    |
| xml_etree_process          | 59.1 ms                                                                | 66.0 ms: 1.12x slower                                                    |
| scimark_sparse_mat_mult    | 4.36 ms                                                                | 4.90 ms: 1.12x slower                                                    |
| chaos                      | 53.0 ms                                                                | 59.8 ms: 1.13x slower                                                    |
| telco                      | 7.22 ms                                                                | 8.18 ms: 1.13x slower                                                    |
| nqueens                    | 75.8 ms                                                                | 86.0 ms: 1.13x slower                                                    |
| pyflate                    | 401 ms                                                                 | 455 ms: 1.13x slower                                                     |
| 2to3                       | 247 ms                                                                 | 280 ms: 1.13x slower                                                     |
| genshi_xml                 | 47.7 ms                                                                | 54.3 ms: 1.14x slower                                                    |
| sqlglot_v2_optimize        | 50.2 ms                                                                | 57.6 ms: 1.15x slower                                                    |
| sqlglot_v2_normalize       | 98.8 ms                                                                | 113 ms: 1.15x slower                                                     |
| sympy_expand               | 449 ms                                                                 | 516 ms: 1.15x slower                                                     |
| deepcopy_reduce            | 2.56 us                                                                | 2.95 us: 1.15x slower                                                    |
| django_template            | 34.5 ms                                                                | 39.9 ms: 1.15x slower                                                    |
| logging_simple             | 5.92 us                                                                | 6.84 us: 1.15x slower                                                    |
| mdp                        | 1.13 sec                                                               | 1.30 sec: 1.16x slower                                                   |
| sympy_sum                  | 153 ms                                                                 | 177 ms: 1.16x slower                                                     |
| raytrace                   | 248 ms                                                                 | 287 ms: 1.16x slower                                                     |
| scimark_lu                 | 113 ms                                                                 | 131 ms: 1.17x slower                                                     |
| sympy_str                  | 268 ms                                                                 | 312 ms: 1.17x slower                                                     |
| sqlglot_v2_transpile       | 1.51 ms                                                                | 1.76 ms: 1.17x slower                                                    |
| logging_format             | 6.58 us                                                                | 7.68 us: 1.17x slower                                                    |
| hexiom                     | 5.65 ms                                                                | 6.60 ms: 1.17x slower                                                    |
| sympy_integrate            | 18.7 ms                                                                | 21.9 ms: 1.17x slower                                                    |
| regex_compile              | 121 ms                                                                 | 143 ms: 1.18x slower                                                     |
| deepcopy                   | 246 us                                                                 | 290 us: 1.18x slower                                                     |
| go                         | 105 ms                                                                 | 123 ms: 1.18x slower                                                     |
| sqlalchemy_declarative     | 129 ms                                                                 | 152 ms: 1.18x slower                                                     |
| comprehensions             | 16.4 us                                                                | 19.4 us: 1.18x slower                                                    |
| pidigits                   | 198 ms                                                                 | 235 ms: 1.19x slower                                                     |
| sqlalchemy_imperative      | 19.6 ms                                                                | 23.4 ms: 1.19x slower                                                    |
| deepcopy_memo              | 28.8 us                                                                | 34.5 us: 1.20x slower                                                    |
| sqlglot_v2_parse           | 1.21 ms                                                                | 1.45 ms: 1.20x slower                                                    |
| crypto_pyaes               | 67.7 ms                                                                | 81.9 ms: 1.21x slower                                                    |
| shortest_path              | 436 ms                                                                 | 529 ms: 1.21x slower                                                     |
| fannkuch                   | 372 ms                                                                 | 454 ms: 1.22x slower                                                     |
| scimark_monte_carlo        | 59.8 ms                                                                | 73.1 ms: 1.22x slower                                                    |
| connected_components       | 394 ms                                                                 | 482 ms: 1.22x slower                                                     |
| richards                   | 40.5 ms                                                                | 49.7 ms: 1.23x slower                                                    |
| typing_runtime_protocols   | 153 us                                                                 | 189 us: 1.23x slower                                                     |
| richards_super             | 46.3 ms                                                                | 57.4 ms: 1.24x slower                                                    |
| mako                       | 12.1 ms                                                                | 15.0 ms: 1.25x slower                                                    |
| genshi_text                | 20.3 ms                                                                | 25.6 ms: 1.26x slower                                                    |
| meteor_contest             | 100 ms                                                                 | 126 ms: 1.26x slower                                                     |
| nbody                      | 85.2 ms                                                                | 109 ms: 1.28x slower                                                     |
| python_startup_no_site     | 8.64 ms                                                                | 11.1 ms: 1.29x slower                                                    |
| coverage                   | 81.7 ms                                                                | 108 ms: 1.33x slower                                                     |
| bench_thread_pool          | 1.05 ms                                                                | 3.13 ms: 3.00x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.10x slower                                                             |

Benchmark hidden because not significant (3): async_tree_memoization, asyncio_websockets, json
Ignored benchmarks (1) of results/bm-20250416-3.14.0a7+-956e5d1-NOGIL/bm-20250416-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-956e5d1.json: html5lib

- Geometric mean (including insignificant results): 1.080x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.20x