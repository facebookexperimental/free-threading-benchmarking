# Results vs. base

- fork: python
- ref: 43c60ec2fddd316a4a6b
- machine: linux-x86_64
- commit hash: 43c60ec
- commit date: 2026-05-24
- overall geometric mean: 1.099x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260524-3.16.0a0-43c60ec/bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec.json | results/bm-20260524-3.16.0a0-43c60ec-NOGIL/bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| docutils       | 2.40 sec                                                                                                        | 2.97 sec: 1.24x slower                                                                                                |
| html5lib       | 60.2 ms                                                                                                         | 68.4 ms: 1.14x slower                                                                                                 |
| sphinx         | 984 ms                                                                                                          | 1.13 sec: 1.14x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.17x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260524-3.16.0a0-43c60ec/bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec.json | results/bm-20260524-3.16.0a0-43c60ec-NOGIL/bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 749 ms                                                                                                          | 691 ms: 1.08x faster                                                                                                  |
| asyncio_websockets         | 545 ms                                                                                                          | 510 ms: 1.07x faster                                                                                                  |
| async_tree_io              | 715 ms                                                                                                          | 709 ms: 1.01x faster                                                                                                  |
| coroutines                 | 24.4 ms                                                                                                         | 24.6 ms: 1.01x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 553 ms                                                                                                          | 578 ms: 1.05x slower                                                                                                  |
| async_tree_memoization_tg  | 365 ms                                                                                                          | 399 ms: 1.09x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 542 ms                                                                                                          | 594 ms: 1.10x slower                                                                                                  |
| async_tree_none_tg         | 296 ms                                                                                                          | 327 ms: 1.10x slower                                                                                                  |
| async_tree_memoization     | 379 ms                                                                                                          | 426 ms: 1.12x slower                                                                                                  |
| async_generators           | 343 ms                                                                                                          | 389 ms: 1.13x slower                                                                                                  |
| async_tree_none            | 294 ms                                                                                                          | 343 ms: 1.17x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.05x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260524-3.16.0a0-43c60ec/bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec.json | results/bm-20260524-3.16.0a0-43c60ec-NOGIL/bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                                                                          | 184 ms: 1.00x slower                                                                                                  |
| float          | 75.1 ms                                                                                                         | 88.6 ms: 1.18x slower                                                                                                 |
| nbody          | 93.6 ms                                                                                                         | 127 ms: 1.36x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.17x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260524-3.16.0a0-43c60ec/bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec.json | results/bm-20260524-3.16.0a0-43c60ec-NOGIL/bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.5 ms                                                                                                         | 20.3 ms: 1.06x faster                                                                                                 |
| regex_dna      | 182 ms                                                                                                          | 175 ms: 1.04x faster                                                                                                  |
| regex_effbot   | 2.83 ms                                                                                                         | 2.85 ms: 1.01x slower                                                                                                 |
| regex_compile  | 125 ms                                                                                                          | 144 ms: 1.15x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.01x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260524-3.16.0a0-43c60ec/bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec.json | results/bm-20260524-3.16.0a0-43c60ec-NOGIL/bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 143 ms                                                                                                          | 140 ms: 1.02x faster                                                                                                  |
| xml_etree_iterparse  | 90.3 ms                                                                                                         | 95.6 ms: 1.06x slower                                                                                                 |
| json_dumps           | 10.0 ms                                                                                                         | 10.8 ms: 1.08x slower                                                                                                 |
| tomli_loads          | 1.83 sec                                                                                                        | 1.98 sec: 1.08x slower                                                                                                |
| pickle_pure_python   | 318 us                                                                                                          | 346 us: 1.09x slower                                                                                                  |
| unpickle_pure_python | 215 us                                                                                                          | 242 us: 1.12x slower                                                                                                  |
| json_loads           | 27.6 us                                                                                                         | 31.0 us: 1.12x slower                                                                                                 |
| xml_etree_generate   | 87.1 ms                                                                                                         | 103 ms: 1.18x slower                                                                                                  |
| xml_etree_process    | 61.5 ms                                                                                                         | 76.0 ms: 1.23x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260524-3.16.0a0-43c60ec/bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec.json | results/bm-20260524-3.16.0a0-43c60ec-NOGIL/bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 36.1 ms                                                                                                         | 40.5 ms: 1.12x slower                                                                                                 |
| mako            | 12.0 ms                                                                                                         | 16.0 ms: 1.34x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.23x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260524-3.16.0a0-43c60ec/bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec.json | results/bm-20260524-3.16.0a0-43c60ec-NOGIL/bm-20260524-vultr-x86_64-python-43c60ec2fddd316a4a6b-3.16.0a0-43c60ec.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 246 ms                                                                                                          | 6.98 ms: 35.33x faster                                                                                                |
| gc_traversal               | 3.84 ms                                                                                                         | 1.96 ms: 1.96x faster                                                                                                 |
| create_gc_cycles           | 1.81 ms                                                                                                         | 1.54 ms: 1.18x faster                                                                                                 |
| sqlite_synth               | 2.24 us                                                                                                         | 1.93 us: 1.16x faster                                                                                                 |
| async_tree_io_tg           | 749 ms                                                                                                          | 691 ms: 1.08x faster                                                                                                  |
| asyncio_websockets         | 545 ms                                                                                                          | 510 ms: 1.07x faster                                                                                                  |
| regex_v8                   | 21.5 ms                                                                                                         | 20.3 ms: 1.06x faster                                                                                                 |
| pycparser                  | 1.18 sec                                                                                                        | 1.14 sec: 1.04x faster                                                                                                |
| regex_dna                  | 182 ms                                                                                                          | 175 ms: 1.04x faster                                                                                                  |
| xml_etree_parse            | 143 ms                                                                                                          | 140 ms: 1.02x faster                                                                                                  |
| async_tree_io              | 715 ms                                                                                                          | 709 ms: 1.01x faster                                                                                                  |
| pidigits                   | 184 ms                                                                                                          | 184 ms: 1.00x slower                                                                                                  |
| regex_effbot               | 2.83 ms                                                                                                         | 2.85 ms: 1.01x slower                                                                                                 |
| coroutines                 | 24.4 ms                                                                                                         | 24.6 ms: 1.01x slower                                                                                                 |
| pathlib                    | 17.9 ms                                                                                                         | 18.1 ms: 1.01x slower                                                                                                 |
| dulwich_log                | 69.0 ms                                                                                                         | 71.7 ms: 1.04x slower                                                                                                 |
| json                       | 5.15 ms                                                                                                         | 5.35 ms: 1.04x slower                                                                                                 |
| logging_silent             | 98.9 ns                                                                                                         | 103 ns: 1.04x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg | 553 ms                                                                                                          | 578 ms: 1.05x slower                                                                                                  |
| bpe_tokeniser              | 4.20 sec                                                                                                        | 4.42 sec: 1.05x slower                                                                                                |
| xml_etree_iterparse        | 90.3 ms                                                                                                         | 95.6 ms: 1.06x slower                                                                                                 |
| json_dumps                 | 10.0 ms                                                                                                         | 10.8 ms: 1.08x slower                                                                                                 |
| tomli_loads                | 1.83 sec                                                                                                        | 1.98 sec: 1.08x slower                                                                                                |
| pickle_pure_python         | 318 us                                                                                                          | 346 us: 1.09x slower                                                                                                  |
| k_core                     | 2.09 sec                                                                                                        | 2.27 sec: 1.09x slower                                                                                                |
| telco                      | 161 ms                                                                                                          | 176 ms: 1.09x slower                                                                                                  |
| scimark_sor                | 113 ms                                                                                                          | 124 ms: 1.09x slower                                                                                                  |
| async_tree_memoization_tg  | 365 ms                                                                                                          | 399 ms: 1.09x slower                                                                                                  |
| scimark_fft                | 320 ms                                                                                                          | 351 ms: 1.10x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 542 ms                                                                                                          | 594 ms: 1.10x slower                                                                                                  |
| deltablue                  | 3.39 ms                                                                                                         | 3.72 ms: 1.10x slower                                                                                                 |
| pprint_safe_repr           | 744 ms                                                                                                          | 819 ms: 1.10x slower                                                                                                  |
| async_tree_none_tg         | 296 ms                                                                                                          | 327 ms: 1.10x slower                                                                                                  |
| bench_thread_pool          | 1.33 ms                                                                                                         | 1.48 ms: 1.11x slower                                                                                                 |
| many_optionals             | 912 us                                                                                                          | 1.02 ms: 1.11x slower                                                                                                 |
| pprint_pformat             | 1.51 sec                                                                                                        | 1.69 sec: 1.11x slower                                                                                                |
| hexiom                     | 5.87 ms                                                                                                         | 6.56 ms: 1.12x slower                                                                                                 |
| comprehensions             | 16.0 us                                                                                                         | 17.9 us: 1.12x slower                                                                                                 |
| scimark_lu                 | 115 ms                                                                                                          | 128 ms: 1.12x slower                                                                                                  |
| unpickle_pure_python       | 215 us                                                                                                          | 242 us: 1.12x slower                                                                                                  |
| json_loads                 | 27.6 us                                                                                                         | 31.0 us: 1.12x slower                                                                                                 |
| django_template            | 36.1 ms                                                                                                         | 40.5 ms: 1.12x slower                                                                                                 |
| sympy_expand               | 479 ms                                                                                                          | 539 ms: 1.12x slower                                                                                                  |
| async_tree_memoization     | 379 ms                                                                                                          | 426 ms: 1.12x slower                                                                                                  |
| go                         | 108 ms                                                                                                          | 122 ms: 1.13x slower                                                                                                  |
| pyflate                    | 411 ms                                                                                                          | 466 ms: 1.13x slower                                                                                                  |
| sqlglot_v2_optimize        | 51.4 ms                                                                                                         | 58.2 ms: 1.13x slower                                                                                                 |
| async_generators           | 343 ms                                                                                                          | 389 ms: 1.13x slower                                                                                                  |
| chaos                      | 56.3 ms                                                                                                         | 63.9 ms: 1.14x slower                                                                                                 |
| html5lib                   | 60.2 ms                                                                                                         | 68.4 ms: 1.14x slower                                                                                                 |
| scimark_sparse_mat_mult    | 4.67 ms                                                                                                         | 5.32 ms: 1.14x slower                                                                                                 |
| thrift                     | 801 us                                                                                                          | 912 us: 1.14x slower                                                                                                  |
| sqlglot_v2_normalize       | 101 ms                                                                                                          | 115 ms: 1.14x slower                                                                                                  |
| subparsers                 | 9.46 ms                                                                                                         | 10.8 ms: 1.14x slower                                                                                                 |
| sympy_str                  | 277 ms                                                                                                          | 316 ms: 1.14x slower                                                                                                  |
| sphinx                     | 984 ms                                                                                                          | 1.13 sec: 1.14x slower                                                                                                |
| deepcopy_reduce            | 2.62 us                                                                                                         | 3.00 us: 1.15x slower                                                                                                 |
| regex_compile              | 125 ms                                                                                                          | 144 ms: 1.15x slower                                                                                                  |
| deepcopy                   | 237 us                                                                                                          | 273 us: 1.15x slower                                                                                                  |
| mdp                        | 1.14 sec                                                                                                        | 1.32 sec: 1.16x slower                                                                                                |
| sympy_integrate            | 19.2 ms                                                                                                         | 22.2 ms: 1.16x slower                                                                                                 |
| logging_simple             | 5.93 us                                                                                                         | 6.86 us: 1.16x slower                                                                                                 |
| sympy_sum                  | 156 ms                                                                                                          | 181 ms: 1.16x slower                                                                                                  |
| deepcopy_memo              | 27.4 us                                                                                                         | 31.8 us: 1.16x slower                                                                                                 |
| raytrace                   | 262 ms                                                                                                          | 304 ms: 1.16x slower                                                                                                  |
| logging_format             | 6.73 us                                                                                                         | 7.83 us: 1.16x slower                                                                                                 |
| pylint                     | 114 ms                                                                                                          | 133 ms: 1.17x slower                                                                                                  |
| async_tree_none            | 294 ms                                                                                                          | 343 ms: 1.17x slower                                                                                                  |
| float                      | 75.1 ms                                                                                                         | 88.6 ms: 1.18x slower                                                                                                 |
| xml_etree_generate         | 87.1 ms                                                                                                         | 103 ms: 1.18x slower                                                                                                  |
| sqlglot_v2_transpile       | 1.47 ms                                                                                                         | 1.74 ms: 1.19x slower                                                                                                 |
| spectral_norm              | 93.1 ms                                                                                                         | 111 ms: 1.19x slower                                                                                                  |
| nqueens                    | 74.0 ms                                                                                                         | 88.8 ms: 1.20x slower                                                                                                 |
| typing_runtime_protocols   | 119 us                                                                                                          | 143 us: 1.20x slower                                                                                                  |
| richards                   | 43.5 ms                                                                                                         | 52.3 ms: 1.20x slower                                                                                                 |
| richards_super             | 49.7 ms                                                                                                         | 60.0 ms: 1.21x slower                                                                                                 |
| sqlglot_v2_parse           | 1.16 ms                                                                                                         | 1.41 ms: 1.22x slower                                                                                                 |
| shortest_path              | 438 ms                                                                                                          | 535 ms: 1.22x slower                                                                                                  |
| fannkuch                   | 378 ms                                                                                                          | 465 ms: 1.23x slower                                                                                                  |
| xml_etree_process          | 61.5 ms                                                                                                         | 76.0 ms: 1.23x slower                                                                                                 |
| scimark_monte_carlo        | 64.6 ms                                                                                                         | 79.9 ms: 1.24x slower                                                                                                 |
| generators                 | 27.4 ms                                                                                                         | 33.9 ms: 1.24x slower                                                                                                 |
| docutils                   | 2.40 sec                                                                                                        | 2.97 sec: 1.24x slower                                                                                                |
| connected_components       | 395 ms                                                                                                          | 492 ms: 1.25x slower                                                                                                  |
| crypto_pyaes               | 69.1 ms                                                                                                         | 89.2 ms: 1.29x slower                                                                                                 |
| meteor_contest             | 99.3 ms                                                                                                         | 129 ms: 1.30x slower                                                                                                  |
| mako                       | 12.0 ms                                                                                                         | 16.0 ms: 1.34x slower                                                                                                 |
| nbody                      | 93.6 ms                                                                                                         | 127 ms: 1.36x slower                                                                                                  |
| coverage                   | 84.0 ms                                                                                                         | 115 ms: 1.37x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.06x slower                                                                                                          |

- Geometric mean (including insignificant results): 1.099x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.19x