# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: restore_load_bearing
- machine: linux-x86_64
- commit hash: 5a139fe
- commit date: 2025-04-08
- overall geometric mean: 1.081x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.07x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 289 ms: 1.13x slower                                                  |
| docutils       | 2.60 sec                                                               | 2.77 sec: 1.06x slower                                                |
| sphinx         | 1.00 sec                                                               | 1.09 sec: 1.08x slower                                                |
| Geometric mean | (ref)                                                                  | 1.09x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 626 ms                                                                 | 538 ms: 1.16x faster                                                  |
| async_tree_none_tg         | 263 ms                                                                 | 234 ms: 1.13x faster                                                  |
| async_tree_memoization_tg  | 325 ms                                                                 | 293 ms: 1.11x faster                                                  |
| async_tree_io              | 628 ms                                                                 | 567 ms: 1.11x faster                                                  |
| coroutines                 | 24.6 ms                                                                | 23.6 ms: 1.04x faster                                                 |
| async_tree_none            | 278 ms                                                                 | 267 ms: 1.04x faster                                                  |
| async_tree_cpu_io_mixed_tg | 503 ms                                                                 | 486 ms: 1.04x faster                                                  |
| async_tree_memoization     | 318 ms                                                                 | 321 ms: 1.01x slower                                                  |
| async_tree_cpu_io_mixed    | 506 ms                                                                 | 516 ms: 1.02x slower                                                  |
| async_generators           | 336 ms                                                                 | 372 ms: 1.11x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.04x faster                                                          |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 72.3 ms                                                                | 70.4 ms: 1.03x faster                                                 |
| pidigits       | 192 ms                                                                 | 193 ms: 1.00x slower                                                  |
| nbody          | 94.9 ms                                                                | 116 ms: 1.23x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 21.8 ms                                                                | 21.2 ms: 1.03x faster                                                 |
| regex_effbot   | 2.70 ms                                                                | 2.85 ms: 1.05x slower                                                 |
| regex_dna      | 171 ms                                                                 | 181 ms: 1.06x slower                                                  |
| regex_compile  | 130 ms                                                                 | 151 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.06x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.0 ms                                                                | 87.0 ms: 1.07x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 130 ms: 1.01x slower                                                  |
| json_loads           | 28.8 us                                                                | 30.5 us: 1.06x slower                                                 |
| pickle_pure_python   | 318 us                                                                 | 343 us: 1.08x slower                                                  |
| unpickle_pure_python | 222 us                                                                 | 240 us: 1.08x slower                                                  |
| xml_etree_generate   | 85.7 ms                                                                | 95.6 ms: 1.12x slower                                                 |
| tomli_loads          | 2.01 sec                                                               | 2.25 sec: 1.12x slower                                                |
| xml_etree_process    | 61.4 ms                                                                | 69.2 ms: 1.13x slower                                                 |
| json_dumps           | 11.3 ms                                                                | 12.8 ms: 1.13x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 15.2 ms                                                                | 15.9 ms: 1.05x slower                                                 |
| python_startup_no_site | 8.68 ms                                                                | 11.2 ms: 1.29x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| django_template | 36.7 ms                                                                | 41.9 ms: 1.14x slower                                                 |
| genshi_xml      | 50.6 ms                                                                | 58.5 ms: 1.16x slower                                                 |
| genshi_text     | 22.0 ms                                                                | 27.3 ms: 1.24x slower                                                 |
| mako            | 12.3 ms                                                                | 15.8 ms: 1.28x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.20x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.34 ms                                                                | 1.82 ms: 2.38x faster                                                 |
| create_gc_cycles           | 1.86 ms                                                                | 1.38 ms: 1.34x faster                                                 |
| async_tree_io_tg           | 626 ms                                                                 | 538 ms: 1.16x faster                                                  |
| async_tree_none_tg         | 263 ms                                                                 | 234 ms: 1.13x faster                                                  |
| async_tree_memoization_tg  | 325 ms                                                                 | 293 ms: 1.11x faster                                                  |
| async_tree_io              | 628 ms                                                                 | 567 ms: 1.11x faster                                                  |
| sqlite_synth               | 2.23 us                                                                | 2.02 us: 1.10x faster                                                 |
| xml_etree_iterparse        | 93.0 ms                                                                | 87.0 ms: 1.07x faster                                                 |
| coroutines                 | 24.6 ms                                                                | 23.6 ms: 1.04x faster                                                 |
| async_tree_none            | 278 ms                                                                 | 267 ms: 1.04x faster                                                  |
| async_tree_cpu_io_mixed_tg | 503 ms                                                                 | 486 ms: 1.04x faster                                                  |
| float                      | 72.3 ms                                                                | 70.4 ms: 1.03x faster                                                 |
| regex_v8                   | 21.8 ms                                                                | 21.2 ms: 1.03x faster                                                 |
| pidigits                   | 192 ms                                                                 | 193 ms: 1.00x slower                                                  |
| xml_etree_parse            | 129 ms                                                                 | 130 ms: 1.01x slower                                                  |
| async_tree_memoization     | 318 ms                                                                 | 321 ms: 1.01x slower                                                  |
| json                       | 5.19 ms                                                                | 5.24 ms: 1.01x slower                                                 |
| pycparser                  | 1.15 sec                                                               | 1.17 sec: 1.01x slower                                                |
| pathlib                    | 19.3 ms                                                                | 19.7 ms: 1.02x slower                                                 |
| async_tree_cpu_io_mixed    | 506 ms                                                                 | 516 ms: 1.02x slower                                                  |
| python_startup             | 15.2 ms                                                                | 15.9 ms: 1.05x slower                                                 |
| regex_effbot               | 2.70 ms                                                                | 2.85 ms: 1.05x slower                                                 |
| regex_dna                  | 171 ms                                                                 | 181 ms: 1.06x slower                                                  |
| json_loads                 | 28.8 us                                                                | 30.5 us: 1.06x slower                                                 |
| bpe_tokeniser              | 4.35 sec                                                               | 4.62 sec: 1.06x slower                                                |
| docutils                   | 2.60 sec                                                               | 2.77 sec: 1.06x slower                                                |
| dulwich_log                | 69.1 ms                                                                | 73.7 ms: 1.07x slower                                                 |
| logging_silent             | 103 ns                                                                 | 110 ns: 1.08x slower                                                  |
| bench_mp_pool              | 89.1 ms                                                                | 96.2 ms: 1.08x slower                                                 |
| pickle_pure_python         | 318 us                                                                 | 343 us: 1.08x slower                                                  |
| unpickle_pure_python       | 222 us                                                                 | 240 us: 1.08x slower                                                  |
| pprint_safe_repr           | 739 ms                                                                 | 798 ms: 1.08x slower                                                  |
| sphinx                     | 1.00 sec                                                               | 1.09 sec: 1.08x slower                                                |
| k_core                     | 2.06 sec                                                               | 2.24 sec: 1.09x slower                                                |
| deltablue                  | 3.42 ms                                                                | 3.75 ms: 1.10x slower                                                 |
| deepcopy_reduce            | 2.75 us                                                                | 3.02 us: 1.10x slower                                                 |
| many_optionals             | 1.04 ms                                                                | 1.15 ms: 1.10x slower                                                 |
| pprint_pformat             | 1.51 sec                                                               | 1.66 sec: 1.10x slower                                                |
| spectral_norm              | 99.1 ms                                                                | 109 ms: 1.10x slower                                                  |
| pylint                     | 287 ms                                                                 | 316 ms: 1.10x slower                                                  |
| scimark_fft                | 324 ms                                                                 | 358 ms: 1.10x slower                                                  |
| async_generators           | 336 ms                                                                 | 372 ms: 1.11x slower                                                  |
| xml_etree_generate         | 85.7 ms                                                                | 95.6 ms: 1.12x slower                                                 |
| scimark_sor                | 115 ms                                                                 | 128 ms: 1.12x slower                                                  |
| sqlglot_v2_normalize       | 106 ms                                                                 | 118 ms: 1.12x slower                                                  |
| scimark_sparse_mat_mult    | 4.59 ms                                                                | 5.13 ms: 1.12x slower                                                 |
| tomli_loads                | 2.01 sec                                                               | 2.25 sec: 1.12x slower                                                |
| nqueens                    | 80.2 ms                                                                | 90.2 ms: 1.12x slower                                                 |
| sqlglot_v2_optimize        | 52.7 ms                                                                | 59.3 ms: 1.13x slower                                                 |
| xml_etree_process          | 61.4 ms                                                                | 69.2 ms: 1.13x slower                                                 |
| pyflate                    | 421 ms                                                                 | 475 ms: 1.13x slower                                                  |
| scimark_lu                 | 118 ms                                                                 | 134 ms: 1.13x slower                                                  |
| chaos                      | 56.3 ms                                                                | 63.6 ms: 1.13x slower                                                 |
| json_dumps                 | 11.3 ms                                                                | 12.8 ms: 1.13x slower                                                 |
| 2to3                       | 255 ms                                                                 | 289 ms: 1.13x slower                                                  |
| deepcopy                   | 263 us                                                                 | 298 us: 1.13x slower                                                  |
| generators                 | 29.1 ms                                                                | 33.0 ms: 1.14x slower                                                 |
| django_template            | 36.7 ms                                                                | 41.9 ms: 1.14x slower                                                 |
| subparsers                 | 22.3 ms                                                                | 25.7 ms: 1.15x slower                                                 |
| mdp                        | 1.18 sec                                                               | 1.36 sec: 1.15x slower                                                |
| sympy_expand               | 473 ms                                                                 | 545 ms: 1.15x slower                                                  |
| go                         | 115 ms                                                                 | 133 ms: 1.15x slower                                                  |
| sqlglot_v2_transpile       | 1.60 ms                                                                | 1.85 ms: 1.15x slower                                                 |
| hexiom                     | 6.12 ms                                                                | 7.07 ms: 1.15x slower                                                 |
| genshi_xml                 | 50.6 ms                                                                | 58.5 ms: 1.16x slower                                                 |
| sympy_sum                  | 160 ms                                                                 | 185 ms: 1.16x slower                                                  |
| regex_compile              | 130 ms                                                                 | 151 ms: 1.16x slower                                                  |
| comprehensions             | 17.3 us                                                                | 20.1 us: 1.16x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 23.0 ms: 1.16x slower                                                 |
| sympy_str                  | 282 ms                                                                 | 329 ms: 1.17x slower                                                  |
| telco                      | 7.31 ms                                                                | 8.55 ms: 1.17x slower                                                 |
| sqlalchemy_imperative      | 20.6 ms                                                                | 24.1 ms: 1.17x slower                                                 |
| raytrace                   | 258 ms                                                                 | 303 ms: 1.18x slower                                                  |
| logging_simple             | 6.22 us                                                                | 7.32 us: 1.18x slower                                                 |
| logging_format             | 6.98 us                                                                | 8.24 us: 1.18x slower                                                 |
| sqlalchemy_declarative     | 133 ms                                                                 | 157 ms: 1.18x slower                                                  |
| fannkuch                   | 389 ms                                                                 | 463 ms: 1.19x slower                                                  |
| sqlglot_v2_parse           | 1.29 ms                                                                | 1.54 ms: 1.19x slower                                                 |
| crypto_pyaes               | 70.5 ms                                                                | 84.6 ms: 1.20x slower                                                 |
| shortest_path              | 442 ms                                                                 | 534 ms: 1.21x slower                                                  |
| richards_super             | 50.6 ms                                                                | 61.2 ms: 1.21x slower                                                 |
| richards                   | 44.4 ms                                                                | 53.8 ms: 1.21x slower                                                 |
| deepcopy_memo              | 30.1 us                                                                | 36.7 us: 1.22x slower                                                 |
| connected_components       | 400 ms                                                                 | 489 ms: 1.22x slower                                                  |
| scimark_monte_carlo        | 63.3 ms                                                                | 77.5 ms: 1.22x slower                                                 |
| nbody                      | 94.9 ms                                                                | 116 ms: 1.23x slower                                                  |
| typing_runtime_protocols   | 160 us                                                                 | 197 us: 1.23x slower                                                  |
| genshi_text                | 22.0 ms                                                                | 27.3 ms: 1.24x slower                                                 |
| meteor_contest             | 101 ms                                                                 | 128 ms: 1.26x slower                                                  |
| mako                       | 12.3 ms                                                                | 15.8 ms: 1.28x slower                                                 |
| python_startup_no_site     | 8.68 ms                                                                | 11.2 ms: 1.29x slower                                                 |
| coverage                   | 79.9 ms                                                                | 108 ms: 1.36x slower                                                  |
| bench_thread_pool          | 1.07 ms                                                                | 3.16 ms: 2.96x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.10x slower                                                          |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (1) of results/bm-20250408-3.14.0a7+-5a139fe-NOGIL/bm-20250408-vultr-x86_64-mpage-restore_load_bearing-3.14.0a7+-5a139fe.json: html5lib

- Geometric mean (including insignificant results): 1.081x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.08x
- 99% likely to have a slowdown of 1.07x

# Memory
- memory change: 1.20x