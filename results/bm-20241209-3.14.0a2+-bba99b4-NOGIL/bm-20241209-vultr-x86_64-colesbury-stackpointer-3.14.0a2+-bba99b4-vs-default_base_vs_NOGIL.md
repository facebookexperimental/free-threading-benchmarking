# Results vs. default_base_vs_NOGIL

- fork: colesbury
- ref: stackpointer
- machine: linux-x86_64
- commit hash: bba99b4
- commit date: 2024-12-09
- overall geometric mean: 1.272x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.28x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| 2to3           | 259 ms                                                                 | 372 ms: 1.44x slower                                              |
| docutils       | 2.57 sec                                                               | 3.11 sec: 1.21x slower                                            |
| sphinx         | 997 ms                                                                 | 1.20 sec: 1.20x slower                                            |
| Geometric mean | (ref)                                                                  | 1.28x slower                                                      |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 521 ms: 1.00x faster                                              |
| async_tree_cpu_io_mixed_tg | 599 ms                                                                 | 627 ms: 1.05x slower                                              |
| async_tree_cpu_io_mixed    | 603 ms                                                                 | 654 ms: 1.08x slower                                              |
| coroutines                 | 22.0 ms                                                                | 25.1 ms: 1.14x slower                                             |
| async_generators           | 362 ms                                                                 | 469 ms: 1.30x slower                                              |
| async_tree_none_tg         | 275 ms                                                                 | 366 ms: 1.33x slower                                              |
| async_tree_io_tg           | 622 ms                                                                 | 838 ms: 1.35x slower                                              |
| async_tree_memoization_tg  | 334 ms                                                                 | 460 ms: 1.38x slower                                              |
| async_tree_memoization     | 341 ms                                                                 | 482 ms: 1.42x slower                                              |
| async_tree_io              | 602 ms                                                                 | 864 ms: 1.43x slower                                              |
| async_tree_none            | 275 ms                                                                 | 399 ms: 1.45x slower                                              |
| Geometric mean             | (ref)                                                                  | 1.25x slower                                                      |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| pidigits       | 221 ms                                                                 | 184 ms: 1.20x faster                                              |
| nbody          | 96.1 ms                                                                | 134 ms: 1.39x slower                                              |
| float          | 79.3 ms                                                                | 142 ms: 1.79x slower                                              |
| Geometric mean | (ref)                                                                  | 1.27x slower                                                      |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| regex_v8       | 25.2 ms                                                                | 24.1 ms: 1.05x faster                                             |
| regex_dna      | 179 ms                                                                 | 176 ms: 1.02x faster                                              |
| regex_effbot   | 2.77 ms                                                                | 2.73 ms: 1.01x faster                                             |
| regex_compile  | 131 ms                                                                 | 185 ms: 1.41x slower                                              |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                      |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| xml_etree_iterparse  | 91.0 ms                                                                | 91.5 ms: 1.01x slower                                             |
| xml_etree_parse      | 127 ms                                                                 | 131 ms: 1.03x slower                                              |
| json_loads           | 24.9 us                                                                | 28.6 us: 1.15x slower                                             |
| xml_etree_generate   | 85.3 ms                                                                | 99.5 ms: 1.17x slower                                             |
| json_dumps           | 11.5 ms                                                                | 14.3 ms: 1.25x slower                                             |
| tomli_loads          | 2.09 sec                                                               | 2.72 sec: 1.30x slower                                            |
| xml_etree_process    | 59.7 ms                                                                | 78.8 ms: 1.32x slower                                             |
| unpickle_pure_python | 215 us                                                                 | 339 us: 1.57x slower                                              |
| pickle_pure_python   | 320 us                                                                 | 520 us: 1.62x slower                                              |
| Geometric mean       | (ref)                                                                  | 1.25x slower                                                      |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.4 ms: 1.19x slower                                             |
| python_startup_no_site | 7.47 ms                                                                | 10.2 ms: 1.37x slower                                             |
| Geometric mean         | (ref)                                                                  | 1.28x slower                                                      |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|-----------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| genshi_xml      | 50.4 ms                                                                | 66.0 ms: 1.31x slower                                             |
| django_template | 35.8 ms                                                                | 51.5 ms: 1.44x slower                                             |
| genshi_text     | 22.0 ms                                                                | 32.3 ms: 1.47x slower                                             |
| mako            | 11.6 ms                                                                | 18.2 ms: 1.57x slower                                             |
| Geometric mean  | (ref)                                                                  | 1.44x slower                                                      |

All benchmarks:
===============

| Benchmark                  | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf | bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4 |
|----------------------------|:----------------------------------------------------------------------:|:-----------------------------------------------------------------:|
| gc_traversal               | 4.02 ms                                                                | 3.17 ms: 1.27x faster                                             |
| pidigits                   | 221 ms                                                                 | 184 ms: 1.20x faster                                              |
| regex_v8                   | 25.2 ms                                                                | 24.1 ms: 1.05x faster                                             |
| regex_dna                  | 179 ms                                                                 | 176 ms: 1.02x faster                                              |
| regex_effbot               | 2.77 ms                                                                | 2.73 ms: 1.01x faster                                             |
| asyncio_websockets         | 523 ms                                                                 | 521 ms: 1.00x faster                                              |
| xml_etree_iterparse        | 91.0 ms                                                                | 91.5 ms: 1.01x slower                                             |
| xml_etree_parse            | 127 ms                                                                 | 131 ms: 1.03x slower                                              |
| sqlite_synth               | 2.22 us                                                                | 2.32 us: 1.05x slower                                             |
| async_tree_cpu_io_mixed_tg | 599 ms                                                                 | 627 ms: 1.05x slower                                              |
| create_gc_cycles           | 1.69 ms                                                                | 1.81 ms: 1.07x slower                                             |
| json                       | 4.68 ms                                                                | 5.07 ms: 1.08x slower                                             |
| async_tree_cpu_io_mixed    | 603 ms                                                                 | 654 ms: 1.08x slower                                              |
| pathlib                    | 18.3 ms                                                                | 20.6 ms: 1.13x slower                                             |
| spectral_norm              | 107 ms                                                                 | 123 ms: 1.14x slower                                              |
| coroutines                 | 22.0 ms                                                                | 25.1 ms: 1.14x slower                                             |
| json_loads                 | 24.9 us                                                                | 28.6 us: 1.15x slower                                             |
| xml_etree_generate         | 85.3 ms                                                                | 99.5 ms: 1.17x slower                                             |
| bpe_tokeniser              | 4.32 sec                                                               | 5.05 sec: 1.17x slower                                            |
| scimark_fft                | 349 ms                                                                 | 410 ms: 1.17x slower                                              |
| mdp                        | 2.35 sec                                                               | 2.80 sec: 1.19x slower                                            |
| python_startup             | 14.6 ms                                                                | 17.4 ms: 1.19x slower                                             |
| telco                      | 7.38 ms                                                                | 8.82 ms: 1.20x slower                                             |
| sphinx                     | 997 ms                                                                 | 1.20 sec: 1.20x slower                                            |
| k_core                     | 2.02 sec                                                               | 2.43 sec: 1.20x slower                                            |
| docutils                   | 2.57 sec                                                               | 3.11 sec: 1.21x slower                                            |
| json_dumps                 | 11.5 ms                                                                | 14.3 ms: 1.25x slower                                             |
| scimark_sparse_mat_mult    | 4.76 ms                                                                | 5.93 ms: 1.25x slower                                             |
| shortest_path              | 441 ms                                                                 | 555 ms: 1.26x slower                                              |
| nqueens                    | 79.0 ms                                                                | 99.5 ms: 1.26x slower                                             |
| many_optionals             | 1.03 ms                                                                | 1.31 ms: 1.27x slower                                             |
| bench_mp_pool              | 86.0 ms                                                                | 109 ms: 1.27x slower                                              |
| coverage                   | 79.4 ms                                                                | 101 ms: 1.27x slower                                              |
| deepcopy                   | 262 us                                                                 | 333 us: 1.27x slower                                              |
| connected_components       | 399 ms                                                                 | 507 ms: 1.27x slower                                              |
| dulwich_log                | 76.0 ms                                                                | 97.6 ms: 1.29x slower                                             |
| async_generators           | 362 ms                                                                 | 469 ms: 1.30x slower                                              |
| tomli_loads                | 2.09 sec                                                               | 2.72 sec: 1.30x slower                                            |
| sqlglot_normalize          | 109 ms                                                                 | 142 ms: 1.30x slower                                              |
| sqlglot_optimize           | 54.1 ms                                                                | 70.6 ms: 1.30x slower                                             |
| genshi_xml                 | 50.4 ms                                                                | 66.0 ms: 1.31x slower                                             |
| meteor_contest             | 99.3 ms                                                                | 131 ms: 1.32x slower                                              |
| xml_etree_process          | 59.7 ms                                                                | 78.8 ms: 1.32x slower                                             |
| typing_runtime_protocols   | 158 us                                                                 | 208 us: 1.32x slower                                              |
| async_tree_none_tg         | 275 ms                                                                 | 366 ms: 1.33x slower                                              |
| deepcopy_reduce            | 2.68 us                                                                | 3.56 us: 1.33x slower                                             |
| async_tree_io_tg           | 622 ms                                                                 | 838 ms: 1.35x slower                                              |
| deepcopy_memo              | 30.1 us                                                                | 40.6 us: 1.35x slower                                             |
| generators                 | 29.0 ms                                                                | 39.8 ms: 1.37x slower                                             |
| python_startup_no_site     | 7.47 ms                                                                | 10.2 ms: 1.37x slower                                             |
| pylint                     | 280 ms                                                                 | 385 ms: 1.38x slower                                              |
| async_tree_memoization_tg  | 334 ms                                                                 | 460 ms: 1.38x slower                                              |
| fannkuch                   | 370 ms                                                                 | 514 ms: 1.39x slower                                              |
| nbody                      | 96.1 ms                                                                | 134 ms: 1.39x slower                                              |
| pycparser                  | 1.12 sec                                                               | 1.58 sec: 1.40x slower                                            |
| pprint_safe_repr           | 716 ms                                                                 | 1.01 sec: 1.41x slower                                            |
| regex_compile              | 131 ms                                                                 | 185 ms: 1.41x slower                                              |
| async_tree_memoization     | 341 ms                                                                 | 482 ms: 1.42x slower                                              |
| crypto_pyaes               | 66.5 ms                                                                | 94.3 ms: 1.42x slower                                             |
| subparsers                 | 22.5 ms                                                                | 32.0 ms: 1.42x slower                                             |
| pprint_pformat             | 1.46 sec                                                               | 2.08 sec: 1.42x slower                                            |
| async_tree_io              | 602 ms                                                                 | 864 ms: 1.43x slower                                              |
| django_template            | 35.8 ms                                                                | 51.5 ms: 1.44x slower                                             |
| 2to3                       | 259 ms                                                                 | 372 ms: 1.44x slower                                              |
| async_tree_none            | 275 ms                                                                 | 399 ms: 1.45x slower                                              |
| genshi_text                | 22.0 ms                                                                | 32.3 ms: 1.47x slower                                             |
| sympy_integrate            | 20.1 ms                                                                | 29.7 ms: 1.48x slower                                             |
| sqlalchemy_imperative      | 19.5 ms                                                                | 29.9 ms: 1.53x slower                                             |
| thrift                     | 750 us                                                                 | 1.16 ms: 1.55x slower                                             |
| pyflate                    | 444 ms                                                                 | 693 ms: 1.56x slower                                              |
| mako                       | 11.6 ms                                                                | 18.2 ms: 1.57x slower                                             |
| unpickle_pure_python       | 215 us                                                                 | 339 us: 1.57x slower                                              |
| comprehensions             | 17.5 us                                                                | 27.9 us: 1.59x slower                                             |
| sqlalchemy_declarative     | 128 ms                                                                 | 205 ms: 1.61x slower                                              |
| pickle_pure_python         | 320 us                                                                 | 520 us: 1.62x slower                                              |
| scimark_lu                 | 112 ms                                                                 | 184 ms: 1.65x slower                                              |
| richards_super             | 52.9 ms                                                                | 89.0 ms: 1.68x slower                                             |
| hexiom                     | 5.99 ms                                                                | 10.1 ms: 1.69x slower                                             |
| richards                   | 46.3 ms                                                                | 79.0 ms: 1.71x slower                                             |
| logging_silent             | 108 ns                                                                 | 187 ns: 1.73x slower                                              |
| sympy_str                  | 275 ms                                                                 | 482 ms: 1.75x slower                                              |
| scimark_sor                | 135 ms                                                                 | 237 ms: 1.76x slower                                              |
| float                      | 79.3 ms                                                                | 142 ms: 1.79x slower                                              |
| logging_format             | 6.79 us                                                                | 12.2 us: 1.80x slower                                             |
| chaos                      | 58.9 ms                                                                | 106 ms: 1.80x slower                                              |
| logging_simple             | 6.06 us                                                                | 11.0 us: 1.82x slower                                             |
| scimark_monte_carlo        | 65.2 ms                                                                | 121 ms: 1.85x slower                                              |
| sqlglot_transpile          | 1.60 ms                                                                | 3.00 ms: 1.87x slower                                             |
| sqlglot_parse              | 1.29 ms                                                                | 2.60 ms: 2.01x slower                                             |
| sympy_expand               | 461 ms                                                                 | 963 ms: 2.09x slower                                              |
| raytrace                   | 265 ms                                                                 | 555 ms: 2.09x slower                                              |
| go                         | 120 ms                                                                 | 274 ms: 2.28x slower                                              |
| sympy_sum                  | 153 ms                                                                 | 352 ms: 2.29x slower                                              |
| deltablue                  | 3.21 ms                                                                | 8.21 ms: 2.55x slower                                             |
| bench_thread_pool          | 1.03 ms                                                                | 3.44 ms: 3.33x slower                                             |
| Geometric mean             | (ref)                                                                  | 1.39x slower                                                      |
Ignored benchmarks (1) of results/bm-20241209-3.14.0a2+-bba99b4-NOGIL/bm-20241209-vultr-x86_64-colesbury-stackpointer-3.14.0a2+-bba99b4.json: html5lib

- Geometric mean (including insignificant results): 1.272x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.30x
- 95% likely to have a slowdown of 1.30x
- 99% likely to have a slowdown of 1.28x

# Memory
- memory change: 1.19x