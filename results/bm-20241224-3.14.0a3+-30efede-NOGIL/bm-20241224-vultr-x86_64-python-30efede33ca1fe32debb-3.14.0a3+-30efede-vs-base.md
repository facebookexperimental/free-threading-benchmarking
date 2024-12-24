# Results vs. base

- fork: python
- ref: 30efede33ca1fe32debb
- machine: linux-x86_64
- commit hash: 30efede
- commit date: 2024-12-24
- overall geometric mean: 1.229x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.22x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | results/bm-20241224-3.14.0a3+-30efede/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json | results/bm-20241224-3.14.0a3+-30efede-NOGIL/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                                                            | 349 ms: 1.36x slower                                                                                                    |
| docutils       | 2.55 sec                                                                                                          | 3.01 sec: 1.18x slower                                                                                                  |
| sphinx         | 986 ms                                                                                                            | 1.16 sec: 1.18x slower                                                                                                  |
| Geometric mean | (ref)                                                                                                             | 1.24x slower                                                                                                            |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | results/bm-20241224-3.14.0a3+-30efede/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json | results/bm-20241224-3.14.0a3+-30efede-NOGIL/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| coroutines                 | 21.8 ms                                                                                                           | 23.9 ms: 1.10x slower                                                                                                   |
| async_tree_cpu_io_mixed_tg | 480 ms                                                                                                            | 566 ms: 1.18x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 496 ms                                                                                                            | 592 ms: 1.19x slower                                                                                                    |
| async_tree_io              | 634 ms                                                                                                            | 758 ms: 1.20x slower                                                                                                    |
| async_tree_io_tg           | 610 ms                                                                                                            | 736 ms: 1.21x slower                                                                                                    |
| async_tree_none_tg         | 258 ms                                                                                                            | 316 ms: 1.23x slower                                                                                                    |
| async_tree_none            | 279 ms                                                                                                            | 349 ms: 1.25x slower                                                                                                    |
| async_tree_memoization     | 335 ms                                                                                                            | 432 ms: 1.29x slower                                                                                                    |
| async_generators           | 353 ms                                                                                                            | 455 ms: 1.29x slower                                                                                                    |
| async_tree_memoization_tg  | 310 ms                                                                                                            | 404 ms: 1.30x slower                                                                                                    |
| Geometric mean             | (ref)                                                                                                             | 1.20x slower                                                                                                            |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | results/bm-20241224-3.14.0a3+-30efede/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json | results/bm-20241224-3.14.0a3+-30efede-NOGIL/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| pidigits       | 185 ms                                                                                                            | 181 ms: 1.02x faster                                                                                                    |
| nbody          | 90.4 ms                                                                                                           | 128 ms: 1.42x slower                                                                                                    |
| float          | 76.2 ms                                                                                                           | 113 ms: 1.48x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.27x slower                                                                                                            |

Benchmarks with tag 'regex':
============================

| Benchmark      | results/bm-20241224-3.14.0a3+-30efede/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json | results/bm-20241224-3.14.0a3+-30efede-NOGIL/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json |
|----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| regex_v8       | 24.4 ms                                                                                                           | 23.8 ms: 1.02x faster                                                                                                   |
| regex_effbot   | 2.71 ms                                                                                                           | 2.77 ms: 1.02x slower                                                                                                   |
| regex_dna      | 174 ms                                                                                                            | 182 ms: 1.05x slower                                                                                                    |
| regex_compile  | 127 ms                                                                                                            | 169 ms: 1.33x slower                                                                                                    |
| Geometric mean | (ref)                                                                                                             | 1.09x slower                                                                                                            |

Benchmarks with tag 'serialize':
================================

| Benchmark            | results/bm-20241224-3.14.0a3+-30efede/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json | results/bm-20241224-3.14.0a3+-30efede-NOGIL/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json |
|----------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| xml_etree_parse      | 128 ms                                                                                                            | 131 ms: 1.03x slower                                                                                                    |
| json_loads           | 26.3 us                                                                                                           | 28.1 us: 1.07x slower                                                                                                   |
| xml_etree_generate   | 83.4 ms                                                                                                           | 97.7 ms: 1.17x slower                                                                                                   |
| json_dumps           | 11.3 ms                                                                                                           | 13.8 ms: 1.22x slower                                                                                                   |
| xml_etree_process    | 58.0 ms                                                                                                           | 73.5 ms: 1.27x slower                                                                                                   |
| tomli_loads          | 1.92 sec                                                                                                          | 2.53 sec: 1.31x slower                                                                                                  |
| unpickle_pure_python | 213 us                                                                                                            | 329 us: 1.54x slower                                                                                                    |
| pickle_pure_python   | 311 us                                                                                                            | 498 us: 1.60x slower                                                                                                    |
| Geometric mean       | (ref)                                                                                                             | 1.23x slower                                                                                                            |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | results/bm-20241224-3.14.0a3+-30efede/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json | results/bm-20241224-3.14.0a3+-30efede-NOGIL/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json |
|------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                                                           | 15.7 ms: 1.06x slower                                                                                                   |
| python_startup_no_site | 7.51 ms                                                                                                           | 9.79 ms: 1.30x slower                                                                                                   |
| Geometric mean         | (ref)                                                                                                             | 1.18x slower                                                                                                            |

Benchmarks with tag 'template':
===============================

| Benchmark       | results/bm-20241224-3.14.0a3+-30efede/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json | results/bm-20241224-3.14.0a3+-30efede-NOGIL/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json |
|-----------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| genshi_xml      | 49.1 ms                                                                                                           | 63.1 ms: 1.28x slower                                                                                                   |
| django_template | 34.7 ms                                                                                                           | 49.4 ms: 1.43x slower                                                                                                   |
| mako            | 11.9 ms                                                                                                           | 17.0 ms: 1.43x slower                                                                                                   |
| genshi_text     | 21.3 ms                                                                                                           | 30.8 ms: 1.45x slower                                                                                                   |
| Geometric mean  | (ref)                                                                                                             | 1.40x slower                                                                                                            |

All benchmarks:
===============

| Benchmark                  | results/bm-20241224-3.14.0a3+-30efede/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json | results/bm-20241224-3.14.0a3+-30efede-NOGIL/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json |
|----------------------------|:-----------------------------------------------------------------------------------------------------------------:|:-----------------------------------------------------------------------------------------------------------------------:|
| gc_traversal               | 4.32 ms                                                                                                           | 3.19 ms: 1.35x faster                                                                                                   |
| sqlite_synth               | 2.20 us                                                                                                           | 2.14 us: 1.03x faster                                                                                                   |
| regex_v8                   | 24.4 ms                                                                                                           | 23.8 ms: 1.02x faster                                                                                                   |
| pidigits                   | 185 ms                                                                                                            | 181 ms: 1.02x faster                                                                                                    |
| create_gc_cycles           | 1.84 ms                                                                                                           | 1.81 ms: 1.01x faster                                                                                                   |
| regex_effbot               | 2.71 ms                                                                                                           | 2.77 ms: 1.02x slower                                                                                                   |
| xml_etree_parse            | 128 ms                                                                                                            | 131 ms: 1.03x slower                                                                                                    |
| json                       | 4.82 ms                                                                                                           | 5.02 ms: 1.04x slower                                                                                                   |
| regex_dna                  | 174 ms                                                                                                            | 182 ms: 1.05x slower                                                                                                    |
| python_startup             | 14.7 ms                                                                                                           | 15.7 ms: 1.06x slower                                                                                                   |
| json_loads                 | 26.3 us                                                                                                           | 28.1 us: 1.07x slower                                                                                                   |
| pathlib                    | 18.1 ms                                                                                                           | 19.6 ms: 1.08x slower                                                                                                   |
| mdp                        | 2.46 sec                                                                                                          | 2.68 sec: 1.09x slower                                                                                                  |
| coroutines                 | 21.8 ms                                                                                                           | 23.9 ms: 1.10x slower                                                                                                   |
| bench_mp_pool              | 89.7 ms                                                                                                           | 100 ms: 1.12x slower                                                                                                    |
| k_core                     | 2.06 sec                                                                                                          | 2.36 sec: 1.14x slower                                                                                                  |
| telco                      | 7.36 ms                                                                                                           | 8.54 ms: 1.16x slower                                                                                                   |
| xml_etree_generate         | 83.4 ms                                                                                                           | 97.7 ms: 1.17x slower                                                                                                   |
| bpe_tokeniser              | 4.28 sec                                                                                                          | 5.02 sec: 1.17x slower                                                                                                  |
| sphinx                     | 986 ms                                                                                                            | 1.16 sec: 1.18x slower                                                                                                  |
| async_tree_cpu_io_mixed_tg | 480 ms                                                                                                            | 566 ms: 1.18x slower                                                                                                    |
| docutils                   | 2.55 sec                                                                                                          | 3.01 sec: 1.18x slower                                                                                                  |
| spectral_norm              | 95.8 ms                                                                                                           | 113 ms: 1.18x slower                                                                                                    |
| async_tree_cpu_io_mixed    | 496 ms                                                                                                            | 592 ms: 1.19x slower                                                                                                    |
| async_tree_io              | 634 ms                                                                                                            | 758 ms: 1.20x slower                                                                                                    |
| dulwich_log                | 75.5 ms                                                                                                           | 90.7 ms: 1.20x slower                                                                                                   |
| async_tree_io_tg           | 610 ms                                                                                                            | 736 ms: 1.21x slower                                                                                                    |
| many_optionals             | 1.03 ms                                                                                                           | 1.24 ms: 1.21x slower                                                                                                   |
| scimark_fft                | 319 ms                                                                                                            | 386 ms: 1.21x slower                                                                                                    |
| json_dumps                 | 11.3 ms                                                                                                           | 13.8 ms: 1.22x slower                                                                                                   |
| async_tree_none_tg         | 258 ms                                                                                                            | 316 ms: 1.23x slower                                                                                                    |
| pylint                     | 281 ms                                                                                                            | 347 ms: 1.23x slower                                                                                                    |
| pycparser                  | 1.12 sec                                                                                                          | 1.39 sec: 1.24x slower                                                                                                  |
| scimark_sparse_mat_mult    | 4.46 ms                                                                                                           | 5.58 ms: 1.25x slower                                                                                                   |
| async_tree_none            | 279 ms                                                                                                            | 349 ms: 1.25x slower                                                                                                    |
| sympy_expand               | 460 ms                                                                                                            | 578 ms: 1.26x slower                                                                                                    |
| nqueens                    | 77.7 ms                                                                                                           | 98.2 ms: 1.26x slower                                                                                                   |
| sqlglot_optimize           | 52.1 ms                                                                                                           | 65.9 ms: 1.26x slower                                                                                                   |
| shortest_path              | 435 ms                                                                                                            | 551 ms: 1.27x slower                                                                                                    |
| xml_etree_process          | 58.0 ms                                                                                                           | 73.5 ms: 1.27x slower                                                                                                   |
| sympy_sum                  | 153 ms                                                                                                            | 194 ms: 1.27x slower                                                                                                    |
| sqlglot_normalize          | 104 ms                                                                                                            | 132 ms: 1.27x slower                                                                                                    |
| sympy_integrate            | 19.8 ms                                                                                                           | 25.3 ms: 1.28x slower                                                                                                   |
| coverage                   | 78.9 ms                                                                                                           | 101 ms: 1.28x slower                                                                                                    |
| connected_components       | 392 ms                                                                                                            | 503 ms: 1.28x slower                                                                                                    |
| genshi_xml                 | 49.1 ms                                                                                                           | 63.1 ms: 1.28x slower                                                                                                   |
| async_tree_memoization     | 335 ms                                                                                                            | 432 ms: 1.29x slower                                                                                                    |
| async_generators           | 353 ms                                                                                                            | 455 ms: 1.29x slower                                                                                                    |
| deepcopy                   | 254 us                                                                                                            | 327 us: 1.29x slower                                                                                                    |
| sympy_str                  | 273 ms                                                                                                            | 354 ms: 1.30x slower                                                                                                    |
| async_tree_memoization_tg  | 310 ms                                                                                                            | 404 ms: 1.30x slower                                                                                                    |
| python_startup_no_site     | 7.51 ms                                                                                                           | 9.79 ms: 1.30x slower                                                                                                   |
| tomli_loads                | 1.92 sec                                                                                                          | 2.53 sec: 1.31x slower                                                                                                  |
| meteor_contest             | 101 ms                                                                                                            | 133 ms: 1.31x slower                                                                                                    |
| subparsers                 | 21.7 ms                                                                                                           | 28.7 ms: 1.32x slower                                                                                                   |
| regex_compile              | 127 ms                                                                                                            | 169 ms: 1.33x slower                                                                                                    |
| typing_runtime_protocols   | 157 us                                                                                                            | 209 us: 1.33x slower                                                                                                    |
| crypto_pyaes               | 67.5 ms                                                                                                           | 90.3 ms: 1.34x slower                                                                                                   |
| deepcopy_reduce            | 2.57 us                                                                                                           | 3.45 us: 1.34x slower                                                                                                   |
| thrift                     | 730 us                                                                                                            | 984 us: 1.35x slower                                                                                                    |
| deepcopy_memo              | 30.2 us                                                                                                           | 40.8 us: 1.35x slower                                                                                                   |
| pprint_safe_repr           | 705 ms                                                                                                            | 960 ms: 1.36x slower                                                                                                    |
| 2to3                       | 256 ms                                                                                                            | 349 ms: 1.36x slower                                                                                                    |
| fannkuch                   | 362 ms                                                                                                            | 496 ms: 1.37x slower                                                                                                    |
| pprint_pformat             | 1.45 sec                                                                                                          | 2.00 sec: 1.38x slower                                                                                                  |
| generators                 | 27.7 ms                                                                                                           | 38.2 ms: 1.38x slower                                                                                                   |
| nbody                      | 90.4 ms                                                                                                           | 128 ms: 1.42x slower                                                                                                    |
| django_template            | 34.7 ms                                                                                                           | 49.4 ms: 1.43x slower                                                                                                   |
| sqlalchemy_declarative     | 128 ms                                                                                                            | 183 ms: 1.43x slower                                                                                                    |
| mako                       | 11.9 ms                                                                                                           | 17.0 ms: 1.43x slower                                                                                                   |
| sqlalchemy_imperative      | 19.4 ms                                                                                                           | 27.9 ms: 1.44x slower                                                                                                   |
| genshi_text                | 21.3 ms                                                                                                           | 30.8 ms: 1.45x slower                                                                                                   |
| scimark_lu                 | 109 ms                                                                                                            | 159 ms: 1.45x slower                                                                                                    |
| float                      | 76.2 ms                                                                                                           | 113 ms: 1.48x slower                                                                                                    |
| logging_simple             | 5.97 us                                                                                                           | 9.14 us: 1.53x slower                                                                                                   |
| pyflate                    | 420 ms                                                                                                            | 644 ms: 1.53x slower                                                                                                    |
| logging_format             | 6.62 us                                                                                                           | 10.2 us: 1.54x slower                                                                                                   |
| unpickle_pure_python       | 213 us                                                                                                            | 329 us: 1.54x slower                                                                                                    |
| richards_super             | 48.5 ms                                                                                                           | 75.2 ms: 1.55x slower                                                                                                   |
| richards                   | 42.5 ms                                                                                                           | 67.2 ms: 1.58x slower                                                                                                   |
| pickle_pure_python         | 311 us                                                                                                            | 498 us: 1.60x slower                                                                                                    |
| comprehensions             | 17.0 us                                                                                                           | 27.3 us: 1.60x slower                                                                                                   |
| hexiom                     | 5.90 ms                                                                                                           | 9.57 ms: 1.62x slower                                                                                                   |
| chaos                      | 57.6 ms                                                                                                           | 94.2 ms: 1.63x slower                                                                                                   |
| logging_silent             | 107 ns                                                                                                            | 177 ns: 1.65x slower                                                                                                    |
| scimark_monte_carlo        | 63.1 ms                                                                                                           | 106 ms: 1.68x slower                                                                                                    |
| sqlglot_transpile          | 1.58 ms                                                                                                           | 2.73 ms: 1.73x slower                                                                                                   |
| sqlglot_parse              | 1.27 ms                                                                                                           | 2.36 ms: 1.86x slower                                                                                                   |
| scimark_sor                | 115 ms                                                                                                            | 214 ms: 1.86x slower                                                                                                    |
| raytrace                   | 260 ms                                                                                                            | 487 ms: 1.88x slower                                                                                                    |
| go                         | 116 ms                                                                                                            | 238 ms: 2.05x slower                                                                                                    |
| deltablue                  | 3.15 ms                                                                                                           | 7.37 ms: 2.34x slower                                                                                                   |
| bench_thread_pool          | 1.04 ms                                                                                                           | 3.39 ms: 3.27x slower                                                                                                   |
| Geometric mean             | (ref)                                                                                                             | 1.31x slower                                                                                                            |

Benchmark hidden because not significant (2): xml_etree_iterparse, asyncio_websockets
Ignored benchmarks (1) of results/bm-20241224-3.14.0a3+-30efede-NOGIL/bm-20241224-vultr-x86_64-python-30efede33ca1fe32debb-3.14.0a3+-30efede.json: html5lib

- Geometric mean (including insignificant results): 1.229x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.24x
- 95% likely to have a slowdown of 1.24x
- 99% likely to have a slowdown of 1.22x

# Memory
- memory change: 1.19x