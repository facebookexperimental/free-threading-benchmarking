# Results vs. default_base_vs_NOGIL

- fork: nascheme
- ref: gh_115999_load_super
- machine: linux-x86_64
- commit hash: a515a0d
- commit date: 2024-11-25
- overall geometric mean: 1.431x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.43x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                 | 455 ms: 1.77x slower                                                     |
| docutils       | 2.60 sec                                                               | 3.33 sec: 1.28x slower                                                   |
| sphinx         | 1.03 sec                                                               | 1.45 sec: 1.42x slower                                                   |
| Geometric mean | (ref)                                                                  | 1.47x slower                                                             |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| async_tree_none_tg         | 346 ms                                                                 | 384 ms: 1.11x slower                                                     |
| async_generators           | 370 ms                                                                 | 480 ms: 1.30x slower                                                     |
| async_tree_cpu_io_mixed_tg | 626 ms                                                                 | 815 ms: 1.30x slower                                                     |
| coroutines                 | 22.0 ms                                                                | 29.7 ms: 1.35x slower                                                    |
| async_tree_cpu_io_mixed    | 629 ms                                                                 | 1.08 sec: 1.72x slower                                                   |
| async_tree_memoization_tg  | 390 ms                                                                 | 725 ms: 1.86x slower                                                     |
| async_tree_none            | 331 ms                                                                 | 664 ms: 2.01x slower                                                     |
| async_tree_memoization     | 407 ms                                                                 | 998 ms: 2.45x slower                                                     |
| async_tree_io_tg           | 868 ms                                                                 | 3.36 sec: 3.87x slower                                                   |
| async_tree_io              | 849 ms                                                                 | 3.62 sec: 4.27x slower                                                   |
| Geometric mean             | (ref)                                                                  | 1.80x slower                                                             |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| pidigits       | 217 ms                                                                 | 199 ms: 1.09x faster                                                     |
| float          | 80.0 ms                                                                | 148 ms: 1.85x slower                                                     |
| nbody          | 95.4 ms                                                                | 201 ms: 2.11x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.53x slower                                                             |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| regex_effbot   | 2.75 ms                                                                | 2.85 ms: 1.04x slower                                                    |
| regex_dna      | 177 ms                                                                 | 188 ms: 1.07x slower                                                     |
| regex_v8       | 23.4 ms                                                                | 25.1 ms: 1.07x slower                                                    |
| regex_compile  | 132 ms                                                                 | 209 ms: 1.59x slower                                                     |
| Geometric mean | (ref)                                                                  | 1.17x slower                                                             |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| xml_etree_parse      | 138 ms                                                                 | 132 ms: 1.04x faster                                                     |
| xml_etree_iterparse  | 98.4 ms                                                                | 102 ms: 1.04x slower                                                     |
| json_loads           | 25.0 us                                                                | 28.6 us: 1.15x slower                                                    |
| xml_etree_generate   | 85.4 ms                                                                | 107 ms: 1.25x slower                                                     |
| json_dumps           | 11.7 ms                                                                | 14.8 ms: 1.27x slower                                                    |
| xml_etree_process    | 59.6 ms                                                                | 86.2 ms: 1.45x slower                                                    |
| tomli_loads          | 2.10 sec                                                               | 3.06 sec: 1.45x slower                                                   |
| unpickle_pure_python | 215 us                                                                 | 381 us: 1.77x slower                                                     |
| pickle_pure_python   | 314 us                                                                 | 576 us: 1.84x slower                                                     |
| Geometric mean       | (ref)                                                                  | 1.32x slower                                                             |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 20.3 ms: 1.39x slower                                                    |
| python_startup_no_site | 7.40 ms                                                                | 11.3 ms: 1.53x slower                                                    |
| Geometric mean         | (ref)                                                                  | 1.46x slower                                                             |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| genshi_xml      | 50.4 ms                                                                | 74.5 ms: 1.48x slower                                                    |
| genshi_text     | 22.2 ms                                                                | 36.2 ms: 1.64x slower                                                    |
| django_template | 36.2 ms                                                                | 61.8 ms: 1.71x slower                                                    |
| mako            | 11.7 ms                                                                | 20.1 ms: 1.72x slower                                                    |
| Geometric mean  | (ref)                                                                  | 1.63x slower                                                             |

All benchmarks:
===============

| Benchmark                  | bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f | bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------------------------:|
| gc_traversal               | 4.45 ms                                                                | 3.48 ms: 1.28x faster                                                    |
| pidigits                   | 217 ms                                                                 | 199 ms: 1.09x faster                                                     |
| create_gc_cycles           | 1.94 ms                                                                | 1.81 ms: 1.07x faster                                                    |
| xml_etree_parse            | 138 ms                                                                 | 132 ms: 1.04x faster                                                     |
| k_core                     | 2.50 sec                                                               | 2.55 sec: 1.02x slower                                                   |
| xml_etree_iterparse        | 98.4 ms                                                                | 102 ms: 1.04x slower                                                     |
| regex_effbot               | 2.75 ms                                                                | 2.85 ms: 1.04x slower                                                    |
| regex_dna                  | 177 ms                                                                 | 188 ms: 1.07x slower                                                     |
| regex_v8                   | 23.4 ms                                                                | 25.1 ms: 1.07x slower                                                    |
| sqlite_synth               | 2.22 us                                                                | 2.41 us: 1.08x slower                                                    |
| async_tree_none_tg         | 346 ms                                                                 | 384 ms: 1.11x slower                                                     |
| json_loads                 | 25.0 us                                                                | 28.6 us: 1.15x slower                                                    |
| json                       | 4.56 ms                                                                | 5.22 ms: 1.15x slower                                                    |
| pathlib                    | 18.3 ms                                                                | 21.1 ms: 1.15x slower                                                    |
| telco                      | 7.39 ms                                                                | 9.20 ms: 1.24x slower                                                    |
| xml_etree_generate         | 85.4 ms                                                                | 107 ms: 1.25x slower                                                     |
| scimark_fft                | 337 ms                                                                 | 427 ms: 1.26x slower                                                     |
| json_dumps                 | 11.7 ms                                                                | 14.8 ms: 1.27x slower                                                    |
| coverage                   | 80.3 ms                                                                | 102 ms: 1.27x slower                                                     |
| scimark_sparse_mat_mult    | 4.72 ms                                                                | 6.02 ms: 1.27x slower                                                    |
| docutils                   | 2.60 sec                                                               | 3.33 sec: 1.28x slower                                                   |
| async_generators           | 370 ms                                                                 | 480 ms: 1.30x slower                                                     |
| shortest_path              | 445 ms                                                                 | 578 ms: 1.30x slower                                                     |
| bpe_tokeniser              | 4.42 sec                                                               | 5.74 sec: 1.30x slower                                                   |
| async_tree_cpu_io_mixed_tg | 626 ms                                                                 | 815 ms: 1.30x slower                                                     |
| connected_components       | 403 ms                                                                 | 534 ms: 1.32x slower                                                     |
| coroutines                 | 22.0 ms                                                                | 29.7 ms: 1.35x slower                                                    |
| generators                 | 29.6 ms                                                                | 41.0 ms: 1.38x slower                                                    |
| meteor_contest             | 100 ms                                                                 | 139 ms: 1.38x slower                                                     |
| typing_runtime_protocols   | 160 us                                                                 | 222 us: 1.39x slower                                                     |
| python_startup             | 14.6 ms                                                                | 20.3 ms: 1.39x slower                                                    |
| spectral_norm              | 111 ms                                                                 | 157 ms: 1.41x slower                                                     |
| sphinx                     | 1.03 sec                                                               | 1.45 sec: 1.42x slower                                                   |
| nqueens                    | 78.9 ms                                                                | 112 ms: 1.42x slower                                                     |
| xml_etree_process          | 59.6 ms                                                                | 86.2 ms: 1.45x slower                                                    |
| tomli_loads                | 2.10 sec                                                               | 3.06 sec: 1.45x slower                                                   |
| fannkuch                   | 385 ms                                                                 | 561 ms: 1.46x slower                                                     |
| pycparser                  | 1.13 sec                                                               | 1.66 sec: 1.47x slower                                                   |
| deepcopy                   | 260 us                                                                 | 383 us: 1.47x slower                                                     |
| genshi_xml                 | 50.4 ms                                                                | 74.5 ms: 1.48x slower                                                    |
| sqlglot_optimize           | 53.3 ms                                                                | 80.2 ms: 1.51x slower                                                    |
| sqlglot_normalize          | 106 ms                                                                 | 162 ms: 1.52x slower                                                     |
| python_startup_no_site     | 7.40 ms                                                                | 11.3 ms: 1.53x slower                                                    |
| deepcopy_reduce            | 2.59 us                                                                | 3.98 us: 1.53x slower                                                    |
| deepcopy_memo              | 30.3 us                                                                | 46.4 us: 1.53x slower                                                    |
| regex_compile              | 132 ms                                                                 | 209 ms: 1.59x slower                                                     |
| crypto_pyaes               | 67.5 ms                                                                | 108 ms: 1.59x slower                                                     |
| pprint_safe_repr           | 716 ms                                                                 | 1.16 sec: 1.63x slower                                                   |
| genshi_text                | 22.2 ms                                                                | 36.2 ms: 1.64x slower                                                    |
| pprint_pformat             | 1.47 sec                                                               | 2.43 sec: 1.65x slower                                                   |
| django_template            | 36.2 ms                                                                | 61.8 ms: 1.71x slower                                                    |
| pyflate                    | 446 ms                                                                 | 763 ms: 1.71x slower                                                     |
| mako                       | 11.7 ms                                                                | 20.1 ms: 1.72x slower                                                    |
| async_tree_cpu_io_mixed    | 629 ms                                                                 | 1.08 sec: 1.72x slower                                                   |
| comprehensions             | 17.1 us                                                                | 29.7 us: 1.74x slower                                                    |
| 2to3                       | 257 ms                                                                 | 455 ms: 1.77x slower                                                     |
| unpickle_pure_python       | 215 us                                                                 | 381 us: 1.77x slower                                                     |
| pickle_pure_python         | 314 us                                                                 | 576 us: 1.84x slower                                                     |
| logging_format             | 6.94 us                                                                | 12.8 us: 1.85x slower                                                    |
| float                      | 80.0 ms                                                                | 148 ms: 1.85x slower                                                     |
| async_tree_memoization_tg  | 390 ms                                                                 | 725 ms: 1.86x slower                                                     |
| logging_simple             | 6.20 us                                                                | 11.6 us: 1.88x slower                                                    |
| scimark_monte_carlo        | 65.6 ms                                                                | 123 ms: 1.88x slower                                                     |
| richards                   | 45.5 ms                                                                | 86.1 ms: 1.89x slower                                                    |
| dulwich_log                | 75.9 ms                                                                | 145 ms: 1.91x slower                                                     |
| scimark_lu                 | 111 ms                                                                 | 213 ms: 1.92x slower                                                     |
| hexiom                     | 5.96 ms                                                                | 11.7 ms: 1.96x slower                                                    |
| logging_silent             | 105 ns                                                                 | 209 ns: 2.00x slower                                                     |
| async_tree_none            | 331 ms                                                                 | 664 ms: 2.01x slower                                                     |
| chaos                      | 59.0 ms                                                                | 119 ms: 2.01x slower                                                     |
| sqlglot_transpile          | 1.59 ms                                                                | 3.21 ms: 2.02x slower                                                    |
| scimark_sor                | 134 ms                                                                 | 273 ms: 2.03x slower                                                     |
| nbody                      | 95.4 ms                                                                | 201 ms: 2.11x slower                                                     |
| sympy_integrate            | 20.0 ms                                                                | 42.2 ms: 2.12x slower                                                    |
| sqlglot_parse              | 1.29 ms                                                                | 2.78 ms: 2.15x slower                                                    |
| bench_mp_pool              | 86.0 ms                                                                | 202 ms: 2.35x slower                                                     |
| raytrace                   | 263 ms                                                                 | 619 ms: 2.35x slower                                                     |
| pylint                     | 270 ms                                                                 | 642 ms: 2.37x slower                                                     |
| go                         | 120 ms                                                                 | 288 ms: 2.41x slower                                                     |
| async_tree_memoization     | 407 ms                                                                 | 998 ms: 2.45x slower                                                     |
| sympy_expand               | 457 ms                                                                 | 1.25 sec: 2.74x slower                                                   |
| many_optionals             | 1.02 ms                                                                | 3.29 ms: 3.23x slower                                                    |
| sympy_sum                  | 153 ms                                                                 | 535 ms: 3.49x slower                                                     |
| sympy_str                  | 275 ms                                                                 | 1.01 sec: 3.68x slower                                                   |
| async_tree_io_tg           | 868 ms                                                                 | 3.36 sec: 3.87x slower                                                   |
| subparsers                 | 22.3 ms                                                                | 87.7 ms: 3.93x slower                                                    |
| bench_thread_pool          | 1.02 ms                                                                | 4.32 ms: 4.23x slower                                                    |
| async_tree_io              | 849 ms                                                                 | 3.62 sec: 4.27x slower                                                   |
| mdp                        | 2.36 sec                                                               | 16.3 sec: 6.89x slower                                                   |
| thrift                     | 748 us                                                                 | 6.57 ms: 8.79x slower                                                    |
| deltablue                  | 3.23 ms                                                                | 43.9 ms: 13.58x slower                                                   |
| richards_super             | 51.7 ms                                                                | 1.82 sec: 35.12x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.78x slower                                                             |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (2) of results/bm-20241121-3.14.0a2+-09c240f/bm-20241121-vultr-x86_64-python-09c240f20c47db126ad7-3.14.0a2+-09c240f.json: sqlalchemy_declarative, sqlalchemy_imperative
Ignored benchmarks (1) of results/bm-20241125-3.14.0a2+-a515a0d-NOGIL/bm-20241125-vultr-x86_64-nascheme-gh_115999_load_super-3.14.0a2+-a515a0d.json: html5lib

- Geometric mean (including insignificant results): 1.431x slower
# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.48x
- 95% likely to have a slowdown of 1.46x
- 99% likely to have a slowdown of 1.43x

# Memory
- memory change: 1.19x