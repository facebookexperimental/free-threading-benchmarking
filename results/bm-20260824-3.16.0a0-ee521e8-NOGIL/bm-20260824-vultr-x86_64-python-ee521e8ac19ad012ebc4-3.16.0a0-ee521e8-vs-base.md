# Results vs. base

- fork: python
- ref: ee521e8ac19ad012ebc4
- machine: linux-x86_64
- commit hash: ee521e8
- commit date: 2026-08-24
- overall geometric mean: 1.107x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260824-3.16.0a0-ee521e8/bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json | results/bm-20260824-3.16.0a0-ee521e8-NOGIL/bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 259 ms                                                                                                          | 295 ms: 1.14x slower                                                                                                  |
| docutils       | 2.37 sec                                                                                                        | 2.92 sec: 1.24x slower                                                                                                |
| html5lib       | 59.5 ms                                                                                                         | 67.8 ms: 1.14x slower                                                                                                 |
| sphinx         | 988 ms                                                                                                          | 1.11 sec: 1.13x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.16x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260824-3.16.0a0-ee521e8/bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json | results/bm-20260824-3.16.0a0-ee521e8-NOGIL/bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 759 ms                                                                                                          | 693 ms: 1.09x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 512 ms: 1.06x faster                                                                                                  |
| async_tree_io              | 721 ms                                                                                                          | 701 ms: 1.03x faster                                                                                                  |
| async_tree_cpu_io_mixed_tg | 560 ms                                                                                                          | 581 ms: 1.04x slower                                                                                                  |
| coroutines                 | 23.7 ms                                                                                                         | 25.1 ms: 1.06x slower                                                                                                 |
| async_tree_memoization_tg  | 370 ms                                                                                                          | 399 ms: 1.08x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 545 ms                                                                                                          | 599 ms: 1.10x slower                                                                                                  |
| async_tree_memoization     | 378 ms                                                                                                          | 416 ms: 1.10x slower                                                                                                  |
| async_tree_none_tg         | 300 ms                                                                                                          | 333 ms: 1.11x slower                                                                                                  |
| async_tree_none            | 294 ms                                                                                                          | 339 ms: 1.15x slower                                                                                                  |
| async_generators           | 347 ms                                                                                                          | 414 ms: 1.19x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.06x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260824-3.16.0a0-ee521e8/bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json | results/bm-20260824-3.16.0a0-ee521e8-NOGIL/bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 195 ms                                                                                                          | 180 ms: 1.09x faster                                                                                                  |
| float          | 73.3 ms                                                                                                         | 84.3 ms: 1.15x slower                                                                                                 |
| nbody          | 89.7 ms                                                                                                         | 124 ms: 1.38x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.13x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260824-3.16.0a0-ee521e8/bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json | results/bm-20260824-3.16.0a0-ee521e8-NOGIL/bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.6 ms                                                                                                         | 21.3 ms: 1.01x faster                                                                                                 |
| regex_dna      | 182 ms                                                                                                          | 188 ms: 1.03x slower                                                                                                  |
| regex_compile  | 149 ms                                                                                                          | 169 ms: 1.13x slower                                                                                                  |
| regex_effbot   | 2.63 ms                                                                                                         | 3.01 ms: 1.15x slower                                                                                                 |
| Geometric mean | (ref)                                                                                                           | 1.07x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260824-3.16.0a0-ee521e8/bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json | results/bm-20260824-3.16.0a0-ee521e8-NOGIL/bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 142 ms                                                                                                          | 140 ms: 1.01x faster                                                                                                  |
| json_dumps           | 9.43 ms                                                                                                         | 10.0 ms: 1.06x slower                                                                                                 |
| xml_etree_iterparse  | 90.6 ms                                                                                                         | 96.5 ms: 1.06x slower                                                                                                 |
| tomli_loads          | 1.82 sec                                                                                                        | 1.97 sec: 1.08x slower                                                                                                |
| pickle_pure_python   | 302 us                                                                                                          | 336 us: 1.11x slower                                                                                                  |
| unpickle_pure_python | 213 us                                                                                                          | 238 us: 1.12x slower                                                                                                  |
| json_loads           | 27.5 us                                                                                                         | 30.7 us: 1.12x slower                                                                                                 |
| xml_etree_generate   | 87.6 ms                                                                                                         | 102 ms: 1.17x slower                                                                                                  |
| xml_etree_process    | 61.9 ms                                                                                                         | 76.0 ms: 1.23x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260824-3.16.0a0-ee521e8/bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json | results/bm-20260824-3.16.0a0-ee521e8-NOGIL/bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.9 ms                                                                                                         | 16.1 ms: 1.24x slower                                                                                                 |
| python_startup_no_site | 7.70 ms                                                                                                         | 9.91 ms: 1.29x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.26x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260824-3.16.0a0-ee521e8/bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json | results/bm-20260824-3.16.0a0-ee521e8-NOGIL/bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.6 ms                                                                                                         | 40.9 ms: 1.12x slower                                                                                                 |
| mako            | 12.1 ms                                                                                                         | 15.8 ms: 1.31x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.21x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260824-3.16.0a0-ee521e8/bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json | results/bm-20260824-3.16.0a0-ee521e8-NOGIL/bm-20260824-vultr-x86_64-python-ee521e8ac19ad012ebc4-3.16.0a0-ee521e8.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 299 ms                                                                                                          | 6.69 ms: 44.71x faster                                                                                                |
| gc_traversal               | 3.60 ms                                                                                                         | 1.78 ms: 2.02x faster                                                                                                 |
| create_gc_cycles           | 1.70 ms                                                                                                         | 1.37 ms: 1.24x faster                                                                                                 |
| sqlite_synth               | 2.22 us                                                                                                         | 1.94 us: 1.14x faster                                                                                                 |
| async_tree_io_tg           | 759 ms                                                                                                          | 693 ms: 1.09x faster                                                                                                  |
| pidigits                   | 195 ms                                                                                                          | 180 ms: 1.09x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 512 ms: 1.06x faster                                                                                                  |
| async_tree_io              | 721 ms                                                                                                          | 701 ms: 1.03x faster                                                                                                  |
| regex_v8                   | 21.6 ms                                                                                                         | 21.3 ms: 1.01x faster                                                                                                 |
| xml_etree_parse            | 142 ms                                                                                                          | 140 ms: 1.01x faster                                                                                                  |
| pathlib                    | 17.6 ms                                                                                                         | 17.9 ms: 1.02x slower                                                                                                 |
| bpe_tokeniser              | 4.23 sec                                                                                                        | 4.35 sec: 1.03x slower                                                                                                |
| regex_dna                  | 182 ms                                                                                                          | 188 ms: 1.03x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg | 560 ms                                                                                                          | 581 ms: 1.04x slower                                                                                                  |
| pycparser                  | 1.12 sec                                                                                                        | 1.18 sec: 1.05x slower                                                                                                |
| dulwich_log                | 67.6 ms                                                                                                         | 71.0 ms: 1.05x slower                                                                                                 |
| coroutines                 | 23.7 ms                                                                                                         | 25.1 ms: 1.06x slower                                                                                                 |
| json_dumps                 | 9.43 ms                                                                                                         | 10.0 ms: 1.06x slower                                                                                                 |
| xml_etree_iterparse        | 90.6 ms                                                                                                         | 96.5 ms: 1.06x slower                                                                                                 |
| k_core                     | 2.08 sec                                                                                                        | 2.24 sec: 1.08x slower                                                                                                |
| async_tree_memoization_tg  | 370 ms                                                                                                          | 399 ms: 1.08x slower                                                                                                  |
| tomli_loads                | 1.82 sec                                                                                                        | 1.97 sec: 1.08x slower                                                                                                |
| json                       | 4.93 ms                                                                                                         | 5.40 ms: 1.10x slower                                                                                                 |
| bench_thread_pool          | 1.34 ms                                                                                                         | 1.48 ms: 1.10x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 545 ms                                                                                                          | 599 ms: 1.10x slower                                                                                                  |
| telco                      | 159 ms                                                                                                          | 174 ms: 1.10x slower                                                                                                  |
| async_tree_memoization     | 378 ms                                                                                                          | 416 ms: 1.10x slower                                                                                                  |
| async_tree_none_tg         | 300 ms                                                                                                          | 333 ms: 1.11x slower                                                                                                  |
| pickle_pure_python         | 302 us                                                                                                          | 336 us: 1.11x slower                                                                                                  |
| many_optionals             | 902 us                                                                                                          | 1.01 ms: 1.11x slower                                                                                                 |
| sqlglot_v2_optimize        | 52.0 ms                                                                                                         | 58.0 ms: 1.12x slower                                                                                                 |
| unpickle_pure_python       | 213 us                                                                                                          | 238 us: 1.12x slower                                                                                                  |
| json_loads                 | 27.5 us                                                                                                         | 30.7 us: 1.12x slower                                                                                                 |
| django_template            | 36.6 ms                                                                                                         | 40.9 ms: 1.12x slower                                                                                                 |
| sqlglot_v2_normalize       | 103 ms                                                                                                          | 115 ms: 1.12x slower                                                                                                  |
| pprint_safe_repr           | 728 ms                                                                                                          | 820 ms: 1.13x slower                                                                                                  |
| sphinx                     | 988 ms                                                                                                          | 1.11 sec: 1.13x slower                                                                                                |
| scimark_fft                | 308 ms                                                                                                          | 347 ms: 1.13x slower                                                                                                  |
| scimark_lu                 | 115 ms                                                                                                          | 130 ms: 1.13x slower                                                                                                  |
| deltablue                  | 3.28 ms                                                                                                         | 3.71 ms: 1.13x slower                                                                                                 |
| logging_silent             | 94.8 ns                                                                                                         | 107 ns: 1.13x slower                                                                                                  |
| regex_compile              | 149 ms                                                                                                          | 169 ms: 1.13x slower                                                                                                  |
| sympy_expand               | 476 ms                                                                                                          | 540 ms: 1.14x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.68 ms                                                                                                         | 5.32 ms: 1.14x slower                                                                                                 |
| 2to3                       | 259 ms                                                                                                          | 295 ms: 1.14x slower                                                                                                  |
| html5lib                   | 59.5 ms                                                                                                         | 67.8 ms: 1.14x slower                                                                                                 |
| sympy_integrate            | 19.2 ms                                                                                                         | 21.8 ms: 1.14x slower                                                                                                 |
| pylint                     | 114 ms                                                                                                          | 131 ms: 1.14x slower                                                                                                  |
| sympy_str                  | 278 ms                                                                                                          | 318 ms: 1.14x slower                                                                                                  |
| pprint_pformat             | 1.48 sec                                                                                                        | 1.69 sec: 1.14x slower                                                                                                |
| comprehensions             | 15.5 us                                                                                                         | 17.8 us: 1.14x slower                                                                                                 |
| spectral_norm              | 92.2 ms                                                                                                         | 105 ms: 1.14x slower                                                                                                  |
| chaos                      | 52.9 ms                                                                                                         | 60.5 ms: 1.14x slower                                                                                                 |
| sympy_sum                  | 158 ms                                                                                                          | 181 ms: 1.14x slower                                                                                                  |
| regex_effbot               | 2.63 ms                                                                                                         | 3.01 ms: 1.15x slower                                                                                                 |
| float                      | 73.3 ms                                                                                                         | 84.3 ms: 1.15x slower                                                                                                 |
| subparsers                 | 9.06 ms                                                                                                         | 10.4 ms: 1.15x slower                                                                                                 |
| async_tree_none            | 294 ms                                                                                                          | 339 ms: 1.15x slower                                                                                                  |
| deepcopy                   | 235 us                                                                                                          | 271 us: 1.15x slower                                                                                                  |
| mdp                        | 1.13 sec                                                                                                        | 1.31 sec: 1.16x slower                                                                                                |
| hexiom                     | 5.65 ms                                                                                                         | 6.57 ms: 1.16x slower                                                                                                 |
| scimark_sor                | 105 ms                                                                                                          | 122 ms: 1.16x slower                                                                                                  |
| xml_etree_generate         | 87.6 ms                                                                                                         | 102 ms: 1.17x slower                                                                                                  |
| go                         | 102 ms                                                                                                          | 120 ms: 1.17x slower                                                                                                  |
| logging_simple             | 6.05 us                                                                                                         | 7.12 us: 1.18x slower                                                                                                 |
| thrift                     | 788 us                                                                                                          | 928 us: 1.18x slower                                                                                                  |
| deepcopy_reduce            | 2.55 us                                                                                                         | 3.01 us: 1.18x slower                                                                                                 |
| raytrace                   | 248 ms                                                                                                          | 294 ms: 1.18x slower                                                                                                  |
| logging_format             | 6.84 us                                                                                                         | 8.11 us: 1.19x slower                                                                                                 |
| async_generators           | 347 ms                                                                                                          | 414 ms: 1.19x slower                                                                                                  |
| richards                   | 44.4 ms                                                                                                         | 52.9 ms: 1.19x slower                                                                                                 |
| pyflate                    | 386 ms                                                                                                          | 461 ms: 1.19x slower                                                                                                  |
| richards_super             | 50.8 ms                                                                                                         | 60.8 ms: 1.20x slower                                                                                                 |
| deepcopy_memo              | 26.6 us                                                                                                         | 31.8 us: 1.20x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.45 ms                                                                                                         | 1.74 ms: 1.20x slower                                                                                                 |
| nqueens                    | 73.1 ms                                                                                                         | 88.2 ms: 1.21x slower                                                                                                 |
| typing_runtime_protocols   | 120 us                                                                                                          | 146 us: 1.21x slower                                                                                                  |
| sqlglot_v2_parse           | 1.15 ms                                                                                                         | 1.41 ms: 1.22x slower                                                                                                 |
| generators                 | 27.4 ms                                                                                                         | 33.5 ms: 1.22x slower                                                                                                 |
| xml_etree_process          | 61.9 ms                                                                                                         | 76.0 ms: 1.23x slower                                                                                                 |
| docutils                   | 2.37 sec                                                                                                        | 2.92 sec: 1.24x slower                                                                                                |
| shortest_path              | 437 ms                                                                                                          | 540 ms: 1.24x slower                                                                                                  |
| scimark_monte_carlo        | 63.0 ms                                                                                                         | 78.1 ms: 1.24x slower                                                                                                 |
| python_startup             | 12.9 ms                                                                                                         | 16.1 ms: 1.24x slower                                                                                                 |
| connected_components       | 394 ms                                                                                                          | 492 ms: 1.25x slower                                                                                                  |
| fannkuch                   | 367 ms                                                                                                          | 462 ms: 1.26x slower                                                                                                  |
| meteor_contest             | 101 ms                                                                                                          | 128 ms: 1.27x slower                                                                                                  |
| python_startup_no_site     | 7.70 ms                                                                                                         | 9.91 ms: 1.29x slower                                                                                                 |
| crypto_pyaes               | 68.2 ms                                                                                                         | 88.5 ms: 1.30x slower                                                                                                 |
| mako                       | 12.1 ms                                                                                                         | 15.8 ms: 1.31x slower                                                                                                 |
| coverage                   | 85.5 ms                                                                                                         | 116 ms: 1.36x slower                                                                                                  |
| nbody                      | 89.7 ms                                                                                                         | 124 ms: 1.38x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.07x slower                                                                                                          |

- Geometric mean (including insignificant results): 1.107x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.19x