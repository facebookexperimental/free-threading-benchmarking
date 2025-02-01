# Results vs. base

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: d89a5f6
- commit date: 2025-01-31
- overall geometric mean: 1.104x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.09x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250131-vultr-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4+-d89a5f6 | bm-20250131-vultr-x86_64-python-main-3.14.0a4+-d89a5f6 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 296 ms: 1.17x slower                                   |
| docutils       | 2.56 sec                                                               | 2.75 sec: 1.08x slower                                 |
| sphinx         | 979 ms                                                                 | 1.09 sec: 1.12x slower                                 |
| Geometric mean | (ref)                                                                  | 1.12x slower                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20250131-vultr-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4+-d89a5f6 | bm-20250131-vultr-x86_64-python-main-3.14.0a4+-d89a5f6 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| async_tree_io_tg           | 631 ms                                                                 | 559 ms: 1.13x faster                                   |
| async_tree_io              | 626 ms                                                                 | 597 ms: 1.05x faster                                   |
| async_tree_none_tg         | 265 ms                                                                 | 255 ms: 1.04x faster                                   |
| async_tree_memoization_tg  | 316 ms                                                                 | 312 ms: 1.01x faster                                   |
| coroutines                 | 22.9 ms                                                                | 22.6 ms: 1.01x faster                                  |
| async_tree_cpu_io_mixed_tg | 487 ms                                                                 | 495 ms: 1.02x slower                                   |
| async_tree_none            | 274 ms                                                                 | 282 ms: 1.03x slower                                   |
| async_tree_memoization     | 327 ms                                                                 | 345 ms: 1.05x slower                                   |
| async_tree_cpu_io_mixed    | 501 ms                                                                 | 529 ms: 1.06x slower                                   |
| async_generators           | 328 ms                                                                 | 368 ms: 1.12x slower                                   |
| Geometric mean             | (ref)                                                                  | 1.00x slower                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250131-vultr-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4+-d89a5f6 | bm-20250131-vultr-x86_64-python-main-3.14.0a4+-d89a5f6 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| float          | 73.1 ms                                                                | 73.9 ms: 1.01x slower                                  |
| pidigits       | 187 ms                                                                 | 197 ms: 1.05x slower                                   |
| nbody          | 92.2 ms                                                                | 126 ms: 1.36x slower                                   |
| Geometric mean | (ref)                                                                  | 1.13x slower                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250131-vultr-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4+-d89a5f6 | bm-20250131-vultr-x86_64-python-main-3.14.0a4+-d89a5f6 |
|----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| regex_effbot   | 2.83 ms                                                                | 2.77 ms: 1.02x faster                                  |
| regex_v8       | 23.8 ms                                                                | 23.6 ms: 1.01x faster                                  |
| regex_dna      | 168 ms                                                                 | 182 ms: 1.09x slower                                   |
| regex_compile  | 127 ms                                                                 | 145 ms: 1.14x slower                                   |
| Geometric mean | (ref)                                                                  | 1.05x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250131-vultr-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4+-d89a5f6 | bm-20250131-vultr-x86_64-python-main-3.14.0a4+-d89a5f6 |
|----------------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| xml_etree_iterparse  | 91.6 ms                                                                | 87.3 ms: 1.05x faster                                  |
| json_dumps           | 11.5 ms                                                                | 12.6 ms: 1.10x slower                                  |
| json_loads           | 28.6 us                                                                | 31.4 us: 1.10x slower                                  |
| unpickle_pure_python | 218 us                                                                 | 241 us: 1.11x slower                                   |
| xml_etree_generate   | 83.7 ms                                                                | 94.9 ms: 1.13x slower                                  |
| pickle_pure_python   | 312 us                                                                 | 356 us: 1.14x slower                                   |
| xml_etree_process    | 58.0 ms                                                                | 67.4 ms: 1.16x slower                                  |
| tomli_loads          | 1.94 sec                                                               | 2.26 sec: 1.16x slower                                 |
| Geometric mean       | (ref)                                                                  | 1.09x slower                                           |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20250131-vultr-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4+-d89a5f6 | bm-20250131-vultr-x86_64-python-main-3.14.0a4+-d89a5f6 |
|------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| python_startup         | 14.7 ms                                                                | 15.3 ms: 1.04x slower                                  |
| python_startup_no_site | 7.46 ms                                                                | 9.61 ms: 1.29x slower                                  |
| Geometric mean         | (ref)                                                                  | 1.16x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250131-vultr-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4+-d89a5f6 | bm-20250131-vultr-x86_64-python-main-3.14.0a4+-d89a5f6 |
|-----------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| genshi_xml      | 49.0 ms                                                                | 57.5 ms: 1.17x slower                                  |
| django_template | 34.4 ms                                                                | 40.7 ms: 1.18x slower                                  |
| genshi_text     | 21.3 ms                                                                | 26.8 ms: 1.26x slower                                  |
| mako            | 12.2 ms                                                                | 15.6 ms: 1.29x slower                                  |
| Geometric mean  | (ref)                                                                  | 1.22x slower                                           |

All benchmarks:
===============

| Benchmark                  | bm-20250131-vultr-x86_64-python-d89a5f6a6e65511a5f6e-3.14.0a4+-d89a5f6 | bm-20250131-vultr-x86_64-python-main-3.14.0a4+-d89a5f6 |
|----------------------------|:----------------------------------------------------------------------:|:------------------------------------------------------:|
| gc_traversal               | 4.03 ms                                                                | 1.64 ms: 2.45x faster                                  |
| create_gc_cycles           | 1.85 ms                                                                | 1.37 ms: 1.35x faster                                  |
| async_tree_io_tg           | 631 ms                                                                 | 559 ms: 1.13x faster                                   |
| sqlite_synth               | 2.18 us                                                                | 2.05 us: 1.06x faster                                  |
| xml_etree_iterparse        | 91.6 ms                                                                | 87.3 ms: 1.05x faster                                  |
| async_tree_io              | 626 ms                                                                 | 597 ms: 1.05x faster                                   |
| async_tree_none_tg         | 265 ms                                                                 | 255 ms: 1.04x faster                                   |
| regex_effbot               | 2.83 ms                                                                | 2.77 ms: 1.02x faster                                  |
| pathlib                    | 18.5 ms                                                                | 18.2 ms: 1.02x faster                                  |
| async_tree_memoization_tg  | 316 ms                                                                 | 312 ms: 1.01x faster                                   |
| regex_v8                   | 23.8 ms                                                                | 23.6 ms: 1.01x faster                                  |
| coroutines                 | 22.9 ms                                                                | 22.6 ms: 1.01x faster                                  |
| float                      | 73.1 ms                                                                | 73.9 ms: 1.01x slower                                  |
| async_tree_cpu_io_mixed_tg | 487 ms                                                                 | 495 ms: 1.02x slower                                   |
| pycparser                  | 1.12 sec                                                               | 1.16 sec: 1.03x slower                                 |
| async_tree_none            | 274 ms                                                                 | 282 ms: 1.03x slower                                   |
| python_startup             | 14.7 ms                                                                | 15.3 ms: 1.04x slower                                  |
| bench_mp_pool              | 87.6 ms                                                                | 91.7 ms: 1.05x slower                                  |
| pidigits                   | 187 ms                                                                 | 197 ms: 1.05x slower                                   |
| async_tree_memoization     | 327 ms                                                                 | 345 ms: 1.05x slower                                   |
| async_tree_cpu_io_mixed    | 501 ms                                                                 | 529 ms: 1.06x slower                                   |
| dulwich_log                | 75.6 ms                                                                | 80.3 ms: 1.06x slower                                  |
| json                       | 5.06 ms                                                                | 5.38 ms: 1.06x slower                                  |
| generators                 | 28.7 ms                                                                | 30.6 ms: 1.07x slower                                  |
| mdp                        | 2.47 sec                                                               | 2.65 sec: 1.07x slower                                 |
| docutils                   | 2.56 sec                                                               | 2.75 sec: 1.08x slower                                 |
| regex_dna                  | 168 ms                                                                 | 182 ms: 1.09x slower                                   |
| scimark_sor                | 118 ms                                                                 | 128 ms: 1.09x slower                                   |
| json_dumps                 | 11.5 ms                                                                | 12.6 ms: 1.10x slower                                  |
| json_loads                 | 28.6 us                                                                | 31.4 us: 1.10x slower                                  |
| unpickle_pure_python       | 218 us                                                                 | 241 us: 1.11x slower                                   |
| bpe_tokeniser              | 4.16 sec                                                               | 4.61 sec: 1.11x slower                                 |
| pprint_safe_repr           | 699 ms                                                                 | 778 ms: 1.11x slower                                   |
| pylint                     | 277 ms                                                                 | 309 ms: 1.11x slower                                   |
| sphinx                     | 979 ms                                                                 | 1.09 sec: 1.12x slower                                 |
| async_generators           | 328 ms                                                                 | 368 ms: 1.12x slower                                   |
| many_optionals             | 1.02 ms                                                                | 1.15 ms: 1.12x slower                                  |
| pprint_pformat             | 1.42 sec                                                               | 1.61 sec: 1.13x slower                                 |
| spectral_norm              | 92.4 ms                                                                | 105 ms: 1.13x slower                                   |
| xml_etree_generate         | 83.7 ms                                                                | 94.9 ms: 1.13x slower                                  |
| k_core                     | 2.03 sec                                                               | 2.30 sec: 1.13x slower                                 |
| sqlglot_normalize          | 102 ms                                                                 | 116 ms: 1.14x slower                                   |
| pyflate                    | 417 ms                                                                 | 476 ms: 1.14x slower                                   |
| pickle_pure_python         | 312 us                                                                 | 356 us: 1.14x slower                                   |
| go                         | 117 ms                                                                 | 133 ms: 1.14x slower                                   |
| subparsers                 | 22.0 ms                                                                | 25.1 ms: 1.14x slower                                  |
| logging_simple             | 6.16 us                                                                | 7.02 us: 1.14x slower                                  |
| regex_compile              | 127 ms                                                                 | 145 ms: 1.14x slower                                   |
| logging_format             | 6.90 us                                                                | 7.96 us: 1.15x slower                                  |
| xml_etree_process          | 58.0 ms                                                                | 67.4 ms: 1.16x slower                                  |
| sqlglot_optimize           | 51.4 ms                                                                | 59.7 ms: 1.16x slower                                  |
| telco                      | 7.26 ms                                                                | 8.44 ms: 1.16x slower                                  |
| tomli_loads                | 1.94 sec                                                               | 2.26 sec: 1.16x slower                                 |
| scimark_fft                | 322 ms                                                                 | 375 ms: 1.17x slower                                   |
| 2to3                       | 253 ms                                                                 | 296 ms: 1.17x slower                                   |
| comprehensions             | 16.6 us                                                                | 19.4 us: 1.17x slower                                  |
| chaos                      | 57.1 ms                                                                | 66.8 ms: 1.17x slower                                  |
| raytrace                   | 270 ms                                                                 | 317 ms: 1.17x slower                                   |
| genshi_xml                 | 49.0 ms                                                                | 57.5 ms: 1.17x slower                                  |
| deepcopy_reduce            | 2.64 us                                                                | 3.10 us: 1.17x slower                                  |
| sqlglot_transpile          | 1.57 ms                                                                | 1.85 ms: 1.18x slower                                  |
| deepcopy                   | 254 us                                                                 | 300 us: 1.18x slower                                   |
| django_template            | 34.4 ms                                                                | 40.7 ms: 1.18x slower                                  |
| scimark_lu                 | 113 ms                                                                 | 134 ms: 1.18x slower                                   |
| nqueens                    | 78.9 ms                                                                | 93.8 ms: 1.19x slower                                  |
| sympy_expand               | 454 ms                                                                 | 541 ms: 1.19x slower                                   |
| sympy_sum                  | 153 ms                                                                 | 183 ms: 1.20x slower                                   |
| hexiom                     | 5.97 ms                                                                | 7.16 ms: 1.20x slower                                  |
| deepcopy_memo              | 30.7 us                                                                | 36.9 us: 1.20x slower                                  |
| sqlglot_parse              | 1.27 ms                                                                | 1.53 ms: 1.20x slower                                  |
| sympy_integrate            | 19.6 ms                                                                | 23.6 ms: 1.20x slower                                  |
| sqlalchemy_declarative     | 127 ms                                                                 | 154 ms: 1.21x slower                                   |
| sympy_str                  | 269 ms                                                                 | 327 ms: 1.21x slower                                   |
| sqlalchemy_imperative      | 19.4 ms                                                                | 23.8 ms: 1.23x slower                                  |
| coverage                   | 78.6 ms                                                                | 97.0 ms: 1.23x slower                                  |
| fannkuch                   | 387 ms                                                                 | 480 ms: 1.24x slower                                   |
| shortest_path              | 429 ms                                                                 | 535 ms: 1.25x slower                                   |
| connected_components       | 390 ms                                                                 | 487 ms: 1.25x slower                                   |
| thrift                     | 718 us                                                                 | 898 us: 1.25x slower                                   |
| scimark_monte_carlo        | 64.1 ms                                                                | 80.5 ms: 1.26x slower                                  |
| genshi_text                | 21.3 ms                                                                | 26.8 ms: 1.26x slower                                  |
| typing_runtime_protocols   | 152 us                                                                 | 193 us: 1.27x slower                                   |
| richards                   | 42.4 ms                                                                | 54.4 ms: 1.28x slower                                  |
| mako                       | 12.2 ms                                                                | 15.6 ms: 1.29x slower                                  |
| python_startup_no_site     | 7.46 ms                                                                | 9.61 ms: 1.29x slower                                  |
| scimark_sparse_mat_mult    | 4.25 ms                                                                | 5.53 ms: 1.30x slower                                  |
| crypto_pyaes               | 67.1 ms                                                                | 87.3 ms: 1.30x slower                                  |
| meteor_contest             | 98.9 ms                                                                | 129 ms: 1.31x slower                                   |
| richards_super             | 48.4 ms                                                                | 63.3 ms: 1.31x slower                                  |
| nbody                      | 92.2 ms                                                                | 126 ms: 1.36x slower                                   |
| deltablue                  | 3.18 ms                                                                | 4.57 ms: 1.44x slower                                  |
| bench_thread_pool          | 1.03 ms                                                                | 3.31 ms: 3.21x slower                                  |
| Geometric mean             | (ref)                                                                  | 1.13x slower                                           |

Benchmark hidden because not significant (3): logging_silent, asyncio_websockets, xml_etree_parse
Ignored benchmarks (1) of results/bm-20250131-3.14.0a4+-d89a5f6-NOGIL/bm-20250131-vultr-x86_64-python-main-3.14.0a4+-d89a5f6.json: html5lib

- Geometric mean (including insignificant results): 1.104x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.11x
- 95% likely to have a slowdown of 1.10x
- 99% likely to have a slowdown of 1.09x

# Memory
- memory change: 1.20x