# Results vs. 3.12.6

- fork: tom-pytel
- ref: 579bd08e9f4db18fbbe0
- machine: linux-x86_64
- commit hash: 579bd08
- commit date: 2025-03-30
- overall geometric mean: 1.062x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.02x faster
- Memory change: 1.12x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 257 ms: 1.03x faster                                                        |
| docutils       | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                      |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                        |
| async_tree_memoization     | 555 ms                                                 | 320 ms: 1.73x faster                                                        |
| async_tree_none_tg         | 446 ms                                                 | 259 ms: 1.72x faster                                                        |
| async_tree_io_tg           | 1.11 sec                                               | 646 ms: 1.72x faster                                                        |
| async_tree_io              | 1.08 sec                                               | 632 ms: 1.71x faster                                                        |
| async_tree_none            | 464 ms                                                 | 277 ms: 1.67x faster                                                        |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 492 ms: 1.47x faster                                                        |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 511 ms: 1.40x faster                                                        |
| async_generators           | 384 ms                                                 | 337 ms: 1.14x faster                                                        |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.01x faster                                                       |
| Geometric mean             | (ref)                                                  | 1.46x faster                                                                |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 75.0 ms: 1.08x faster                                                       |
| nbody          | 89.3 ms                                                | 102 ms: 1.14x slower                                                        |
| pidigits       | 184 ms                                                 | 227 ms: 1.23x slower                                                        |
| Geometric mean | (ref)                                                  | 1.09x slower                                                                |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                       |
| regex_compile  | 142 ms                                                 | 129 ms: 1.11x faster                                                        |
| regex_dna      | 168 ms                                                 | 181 ms: 1.08x slower                                                        |
| regex_v8       | 20.6 ms                                                | 22.4 ms: 1.09x slower                                                       |
| Geometric mean | (ref)                                                  | 1.02x faster                                                                |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 130 ms: 1.06x faster                                                        |
| tomli_loads          | 2.11 sec                                               | 2.02 sec: 1.04x faster                                                      |
| xml_etree_iterparse  | 96.7 ms                                                | 93.4 ms: 1.04x faster                                                       |
| xml_etree_generate   | 85.2 ms                                                | 84.7 ms: 1.01x faster                                                       |
| unpickle_pure_python | 221 us                                                 | 224 us: 1.01x slower                                                        |
| json_loads           | 26.5 us                                                | 27.0 us: 1.02x slower                                                       |
| xml_etree_process    | 59.0 ms                                                | 60.1 ms: 1.02x slower                                                       |
| pickle_pure_python   | 308 us                                                 | 321 us: 1.04x slower                                                        |
| json_dumps           | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                       |
| Geometric mean       | (ref)                                                  | 1.00x slower                                                                |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 8.62 ms: 1.20x slower                                                       |
| python_startup         | 9.93 ms                                                | 14.9 ms: 1.50x slower                                                       |
| Geometric mean         | (ref)                                                  | 1.35x slower                                                                |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|-----------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.5 ms: 1.01x faster                                                       |
| genshi_xml      | 50.2 ms                                                | 50.5 ms: 1.01x slower                                                       |
| django_template | 34.7 ms                                                | 35.8 ms: 1.03x slower                                                       |
| mako            | 11.0 ms                                                | 12.3 ms: 1.12x slower                                                       |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                                |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08 |
|----------------------------|:------------------------------------------------------:|:---------------------------------------------------------------------------:|
| async_tree_memoization_tg  | 560 ms                                                 | 311 ms: 1.80x faster                                                        |
| async_tree_memoization     | 555 ms                                                 | 320 ms: 1.73x faster                                                        |
| async_tree_none_tg         | 446 ms                                                 | 259 ms: 1.72x faster                                                        |
| async_tree_io_tg           | 1.11 sec                                               | 646 ms: 1.72x faster                                                        |
| async_tree_io              | 1.08 sec                                               | 632 ms: 1.71x faster                                                        |
| async_tree_none            | 464 ms                                                 | 277 ms: 1.67x faster                                                        |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 492 ms: 1.47x faster                                                        |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 511 ms: 1.40x faster                                                        |
| deepcopy                   | 352 us                                                 | 263 us: 1.34x faster                                                        |
| deepcopy_memo              | 40.3 us                                                | 30.6 us: 1.32x faster                                                       |
| go                         | 139 ms                                                 | 116 ms: 1.20x faster                                                        |
| dulwich_log                | 78.9 ms                                                | 67.1 ms: 1.18x faster                                                       |
| comprehensions             | 19.8 us                                                | 17.1 us: 1.16x faster                                                       |
| deepcopy_reduce            | 3.08 us                                                | 2.70 us: 1.14x faster                                                       |
| async_generators           | 384 ms                                                 | 337 ms: 1.14x faster                                                        |
| spectral_norm              | 110 ms                                                 | 97.2 ms: 1.13x faster                                                       |
| regex_effbot               | 3.17 ms                                                | 2.80 ms: 1.13x faster                                                       |
| pylint                     | 319 ms                                                 | 282 ms: 1.13x faster                                                        |
| scimark_sor                | 130 ms                                                 | 116 ms: 1.12x faster                                                        |
| raytrace                   | 299 ms                                                 | 269 ms: 1.11x faster                                                        |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.6 ms: 1.11x faster                                                       |
| logging_format             | 7.35 us                                                | 6.63 us: 1.11x faster                                                       |
| pathlib                    | 21.5 ms                                                | 19.4 ms: 1.11x faster                                                       |
| regex_compile              | 142 ms                                                 | 129 ms: 1.11x faster                                                        |
| sqlalchemy_declarative     | 143 ms                                                 | 131 ms: 1.09x faster                                                        |
| logging_simple             | 6.63 us                                                | 6.07 us: 1.09x faster                                                       |
| logging_silent             | 109 ns                                                 | 99.9 ns: 1.09x faster                                                       |
| generators                 | 32.2 ms                                                | 29.7 ms: 1.09x faster                                                       |
| deltablue                  | 3.45 ms                                                | 3.17 ms: 1.09x faster                                                       |
| float                      | 80.8 ms                                                | 75.0 ms: 1.08x faster                                                       |
| richards                   | 45.9 ms                                                | 42.7 ms: 1.08x faster                                                       |
| chaos                      | 62.8 ms                                                | 58.6 ms: 1.07x faster                                                       |
| bpe_tokeniser              | 4.74 sec                                               | 4.44 sec: 1.07x faster                                                      |
| sympy_sum                  | 166 ms                                                 | 156 ms: 1.07x faster                                                        |
| xml_etree_parse            | 139 ms                                                 | 130 ms: 1.06x faster                                                        |
| crypto_pyaes               | 76.6 ms                                                | 72.4 ms: 1.06x faster                                                       |
| pyflate                    | 448 ms                                                 | 424 ms: 1.06x faster                                                        |
| richards_super             | 51.9 ms                                                | 49.1 ms: 1.06x faster                                                       |
| sympy_str                  | 292 ms                                                 | 277 ms: 1.05x faster                                                        |
| sympy_integrate            | 20.5 ms                                                | 19.6 ms: 1.05x faster                                                       |
| tomli_loads                | 2.11 sec                                               | 2.02 sec: 1.04x faster                                                      |
| mdp                        | 2.42 sec                                               | 2.32 sec: 1.04x faster                                                      |
| xml_etree_iterparse        | 96.7 ms                                                | 93.4 ms: 1.04x faster                                                       |
| typing_runtime_protocols   | 163 us                                                 | 158 us: 1.03x faster                                                        |
| json                       | 5.02 ms                                                | 4.86 ms: 1.03x faster                                                       |
| pycparser                  | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                      |
| scimark_monte_carlo        | 68.4 ms                                                | 66.5 ms: 1.03x faster                                                       |
| 2to3                       | 264 ms                                                 | 257 ms: 1.03x faster                                                        |
| docutils                   | 2.64 sec                                               | 2.58 sec: 1.02x faster                                                      |
| thrift                     | 791 us                                                 | 774 us: 1.02x faster                                                        |
| pprint_pformat             | 1.52 sec                                               | 1.50 sec: 1.01x faster                                                      |
| coroutines                 | 23.9 ms                                                | 23.6 ms: 1.01x faster                                                       |
| genshi_text                | 22.8 ms                                                | 22.5 ms: 1.01x faster                                                       |
| meteor_contest             | 104 ms                                                 | 102 ms: 1.01x faster                                                        |
| hexiom                     | 6.17 ms                                                | 6.10 ms: 1.01x faster                                                       |
| pprint_safe_repr           | 743 ms                                                 | 736 ms: 1.01x faster                                                        |
| sympy_expand               | 468 ms                                                 | 465 ms: 1.01x faster                                                        |
| xml_etree_generate         | 85.2 ms                                                | 84.7 ms: 1.01x faster                                                       |
| scimark_fft                | 342 ms                                                 | 340 ms: 1.00x faster                                                        |
| genshi_xml                 | 50.2 ms                                                | 50.5 ms: 1.01x slower                                                       |
| sqlite_synth               | 2.20 us                                                | 2.23 us: 1.01x slower                                                       |
| unpickle_pure_python       | 221 us                                                 | 224 us: 1.01x slower                                                        |
| json_loads                 | 26.5 us                                                | 27.0 us: 1.02x slower                                                       |
| xml_etree_process          | 59.0 ms                                                | 60.1 ms: 1.02x slower                                                       |
| nqueens                    | 80.1 ms                                                | 81.9 ms: 1.02x slower                                                       |
| scimark_lu                 | 114 ms                                                 | 117 ms: 1.03x slower                                                        |
| django_template            | 34.7 ms                                                | 35.8 ms: 1.03x slower                                                       |
| pickle_pure_python         | 308 us                                                 | 321 us: 1.04x slower                                                        |
| regex_dna                  | 168 ms                                                 | 181 ms: 1.08x slower                                                        |
| json_dumps                 | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                       |
| regex_v8                   | 20.6 ms                                                | 22.4 ms: 1.09x slower                                                       |
| fannkuch                   | 372 ms                                                 | 408 ms: 1.10x slower                                                        |
| mako                       | 11.0 ms                                                | 12.3 ms: 1.12x slower                                                       |
| bench_thread_pool          | 941 us                                                 | 1.05 ms: 1.12x slower                                                       |
| coverage                   | 71.4 ms                                                | 80.5 ms: 1.13x slower                                                       |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.97 ms: 1.13x slower                                                       |
| telco                      | 6.53 ms                                                | 7.42 ms: 1.14x slower                                                       |
| nbody                      | 89.3 ms                                                | 102 ms: 1.14x slower                                                        |
| python_startup_no_site     | 7.16 ms                                                | 8.62 ms: 1.20x slower                                                       |
| pidigits                   | 184 ms                                                 | 227 ms: 1.23x slower                                                        |
| gc_traversal               | 3.46 ms                                                | 4.64 ms: 1.34x slower                                                       |
| python_startup             | 9.93 ms                                                | 14.9 ms: 1.50x slower                                                       |
| create_gc_cycles           | 1.09 ms                                                | 1.87 ms: 1.71x slower                                                       |
| bench_mp_pool              | 10.8 ms                                                | 89.6 ms: 8.30x slower                                                       |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                                |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (20) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, sqlglot_normalize, sqlglot_optimize, sqlglot_parse, sqlglot_transpile, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (10) of results/bm-20250330-3.14.0a6+-579bd08/bm-20250330-vultr-x86_64-tom%2dpytel-579bd08e9f4db18fbbe0-3.14.0a6+-579bd08.json: connected_components, k_core, many_optionals, shortest_path, sphinx, sqlglot_v2_normalize, sqlglot_v2_optimize, sqlglot_v2_parse, sqlglot_v2_transpile, subparsers

- Geometric mean (including insignificant results): 1.062x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.03x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.02x

# Memory
- memory change: 1.12x