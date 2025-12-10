# Results vs. default_base_vs_NOGIL

- fork: colesbury
- ref: gh_142472_stackrefs
- machine: linux-x86_64
- commit hash: a2c45c6
- commit date: 2025-12-09
- overall geometric mean: 1.098x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 249 ms                                                                 | 277 ms: 1.12x slower                                                     |
| docutils       | 2.54 sec                                                               | 2.70 sec: 1.07x slower                                                   |
| html5lib       | 61.0 ms                                                                | 65.9 ms: 1.08x slower                                                    |
| sphinx         | 964 ms                                                                 | 1.08 sec: 1.12x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.10x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| asyncio_websockets         | 544 ms                                                                 | 510 ms: 1.07x faster                                                     |
| async_tree_io_tg           | 587 ms                                                                 | 611 ms: 1.04x slower                                                     |
| async_tree_memoization_tg  | 305 ms                                                                 | 329 ms: 1.08x slower                                                     |
| async_tree_none_tg         | 243 ms                                                                 | 269 ms: 1.11x slower                                                     |
| async_generators           | 342 ms                                                                 | 380 ms: 1.11x slower                                                     |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 540 ms: 1.12x slower                                                     |
| async_tree_io              | 549 ms                                                                 | 623 ms: 1.13x slower                                                     |
| async_tree_cpu_io_mixed    | 486 ms                                                                 | 560 ms: 1.15x slower                                                     |
| async_tree_memoization     | 302 ms                                                                 | 355 ms: 1.17x slower                                                     |
| async_tree_none            | 242 ms                                                                 | 287 ms: 1.19x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.09x slower                                                             |

Benchmark hidden because not significant (1): coroutines

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| float          | 69.9 ms                                                                | 72.3 ms: 1.03x slower                                                    |
| pidigits       | 196 ms                                                                 | 215 ms: 1.10x slower                                                     |
| nbody          | 88.3 ms                                                                | 121 ms: 1.37x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.16x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 23.3 ms                                                                | 22.1 ms: 1.05x faster                                                    |
| regex_dna      | 183 ms                                                                 | 181 ms: 1.01x faster                                                     |
| regex_effbot   | 2.87 ms                                                                | 2.87 ms: 1.00x faster                                                    |
| regex_compile  | 125 ms                                                                 | 141 ms: 1.13x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.02x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 130 ms                                                                 | 133 ms: 1.03x slower                                                     |
| tomli_loads          | 2.19 sec                                                               | 2.29 sec: 1.04x slower                                                   |
| pickle_pure_python   | 306 us                                                                 | 330 us: 1.08x slower                                                     |
| unpickle_pure_python | 211 us                                                                 | 233 us: 1.11x slower                                                     |
| xml_etree_iterparse  | 84.1 ms                                                                | 93.5 ms: 1.11x slower                                                    |
| json_dumps           | 9.66 ms                                                                | 10.7 ms: 1.11x slower                                                    |
| json_loads           | 28.3 us                                                                | 31.9 us: 1.13x slower                                                    |
| xml_etree_generate   | 81.8 ms                                                                | 95.3 ms: 1.17x slower                                                    |
| xml_etree_process    | 57.7 ms                                                                | 68.1 ms: 1.18x slower                                                    |
| Geometric mean       | (ref)                                                                  | 1.10x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 12.4 ms                                                                | 15.8 ms: 1.27x slower                                                    |
| python_startup_no_site | 7.30 ms                                                                | 9.70 ms: 1.33x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.30x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 49.2 ms                                                                | 56.9 ms: 1.15x slower                                                    |
| django_template | 34.4 ms                                                                | 40.4 ms: 1.17x slower                                                    |
| genshi_text     | 20.5 ms                                                                | 26.3 ms: 1.29x slower                                                    |
| mako            | 11.6 ms                                                                | 15.5 ms: 1.33x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.23x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20251209-vultr-x86_64-python-b20722c300a78c384620-3.15.0a2+-b20722c | bm-20251209-vultr-x86_64-colesbury-gh_142472_stackrefs-3.15.0a2+-a2c45c6 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| bench_mp_pool              | 298 ms                                                                 | 7.30 ms: 40.84x faster                                                   |
| gc_traversal               | 4.43 ms                                                                | 1.90 ms: 2.33x faster                                                    |
| create_gc_cycles           | 1.89 ms                                                                | 1.48 ms: 1.28x faster                                                    |
| sqlite_synth               | 2.27 us                                                                | 2.09 us: 1.09x faster                                                    |
| asyncio_websockets         | 544 ms                                                                 | 510 ms: 1.07x faster                                                     |
| regex_v8                   | 23.3 ms                                                                | 22.1 ms: 1.05x faster                                                    |
| regex_dna                  | 183 ms                                                                 | 181 ms: 1.01x faster                                                     |
| regex_effbot               | 2.87 ms                                                                | 2.87 ms: 1.00x faster                                                    |
| logging_silent             | 101 ns                                                                 | 103 ns: 1.02x slower                                                     |
| bpe_tokeniser              | 4.19 sec                                                               | 4.30 sec: 1.03x slower                                                   |
| xml_etree_parse            | 130 ms                                                                 | 133 ms: 1.03x slower                                                     |
| float                      | 69.9 ms                                                                | 72.3 ms: 1.03x slower                                                    |
| async_tree_io_tg           | 587 ms                                                                 | 611 ms: 1.04x slower                                                     |
| pycparser                  | 1.08 sec                                                               | 1.13 sec: 1.04x slower                                                   |
| tomli_loads                | 2.19 sec                                                               | 2.29 sec: 1.04x slower                                                   |
| pylint                     | 285 ms                                                                 | 302 ms: 1.06x slower                                                     |
| json                       | 5.14 ms                                                                | 5.45 ms: 1.06x slower                                                    |
| docutils                   | 2.54 sec                                                               | 2.70 sec: 1.07x slower                                                   |
| many_optionals             | 936 us                                                                 | 1.00 ms: 1.07x slower                                                    |
| dulwich_log                | 66.7 ms                                                                | 71.9 ms: 1.08x slower                                                    |
| async_tree_memoization_tg  | 305 ms                                                                 | 329 ms: 1.08x slower                                                     |
| pickle_pure_python         | 306 us                                                                 | 330 us: 1.08x slower                                                     |
| hexiom                     | 5.77 ms                                                                | 6.23 ms: 1.08x slower                                                    |
| html5lib                   | 61.0 ms                                                                | 65.9 ms: 1.08x slower                                                    |
| nqueens                    | 80.0 ms                                                                | 87.5 ms: 1.09x slower                                                    |
| scimark_sor                | 109 ms                                                                 | 120 ms: 1.10x slower                                                     |
| pidigits                   | 196 ms                                                                 | 215 ms: 1.10x slower                                                     |
| comprehensions             | 15.9 us                                                                | 17.4 us: 1.10x slower                                                    |
| chaos                      | 56.2 ms                                                                | 61.7 ms: 1.10x slower                                                    |
| sympy_expand               | 473 ms                                                                 | 520 ms: 1.10x slower                                                     |
| pprint_safe_repr           | 698 ms                                                                 | 767 ms: 1.10x slower                                                     |
| pyflate                    | 408 ms                                                                 | 451 ms: 1.10x slower                                                     |
| unpickle_pure_python       | 211 us                                                                 | 233 us: 1.11x slower                                                     |
| async_tree_none_tg         | 243 ms                                                                 | 269 ms: 1.11x slower                                                     |
| telco                      | 158 ms                                                                 | 175 ms: 1.11x slower                                                     |
| go                         | 106 ms                                                                 | 118 ms: 1.11x slower                                                     |
| async_generators           | 342 ms                                                                 | 380 ms: 1.11x slower                                                     |
| subparsers                 | 9.13 ms                                                                | 10.1 ms: 1.11x slower                                                    |
| xml_etree_iterparse        | 84.1 ms                                                                | 93.5 ms: 1.11x slower                                                    |
| json_dumps                 | 9.66 ms                                                                | 10.7 ms: 1.11x slower                                                    |
| thrift                     | 777 us                                                                 | 865 us: 1.11x slower                                                     |
| async_tree_cpu_io_mixed_tg | 484 ms                                                                 | 540 ms: 1.12x slower                                                     |
| deltablue                  | 3.38 ms                                                                | 3.77 ms: 1.12x slower                                                    |
| generators                 | 27.2 ms                                                                | 30.3 ms: 1.12x slower                                                    |
| 2to3                       | 249 ms                                                                 | 277 ms: 1.12x slower                                                     |
| bench_thread_pool          | 1.32 ms                                                                | 1.47 ms: 1.12x slower                                                    |
| pprint_pformat             | 1.42 sec                                                               | 1.59 sec: 1.12x slower                                                   |
| deepcopy                   | 243 us                                                                 | 272 us: 1.12x slower                                                     |
| scimark_fft                | 307 ms                                                                 | 344 ms: 1.12x slower                                                     |
| sphinx                     | 964 ms                                                                 | 1.08 sec: 1.12x slower                                                   |
| sympy_str                  | 273 ms                                                                 | 306 ms: 1.12x slower                                                     |
| json_loads                 | 28.3 us                                                                | 31.9 us: 1.13x slower                                                    |
| sqlglot_v2_normalize       | 101 ms                                                                 | 114 ms: 1.13x slower                                                     |
| deepcopy_memo              | 26.8 us                                                                | 30.3 us: 1.13x slower                                                    |
| deepcopy_reduce            | 2.57 us                                                                | 2.90 us: 1.13x slower                                                    |
| spectral_norm              | 95.3 ms                                                                | 108 ms: 1.13x slower                                                     |
| regex_compile              | 125 ms                                                                 | 141 ms: 1.13x slower                                                     |
| async_tree_io              | 549 ms                                                                 | 623 ms: 1.13x slower                                                     |
| mdp                        | 1.14 sec                                                               | 1.30 sec: 1.14x slower                                                   |
| sympy_integrate            | 19.0 ms                                                                | 21.6 ms: 1.14x slower                                                    |
| sympy_sum                  | 154 ms                                                                 | 176 ms: 1.14x slower                                                     |
| sqlglot_v2_optimize        | 50.4 ms                                                                | 57.7 ms: 1.14x slower                                                    |
| async_tree_cpu_io_mixed    | 486 ms                                                                 | 560 ms: 1.15x slower                                                     |
| logging_simple             | 5.86 us                                                                | 6.77 us: 1.15x slower                                                    |
| genshi_xml                 | 49.2 ms                                                                | 56.9 ms: 1.15x slower                                                    |
| raytrace                   | 255 ms                                                                 | 296 ms: 1.16x slower                                                     |
| sqlglot_v2_transpile       | 1.49 ms                                                                | 1.73 ms: 1.16x slower                                                    |
| xml_etree_generate         | 81.8 ms                                                                | 95.3 ms: 1.17x slower                                                    |
| logging_format             | 6.64 us                                                                | 7.76 us: 1.17x slower                                                    |
| fannkuch                   | 389 ms                                                                 | 456 ms: 1.17x slower                                                     |
| django_template            | 34.4 ms                                                                | 40.4 ms: 1.17x slower                                                    |
| async_tree_memoization     | 302 ms                                                                 | 355 ms: 1.17x slower                                                     |
| xml_etree_process          | 57.7 ms                                                                | 68.1 ms: 1.18x slower                                                    |
| k_core                     | 1.87 sec                                                               | 2.21 sec: 1.18x slower                                                   |
| async_tree_none            | 242 ms                                                                 | 287 ms: 1.19x slower                                                     |
| meteor_contest             | 99.8 ms                                                                | 119 ms: 1.19x slower                                                     |
| scimark_lu                 | 107 ms                                                                 | 128 ms: 1.20x slower                                                     |
| sqlglot_v2_parse           | 1.21 ms                                                                | 1.45 ms: 1.20x slower                                                    |
| richards_super             | 48.5 ms                                                                | 58.6 ms: 1.21x slower                                                    |
| richards                   | 42.2 ms                                                                | 51.1 ms: 1.21x slower                                                    |
| shortest_path              | 429 ms                                                                 | 521 ms: 1.21x slower                                                     |
| scimark_monte_carlo        | 63.2 ms                                                                | 76.7 ms: 1.21x slower                                                    |
| scimark_sparse_mat_mult    | 4.32 ms                                                                | 5.25 ms: 1.22x slower                                                    |
| connected_components       | 386 ms                                                                 | 473 ms: 1.23x slower                                                     |
| crypto_pyaes               | 69.5 ms                                                                | 85.3 ms: 1.23x slower                                                    |
| typing_runtime_protocols   | 153 us                                                                 | 190 us: 1.24x slower                                                     |
| python_startup             | 12.4 ms                                                                | 15.8 ms: 1.27x slower                                                    |
| genshi_text                | 20.5 ms                                                                | 26.3 ms: 1.29x slower                                                    |
| python_startup_no_site     | 7.30 ms                                                                | 9.70 ms: 1.33x slower                                                    |
| mako                       | 11.6 ms                                                                | 15.5 ms: 1.33x slower                                                    |
| coverage                   | 81.2 ms                                                                | 111 ms: 1.37x slower                                                     |
| nbody                      | 88.3 ms                                                                | 121 ms: 1.37x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.06x slower                                                             |

Benchmark hidden because not significant (2): coroutines, pathlib

- Geometric mean (including insignificant results): 1.098x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.11x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.19x