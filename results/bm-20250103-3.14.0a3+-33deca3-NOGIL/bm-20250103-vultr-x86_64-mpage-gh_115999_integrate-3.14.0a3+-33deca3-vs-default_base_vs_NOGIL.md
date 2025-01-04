# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_integrate
- machine: linux-x86_64
- commit hash: 33deca3
- commit date: 2025-01-03
- overall geometric mean: 1.136x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.11x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3+-f157485 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 312 ms: 1.22x slower                                                 |
| docutils       | 2.55 sec                                                               | 2.84 sec: 1.11x slower                                               |
| sphinx         | 983 ms                                                                 | 1.13 sec: 1.15x slower                                               |
| Geometric mean | (ref)                                                                  | 1.16x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3+-f157485 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_tree_none_tg         | 253 ms                                                                 | 234 ms: 1.08x faster                                                 |
| async_tree_io_tg           | 608 ms                                                                 | 587 ms: 1.04x faster                                                 |
| async_tree_io              | 617 ms                                                                 | 600 ms: 1.03x faster                                                 |
| asyncio_websockets         | 523 ms                                                                 | 519 ms: 1.01x faster                                                 |
| async_tree_cpu_io_mixed_tg | 473 ms                                                                 | 478 ms: 1.01x slower                                                 |
| async_tree_memoization_tg  | 303 ms                                                                 | 306 ms: 1.01x slower                                                 |
| async_tree_none            | 275 ms                                                                 | 278 ms: 1.01x slower                                                 |
| async_tree_memoization     | 331 ms                                                                 | 344 ms: 1.04x slower                                                 |
| async_tree_cpu_io_mixed    | 492 ms                                                                 | 512 ms: 1.04x slower                                                 |
| coroutines                 | 21.6 ms                                                                | 23.2 ms: 1.08x slower                                                |
| async_generators           | 357 ms                                                                 | 419 ms: 1.17x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.02x slower                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3+-f157485 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 185 ms                                                                 | 191 ms: 1.04x slower                                                 |
| float          | 72.8 ms                                                                | 79.1 ms: 1.09x slower                                                |
| nbody          | 92.5 ms                                                                | 132 ms: 1.42x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.17x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3+-f157485 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 2.84 ms                                                                | 2.72 ms: 1.04x faster                                                |
| regex_v8       | 24.4 ms                                                                | 23.8 ms: 1.02x faster                                                |
| regex_dna      | 182 ms                                                                 | 179 ms: 1.02x faster                                                 |
| regex_compile  | 127 ms                                                                 | 151 ms: 1.19x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3+-f157485 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.7 ms                                                                | 87.9 ms: 1.03x faster                                                |
| xml_etree_parse      | 129 ms                                                                 | 130 ms: 1.01x slower                                                 |
| json_loads           | 25.9 us                                                                | 27.5 us: 1.06x slower                                                |
| json_dumps           | 11.3 ms                                                                | 13.0 ms: 1.16x slower                                                |
| unpickle_pure_python | 215 us                                                                 | 249 us: 1.16x slower                                                 |
| xml_etree_generate   | 83.2 ms                                                                | 96.9 ms: 1.16x slower                                                |
| pickle_pure_python   | 317 us                                                                 | 373 us: 1.18x slower                                                 |
| xml_etree_process    | 57.9 ms                                                                | 69.0 ms: 1.19x slower                                                |
| tomli_loads          | 1.90 sec                                                               | 2.33 sec: 1.22x slower                                               |
| Geometric mean       | (ref)                                                                  | 1.12x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3+-f157485 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 15.5 ms: 1.06x slower                                                |
| python_startup_no_site | 7.47 ms                                                                | 9.71 ms: 1.30x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.17x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3+-f157485 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| django_template | 35.8 ms                                                                | 43.5 ms: 1.22x slower                                                |
| genshi_xml      | 49.4 ms                                                                | 61.2 ms: 1.24x slower                                                |
| genshi_text     | 21.6 ms                                                                | 28.5 ms: 1.32x slower                                                |
| mako            | 11.9 ms                                                                | 15.8 ms: 1.33x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.28x slower                                                         |

All benchmarks:
===============

| Benchmark                  | bm-20250103-vultr-x86_64-python-f1574859d7d6cd259f86-3.14.0a3+-f157485 | bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3 |
|----------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal               | 4.20 ms                                                                | 3.30 ms: 1.27x faster                                                |
| async_tree_none_tg         | 253 ms                                                                 | 234 ms: 1.08x faster                                                 |
| sqlite_synth               | 2.19 us                                                                | 2.06 us: 1.06x faster                                                |
| regex_effbot               | 2.84 ms                                                                | 2.72 ms: 1.04x faster                                                |
| async_tree_io_tg           | 608 ms                                                                 | 587 ms: 1.04x faster                                                 |
| xml_etree_iterparse        | 90.7 ms                                                                | 87.9 ms: 1.03x faster                                                |
| async_tree_io              | 617 ms                                                                 | 600 ms: 1.03x faster                                                 |
| regex_v8                   | 24.4 ms                                                                | 23.8 ms: 1.02x faster                                                |
| create_gc_cycles           | 1.84 ms                                                                | 1.80 ms: 1.02x faster                                                |
| regex_dna                  | 182 ms                                                                 | 179 ms: 1.02x faster                                                 |
| asyncio_websockets         | 523 ms                                                                 | 519 ms: 1.01x faster                                                 |
| async_tree_cpu_io_mixed_tg | 473 ms                                                                 | 478 ms: 1.01x slower                                                 |
| async_tree_memoization_tg  | 303 ms                                                                 | 306 ms: 1.01x slower                                                 |
| xml_etree_parse            | 129 ms                                                                 | 130 ms: 1.01x slower                                                 |
| async_tree_none            | 275 ms                                                                 | 278 ms: 1.01x slower                                                 |
| json                       | 4.75 ms                                                                | 4.84 ms: 1.02x slower                                                |
| pidigits                   | 185 ms                                                                 | 191 ms: 1.04x slower                                                 |
| pathlib                    | 18.0 ms                                                                | 18.7 ms: 1.04x slower                                                |
| async_tree_memoization     | 331 ms                                                                 | 344 ms: 1.04x slower                                                 |
| async_tree_cpu_io_mixed    | 492 ms                                                                 | 512 ms: 1.04x slower                                                 |
| python_startup             | 14.6 ms                                                                | 15.5 ms: 1.06x slower                                                |
| json_loads                 | 25.9 us                                                                | 27.5 us: 1.06x slower                                                |
| pycparser                  | 1.13 sec                                                               | 1.21 sec: 1.07x slower                                               |
| coroutines                 | 21.6 ms                                                                | 23.2 ms: 1.08x slower                                                |
| float                      | 72.8 ms                                                                | 79.1 ms: 1.09x slower                                                |
| dulwich_log                | 75.1 ms                                                                | 81.8 ms: 1.09x slower                                                |
| bench_mp_pool              | 88.9 ms                                                                | 97.8 ms: 1.10x slower                                                |
| bpe_tokeniser              | 4.30 sec                                                               | 4.76 sec: 1.11x slower                                               |
| docutils                   | 2.55 sec                                                               | 2.84 sec: 1.11x slower                                               |
| mdp                        | 2.33 sec                                                               | 2.60 sec: 1.12x slower                                               |
| spectral_norm              | 98.4 ms                                                                | 110 ms: 1.12x slower                                                 |
| logging_silent             | 104 ns                                                                 | 117 ns: 1.13x slower                                                 |
| k_core                     | 2.05 sec                                                               | 2.31 sec: 1.13x slower                                               |
| many_optionals             | 1.03 ms                                                                | 1.17 ms: 1.14x slower                                                |
| sphinx                     | 983 ms                                                                 | 1.13 sec: 1.15x slower                                               |
| generators                 | 27.3 ms                                                                | 31.6 ms: 1.15x slower                                                |
| json_dumps                 | 11.3 ms                                                                | 13.0 ms: 1.16x slower                                                |
| unpickle_pure_python       | 215 us                                                                 | 249 us: 1.16x slower                                                 |
| xml_etree_generate         | 83.2 ms                                                                | 96.9 ms: 1.16x slower                                                |
| pprint_safe_repr           | 701 ms                                                                 | 819 ms: 1.17x slower                                                 |
| pyflate                    | 418 ms                                                                 | 488 ms: 1.17x slower                                                 |
| pylint                     | 279 ms                                                                 | 326 ms: 1.17x slower                                                 |
| async_generators           | 357 ms                                                                 | 419 ms: 1.17x slower                                                 |
| subparsers                 | 21.9 ms                                                                | 25.7 ms: 1.17x slower                                                |
| pickle_pure_python         | 317 us                                                                 | 373 us: 1.18x slower                                                 |
| scimark_sor                | 115 ms                                                                 | 136 ms: 1.18x slower                                                 |
| sqlglot_normalize          | 103 ms                                                                 | 122 ms: 1.18x slower                                                 |
| go                         | 118 ms                                                                 | 140 ms: 1.19x slower                                                 |
| pprint_pformat             | 1.43 sec                                                               | 1.70 sec: 1.19x slower                                               |
| regex_compile              | 127 ms                                                                 | 151 ms: 1.19x slower                                                 |
| xml_etree_process          | 57.9 ms                                                                | 69.0 ms: 1.19x slower                                                |
| sqlglot_optimize           | 52.2 ms                                                                | 62.5 ms: 1.20x slower                                                |
| sympy_expand               | 461 ms                                                                 | 554 ms: 1.20x slower                                                 |
| telco                      | 7.24 ms                                                                | 8.73 ms: 1.20x slower                                                |
| scimark_fft                | 316 ms                                                                 | 382 ms: 1.21x slower                                                 |
| sympy_sum                  | 153 ms                                                                 | 186 ms: 1.21x slower                                                 |
| django_template            | 35.8 ms                                                                | 43.5 ms: 1.22x slower                                                |
| chaos                      | 58.6 ms                                                                | 71.3 ms: 1.22x slower                                                |
| 2to3                       | 256 ms                                                                 | 312 ms: 1.22x slower                                                 |
| tomli_loads                | 1.90 sec                                                               | 2.33 sec: 1.22x slower                                               |
| sympy_integrate            | 19.8 ms                                                                | 24.3 ms: 1.23x slower                                                |
| sympy_str                  | 274 ms                                                                 | 336 ms: 1.23x slower                                                 |
| nqueens                    | 79.1 ms                                                                | 97.6 ms: 1.23x slower                                                |
| deepcopy                   | 257 us                                                                 | 318 us: 1.23x slower                                                 |
| sqlglot_transpile          | 1.57 ms                                                                | 1.94 ms: 1.24x slower                                                |
| genshi_xml                 | 49.4 ms                                                                | 61.2 ms: 1.24x slower                                                |
| comprehensions             | 16.9 us                                                                | 21.0 us: 1.24x slower                                                |
| thrift                     | 745 us                                                                 | 926 us: 1.24x slower                                                 |
| coverage                   | 79.3 ms                                                                | 98.8 ms: 1.25x slower                                                |
| logging_simple             | 5.88 us                                                                | 7.35 us: 1.25x slower                                                |
| logging_format             | 6.63 us                                                                | 8.29 us: 1.25x slower                                                |
| shortest_path              | 432 ms                                                                 | 541 ms: 1.25x slower                                                 |
| typing_runtime_protocols   | 159 us                                                                 | 199 us: 1.25x slower                                                 |
| connected_components       | 391 ms                                                                 | 491 ms: 1.26x slower                                                 |
| hexiom                     | 5.95 ms                                                                | 7.51 ms: 1.26x slower                                                |
| raytrace                   | 262 ms                                                                 | 331 ms: 1.26x slower                                                 |
| deepcopy_reduce            | 2.63 us                                                                | 3.34 us: 1.27x slower                                                |
| sqlglot_parse              | 1.26 ms                                                                | 1.60 ms: 1.27x slower                                                |
| sqlalchemy_declarative     | 129 ms                                                                 | 163 ms: 1.27x slower                                                 |
| sqlalchemy_imperative      | 19.4 ms                                                                | 24.7 ms: 1.27x slower                                                |
| scimark_lu                 | 111 ms                                                                 | 142 ms: 1.28x slower                                                 |
| scimark_monte_carlo        | 64.3 ms                                                                | 82.3 ms: 1.28x slower                                                |
| meteor_contest             | 99.8 ms                                                                | 128 ms: 1.28x slower                                                 |
| deepcopy_memo              | 30.2 us                                                                | 38.7 us: 1.28x slower                                                |
| crypto_pyaes               | 66.7 ms                                                                | 86.7 ms: 1.30x slower                                                |
| python_startup_no_site     | 7.47 ms                                                                | 9.71 ms: 1.30x slower                                                |
| fannkuch                   | 368 ms                                                                 | 480 ms: 1.31x slower                                                 |
| scimark_sparse_mat_mult    | 4.30 ms                                                                | 5.67 ms: 1.32x slower                                                |
| genshi_text                | 21.6 ms                                                                | 28.5 ms: 1.32x slower                                                |
| richards                   | 42.2 ms                                                                | 56.0 ms: 1.33x slower                                                |
| mako                       | 11.9 ms                                                                | 15.8 ms: 1.33x slower                                                |
| richards_super             | 48.2 ms                                                                | 65.4 ms: 1.36x slower                                                |
| nbody                      | 92.5 ms                                                                | 132 ms: 1.42x slower                                                 |
| deltablue                  | 3.17 ms                                                                | 4.80 ms: 1.52x slower                                                |
| bench_thread_pool          | 1.04 ms                                                                | 3.34 ms: 3.22x slower                                                |
| Geometric mean             | (ref)                                                                  | 1.17x slower                                                         |
Ignored benchmarks (1) of results/bm-20250103-3.14.0a3+-33deca3-NOGIL/bm-20250103-vultr-x86_64-mpage-gh_115999_integrate-3.14.0a3+-33deca3.json: html5lib

- Geometric mean (including insignificant results): 1.136x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.13x
- 95% likely to have a slowdown of 1.12x
- 99% likely to have a slowdown of 1.11x

# Memory
- memory change: 1.20x