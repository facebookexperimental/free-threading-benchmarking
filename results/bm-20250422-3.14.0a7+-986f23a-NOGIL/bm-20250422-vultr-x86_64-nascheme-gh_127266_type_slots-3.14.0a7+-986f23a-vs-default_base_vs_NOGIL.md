# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: gh_127266_type_slots
- machine: linux-x86_64
- commit hash: 986f23a
- commit date: 2025-04-22
- overall geometric mean: 1.080x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250422-vultr-x86_64-python-b5bf8c80a921679b2354-3.14.0a7+-b5bf8c8 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 246 ms                                                                 | 281 ms: 1.14x slower                                                     |
| docutils       | 2.52 sec                                                               | 2.70 sec: 1.07x slower                                                   |
| sphinx         | 970 ms                                                                 | 1.07 sec: 1.10x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.11x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250422-vultr-x86_64-python-b5bf8c80a921679b2354-3.14.0a7+-b5bf8c8 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_io_tg           | 601 ms                                                                 | 519 ms: 1.16x faster                                                     |
| async_tree_none_tg         | 254 ms                                                                 | 227 ms: 1.12x faster                                                     |
| async_tree_memoization_tg  | 313 ms                                                                 | 284 ms: 1.10x faster                                                     |
| async_tree_io              | 604 ms                                                                 | 551 ms: 1.10x faster                                                     |
| async_tree_cpu_io_mixed_tg | 508 ms                                                                 | 468 ms: 1.09x faster                                                     |
| coroutines                 | 23.9 ms                                                                | 22.8 ms: 1.05x faster                                                    |
| async_tree_none            | 268 ms                                                                 | 259 ms: 1.04x faster                                                     |
| async_tree_cpu_io_mixed    | 504 ms                                                                 | 494 ms: 1.02x faster                                                     |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                                     |
| async_tree_memoization     | 306 ms                                                                 | 311 ms: 1.02x slower                                                     |
| async_generators           | 330 ms                                                                 | 358 ms: 1.08x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.05x faster                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250422-vultr-x86_64-python-b5bf8c80a921679b2354-3.14.0a7+-b5bf8c8 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 202 ms                                                                 | 186 ms: 1.09x faster                                                     |
| float          | 69.1 ms                                                                | 67.2 ms: 1.03x faster                                                    |
| nbody          | 86.4 ms                                                                | 110 ms: 1.27x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250422-vultr-x86_64-python-b5bf8c80a921679b2354-3.14.0a7+-b5bf8c8 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 21.9 ms                                                                | 21.0 ms: 1.04x faster                                                    |
| regex_dna      | 182 ms                                                                 | 180 ms: 1.01x faster                                                     |
| regex_effbot   | 2.78 ms                                                                | 2.78 ms: 1.00x faster                                                    |
| regex_compile  | 122 ms                                                                 | 143 ms: 1.18x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.03x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250422-vultr-x86_64-python-b5bf8c80a921679b2354-3.14.0a7+-b5bf8c8 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.7 ms                                                                | 86.8 ms: 1.06x faster                                                    |
| xml_etree_parse      | 132 ms                                                                 | 129 ms: 1.02x faster                                                     |
| json_loads           | 27.9 us                                                                | 29.4 us: 1.05x slower                                                    |
| unpickle_pure_python | 210 us                                                                 | 228 us: 1.09x slower                                                     |
| pickle_pure_python   | 300 us                                                                 | 326 us: 1.09x slower                                                     |
| tomli_loads          | 1.87 sec                                                               | 2.07 sec: 1.11x slower                                                   |
| json_dumps           | 11.3 ms                                                                | 12.6 ms: 1.11x slower                                                    |
| xml_etree_generate   | 81.8 ms                                                                | 93.3 ms: 1.14x slower                                                    |
| xml_etree_process    | 57.4 ms                                                                | 66.6 ms: 1.16x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.07x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250422-vultr-x86_64-python-b5bf8c80a921679b2354-3.14.0a7+-b5bf8c8 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 15.1 ms                                                                | 15.8 ms: 1.05x slower                                                    |
| python_startup_no_site | 8.63 ms                                                                | 11.1 ms: 1.29x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250422-vultr-x86_64-python-b5bf8c80a921679b2354-3.14.0a7+-b5bf8c8 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 48.9 ms                                                                | 55.4 ms: 1.13x slower                                                    |
| django_template | 34.4 ms                                                                | 40.4 ms: 1.18x slower                                                    |
| genshi_text     | 20.6 ms                                                                | 25.8 ms: 1.25x slower                                                    |
| mako            | 11.9 ms                                                                | 15.2 ms: 1.28x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.21x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20250422-vultr-x86_64-python-b5bf8c80a921679b2354-3.14.0a7+-b5bf8c8 | bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 4.24 ms                                                                | 1.79 ms: 2.36x faster                                                    |
| create_gc_cycles           | 1.86 ms                                                                | 1.37 ms: 1.36x faster                                                    |
| async_tree_io_tg           | 601 ms                                                                 | 519 ms: 1.16x faster                                                     |
| async_tree_none_tg         | 254 ms                                                                 | 227 ms: 1.12x faster                                                     |
| sqlite_synth               | 2.21 us                                                                | 1.99 us: 1.11x faster                                                    |
| async_tree_memoization_tg  | 313 ms                                                                 | 284 ms: 1.10x faster                                                     |
| async_tree_io              | 604 ms                                                                 | 551 ms: 1.10x faster                                                     |
| pidigits                   | 202 ms                                                                 | 186 ms: 1.09x faster                                                     |
| async_tree_cpu_io_mixed_tg | 508 ms                                                                 | 468 ms: 1.09x faster                                                     |
| xml_etree_iterparse        | 91.7 ms                                                                | 86.8 ms: 1.06x faster                                                    |
| coroutines                 | 23.9 ms                                                                | 22.8 ms: 1.05x faster                                                    |
| regex_v8                   | 21.9 ms                                                                | 21.0 ms: 1.04x faster                                                    |
| async_tree_none            | 268 ms                                                                 | 259 ms: 1.04x faster                                                     |
| float                      | 69.1 ms                                                                | 67.2 ms: 1.03x faster                                                    |
| xml_etree_parse            | 132 ms                                                                 | 129 ms: 1.02x faster                                                     |
| async_tree_cpu_io_mixed    | 504 ms                                                                 | 494 ms: 1.02x faster                                                     |
| regex_dna                  | 182 ms                                                                 | 180 ms: 1.01x faster                                                     |
| asyncio_websockets         | 517 ms                                                                 | 516 ms: 1.00x faster                                                     |
| regex_effbot               | 2.78 ms                                                                | 2.78 ms: 1.00x faster                                                    |
| json                       | 4.93 ms                                                                | 5.00 ms: 1.02x slower                                                    |
| async_tree_memoization     | 306 ms                                                                 | 311 ms: 1.02x slower                                                     |
| pathlib                    | 19.0 ms                                                                | 19.4 ms: 1.02x slower                                                    |
| pycparser                  | 1.09 sec                                                               | 1.13 sec: 1.04x slower                                                   |
| dulwich_log                | 67.8 ms                                                                | 70.6 ms: 1.04x slower                                                    |
| python_startup             | 15.1 ms                                                                | 15.8 ms: 1.05x slower                                                    |
| json_loads                 | 27.9 us                                                                | 29.4 us: 1.05x slower                                                    |
| bpe_tokeniser              | 4.12 sec                                                               | 4.34 sec: 1.05x slower                                                   |
| logging_silent             | 96.2 ns                                                                | 102 ns: 1.06x slower                                                     |
| scimark_fft                | 316 ms                                                                 | 335 ms: 1.06x slower                                                     |
| scimark_sor                | 112 ms                                                                 | 119 ms: 1.06x slower                                                     |
| spectral_norm              | 96.0 ms                                                                | 102 ms: 1.07x slower                                                     |
| docutils                   | 2.52 sec                                                               | 2.70 sec: 1.07x slower                                                   |
| generators                 | 27.9 ms                                                                | 30.1 ms: 1.08x slower                                                    |
| deltablue                  | 3.26 ms                                                                | 3.52 ms: 1.08x slower                                                    |
| async_generators           | 330 ms                                                                 | 358 ms: 1.08x slower                                                     |
| bench_mp_pool              | 88.3 ms                                                                | 96.0 ms: 1.09x slower                                                    |
| unpickle_pure_python       | 210 us                                                                 | 228 us: 1.09x slower                                                     |
| pickle_pure_python         | 300 us                                                                 | 326 us: 1.09x slower                                                     |
| scimark_sparse_mat_mult    | 4.56 ms                                                                | 5.01 ms: 1.10x slower                                                    |
| many_optionals             | 1.01 ms                                                                | 1.11 ms: 1.10x slower                                                    |
| pprint_safe_repr           | 694 ms                                                                 | 764 ms: 1.10x slower                                                     |
| pylint                     | 277 ms                                                                 | 306 ms: 1.10x slower                                                     |
| sphinx                     | 970 ms                                                                 | 1.07 sec: 1.10x slower                                                   |
| k_core                     | 2.02 sec                                                               | 2.23 sec: 1.10x slower                                                   |
| tomli_loads                | 1.87 sec                                                               | 2.07 sec: 1.11x slower                                                   |
| json_dumps                 | 11.3 ms                                                                | 12.6 ms: 1.11x slower                                                    |
| pprint_pformat             | 1.42 sec                                                               | 1.59 sec: 1.12x slower                                                   |
| chaos                      | 54.0 ms                                                                | 61.0 ms: 1.13x slower                                                    |
| pyflate                    | 406 ms                                                                 | 459 ms: 1.13x slower                                                     |
| genshi_xml                 | 48.9 ms                                                                | 55.4 ms: 1.13x slower                                                    |
| subparsers                 | 21.7 ms                                                                | 24.6 ms: 1.13x slower                                                    |
| nqueens                    | 76.6 ms                                                                | 87.2 ms: 1.14x slower                                                    |
| 2to3                       | 246 ms                                                                 | 281 ms: 1.14x slower                                                     |
| xml_etree_generate         | 81.8 ms                                                                | 93.3 ms: 1.14x slower                                                    |
| telco                      | 7.41 ms                                                                | 8.49 ms: 1.15x slower                                                    |
| go                         | 108 ms                                                                 | 124 ms: 1.15x slower                                                     |
| deepcopy_reduce            | 2.61 us                                                                | 3.02 us: 1.16x slower                                                    |
| comprehensions             | 16.7 us                                                                | 19.3 us: 1.16x slower                                                    |
| hexiom                     | 5.65 ms                                                                | 6.55 ms: 1.16x slower                                                    |
| xml_etree_process          | 57.4 ms                                                                | 66.6 ms: 1.16x slower                                                    |
| mdp                        | 1.12 sec                                                               | 1.31 sec: 1.16x slower                                                   |
| sqlglot_v2_normalize       | 98.7 ms                                                                | 115 ms: 1.16x slower                                                     |
| raytrace                   | 248 ms                                                                 | 288 ms: 1.16x slower                                                     |
| sqlglot_v2_optimize        | 49.6 ms                                                                | 58.0 ms: 1.17x slower                                                    |
| deepcopy                   | 248 us                                                                 | 290 us: 1.17x slower                                                     |
| sympy_sum                  | 151 ms                                                                 | 177 ms: 1.17x slower                                                     |
| sympy_expand               | 447 ms                                                                 | 525 ms: 1.17x slower                                                     |
| scimark_lu                 | 110 ms                                                                 | 130 ms: 1.18x slower                                                     |
| django_template            | 34.4 ms                                                                | 40.4 ms: 1.18x slower                                                    |
| regex_compile              | 122 ms                                                                 | 143 ms: 1.18x slower                                                     |
| sympy_str                  | 265 ms                                                                 | 313 ms: 1.18x slower                                                     |
| logging_format             | 6.57 us                                                                | 7.78 us: 1.18x slower                                                    |
| sqlglot_v2_transpile       | 1.50 ms                                                                | 1.78 ms: 1.19x slower                                                    |
| sqlalchemy_imperative      | 19.7 ms                                                                | 23.4 ms: 1.19x slower                                                    |
| sympy_integrate            | 18.6 ms                                                                | 22.1 ms: 1.19x slower                                                    |
| sqlalchemy_declarative     | 128 ms                                                                 | 153 ms: 1.19x slower                                                     |
| fannkuch                   | 380 ms                                                                 | 452 ms: 1.19x slower                                                     |
| logging_simple             | 5.84 us                                                                | 6.96 us: 1.19x slower                                                    |
| scimark_monte_carlo        | 61.6 ms                                                                | 73.4 ms: 1.19x slower                                                    |
| deepcopy_memo              | 28.9 us                                                                | 34.8 us: 1.20x slower                                                    |
| typing_runtime_protocols   | 156 us                                                                 | 188 us: 1.21x slower                                                     |
| shortest_path              | 435 ms                                                                 | 527 ms: 1.21x slower                                                     |
| sqlglot_v2_parse           | 1.21 ms                                                                | 1.47 ms: 1.22x slower                                                    |
| richards                   | 40.8 ms                                                                | 49.7 ms: 1.22x slower                                                    |
| connected_components       | 392 ms                                                                 | 479 ms: 1.22x slower                                                     |
| crypto_pyaes               | 66.9 ms                                                                | 81.8 ms: 1.22x slower                                                    |
| richards_super             | 46.5 ms                                                                | 57.3 ms: 1.23x slower                                                    |
| meteor_contest             | 102 ms                                                                 | 126 ms: 1.24x slower                                                     |
| genshi_text                | 20.6 ms                                                                | 25.8 ms: 1.25x slower                                                    |
| nbody                      | 86.4 ms                                                                | 110 ms: 1.27x slower                                                     |
| mako                       | 11.9 ms                                                                | 15.2 ms: 1.28x slower                                                    |
| python_startup_no_site     | 8.63 ms                                                                | 11.1 ms: 1.29x slower                                                    |
| coverage                   | 81.2 ms                                                                | 110 ms: 1.35x slower                                                     |
| bench_thread_pool          | 1.05 ms                                                                | 3.13 ms: 2.99x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.10x slower                                                             |
Ignored benchmarks (1) of results/bm-20250422-3.14.0a7+-986f23a-NOGIL/bm-20250422-vultr-x86_64-nascheme-gh_127266_type_slots-3.14.0a7+-986f23a.json: html5lib

- Geometric mean (including insignificant results): 1.080x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.20x