# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: gh_115999_load_super
- machine: linux-x86_64
- commit hash: ab3af14
- commit date: 2024-11-26
- overall geometric mean: 1.306x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.29x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                 | 406 ms: 1.58x slower                                                     |
| docutils       | 2.60 sec                                                               | 3.29 sec: 1.26x slower                                                   |
| sphinx         | 1.03 sec                                                               | 1.27 sec: 1.24x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.35x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 521 ms: 1.00x faster                                                     |
| async_tree_io_tg           | 868 ms                                                                 | 893 ms: 1.03x slower                                                     |
| async_tree_cpu_io_mixed_tg | 626 ms                                                                 | 657 ms: 1.05x slower                                                     |
| async_tree_io              | 849 ms                                                                 | 918 ms: 1.08x slower                                                     |
| async_tree_cpu_io_mixed    | 629 ms                                                                 | 684 ms: 1.09x slower                                                     |
| async_tree_none_tg         | 346 ms                                                                 | 385 ms: 1.11x slower                                                     |
| async_tree_memoization_tg  | 390 ms                                                                 | 480 ms: 1.23x slower                                                     |
| async_tree_memoization     | 407 ms                                                                 | 509 ms: 1.25x slower                                                     |
| async_tree_none            | 331 ms                                                                 | 420 ms: 1.27x slower                                                     |
| async_generators           | 370 ms                                                                 | 482 ms: 1.30x slower                                                     |
| coroutines                 | 22.0 ms                                                                | 29.2 ms: 1.33x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.15x slower                                                             |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                                 | 183 ms: 1.19x faster                                                     |
| float          | 80.0 ms                                                                | 148 ms: 1.85x slower                                                     |
| nbody          | 95.4 ms                                                                | 197 ms: 2.07x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.48x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 2.75 ms                                                                | 2.86 ms: 1.04x slower                                                    |
| regex_dna      | 177 ms                                                                 | 191 ms: 1.08x slower                                                     |
| regex_v8       | 23.4 ms                                                                | 25.6 ms: 1.10x slower                                                    |
| regex_compile  | 132 ms                                                                 | 209 ms: 1.59x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.18x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 138 ms                                                                 | 131 ms: 1.05x faster                                                     |
| xml_etree_iterparse  | 98.4 ms                                                                | 102 ms: 1.04x slower                                                     |
| json_loads           | 25.0 us                                                                | 28.3 us: 1.13x slower                                                    |
| xml_etree_generate   | 85.4 ms                                                                | 106 ms: 1.25x slower                                                     |
| json_dumps           | 11.7 ms                                                                | 14.6 ms: 1.25x slower                                                    |
| tomli_loads          | 2.10 sec                                                               | 3.05 sec: 1.45x slower                                                   |
| xml_etree_process    | 59.6 ms                                                                | 86.5 ms: 1.45x slower                                                    |
| unpickle_pure_python | 215 us                                                                 | 383 us: 1.78x slower                                                     |
| pickle_pure_python   | 314 us                                                                 | 575 us: 1.83x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.32x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.5 ms: 1.20x slower                                                    |
| python_startup_no_site | 7.40 ms                                                                | 10.3 ms: 1.39x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.29x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.4 ms                                                                | 75.0 ms: 1.49x slower                                                    |
| django_template | 36.2 ms                                                                | 58.6 ms: 1.62x slower                                                    |
| genshi_text     | 22.2 ms                                                                | 36.0 ms: 1.62x slower                                                    |
| mako            | 11.7 ms                                                                | 19.9 ms: 1.70x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.61x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 4.45 ms                                                                | 3.49 ms: 1.28x faster                                                    |
| pidigits                   | 217 ms                                                                 | 183 ms: 1.19x faster                                                     |
| create_gc_cycles           | 1.94 ms                                                                | 1.82 ms: 1.07x faster                                                    |
| xml_etree_parse            | 138 ms                                                                 | 131 ms: 1.05x faster                                                     |
| asyncio_websockets         | 523 ms                                                                 | 521 ms: 1.00x faster                                                     |
| async_tree_io_tg           | 868 ms                                                                 | 893 ms: 1.03x slower                                                     |
| xml_etree_iterparse        | 98.4 ms                                                                | 102 ms: 1.04x slower                                                     |
| regex_effbot               | 2.75 ms                                                                | 2.86 ms: 1.04x slower                                                    |
| async_tree_cpu_io_mixed_tg | 626 ms                                                                 | 657 ms: 1.05x slower                                                     |
| sqlite_synth               | 2.22 us                                                                | 2.39 us: 1.08x slower                                                    |
| async_tree_io              | 849 ms                                                                 | 918 ms: 1.08x slower                                                     |
| regex_dna                  | 177 ms                                                                 | 191 ms: 1.08x slower                                                     |
| async_tree_cpu_io_mixed    | 629 ms                                                                 | 684 ms: 1.09x slower                                                     |
| regex_v8                   | 23.4 ms                                                                | 25.6 ms: 1.10x slower                                                    |
| async_tree_none_tg         | 346 ms                                                                 | 385 ms: 1.11x slower                                                     |
| json_loads                 | 25.0 us                                                                | 28.3 us: 1.13x slower                                                    |
| json                       | 4.56 ms                                                                | 5.19 ms: 1.14x slower                                                    |
| pathlib                    | 18.3 ms                                                                | 21.2 ms: 1.16x slower                                                    |
| python_startup             | 14.6 ms                                                                | 17.5 ms: 1.20x slower                                                    |
| scimark_fft                | 337 ms                                                                 | 410 ms: 1.21x slower                                                     |
| async_tree_memoization_tg  | 390 ms                                                                 | 480 ms: 1.23x slower                                                     |
| telco                      | 7.39 ms                                                                | 9.11 ms: 1.23x slower                                                    |
| sphinx                     | 1.03 sec                                                               | 1.27 sec: 1.24x slower                                                   |
| xml_etree_generate         | 85.4 ms                                                                | 106 ms: 1.25x slower                                                     |
| json_dumps                 | 11.7 ms                                                                | 14.6 ms: 1.25x slower                                                    |
| async_tree_memoization     | 407 ms                                                                 | 509 ms: 1.25x slower                                                     |
| docutils                   | 2.60 sec                                                               | 3.29 sec: 1.26x slower                                                   |
| async_tree_none            | 331 ms                                                                 | 420 ms: 1.27x slower                                                     |
| scimark_sparse_mat_mult    | 4.72 ms                                                                | 6.00 ms: 1.27x slower                                                    |
| bench_mp_pool              | 86.0 ms                                                                | 110 ms: 1.28x slower                                                     |
| coverage                   | 80.3 ms                                                                | 103 ms: 1.29x slower                                                     |
| shortest_path              | 445 ms                                                                 | 574 ms: 1.29x slower                                                     |
| bpe_tokeniser              | 4.42 sec                                                               | 5.73 sec: 1.30x slower                                                   |
| async_generators           | 370 ms                                                                 | 482 ms: 1.30x slower                                                     |
| connected_components       | 403 ms                                                                 | 535 ms: 1.33x slower                                                     |
| coroutines                 | 22.0 ms                                                                | 29.2 ms: 1.33x slower                                                    |
| dulwich_log                | 75.9 ms                                                                | 102 ms: 1.35x slower                                                     |
| mdp                        | 2.36 sec                                                               | 3.19 sec: 1.35x slower                                                   |
| many_optionals             | 1.02 ms                                                                | 1.38 ms: 1.35x slower                                                    |
| typing_runtime_protocols   | 160 us                                                                 | 218 us: 1.36x slower                                                     |
| meteor_contest             | 100 ms                                                                 | 137 ms: 1.37x slower                                                     |
| spectral_norm              | 111 ms                                                                 | 152 ms: 1.37x slower                                                     |
| python_startup_no_site     | 7.40 ms                                                                | 10.3 ms: 1.39x slower                                                    |
| generators                 | 29.6 ms                                                                | 41.2 ms: 1.39x slower                                                    |
| nqueens                    | 78.9 ms                                                                | 112 ms: 1.42x slower                                                     |
| fannkuch                   | 385 ms                                                                 | 555 ms: 1.44x slower                                                     |
| tomli_loads                | 2.10 sec                                                               | 3.05 sec: 1.45x slower                                                   |
| xml_etree_process          | 59.6 ms                                                                | 86.5 ms: 1.45x slower                                                    |
| deepcopy                   | 260 us                                                                 | 379 us: 1.46x slower                                                     |
| pycparser                  | 1.13 sec                                                               | 1.66 sec: 1.47x slower                                                   |
| genshi_xml                 | 50.4 ms                                                                | 75.0 ms: 1.49x slower                                                    |
| pylint                     | 270 ms                                                                 | 407 ms: 1.50x slower                                                     |
| sqlglot_optimize           | 53.3 ms                                                                | 80.5 ms: 1.51x slower                                                    |
| deepcopy_memo              | 30.3 us                                                                | 45.8 us: 1.51x slower                                                    |
| deepcopy_reduce            | 2.59 us                                                                | 3.94 us: 1.52x slower                                                    |
| sqlglot_normalize          | 106 ms                                                                 | 163 ms: 1.54x slower                                                     |
| subparsers                 | 22.3 ms                                                                | 34.3 ms: 1.54x slower                                                    |
| 2to3                       | 257 ms                                                                 | 406 ms: 1.58x slower                                                     |
| crypto_pyaes               | 67.5 ms                                                                | 107 ms: 1.58x slower                                                     |
| regex_compile              | 132 ms                                                                 | 209 ms: 1.59x slower                                                     |
| pprint_safe_repr           | 716 ms                                                                 | 1.15 sec: 1.60x slower                                                   |
| sympy_integrate            | 20.0 ms                                                                | 32.0 ms: 1.60x slower                                                    |
| django_template            | 36.2 ms                                                                | 58.6 ms: 1.62x slower                                                    |
| pprint_pformat             | 1.47 sec                                                               | 2.38 sec: 1.62x slower                                                   |
| genshi_text                | 22.2 ms                                                                | 36.0 ms: 1.62x slower                                                    |
| thrift                     | 748 us                                                                 | 1.23 ms: 1.64x slower                                                    |
| mako                       | 11.7 ms                                                                | 19.9 ms: 1.70x slower                                                    |
| pyflate                    | 446 ms                                                                 | 770 ms: 1.73x slower                                                     |
| comprehensions             | 17.1 us                                                                | 30.1 us: 1.76x slower                                                    |
| unpickle_pure_python       | 215 us                                                                 | 383 us: 1.78x slower                                                     |
| pickle_pure_python         | 314 us                                                                 | 575 us: 1.83x slower                                                     |
| richards_super             | 51.7 ms                                                                | 94.8 ms: 1.83x slower                                                    |
| float                      | 80.0 ms                                                                | 148 ms: 1.85x slower                                                     |
| logging_simple             | 6.20 us                                                                | 11.5 us: 1.85x slower                                                    |
| logging_format             | 6.94 us                                                                | 13.0 us: 1.87x slower                                                    |
| sympy_str                  | 275 ms                                                                 | 519 ms: 1.89x slower                                                     |
| richards                   | 45.5 ms                                                                | 86.2 ms: 1.89x slower                                                    |
| scimark_monte_carlo        | 65.6 ms                                                                | 125 ms: 1.90x slower                                                     |
| scimark_lu                 | 111 ms                                                                 | 212 ms: 1.91x slower                                                     |
| hexiom                     | 5.96 ms                                                                | 11.7 ms: 1.96x slower                                                    |
| chaos                      | 59.0 ms                                                                | 119 ms: 2.01x slower                                                     |
| logging_silent             | 105 ns                                                                 | 210 ns: 2.01x slower                                                     |
| scimark_sor                | 134 ms                                                                 | 271 ms: 2.02x slower                                                     |
| sqlglot_transpile          | 1.59 ms                                                                | 3.23 ms: 2.03x slower                                                    |
| nbody                      | 95.4 ms                                                                | 197 ms: 2.07x slower                                                     |
| sqlglot_parse              | 1.29 ms                                                                | 2.80 ms: 2.16x slower                                                    |
| sympy_expand               | 457 ms                                                                 | 1.02 sec: 2.23x slower                                                   |
| raytrace                   | 263 ms                                                                 | 630 ms: 2.39x slower                                                     |
| sympy_sum                  | 153 ms                                                                 | 370 ms: 2.42x slower                                                     |
| go                         | 120 ms                                                                 | 291 ms: 2.43x slower                                                     |
| deltablue                  | 3.23 ms                                                                | 8.72 ms: 2.70x slower                                                    |
| bench_thread_pool          | 1.02 ms                                                                | 3.47 ms: 3.40x slower                                                    |
| Geometric mean             | (ref)                                                                  | 1.46x slower                                                             |

Benchmark hidden because not significant (1): k_core
Ignored benchmarks (2) of results/bm-20241121-3.14.0a2+-09c240f/bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (1) of results/bm-20241126-3.14.0a2+-ab3af14-NOGIL/bm-20241126-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-ab3af14.json: html5lib

- Geometric mean (including insignificant results): 1.306x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.33x
- 95% likely to have a slowdown of 1.31x
- 99% likely to have a slowdown of 1.29x

# Memory
- memory change: 1.19x