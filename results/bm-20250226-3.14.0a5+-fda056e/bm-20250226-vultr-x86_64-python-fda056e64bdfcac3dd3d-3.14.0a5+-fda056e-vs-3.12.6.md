# Results vs. 3.12.6

- fork: python
- ref: fda056e64bdfcac3dd3d
- machine: linux-x86_64
- commit hash: fda056e
- commit date: 2025-02-26
- overall geometric mean: 1.099x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 250 ms: 1.05x faster                                                   |
| docutils       | 2.64 sec                                               | 2.53 sec: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.05x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 600 ms: 1.85x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 599 ms: 1.81x faster                                                   |
| async_tree_none            | 464 ms                                                 | 259 ms: 1.80x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.78x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.76x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 478 ms: 1.51x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 487 ms: 1.47x faster                                                   |
| async_generators           | 384 ms                                                 | 316 ms: 1.22x faster                                                   |
| coroutines                 | 23.9 ms                                                | 21.3 ms: 1.12x faster                                                  |
| asyncio_websockets         | 517 ms                                                 | 516 ms: 1.00x faster                                                   |
| Geometric mean             | (ref)                                                  | 1.53x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.4 ms: 1.15x faster                                                  |
| nbody          | 89.3 ms                                                | 84.1 ms: 1.06x faster                                                  |
| pidigits       | 184 ms                                                 | 212 ms: 1.15x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.73 ms: 1.16x faster                                                  |
| regex_compile  | 142 ms                                                 | 124 ms: 1.15x faster                                                   |
| regex_dna      | 168 ms                                                 | 173 ms: 1.03x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.8 ms: 1.20x slower                                                  |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.85 sec: 1.14x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.09x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 89.7 ms: 1.08x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 208 us: 1.06x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 81.5 ms: 1.05x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 56.8 ms: 1.04x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 304 us: 1.01x faster                                                   |
| json_dumps           | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                  |
| json_loads           | 26.5 us                                                | 28.6 us: 1.08x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.54 ms: 1.05x slower                                                  |
| python_startup         | 9.93 ms                                                | 14.8 ms: 1.49x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.25x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.3 ms: 1.12x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 47.1 ms: 1.06x faster                                                  |
| django_template | 34.7 ms                                                | 32.8 ms: 1.06x faster                                                  |
| mako            | 11.0 ms                                                | 11.5 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.05x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 600 ms: 1.85x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 307 ms: 1.82x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 599 ms: 1.81x faster                                                   |
| async_tree_none            | 464 ms                                                 | 259 ms: 1.80x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 311 ms: 1.78x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 254 ms: 1.76x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 478 ms: 1.51x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 487 ms: 1.47x faster                                                   |
| deepcopy                   | 352 us                                                 | 244 us: 1.44x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 28.7 us: 1.41x faster                                                  |
| spectral_norm              | 110 ms                                                 | 86.6 ms: 1.27x faster                                                  |
| go                         | 139 ms                                                 | 111 ms: 1.26x faster                                                   |
| comprehensions             | 19.8 us                                                | 16.0 us: 1.24x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.52 us: 1.22x faster                                                  |
| async_generators           | 384 ms                                                 | 316 ms: 1.22x faster                                                   |
| generators                 | 32.2 ms                                                | 26.6 ms: 1.21x faster                                                  |
| scimark_sor                | 130 ms                                                 | 110 ms: 1.18x faster                                                   |
| raytrace                   | 299 ms                                                 | 255 ms: 1.17x faster                                                   |
| chaos                      | 62.8 ms                                                | 53.7 ms: 1.17x faster                                                  |
| pylint                     | 319 ms                                                 | 274 ms: 1.16x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 65.9 ms: 1.16x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.73 ms: 1.16x faster                                                  |
| sqlalchemy_imperative      | 21.8 ms                                                | 18.9 ms: 1.15x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.12 sec: 1.15x faster                                                 |
| regex_compile              | 142 ms                                                 | 124 ms: 1.15x faster                                                   |
| float                      | 80.8 ms                                                | 70.4 ms: 1.15x faster                                                  |
| tomli_loads                | 2.11 sec                                               | 1.85 sec: 1.14x faster                                                 |
| sqlalchemy_declarative     | 143 ms                                                 | 126 ms: 1.13x faster                                                   |
| pyflate                    | 448 ms                                                 | 396 ms: 1.13x faster                                                   |
| pathlib                    | 21.5 ms                                                | 19.1 ms: 1.13x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.3 ms: 1.12x faster                                                  |
| coroutines                 | 23.9 ms                                                | 21.3 ms: 1.12x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.07 ms: 1.12x faster                                                  |
| logging_simple             | 6.63 us                                                | 5.92 us: 1.12x faster                                                  |
| richards                   | 45.9 ms                                                | 41.4 ms: 1.11x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 61.7 ms: 1.11x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 150 ms: 1.11x faster                                                   |
| sqlglot_parse              | 1.36 ms                                                | 1.23 ms: 1.10x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.59 ms: 1.10x faster                                                  |
| richards_super             | 51.9 ms                                                | 47.0 ms: 1.10x faster                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.52 ms: 1.10x faster                                                  |
| scimark_fft                | 342 ms                                                 | 311 ms: 1.10x faster                                                   |
| sympy_str                  | 292 ms                                                 | 266 ms: 1.09x faster                                                   |
| logging_format             | 7.35 us                                                | 6.71 us: 1.09x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.39 sec: 1.09x faster                                                 |
| pprint_safe_repr           | 743 ms                                                 | 681 ms: 1.09x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.09x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 151 us: 1.08x faster                                                   |
| meteor_contest             | 104 ms                                                 | 95.8 ms: 1.08x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 89.7 ms: 1.08x faster                                                  |
| nqueens                    | 80.1 ms                                                | 74.6 ms: 1.07x faster                                                  |
| logging_silent             | 109 ns                                                 | 102 ns: 1.07x faster                                                   |
| thrift                     | 791 us                                                 | 741 us: 1.07x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 19.3 ms: 1.07x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 47.1 ms: 1.06x faster                                                  |
| nbody                      | 89.3 ms                                                | 84.1 ms: 1.06x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.10 sec: 1.06x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 208 us: 1.06x faster                                                   |
| sqlglot_optimize           | 53.3 ms                                                | 50.4 ms: 1.06x faster                                                  |
| django_template            | 34.7 ms                                                | 32.8 ms: 1.06x faster                                                  |
| 2to3                       | 264 ms                                                 | 250 ms: 1.05x faster                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.19 ms: 1.05x faster                                                  |
| sympy_expand               | 468 ms                                                 | 446 ms: 1.05x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 81.5 ms: 1.05x faster                                                  |
| docutils                   | 2.64 sec                                               | 2.53 sec: 1.04x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 75.9 ms: 1.04x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 56.8 ms: 1.04x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 111 ms: 1.03x faster                                                   |
| fannkuch                   | 372 ms                                                 | 367 ms: 1.01x faster                                                   |
| pickle_pure_python         | 308 us                                                 | 304 us: 1.01x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 516 ms: 1.00x faster                                                   |
| regex_dna                  | 168 ms                                                 | 173 ms: 1.03x slower                                                   |
| mako                       | 11.0 ms                                                | 11.5 ms: 1.05x slower                                                  |
| python_startup_no_site     | 7.16 ms                                                | 7.54 ms: 1.05x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.6 us: 1.08x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.09x slower                                                  |
| telco                      | 6.53 ms                                                | 7.17 ms: 1.10x slower                                                  |
| coverage                   | 71.4 ms                                                | 78.9 ms: 1.10x slower                                                  |
| pidigits                   | 184 ms                                                 | 212 ms: 1.15x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 24.8 ms: 1.20x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.44 ms: 1.29x slower                                                  |
| python_startup             | 9.93 ms                                                | 14.8 ms: 1.49x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.83 ms: 1.67x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 277 ms: 2.60x slower                                                   |
| bench_mp_pool              | 10.8 ms                                                | 88.0 ms: 8.15x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (3): mdp, sqlite_synth, json
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250226-3.14.0a5+-fda056e/bm-20250226-vultr-x86_64-python-fda056e64bdfcac3dd3d-3.14.0a5+-fda056e.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.099x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.08x
- 95% likely to have a speedup of 1.07x
- 99% likely to have a speedup of 1.06x

# Memory
- memory change: 1.11x