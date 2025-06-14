# Results vs. base

- fork: python
- ref: 56eabea056ae1da49b55
- machine: linux-x86_64
- commit hash: 56eabea
- commit date: 2025-06-13
- overall geometric mean: 1.092x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.08x slower
- Memory change: 1.22x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20250613-3.15.0a0-56eabea/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea.json | results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 248 ms                                                                                                          | 281 ms: 1.14x slower                                                                                                  |
| docutils       | 2.52 sec                                                                                                        | 2.67 sec: 1.06x slower                                                                                                |
| html5lib       | 61.3 ms                                                                                                         | 66.5 ms: 1.09x slower                                                                                                 |
| sphinx         | 973 ms                                                                                                          | 1.06 sec: 1.09x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20250613-3.15.0a0-56eabea/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea.json | results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 619 ms                                                                                                          | 524 ms: 1.18x faster                                                                                                  |
| async_tree_none_tg         | 251 ms                                                                                                          | 228 ms: 1.10x faster                                                                                                  |
| async_tree_io              | 606 ms                                                                                                          | 552 ms: 1.10x faster                                                                                                  |
| async_tree_memoization_tg  | 308 ms                                                                                                          | 287 ms: 1.07x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 497 ms                                                                                                          | 469 ms: 1.06x faster                                                                                                  |
| async_tree_none            | 267 ms                                                                                                          | 260 ms: 1.03x faster                                                                                                  |
| coroutines                 | 23.4 ms                                                                                                         | 23.8 ms: 1.02x slower                                                                                                 |
| async_tree_memoization     | 305 ms                                                                                                          | 313 ms: 1.02x slower                                                                                                  |
| async_generators           | 336 ms                                                                                                          | 368 ms: 1.10x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.03x faster                                                                                                          |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed, asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20250613-3.15.0a0-56eabea/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea.json | results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 206 ms                                                                                                          | 181 ms: 1.14x faster                                                                                                  |
| float          | 71.0 ms                                                                                                         | 69.6 ms: 1.02x faster                                                                                                 |
| nbody          | 88.0 ms                                                                                                         | 122 ms: 1.39x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20250613-3.15.0a0-56eabea/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea.json | results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.6 ms                                                                                                         | 20.1 ms: 1.07x faster                                                                                                 |
| regex_dna      | 171 ms                                                                                                          | 169 ms: 1.01x faster                                                                                                  |
| regex_effbot   | 2.63 ms                                                                                                         | 2.71 ms: 1.03x slower                                                                                                 |
| regex_compile  | 123 ms                                                                                                          | 143 ms: 1.16x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.03x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20250613-3.15.0a0-56eabea/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea.json | results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_iterparse  | 92.1 ms                                                                                                         | 88.6 ms: 1.04x faster                                                                                                 |
| xml_etree_parse      | 132 ms                                                                                                          | 130 ms: 1.01x faster                                                                                                  |
| json_loads           | 28.6 us                                                                                                         | 31.3 us: 1.09x slower                                                                                                 |
| unpickle_pure_python | 208 us                                                                                                          | 228 us: 1.10x slower                                                                                                  |
| json_dumps           | 10.8 ms                                                                                                         | 11.9 ms: 1.11x slower                                                                                                 |
| pickle_pure_python   | 304 us                                                                                                          | 337 us: 1.11x slower                                                                                                  |
| tomli_loads          | 1.91 sec                                                                                                        | 2.15 sec: 1.13x slower                                                                                                |
| xml_etree_generate   | 82.6 ms                                                                                                         | 95.0 ms: 1.15x slower                                                                                                 |
| xml_etree_process    | 58.5 ms                                                                                                         | 69.0 ms: 1.18x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.09x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20250613-3.15.0a0-56eabea/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea.json | results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.5 ms                                                                                                         | 16.0 ms: 1.28x slower                                                                                                 |
| python_startup_no_site | 7.27 ms                                                                                                         | 9.58 ms: 1.32x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.30x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20250613-3.15.0a0-56eabea/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea.json | results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 34.3 ms                                                                                                         | 39.5 ms: 1.15x slower                                                                                                 |
| genshi_xml      | 47.2 ms                                                                                                         | 57.4 ms: 1.22x slower                                                                                                 |
| genshi_text     | 20.0 ms                                                                                                         | 26.4 ms: 1.32x slower                                                                                                 |
| mako            | 11.8 ms                                                                                                         | 16.0 ms: 1.35x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.26x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20250613-3.15.0a0-56eabea/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea.json | results/bm-20250613-3.15.0a0-56eabea-NOGIL/bm-20250613-vultr-x86_64-python-56eabea056ae1da49b55-3.15.0a0-56eabea.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.40 ms                                                                                                         | 1.91 ms: 2.31x faster                                                                                                 |
| create_gc_cycles           | 1.89 ms                                                                                                         | 1.48 ms: 1.28x faster                                                                                                 |
| async_tree_io_tg           | 619 ms                                                                                                          | 524 ms: 1.18x faster                                                                                                  |
| pidigits                   | 206 ms                                                                                                          | 181 ms: 1.14x faster                                                                                                  |
| sqlite_synth               | 2.27 us                                                                                                         | 2.03 us: 1.12x faster                                                                                                 |
| async_tree_none_tg         | 251 ms                                                                                                          | 228 ms: 1.10x faster                                                                                                  |
| async_tree_io              | 606 ms                                                                                                          | 552 ms: 1.10x faster                                                                                                  |
| regex_v8                   | 21.6 ms                                                                                                         | 20.1 ms: 1.07x faster                                                                                                 |
| async_tree_memoization_tg  | 308 ms                                                                                                          | 287 ms: 1.07x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 497 ms                                                                                                          | 469 ms: 1.06x faster                                                                                                  |
| xml_etree_iterparse        | 92.1 ms                                                                                                         | 88.6 ms: 1.04x faster                                                                                                 |
| async_tree_none            | 267 ms                                                                                                          | 260 ms: 1.03x faster                                                                                                  |
| float                      | 71.0 ms                                                                                                         | 69.6 ms: 1.02x faster                                                                                                 |
| xml_etree_parse            | 132 ms                                                                                                          | 130 ms: 1.01x faster                                                                                                  |
| regex_dna                  | 171 ms                                                                                                          | 169 ms: 1.01x faster                                                                                                  |
| coroutines                 | 23.4 ms                                                                                                         | 23.8 ms: 1.02x slower                                                                                                 |
| async_tree_memoization     | 305 ms                                                                                                          | 313 ms: 1.02x slower                                                                                                  |
| pathlib                    | 19.3 ms                                                                                                         | 19.8 ms: 1.03x slower                                                                                                 |
| regex_effbot               | 2.63 ms                                                                                                         | 2.71 ms: 1.03x slower                                                                                                 |
| pycparser                  | 1.09 sec                                                                                                        | 1.13 sec: 1.04x slower                                                                                                |
| json                       | 5.10 ms                                                                                                         | 5.33 ms: 1.05x slower                                                                                                 |
| bench_mp_pool              | 98.3 ms                                                                                                         | 103 ms: 1.05x slower                                                                                                  |
| docutils                   | 2.52 sec                                                                                                        | 2.67 sec: 1.06x slower                                                                                                |
| bpe_tokeniser              | 4.13 sec                                                                                                        | 4.38 sec: 1.06x slower                                                                                                |
| dulwich_log                | 66.7 ms                                                                                                         | 72.0 ms: 1.08x slower                                                                                                 |
| many_optionals             | 1.04 ms                                                                                                         | 1.12 ms: 1.08x slower                                                                                                 |
| sphinx                     | 973 ms                                                                                                          | 1.06 sec: 1.09x slower                                                                                                |
| html5lib                   | 61.3 ms                                                                                                         | 66.5 ms: 1.09x slower                                                                                                 |
| json_loads                 | 28.6 us                                                                                                         | 31.3 us: 1.09x slower                                                                                                 |
| deltablue                  | 3.24 ms                                                                                                         | 3.56 ms: 1.10x slower                                                                                                 |
| pylint                     | 279 ms                                                                                                          | 306 ms: 1.10x slower                                                                                                  |
| async_generators           | 336 ms                                                                                                          | 368 ms: 1.10x slower                                                                                                  |
| unpickle_pure_python       | 208 us                                                                                                          | 228 us: 1.10x slower                                                                                                  |
| k_core                     | 2.03 sec                                                                                                        | 2.24 sec: 1.10x slower                                                                                                |
| json_dumps                 | 10.8 ms                                                                                                         | 11.9 ms: 1.11x slower                                                                                                 |
| pickle_pure_python         | 304 us                                                                                                          | 337 us: 1.11x slower                                                                                                  |
| comprehensions             | 15.6 us                                                                                                         | 17.3 us: 1.11x slower                                                                                                 |
| subparsers                 | 25.2 ms                                                                                                         | 28.1 ms: 1.11x slower                                                                                                 |
| logging_silent             | 469 ns                                                                                                          | 522 ns: 1.11x slower                                                                                                  |
| scimark_sor                | 111 ms                                                                                                          | 123 ms: 1.11x slower                                                                                                  |
| chaos                      | 55.8 ms                                                                                                         | 62.2 ms: 1.11x slower                                                                                                 |
| spectral_norm              | 97.4 ms                                                                                                         | 109 ms: 1.12x slower                                                                                                  |
| scimark_fft                | 328 ms                                                                                                          | 368 ms: 1.12x slower                                                                                                  |
| tomli_loads                | 1.91 sec                                                                                                        | 2.15 sec: 1.13x slower                                                                                                |
| nqueens                    | 74.9 ms                                                                                                         | 85.0 ms: 1.13x slower                                                                                                 |
| 2to3                       | 248 ms                                                                                                          | 281 ms: 1.14x slower                                                                                                  |
| pprint_safe_repr           | 764 ms                                                                                                          | 868 ms: 1.14x slower                                                                                                  |
| deepcopy_reduce            | 2.65 us                                                                                                         | 3.02 us: 1.14x slower                                                                                                 |
| mdp                        | 1.15 sec                                                                                                        | 1.31 sec: 1.14x slower                                                                                                |
| logging_simple             | 6.71 us                                                                                                         | 7.68 us: 1.14x slower                                                                                                 |
| pprint_pformat             | 1.56 sec                                                                                                        | 1.79 sec: 1.15x slower                                                                                                |
| deepcopy                   | 250 us                                                                                                          | 287 us: 1.15x slower                                                                                                  |
| xml_etree_generate         | 82.6 ms                                                                                                         | 95.0 ms: 1.15x slower                                                                                                 |
| django_template            | 34.3 ms                                                                                                         | 39.5 ms: 1.15x slower                                                                                                 |
| sqlglot_v2_optimize        | 49.3 ms                                                                                                         | 57.1 ms: 1.16x slower                                                                                                 |
| go                         | 105 ms                                                                                                          | 122 ms: 1.16x slower                                                                                                  |
| sqlglot_v2_normalize       | 98.1 ms                                                                                                         | 114 ms: 1.16x slower                                                                                                  |
| hexiom                     | 5.54 ms                                                                                                         | 6.43 ms: 1.16x slower                                                                                                 |
| regex_compile              | 123 ms                                                                                                          | 143 ms: 1.16x slower                                                                                                  |
| scimark_lu                 | 110 ms                                                                                                          | 128 ms: 1.17x slower                                                                                                  |
| pyflate                    | 398 ms                                                                                                          | 464 ms: 1.17x slower                                                                                                  |
| logging_format             | 7.44 us                                                                                                         | 8.68 us: 1.17x slower                                                                                                 |
| generators                 | 27.3 ms                                                                                                         | 31.8 ms: 1.17x slower                                                                                                 |
| sympy_integrate            | 18.7 ms                                                                                                         | 21.9 ms: 1.17x slower                                                                                                 |
| sympy_sum                  | 152 ms                                                                                                          | 178 ms: 1.18x slower                                                                                                  |
| sympy_expand               | 444 ms                                                                                                          | 523 ms: 1.18x slower                                                                                                  |
| sympy_str                  | 265 ms                                                                                                          | 313 ms: 1.18x slower                                                                                                  |
| telco                      | 7.23 ms                                                                                                         | 8.53 ms: 1.18x slower                                                                                                 |
| xml_etree_process          | 58.5 ms                                                                                                         | 69.0 ms: 1.18x slower                                                                                                 |
| raytrace                   | 249 ms                                                                                                          | 296 ms: 1.19x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.48 ms                                                                                                         | 1.78 ms: 1.20x slower                                                                                                 |
| thrift                     | 729 us                                                                                                          | 874 us: 1.20x slower                                                                                                  |
| deepcopy_memo              | 28.9 us                                                                                                         | 34.7 us: 1.20x slower                                                                                                 |
| meteor_contest             | 98.7 ms                                                                                                         | 120 ms: 1.21x slower                                                                                                  |
| fannkuch                   | 378 ms                                                                                                          | 458 ms: 1.21x slower                                                                                                  |
| genshi_xml                 | 47.2 ms                                                                                                         | 57.4 ms: 1.22x slower                                                                                                 |
| shortest_path              | 443 ms                                                                                                          | 539 ms: 1.22x slower                                                                                                  |
| sqlglot_v2_parse           | 1.19 ms                                                                                                         | 1.46 ms: 1.22x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.49 ms                                                                                                         | 5.49 ms: 1.22x slower                                                                                                 |
| typing_runtime_protocols   | 152 us                                                                                                          | 187 us: 1.23x slower                                                                                                  |
| connected_components       | 395 ms                                                                                                          | 488 ms: 1.24x slower                                                                                                  |
| crypto_pyaes               | 67.6 ms                                                                                                         | 85.2 ms: 1.26x slower                                                                                                 |
| scimark_monte_carlo        | 61.3 ms                                                                                                         | 77.4 ms: 1.26x slower                                                                                                 |
| richards                   | 41.2 ms                                                                                                         | 52.5 ms: 1.27x slower                                                                                                 |
| python_startup             | 12.5 ms                                                                                                         | 16.0 ms: 1.28x slower                                                                                                 |
| richards_super             | 46.8 ms                                                                                                         | 59.7 ms: 1.28x slower                                                                                                 |
| genshi_text                | 20.0 ms                                                                                                         | 26.4 ms: 1.32x slower                                                                                                 |
| python_startup_no_site     | 7.27 ms                                                                                                         | 9.58 ms: 1.32x slower                                                                                                 |
| mako                       | 11.8 ms                                                                                                         | 16.0 ms: 1.35x slower                                                                                                 |
| coverage                   | 81.2 ms                                                                                                         | 110 ms: 1.36x slower                                                                                                  |
| nbody                      | 88.0 ms                                                                                                         | 122 ms: 1.39x slower                                                                                                  |
| bench_thread_pool          | 1.04 ms                                                                                                         | 3.10 ms: 2.99x slower                                                                                                 |
| Geometric mean             | (ref)                                                                                                           | 1.11x slower                                                                                                          |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed, asyncio_websockets

- Geometric mean (including insignificant results): 1.092x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.09x
- 95% likely to have a slowdown of 1.09x
- 99% likely to have a slowdown of 1.08x

# Memory
- memory change: 1.22x