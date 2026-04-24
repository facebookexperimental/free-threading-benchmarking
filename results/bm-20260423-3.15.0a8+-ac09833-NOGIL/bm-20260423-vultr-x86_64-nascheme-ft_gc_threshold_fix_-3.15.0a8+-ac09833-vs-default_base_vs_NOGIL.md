# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: ft_gc_threshold_fix_
- machine: linux-x86_64
- commit hash: ac09833
- commit date: 2026-04-23
- overall geometric mean: 1.101x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.10x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8+-448d7b9 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 287 ms: 1.12x slower                                                     |
| docutils       | 2.46 sec                                                               | 2.76 sec: 1.12x slower                                                   |
| html5lib       | 60.4 ms                                                                | 68.9 ms: 1.14x slower                                                    |
| sphinx         | 952 ms                                                                 | 1.07 sec: 1.13x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8+-448d7b9 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| asyncio_websockets         | 545 ms                                                                 | 513 ms: 1.06x faster                                                     |
| coroutines                 | 23.3 ms                                                                | 24.6 ms: 1.06x slower                                                    |
| async_tree_io_tg           | 591 ms                                                                 | 646 ms: 1.09x slower                                                     |
| async_generators           | 345 ms                                                                 | 379 ms: 1.10x slower                                                     |
| async_tree_cpu_io_mixed_tg | 494 ms                                                                 | 545 ms: 1.10x slower                                                     |
| async_tree_io              | 582 ms                                                                 | 650 ms: 1.12x slower                                                     |
| async_tree_cpu_io_mixed    | 499 ms                                                                 | 570 ms: 1.14x slower                                                     |
| async_tree_none_tg         | 251 ms                                                                 | 293 ms: 1.17x slower                                                     |
| async_tree_memoization_tg  | 305 ms                                                                 | 357 ms: 1.17x slower                                                     |
| async_tree_memoization     | 313 ms                                                                 | 382 ms: 1.22x slower                                                     |
| async_tree_none            | 247 ms                                                                 | 309 ms: 1.25x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.12x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8+-448d7b9 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 185 ms                                                                 | 180 ms: 1.02x faster                                                     |
| float          | 70.9 ms                                                                | 77.9 ms: 1.10x slower                                                    |
| nbody          | 92.4 ms                                                                | 122 ms: 1.32x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8+-448d7b9 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_v8       | 22.0 ms                                                                | 21.5 ms: 1.02x faster                                                    |
| regex_dna      | 169 ms                                                                 | 184 ms: 1.09x slower                                                     |
| regex_effbot   | 2.76 ms                                                                | 3.06 ms: 1.11x slower                                                    |
| regex_compile  | 124 ms                                                                 | 141 ms: 1.14x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.08x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8+-448d7b9 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 131 ms                                                                 | 134 ms: 1.02x slower                                                     |
| tomli_loads          | 1.86 sec                                                               | 1.92 sec: 1.03x slower                                                   |
| xml_etree_iterparse  | 84.5 ms                                                                | 87.1 ms: 1.03x slower                                                    |
| pickle_pure_python   | 310 us                                                                 | 336 us: 1.09x slower                                                     |
| json_dumps           | 9.74 ms                                                                | 10.7 ms: 1.09x slower                                                    |
| json_loads           | 27.7 us                                                                | 30.4 us: 1.10x slower                                                    |
| xml_etree_generate   | 86.8 ms                                                                | 95.4 ms: 1.10x slower                                                    |
| xml_etree_process    | 61.7 ms                                                                | 68.2 ms: 1.10x slower                                                    |
| unpickle_pure_python | 211 us                                                                 | 237 us: 1.12x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.08x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8+-448d7b9 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 12.3 ms                                                                | 15.5 ms: 1.25x slower                                                    |
| python_startup_no_site | 6.80 ms                                                                | 8.95 ms: 1.32x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.28x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8+-448d7b9 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| django_template | 36.0 ms                                                                | 39.0 ms: 1.08x slower                                                    |
| genshi_xml      | 50.0 ms                                                                | 54.3 ms: 1.08x slower                                                    |
| genshi_text     | 21.3 ms                                                                | 25.7 ms: 1.21x slower                                                    |
| mako            | 12.2 ms                                                                | 15.5 ms: 1.27x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.16x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20260423-vultr-x86_64-python-448d7b96c181d13ca7f8-3.15.0a8+-448d7b9 | bm-20260423-vultr-x86_64-nascheme-ft_gc_threshold_fix_-3.15.0a8+-ac09833 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| bench_mp_pool              | 260 ms                                                                 | 7.27 ms: 35.83x faster                                                   |
| gc_traversal               | 4.37 ms                                                                | 1.91 ms: 2.28x faster                                                    |
| create_gc_cycles           | 1.90 ms                                                                | 1.49 ms: 1.27x faster                                                    |
| sqlite_synth               | 2.21 us                                                                | 1.90 us: 1.17x faster                                                    |
| asyncio_websockets         | 545 ms                                                                 | 513 ms: 1.06x faster                                                     |
| regex_v8                   | 22.0 ms                                                                | 21.5 ms: 1.02x faster                                                    |
| pidigits                   | 185 ms                                                                 | 180 ms: 1.02x faster                                                     |
| dulwich_log                | 68.4 ms                                                                | 69.6 ms: 1.02x slower                                                    |
| xml_etree_parse            | 131 ms                                                                 | 134 ms: 1.02x slower                                                     |
| pathlib                    | 17.3 ms                                                                | 17.7 ms: 1.02x slower                                                    |
| tomli_loads                | 1.86 sec                                                               | 1.92 sec: 1.03x slower                                                   |
| json                       | 5.09 ms                                                                | 5.24 ms: 1.03x slower                                                    |
| xml_etree_iterparse        | 84.5 ms                                                                | 87.1 ms: 1.03x slower                                                    |
| pycparser                  | 1.08 sec                                                               | 1.12 sec: 1.04x slower                                                   |
| logging_silent             | 100 ns                                                                 | 104 ns: 1.04x slower                                                     |
| bpe_tokeniser              | 4.14 sec                                                               | 4.32 sec: 1.04x slower                                                   |
| coroutines                 | 23.3 ms                                                                | 24.6 ms: 1.06x slower                                                    |
| scimark_fft                | 315 ms                                                                 | 337 ms: 1.07x slower                                                     |
| many_optionals             | 947 us                                                                 | 1.02 ms: 1.08x slower                                                    |
| sympy_expand               | 482 ms                                                                 | 520 ms: 1.08x slower                                                     |
| django_template            | 36.0 ms                                                                | 39.0 ms: 1.08x slower                                                    |
| genshi_xml                 | 50.0 ms                                                                | 54.3 ms: 1.08x slower                                                    |
| telco                      | 159 ms                                                                 | 172 ms: 1.09x slower                                                     |
| regex_dna                  | 169 ms                                                                 | 184 ms: 1.09x slower                                                     |
| pickle_pure_python         | 310 us                                                                 | 336 us: 1.09x slower                                                     |
| generators                 | 29.3 ms                                                                | 32.0 ms: 1.09x slower                                                    |
| async_tree_io_tg           | 591 ms                                                                 | 646 ms: 1.09x slower                                                     |
| comprehensions             | 16.0 us                                                                | 17.6 us: 1.09x slower                                                    |
| json_dumps                 | 9.74 ms                                                                | 10.7 ms: 1.09x slower                                                    |
| json_loads                 | 27.7 us                                                                | 30.4 us: 1.10x slower                                                    |
| async_generators           | 345 ms                                                                 | 379 ms: 1.10x slower                                                     |
| deltablue                  | 3.32 ms                                                                | 3.64 ms: 1.10x slower                                                    |
| float                      | 70.9 ms                                                                | 77.9 ms: 1.10x slower                                                    |
| xml_etree_generate         | 86.8 ms                                                                | 95.4 ms: 1.10x slower                                                    |
| scimark_sor                | 108 ms                                                                 | 119 ms: 1.10x slower                                                     |
| sqlglot_v2_optimize        | 51.3 ms                                                                | 56.4 ms: 1.10x slower                                                    |
| pyflate                    | 412 ms                                                                 | 454 ms: 1.10x slower                                                     |
| async_tree_cpu_io_mixed_tg | 494 ms                                                                 | 545 ms: 1.10x slower                                                     |
| bench_thread_pool          | 1.32 ms                                                                | 1.46 ms: 1.10x slower                                                    |
| xml_etree_process          | 61.7 ms                                                                | 68.2 ms: 1.10x slower                                                    |
| regex_effbot               | 2.76 ms                                                                | 3.06 ms: 1.11x slower                                                    |
| sqlglot_v2_normalize       | 103 ms                                                                 | 114 ms: 1.11x slower                                                     |
| pprint_safe_repr           | 720 ms                                                                 | 800 ms: 1.11x slower                                                     |
| async_tree_io              | 582 ms                                                                 | 650 ms: 1.12x slower                                                     |
| scimark_lu                 | 110 ms                                                                 | 123 ms: 1.12x slower                                                     |
| docutils                   | 2.46 sec                                                               | 2.76 sec: 1.12x slower                                                   |
| unpickle_pure_python       | 211 us                                                                 | 237 us: 1.12x slower                                                     |
| 2to3                       | 255 ms                                                                 | 287 ms: 1.12x slower                                                     |
| subparsers                 | 9.16 ms                                                                | 10.3 ms: 1.12x slower                                                    |
| sympy_str                  | 277 ms                                                                 | 312 ms: 1.13x slower                                                     |
| sympy_sum                  | 157 ms                                                                 | 176 ms: 1.13x slower                                                     |
| sphinx                     | 952 ms                                                                 | 1.07 sec: 1.13x slower                                                   |
| pprint_pformat             | 1.47 sec                                                               | 1.66 sec: 1.13x slower                                                   |
| hexiom                     | 5.74 ms                                                                | 6.49 ms: 1.13x slower                                                    |
| pylint                     | 116 ms                                                                 | 131 ms: 1.13x slower                                                     |
| mdp                        | 1.15 sec                                                               | 1.31 sec: 1.14x slower                                                   |
| regex_compile              | 124 ms                                                                 | 141 ms: 1.14x slower                                                     |
| html5lib                   | 60.4 ms                                                                | 68.9 ms: 1.14x slower                                                    |
| nqueens                    | 75.5 ms                                                                | 86.3 ms: 1.14x slower                                                    |
| async_tree_cpu_io_mixed    | 499 ms                                                                 | 570 ms: 1.14x slower                                                     |
| sympy_integrate            | 19.1 ms                                                                | 21.8 ms: 1.14x slower                                                    |
| deepcopy_reduce            | 2.54 us                                                                | 2.91 us: 1.14x slower                                                    |
| chaos                      | 54.7 ms                                                                | 62.7 ms: 1.15x slower                                                    |
| go                         | 105 ms                                                                 | 121 ms: 1.15x slower                                                     |
| deepcopy                   | 231 us                                                                 | 267 us: 1.16x slower                                                     |
| sqlglot_v2_transpile       | 1.47 ms                                                                | 1.71 ms: 1.16x slower                                                    |
| async_tree_none_tg         | 251 ms                                                                 | 293 ms: 1.17x slower                                                     |
| sqlglot_v2_parse           | 1.17 ms                                                                | 1.36 ms: 1.17x slower                                                    |
| async_tree_memoization_tg  | 305 ms                                                                 | 357 ms: 1.17x slower                                                     |
| thrift                     | 761 us                                                                 | 893 us: 1.17x slower                                                     |
| deepcopy_memo              | 26.9 us                                                                | 31.5 us: 1.17x slower                                                    |
| spectral_norm              | 94.2 ms                                                                | 111 ms: 1.18x slower                                                     |
| k_core                     | 1.89 sec                                                               | 2.23 sec: 1.18x slower                                                   |
| logging_simple             | 5.68 us                                                                | 6.76 us: 1.19x slower                                                    |
| fannkuch                   | 385 ms                                                                 | 458 ms: 1.19x slower                                                     |
| logging_format             | 6.47 us                                                                | 7.70 us: 1.19x slower                                                    |
| raytrace                   | 253 ms                                                                 | 303 ms: 1.20x slower                                                     |
| scimark_sparse_mat_mult    | 4.46 ms                                                                | 5.36 ms: 1.20x slower                                                    |
| typing_runtime_protocols   | 161 us                                                                 | 194 us: 1.20x slower                                                     |
| genshi_text                | 21.3 ms                                                                | 25.7 ms: 1.21x slower                                                    |
| richards_super             | 48.9 ms                                                                | 59.5 ms: 1.22x slower                                                    |
| async_tree_memoization     | 313 ms                                                                 | 382 ms: 1.22x slower                                                     |
| scimark_monte_carlo        | 63.2 ms                                                                | 77.4 ms: 1.23x slower                                                    |
| shortest_path              | 434 ms                                                                 | 537 ms: 1.24x slower                                                     |
| richards                   | 42.6 ms                                                                | 52.7 ms: 1.24x slower                                                    |
| meteor_contest             | 102 ms                                                                 | 127 ms: 1.24x slower                                                     |
| crypto_pyaes               | 69.8 ms                                                                | 87.1 ms: 1.25x slower                                                    |
| async_tree_none            | 247 ms                                                                 | 309 ms: 1.25x slower                                                     |
| python_startup             | 12.3 ms                                                                | 15.5 ms: 1.25x slower                                                    |
| mako                       | 12.2 ms                                                                | 15.5 ms: 1.27x slower                                                    |
| connected_components       | 387 ms                                                                 | 496 ms: 1.28x slower                                                     |
| python_startup_no_site     | 6.80 ms                                                                | 8.95 ms: 1.32x slower                                                    |
| nbody                      | 92.4 ms                                                                | 122 ms: 1.32x slower                                                     |
| coverage                   | 82.1 ms                                                                | 110 ms: 1.34x slower                                                     |
| Geometric mean             | (ref)                                                                  | 1.07x slower                                                             |

- Geometric mean (including insignificant results): 1.101x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.10x

# Memory
- memory change: 1.19x