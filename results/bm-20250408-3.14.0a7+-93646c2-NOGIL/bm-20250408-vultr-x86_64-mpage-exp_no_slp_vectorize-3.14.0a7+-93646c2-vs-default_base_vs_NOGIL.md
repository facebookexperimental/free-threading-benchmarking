# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: exp_no_slp_vectorize
- machine: linux-x86_64
- commit hash: 93646c2
- commit date: 2025-04-08
- overall geometric mean: 1.047x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 280 ms: 1.10x slower                                                  |
| docutils       | 2.60 sec                                                               | 2.71 sec: 1.04x slower                                                |
| sphinx         | 1.00 sec                                                               | 1.06 sec: 1.06x slower                                                |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 626 ms                                                                 | 512 ms: 1.22x faster                                                  |
| async_tree_none_tg         | 263 ms                                                                 | 222 ms: 1.19x faster                                                  |
| async_tree_io              | 628 ms                                                                 | 541 ms: 1.16x faster                                                  |
| async_tree_memoization_tg  | 325 ms                                                                 | 280 ms: 1.16x faster                                                  |
| async_tree_none            | 278 ms                                                                 | 252 ms: 1.10x faster                                                  |
| coroutines                 | 24.6 ms                                                                | 22.3 ms: 1.10x faster                                                 |
| async_tree_memoization     | 318 ms                                                                 | 309 ms: 1.03x faster                                                  |
| asyncio_websockets         | 518 ms                                                                 | 516 ms: 1.00x faster                                                  |
| async_tree_cpu_io_mixed_tg | 503 ms                                                                 | 521 ms: 1.04x slower                                                  |
| async_generators           | 336 ms                                                                 | 354 ms: 1.05x slower                                                  |
| async_tree_cpu_io_mixed    | 506 ms                                                                 | 549 ms: 1.08x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.07x faster                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 72.3 ms                                                                | 67.2 ms: 1.08x faster                                                 |
| nbody          | 94.9 ms                                                                | 107 ms: 1.13x slower                                                  |
| pidigits       | 192 ms                                                                 | 223 ms: 1.16x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.07x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 21.8 ms                                                                | 21.5 ms: 1.01x faster                                                 |
| regex_dna      | 171 ms                                                                 | 176 ms: 1.03x slower                                                  |
| regex_effbot   | 2.70 ms                                                                | 2.86 ms: 1.06x slower                                                 |
| regex_compile  | 130 ms                                                                 | 142 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 93.0 ms                                                                | 84.1 ms: 1.11x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 126 ms: 1.02x faster                                                  |
| unpickle_pure_python | 222 us                                                                 | 226 us: 1.02x slower                                                  |
| tomli_loads          | 2.01 sec                                                               | 2.08 sec: 1.03x slower                                                |
| pickle_pure_python   | 318 us                                                                 | 328 us: 1.03x slower                                                  |
| json_loads           | 28.8 us                                                                | 30.2 us: 1.05x slower                                                 |
| xml_etree_process    | 61.4 ms                                                                | 65.6 ms: 1.07x slower                                                 |
| xml_etree_generate   | 85.7 ms                                                                | 92.1 ms: 1.07x slower                                                 |
| json_dumps           | 11.3 ms                                                                | 12.5 ms: 1.11x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.03x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 15.2 ms                                                                | 15.8 ms: 1.04x slower                                                 |
| python_startup_no_site | 8.68 ms                                                                | 11.1 ms: 1.28x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.6 ms                                                                | 54.3 ms: 1.07x slower                                                 |
| django_template | 36.7 ms                                                                | 39.8 ms: 1.08x slower                                                 |
| genshi_text     | 22.0 ms                                                                | 25.5 ms: 1.16x slower                                                 |
| mako            | 12.3 ms                                                                | 15.3 ms: 1.24x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.14x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20250408-vultr-x86_64-python-f5f1ac84b3b9d688b9e7-3.14.0a7+-f5f1ac8 | bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.34 ms                                                                | 1.78 ms: 2.44x faster                                                 |
| create_gc_cycles           | 1.86 ms                                                                | 1.34 ms: 1.39x faster                                                 |
| async_tree_io_tg           | 626 ms                                                                 | 512 ms: 1.22x faster                                                  |
| async_tree_none_tg         | 263 ms                                                                 | 222 ms: 1.19x faster                                                  |
| async_tree_io              | 628 ms                                                                 | 541 ms: 1.16x faster                                                  |
| async_tree_memoization_tg  | 325 ms                                                                 | 280 ms: 1.16x faster                                                  |
| sqlite_synth               | 2.23 us                                                                | 2.01 us: 1.11x faster                                                 |
| xml_etree_iterparse        | 93.0 ms                                                                | 84.1 ms: 1.11x faster                                                 |
| async_tree_none            | 278 ms                                                                 | 252 ms: 1.10x faster                                                  |
| coroutines                 | 24.6 ms                                                                | 22.3 ms: 1.10x faster                                                 |
| float                      | 72.3 ms                                                                | 67.2 ms: 1.08x faster                                                 |
| async_tree_memoization     | 318 ms                                                                 | 309 ms: 1.03x faster                                                  |
| xml_etree_parse            | 129 ms                                                                 | 126 ms: 1.02x faster                                                  |
| pycparser                  | 1.15 sec                                                               | 1.13 sec: 1.02x faster                                                |
| pathlib                    | 19.3 ms                                                                | 19.0 ms: 1.02x faster                                                 |
| regex_v8                   | 21.8 ms                                                                | 21.5 ms: 1.01x faster                                                 |
| logging_silent             | 103 ns                                                                 | 102 ns: 1.01x faster                                                  |
| asyncio_websockets         | 518 ms                                                                 | 516 ms: 1.00x faster                                                  |
| generators                 | 29.1 ms                                                                | 29.5 ms: 1.01x slower                                                 |
| unpickle_pure_python       | 222 us                                                                 | 226 us: 1.02x slower                                                  |
| deltablue                  | 3.42 ms                                                                | 3.50 ms: 1.02x slower                                                 |
| regex_dna                  | 171 ms                                                                 | 176 ms: 1.03x slower                                                  |
| bpe_tokeniser              | 4.35 sec                                                               | 4.47 sec: 1.03x slower                                                |
| spectral_norm              | 99.1 ms                                                                | 102 ms: 1.03x slower                                                  |
| pprint_safe_repr           | 739 ms                                                                 | 762 ms: 1.03x slower                                                  |
| tomli_loads                | 2.01 sec                                                               | 2.08 sec: 1.03x slower                                                |
| pickle_pure_python         | 318 us                                                                 | 328 us: 1.03x slower                                                  |
| dulwich_log                | 69.1 ms                                                                | 71.5 ms: 1.04x slower                                                 |
| async_tree_cpu_io_mixed_tg | 503 ms                                                                 | 521 ms: 1.04x slower                                                  |
| scimark_sor                | 115 ms                                                                 | 119 ms: 1.04x slower                                                  |
| docutils                   | 2.60 sec                                                               | 2.71 sec: 1.04x slower                                                |
| python_startup             | 15.2 ms                                                                | 15.8 ms: 1.04x slower                                                 |
| deepcopy_reduce            | 2.75 us                                                                | 2.88 us: 1.05x slower                                                 |
| pprint_pformat             | 1.51 sec                                                               | 1.58 sec: 1.05x slower                                                |
| json_loads                 | 28.8 us                                                                | 30.2 us: 1.05x slower                                                 |
| nqueens                    | 80.2 ms                                                                | 84.2 ms: 1.05x slower                                                 |
| async_generators           | 336 ms                                                                 | 354 ms: 1.05x slower                                                  |
| scimark_sparse_mat_mult    | 4.59 ms                                                                | 4.85 ms: 1.06x slower                                                 |
| scimark_fft                | 324 ms                                                                 | 343 ms: 1.06x slower                                                  |
| sphinx                     | 1.00 sec                                                               | 1.06 sec: 1.06x slower                                                |
| regex_effbot               | 2.70 ms                                                                | 2.86 ms: 1.06x slower                                                 |
| sqlglot_v2_normalize       | 106 ms                                                                 | 112 ms: 1.06x slower                                                  |
| bench_mp_pool              | 89.1 ms                                                                | 95.0 ms: 1.07x slower                                                 |
| chaos                      | 56.3 ms                                                                | 60.1 ms: 1.07x slower                                                 |
| many_optionals             | 1.04 ms                                                                | 1.12 ms: 1.07x slower                                                 |
| scimark_lu                 | 118 ms                                                                 | 126 ms: 1.07x slower                                                  |
| xml_etree_process          | 61.4 ms                                                                | 65.6 ms: 1.07x slower                                                 |
| pylint                     | 287 ms                                                                 | 307 ms: 1.07x slower                                                  |
| go                         | 115 ms                                                                 | 124 ms: 1.07x slower                                                  |
| genshi_xml                 | 50.6 ms                                                                | 54.3 ms: 1.07x slower                                                 |
| xml_etree_generate         | 85.7 ms                                                                | 92.1 ms: 1.07x slower                                                 |
| k_core                     | 2.06 sec                                                               | 2.22 sec: 1.08x slower                                                |
| hexiom                     | 6.12 ms                                                                | 6.62 ms: 1.08x slower                                                 |
| django_template            | 36.7 ms                                                                | 39.8 ms: 1.08x slower                                                 |
| async_tree_cpu_io_mixed    | 506 ms                                                                 | 549 ms: 1.08x slower                                                  |
| sqlglot_v2_optimize        | 52.7 ms                                                                | 57.1 ms: 1.08x slower                                                 |
| pyflate                    | 421 ms                                                                 | 458 ms: 1.09x slower                                                  |
| regex_compile              | 130 ms                                                                 | 142 ms: 1.09x slower                                                  |
| subparsers                 | 22.3 ms                                                                | 24.4 ms: 1.09x slower                                                 |
| 2to3                       | 255 ms                                                                 | 280 ms: 1.10x slower                                                  |
| deepcopy                   | 263 us                                                                 | 289 us: 1.10x slower                                                  |
| mdp                        | 1.18 sec                                                               | 1.30 sec: 1.10x slower                                                |
| comprehensions             | 17.3 us                                                                | 19.0 us: 1.10x slower                                                 |
| sqlglot_v2_transpile       | 1.60 ms                                                                | 1.76 ms: 1.10x slower                                                 |
| sympy_expand               | 473 ms                                                                 | 522 ms: 1.10x slower                                                  |
| raytrace                   | 258 ms                                                                 | 284 ms: 1.10x slower                                                  |
| json_dumps                 | 11.3 ms                                                                | 12.5 ms: 1.11x slower                                                 |
| sympy_str                  | 282 ms                                                                 | 318 ms: 1.13x slower                                                  |
| sympy_sum                  | 160 ms                                                                 | 180 ms: 1.13x slower                                                  |
| telco                      | 7.31 ms                                                                | 8.25 ms: 1.13x slower                                                 |
| sympy_integrate            | 19.7 ms                                                                | 22.3 ms: 1.13x slower                                                 |
| nbody                      | 94.9 ms                                                                | 107 ms: 1.13x slower                                                  |
| logging_simple             | 6.22 us                                                                | 7.04 us: 1.13x slower                                                 |
| richards                   | 44.4 ms                                                                | 50.4 ms: 1.14x slower                                                 |
| sqlglot_v2_parse           | 1.29 ms                                                                | 1.47 ms: 1.14x slower                                                 |
| richards_super             | 50.6 ms                                                                | 57.7 ms: 1.14x slower                                                 |
| fannkuch                   | 389 ms                                                                 | 444 ms: 1.14x slower                                                  |
| logging_format             | 6.98 us                                                                | 7.96 us: 1.14x slower                                                 |
| sqlalchemy_imperative      | 20.6 ms                                                                | 23.6 ms: 1.15x slower                                                 |
| scimark_monte_carlo        | 63.3 ms                                                                | 73.2 ms: 1.16x slower                                                 |
| pidigits                   | 192 ms                                                                 | 223 ms: 1.16x slower                                                  |
| genshi_text                | 22.0 ms                                                                | 25.5 ms: 1.16x slower                                                 |
| sqlalchemy_declarative     | 133 ms                                                                 | 154 ms: 1.16x slower                                                  |
| deepcopy_memo              | 30.1 us                                                                | 35.4 us: 1.17x slower                                                 |
| crypto_pyaes               | 70.5 ms                                                                | 83.5 ms: 1.19x slower                                                 |
| typing_runtime_protocols   | 160 us                                                                 | 190 us: 1.19x slower                                                  |
| shortest_path              | 442 ms                                                                 | 529 ms: 1.20x slower                                                  |
| connected_components       | 400 ms                                                                 | 485 ms: 1.21x slower                                                  |
| meteor_contest             | 101 ms                                                                 | 123 ms: 1.22x slower                                                  |
| mako                       | 12.3 ms                                                                | 15.3 ms: 1.24x slower                                                 |
| python_startup_no_site     | 8.68 ms                                                                | 11.1 ms: 1.28x slower                                                 |
| coverage                   | 79.9 ms                                                                | 109 ms: 1.36x slower                                                  |
| bench_thread_pool          | 1.07 ms                                                                | 3.14 ms: 2.94x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.06x slower                                                          |

Benchmark hidden because not significant (1): json
Ignored benchmarks (1) of results/bm-20250408-3.14.0a7+-93646c2-NOGIL/bm-20250408-vultr-x86_64-mpage-exp_no_slp_vectorize-3.14.0a7+-93646c2.json: html5lib

- Geometric mean (including insignificant results): 1.047x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.04x
- 95% likely to have a slowdown of 1.04x
- 99% likely to have a slowdown of 1.04x

# Memory
- memory change: 1.20x