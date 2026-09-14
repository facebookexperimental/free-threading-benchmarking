# Results vs. base

- fork: python
- ref: fd0970c0ab7eb8c685ef
- machine: linux-x86_64
- commit hash: fd0970c
- commit date: 2026-09-13
- overall geometric mean: 1.107x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260913-3.16.0a0-fd0970c/bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json | results/bm-20260913-3.16.0a0-fd0970c-NOGIL/bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 260 ms                                                                                                          | 298 ms: 1.15x slower                                                                                                  |
| docutils       | 2.36 sec                                                                                                        | 2.95 sec: 1.25x slower                                                                                                |
| html5lib       | 59.3 ms                                                                                                         | 67.6 ms: 1.14x slower                                                                                                 |
| sphinx         | 992 ms                                                                                                          | 1.11 sec: 1.12x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.16x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260913-3.16.0a0-fd0970c/bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json | results/bm-20260913-3.16.0a0-fd0970c-NOGIL/bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 761 ms                                                                                                          | 695 ms: 1.10x faster                                                                                                  |
| async_tree_io              | 778 ms                                                                                                          | 723 ms: 1.08x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 512 ms: 1.06x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 556 ms                                                                                                          | 583 ms: 1.05x slower                                                                                                  |
| coroutines                 | 23.8 ms                                                                                                         | 25.4 ms: 1.07x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 567 ms                                                                                                          | 611 ms: 1.08x slower                                                                                                  |
| async_tree_memoization_tg  | 366 ms                                                                                                          | 399 ms: 1.09x slower                                                                                                  |
| async_tree_memoization     | 409 ms                                                                                                          | 449 ms: 1.10x slower                                                                                                  |
| async_tree_none_tg         | 302 ms                                                                                                          | 332 ms: 1.10x slower                                                                                                  |
| async_tree_none            | 330 ms                                                                                                          | 373 ms: 1.13x slower                                                                                                  |
| async_generators           | 346 ms                                                                                                          | 415 ms: 1.20x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.05x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260913-3.16.0a0-fd0970c/bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json | results/bm-20260913-3.16.0a0-fd0970c-NOGIL/bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                                                                          | 180 ms: 1.02x faster                                                                                                  |
| float          | 73.0 ms                                                                                                         | 85.4 ms: 1.17x slower                                                                                                 |
| nbody          | 88.4 ms                                                                                                         | 122 ms: 1.38x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.16x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260913-3.16.0a0-fd0970c/bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json | results/bm-20260913-3.16.0a0-fd0970c-NOGIL/bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.0 ms                                                                                                         | 20.8 ms: 1.01x faster                                                                                                 |
| regex_dna      | 179 ms                                                                                                          | 184 ms: 1.02x slower                                                                                                  |
| regex_effbot   | 2.80 ms                                                                                                         | 2.98 ms: 1.07x slower                                                                                                 |
| regex_compile  | 149 ms                                                                                                          | 171 ms: 1.15x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260913-3.16.0a0-fd0970c/bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json | results/bm-20260913-3.16.0a0-fd0970c-NOGIL/bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 145 ms                                                                                                          | 144 ms: 1.01x faster                                                                                                  |
| xml_etree_iterparse  | 92.1 ms                                                                                                         | 96.2 ms: 1.04x slower                                                                                                 |
| tomli_loads          | 1.82 sec                                                                                                        | 1.95 sec: 1.07x slower                                                                                                |
| json_dumps           | 9.32 ms                                                                                                         | 10.0 ms: 1.07x slower                                                                                                 |
| pickle_pure_python   | 309 us                                                                                                          | 338 us: 1.09x slower                                                                                                  |
| json_loads           | 27.1 us                                                                                                         | 30.6 us: 1.13x slower                                                                                                 |
| unpickle_pure_python | 213 us                                                                                                          | 241 us: 1.13x slower                                                                                                  |
| xml_etree_generate   | 87.8 ms                                                                                                         | 103 ms: 1.17x slower                                                                                                  |
| xml_etree_process    | 62.2 ms                                                                                                         | 76.2 ms: 1.22x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260913-3.16.0a0-fd0970c/bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json | results/bm-20260913-3.16.0a0-fd0970c-NOGIL/bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 13.0 ms                                                                                                         | 16.4 ms: 1.27x slower                                                                                                 |
| python_startup_no_site | 7.74 ms                                                                                                         | 9.96 ms: 1.29x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.28x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260913-3.16.0a0-fd0970c/bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json | results/bm-20260913-3.16.0a0-fd0970c-NOGIL/bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.6 ms                                                                                                         | 41.8 ms: 1.14x slower                                                                                                 |
| mako            | 12.0 ms                                                                                                         | 15.9 ms: 1.32x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.23x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260913-3.16.0a0-fd0970c/bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json | results/bm-20260913-3.16.0a0-fd0970c-NOGIL/bm-20260913-vultr-x86_64-python-fd0970c0ab7eb8c685ef-3.16.0a0-fd0970c.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 275 ms                                                                                                          | 6.73 ms: 40.79x faster                                                                                                |
| gc_traversal               | 3.62 ms                                                                                                         | 1.78 ms: 2.03x faster                                                                                                 |
| create_gc_cycles           | 1.67 ms                                                                                                         | 1.38 ms: 1.21x faster                                                                                                 |
| sqlite_synth               | 2.29 us                                                                                                         | 1.94 us: 1.18x faster                                                                                                 |
| async_tree_io_tg           | 761 ms                                                                                                          | 695 ms: 1.10x faster                                                                                                  |
| async_tree_io              | 778 ms                                                                                                          | 723 ms: 1.08x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 512 ms: 1.06x faster                                                                                                  |
| pidigits                   | 184 ms                                                                                                          | 180 ms: 1.02x faster                                                                                                  |
| regex_v8                   | 21.0 ms                                                                                                         | 20.8 ms: 1.01x faster                                                                                                 |
| xml_etree_parse            | 145 ms                                                                                                          | 144 ms: 1.01x faster                                                                                                  |
| regex_dna                  | 179 ms                                                                                                          | 184 ms: 1.02x slower                                                                                                  |
| pathlib                    | 17.7 ms                                                                                                         | 18.1 ms: 1.02x slower                                                                                                 |
| bpe_tokeniser              | 4.23 sec                                                                                                        | 4.35 sec: 1.03x slower                                                                                                |
| xml_etree_iterparse        | 92.1 ms                                                                                                         | 96.2 ms: 1.04x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 556 ms                                                                                                          | 583 ms: 1.05x slower                                                                                                  |
| pycparser                  | 1.12 sec                                                                                                        | 1.18 sec: 1.06x slower                                                                                                |
| regex_effbot               | 2.80 ms                                                                                                         | 2.98 ms: 1.07x slower                                                                                                 |
| dulwich_log                | 66.8 ms                                                                                                         | 71.3 ms: 1.07x slower                                                                                                 |
| coroutines                 | 23.8 ms                                                                                                         | 25.4 ms: 1.07x slower                                                                                                 |
| tomli_loads                | 1.82 sec                                                                                                        | 1.95 sec: 1.07x slower                                                                                                |
| k_core                     | 2.10 sec                                                                                                        | 2.25 sec: 1.07x slower                                                                                                |
| json_dumps                 | 9.32 ms                                                                                                         | 10.0 ms: 1.07x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 567 ms                                                                                                          | 611 ms: 1.08x slower                                                                                                  |
| logging_silent             | 97.4 ns                                                                                                         | 106 ns: 1.09x slower                                                                                                  |
| async_tree_memoization_tg  | 366 ms                                                                                                          | 399 ms: 1.09x slower                                                                                                  |
| json                       | 4.95 ms                                                                                                         | 5.40 ms: 1.09x slower                                                                                                 |
| telco                      | 161 ms                                                                                                          | 175 ms: 1.09x slower                                                                                                  |
| pickle_pure_python         | 309 us                                                                                                          | 338 us: 1.09x slower                                                                                                  |
| bench_thread_pool          | 1.35 ms                                                                                                         | 1.49 ms: 1.10x slower                                                                                                 |
| async_tree_memoization     | 409 ms                                                                                                          | 449 ms: 1.10x slower                                                                                                  |
| async_tree_none_tg         | 302 ms                                                                                                          | 332 ms: 1.10x slower                                                                                                  |
| deltablue                  | 3.37 ms                                                                                                         | 3.73 ms: 1.11x slower                                                                                                 |
| scimark_lu                 | 119 ms                                                                                                          | 133 ms: 1.11x slower                                                                                                  |
| many_optionals             | 916 us                                                                                                          | 1.02 ms: 1.12x slower                                                                                                 |
| generators                 | 30.4 ms                                                                                                         | 34.0 ms: 1.12x slower                                                                                                 |
| sphinx                     | 992 ms                                                                                                          | 1.11 sec: 1.12x slower                                                                                                |
| comprehensions             | 15.9 us                                                                                                         | 17.9 us: 1.13x slower                                                                                                 |
| scimark_sor                | 109 ms                                                                                                          | 123 ms: 1.13x slower                                                                                                  |
| sqlglot_v2_optimize        | 51.7 ms                                                                                                         | 58.4 ms: 1.13x slower                                                                                                 |
| pprint_safe_repr           | 729 ms                                                                                                          | 824 ms: 1.13x slower                                                                                                  |
| json_loads                 | 27.1 us                                                                                                         | 30.6 us: 1.13x slower                                                                                                 |
| sqlglot_v2_normalize       | 103 ms                                                                                                          | 116 ms: 1.13x slower                                                                                                  |
| unpickle_pure_python       | 213 us                                                                                                          | 241 us: 1.13x slower                                                                                                  |
| scimark_fft                | 305 ms                                                                                                          | 346 ms: 1.13x slower                                                                                                  |
| async_tree_none            | 330 ms                                                                                                          | 373 ms: 1.13x slower                                                                                                  |
| sympy_expand               | 477 ms                                                                                                          | 541 ms: 1.13x slower                                                                                                  |
| go                         | 106 ms                                                                                                          | 121 ms: 1.13x slower                                                                                                  |
| chaos                      | 53.6 ms                                                                                                         | 61.2 ms: 1.14x slower                                                                                                 |
| html5lib                   | 59.3 ms                                                                                                         | 67.6 ms: 1.14x slower                                                                                                 |
| django_template            | 36.6 ms                                                                                                         | 41.8 ms: 1.14x slower                                                                                                 |
| sympy_integrate            | 19.4 ms                                                                                                         | 22.2 ms: 1.14x slower                                                                                                 |
| sympy_str                  | 281 ms                                                                                                          | 321 ms: 1.14x slower                                                                                                  |
| pylint                     | 114 ms                                                                                                          | 130 ms: 1.14x slower                                                                                                  |
| 2to3                       | 260 ms                                                                                                          | 298 ms: 1.15x slower                                                                                                  |
| pprint_pformat             | 1.48 sec                                                                                                        | 1.70 sec: 1.15x slower                                                                                                |
| regex_compile              | 149 ms                                                                                                          | 171 ms: 1.15x slower                                                                                                  |
| thrift                     | 793 us                                                                                                          | 916 us: 1.16x slower                                                                                                  |
| sympy_sum                  | 160 ms                                                                                                          | 185 ms: 1.16x slower                                                                                                  |
| mdp                        | 1.13 sec                                                                                                        | 1.31 sec: 1.16x slower                                                                                                |
| deepcopy_reduce            | 2.61 us                                                                                                         | 3.02 us: 1.16x slower                                                                                                 |
| deepcopy                   | 235 us                                                                                                          | 274 us: 1.17x slower                                                                                                  |
| subparsers                 | 9.02 ms                                                                                                         | 10.5 ms: 1.17x slower                                                                                                 |
| pyflate                    | 395 ms                                                                                                          | 461 ms: 1.17x slower                                                                                                  |
| hexiom                     | 5.64 ms                                                                                                         | 6.58 ms: 1.17x slower                                                                                                 |
| float                      | 73.0 ms                                                                                                         | 85.4 ms: 1.17x slower                                                                                                 |
| logging_simple             | 6.08 us                                                                                                         | 7.12 us: 1.17x slower                                                                                                 |
| xml_etree_generate         | 87.8 ms                                                                                                         | 103 ms: 1.17x slower                                                                                                  |
| raytrace                   | 251 ms                                                                                                          | 295 ms: 1.17x slower                                                                                                  |
| richards                   | 45.3 ms                                                                                                         | 53.3 ms: 1.18x slower                                                                                                 |
| deepcopy_memo              | 26.9 us                                                                                                         | 31.8 us: 1.18x slower                                                                                                 |
| richards_super             | 51.5 ms                                                                                                         | 60.9 ms: 1.18x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.40 ms                                                                                                         | 5.25 ms: 1.20x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.46 ms                                                                                                         | 1.75 ms: 1.20x slower                                                                                                 |
| async_generators           | 346 ms                                                                                                          | 415 ms: 1.20x slower                                                                                                  |
| logging_format             | 6.82 us                                                                                                         | 8.20 us: 1.20x slower                                                                                                 |
| spectral_norm              | 89.8 ms                                                                                                         | 108 ms: 1.21x slower                                                                                                  |
| nqueens                    | 73.8 ms                                                                                                         | 89.6 ms: 1.21x slower                                                                                                 |
| sqlglot_v2_parse           | 1.17 ms                                                                                                         | 1.43 ms: 1.22x slower                                                                                                 |
| shortest_path              | 438 ms                                                                                                          | 534 ms: 1.22x slower                                                                                                  |
| xml_etree_process          | 62.2 ms                                                                                                         | 76.2 ms: 1.22x slower                                                                                                 |
| typing_runtime_protocols   | 121 us                                                                                                          | 148 us: 1.23x slower                                                                                                  |
| connected_components       | 397 ms                                                                                                          | 489 ms: 1.23x slower                                                                                                  |
| docutils                   | 2.36 sec                                                                                                        | 2.95 sec: 1.25x slower                                                                                                |
| scimark_monte_carlo        | 62.1 ms                                                                                                         | 77.9 ms: 1.26x slower                                                                                                 |
| fannkuch                   | 376 ms                                                                                                          | 472 ms: 1.26x slower                                                                                                  |
| python_startup             | 13.0 ms                                                                                                         | 16.4 ms: 1.27x slower                                                                                                 |
| meteor_contest             | 101 ms                                                                                                          | 129 ms: 1.27x slower                                                                                                  |
| python_startup_no_site     | 7.74 ms                                                                                                         | 9.96 ms: 1.29x slower                                                                                                 |
| crypto_pyaes               | 67.5 ms                                                                                                         | 88.8 ms: 1.31x slower                                                                                                 |
| mako                       | 12.0 ms                                                                                                         | 15.9 ms: 1.32x slower                                                                                                 |
| nbody                      | 88.4 ms                                                                                                         | 122 ms: 1.38x slower                                                                                                  |
| coverage                   | 83.4 ms                                                                                                         | 117 ms: 1.41x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.07x slower                                                                                                          |

- Geometric mean (including insignificant results): 1.107x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.19x