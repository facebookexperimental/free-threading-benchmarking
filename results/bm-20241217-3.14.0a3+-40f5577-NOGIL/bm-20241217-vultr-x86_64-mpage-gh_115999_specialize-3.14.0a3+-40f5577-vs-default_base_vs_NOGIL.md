# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_specialize
- machine: linux-x86_64
- commit hash: 40f5577
- commit date: 2024-12-17
- overall geometric mean: 1.245x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.24x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 255 ms                                                                 | 360 ms: 1.41x slower                                                  |
| docutils       | 2.54 sec                                                               | 3.06 sec: 1.20x slower                                                |
| sphinx         | 987 ms                                                                 | 1.16 sec: 1.18x slower                                                |
| Geometric mean | (ref)                                                                  | 1.26x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_websockets        | 523 ms                                                                 | 516 ms: 1.01x faster                                                  |
| coroutines                | 21.8 ms                                                                | 24.1 ms: 1.11x slower                                                 |
| async_tree_io_tg          | 609 ms                                                                 | 732 ms: 1.20x slower                                                  |
| async_tree_io             | 621 ms                                                                 | 760 ms: 1.22x slower                                                  |
| async_tree_none_tg        | 257 ms                                                                 | 323 ms: 1.26x slower                                                  |
| async_generators          | 353 ms                                                                 | 448 ms: 1.27x slower                                                  |
| async_tree_memoization    | 336 ms                                                                 | 430 ms: 1.28x slower                                                  |
| async_tree_none           | 277 ms                                                                 | 356 ms: 1.29x slower                                                  |
| async_tree_memoization_tg | 308 ms                                                                 | 405 ms: 1.32x slower                                                  |
| Geometric mean            | (ref)                                                                  | 1.17x slower                                                          |

Benchmark hidden because not significant (2): async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 222 ms                                                                 | 181 ms: 1.22x faster                                                  |
| nbody          | 89.7 ms                                                                | 125 ms: 1.40x slower                                                  |
| float          | 75.9 ms                                                                | 111 ms: 1.46x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.19x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 24.1 ms                                                                | 25.2 ms: 1.04x slower                                                 |
| regex_effbot   | 2.82 ms                                                                | 2.98 ms: 1.06x slower                                                 |
| regex_dna      | 173 ms                                                                 | 187 ms: 1.08x slower                                                  |
| regex_compile  | 126 ms                                                                 | 170 ms: 1.35x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_parse      | 128 ms                                                                 | 130 ms: 1.01x slower                                                  |
| json_loads           | 26.3 us                                                                | 28.4 us: 1.08x slower                                                 |
| xml_etree_generate   | 84.1 ms                                                                | 96.6 ms: 1.15x slower                                                 |
| json_dumps           | 11.4 ms                                                                | 14.0 ms: 1.22x slower                                                 |
| xml_etree_process    | 58.7 ms                                                                | 73.9 ms: 1.26x slower                                                 |
| tomli_loads          | 1.97 sec                                                               | 2.53 sec: 1.28x slower                                                |
| unpickle_pure_python | 211 us                                                                 | 327 us: 1.55x slower                                                  |
| pickle_pure_python   | 313 us                                                                 | 504 us: 1.61x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.22x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 17.1 ms: 1.17x slower                                                 |
| python_startup_no_site | 7.50 ms                                                                | 10.2 ms: 1.36x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 49.8 ms                                                                | 62.6 ms: 1.26x slower                                                 |
| genshi_text     | 21.6 ms                                                                | 30.0 ms: 1.39x slower                                                 |
| django_template | 35.1 ms                                                                | 50.0 ms: 1.42x slower                                                 |
| mako            | 11.7 ms                                                                | 17.1 ms: 1.47x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.38x slower                                                          |

All benchmarks:
===============

| Benchmark                 | bm-20241217-vultr-x86_64-python-329165639f9ac00ba64f-3.14.0a3+-3291656 | bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577 |
|---------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal              | 4.20 ms                                                                | 3.28 ms: 1.28x faster                                                 |
| pidigits                  | 222 ms                                                                 | 181 ms: 1.22x faster                                                  |
| sqlite_synth              | 2.25 us                                                                | 2.16 us: 1.04x faster                                                 |
| create_gc_cycles          | 1.84 ms                                                                | 1.80 ms: 1.02x faster                                                 |
| asyncio_websockets        | 523 ms                                                                 | 516 ms: 1.01x faster                                                  |
| xml_etree_parse           | 128 ms                                                                 | 130 ms: 1.01x slower                                                  |
| regex_v8                  | 24.1 ms                                                                | 25.2 ms: 1.04x slower                                                 |
| regex_effbot              | 2.82 ms                                                                | 2.98 ms: 1.06x slower                                                 |
| json                      | 4.78 ms                                                                | 5.07 ms: 1.06x slower                                                 |
| pathlib                   | 18.3 ms                                                                | 19.6 ms: 1.08x slower                                                 |
| json_loads                | 26.3 us                                                                | 28.4 us: 1.08x slower                                                 |
| regex_dna                 | 173 ms                                                                 | 187 ms: 1.08x slower                                                  |
| coroutines                | 21.8 ms                                                                | 24.1 ms: 1.11x slower                                                 |
| spectral_norm             | 98.0 ms                                                                | 109 ms: 1.11x slower                                                  |
| k_core                    | 2.05 sec                                                               | 2.35 sec: 1.14x slower                                                |
| xml_etree_generate        | 84.1 ms                                                                | 96.6 ms: 1.15x slower                                                 |
| mdp                       | 2.32 sec                                                               | 2.69 sec: 1.16x slower                                                |
| bpe_tokeniser             | 4.25 sec                                                               | 4.96 sec: 1.17x slower                                                |
| python_startup            | 14.7 ms                                                                | 17.1 ms: 1.17x slower                                                 |
| sphinx                    | 987 ms                                                                 | 1.16 sec: 1.18x slower                                                |
| many_optionals            | 1.03 ms                                                                | 1.23 ms: 1.19x slower                                                 |
| bench_mp_pool             | 89.3 ms                                                                | 107 ms: 1.20x slower                                                  |
| scimark_fft               | 309 ms                                                                 | 372 ms: 1.20x slower                                                  |
| async_tree_io_tg          | 609 ms                                                                 | 732 ms: 1.20x slower                                                  |
| docutils                  | 2.54 sec                                                               | 3.06 sec: 1.20x slower                                                |
| telco                     | 7.15 ms                                                                | 8.65 ms: 1.21x slower                                                 |
| dulwich_log               | 75.3 ms                                                                | 91.2 ms: 1.21x slower                                                 |
| json_dumps                | 11.4 ms                                                                | 14.0 ms: 1.22x slower                                                 |
| async_tree_io             | 621 ms                                                                 | 760 ms: 1.22x slower                                                  |
| connected_components      | 399 ms                                                                 | 499 ms: 1.25x slower                                                  |
| genshi_xml                | 49.8 ms                                                                | 62.6 ms: 1.26x slower                                                 |
| shortest_path             | 439 ms                                                                 | 551 ms: 1.26x slower                                                  |
| async_tree_none_tg        | 257 ms                                                                 | 323 ms: 1.26x slower                                                  |
| xml_etree_process         | 58.7 ms                                                                | 73.9 ms: 1.26x slower                                                 |
| pycparser                 | 1.11 sec                                                               | 1.40 sec: 1.26x slower                                                |
| coverage                  | 79.3 ms                                                                | 100 ms: 1.27x slower                                                  |
| sqlglot_optimize          | 51.9 ms                                                                | 65.8 ms: 1.27x slower                                                 |
| async_generators          | 353 ms                                                                 | 448 ms: 1.27x slower                                                  |
| nqueens                   | 77.1 ms                                                                | 98.2 ms: 1.27x slower                                                 |
| async_tree_memoization    | 336 ms                                                                 | 430 ms: 1.28x slower                                                  |
| tomli_loads               | 1.97 sec                                                               | 2.53 sec: 1.28x slower                                                |
| deepcopy                  | 253 us                                                                 | 325 us: 1.28x slower                                                  |
| async_tree_none           | 277 ms                                                                 | 356 ms: 1.29x slower                                                  |
| sqlglot_normalize         | 103 ms                                                                 | 133 ms: 1.29x slower                                                  |
| scimark_sparse_mat_mult   | 4.18 ms                                                                | 5.42 ms: 1.30x slower                                                 |
| meteor_contest            | 100 ms                                                                 | 130 ms: 1.30x slower                                                  |
| pylint                    | 279 ms                                                                 | 365 ms: 1.31x slower                                                  |
| fannkuch                  | 371 ms                                                                 | 486 ms: 1.31x slower                                                  |
| async_tree_memoization_tg | 308 ms                                                                 | 405 ms: 1.32x slower                                                  |
| crypto_pyaes              | 67.3 ms                                                                | 89.0 ms: 1.32x slower                                                 |
| deepcopy_reduce           | 2.58 us                                                                | 3.42 us: 1.33x slower                                                 |
| subparsers                | 21.7 ms                                                                | 29.1 ms: 1.34x slower                                                 |
| typing_runtime_protocols  | 156 us                                                                 | 208 us: 1.34x slower                                                  |
| thrift                    | 736 us                                                                 | 987 us: 1.34x slower                                                  |
| deepcopy_memo             | 29.6 us                                                                | 39.8 us: 1.34x slower                                                 |
| regex_compile             | 126 ms                                                                 | 170 ms: 1.35x slower                                                  |
| python_startup_no_site    | 7.50 ms                                                                | 10.2 ms: 1.36x slower                                                 |
| pprint_safe_repr          | 702 ms                                                                 | 961 ms: 1.37x slower                                                  |
| pprint_pformat            | 1.45 sec                                                               | 2.00 sec: 1.38x slower                                                |
| genshi_text               | 21.6 ms                                                                | 30.0 ms: 1.39x slower                                                 |
| nbody                     | 89.7 ms                                                                | 125 ms: 1.40x slower                                                  |
| 2to3                      | 255 ms                                                                 | 360 ms: 1.41x slower                                                  |
| generators                | 27.0 ms                                                                | 38.4 ms: 1.42x slower                                                 |
| django_template           | 35.1 ms                                                                | 50.0 ms: 1.42x slower                                                 |
| float                     | 75.9 ms                                                                | 111 ms: 1.46x slower                                                  |
| mako                      | 11.7 ms                                                                | 17.1 ms: 1.47x slower                                                 |
| sqlalchemy_imperative     | 18.9 ms                                                                | 27.8 ms: 1.47x slower                                                 |
| sympy_integrate           | 19.7 ms                                                                | 29.4 ms: 1.49x slower                                                 |
| logging_format            | 6.79 us                                                                | 10.2 us: 1.50x slower                                                 |
| logging_simple            | 6.04 us                                                                | 9.08 us: 1.50x slower                                                 |
| pyflate                   | 424 ms                                                                 | 650 ms: 1.53x slower                                                  |
| richards_super            | 50.3 ms                                                                | 77.5 ms: 1.54x slower                                                 |
| unpickle_pure_python      | 211 us                                                                 | 327 us: 1.55x slower                                                  |
| richards                  | 44.4 ms                                                                | 68.9 ms: 1.55x slower                                                 |
| sqlalchemy_declarative    | 125 ms                                                                 | 197 ms: 1.57x slower                                                  |
| pickle_pure_python        | 313 us                                                                 | 504 us: 1.61x slower                                                  |
| comprehensions            | 16.9 us                                                                | 27.5 us: 1.63x slower                                                 |
| scimark_lu                | 111 ms                                                                 | 183 ms: 1.65x slower                                                  |
| chaos                     | 57.5 ms                                                                | 95.1 ms: 1.65x slower                                                 |
| hexiom                    | 5.80 ms                                                                | 9.72 ms: 1.67x slower                                                 |
| scimark_monte_carlo       | 62.9 ms                                                                | 105 ms: 1.67x slower                                                  |
| sqlglot_transpile         | 1.56 ms                                                                | 2.70 ms: 1.73x slower                                                 |
| sympy_str                 | 270 ms                                                                 | 475 ms: 1.76x slower                                                  |
| logging_silent            | 104 ns                                                                 | 185 ns: 1.77x slower                                                  |
| sqlglot_parse             | 1.25 ms                                                                | 2.34 ms: 1.87x slower                                                 |
| scimark_sor               | 123 ms                                                                 | 231 ms: 1.87x slower                                                  |
| raytrace                  | 256 ms                                                                 | 498 ms: 1.94x slower                                                  |
| sympy_expand              | 455 ms                                                                 | 956 ms: 2.10x slower                                                  |
| go                        | 115 ms                                                                 | 243 ms: 2.11x slower                                                  |
| sympy_sum                 | 153 ms                                                                 | 347 ms: 2.28x slower                                                  |
| deltablue                 | 3.15 ms                                                                | 7.60 ms: 2.41x slower                                                 |
| bench_thread_pool         | 1.03 ms                                                                | 3.38 ms: 3.28x slower                                                 |
| Geometric mean            | (ref)                                                                  | 1.34x slower                                                          |

Benchmark hidden because not significant (3): async_tree_cpu_io_mixed_tg, xml_etree_iterparse, async_tree_cpu_io_mixed
Ignored benchmarks (1) of results/bm-20241217-3.14.0a3+-40f5577-NOGIL/bm-20241217-vultr-x86_64-mpage-gh_115999_specialize-3.14.0a3+-40f5577.json: html5lib

- Geometric mean (including insignificant results): 1.245x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.26x
- 95% likely to have a slowdown of 1.25x
- 99% likely to have a slowdown of 1.24x

# Memory
- memory change: 1.19x