# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_load_attr_
- machine: linux-x86_64
- commit hash: d6d4c73
- commit date: 2024-12-20
- overall geometric mean: 1.157x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.12x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 322 ms: 1.26x slower                                                  |
| docutils       | 2.54 sec                                                               | 2.84 sec: 1.12x slower                                                |
| sphinx         | 989 ms                                                                 | 1.12 sec: 1.13x slower                                                |
| Geometric mean | (ref)                                                                  | 1.17x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_cpu_io_mixed_tg | 549 ms                                                                 | 484 ms: 1.13x faster                                                  |
| async_tree_cpu_io_mixed    | 566 ms                                                                 | 518 ms: 1.09x faster                                                  |
| async_tree_none_tg         | 254 ms                                                                 | 241 ms: 1.06x faster                                                  |
| async_tree_io              | 624 ms                                                                 | 604 ms: 1.03x faster                                                  |
| async_tree_io_tg           | 605 ms                                                                 | 586 ms: 1.03x faster                                                  |
| asyncio_websockets         | 523 ms                                                                 | 518 ms: 1.01x faster                                                  |
| async_tree_memoization_tg  | 307 ms                                                                 | 315 ms: 1.03x slower                                                  |
| async_tree_none            | 275 ms                                                                 | 284 ms: 1.03x slower                                                  |
| async_tree_memoization     | 332 ms                                                                 | 350 ms: 1.06x slower                                                  |
| coroutines                 | 22.2 ms                                                                | 24.0 ms: 1.08x slower                                                 |
| async_generators           | 357 ms                                                                 | 420 ms: 1.18x slower                                                  |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                                 | 184 ms: 1.18x faster                                                  |
| float          | 74.6 ms                                                                | 81.9 ms: 1.10x slower                                                 |
| nbody          | 91.1 ms                                                                | 136 ms: 1.49x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.12x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 25.0 ms                                                                | 24.3 ms: 1.03x faster                                                 |
| regex_dna      | 181 ms                                                                 | 177 ms: 1.02x faster                                                  |
| regex_effbot   | 2.81 ms                                                                | 2.92 ms: 1.04x slower                                                 |
| regex_compile  | 127 ms                                                                 | 151 ms: 1.19x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.04x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 90.6 ms                                                                | 88.5 ms: 1.02x faster                                                 |
| xml_etree_parse      | 127 ms                                                                 | 130 ms: 1.03x slower                                                  |
| json_loads           | 26.1 us                                                                | 27.9 us: 1.07x slower                                                 |
| json_dumps           | 11.3 ms                                                                | 13.1 ms: 1.16x slower                                                 |
| unpickle_pure_python | 213 us                                                                 | 247 us: 1.16x slower                                                  |
| xml_etree_generate   | 82.9 ms                                                                | 96.8 ms: 1.17x slower                                                 |
| pickle_pure_python   | 316 us                                                                 | 370 us: 1.17x slower                                                  |
| xml_etree_process    | 57.9 ms                                                                | 68.6 ms: 1.19x slower                                                 |
| tomli_loads          | 1.90 sec                                                               | 2.49 sec: 1.31x slower                                                |
| Geometric mean       | (ref)                                                                  | 1.13x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 14.6 ms                                                                | 17.1 ms: 1.16x slower                                                 |
| python_startup_no_site | 7.48 ms                                                                | 10.2 ms: 1.36x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.26x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.9 ms                                                                | 60.1 ms: 1.23x slower                                                 |
| django_template | 34.7 ms                                                                | 42.9 ms: 1.24x slower                                                 |
| genshi_text     | 21.4 ms                                                                | 28.5 ms: 1.33x slower                                                 |
| mako            | 11.5 ms                                                                | 15.8 ms: 1.37x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.29x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20241219-vultr-x86_64-python-39e69a7cd54d44c9061d-3.14.0a3+-39e69a7 | bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73 |
|----------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal               | 4.37 ms                                                                | 3.29 ms: 1.33x faster                                                 |
| pidigits                   | 217 ms                                                                 | 184 ms: 1.18x faster                                                  |
| async_tree_cpu_io_mixed_tg | 549 ms                                                                 | 484 ms: 1.13x faster                                                  |
| async_tree_cpu_io_mixed    | 566 ms                                                                 | 518 ms: 1.09x faster                                                  |
| sqlite_synth               | 2.21 us                                                                | 2.07 us: 1.07x faster                                                 |
| async_tree_none_tg         | 254 ms                                                                 | 241 ms: 1.06x faster                                                  |
| async_tree_io              | 624 ms                                                                 | 604 ms: 1.03x faster                                                  |
| async_tree_io_tg           | 605 ms                                                                 | 586 ms: 1.03x faster                                                  |
| create_gc_cycles           | 1.85 ms                                                                | 1.79 ms: 1.03x faster                                                 |
| regex_v8                   | 25.0 ms                                                                | 24.3 ms: 1.03x faster                                                 |
| xml_etree_iterparse        | 90.6 ms                                                                | 88.5 ms: 1.02x faster                                                 |
| regex_dna                  | 181 ms                                                                 | 177 ms: 1.02x faster                                                  |
| asyncio_websockets         | 523 ms                                                                 | 518 ms: 1.01x faster                                                  |
| json                       | 4.79 ms                                                                | 4.89 ms: 1.02x slower                                                 |
| xml_etree_parse            | 127 ms                                                                 | 130 ms: 1.03x slower                                                  |
| async_tree_memoization_tg  | 307 ms                                                                 | 315 ms: 1.03x slower                                                  |
| async_tree_none            | 275 ms                                                                 | 284 ms: 1.03x slower                                                  |
| regex_effbot               | 2.81 ms                                                                | 2.92 ms: 1.04x slower                                                 |
| async_tree_memoization     | 332 ms                                                                 | 350 ms: 1.06x slower                                                  |
| json_loads                 | 26.1 us                                                                | 27.9 us: 1.07x slower                                                 |
| pathlib                    | 17.9 ms                                                                | 19.1 ms: 1.07x slower                                                 |
| coroutines                 | 22.2 ms                                                                | 24.0 ms: 1.08x slower                                                 |
| pycparser                  | 1.11 sec                                                               | 1.22 sec: 1.09x slower                                                |
| logging_silent             | 106 ns                                                                 | 116 ns: 1.09x slower                                                  |
| float                      | 74.6 ms                                                                | 81.9 ms: 1.10x slower                                                 |
| dulwich_log                | 74.3 ms                                                                | 82.5 ms: 1.11x slower                                                 |
| mdp                        | 2.34 sec                                                               | 2.60 sec: 1.11x slower                                                |
| docutils                   | 2.54 sec                                                               | 2.84 sec: 1.12x slower                                                |
| bpe_tokeniser              | 4.28 sec                                                               | 4.79 sec: 1.12x slower                                                |
| k_core                     | 2.06 sec                                                               | 2.32 sec: 1.13x slower                                                |
| sphinx                     | 989 ms                                                                 | 1.12 sec: 1.13x slower                                                |
| many_optionals             | 1.03 ms                                                                | 1.18 ms: 1.14x slower                                                 |
| generators                 | 27.1 ms                                                                | 31.3 ms: 1.15x slower                                                 |
| json_dumps                 | 11.3 ms                                                                | 13.1 ms: 1.16x slower                                                 |
| unpickle_pure_python       | 213 us                                                                 | 247 us: 1.16x slower                                                  |
| python_startup             | 14.6 ms                                                                | 17.1 ms: 1.16x slower                                                 |
| xml_etree_generate         | 82.9 ms                                                                | 96.8 ms: 1.17x slower                                                 |
| telco                      | 7.25 ms                                                                | 8.47 ms: 1.17x slower                                                 |
| pickle_pure_python         | 316 us                                                                 | 370 us: 1.17x slower                                                  |
| sqlglot_normalize          | 103 ms                                                                 | 121 ms: 1.17x slower                                                  |
| spectral_norm              | 97.3 ms                                                                | 115 ms: 1.18x slower                                                  |
| async_generators           | 357 ms                                                                 | 420 ms: 1.18x slower                                                  |
| sqlglot_optimize           | 52.0 ms                                                                | 61.4 ms: 1.18x slower                                                 |
| pyflate                    | 419 ms                                                                 | 497 ms: 1.18x slower                                                  |
| xml_etree_process          | 57.9 ms                                                                | 68.6 ms: 1.19x slower                                                 |
| subparsers                 | 21.6 ms                                                                | 25.7 ms: 1.19x slower                                                 |
| regex_compile              | 127 ms                                                                 | 151 ms: 1.19x slower                                                  |
| bench_mp_pool              | 88.6 ms                                                                | 105 ms: 1.19x slower                                                  |
| pprint_safe_repr           | 704 ms                                                                 | 841 ms: 1.19x slower                                                  |
| chaos                      | 58.9 ms                                                                | 71.1 ms: 1.21x slower                                                 |
| pprint_pformat             | 1.44 sec                                                               | 1.74 sec: 1.21x slower                                                |
| scimark_fft                | 313 ms                                                                 | 380 ms: 1.21x slower                                                  |
| genshi_xml                 | 48.9 ms                                                                | 60.1 ms: 1.23x slower                                                 |
| pylint                     | 282 ms                                                                 | 346 ms: 1.23x slower                                                  |
| go                         | 116 ms                                                                 | 143 ms: 1.23x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                                | 1.93 ms: 1.23x slower                                                 |
| comprehensions             | 17.0 us                                                                | 21.0 us: 1.23x slower                                                 |
| django_template            | 34.7 ms                                                                | 42.9 ms: 1.24x slower                                                 |
| thrift                     | 739 us                                                                 | 915 us: 1.24x slower                                                  |
| deepcopy                   | 253 us                                                                 | 314 us: 1.24x slower                                                  |
| raytrace                   | 260 ms                                                                 | 323 ms: 1.24x slower                                                  |
| logging_simple             | 5.95 us                                                                | 7.42 us: 1.25x slower                                                 |
| connected_components       | 394 ms                                                                 | 494 ms: 1.25x slower                                                  |
| coverage                   | 79.2 ms                                                                | 99.3 ms: 1.25x slower                                                 |
| nqueens                    | 77.7 ms                                                                | 97.5 ms: 1.26x slower                                                 |
| shortest_path              | 433 ms                                                                 | 544 ms: 1.26x slower                                                  |
| deepcopy_reduce            | 2.57 us                                                                | 3.23 us: 1.26x slower                                                 |
| 2to3                       | 256 ms                                                                 | 322 ms: 1.26x slower                                                  |
| sqlalchemy_imperative      | 19.4 ms                                                                | 24.4 ms: 1.26x slower                                                 |
| typing_runtime_protocols   | 157 us                                                                 | 199 us: 1.26x slower                                                  |
| logging_format             | 6.63 us                                                                | 8.39 us: 1.27x slower                                                 |
| sqlglot_parse              | 1.26 ms                                                                | 1.60 ms: 1.27x slower                                                 |
| scimark_lu                 | 111 ms                                                                 | 142 ms: 1.27x slower                                                  |
| deepcopy_memo              | 30.1 us                                                                | 38.7 us: 1.28x slower                                                 |
| crypto_pyaes               | 67.5 ms                                                                | 86.8 ms: 1.29x slower                                                 |
| hexiom                     | 5.88 ms                                                                | 7.62 ms: 1.30x slower                                                 |
| tomli_loads                | 1.90 sec                                                               | 2.49 sec: 1.31x slower                                                |
| meteor_contest             | 98.9 ms                                                                | 130 ms: 1.32x slower                                                  |
| genshi_text                | 21.4 ms                                                                | 28.5 ms: 1.33x slower                                                 |
| scimark_monte_carlo        | 63.4 ms                                                                | 84.5 ms: 1.33x slower                                                 |
| scimark_sparse_mat_mult    | 4.26 ms                                                                | 5.69 ms: 1.34x slower                                                 |
| fannkuch                   | 365 ms                                                                 | 490 ms: 1.34x slower                                                  |
| richards                   | 42.3 ms                                                                | 56.9 ms: 1.35x slower                                                 |
| richards_super             | 48.6 ms                                                                | 65.9 ms: 1.35x slower                                                 |
| python_startup_no_site     | 7.48 ms                                                                | 10.2 ms: 1.36x slower                                                 |
| mako                       | 11.5 ms                                                                | 15.8 ms: 1.37x slower                                                 |
| sqlalchemy_declarative     | 128 ms                                                                 | 176 ms: 1.38x slower                                                  |
| scimark_sor                | 117 ms                                                                 | 162 ms: 1.38x slower                                                  |
| sympy_integrate            | 19.8 ms                                                                | 28.9 ms: 1.45x slower                                                 |
| nbody                      | 91.1 ms                                                                | 136 ms: 1.49x slower                                                  |
| deltablue                  | 3.17 ms                                                                | 4.84 ms: 1.53x slower                                                 |
| sympy_str                  | 272 ms                                                                 | 459 ms: 1.69x slower                                                  |
| sympy_expand               | 456 ms                                                                 | 929 ms: 2.04x slower                                                  |
| sympy_sum                  | 153 ms                                                                 | 343 ms: 2.24x slower                                                  |
| bench_thread_pool          | 1.03 ms                                                                | 3.34 ms: 3.23x slower                                                 |
| Geometric mean             | (ref)                                                                  | 1.20x slower                                                          |
Ignored benchmarks (1) of results/bm-20241220-3.14.0a3+-d6d4c73-NOGIL/bm-20241220-vultr-x86_64-mpage-gh_115999_load_attr_-3.14.0a3+-d6d4c73.json: html5lib

- Geometric mean (including insignificant results): 1.157x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.16x
- 95% likely to have a slowdown of 1.14x
- 99% likely to have a slowdown of 1.12x

# Memory
- memory change: 1.20x