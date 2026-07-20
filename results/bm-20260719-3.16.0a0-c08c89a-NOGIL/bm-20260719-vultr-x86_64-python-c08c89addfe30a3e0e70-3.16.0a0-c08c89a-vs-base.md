# Results vs. base

- fork: python
- ref: c08c89addfe30a3e0e70
- machine: linux-x86_64
- commit hash: c08c89a
- commit date: 2026-07-19
- overall geometric mean: 1.108x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-NOGIL/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                                                          | 295 ms: 1.15x slower                                                                                                  |
| docutils       | 2.42 sec                                                                                                        | 2.97 sec: 1.23x slower                                                                                                |
| html5lib       | 59.9 ms                                                                                                         | 66.9 ms: 1.12x slower                                                                                                 |
| sphinx         | 990 ms                                                                                                          | 1.13 sec: 1.14x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.16x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-NOGIL/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 752 ms                                                                                                          | 685 ms: 1.10x faster                                                                                                  |
| asyncio_websockets         | 544 ms                                                                                                          | 513 ms: 1.06x faster                                                                                                  |
| coroutines                 | 23.4 ms                                                                                                         | 24.0 ms: 1.02x slower                                                                                                 |
| asyncio_tcp                | 447 ms                                                                                                          | 464 ms: 1.04x slower                                                                                                  |
| async_tree_memoization_tg  | 360 ms                                                                                                          | 391 ms: 1.09x slower                                                                                                  |
| async_tree_none_tg         | 295 ms                                                                                                          | 323 ms: 1.10x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg | 556 ms                                                                                                          | 609 ms: 1.10x slower                                                                                                  |
| async_tree_memoization     | 371 ms                                                                                                          | 416 ms: 1.12x slower                                                                                                  |
| async_generators           | 337 ms                                                                                                          | 388 ms: 1.15x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 542 ms                                                                                                          | 630 ms: 1.16x slower                                                                                                  |
| asyncio_tcp_ssl            | 1.45 sec                                                                                                        | 1.71 sec: 1.17x slower                                                                                                |
| async_tree_none            | 287 ms                                                                                                          | 338 ms: 1.18x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.07x slower                                                                                                          |

Benchmark hidden because not significant (1): async_tree_io

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-NOGIL/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 195 ms                                                                                                          | 205 ms: 1.05x slower                                                                                                  |
| float          | 73.6 ms                                                                                                         | 85.3 ms: 1.16x slower                                                                                                 |
| nbody          | 90.8 ms                                                                                                         | 127 ms: 1.40x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.20x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-NOGIL/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.6 ms                                                                                                         | 20.3 ms: 1.06x faster                                                                                                 |
| regex_dna      | 181 ms                                                                                                          | 178 ms: 1.01x faster                                                                                                  |
| regex_effbot   | 2.57 ms                                                                                                         | 2.88 ms: 1.12x slower                                                                                                 |
| regex_compile  | 148 ms                                                                                                          | 169 ms: 1.15x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.04x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-NOGIL/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pickle_dict          | 33.7 us                                                                                                         | 33.1 us: 1.02x faster                                                                                                 |
| xml_etree_parse      | 144 ms                                                                                                          | 141 ms: 1.02x faster                                                                                                  |
| pickle               | 12.9 us                                                                                                         | 13.1 us: 1.02x slower                                                                                                 |
| xml_etree_iterparse  | 90.3 ms                                                                                                         | 95.9 ms: 1.06x slower                                                                                                 |
| tomli_loads          | 1.81 sec                                                                                                        | 1.95 sec: 1.08x slower                                                                                                |
| unpickle_list        | 5.48 us                                                                                                         | 5.96 us: 1.09x slower                                                                                                 |
| json_dumps           | 9.80 ms                                                                                                         | 10.7 ms: 1.09x slower                                                                                                 |
| json_loads           | 27.5 us                                                                                                         | 30.3 us: 1.10x slower                                                                                                 |
| pickle_pure_python   | 310 us                                                                                                          | 342 us: 1.10x slower                                                                                                  |
| unpickle_pure_python | 214 us                                                                                                          | 239 us: 1.12x slower                                                                                                  |
| unpickle             | 15.3 us                                                                                                         | 17.2 us: 1.12x slower                                                                                                 |
| xml_etree_generate   | 85.7 ms                                                                                                         | 102 ms: 1.19x slower                                                                                                  |
| xml_etree_process    | 60.5 ms                                                                                                         | 75.0 ms: 1.24x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmark hidden because not significant (1): pickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-NOGIL/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 12.4 ms                                                                                                         | 15.7 ms: 1.26x slower                                                                                                 |
| python_startup_no_site | 7.04 ms                                                                                                         | 9.32 ms: 1.32x slower                                                                                                 |
| Geometric mean         | (ref)                                                                                                           | 1.29x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-NOGIL/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.0 ms                                                                                                         | 40.4 ms: 1.12x slower                                                                                                 |
| mako            | 12.0 ms                                                                                                         | 15.7 ms: 1.31x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.21x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260719-3.16.0a0-c08c89a/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json | results/bm-20260719-3.16.0a0-c08c89a-NOGIL/bm-20260719-vultr-x86_64-python-c08c89addfe30a3e0e70-3.16.0a0-c08c89a.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 274 ms                                                                                                          | 13.3 ms: 20.58x faster                                                                                                |
| gc_traversal               | 4.04 ms                                                                                                         | 1.78 ms: 2.26x faster                                                                                                 |
| create_gc_cycles           | 1.67 ms                                                                                                         | 1.38 ms: 1.21x faster                                                                                                 |
| sqlite_synth               | 2.22 us                                                                                                         | 1.95 us: 1.13x faster                                                                                                 |
| async_tree_io_tg           | 752 ms                                                                                                          | 685 ms: 1.10x faster                                                                                                  |
| regex_v8                   | 21.6 ms                                                                                                         | 20.3 ms: 1.06x faster                                                                                                 |
| asyncio_websockets         | 544 ms                                                                                                          | 513 ms: 1.06x faster                                                                                                  |
| pickle_dict                | 33.7 us                                                                                                         | 33.1 us: 1.02x faster                                                                                                 |
| xml_etree_parse            | 144 ms                                                                                                          | 141 ms: 1.02x faster                                                                                                  |
| regex_dna                  | 181 ms                                                                                                          | 178 ms: 1.01x faster                                                                                                  |
| pathlib                    | 17.9 ms                                                                                                         | 17.8 ms: 1.01x faster                                                                                                 |
| pickle                     | 12.9 us                                                                                                         | 13.1 us: 1.02x slower                                                                                                 |
| coroutines                 | 23.4 ms                                                                                                         | 24.0 ms: 1.02x slower                                                                                                 |
| pycparser                  | 1.10 sec                                                                                                        | 1.14 sec: 1.03x slower                                                                                                |
| asyncio_tcp                | 447 ms                                                                                                          | 464 ms: 1.04x slower                                                                                                  |
| dulwich_log                | 68.6 ms                                                                                                         | 71.7 ms: 1.05x slower                                                                                                 |
| bpe_tokeniser              | 4.19 sec                                                                                                        | 4.40 sec: 1.05x slower                                                                                                |
| pidigits                   | 195 ms                                                                                                          | 205 ms: 1.05x slower                                                                                                  |
| xml_etree_iterparse        | 90.3 ms                                                                                                         | 95.9 ms: 1.06x slower                                                                                                 |
| tomli_loads                | 1.81 sec                                                                                                        | 1.95 sec: 1.08x slower                                                                                                |
| json                       | 4.95 ms                                                                                                         | 5.36 ms: 1.08x slower                                                                                                 |
| async_tree_memoization_tg  | 360 ms                                                                                                          | 391 ms: 1.09x slower                                                                                                  |
| unpickle_list              | 5.48 us                                                                                                         | 5.96 us: 1.09x slower                                                                                                 |
| json_dumps                 | 9.80 ms                                                                                                         | 10.7 ms: 1.09x slower                                                                                                 |
| k_core                     | 2.07 sec                                                                                                        | 2.26 sec: 1.09x slower                                                                                                |
| async_tree_none_tg         | 295 ms                                                                                                          | 323 ms: 1.10x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg | 556 ms                                                                                                          | 609 ms: 1.10x slower                                                                                                  |
| json_loads                 | 27.5 us                                                                                                         | 30.3 us: 1.10x slower                                                                                                 |
| pickle_pure_python         | 310 us                                                                                                          | 342 us: 1.10x slower                                                                                                  |
| telco                      | 159 ms                                                                                                          | 175 ms: 1.10x slower                                                                                                  |
| many_optionals             | 910 us                                                                                                          | 1.01 ms: 1.11x slower                                                                                                 |
| scimark_fft                | 319 ms                                                                                                          | 354 ms: 1.11x slower                                                                                                  |
| unpickle_pure_python       | 214 us                                                                                                          | 239 us: 1.12x slower                                                                                                  |
| html5lib                   | 59.9 ms                                                                                                         | 66.9 ms: 1.12x slower                                                                                                 |
| bench_thread_pool          | 1.34 ms                                                                                                         | 1.50 ms: 1.12x slower                                                                                                 |
| regex_effbot               | 2.57 ms                                                                                                         | 2.88 ms: 1.12x slower                                                                                                 |
| django_template            | 36.0 ms                                                                                                         | 40.4 ms: 1.12x slower                                                                                                 |
| async_tree_memoization     | 371 ms                                                                                                          | 416 ms: 1.12x slower                                                                                                  |
| deltablue                  | 3.28 ms                                                                                                         | 3.69 ms: 1.12x slower                                                                                                 |
| unpickle                   | 15.3 us                                                                                                         | 17.2 us: 1.12x slower                                                                                                 |
| scimark_sor                | 109 ms                                                                                                          | 123 ms: 1.12x slower                                                                                                  |
| logging_silent             | 96.1 ns                                                                                                         | 108 ns: 1.13x slower                                                                                                  |
| pprint_safe_repr           | 724 ms                                                                                                          | 817 ms: 1.13x slower                                                                                                  |
| sqlglot_v2_optimize        | 51.0 ms                                                                                                         | 57.7 ms: 1.13x slower                                                                                                 |
| comprehensions             | 15.9 us                                                                                                         | 18.0 us: 1.13x slower                                                                                                 |
| sqlglot_v2_normalize       | 100 ms                                                                                                          | 114 ms: 1.14x slower                                                                                                  |
| sphinx                     | 990 ms                                                                                                          | 1.13 sec: 1.14x slower                                                                                                |
| sympy_expand               | 461 ms                                                                                                          | 526 ms: 1.14x slower                                                                                                  |
| generators                 | 29.0 ms                                                                                                         | 33.0 ms: 1.14x slower                                                                                                 |
| thrift                     | 796 us                                                                                                          | 909 us: 1.14x slower                                                                                                  |
| scimark_lu                 | 114 ms                                                                                                          | 131 ms: 1.14x slower                                                                                                  |
| sympy_sum                  | 157 ms                                                                                                          | 180 ms: 1.15x slower                                                                                                  |
| subparsers                 | 9.41 ms                                                                                                         | 10.8 ms: 1.15x slower                                                                                                 |
| regex_compile              | 148 ms                                                                                                          | 169 ms: 1.15x slower                                                                                                  |
| sympy_str                  | 274 ms                                                                                                          | 314 ms: 1.15x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.79 ms                                                                                                         | 5.50 ms: 1.15x slower                                                                                                 |
| chaos                      | 54.5 ms                                                                                                         | 62.6 ms: 1.15x slower                                                                                                 |
| async_generators           | 337 ms                                                                                                          | 388 ms: 1.15x slower                                                                                                  |
| 2to3                       | 256 ms                                                                                                          | 295 ms: 1.15x slower                                                                                                  |
| go                         | 105 ms                                                                                                          | 121 ms: 1.15x slower                                                                                                  |
| unpack_sequence            | 40.3 ns                                                                                                         | 46.4 ns: 1.15x slower                                                                                                 |
| mdp                        | 1.13 sec                                                                                                        | 1.30 sec: 1.15x slower                                                                                                |
| sympy_integrate            | 19.1 ms                                                                                                         | 22.0 ms: 1.15x slower                                                                                                 |
| pyflate                    | 402 ms                                                                                                          | 464 ms: 1.15x slower                                                                                                  |
| hexiom                     | 5.71 ms                                                                                                         | 6.60 ms: 1.16x slower                                                                                                 |
| pprint_pformat             | 1.46 sec                                                                                                        | 1.69 sec: 1.16x slower                                                                                                |
| logging_simple             | 6.04 us                                                                                                         | 7.00 us: 1.16x slower                                                                                                 |
| float                      | 73.6 ms                                                                                                         | 85.3 ms: 1.16x slower                                                                                                 |
| deepcopy_reduce            | 2.59 us                                                                                                         | 3.00 us: 1.16x slower                                                                                                 |
| async_tree_cpu_io_mixed    | 542 ms                                                                                                          | 630 ms: 1.16x slower                                                                                                  |
| pylint                     | 113 ms                                                                                                          | 132 ms: 1.17x slower                                                                                                  |
| asyncio_tcp_ssl            | 1.45 sec                                                                                                        | 1.71 sec: 1.17x slower                                                                                                |
| nqueens                    | 74.4 ms                                                                                                         | 87.4 ms: 1.18x slower                                                                                                 |
| async_tree_none            | 287 ms                                                                                                          | 338 ms: 1.18x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.48 ms                                                                                                         | 1.75 ms: 1.18x slower                                                                                                 |
| spectral_norm              | 92.4 ms                                                                                                         | 109 ms: 1.18x slower                                                                                                  |
| deepcopy                   | 235 us                                                                                                          | 279 us: 1.19x slower                                                                                                  |
| deepcopy_memo              | 26.7 us                                                                                                         | 31.7 us: 1.19x slower                                                                                                 |
| xml_etree_generate         | 85.7 ms                                                                                                         | 102 ms: 1.19x slower                                                                                                  |
| raytrace                   | 253 ms                                                                                                          | 304 ms: 1.20x slower                                                                                                  |
| logging_format             | 6.68 us                                                                                                         | 8.01 us: 1.20x slower                                                                                                 |
| typing_runtime_protocols   | 119 us                                                                                                          | 144 us: 1.21x slower                                                                                                  |
| shortest_path              | 443 ms                                                                                                          | 538 ms: 1.21x slower                                                                                                  |
| sqlglot_v2_parse           | 1.16 ms                                                                                                         | 1.41 ms: 1.22x slower                                                                                                 |
| docutils                   | 2.42 sec                                                                                                        | 2.97 sec: 1.23x slower                                                                                                |
| scimark_monte_carlo        | 64.0 ms                                                                                                         | 78.9 ms: 1.23x slower                                                                                                 |
| xml_etree_process          | 60.5 ms                                                                                                         | 75.0 ms: 1.24x slower                                                                                                 |
| fannkuch                   | 374 ms                                                                                                          | 465 ms: 1.24x slower                                                                                                  |
| connected_components       | 397 ms                                                                                                          | 495 ms: 1.25x slower                                                                                                  |
| richards_super             | 48.1 ms                                                                                                         | 60.0 ms: 1.25x slower                                                                                                 |
| meteor_contest             | 99.8 ms                                                                                                         | 125 ms: 1.25x slower                                                                                                  |
| python_startup             | 12.4 ms                                                                                                         | 15.7 ms: 1.26x slower                                                                                                 |
| richards                   | 42.0 ms                                                                                                         | 54.0 ms: 1.29x slower                                                                                                 |
| crypto_pyaes               | 69.4 ms                                                                                                         | 89.7 ms: 1.29x slower                                                                                                 |
| mako                       | 12.0 ms                                                                                                         | 15.7 ms: 1.31x slower                                                                                                 |
| python_startup_no_site     | 7.04 ms                                                                                                         | 9.32 ms: 1.32x slower                                                                                                 |
| coverage                   | 83.5 ms                                                                                                         | 114 ms: 1.36x slower                                                                                                  |
| nbody                      | 90.8 ms                                                                                                         | 127 ms: 1.40x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.08x slower                                                                                                          |

Benchmark hidden because not significant (2): async_tree_io, pickle_list

- Geometric mean (including insignificant results): 1.108x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.12x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.18x