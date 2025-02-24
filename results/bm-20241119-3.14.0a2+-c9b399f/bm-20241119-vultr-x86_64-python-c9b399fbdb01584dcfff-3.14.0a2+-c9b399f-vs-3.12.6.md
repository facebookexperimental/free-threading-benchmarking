# Results vs. 3.12.6

- fork: python
- ref: c9b399fbdb01584dcfff
- machine: linux-x86_64
- commit hash: c9b399f
- commit date: 2024-11-19
- overall geometric mean: 1.01x slower
- HPT reliability: 98.71%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 255 ms: 1.04x faster                                                   |
| docutils       | 2.64 sec                                               | 2.60 sec: 1.01x faster                                                 |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|--------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| coroutines         | 23.9 ms                                                | 22.9 ms: 1.04x faster                                                  |
| asyncio_tcp        | 519 ms                                                 | 504 ms: 1.03x faster                                                   |
| async_generators   | 384 ms                                                 | 375 ms: 1.03x faster                                                   |
| asyncio_websockets | 517 ms                                                 | 521 ms: 1.01x slower                                                   |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.53 sec: 1.01x slower                                                 |
| Geometric mean     | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 79.8 ms: 1.01x faster                                                  |
| nbody          | 89.3 ms                                                | 96.3 ms: 1.08x slower                                                  |
| pidigits       | 184 ms                                                 | 217 ms: 1.18x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.89 ms: 1.10x faster                                                  |
| regex_compile  | 142 ms                                                 | 135 ms: 1.06x faster                                                   |
| regex_dna      | 168 ms                                                 | 183 ms: 1.09x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.6 ms: 1.20x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_loads           | 26.5 us                                                | 25.1 us: 1.06x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 135 ms: 1.03x faster                                                   |
| unpickle_pure_python | 221 us                                                 | 215 us: 1.03x faster                                                   |
| unpickle             | 14.1 us                                                | 13.7 us: 1.03x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 96.1 ms: 1.01x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.13 sec: 1.01x slower                                                 |
| pickle_pure_python   | 308 us                                                 | 317 us: 1.03x slower                                                   |
| pickle_dict          | 31.8 us                                                | 32.8 us: 1.03x slower                                                  |
| unpickle_list        | 4.67 us                                                | 4.83 us: 1.03x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                  |
| pickle_list          | 4.77 us                                                | 5.32 us: 1.12x slower                                                  |
| pickle               | 10.9 us                                                | 12.6 us: 1.15x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.02x slower                                                           |

Benchmark hidden because not significant (2): xml_etree_process, xml_etree_generate

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.47 ms: 1.04x slower                                                  |
| python_startup         | 9.93 ms                                                | 11.1 ms: 1.12x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.4 ms: 1.02x faster                                                  |
| django_template | 34.7 ms                                                | 35.1 ms: 1.01x slower                                                  |
| mako            | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-python-c9b399fbdb01584dcfff-3.14.0a2+-c9b399f |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy_memo            | 40.3 us                                                | 30.3 us: 1.33x faster                                                  |
| deepcopy                 | 352 us                                                 | 266 us: 1.32x faster                                                   |
| pathlib                  | 21.5 ms                                                | 18.4 ms: 1.17x faster                                                  |
| comprehensions           | 19.8 us                                                | 17.1 us: 1.16x faster                                                  |
| go                       | 139 ms                                                 | 120 ms: 1.16x faster                                                   |
| deepcopy_reduce          | 3.08 us                                                | 2.69 us: 1.14x faster                                                  |
| raytrace                 | 299 ms                                                 | 262 ms: 1.14x faster                                                   |
| crypto_pyaes             | 76.6 ms                                                | 68.4 ms: 1.12x faster                                                  |
| regex_effbot             | 3.17 ms                                                | 2.89 ms: 1.10x faster                                                  |
| bpe_tokeniser            | 4.74 sec                                               | 4.35 sec: 1.09x faster                                                 |
| sympy_sum                | 166 ms                                                 | 153 ms: 1.09x faster                                                   |
| generators               | 32.2 ms                                                | 29.7 ms: 1.09x faster                                                  |
| unpack_sequence          | 52.1 ns                                                | 48.1 ns: 1.08x faster                                                  |
| json                     | 5.02 ms                                                | 4.67 ms: 1.08x faster                                                  |
| logging_simple           | 6.63 us                                                | 6.17 us: 1.07x faster                                                  |
| sympy_str                | 292 ms                                                 | 274 ms: 1.06x faster                                                   |
| chaos                    | 62.8 ms                                                | 59.1 ms: 1.06x faster                                                  |
| thrift                   | 791 us                                                 | 745 us: 1.06x faster                                                   |
| json_loads               | 26.5 us                                                | 25.1 us: 1.06x faster                                                  |
| regex_compile            | 142 ms                                                 | 135 ms: 1.06x faster                                                   |
| pprint_safe_repr         | 743 ms                                                 | 704 ms: 1.05x faster                                                   |
| logging_silent           | 109 ns                                                 | 104 ns: 1.05x faster                                                   |
| dulwich_log              | 78.9 ms                                                | 75.2 ms: 1.05x faster                                                  |
| deltablue                | 3.45 ms                                                | 3.29 ms: 1.05x faster                                                  |
| sqlglot_transpile        | 1.67 ms                                                | 1.60 ms: 1.05x faster                                                  |
| logging_format           | 7.35 us                                                | 7.02 us: 1.05x faster                                                  |
| sqlglot_parse            | 1.36 ms                                                | 1.30 ms: 1.04x faster                                                  |
| coroutines               | 23.9 ms                                                | 22.9 ms: 1.04x faster                                                  |
| pprint_pformat           | 1.52 sec                                               | 1.46 sec: 1.04x faster                                                 |
| typing_runtime_protocols | 163 us                                                 | 157 us: 1.04x faster                                                   |
| 2to3                     | 264 ms                                                 | 255 ms: 1.04x faster                                                   |
| hexiom                   | 6.17 ms                                                | 5.98 ms: 1.03x faster                                                  |
| sympy_integrate          | 20.5 ms                                                | 19.9 ms: 1.03x faster                                                  |
| scimark_monte_carlo      | 68.4 ms                                                | 66.4 ms: 1.03x faster                                                  |
| asyncio_tcp              | 519 ms                                                 | 504 ms: 1.03x faster                                                   |
| xml_etree_parse          | 139 ms                                                 | 135 ms: 1.03x faster                                                   |
| meteor_contest           | 104 ms                                                 | 101 ms: 1.03x faster                                                   |
| unpickle_pure_python     | 221 us                                                 | 215 us: 1.03x faster                                                   |
| unpickle                 | 14.1 us                                                | 13.7 us: 1.03x faster                                                  |
| async_generators         | 384 ms                                                 | 375 ms: 1.03x faster                                                   |
| mdp                      | 2.42 sec                                               | 2.36 sec: 1.02x faster                                                 |
| gc_traversal             | 3.46 ms                                                | 3.38 ms: 1.02x faster                                                  |
| spectral_norm            | 110 ms                                                 | 108 ms: 1.02x faster                                                   |
| pycparser                | 1.17 sec                                               | 1.14 sec: 1.02x faster                                                 |
| genshi_text              | 22.8 ms                                                | 22.4 ms: 1.02x faster                                                  |
| sympy_expand             | 468 ms                                                 | 460 ms: 1.02x faster                                                   |
| docutils                 | 2.64 sec                                               | 2.60 sec: 1.01x faster                                                 |
| richards                 | 45.9 ms                                                | 45.4 ms: 1.01x faster                                                  |
| float                    | 80.8 ms                                                | 79.8 ms: 1.01x faster                                                  |
| scimark_lu               | 114 ms                                                 | 113 ms: 1.01x faster                                                   |
| nqueens                  | 80.1 ms                                                | 79.3 ms: 1.01x faster                                                  |
| xml_etree_iterparse      | 96.7 ms                                                | 96.1 ms: 1.01x faster                                                  |
| sqlglot_optimize         | 53.3 ms                                                | 53.7 ms: 1.01x slower                                                  |
| asyncio_websockets       | 517 ms                                                 | 521 ms: 1.01x slower                                                   |
| fannkuch                 | 372 ms                                                 | 376 ms: 1.01x slower                                                   |
| pyflate                  | 448 ms                                                 | 453 ms: 1.01x slower                                                   |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.53 sec: 1.01x slower                                                 |
| django_template          | 34.7 ms                                                | 35.1 ms: 1.01x slower                                                  |
| tomli_loads              | 2.11 sec                                               | 2.13 sec: 1.01x slower                                                 |
| scimark_fft              | 342 ms                                                 | 347 ms: 1.02x slower                                                   |
| pickle_pure_python       | 308 us                                                 | 317 us: 1.03x slower                                                   |
| pickle_dict              | 31.8 us                                                | 32.8 us: 1.03x slower                                                  |
| unpickle_list            | 4.67 us                                                | 4.83 us: 1.03x slower                                                  |
| python_startup_no_site   | 7.16 ms                                                | 7.47 ms: 1.04x slower                                                  |
| scimark_sor              | 130 ms                                                 | 136 ms: 1.05x slower                                                   |
| mako                     | 11.0 ms                                                | 11.7 ms: 1.06x slower                                                  |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 4.71 ms: 1.07x slower                                                  |
| bench_thread_pool        | 941 us                                                 | 1.02 ms: 1.08x slower                                                  |
| nbody                    | 89.3 ms                                                | 96.3 ms: 1.08x slower                                                  |
| regex_dna                | 168 ms                                                 | 183 ms: 1.09x slower                                                   |
| json_dumps               | 10.4 ms                                                | 11.4 ms: 1.10x slower                                                  |
| pickle_list              | 4.77 us                                                | 5.32 us: 1.12x slower                                                  |
| python_startup           | 9.93 ms                                                | 11.1 ms: 1.12x slower                                                  |
| telco                    | 6.53 ms                                                | 7.35 ms: 1.13x slower                                                  |
| coverage                 | 71.4 ms                                                | 80.6 ms: 1.13x slower                                                  |
| pickle                   | 10.9 us                                                | 12.6 us: 1.15x slower                                                  |
| pidigits                 | 184 ms                                                 | 217 ms: 1.18x slower                                                   |
| regex_v8                 | 20.6 ms                                                | 24.6 ms: 1.20x slower                                                  |
| create_gc_cycles         | 1.09 ms                                                | 1.38 ms: 1.26x slower                                                  |
| bench_mp_pool            | 10.8 ms                                                | 63.8 ms: 5.90x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (8): sqlite_synth, xml_etree_process, xml_etree_generate, sqlglot_normalize, genshi_xml, pylint, richards_super, html5lib
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 98.71% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x