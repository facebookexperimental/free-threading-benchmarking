# Results vs. base

- fork: mpage
- ref: aa_test_2
- machine: linux-x86_64
- commit hash: f1b75b3
- commit date: 2025-01-16
- overall geometric mean: 1.013x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.00x slower
- Memory change: 0.99x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4+-3893a92 | bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4+-f1b75b3 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| 2to3           | 253 ms                                                                 | 256 ms: 1.01x slower                                       |
| docutils       | 2.56 sec                                                               | 2.58 sec: 1.01x slower                                     |
| Geometric mean | (ref)                                                                  | 1.01x slower                                               |

Benchmark hidden because not significant (1): sphinx

Benchmarks with tag 'asyncio':
==============================

| Benchmark                 | bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4+-3893a92 | bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4+-f1b75b3 |
|---------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| async_tree_memoization_tg | 300 ms                                                                 | 304 ms: 1.01x slower                                       |
| async_tree_none_tg        | 254 ms                                                                 | 257 ms: 1.01x slower                                       |
| async_generators          | 316 ms                                                                 | 326 ms: 1.03x slower                                       |
| coroutines                | 21.1 ms                                                                | 22.0 ms: 1.04x slower                                      |
| Geometric mean            | (ref)                                                                  | 1.01x slower                                               |

Benchmark hidden because not significant (7): async_tree_io, asyncio_websockets, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, async_tree_none, async_tree_io_tg, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4+-3893a92 | bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4+-f1b75b3 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| pidigits       | 200 ms                                                                 | 196 ms: 1.02x faster                                       |
| nbody          | 87.9 ms                                                                | 90.1 ms: 1.03x slower                                      |
| float          | 70.5 ms                                                                | 72.7 ms: 1.03x slower                                      |
| Geometric mean | (ref)                                                                  | 1.01x slower                                               |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4+-3893a92 | bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4+-f1b75b3 |
|----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| regex_effbot   | 2.81 ms                                                                | 2.70 ms: 1.04x faster                                      |
| regex_v8       | 24.1 ms                                                                | 23.3 ms: 1.03x faster                                      |
| regex_compile  | 126 ms                                                                 | 128 ms: 1.01x slower                                       |
| regex_dna      | 170 ms                                                                 | 174 ms: 1.02x slower                                       |
| Geometric mean | (ref)                                                                  | 1.01x faster                                               |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4+-3893a92 | bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4+-f1b75b3 |
|----------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| xml_etree_parse      | 129 ms                                                                 | 128 ms: 1.00x faster                                       |
| xml_etree_iterparse  | 90.4 ms                                                                | 91.5 ms: 1.01x slower                                      |
| json_dumps           | 11.4 ms                                                                | 11.5 ms: 1.01x slower                                      |
| unpickle_pure_python | 212 us                                                                 | 215 us: 1.01x slower                                       |
| json_loads           | 27.4 us                                                                | 28.0 us: 1.02x slower                                      |
| tomli_loads          | 1.89 sec                                                               | 1.93 sec: 1.02x slower                                     |
| xml_etree_generate   | 82.9 ms                                                                | 85.0 ms: 1.03x slower                                      |
| xml_etree_process    | 58.1 ms                                                                | 59.7 ms: 1.03x slower                                      |
| pickle_pure_python   | 311 us                                                                 | 321 us: 1.03x slower                                       |
| Geometric mean       | (ref)                                                                  | 1.02x slower                                               |

Benchmarks with tag 'startup':
==============================

Benchmark hidden because not significant (2): python_startup_no_site, python_startup

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4+-3893a92 | bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4+-f1b75b3 |
|-----------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| django_template | 35.2 ms                                                                | 35.9 ms: 1.02x slower                                      |
| genshi_xml      | 48.2 ms                                                                | 49.4 ms: 1.02x slower                                      |
| mako            | 11.6 ms                                                                | 12.0 ms: 1.04x slower                                      |
| genshi_text     | 20.6 ms                                                                | 21.5 ms: 1.04x slower                                      |
| Geometric mean  | (ref)                                                                  | 1.03x slower                                               |

All benchmarks:
===============

| Benchmark                 | bm-20250116-vultr-x86_64-python-3893a92d956363fa2443-3.14.0a4+-3893a92 | bm-20250116-vultr-x86_64-mpage-aa_test_2-3.14.0a4+-f1b75b3 |
|---------------------------|:----------------------------------------------------------------------:|:----------------------------------------------------------:|
| mdp                       | 2.45 sec                                                               | 2.32 sec: 1.05x faster                                     |
| regex_effbot              | 2.81 ms                                                                | 2.70 ms: 1.04x faster                                      |
| regex_v8                  | 24.1 ms                                                                | 23.3 ms: 1.03x faster                                      |
| pidigits                  | 200 ms                                                                 | 196 ms: 1.02x faster                                       |
| telco                     | 7.27 ms                                                                | 7.17 ms: 1.01x faster                                      |
| comprehensions            | 16.9 us                                                                | 16.7 us: 1.01x faster                                      |
| pycparser                 | 1.12 sec                                                               | 1.11 sec: 1.00x faster                                     |
| xml_etree_parse           | 129 ms                                                                 | 128 ms: 1.00x faster                                       |
| scimark_fft               | 311 ms                                                                 | 312 ms: 1.00x slower                                       |
| many_optionals            | 1.03 ms                                                                | 1.03 ms: 1.00x slower                                      |
| sympy_sum                 | 153 ms                                                                 | 154 ms: 1.01x slower                                       |
| sympy_str                 | 272 ms                                                                 | 274 ms: 1.01x slower                                       |
| bench_thread_pool         | 1.04 ms                                                                | 1.04 ms: 1.01x slower                                      |
| dulwich_log               | 75.8 ms                                                                | 76.3 ms: 1.01x slower                                      |
| sqlalchemy_declarative    | 128 ms                                                                 | 129 ms: 1.01x slower                                       |
| scimark_lu                | 110 ms                                                                 | 111 ms: 1.01x slower                                       |
| create_gc_cycles          | 1.84 ms                                                                | 1.85 ms: 1.01x slower                                      |
| docutils                  | 2.56 sec                                                               | 2.58 sec: 1.01x slower                                     |
| meteor_contest            | 99.0 ms                                                                | 99.9 ms: 1.01x slower                                      |
| sqlglot_optimize          | 52.0 ms                                                                | 52.4 ms: 1.01x slower                                      |
| typing_runtime_protocols  | 155 us                                                                 | 156 us: 1.01x slower                                       |
| pyflate                   | 416 ms                                                                 | 420 ms: 1.01x slower                                       |
| shortest_path             | 428 ms                                                                 | 432 ms: 1.01x slower                                       |
| coverage                  | 78.4 ms                                                                | 79.3 ms: 1.01x slower                                      |
| xml_etree_iterparse       | 90.4 ms                                                                | 91.5 ms: 1.01x slower                                      |
| sqlalchemy_imperative     | 19.3 ms                                                                | 19.6 ms: 1.01x slower                                      |
| json_dumps                | 11.4 ms                                                                | 11.5 ms: 1.01x slower                                      |
| bpe_tokeniser             | 4.16 sec                                                               | 4.21 sec: 1.01x slower                                     |
| k_core                    | 2.04 sec                                                               | 2.06 sec: 1.01x slower                                     |
| unpickle_pure_python      | 212 us                                                                 | 215 us: 1.01x slower                                       |
| 2to3                      | 253 ms                                                                 | 256 ms: 1.01x slower                                       |
| crypto_pyaes              | 66.3 ms                                                                | 67.1 ms: 1.01x slower                                      |
| sympy_integrate           | 19.7 ms                                                                | 20.0 ms: 1.01x slower                                      |
| async_tree_memoization_tg | 300 ms                                                                 | 304 ms: 1.01x slower                                       |
| async_tree_none_tg        | 254 ms                                                                 | 257 ms: 1.01x slower                                       |
| regex_compile             | 126 ms                                                                 | 128 ms: 1.01x slower                                       |
| sqlglot_transpile         | 1.54 ms                                                                | 1.57 ms: 1.02x slower                                      |
| nqueens                   | 77.5 ms                                                                | 78.7 ms: 1.02x slower                                      |
| deltablue                 | 3.13 ms                                                                | 3.18 ms: 1.02x slower                                      |
| sqlglot_parse             | 1.24 ms                                                                | 1.26 ms: 1.02x slower                                      |
| connected_components      | 387 ms                                                                 | 394 ms: 1.02x slower                                       |
| richards_super            | 48.2 ms                                                                | 49.1 ms: 1.02x slower                                      |
| hexiom                    | 5.71 ms                                                                | 5.81 ms: 1.02x slower                                      |
| django_template           | 35.2 ms                                                                | 35.9 ms: 1.02x slower                                      |
| raytrace                  | 262 ms                                                                 | 267 ms: 1.02x slower                                       |
| spectral_norm             | 89.3 ms                                                                | 91.1 ms: 1.02x slower                                      |
| richards                  | 42.2 ms                                                                | 43.0 ms: 1.02x slower                                      |
| json_loads                | 27.4 us                                                                | 28.0 us: 1.02x slower                                      |
| tomli_loads               | 1.89 sec                                                               | 1.93 sec: 1.02x slower                                     |
| scimark_sor               | 114 ms                                                                 | 116 ms: 1.02x slower                                       |
| regex_dna                 | 170 ms                                                                 | 174 ms: 1.02x slower                                       |
| genshi_xml                | 48.2 ms                                                                | 49.4 ms: 1.02x slower                                      |
| deepcopy_reduce           | 2.59 us                                                                | 2.65 us: 1.02x slower                                      |
| json                      | 4.92 ms                                                                | 5.04 ms: 1.02x slower                                      |
| nbody                     | 87.9 ms                                                                | 90.1 ms: 1.03x slower                                      |
| xml_etree_generate        | 82.9 ms                                                                | 85.0 ms: 1.03x slower                                      |
| xml_etree_process         | 58.1 ms                                                                | 59.7 ms: 1.03x slower                                      |
| deepcopy                  | 255 us                                                                 | 262 us: 1.03x slower                                       |
| pprint_pformat            | 1.41 sec                                                               | 1.45 sec: 1.03x slower                                     |
| async_generators          | 316 ms                                                                 | 326 ms: 1.03x slower                                       |
| sqlglot_normalize         | 102 ms                                                                 | 105 ms: 1.03x slower                                       |
| pprint_safe_repr          | 691 ms                                                                 | 712 ms: 1.03x slower                                       |
| pickle_pure_python        | 311 us                                                                 | 321 us: 1.03x slower                                       |
| go                        | 113 ms                                                                 | 117 ms: 1.03x slower                                       |
| float                     | 70.5 ms                                                                | 72.7 ms: 1.03x slower                                      |
| mako                      | 11.6 ms                                                                | 12.0 ms: 1.04x slower                                      |
| generators                | 27.0 ms                                                                | 28.1 ms: 1.04x slower                                      |
| coroutines                | 21.1 ms                                                                | 22.0 ms: 1.04x slower                                      |
| genshi_text               | 20.6 ms                                                                | 21.5 ms: 1.04x slower                                      |
| chaos                     | 54.2 ms                                                                | 56.7 ms: 1.05x slower                                      |
| logging_silent            | 102 ns                                                                 | 107 ns: 1.05x slower                                       |
| scimark_monte_carlo       | 61.9 ms                                                                | 64.8 ms: 1.05x slower                                      |
| scimark_sparse_mat_mult   | 4.16 ms                                                                | 4.35 ms: 1.05x slower                                      |
| fannkuch                  | 358 ms                                                                 | 377 ms: 1.05x slower                                       |
| deepcopy_memo             | 29.5 us                                                                | 31.2 us: 1.06x slower                                      |
| gc_traversal              | 4.28 ms                                                                | 4.78 ms: 1.12x slower                                      |
| Geometric mean            | (ref)                                                                  | 1.01x slower                                               |

Benchmark hidden because not significant (19): async_tree_io, sqlite_synth, bench_mp_pool, subparsers, asyncio_websockets, sympy_expand, python_startup_no_site, python_startup, logging_format, pathlib, thrift, async_tree_cpu_io_mixed_tg, async_tree_cpu_io_mixed, logging_simple, pylint, sphinx, async_tree_none, async_tree_io_tg, async_tree_memoization

- Geometric mean (including insignificant results): 1.013x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.00x
- 95% likely to have a slowdown of 1.00x
- 99% likely to have a slowdown of 1.00x

# Memory
- memory change: 0.99x