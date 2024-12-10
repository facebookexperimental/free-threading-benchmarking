# Results vs. 3.12.6

- fork: python
- ref: 5c89adf385aaaca97c2e
- machine: linux-x86_64
- commit hash: 5c89adf
- commit date: 2024-12-09
- overall geometric mean: 1.060x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.01x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 259 ms: 1.02x faster                                                   |
| docutils       | 2.64 sec                                               | 2.57 sec: 1.03x faster                                                 |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 602 ms: 1.80x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 622 ms: 1.79x faster                                                   |
| async_tree_none            | 464 ms                                                 | 275 ms: 1.69x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 334 ms: 1.68x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 341 ms: 1.63x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 275 ms: 1.62x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 599 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 603 ms: 1.19x faster                                                   |
| coroutines                 | 23.9 ms                                                | 22.0 ms: 1.09x faster                                                  |
| async_generators           | 384 ms                                                 | 362 ms: 1.06x faster                                                   |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                   |
| Geometric mean             | (ref)                                                  | 1.40x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 79.3 ms: 1.02x faster                                                  |
| nbody          | 89.3 ms                                                | 96.1 ms: 1.08x slower                                                  |
| pidigits       | 184 ms                                                 | 221 ms: 1.20x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                  |
| regex_compile  | 142 ms                                                 | 131 ms: 1.09x faster                                                   |
| regex_dna      | 168 ms                                                 | 179 ms: 1.06x slower                                                   |
| regex_v8       | 20.6 ms                                                | 25.2 ms: 1.23x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                                   |
| json_loads           | 26.5 us                                                | 24.9 us: 1.07x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 91.0 ms: 1.06x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 215 us: 1.02x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 2.09 sec: 1.01x faster                                                 |
| xml_etree_process    | 59.0 ms                                                | 59.7 ms: 1.01x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 320 us: 1.04x slower                                                   |
| json_dumps           | 10.4 ms                                                | 11.5 ms: 1.11x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.47 ms: 1.04x slower                                                  |
| python_startup         | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.0 ms: 1.04x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 50.4 ms: 1.00x slower                                                  |
| django_template | 34.7 ms                                                | 35.8 ms: 1.03x slower                                                  |
| mako            | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io              | 1.08 sec                                               | 602 ms: 1.80x faster                                                   |
| async_tree_io_tg           | 1.11 sec                                               | 622 ms: 1.79x faster                                                   |
| async_tree_none            | 464 ms                                                 | 275 ms: 1.69x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 334 ms: 1.68x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 341 ms: 1.63x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 275 ms: 1.62x faster                                                   |
| deepcopy                   | 352 us                                                 | 262 us: 1.34x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 30.1 us: 1.34x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 599 ms: 1.21x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 603 ms: 1.19x faster                                                   |
| pathlib                    | 21.5 ms                                                | 18.3 ms: 1.18x faster                                                  |
| go                         | 139 ms                                                 | 120 ms: 1.16x faster                                                   |
| crypto_pyaes               | 76.6 ms                                                | 66.5 ms: 1.15x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.68 us: 1.15x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.77 ms: 1.14x faster                                                  |
| pylint                     | 319 ms                                                 | 280 ms: 1.14x faster                                                   |
| comprehensions             | 19.8 us                                                | 17.5 us: 1.13x faster                                                  |
| raytrace                   | 299 ms                                                 | 265 ms: 1.13x faster                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 128 ms: 1.12x faster                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.5 ms: 1.12x faster                                                  |
| generators                 | 32.2 ms                                                | 29.0 ms: 1.11x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.32 sec: 1.10x faster                                                 |
| logging_simple             | 6.63 us                                                | 6.06 us: 1.09x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                                   |
| regex_compile              | 142 ms                                                 | 131 ms: 1.09x faster                                                   |
| coroutines                 | 23.9 ms                                                | 22.0 ms: 1.09x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 153 ms: 1.08x faster                                                   |
| logging_format             | 7.35 us                                                | 6.79 us: 1.08x faster                                                  |
| json                       | 5.02 ms                                                | 4.68 ms: 1.07x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.21 ms: 1.07x faster                                                  |
| chaos                      | 62.8 ms                                                | 58.9 ms: 1.07x faster                                                  |
| json_loads                 | 26.5 us                                                | 24.9 us: 1.07x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 91.0 ms: 1.06x faster                                                  |
| async_generators           | 384 ms                                                 | 362 ms: 1.06x faster                                                   |
| sympy_str                  | 292 ms                                                 | 275 ms: 1.06x faster                                                   |
| thrift                     | 791 us                                                 | 750 us: 1.06x faster                                                   |
| scimark_monte_carlo        | 68.4 ms                                                | 65.2 ms: 1.05x faster                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.29 ms: 1.05x faster                                                  |
| sqlglot_transpile          | 1.67 ms                                                | 1.60 ms: 1.04x faster                                                  |
| meteor_contest             | 104 ms                                                 | 99.3 ms: 1.04x faster                                                  |
| pycparser                  | 1.17 sec                                               | 1.12 sec: 1.04x faster                                                 |
| pprint_pformat             | 1.52 sec                                               | 1.46 sec: 1.04x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 76.0 ms: 1.04x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 716 ms: 1.04x faster                                                   |
| genshi_text                | 22.8 ms                                                | 22.0 ms: 1.04x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 158 us: 1.04x faster                                                   |
| hexiom                     | 6.17 ms                                                | 5.99 ms: 1.03x faster                                                  |
| mdp                        | 2.42 sec                                               | 2.35 sec: 1.03x faster                                                 |
| spectral_norm              | 110 ms                                                 | 107 ms: 1.03x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.57 sec: 1.03x faster                                                 |
| unpickle_pure_python       | 221 us                                                 | 215 us: 1.02x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 112 ms: 1.02x faster                                                   |
| sympy_integrate            | 20.5 ms                                                | 20.1 ms: 1.02x faster                                                  |
| float                      | 80.8 ms                                                | 79.3 ms: 1.02x faster                                                  |
| 2to3                       | 264 ms                                                 | 259 ms: 1.02x faster                                                   |
| sympy_expand               | 468 ms                                                 | 461 ms: 1.01x faster                                                   |
| nqueens                    | 80.1 ms                                                | 79.0 ms: 1.01x faster                                                  |
| pyflate                    | 448 ms                                                 | 444 ms: 1.01x faster                                                   |
| logging_silent             | 109 ns                                                 | 108 ns: 1.01x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 2.09 sec: 1.01x faster                                                 |
| fannkuch                   | 372 ms                                                 | 370 ms: 1.01x faster                                                   |
| genshi_xml                 | 50.2 ms                                                | 50.4 ms: 1.00x slower                                                  |
| sqlite_synth               | 2.20 us                                                | 2.22 us: 1.01x slower                                                  |
| asyncio_websockets         | 517 ms                                                 | 523 ms: 1.01x slower                                                   |
| xml_etree_process          | 59.0 ms                                                | 59.7 ms: 1.01x slower                                                  |
| sqlglot_optimize           | 53.3 ms                                                | 54.1 ms: 1.02x slower                                                  |
| richards_super             | 51.9 ms                                                | 52.9 ms: 1.02x slower                                                  |
| sqlglot_normalize          | 107 ms                                                 | 109 ms: 1.02x slower                                                   |
| scimark_fft                | 342 ms                                                 | 349 ms: 1.02x slower                                                   |
| django_template            | 34.7 ms                                                | 35.8 ms: 1.03x slower                                                  |
| scimark_sor                | 130 ms                                                 | 135 ms: 1.04x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 320 us: 1.04x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.47 ms: 1.04x slower                                                  |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                  |
| regex_dna                  | 168 ms                                                 | 179 ms: 1.06x slower                                                   |
| nbody                      | 89.3 ms                                                | 96.1 ms: 1.08x slower                                                  |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.76 ms: 1.08x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.10x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.5 ms: 1.11x slower                                                  |
| coverage                   | 71.4 ms                                                | 79.4 ms: 1.11x slower                                                  |
| telco                      | 6.53 ms                                                | 7.38 ms: 1.13x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.02 ms: 1.16x slower                                                  |
| pidigits                   | 184 ms                                                 | 221 ms: 1.20x slower                                                   |
| regex_v8                   | 20.6 ms                                                | 25.2 ms: 1.23x slower                                                  |
| python_startup             | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.69 ms: 1.55x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 86.0 ms: 7.96x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (2): xml_etree_generate, richards
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20241209-3.14.0a2+-5c89adf/bm-20241209-vultr-x86_64-python-5c89adf385aaaca97c2e-3.14.0a2+-5c89adf.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.060x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.02x
- 95% likely to have a speedup of 1.02x
- 99% likely to have a speedup of 1.01x

# Memory
- memory change: 1.11x