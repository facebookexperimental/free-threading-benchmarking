# Results vs. 3.13.0rc2

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: c0d3c19
- commit date: 2024-12-04
- overall geometric mean: 1.249x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.19x slower
- Memory change: 1.31x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 260 ms                                                       | 367 ms: 1.41x slower                                                  |
| docutils       | 2.62 sec                                                     | 3.10 sec: 1.19x slower                                                |
| html5lib       | 67.0 ms                                                      | 98.6 ms: 1.47x slower                                                 |
| Geometric mean | (ref)                                                        | 1.35x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg           | 913 ms                                                       | 826 ms: 1.11x faster                                                  |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 639 ms: 1.04x faster                                                  |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 615 ms: 1.04x faster                                                  |
| async_tree_io              | 876 ms                                                       | 851 ms: 1.03x faster                                                  |
| coroutines                 | 23.6 ms                                                      | 25.1 ms: 1.06x slower                                                 |
| async_tree_none_tg         | 336 ms                                                       | 360 ms: 1.07x slower                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 450 ms: 1.09x slower                                                  |
| async_tree_none            | 354 ms                                                       | 388 ms: 1.10x slower                                                  |
| async_generators           | 377 ms                                                       | 459 ms: 1.22x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.03x slower                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 217 ms                                                       | 181 ms: 1.20x faster                                                  |
| nbody          | 85.1 ms                                                      | 127 ms: 1.50x slower                                                  |
| float          | 77.5 ms                                                      | 138 ms: 1.78x slower                                                  |
| Geometric mean | (ref)                                                        | 1.31x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.08 ms                                                      | 2.91 ms: 1.06x faster                                                 |
| regex_dna      | 180 ms                                                       | 188 ms: 1.04x slower                                                  |
| regex_v8       | 22.7 ms                                                      | 24.7 ms: 1.09x slower                                                 |
| regex_compile  | 132 ms                                                       | 179 ms: 1.35x slower                                                  |
| Geometric mean | (ref)                                                        | 1.10x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| xml_etree_iterparse  | 94.9 ms                                                      | 91.1 ms: 1.04x faster                                                 |
| xml_etree_parse      | 136 ms                                                       | 132 ms: 1.04x faster                                                  |
| json_loads           | 27.0 us                                                      | 28.4 us: 1.05x slower                                                 |
| xml_etree_generate   | 85.4 ms                                                      | 97.3 ms: 1.14x slower                                                 |
| xml_etree_process    | 59.3 ms                                                      | 77.3 ms: 1.30x slower                                                 |
| tomli_loads          | 2.01 sec                                                     | 2.66 sec: 1.32x slower                                                |
| json_dumps           | 10.5 ms                                                      | 14.3 ms: 1.36x slower                                                 |
| unpickle_pure_python | 210 us                                                       | 337 us: 1.60x slower                                                  |
| pickle_pure_python   | 294 us                                                       | 506 us: 1.72x slower                                                  |
| Geometric mean       | (ref)                                                        | 1.24x slower                                                          |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                 |
| python_startup         | 11.0 ms                                                      | 17.4 ms: 1.59x slower                                                 |
| Geometric mean         | (ref)                                                        | 1.48x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|-----------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 48.8 ms                                                      | 63.8 ms: 1.31x slower                                                 |
| genshi_text     | 21.5 ms                                                      | 32.0 ms: 1.49x slower                                                 |
| django_template | 34.1 ms                                                      | 51.6 ms: 1.51x slower                                                 |
| mako            | 11.3 ms                                                      | 17.7 ms: 1.56x slower                                                 |
| Geometric mean  | (ref)                                                        | 1.46x slower                                                          |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006 | bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19 |
|----------------------------|:------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits                   | 217 ms                                                       | 181 ms: 1.20x faster                                                  |
| async_tree_io_tg           | 913 ms                                                       | 826 ms: 1.11x faster                                                  |
| deepcopy                   | 355 us                                                       | 327 us: 1.09x faster                                                  |
| regex_effbot               | 3.08 ms                                                      | 2.91 ms: 1.06x faster                                                 |
| async_tree_cpu_io_mixed    | 666 ms                                                       | 639 ms: 1.04x faster                                                  |
| xml_etree_iterparse        | 94.9 ms                                                      | 91.1 ms: 1.04x faster                                                 |
| async_tree_cpu_io_mixed_tg | 638 ms                                                       | 615 ms: 1.04x faster                                                  |
| xml_etree_parse            | 136 ms                                                       | 132 ms: 1.04x faster                                                  |
| async_tree_io              | 876 ms                                                       | 851 ms: 1.03x faster                                                  |
| gc_traversal               | 3.14 ms                                                      | 3.19 ms: 1.01x slower                                                 |
| json                       | 4.93 ms                                                      | 5.08 ms: 1.03x slower                                                 |
| deepcopy_memo              | 39.1 us                                                      | 40.5 us: 1.04x slower                                                 |
| regex_dna                  | 180 ms                                                       | 188 ms: 1.04x slower                                                  |
| sqlite_synth               | 2.21 us                                                      | 2.31 us: 1.05x slower                                                 |
| json_loads                 | 27.0 us                                                      | 28.4 us: 1.05x slower                                                 |
| pathlib                    | 19.2 ms                                                      | 20.2 ms: 1.05x slower                                                 |
| coroutines                 | 23.6 ms                                                      | 25.1 ms: 1.06x slower                                                 |
| async_tree_none_tg         | 336 ms                                                       | 360 ms: 1.07x slower                                                  |
| spectral_norm              | 111 ms                                                       | 120 ms: 1.08x slower                                                  |
| async_tree_memoization_tg  | 414 ms                                                       | 450 ms: 1.09x slower                                                  |
| regex_v8                   | 22.7 ms                                                      | 24.7 ms: 1.09x slower                                                 |
| async_tree_none            | 354 ms                                                       | 388 ms: 1.10x slower                                                  |
| telco                      | 7.82 ms                                                      | 8.64 ms: 1.10x slower                                                 |
| bpe_tokeniser              | 4.45 sec                                                     | 4.97 sec: 1.12x slower                                                |
| deepcopy_reduce            | 3.11 us                                                      | 3.48 us: 1.12x slower                                                 |
| scimark_fft                | 349 ms                                                       | 397 ms: 1.14x slower                                                  |
| xml_etree_generate         | 85.4 ms                                                      | 97.3 ms: 1.14x slower                                                 |
| docutils                   | 2.62 sec                                                     | 3.10 sec: 1.19x slower                                                |
| pylint                     | 317 ms                                                       | 383 ms: 1.21x slower                                                  |
| coverage                   | 83.0 ms                                                      | 101 ms: 1.21x slower                                                  |
| async_generators           | 377 ms                                                       | 459 ms: 1.22x slower                                                  |
| mdp                        | 2.36 sec                                                     | 2.88 sec: 1.22x slower                                                |
| scimark_sparse_mat_mult    | 4.71 ms                                                      | 5.84 ms: 1.24x slower                                                 |
| nqueens                    | 78.6 ms                                                      | 98.4 ms: 1.25x slower                                                 |
| meteor_contest             | 102 ms                                                       | 130 ms: 1.28x slower                                                  |
| dulwich_log                | 74.8 ms                                                      | 96.1 ms: 1.29x slower                                                 |
| xml_etree_process          | 59.3 ms                                                      | 77.3 ms: 1.30x slower                                                 |
| pprint_safe_repr           | 738 ms                                                       | 961 ms: 1.30x slower                                                  |
| sqlglot_normalize          | 106 ms                                                       | 138 ms: 1.30x slower                                                  |
| genshi_xml                 | 48.8 ms                                                      | 63.8 ms: 1.31x slower                                                 |
| sqlglot_optimize           | 52.7 ms                                                      | 69.3 ms: 1.31x slower                                                 |
| typing_runtime_protocols   | 155 us                                                       | 204 us: 1.32x slower                                                  |
| fannkuch                   | 370 ms                                                       | 489 ms: 1.32x slower                                                  |
| tomli_loads                | 2.01 sec                                                     | 2.66 sec: 1.32x slower                                                |
| pprint_pformat             | 1.50 sec                                                     | 2.00 sec: 1.33x slower                                                |
| regex_compile              | 132 ms                                                       | 179 ms: 1.35x slower                                                  |
| generators                 | 28.8 ms                                                      | 39.0 ms: 1.35x slower                                                 |
| crypto_pyaes               | 67.9 ms                                                      | 91.9 ms: 1.35x slower                                                 |
| create_gc_cycles           | 1.34 ms                                                      | 1.81 ms: 1.36x slower                                                 |
| json_dumps                 | 10.5 ms                                                      | 14.3 ms: 1.36x slower                                                 |
| pycparser                  | 1.12 sec                                                     | 1.55 sec: 1.38x slower                                                |
| python_startup_no_site     | 7.39 ms                                                      | 10.3 ms: 1.39x slower                                                 |
| 2to3                       | 260 ms                                                       | 367 ms: 1.41x slower                                                  |
| html5lib                   | 67.0 ms                                                      | 98.6 ms: 1.47x slower                                                 |
| sympy_integrate            | 19.8 ms                                                      | 29.5 ms: 1.49x slower                                                 |
| genshi_text                | 21.5 ms                                                      | 32.0 ms: 1.49x slower                                                 |
| thrift                     | 778 us                                                       | 1.16 ms: 1.49x slower                                                 |
| nbody                      | 85.1 ms                                                      | 127 ms: 1.50x slower                                                  |
| django_template            | 34.1 ms                                                      | 51.6 ms: 1.51x slower                                                 |
| pyflate                    | 449 ms                                                       | 684 ms: 1.52x slower                                                  |
| mako                       | 11.3 ms                                                      | 17.7 ms: 1.56x slower                                                 |
| python_startup             | 11.0 ms                                                      | 17.4 ms: 1.59x slower                                                 |
| unpickle_pure_python       | 210 us                                                       | 337 us: 1.60x slower                                                  |
| scimark_lu                 | 113 ms                                                       | 185 ms: 1.64x slower                                                  |
| hexiom                     | 5.99 ms                                                      | 9.92 ms: 1.66x slower                                                 |
| comprehensions             | 16.5 us                                                      | 27.4 us: 1.67x slower                                                 |
| richards_super             | 51.6 ms                                                      | 87.2 ms: 1.69x slower                                                 |
| pickle_pure_python         | 294 us                                                       | 506 us: 1.72x slower                                                  |
| logging_format             | 6.84 us                                                      | 11.8 us: 1.72x slower                                                 |
| richards                   | 45.2 ms                                                      | 77.9 ms: 1.72x slower                                                 |
| sympy_str                  | 275 ms                                                       | 475 ms: 1.73x slower                                                  |
| logging_simple             | 6.16 us                                                      | 10.8 us: 1.76x slower                                                 |
| scimark_sor                | 134 ms                                                       | 237 ms: 1.76x slower                                                  |
| float                      | 77.5 ms                                                      | 138 ms: 1.78x slower                                                  |
| scimark_monte_carlo        | 65.4 ms                                                      | 118 ms: 1.80x slower                                                  |
| logging_silent             | 103 ns                                                       | 187 ns: 1.82x slower                                                  |
| chaos                      | 57.3 ms                                                      | 105 ms: 1.83x slower                                                  |
| sqlglot_transpile          | 1.56 ms                                                      | 2.96 ms: 1.90x slower                                                 |
| go                         | 141 ms                                                       | 270 ms: 1.92x slower                                                  |
| sqlglot_parse              | 1.25 ms                                                      | 2.56 ms: 2.05x slower                                                 |
| sympy_expand               | 457 ms                                                       | 952 ms: 2.08x slower                                                  |
| raytrace                   | 253 ms                                                       | 557 ms: 2.20x slower                                                  |
| sympy_sum                  | 156 ms                                                       | 349 ms: 2.24x slower                                                  |
| deltablue                  | 3.12 ms                                                      | 8.05 ms: 2.58x slower                                                 |
| bench_thread_pool          | 919 us                                                       | 3.37 ms: 3.66x slower                                                 |
| bench_mp_pool              | 11.0 ms                                                      | 109 ms: 9.89x slower                                                  |
| Geometric mean             | (ref)                                                        | 1.38x slower                                                          |

Benchmark hidden because not significant (2): asyncio_websockets, async_tree_memoization
Ignored benchmarks (14) of results/bm-20240906-3.13.0rc2-ec61006/bm-20240906-vultr-x86_64-python-v3.13.0rc2-3.13.0rc2-ec61006.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (8) of results/bm-20241204-3.14.0a2+-c0d3c19-NOGIL/bm-20241204-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a2+-c0d3c19.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlalchemy_declarative, sqlalchemy_imperative, subparsers

- Geometric mean (including insignificant results): 1.249x slower

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.24x
- 95% likely to have a slowdown of 1.22x
- 99% likely to have a slowdown of 1.19x

# Memory
- memory change: 1.31x