# Results vs. base

- fork: python
- ref: a7d5a6cc179e2eabd780
- machine: linux-x86_64
- commit hash: a7d5a6c
- commit date: 2026-05-23
- overall geometric mean: 1.097x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 1.18x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20260523-3.16.0a0-a7d5a6c/bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c.json | results/bm-20260523-3.16.0a0-a7d5a6c-NOGIL/bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| docutils       | 2.38 sec                                                                                                        | 2.96 sec: 1.24x slower                                                                                                |
| html5lib       | 60.6 ms                                                                                                         | 68.1 ms: 1.12x slower                                                                                                 |
| sphinx         | 986 ms                                                                                                          | 1.12 sec: 1.14x slower                                                                                                |
| Geometric mean | (ref)                                                                                                           | 1.17x slower                                                                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20260523-3.16.0a0-a7d5a6c/bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c.json | results/bm-20260523-3.16.0a0-a7d5a6c-NOGIL/bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| async_tree_io_tg           | 751 ms                                                                                                          | 691 ms: 1.09x faster                                                                                                  |
| asyncio_websockets         | 545 ms                                                                                                          | 510 ms: 1.07x faster                                                                                                  |
| async_tree_io              | 715 ms                                                                                                          | 708 ms: 1.01x faster                                                                                                  |
| coroutines                 | 24.3 ms                                                                                                         | 24.7 ms: 1.02x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 555 ms                                                                                                          | 576 ms: 1.04x slower                                                                                                  |
| async_tree_memoization_tg  | 367 ms                                                                                                          | 396 ms: 1.08x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 541 ms                                                                                                          | 592 ms: 1.09x slower                                                                                                  |
| async_tree_none_tg         | 296 ms                                                                                                          | 328 ms: 1.11x slower                                                                                                  |
| async_generators           | 347 ms                                                                                                          | 388 ms: 1.12x slower                                                                                                  |
| async_tree_memoization     | 374 ms                                                                                                          | 423 ms: 1.13x slower                                                                                                  |
| async_tree_none            | 288 ms                                                                                                          | 348 ms: 1.21x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.05x slower                                                                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20260523-3.16.0a0-a7d5a6c/bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c.json | results/bm-20260523-3.16.0a0-a7d5a6c-NOGIL/bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                                                                          | 188 ms: 1.02x slower                                                                                                  |
| float          | 75.2 ms                                                                                                         | 88.6 ms: 1.18x slower                                                                                                 |
| nbody          | 93.1 ms                                                                                                         | 127 ms: 1.36x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.18x slower                                                                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20260523-3.16.0a0-a7d5a6c/bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c.json | results/bm-20260523-3.16.0a0-a7d5a6c-NOGIL/bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c.json |
|----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 21.6 ms                                                                                                         | 20.3 ms: 1.06x faster                                                                                                 |
| regex_dna      | 182 ms                                                                                                          | 175 ms: 1.04x faster                                                                                                  |
| regex_effbot   | 2.85 ms                                                                                                         | 2.94 ms: 1.03x slower                                                                                                 |
| regex_compile  | 125 ms                                                                                                          | 144 ms: 1.15x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                           | 1.02x slower                                                                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20260523-3.16.0a0-a7d5a6c/bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c.json | results/bm-20260523-3.16.0a0-a7d5a6c-NOGIL/bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c.json |
|----------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 142 ms                                                                                                          | 140 ms: 1.02x faster                                                                                                  |
| xml_etree_iterparse  | 90.1 ms                                                                                                         | 95.2 ms: 1.06x slower                                                                                                 |
| tomli_loads          | 1.80 sec                                                                                                        | 1.92 sec: 1.07x slower                                                                                                |
| pickle_pure_python   | 317 us                                                                                                          | 343 us: 1.08x slower                                                                                                  |
| json_dumps           | 9.99 ms                                                                                                         | 11.1 ms: 1.11x slower                                                                                                 |
| unpickle_pure_python | 216 us                                                                                                          | 243 us: 1.12x slower                                                                                                  |
| json_loads           | 27.5 us                                                                                                         | 31.1 us: 1.13x slower                                                                                                 |
| xml_etree_generate   | 87.5 ms                                                                                                         | 102 ms: 1.17x slower                                                                                                  |
| xml_etree_process    | 61.9 ms                                                                                                         | 75.6 ms: 1.22x slower                                                                                                 |
| Geometric mean       | (ref)                                                                                                           | 1.10x slower                                                                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20260523-3.16.0a0-a7d5a6c/bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c.json | results/bm-20260523-3.16.0a0-a7d5a6c-NOGIL/bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c.json |
|-----------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| django_template | 35.9 ms                                                                                                         | 40.6 ms: 1.13x slower                                                                                                 |
| mako            | 12.1 ms                                                                                                         | 16.0 ms: 1.32x slower                                                                                                 |
| Geometric mean  | (ref)                                                                                                           | 1.22x slower                                                                                                          |

All benchmarks:
===============

| Benchmark                  | results/bm-20260523-3.16.0a0-a7d5a6c/bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c.json | results/bm-20260523-3.16.0a0-a7d5a6c-NOGIL/bm-20260523-vultr-x86_64-python-a7d5a6cc179e2eabd780-3.16.0a0-a7d5a6c.json |
|----------------------------|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| bench_mp_pool              | 331 ms                                                                                                          | 6.98 ms: 47.38x faster                                                                                                |
| gc_traversal               | 3.83 ms                                                                                                         | 1.94 ms: 1.97x faster                                                                                                 |
| create_gc_cycles           | 1.82 ms                                                                                                         | 1.53 ms: 1.19x faster                                                                                                 |
| sqlite_synth               | 2.22 us                                                                                                         | 1.95 us: 1.14x faster                                                                                                 |
| async_tree_io_tg           | 751 ms                                                                                                          | 691 ms: 1.09x faster                                                                                                  |
| asyncio_websockets         | 545 ms                                                                                                          | 510 ms: 1.07x faster                                                                                                  |
| regex_v8                   | 21.6 ms                                                                                                         | 20.3 ms: 1.06x faster                                                                                                 |
| pycparser                  | 1.18 sec                                                                                                        | 1.14 sec: 1.04x faster                                                                                                |
| regex_dna                  | 182 ms                                                                                                          | 175 ms: 1.04x faster                                                                                                  |
| xml_etree_parse            | 142 ms                                                                                                          | 140 ms: 1.02x faster                                                                                                  |
| async_tree_io              | 715 ms                                                                                                          | 708 ms: 1.01x faster                                                                                                  |
| coroutines                 | 24.3 ms                                                                                                         | 24.7 ms: 1.02x slower                                                                                                 |
| pidigits                   | 184 ms                                                                                                          | 188 ms: 1.02x slower                                                                                                  |
| logging_silent             | 99.4 ns                                                                                                         | 102 ns: 1.03x slower                                                                                                  |
| pathlib                    | 17.6 ms                                                                                                         | 18.1 ms: 1.03x slower                                                                                                 |
| regex_effbot               | 2.85 ms                                                                                                         | 2.94 ms: 1.03x slower                                                                                                 |
| async_tree_cpu_io_mixed_tg | 555 ms                                                                                                          | 576 ms: 1.04x slower                                                                                                  |
| bpe_tokeniser              | 4.22 sec                                                                                                        | 4.39 sec: 1.04x slower                                                                                                |
| dulwich_log                | 68.9 ms                                                                                                         | 72.0 ms: 1.04x slower                                                                                                 |
| json                       | 5.11 ms                                                                                                         | 5.36 ms: 1.05x slower                                                                                                 |
| telco                      | 165 ms                                                                                                          | 174 ms: 1.05x slower                                                                                                  |
| xml_etree_iterparse        | 90.1 ms                                                                                                         | 95.2 ms: 1.06x slower                                                                                                 |
| tomli_loads                | 1.80 sec                                                                                                        | 1.92 sec: 1.07x slower                                                                                                |
| scimark_fft                | 318 ms                                                                                                          | 343 ms: 1.08x slower                                                                                                  |
| async_tree_memoization_tg  | 367 ms                                                                                                          | 396 ms: 1.08x slower                                                                                                  |
| pickle_pure_python         | 317 us                                                                                                          | 343 us: 1.08x slower                                                                                                  |
| async_tree_cpu_io_mixed    | 541 ms                                                                                                          | 592 ms: 1.09x slower                                                                                                  |
| deltablue                  | 3.40 ms                                                                                                         | 3.73 ms: 1.10x slower                                                                                                 |
| comprehensions             | 16.1 us                                                                                                         | 17.6 us: 1.10x slower                                                                                                 |
| many_optionals             | 915 us                                                                                                          | 1.00 ms: 1.10x slower                                                                                                 |
| pprint_safe_repr           | 737 ms                                                                                                          | 812 ms: 1.10x slower                                                                                                  |
| k_core                     | 2.07 sec                                                                                                        | 2.28 sec: 1.10x slower                                                                                                |
| chaos                      | 56.0 ms                                                                                                         | 61.9 ms: 1.11x slower                                                                                                 |
| async_tree_none_tg         | 296 ms                                                                                                          | 328 ms: 1.11x slower                                                                                                  |
| bench_thread_pool          | 1.33 ms                                                                                                         | 1.48 ms: 1.11x slower                                                                                                 |
| json_dumps                 | 9.99 ms                                                                                                         | 11.1 ms: 1.11x slower                                                                                                 |
| pprint_pformat             | 1.50 sec                                                                                                        | 1.67 sec: 1.11x slower                                                                                                |
| scimark_sor                | 109 ms                                                                                                          | 121 ms: 1.12x slower                                                                                                  |
| async_generators           | 347 ms                                                                                                          | 388 ms: 1.12x slower                                                                                                  |
| spectral_norm              | 96.3 ms                                                                                                         | 108 ms: 1.12x slower                                                                                                  |
| pyflate                    | 414 ms                                                                                                          | 464 ms: 1.12x slower                                                                                                  |
| html5lib                   | 60.6 ms                                                                                                         | 68.1 ms: 1.12x slower                                                                                                 |
| unpickle_pure_python       | 216 us                                                                                                          | 243 us: 1.12x slower                                                                                                  |
| subparsers                 | 9.43 ms                                                                                                         | 10.6 ms: 1.13x slower                                                                                                 |
| go                         | 108 ms                                                                                                          | 122 ms: 1.13x slower                                                                                                  |
| raytrace                   | 265 ms                                                                                                          | 299 ms: 1.13x slower                                                                                                  |
| logging_format             | 6.78 us                                                                                                         | 7.66 us: 1.13x slower                                                                                                 |
| sqlglot_v2_optimize        | 51.2 ms                                                                                                         | 57.9 ms: 1.13x slower                                                                                                 |
| django_template            | 35.9 ms                                                                                                         | 40.6 ms: 1.13x slower                                                                                                 |
| async_tree_memoization     | 374 ms                                                                                                          | 423 ms: 1.13x slower                                                                                                  |
| json_loads                 | 27.5 us                                                                                                         | 31.1 us: 1.13x slower                                                                                                 |
| logging_simple             | 5.94 us                                                                                                         | 6.73 us: 1.13x slower                                                                                                 |
| deepcopy_memo              | 27.6 us                                                                                                         | 31.3 us: 1.13x slower                                                                                                 |
| sqlglot_v2_normalize       | 101 ms                                                                                                          | 115 ms: 1.14x slower                                                                                                  |
| sphinx                     | 986 ms                                                                                                          | 1.12 sec: 1.14x slower                                                                                                |
| sympy_expand               | 469 ms                                                                                                          | 535 ms: 1.14x slower                                                                                                  |
| scimark_lu                 | 112 ms                                                                                                          | 128 ms: 1.14x slower                                                                                                  |
| hexiom                     | 5.67 ms                                                                                                         | 6.51 ms: 1.15x slower                                                                                                 |
| generators                 | 28.3 ms                                                                                                         | 32.5 ms: 1.15x slower                                                                                                 |
| thrift                     | 791 us                                                                                                          | 911 us: 1.15x slower                                                                                                  |
| regex_compile              | 125 ms                                                                                                          | 144 ms: 1.15x slower                                                                                                  |
| deepcopy                   | 234 us                                                                                                          | 271 us: 1.16x slower                                                                                                  |
| pylint                     | 114 ms                                                                                                          | 132 ms: 1.16x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.65 ms                                                                                                         | 5.38 ms: 1.16x slower                                                                                                 |
| mdp                        | 1.14 sec                                                                                                        | 1.32 sec: 1.16x slower                                                                                                |
| sympy_str                  | 273 ms                                                                                                          | 317 ms: 1.16x slower                                                                                                  |
| sympy_integrate            | 19.0 ms                                                                                                         | 22.0 ms: 1.16x slower                                                                                                 |
| deepcopy_reduce            | 2.55 us                                                                                                         | 2.97 us: 1.16x slower                                                                                                 |
| xml_etree_generate         | 87.5 ms                                                                                                         | 102 ms: 1.17x slower                                                                                                  |
| sympy_sum                  | 154 ms                                                                                                          | 180 ms: 1.17x slower                                                                                                  |
| float                      | 75.2 ms                                                                                                         | 88.6 ms: 1.18x slower                                                                                                 |
| nqueens                    | 74.1 ms                                                                                                         | 87.5 ms: 1.18x slower                                                                                                 |
| sqlglot_v2_transpile       | 1.46 ms                                                                                                         | 1.73 ms: 1.19x slower                                                                                                 |
| async_tree_none            | 288 ms                                                                                                          | 348 ms: 1.21x slower                                                                                                  |
| fannkuch                   | 387 ms                                                                                                          | 467 ms: 1.21x slower                                                                                                  |
| richards                   | 43.4 ms                                                                                                         | 52.6 ms: 1.21x slower                                                                                                 |
| sqlglot_v2_parse           | 1.15 ms                                                                                                         | 1.40 ms: 1.21x slower                                                                                                 |
| richards_super             | 49.6 ms                                                                                                         | 60.2 ms: 1.21x slower                                                                                                 |
| xml_etree_process          | 61.9 ms                                                                                                         | 75.6 ms: 1.22x slower                                                                                                 |
| typing_runtime_protocols   | 118 us                                                                                                          | 144 us: 1.22x slower                                                                                                  |
| scimark_monte_carlo        | 65.1 ms                                                                                                         | 79.7 ms: 1.22x slower                                                                                                 |
| shortest_path              | 434 ms                                                                                                          | 536 ms: 1.23x slower                                                                                                  |
| docutils                   | 2.38 sec                                                                                                        | 2.96 sec: 1.24x slower                                                                                                |
| meteor_contest             | 100.0 ms                                                                                                        | 126 ms: 1.26x slower                                                                                                  |
| connected_components       | 393 ms                                                                                                          | 495 ms: 1.26x slower                                                                                                  |
| crypto_pyaes               | 70.3 ms                                                                                                         | 89.9 ms: 1.28x slower                                                                                                 |
| mako                       | 12.1 ms                                                                                                         | 16.0 ms: 1.32x slower                                                                                                 |
| nbody                      | 93.1 ms                                                                                                         | 127 ms: 1.36x slower                                                                                                  |
| coverage                   | 83.7 ms                                                                                                         | 115 ms: 1.38x slower                                                                                                  |
| Geometric mean             | (ref)                                                                                                           | 1.06x slower                                                                                                          |

- Geometric mean (including insignificant results): 1.097x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 1.18x