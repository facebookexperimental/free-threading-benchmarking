# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: c0d3c19
- commit date: 2024-12-04
- overall geometric mean: 1.269x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.27x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 257 ms                                                                 | 367 ms: 1.43x slower                                                  |
| docutils       | 2.56 sec                                                               | 3.10 sec: 1.21x slower                                                |
| sphinx         | 991 ms                                                                 | 1.19 sec: 1.20x slower                                                |
| Geometric mean | (ref)                                                                  | 1.28x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_websockets         | 523 ms                                                                 | 521 ms: 1.00x faster                                                  |
| coroutines                 | 22.1 ms                                                                | 25.1 ms: 1.14x slower                                                 |
| async_generators           | 369 ms                                                                 | 459 ms: 1.25x slower                                                  |
| async_tree_cpu_io_mixed_tg | 486 ms                                                                 | 615 ms: 1.27x slower                                                  |
| async_tree_cpu_io_mixed    | 501 ms                                                                 | 639 ms: 1.28x slower                                                  |
| async_tree_io_tg           | 631 ms                                                                 | 826 ms: 1.31x slower                                                  |
| async_tree_io              | 629 ms                                                                 | 851 ms: 1.35x slower                                                  |
| async_tree_none_tg         | 263 ms                                                                 | 360 ms: 1.37x slower                                                  |
| async_tree_none            | 279 ms                                                                 | 388 ms: 1.39x slower                                                  |
| async_tree_memoization     | 337 ms                                                                 | 472 ms: 1.40x slower                                                  |
| async_tree_memoization_tg  | 315 ms                                                                 | 450 ms: 1.43x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.28x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 185 ms                                                                 | 181 ms: 1.02x faster                                                  |
| nbody          | 94.9 ms                                                                | 127 ms: 1.34x slower                                                  |
| float          | 78.1 ms                                                                | 138 ms: 1.76x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.32x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 2.79 ms                                                                | 2.91 ms: 1.04x slower                                                 |
| regex_v8       | 23.5 ms                                                                | 24.7 ms: 1.05x slower                                                 |
| regex_dna      | 173 ms                                                                 | 188 ms: 1.08x slower                                                  |
| regex_compile  | 129 ms                                                                 | 179 ms: 1.39x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.13x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 91.8 ms                                                                | 91.1 ms: 1.01x faster                                                 |
| xml_etree_parse      | 129 ms                                                                 | 132 ms: 1.02x slower                                                  |
| json_loads           | 25.2 us                                                                | 28.4 us: 1.13x slower                                                 |
| xml_etree_generate   | 84.9 ms                                                                | 97.3 ms: 1.15x slower                                                 |
| json_dumps           | 11.4 ms                                                                | 14.3 ms: 1.26x slower                                                 |
| tomli_loads          | 2.09 sec                                                               | 2.66 sec: 1.27x slower                                                |
| xml_etree_process    | 59.3 ms                                                                | 77.3 ms: 1.30x slower                                                 |
| unpickle_pure_python | 216 us                                                                 | 337 us: 1.56x slower                                                  |
| pickle_pure_python   | 317 us                                                                 | 506 us: 1.60x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.24x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.4 ms: 1.19x slower                                                 |
| python_startup_no_site | 7.47 ms                                                                | 10.3 ms: 1.37x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.28x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.3 ms                                                                | 63.8 ms: 1.27x slower                                                 |
| genshi_text     | 22.3 ms                                                                | 32.0 ms: 1.44x slower                                                 |
| django_template | 35.6 ms                                                                | 51.6 ms: 1.45x slower                                                 |
| mako            | 11.8 ms                                                                | 17.7 ms: 1.50x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.41x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241204-vultr-x86_64-python-51cfa569e379f84b3418-3.14.0a2+-51cfa56 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.26 ms                                                                | 3.19 ms: 1.34x faster                                                 |
| create_gc_cycles           | 1.86 ms                                                                | 1.81 ms: 1.03x faster                                                 |
| pidigits                   | 185 ms                                                                 | 181 ms: 1.02x faster                                                  |
| xml_etree_iterparse        | 91.8 ms                                                                | 91.1 ms: 1.01x faster                                                 |
| asyncio_websockets         | 523 ms                                                                 | 521 ms: 1.00x faster                                                  |
| xml_etree_parse            | 129 ms                                                                 | 132 ms: 1.02x slower                                                  |
| sqlite_synth               | 2.24 us                                                                | 2.31 us: 1.03x slower                                                 |
| regex_effbot               | 2.79 ms                                                                | 2.91 ms: 1.04x slower                                                 |
| regex_v8                   | 23.5 ms                                                                | 24.7 ms: 1.05x slower                                                 |
| spectral_norm              | 113 ms                                                                 | 120 ms: 1.07x slower                                                  |
| regex_dna                  | 173 ms                                                                 | 188 ms: 1.08x slower                                                  |
| pathlib                    | 18.2 ms                                                                | 20.2 ms: 1.11x slower                                                 |
| json                       | 4.53 ms                                                                | 5.08 ms: 1.12x slower                                                 |
| json_loads                 | 25.2 us                                                                | 28.4 us: 1.13x slower                                                 |
| coroutines                 | 22.1 ms                                                                | 25.1 ms: 1.14x slower                                                 |
| xml_etree_generate         | 84.9 ms                                                                | 97.3 ms: 1.15x slower                                                 |
| bpe_tokeniser              | 4.32 sec                                                               | 4.97 sec: 1.15x slower                                                |
| mdp                        | 2.47 sec                                                               | 2.88 sec: 1.17x slower                                                |
| k_core                     | 2.07 sec                                                               | 2.42 sec: 1.17x slower                                                |
| scimark_fft                | 335 ms                                                                 | 397 ms: 1.18x slower                                                  |
| telco                      | 7.27 ms                                                                | 8.64 ms: 1.19x slower                                                 |
| python_startup             | 14.6 ms                                                                | 17.4 ms: 1.19x slower                                                 |
| sphinx                     | 991 ms                                                                 | 1.19 sec: 1.20x slower                                                |
| docutils                   | 2.56 sec                                                               | 3.10 sec: 1.21x slower                                                |
| bench_mp_pool              | 88.7 ms                                                                | 109 ms: 1.23x slower                                                  |
| shortest_path              | 444 ms                                                                 | 546 ms: 1.23x slower                                                  |
| async_generators           | 369 ms                                                                 | 459 ms: 1.25x slower                                                  |
| connected_components       | 400 ms                                                                 | 498 ms: 1.25x slower                                                  |
| nqueens                    | 78.6 ms                                                                | 98.4 ms: 1.25x slower                                                 |
| json_dumps                 | 11.4 ms                                                                | 14.3 ms: 1.26x slower                                                 |
| deepcopy                   | 260 us                                                                 | 327 us: 1.26x slower                                                  |
| many_optionals             | 1.02 ms                                                                | 1.29 ms: 1.26x slower                                                 |
| async_tree_cpu_io_mixed_tg | 486 ms                                                                 | 615 ms: 1.27x slower                                                  |
| genshi_xml                 | 50.3 ms                                                                | 63.8 ms: 1.27x slower                                                 |
| dulwich_log                | 75.8 ms                                                                | 96.1 ms: 1.27x slower                                                 |
| tomli_loads                | 2.09 sec                                                               | 2.66 sec: 1.27x slower                                                |
| async_tree_cpu_io_mixed    | 501 ms                                                                 | 639 ms: 1.28x slower                                                  |
| coverage                   | 78.8 ms                                                                | 101 ms: 1.28x slower                                                  |
| typing_runtime_protocols   | 159 us                                                                 | 204 us: 1.28x slower                                                  |
| sqlglot_normalize          | 107 ms                                                                 | 138 ms: 1.29x slower                                                  |
| sqlglot_optimize           | 53.9 ms                                                                | 69.3 ms: 1.29x slower                                                 |
| fannkuch                   | 379 ms                                                                 | 489 ms: 1.29x slower                                                  |
| xml_etree_process          | 59.3 ms                                                                | 77.3 ms: 1.30x slower                                                 |
| meteor_contest             | 99.7 ms                                                                | 130 ms: 1.31x slower                                                  |
| async_tree_io_tg           | 631 ms                                                                 | 826 ms: 1.31x slower                                                  |
| deepcopy_reduce            | 2.65 us                                                                | 3.48 us: 1.31x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                                | 5.84 ms: 1.33x slower                                                 |
| pprint_safe_repr           | 723 ms                                                                 | 961 ms: 1.33x slower                                                  |
| nbody                      | 94.9 ms                                                                | 127 ms: 1.34x slower                                                  |
| crypto_pyaes               | 68.3 ms                                                                | 91.9 ms: 1.35x slower                                                 |
| pylint                     | 284 ms                                                                 | 383 ms: 1.35x slower                                                  |
| deepcopy_memo              | 30.0 us                                                                | 40.5 us: 1.35x slower                                                 |
| async_tree_io              | 629 ms                                                                 | 851 ms: 1.35x slower                                                  |
| generators                 | 28.7 ms                                                                | 39.0 ms: 1.35x slower                                                 |
| async_tree_none_tg         | 263 ms                                                                 | 360 ms: 1.37x slower                                                  |
| pprint_pformat             | 1.46 sec                                                               | 2.00 sec: 1.37x slower                                                |
| python_startup_no_site     | 7.47 ms                                                                | 10.3 ms: 1.37x slower                                                 |
| pycparser                  | 1.13 sec                                                               | 1.55 sec: 1.37x slower                                                |
| regex_compile              | 129 ms                                                                 | 179 ms: 1.39x slower                                                  |
| async_tree_none            | 279 ms                                                                 | 388 ms: 1.39x slower                                                  |
| async_tree_memoization     | 337 ms                                                                 | 472 ms: 1.40x slower                                                  |
| subparsers                 | 22.0 ms                                                                | 31.4 ms: 1.42x slower                                                 |
| 2to3                       | 257 ms                                                                 | 367 ms: 1.43x slower                                                  |
| async_tree_memoization_tg  | 315 ms                                                                 | 450 ms: 1.43x slower                                                  |
| genshi_text                | 22.3 ms                                                                | 32.0 ms: 1.44x slower                                                 |
| django_template            | 35.6 ms                                                                | 51.6 ms: 1.45x slower                                                 |
| sympy_integrate            | 20.0 ms                                                                | 29.5 ms: 1.48x slower                                                 |
| mako                       | 11.8 ms                                                                | 17.7 ms: 1.50x slower                                                 |
| pyflate                    | 449 ms                                                                 | 684 ms: 1.52x slower                                                  |
| comprehensions             | 17.6 us                                                                | 27.4 us: 1.56x slower                                                 |
| unpickle_pure_python       | 216 us                                                                 | 337 us: 1.56x slower                                                  |
| sqlalchemy_imperative      | 18.9 ms                                                                | 29.8 ms: 1.57x slower                                                 |
| thrift                     | 734 us                                                                 | 1.16 ms: 1.58x slower                                                 |
| pickle_pure_python         | 317 us                                                                 | 506 us: 1.60x slower                                                  |
| sqlalchemy_declarative     | 127 ms                                                                 | 204 ms: 1.61x slower                                                  |
| richards_super             | 52.4 ms                                                                | 87.2 ms: 1.66x slower                                                 |
| richards                   | 46.6 ms                                                                | 77.9 ms: 1.67x slower                                                 |
| hexiom                     | 5.87 ms                                                                | 9.92 ms: 1.69x slower                                                 |
| scimark_lu                 | 109 ms                                                                 | 185 ms: 1.70x slower                                                  |
| logging_format             | 6.88 us                                                                | 11.8 us: 1.71x slower                                                 |
| sympy_str                  | 273 ms                                                                 | 475 ms: 1.74x slower                                                  |
| float                      | 78.1 ms                                                                | 138 ms: 1.76x slower                                                  |
| logging_silent             | 106 ns                                                                 | 187 ns: 1.77x slower                                                  |
| scimark_sor                | 134 ms                                                                 | 237 ms: 1.78x slower                                                  |
| chaos                      | 58.9 ms                                                                | 105 ms: 1.78x slower                                                  |
| logging_simple             | 6.06 us                                                                | 10.8 us: 1.78x slower                                                 |
| scimark_monte_carlo        | 65.2 ms                                                                | 118 ms: 1.80x slower                                                  |
| sqlglot_transpile          | 1.61 ms                                                                | 2.96 ms: 1.84x slower                                                 |
| sqlglot_parse              | 1.29 ms                                                                | 2.56 ms: 1.98x slower                                                 |
| sympy_expand               | 462 ms                                                                 | 952 ms: 2.06x slower                                                  |
| raytrace                   | 264 ms                                                                 | 557 ms: 2.11x slower                                                  |
| go                         | 120 ms                                                                 | 270 ms: 2.24x slower                                                  |
| sympy_sum                  | 154 ms                                                                 | 349 ms: 2.27x slower                                                  |
| deltablue                  | 3.22 ms                                                                | 8.05 ms: 2.50x slower                                                 |
| bench_thread_pool          | 1.01 ms                                                                | 3.37 ms: 3.32x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.38x slower                                                          |
Ignored benchmarks (1) of results/bm-20241204-3.14.0a2+-c0d3c19-NOGIL/bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19.json: html5lib

- Geometric mean (including insignificant results): 1.269x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.29x
- 95% likely to have a slowdown of 1.28x
- 99% likely to have a slowdown of 1.27x

# Memory
- memory change: 1.19x