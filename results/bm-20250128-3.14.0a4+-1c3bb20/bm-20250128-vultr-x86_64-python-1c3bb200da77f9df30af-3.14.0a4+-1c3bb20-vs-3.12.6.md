# Results vs. 3.12.6

- fork: python
- ref: 1c3bb200da77f9df30af
- machine: linux-x86_64
- commit hash: 1c3bb20
- commit date: 2025-01-28
- overall geometric mean: 1.090x faster
- HPT reliability: 100.00%
- HPT 99th percentile: 1.04x faster
- Memory change: 1.11x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 254 ms: 1.04x faster                                                   |
| docutils       | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                 |
| Geometric mean | (ref)                                                  | 1.03x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 619 ms: 1.79x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 316 ms: 1.77x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 626 ms: 1.73x faster                                                   |
| async_tree_none            | 464 ms                                                 | 272 ms: 1.71x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 325 ms: 1.71x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 264 ms: 1.69x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 483 ms: 1.50x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 494 ms: 1.45x faster                                                   |
| async_generators           | 384 ms                                                 | 320 ms: 1.20x faster                                                   |
| coroutines                 | 23.9 ms                                                | 21.8 ms: 1.10x faster                                                  |
| Geometric mean             | (ref)                                                  | 1.49x faster                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 72.0 ms: 1.12x faster                                                  |
| pidigits       | 184 ms                                                 | 194 ms: 1.05x slower                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmark hidden because not significant (1): nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 126 ms: 1.13x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 2.88 ms: 1.10x faster                                                  |
| regex_dna      | 168 ms                                                 | 172 ms: 1.03x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.8 ms: 1.15x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 127 ms: 1.09x faster                                                   |
| tomli_loads          | 2.11 sec                                               | 1.94 sec: 1.09x faster                                                 |
| xml_etree_iterparse  | 96.7 ms                                                | 90.5 ms: 1.07x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 212 us: 1.04x faster                                                   |
| xml_etree_generate   | 85.2 ms                                                | 83.6 ms: 1.02x faster                                                  |
| pickle_pure_python   | 308 us                                                 | 312 us: 1.02x slower                                                   |
| json_loads           | 26.5 us                                                | 28.4 us: 1.07x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.3 ms: 1.09x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.42 ms: 1.04x slower                                                  |
| python_startup         | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.23x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 21.3 ms: 1.07x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 48.4 ms: 1.04x faster                                                  |
| django_template | 34.7 ms                                                | 34.9 ms: 1.01x slower                                                  |
| mako            | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.01x faster                                                           |

All benchmarks:
===============

| Benchmark                  | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20 |
|----------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_tree_io_tg           | 1.11 sec                                               | 619 ms: 1.79x faster                                                   |
| async_tree_memoization_tg  | 560 ms                                                 | 316 ms: 1.77x faster                                                   |
| async_tree_io              | 1.08 sec                                               | 626 ms: 1.73x faster                                                   |
| async_tree_none            | 464 ms                                                 | 272 ms: 1.71x faster                                                   |
| async_tree_memoization     | 555 ms                                                 | 325 ms: 1.71x faster                                                   |
| async_tree_none_tg         | 446 ms                                                 | 264 ms: 1.69x faster                                                   |
| async_tree_cpu_io_mixed_tg | 723 ms                                                 | 483 ms: 1.50x faster                                                   |
| async_tree_cpu_io_mixed    | 715 ms                                                 | 494 ms: 1.45x faster                                                   |
| deepcopy                   | 352 us                                                 | 256 us: 1.37x faster                                                   |
| deepcopy_memo              | 40.3 us                                                | 30.1 us: 1.34x faster                                                  |
| spectral_norm              | 110 ms                                                 | 90.5 ms: 1.22x faster                                                  |
| go                         | 139 ms                                                 | 115 ms: 1.21x faster                                                   |
| async_generators           | 384 ms                                                 | 320 ms: 1.20x faster                                                   |
| deepcopy_reduce            | 3.08 us                                                | 2.60 us: 1.18x faster                                                  |
| comprehensions             | 19.8 us                                                | 16.8 us: 1.18x faster                                                  |
| pathlib                    | 21.5 ms                                                | 18.5 ms: 1.17x faster                                                  |
| generators                 | 32.2 ms                                                | 28.3 ms: 1.14x faster                                                  |
| pylint                     | 319 ms                                                 | 280 ms: 1.14x faster                                                   |
| sqlalchemy_imperative      | 21.8 ms                                                | 19.2 ms: 1.14x faster                                                  |
| regex_compile              | 142 ms                                                 | 126 ms: 1.13x faster                                                   |
| chaos                      | 62.8 ms                                                | 55.5 ms: 1.13x faster                                                  |
| crypto_pyaes               | 76.6 ms                                                | 67.9 ms: 1.13x faster                                                  |
| bpe_tokeniser              | 4.74 sec                                               | 4.21 sec: 1.13x faster                                                 |
| float                      | 80.8 ms                                                | 72.0 ms: 1.12x faster                                                  |
| scimark_sor                | 130 ms                                                 | 116 ms: 1.12x faster                                                   |
| sqlalchemy_declarative     | 143 ms                                                 | 128 ms: 1.12x faster                                                   |
| raytrace                   | 299 ms                                                 | 268 ms: 1.12x faster                                                   |
| coroutines                 | 23.9 ms                                                | 21.8 ms: 1.10x faster                                                  |
| regex_effbot               | 3.17 ms                                                | 2.88 ms: 1.10x faster                                                  |
| logging_simple             | 6.63 us                                                | 6.04 us: 1.10x faster                                                  |
| sympy_sum                  | 166 ms                                                 | 152 ms: 1.09x faster                                                   |
| logging_format             | 7.35 us                                                | 6.73 us: 1.09x faster                                                  |
| sqlglot_parse              | 1.36 ms                                                | 1.24 ms: 1.09x faster                                                  |
| xml_etree_parse            | 139 ms                                                 | 127 ms: 1.09x faster                                                   |
| tomli_loads                | 2.11 sec                                               | 1.94 sec: 1.09x faster                                                 |
| sqlglot_transpile          | 1.67 ms                                                | 1.54 ms: 1.09x faster                                                  |
| deltablue                  | 3.45 ms                                                | 3.18 ms: 1.08x faster                                                  |
| richards                   | 45.9 ms                                                | 42.5 ms: 1.08x faster                                                  |
| thrift                     | 791 us                                                 | 732 us: 1.08x faster                                                   |
| pyflate                    | 448 ms                                                 | 415 ms: 1.08x faster                                                   |
| scimark_fft                | 342 ms                                                 | 317 ms: 1.08x faster                                                   |
| sympy_str                  | 292 ms                                                 | 271 ms: 1.07x faster                                                   |
| genshi_text                | 22.8 ms                                                | 21.3 ms: 1.07x faster                                                  |
| xml_etree_iterparse        | 96.7 ms                                                | 90.5 ms: 1.07x faster                                                  |
| richards_super             | 51.9 ms                                                | 48.6 ms: 1.07x faster                                                  |
| scimark_monte_carlo        | 68.4 ms                                                | 64.3 ms: 1.06x faster                                                  |
| hexiom                     | 6.17 ms                                                | 5.80 ms: 1.06x faster                                                  |
| pprint_pformat             | 1.52 sec                                               | 1.44 sec: 1.06x faster                                                 |
| dulwich_log                | 78.9 ms                                                | 74.5 ms: 1.06x faster                                                  |
| pprint_safe_repr           | 743 ms                                                 | 703 ms: 1.06x faster                                                   |
| typing_runtime_protocols   | 163 us                                                 | 155 us: 1.06x faster                                                   |
| pycparser                  | 1.17 sec                                               | 1.11 sec: 1.05x faster                                                 |
| sympy_integrate            | 20.5 ms                                                | 19.7 ms: 1.05x faster                                                  |
| meteor_contest             | 104 ms                                                 | 99.4 ms: 1.04x faster                                                  |
| unpickle_pure_python       | 221 us                                                 | 212 us: 1.04x faster                                                   |
| nqueens                    | 80.1 ms                                                | 77.2 ms: 1.04x faster                                                  |
| genshi_xml                 | 50.2 ms                                                | 48.4 ms: 1.04x faster                                                  |
| 2to3                       | 264 ms                                                 | 254 ms: 1.04x faster                                                   |
| docutils                   | 2.64 sec                                               | 2.56 sec: 1.03x faster                                                 |
| sqlglot_optimize           | 53.3 ms                                                | 51.8 ms: 1.03x faster                                                  |
| logging_silent             | 109 ns                                                 | 106 ns: 1.03x faster                                                   |
| sympy_expand               | 468 ms                                                 | 456 ms: 1.03x faster                                                   |
| sqlglot_normalize          | 107 ms                                                 | 104 ms: 1.02x faster                                                   |
| scimark_lu                 | 114 ms                                                 | 111 ms: 1.02x faster                                                   |
| xml_etree_generate         | 85.2 ms                                                | 83.6 ms: 1.02x faster                                                  |
| django_template            | 34.7 ms                                                | 34.9 ms: 1.01x slower                                                  |
| mdp                        | 2.42 sec                                               | 2.44 sec: 1.01x slower                                                 |
| scimark_sparse_mat_mult    | 4.39 ms                                                | 4.44 ms: 1.01x slower                                                  |
| fannkuch                   | 372 ms                                                 | 377 ms: 1.01x slower                                                   |
| pickle_pure_python         | 308 us                                                 | 312 us: 1.02x slower                                                   |
| regex_dna                  | 168 ms                                                 | 172 ms: 1.03x slower                                                   |
| python_startup_no_site     | 7.16 ms                                                | 7.42 ms: 1.04x slower                                                  |
| pidigits                   | 184 ms                                                 | 194 ms: 1.05x slower                                                   |
| mako                       | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                  |
| json_loads                 | 26.5 us                                                | 28.4 us: 1.07x slower                                                  |
| json_dumps                 | 10.4 ms                                                | 11.3 ms: 1.09x slower                                                  |
| bench_thread_pool          | 941 us                                                 | 1.03 ms: 1.10x slower                                                  |
| telco                      | 6.53 ms                                                | 7.21 ms: 1.11x slower                                                  |
| coverage                   | 71.4 ms                                                | 79.5 ms: 1.11x slower                                                  |
| regex_v8                   | 20.6 ms                                                | 23.8 ms: 1.15x slower                                                  |
| gc_traversal               | 3.46 ms                                                | 4.21 ms: 1.22x slower                                                  |
| python_startup             | 9.93 ms                                                | 14.6 ms: 1.47x slower                                                  |
| create_gc_cycles           | 1.09 ms                                                | 1.86 ms: 1.70x slower                                                  |
| bench_mp_pool              | 10.8 ms                                                | 87.8 ms: 8.13x slower                                                  |
| Geometric mean             | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (5): sqlite_synth, nbody, asyncio_websockets, xml_etree_process, json
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, asyncio_tcp, asyncio_tcp_ssl, chameleon, dask, flaskblogging, gunicorn, html5lib, mypy2, pickle, pickle_dict, pickle_list, tornado_http, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (6) of results/bm-20250128-3.14.0a4+-1c3bb20/bm-20250128-vultr-x86_64-python-1c3bb200da77f9df30af-3.14.0a4+-1c3bb20.json: connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

- Geometric mean (including insignificant results): 1.090x faster

# HPT report

- Reliability score: 100.00% likely to be faster
- 90% likely to have a speedup of 1.05x
- 95% likely to have a speedup of 1.05x
- 99% likely to have a speedup of 1.04x

# Memory
- memory change: 1.11x