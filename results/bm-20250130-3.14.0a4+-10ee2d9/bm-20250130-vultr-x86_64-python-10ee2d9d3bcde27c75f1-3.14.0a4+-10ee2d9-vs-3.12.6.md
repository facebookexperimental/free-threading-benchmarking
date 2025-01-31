# Results vs. 3.12.6

- fork: python
- ref: 10ee2d9d3bcde27c75f1
- machine: linux-x86_64
- commit hash: 10ee2d9
- commit date: 2025-01-30
- overall geometric mean: 1.097x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.05x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 253 ms: 1.04x faster                                                   |
| docutils       | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                 |
| Geometric mean | (ref)                                                  | 1.04x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 623 ms: 1.78x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 318 ms: 1.76x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 622 ms: 1.74x faster                                                   |
| async_tree_none            | 464 ms                                                 | 268 ms: 1.73x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 323 ms: 1.72x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 264 ms: 1.69x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 538 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 552 ms: 1.29x faster                                                   |
| async_generators           | 384 ms                                                 | 321 ms: 1.20x faster                                                   |
| coroutines                 | 23.9 ms                                                | 21.9 ms: 1.10x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.46x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 70.8 ms: 1.14x faster                                                  |
| pidigits       | 184 ms                                                 | 210 ms: 1.14x slower                                                   |
| Geometric mean | (ref)                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 125 ms: 1.14x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 2.84 ms: 1.12x faster                                                  |
| regex_dna      | 168 ms                                                 | 171 ms: 1.02x slower                                                   |
| regex_v8       | 20.6 ms                                                | 22.8 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| tomli_loads          | 2.11 sec                                               | 1.85 sec: 1.14x faster                                                 |
| xml_etree_parse      | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 91.4 ms: 1.06x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 209 us: 1.06x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 83.5 ms: 1.02x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 58.0 ms: 1.02x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 309 us: 1.01x slower                                                   |
| json_loads           | 26.5 us                                                | 28.5 us: 1.07x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.47 ms: 1.04x slower                                                  |
| python_startup         | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.24x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 48.1 ms: 1.04x faster                                                  |
| django_template | 34.7 ms                                                | 34.2 ms: 1.01x faster                                                  |
| mako            | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.03x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 623 ms: 1.78x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 318 ms: 1.76x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 622 ms: 1.74x faster                                                   |
| async_tree_none            | 464 ms                                                 | 268 ms: 1.73x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 323 ms: 1.72x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 264 ms: 1.69x faster                                                   |
| deepcopy                   | 352 us                                                 | 252 us: 1.39x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 29.6 us: 1.36x faster                                                  |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 538 ms: 1.34x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 552 ms: 1.29x faster                                                   |
| go                         | 139 ms                                                 | 112 ms: 1.24x faster                                                   |
| spectral_norm              | 110 ms                                                 | 89.3 ms: 1.23x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.4 us: 1.21x faster                                                  |
| async_generators           | 384 ms                                                 | 321 ms: 1.20x faster                                                   |
| pathlib                    | 21.5 ms                                                | 18.0 ms: 1.20x faster                                                  |
| deepcopy_reduce            | 3.08 us                                                | 2.61 us: 1.18x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 65.7 ms: 1.17x faster                                                  |
| scimark_sor                | 130 ms                                                 | 112 ms: 1.15x faster                                                   |
| pylint                     | 319 ms                                                 | 277 ms: 1.15x faster                                                   |
| raytrace                   | 299 ms                                                 | 261 ms: 1.15x faster                                                   |
| bpe_tokeniser              | 4.74 sec                                               | 4.14 sec: 1.14x faster                                                 |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.1 ms: 1.14x faster                                                  |
| float                      | 80.8 ms                                                | 70.8 ms: 1.14x faster                                                  |
| regex_compile              | 142 ms                                                 | 125 ms: 1.14x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.85 sec: 1.14x faster                                                 |
| chaos                      | 62.8 ms                                                | 55.4 ms: 1.13x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.06 ms: 1.13x faster                                                  |
| sqlalchemy_declarative     | 143 ms                                                 | 127 ms: 1.13x faster                                                   |
| logging_simple             | 6.63 us                                                | 5.89 us: 1.12x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 60.9 ms: 1.12x faster                                                  |
| logging_format             | 7.35 us                                                | 6.55 us: 1.12x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.84 ms: 1.12x faster                                                  |
| generators                 | 32.2 ms                                                | 29.0 ms: 1.11x faster                                                  |
| richards                   | 45.9 ms                                                | 41.7 ms: 1.10x faster                                                  |
| genshi_text                | 22.8 ms                                                | 20.7 ms: 1.10x faster                                                  |
| pyflate                    | 448 ms                                                 | 407 ms: 1.10x faster                                                   |
| scimark_fft                | 342 ms                                                 | 311 ms: 1.10x faster                                                   |
| sympy_sum                  | 166 ms                                                 | 151 ms: 1.10x faster                                                   |
| coroutines                 | 23.9 ms                                                | 21.9 ms: 1.10x faster                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.24 ms: 1.09x faster                                                  |
| sympy_str                  | 292 ms                                                 | 269 ms: 1.09x faster                                                   |
| sqlglot_transpile          | 1.67 ms                                                | 1.54 ms: 1.09x faster                                                  |
| thrift                     | 791 us                                                 | 731 us: 1.08x faster                                                   |
| xml_etree_parse            | 139 ms                                                 | 128 ms: 1.08x faster                                                   |
| hexiom                     | 6.17 ms                                                | 5.73 ms: 1.08x faster                                                  |
| richards_super             | 51.9 ms                                                | 48.2 ms: 1.08x faster                                                  |
| typing_runtime_protocols   | 163 us                                                 | 153 us: 1.07x faster                                                   |
| pprint_safe_repr           | 743 ms                                                 | 698 ms: 1.06x faster                                                   |
| pprint_pformat             | 1.52 sec                                               | 1.43 sec: 1.06x faster                                                 |
| xml_etree_iterparse        | 96.7 ms                                                | 91.4 ms: 1.06x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 209 us: 1.06x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 74.9 ms: 1.05x faster                                                  |
| sympy_integrate            | 20.5 ms                                                | 19.6 ms: 1.05x faster                                                  |
| meteor_contest             | 104 ms                                                 | 98.6 ms: 1.05x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 48.1 ms: 1.04x faster                                                  |
| 2to3                       | 264 ms                                                 | 253 ms: 1.04x faster                                                   |
| logging_silent             | 109 ns                                                 | 105 ns: 1.04x faster                                                   |
| nqueens                    | 80.1 ms                                                | 76.9 ms: 1.04x faster                                                  |
| sympy_expand               | 468 ms                                                 | 450 ms: 1.04x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.54 sec: 1.04x faster                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 51.4 ms: 1.04x faster                                                  |
| sqlglot_normalize          | 107 ms                                                 | 103 ms: 1.03x faster                                                   |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.29 ms: 1.03x faster                                                  |
| fannkuch                   | 372 ms                                                 | 364 ms: 1.02x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 83.5 ms: 1.02x faster                                                  |
| xml_etree_process          | 59.0 ms                                                | 58.0 ms: 1.02x faster                                                  |
| django_template            | 34.7 ms                                                | 34.2 ms: 1.01x faster                                                  |
| sqlite_synth               | 2.20 us                                                | 2.17 us: 1.01x faster                                                  |
| scimark_lu                 | 114 ms                                                 | 113 ms: 1.01x faster                                                   |
| pickle_pure_python         | 308 us                                                 | 309 us: 1.01x slower                                                   |
| mdp                        | 2.42 sec                                               | 2.45 sec: 1.01x slower                                                 |
| regex_dna                  | 168 ms                                                 | 171 ms: 1.02x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.47 ms: 1.04x slower                                                  |
| mako                       | 11.0 ms                                                | 11.6 ms: 1.05x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.5 us: 1.07x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.2 ms: 1.08x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.09x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 22.8 ms: 1.11x slower                                                  |
| coverage                   | 71.4 ms                                                | 80.0 ms: 1.12x slower                                                  |
| telco                      | 6.53 ms                                                | 7.31 ms: 1.12x slower                                                  |
| pidigits                   | 184 ms                                                 | 210 ms: 1.14x slower                                                   |
| gc_traversal               | 3.46 ms                                                | 4.27 ms: 1.23x slower                                                  |
| python_startup             | 9.93 ms                                                | 14.7 ms: 1.48x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.84 ms: 1.68x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 88.0 ms: 8.15x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.07x faster                                                           |

Benchmark hidden because not significant (3): nbody, json, asyncio_websockets
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250130-3.14.0a4+-10ee2d9/bm-20250130-vultr-x86_64-python-10ee2d9d3bcde27c75f1-3.14.0a4+-10ee2d9.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.097x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.06x
- 95% likely to have a speedup of 1.06x
- 99% likely to have a speedup of 1.05x

# Memory
- memory change: 1.11x