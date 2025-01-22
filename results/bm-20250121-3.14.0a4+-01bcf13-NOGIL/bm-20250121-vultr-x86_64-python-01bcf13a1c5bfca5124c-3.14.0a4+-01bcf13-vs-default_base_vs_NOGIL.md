# Results vs. default_base_vs_NOGIL

- fork: python
- ref: 01bcf13a1c5bfca5124c
- machine: linux-x86_64
- commit hash: 01bcf13
- commit date: 2025-01-21
- overall geometric mean: 1.155x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.13x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 254 ms                                                                 | 311 ms: 1.23x slower                                                   |
| docutils       | 2.55 sec                                                               | 2.84 sec: 1.12x slower                                                 |
| sphinx         | 985 ms                                                                 | 1.13 sec: 1.15x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.16x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 608 ms                                                                 | 582 ms: 1.05x faster                                                   |
| async_tree_none_tg         | 256 ms                                                                 | 245 ms: 1.04x faster                                                   |
| async_tree_io              | 600 ms                                                                 | 613 ms: 1.02x slower                                                   |
| async_tree_cpu_io_mixed_tg | 476 ms                                                                 | 498 ms: 1.05x slower                                                   |
| async_tree_memoization_tg  | 302 ms                                                                 | 317 ms: 1.05x slower                                                   |
| async_tree_none            | 264 ms                                                                 | 287 ms: 1.09x slower                                                   |
| async_tree_cpu_io_mixed    | 488 ms                                                                 | 532 ms: 1.09x slower                                                   |
| async_tree_memoization     | 320 ms                                                                 | 353 ms: 1.10x slower                                                   |
| coroutines                 | 22.4 ms                                                                | 24.9 ms: 1.11x slower                                                  |
| async_generators           | 319 ms                                                                 | 374 ms: 1.17x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.05x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 196 ms                                                                 | 191 ms: 1.03x faster                                                   |
| float          | 70.0 ms                                                                | 78.0 ms: 1.11x slower                                                  |
| nbody          | 91.6 ms                                                                | 138 ms: 1.50x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.18x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 168 ms                                                                 | 182 ms: 1.08x slower                                                   |
| regex_effbot   | 2.57 ms                                                                | 2.80 ms: 1.09x slower                                                  |
| regex_compile  | 127 ms                                                                 | 159 ms: 1.25x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                           |

Benchmark hidden because not significant (1): regex_v8

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.8 ms                                                                | 88.6 ms: 1.02x faster                                                  |
| xml_etree_parse      | 129 ms                                                                 | 128 ms: 1.01x faster                                                   |
| json_loads           | 27.7 us                                                                | 30.4 us: 1.10x slower                                                  |
| json_dumps           | 11.4 ms                                                                | 13.0 ms: 1.14x slower                                                  |
| xml_etree_generate   | 83.2 ms                                                                | 98.6 ms: 1.18x slower                                                  |
| unpickle_pure_python | 224 us                                                                 | 274 us: 1.22x slower                                                   |
| xml_etree_process    | 60.6 ms                                                                | 74.7 ms: 1.23x slower                                                  |
| pickle_pure_python   | 317 us                                                                 | 392 us: 1.24x slower                                                   |
| tomli_loads          | 1.95 sec                                                               | 2.42 sec: 1.24x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.14x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 15.3 ms: 1.05x slower                                                  |
| python_startup_no_site | 7.43 ms                                                                | 9.59 ms: 1.29x slower                                                  |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 35.0 ms                                                                | 44.8 ms: 1.28x slower                                                  |
| genshi_xml      | 48.9 ms                                                                | 63.1 ms: 1.29x slower                                                  |
| mako            | 11.7 ms                                                                | 16.1 ms: 1.38x slower                                                  |
| genshi_text     | 21.3 ms                                                                | 29.7 ms: 1.39x slower                                                  |
| Geometric mean  | (ref)                                                                  | 1.33x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20250121-vultr-x86_64-python-29caec62ee0650493c83-3.14.0a4+-29caec6 | bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13 |
|----------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------------------:|
| create_gc_cycles           | 1.83 ms                                                                | 1.34 ms: 1.37x faster                                                  |
| gc_traversal               | 4.19 ms                                                                | 3.13 ms: 1.34x faster                                                  |
| sqlite_synth               | 2.22 us                                                                | 2.06 us: 1.08x faster                                                  |
| async_tree_io_tg           | 608 ms                                                                 | 582 ms: 1.05x faster                                                   |
| async_tree_none_tg         | 256 ms                                                                 | 245 ms: 1.04x faster                                                   |
| pidigits                   | 196 ms                                                                 | 191 ms: 1.03x faster                                                   |
| xml_etree_iterparse        | 90.8 ms                                                                | 88.6 ms: 1.02x faster                                                  |
| xml_etree_parse            | 129 ms                                                                 | 128 ms: 1.01x faster                                                   |
| pathlib                    | 18.3 ms                                                                | 18.6 ms: 1.02x slower                                                  |
| async_tree_io              | 600 ms                                                                 | 613 ms: 1.02x slower                                                   |
| async_tree_cpu_io_mixed_tg | 476 ms                                                                 | 498 ms: 1.05x slower                                                   |
| python_startup             | 14.6 ms                                                                | 15.3 ms: 1.05x slower                                                  |
| async_tree_memoization_tg  | 302 ms                                                                 | 317 ms: 1.05x slower                                                   |
| bench_mp_pool              | 88.7 ms                                                                | 95.7 ms: 1.08x slower                                                  |
| regex_dna                  | 168 ms                                                                 | 182 ms: 1.08x slower                                                   |
| json                       | 4.96 ms                                                                | 5.39 ms: 1.09x slower                                                  |
| async_tree_none            | 264 ms                                                                 | 287 ms: 1.09x slower                                                   |
| regex_effbot               | 2.57 ms                                                                | 2.80 ms: 1.09x slower                                                  |
| async_tree_cpu_io_mixed    | 488 ms                                                                 | 532 ms: 1.09x slower                                                   |
| pycparser                  | 1.12 sec                                                               | 1.22 sec: 1.09x slower                                                 |
| json_loads                 | 27.7 us                                                                | 30.4 us: 1.10x slower                                                  |
| async_tree_memoization     | 320 ms                                                                 | 353 ms: 1.10x slower                                                   |
| dulwich_log                | 75.9 ms                                                                | 84.4 ms: 1.11x slower                                                  |
| coroutines                 | 22.4 ms                                                                | 24.9 ms: 1.11x slower                                                  |
| float                      | 70.0 ms                                                                | 78.0 ms: 1.11x slower                                                  |
| docutils                   | 2.55 sec                                                               | 2.84 sec: 1.12x slower                                                 |
| bpe_tokeniser              | 4.23 sec                                                               | 4.81 sec: 1.14x slower                                                 |
| k_core                     | 2.04 sec                                                               | 2.33 sec: 1.14x slower                                                 |
| json_dumps                 | 11.4 ms                                                                | 13.0 ms: 1.14x slower                                                  |
| sphinx                     | 985 ms                                                                 | 1.13 sec: 1.15x slower                                                 |
| pylint                     | 279 ms                                                                 | 323 ms: 1.16x slower                                                   |
| async_generators           | 319 ms                                                                 | 374 ms: 1.17x slower                                                   |
| logging_silent             | 103 ns                                                                 | 121 ns: 1.17x slower                                                   |
| subparsers                 | 22.1 ms                                                                | 26.0 ms: 1.18x slower                                                  |
| many_optionals             | 1.03 ms                                                                | 1.21 ms: 1.18x slower                                                  |
| sqlglot_normalize          | 104 ms                                                                 | 123 ms: 1.18x slower                                                   |
| xml_etree_generate         | 83.2 ms                                                                | 98.6 ms: 1.18x slower                                                  |
| sqlglot_optimize           | 52.6 ms                                                                | 62.3 ms: 1.19x slower                                                  |
| mdp                        | 2.29 sec                                                               | 2.74 sec: 1.19x slower                                                 |
| generators                 | 27.7 ms                                                                | 33.4 ms: 1.20x slower                                                  |
| telco                      | 7.15 ms                                                                | 8.62 ms: 1.21x slower                                                  |
| pprint_safe_repr           | 700 ms                                                                 | 848 ms: 1.21x slower                                                   |
| logging_simple             | 6.34 us                                                                | 7.72 us: 1.22x slower                                                  |
| spectral_norm              | 93.5 ms                                                                | 114 ms: 1.22x slower                                                   |
| unpickle_pure_python       | 224 us                                                                 | 274 us: 1.22x slower                                                   |
| pprint_pformat             | 1.42 sec                                                               | 1.75 sec: 1.23x slower                                                 |
| 2to3                       | 254 ms                                                                 | 311 ms: 1.23x slower                                                   |
| pyflate                    | 421 ms                                                                 | 517 ms: 1.23x slower                                                   |
| logging_format             | 7.07 us                                                                | 8.71 us: 1.23x slower                                                  |
| xml_etree_process          | 60.6 ms                                                                | 74.7 ms: 1.23x slower                                                  |
| coverage                   | 80.5 ms                                                                | 99.3 ms: 1.23x slower                                                  |
| pickle_pure_python         | 317 us                                                                 | 392 us: 1.24x slower                                                   |
| scimark_sor                | 112 ms                                                                 | 139 ms: 1.24x slower                                                   |
| tomli_loads                | 1.95 sec                                                               | 2.42 sec: 1.24x slower                                                 |
| sympy_expand               | 457 ms                                                                 | 567 ms: 1.24x slower                                                   |
| sympy_sum                  | 154 ms                                                                 | 191 ms: 1.24x slower                                                   |
| regex_compile              | 127 ms                                                                 | 159 ms: 1.25x slower                                                   |
| sympy_integrate            | 19.8 ms                                                                | 24.7 ms: 1.25x slower                                                  |
| thrift                     | 740 us                                                                 | 927 us: 1.25x slower                                                   |
| sqlalchemy_imperative      | 19.6 ms                                                                | 24.6 ms: 1.26x slower                                                  |
| go                         | 113 ms                                                                 | 143 ms: 1.26x slower                                                   |
| sympy_str                  | 272 ms                                                                 | 344 ms: 1.26x slower                                                   |
| scimark_fft                | 313 ms                                                                 | 398 ms: 1.27x slower                                                   |
| chaos                      | 55.9 ms                                                                | 71.1 ms: 1.27x slower                                                  |
| sqlalchemy_declarative     | 129 ms                                                                 | 164 ms: 1.27x slower                                                   |
| scimark_lu                 | 111 ms                                                                 | 142 ms: 1.27x slower                                                   |
| deepcopy                   | 254 us                                                                 | 324 us: 1.28x slower                                                   |
| connected_components       | 388 ms                                                                 | 497 ms: 1.28x slower                                                   |
| django_template            | 35.0 ms                                                                | 44.8 ms: 1.28x slower                                                  |
| comprehensions             | 16.8 us                                                                | 21.5 us: 1.29x slower                                                  |
| shortest_path              | 427 ms                                                                 | 549 ms: 1.29x slower                                                   |
| nqueens                    | 77.2 ms                                                                | 99.3 ms: 1.29x slower                                                  |
| raytrace                   | 261 ms                                                                 | 337 ms: 1.29x slower                                                   |
| genshi_xml                 | 48.9 ms                                                                | 63.1 ms: 1.29x slower                                                  |
| python_startup_no_site     | 7.43 ms                                                                | 9.59 ms: 1.29x slower                                                  |
| crypto_pyaes               | 67.3 ms                                                                | 87.6 ms: 1.30x slower                                                  |
| sqlglot_transpile          | 1.52 ms                                                                | 1.99 ms: 1.31x slower                                                  |
| sqlglot_parse              | 1.22 ms                                                                | 1.60 ms: 1.31x slower                                                  |
| scimark_monte_carlo        | 62.5 ms                                                                | 83.0 ms: 1.33x slower                                                  |
| fannkuch                   | 372 ms                                                                 | 495 ms: 1.33x slower                                                   |
| hexiom                     | 5.74 ms                                                                | 7.64 ms: 1.33x slower                                                  |
| deepcopy_reduce            | 2.55 us                                                                | 3.40 us: 1.33x slower                                                  |
| meteor_contest             | 98.3 ms                                                                | 132 ms: 1.34x slower                                                   |
| deepcopy_memo              | 29.8 us                                                                | 40.0 us: 1.34x slower                                                  |
| richards                   | 41.6 ms                                                                | 55.9 ms: 1.34x slower                                                  |
| typing_runtime_protocols   | 157 us                                                                 | 212 us: 1.35x slower                                                   |
| richards_super             | 47.9 ms                                                                | 65.1 ms: 1.36x slower                                                  |
| scimark_sparse_mat_mult    | 4.33 ms                                                                | 5.93 ms: 1.37x slower                                                  |
| mako                       | 11.7 ms                                                                | 16.1 ms: 1.38x slower                                                  |
| genshi_text                | 21.3 ms                                                                | 29.7 ms: 1.39x slower                                                  |
| nbody                      | 91.6 ms                                                                | 138 ms: 1.50x slower                                                   |
| deltablue                  | 3.07 ms                                                                | 4.73 ms: 1.54x slower                                                  |
| bench_thread_pool          | 1.03 ms                                                                | 3.35 ms: 3.25x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.20x slower                                                           |

Benchmark hidden because not significant (2): regex_v8, asyncio_websockets
Ignored benchmarks (1) of results/bm-20250121-3.14.0a4+-01bcf13-NOGIL/bm-20250121-vultr-x86_64-python-01bcf13a1c5bfca5124c-3.14.0a4+-01bcf13.json: html5lib

- Geometric mean (including insignificant results): 1.155x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.17x
- 95% likely to have a slowdown of 1.16x
- 99% likely to have a slowdown of 1.13x

# Memory
- memory change: 1.20x