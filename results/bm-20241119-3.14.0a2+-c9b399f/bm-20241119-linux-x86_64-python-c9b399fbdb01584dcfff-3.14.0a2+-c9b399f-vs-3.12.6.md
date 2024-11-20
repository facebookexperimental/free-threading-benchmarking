# Results vs. 3.12.6

- fork: python
- ref: c9b399fbdb01584dcfff
- machine: linux-x86_64
- commit hash: c9b399f
- commit date: 2024-11-19
- overall geometric mean: 1.01x faster
- HPT reliability: 99.37%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 410 ms: 1.11x faster                                                   |
| docutils       | 4.00 sec                                               | 3.66 sec: 1.09x faster                                                 |
| Geometric mean | (ref)                                                  | 1.06x faster                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_tcp_ssl | 2.81 sec                                               | 2.73 sec: 1.03x faster                                                 |
| coroutines      | 29.5 ms                                                | 31.6 ms: 1.07x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (3): asyncio_tcp, asyncio_websockets, async_generators

Benchmarks with tag 'math':
===========================

Benchmark hidden because not significant (3): float, pidigits, nbody

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.65 ms: 1.10x faster                                                  |
| regex_v8       | 32.5 ms                                                | 35.5 ms: 1.09x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (2): regex_compile, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_dict         | 52.7 us                                                | 45.8 us: 1.15x faster                                                  |
| unpickle            | 21.2 us                                                | 18.9 us: 1.12x faster                                                  |
| xml_etree_parse     | 241 ms                                                 | 215 ms: 1.12x faster                                                   |
| tomli_loads         | 2.88 sec                                               | 2.62 sec: 1.10x faster                                                 |
| xml_etree_iterparse | 169 ms                                                 | 155 ms: 1.10x faster                                                   |
| xml_etree_generate  | 127 ms                                                 | 119 ms: 1.07x faster                                                   |
| unpickle_list       | 6.83 us                                                | 7.03 us: 1.03x slower                                                  |
| pickle              | 16.4 us                                                | 17.5 us: 1.07x slower                                                  |
| pickle_list         | 6.97 us                                                | 7.49 us: 1.07x slower                                                  |
| json_dumps          | 14.3 ms                                                | 15.5 ms: 1.09x slower                                                  |
| Geometric mean      | (ref)                                                  | 1.03x faster                                                           |

Benchmark hidden because not significant (4): xml_etree_process, unpickle_pure_python, pickle_pure_python, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 14.0 ms: 1.26x faster                                                  |
| python_startup         | 23.7 ms                                                | 19.9 ms: 1.19x faster                                                  |
| Geometric mean         | (ref)                                                  | 1.23x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 30.2 ms                                                | 28.7 ms: 1.05x faster                                                  |
| django_template | 44.9 ms                                                | 46.7 ms: 1.04x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 71.6 ms: 1.06x slower                                                  |
| mako            | 15.7 ms                                                | 16.7 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-linux-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy                 | 468 us                                                 | 352 us: 1.33x faster                                                   |
| deepcopy_memo            | 52.4 us                                                | 41.4 us: 1.27x faster                                                  |
| python_startup_no_site   | 17.6 ms                                                | 14.0 ms: 1.26x faster                                                  |
| comprehensions           | 27.1 us                                                | 22.5 us: 1.21x faster                                                  |
| python_startup           | 23.7 ms                                                | 19.9 ms: 1.19x faster                                                  |
| sqlglot_normalize        | 157 ms                                                 | 134 ms: 1.17x faster                                                   |
| bench_thread_pool        | 3.48 ms                                                | 2.99 ms: 1.16x faster                                                  |
| pickle_dict              | 52.7 us                                                | 45.8 us: 1.15x faster                                                  |
| pathlib                  | 31.6 ms                                                | 27.5 ms: 1.15x faster                                                  |
| gc_traversal             | 5.86 ms                                                | 5.16 ms: 1.14x faster                                                  |
| unpickle                 | 21.2 us                                                | 18.9 us: 1.12x faster                                                  |
| xml_etree_parse          | 241 ms                                                 | 215 ms: 1.12x faster                                                   |
| mdp                      | 3.97 sec                                               | 3.55 sec: 1.12x faster                                                 |
| 2to3                     | 456 ms                                                 | 410 ms: 1.11x faster                                                   |
| bpe_tokeniser            | 6.59 sec                                               | 5.93 sec: 1.11x faster                                                 |
| pycparser                | 1.79 sec                                               | 1.62 sec: 1.11x faster                                                 |
| regex_effbot             | 5.13 ms                                                | 4.65 ms: 1.10x faster                                                  |
| tomli_loads              | 2.88 sec                                               | 2.62 sec: 1.10x faster                                                 |
| pyflate                  | 727 ms                                                 | 663 ms: 1.10x faster                                                   |
| scimark_monte_carlo      | 96.4 ms                                                | 87.9 ms: 1.10x faster                                                  |
| xml_etree_iterparse      | 169 ms                                                 | 155 ms: 1.10x faster                                                   |
| crypto_pyaes             | 107 ms                                                 | 98.1 ms: 1.09x faster                                                  |
| docutils                 | 4.00 sec                                               | 3.66 sec: 1.09x faster                                                 |
| sympy_str                | 385 ms                                                 | 353 ms: 1.09x faster                                                   |
| raytrace                 | 408 ms                                                 | 376 ms: 1.08x faster                                                   |
| sympy_sum                | 222 ms                                                 | 205 ms: 1.08x faster                                                   |
| deepcopy_reduce          | 4.04 us                                                | 3.76 us: 1.07x faster                                                  |
| xml_etree_generate       | 127 ms                                                 | 119 ms: 1.07x faster                                                   |
| logging_simple           | 9.45 us                                                | 8.87 us: 1.06x faster                                                  |
| nqueens                  | 117 ms                                                 | 110 ms: 1.06x faster                                                   |
| genshi_text              | 30.2 ms                                                | 28.7 ms: 1.05x faster                                                  |
| generators               | 41.1 ms                                                | 39.4 ms: 1.04x faster                                                  |
| fannkuch                 | 540 ms                                                 | 518 ms: 1.04x faster                                                   |
| typing_runtime_protocols | 224 us                                                 | 216 us: 1.04x faster                                                   |
| pprint_safe_repr         | 967 ms                                                 | 936 ms: 1.03x faster                                                   |
| scimark_fft              | 500 ms                                                 | 485 ms: 1.03x faster                                                   |
| asyncio_tcp_ssl          | 2.81 sec                                               | 2.73 sec: 1.03x faster                                                 |
| pprint_pformat           | 1.98 sec                                               | 1.92 sec: 1.03x faster                                                 |
| unpickle_list            | 6.83 us                                                | 7.03 us: 1.03x slower                                                  |
| django_template          | 44.9 ms                                                | 46.7 ms: 1.04x slower                                                  |
| meteor_contest           | 146 ms                                                 | 152 ms: 1.04x slower                                                   |
| chaos                    | 84.9 ms                                                | 89.2 ms: 1.05x slower                                                  |
| genshi_xml               | 67.6 ms                                                | 71.6 ms: 1.06x slower                                                  |
| scimark_sor              | 167 ms                                                 | 177 ms: 1.06x slower                                                   |
| mako                     | 15.7 ms                                                | 16.7 ms: 1.06x slower                                                  |
| coroutines               | 29.5 ms                                                | 31.6 ms: 1.07x slower                                                  |
| pickle                   | 16.4 us                                                | 17.5 us: 1.07x slower                                                  |
| pickle_list              | 6.97 us                                                | 7.49 us: 1.07x slower                                                  |
| richards                 | 60.3 ms                                                | 64.8 ms: 1.07x slower                                                  |
| logging_silent           | 139 ns                                                 | 150 ns: 1.08x slower                                                   |
| hexiom                   | 8.27 ms                                                | 8.93 ms: 1.08x slower                                                  |
| json_dumps               | 14.3 ms                                                | 15.5 ms: 1.09x slower                                                  |
| unpack_sequence          | 60.2 ns                                                | 65.7 ns: 1.09x slower                                                  |
| regex_v8                 | 32.5 ms                                                | 35.5 ms: 1.09x slower                                                  |
| sympy_expand             | 582 ms                                                 | 641 ms: 1.10x slower                                                   |
| telco                    | 9.59 ms                                                | 10.6 ms: 1.11x slower                                                  |
| deltablue                | 4.27 ms                                                | 4.90 ms: 1.15x slower                                                  |
| coverage                 | 95.4 ms                                                | 113 ms: 1.19x slower                                                   |
| create_gc_cycles         | 1.94 ms                                                | 2.34 ms: 1.21x slower                                                  |
| bench_mp_pool            | 20.7 ms                                                | 68.3 ms: 3.30x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (28): sympy_integrate, regex_compile, spectral_norm, float, asyncio_tcp, xml_etree_process, asyncio_websockets, unpickle_pure_python, pidigits, scimark_sparse_mat_mult, dulwich_log, sqlite_synth, pylint, regex_dna, async_generators, sqlglot_optimize, sqlglot_transpile, pickle_pure_python, sqlglot_parse, go, richards_super, html5lib, logging_format, json, json_loads, scimark_lu, nbody, thrift
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 99.37% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x