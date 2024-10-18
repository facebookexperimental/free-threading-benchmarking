# Results vs. 3.12.6

- fork: python
- ref: main
- machine: linux-x86_64
- commit hash: 2e950e3
- commit date: 2024-10-18
- overall geometric mean: 1.01x faster
- HPT reliability: 99.97%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-python-main-3.14.0a1+-2e950e3 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 253 ms: 1.04x faster                                   |
| docutils       | 2.64 sec                                               | 2.59 sec: 1.02x faster                                 |
| tornado_http   | 119 ms                                                 | 113 ms: 1.05x faster                                   |
| Geometric mean | (ref)                                                  | 1.03x faster                                           |

Benchmark hidden because not significant (1): html5lib

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-python-main-3.14.0a1+-2e950e3 |
|--------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| coroutines         | 23.9 ms                                                | 22.3 ms: 1.08x faster                                  |
| async_generators   | 384 ms                                                 | 369 ms: 1.04x faster                                   |
| asyncio_tcp        | 519 ms                                                 | 503 ms: 1.03x faster                                   |
| asyncio_websockets | 517 ms                                                 | 521 ms: 1.01x slower                                   |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.52 sec: 1.01x slower                                 |
| Geometric mean     | (ref)                                                  | 1.03x faster                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-python-main-3.14.0a1+-2e950e3 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| float          | 80.8 ms                                                | 78.1 ms: 1.03x faster                                  |
| pidigits       | 184 ms                                                 | 185 ms: 1.00x slower                                   |
| nbody          | 89.3 ms                                                | 92.4 ms: 1.04x slower                                  |
| Geometric mean | (ref)                                                  | 1.00x slower                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-python-main-3.14.0a1+-2e950e3 |
|----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 129 ms: 1.10x faster                                   |
| regex_effbot   | 3.17 ms                                                | 3.28 ms: 1.04x slower                                  |
| regex_dna      | 168 ms                                                 | 179 ms: 1.07x slower                                   |
| regex_v8       | 20.6 ms                                                | 23.1 ms: 1.12x slower                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-python-main-3.14.0a1+-2e950e3 |
|----------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| unpickle_pure_python | 221 us                                                 | 215 us: 1.03x faster                                   |
| unpickle_list        | 4.67 us                                                | 4.58 us: 1.02x faster                                  |
| json_loads           | 26.5 us                                                | 26.1 us: 1.02x faster                                  |
| xml_etree_parse      | 139 ms                                                 | 136 ms: 1.02x faster                                   |
| pickle_pure_python   | 308 us                                                 | 305 us: 1.01x faster                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 96.1 ms: 1.01x faster                                  |
| tomli_loads          | 2.11 sec                                               | 2.09 sec: 1.01x faster                                 |
| xml_etree_generate   | 85.2 ms                                                | 84.8 ms: 1.00x faster                                  |
| pickle_list          | 4.77 us                                                | 4.84 us: 1.02x slower                                  |
| pickle_dict          | 31.8 us                                                | 32.7 us: 1.03x slower                                  |
| pickle               | 10.9 us                                                | 11.3 us: 1.03x slower                                  |
| json_dumps           | 10.4 ms                                                | 11.6 ms: 1.12x slower                                  |
| Geometric mean       | (ref)                                                  | 1.00x slower                                           |

Benchmark hidden because not significant (2): unpickle, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-python-main-3.14.0a1+-2e950e3 |
|------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.41 ms: 1.03x slower                                  |
| python_startup         | 9.93 ms                                                | 11.0 ms: 1.11x slower                                  |
| Geometric mean         | (ref)                                                  | 1.07x slower                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-python-main-3.14.0a1+-2e950e3 |
|-----------------|:------------------------------------------------------:|:------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.4 ms: 1.02x faster                                  |
| genshi_xml      | 50.2 ms                                                | 49.7 ms: 1.01x faster                                  |
| django_template | 34.7 ms                                                | 35.8 ms: 1.03x slower                                  |
| mako            | 11.0 ms                                                | 11.7 ms: 1.06x slower                                  |
| Geometric mean  | (ref)                                                  | 1.02x slower                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241018-vultr-x86_64-python-main-3.14.0a1+-2e950e3 |
|--------------------------|:------------------------------------------------------:|:------------------------------------------------------:|
| deepcopy                 | 352 us                                                 | 262 us: 1.34x faster                                   |
| deepcopy_memo            | 40.3 us                                                | 30.0 us: 1.34x faster                                  |
| go                       | 139 ms                                                 | 119 ms: 1.17x faster                                   |
| comprehensions           | 19.8 us                                                | 16.9 us: 1.17x faster                                  |
| pathlib                  | 21.5 ms                                                | 18.5 ms: 1.17x faster                                  |
| deepcopy_reduce          | 3.08 us                                                | 2.65 us: 1.16x faster                                  |
| raytrace                 | 299 ms                                                 | 259 ms: 1.15x faster                                   |
| crypto_pyaes             | 76.6 ms                                                | 66.4 ms: 1.15x faster                                  |
| unpack_sequence          | 52.1 ns                                                | 45.6 ns: 1.14x faster                                  |
| generators               | 32.2 ms                                                | 28.9 ms: 1.12x faster                                  |
| regex_compile            | 142 ms                                                 | 129 ms: 1.10x faster                                   |
| logging_simple           | 6.63 us                                                | 6.02 us: 1.10x faster                                  |
| logging_format           | 7.35 us                                                | 6.72 us: 1.09x faster                                  |
| bpe_tokeniser            | 4.74 sec                                               | 4.34 sec: 1.09x faster                                 |
| sympy_sum                | 166 ms                                                 | 154 ms: 1.08x faster                                   |
| coroutines               | 23.9 ms                                                | 22.3 ms: 1.08x faster                                  |
| deltablue                | 3.45 ms                                                | 3.22 ms: 1.07x faster                                  |
| sympy_str                | 292 ms                                                 | 273 ms: 1.07x faster                                   |
| chaos                    | 62.8 ms                                                | 58.8 ms: 1.07x faster                                  |
| dulwich_log              | 78.9 ms                                                | 74.3 ms: 1.06x faster                                  |
| scimark_monte_carlo      | 68.4 ms                                                | 64.8 ms: 1.06x faster                                  |
| gc_traversal             | 3.46 ms                                                | 3.28 ms: 1.05x faster                                  |
| sqlglot_parse            | 1.36 ms                                                | 1.29 ms: 1.05x faster                                  |
| sqlglot_transpile        | 1.67 ms                                                | 1.59 ms: 1.05x faster                                  |
| tornado_http             | 119 ms                                                 | 113 ms: 1.05x faster                                   |
| typing_runtime_protocols | 163 us                                                 | 155 us: 1.05x faster                                   |
| hexiom                   | 6.17 ms                                                | 5.88 ms: 1.05x faster                                  |
| pprint_safe_repr         | 743 ms                                                 | 709 ms: 1.05x faster                                   |
| async_generators         | 384 ms                                                 | 369 ms: 1.04x faster                                   |
| thrift                   | 791 us                                                 | 759 us: 1.04x faster                                   |
| scimark_lu               | 114 ms                                                 | 109 ms: 1.04x faster                                   |
| pycparser                | 1.17 sec                                               | 1.12 sec: 1.04x faster                                 |
| 2to3                     | 264 ms                                                 | 253 ms: 1.04x faster                                   |
| json                     | 5.02 ms                                                | 4.83 ms: 1.04x faster                                  |
| logging_silent           | 109 ns                                                 | 105 ns: 1.04x faster                                   |
| mdp                      | 2.42 sec                                               | 2.34 sec: 1.03x faster                                 |
| pprint_pformat           | 1.52 sec                                               | 1.47 sec: 1.03x faster                                 |
| float                    | 80.8 ms                                                | 78.1 ms: 1.03x faster                                  |
| asyncio_tcp              | 519 ms                                                 | 503 ms: 1.03x faster                                   |
| sympy_integrate          | 20.5 ms                                                | 20.0 ms: 1.03x faster                                  |
| unpickle_pure_python     | 221 us                                                 | 215 us: 1.03x faster                                   |
| scimark_fft              | 342 ms                                                 | 333 ms: 1.03x faster                                   |
| unpickle_list            | 4.67 us                                                | 4.58 us: 1.02x faster                                  |
| genshi_text              | 22.8 ms                                                | 22.4 ms: 1.02x faster                                  |
| sympy_expand             | 468 ms                                                 | 458 ms: 1.02x faster                                   |
| richards_super           | 51.9 ms                                                | 50.9 ms: 1.02x faster                                  |
| nqueens                  | 80.1 ms                                                | 78.6 ms: 1.02x faster                                  |
| docutils                 | 2.64 sec                                               | 2.59 sec: 1.02x faster                                 |
| json_loads               | 26.5 us                                                | 26.1 us: 1.02x faster                                  |
| xml_etree_parse          | 139 ms                                                 | 136 ms: 1.02x faster                                   |
| richards                 | 45.9 ms                                                | 45.3 ms: 1.02x faster                                  |
| meteor_contest           | 104 ms                                                 | 102 ms: 1.01x faster                                   |
| spectral_norm            | 110 ms                                                 | 109 ms: 1.01x faster                                   |
| genshi_xml               | 50.2 ms                                                | 49.7 ms: 1.01x faster                                  |
| pickle_pure_python       | 308 us                                                 | 305 us: 1.01x faster                                   |
| xml_etree_iterparse      | 96.7 ms                                                | 96.1 ms: 1.01x faster                                  |
| tomli_loads              | 2.11 sec                                               | 2.09 sec: 1.01x faster                                 |
| xml_etree_generate       | 85.2 ms                                                | 84.8 ms: 1.00x faster                                  |
| pidigits                 | 184 ms                                                 | 185 ms: 1.00x slower                                   |
| pyflate                  | 448 ms                                                 | 450 ms: 1.00x slower                                   |
| sqlglot_optimize         | 53.3 ms                                                | 53.6 ms: 1.01x slower                                  |
| asyncio_websockets       | 517 ms                                                 | 521 ms: 1.01x slower                                   |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.52 sec: 1.01x slower                                 |
| pickle_list              | 4.77 us                                                | 4.84 us: 1.02x slower                                  |
| fannkuch                 | 372 ms                                                 | 379 ms: 1.02x slower                                   |
| pickle_dict              | 31.8 us                                                | 32.7 us: 1.03x slower                                  |
| scimark_sor              | 130 ms                                                 | 133 ms: 1.03x slower                                   |
| django_template          | 34.7 ms                                                | 35.8 ms: 1.03x slower                                  |
| pickle                   | 10.9 us                                                | 11.3 us: 1.03x slower                                  |
| python_startup_no_site   | 7.16 ms                                                | 7.41 ms: 1.03x slower                                  |
| nbody                    | 89.3 ms                                                | 92.4 ms: 1.04x slower                                  |
| regex_effbot             | 3.17 ms                                                | 3.28 ms: 1.04x slower                                  |
| mako                     | 11.0 ms                                                | 11.7 ms: 1.06x slower                                  |
| regex_dna                | 168 ms                                                 | 179 ms: 1.07x slower                                   |
| bench_thread_pool        | 941 us                                                 | 1.01 ms: 1.07x slower                                  |
| python_startup           | 9.93 ms                                                | 11.0 ms: 1.11x slower                                  |
| json_dumps               | 10.4 ms                                                | 11.6 ms: 1.12x slower                                  |
| telco                    | 6.53 ms                                                | 7.32 ms: 1.12x slower                                  |
| regex_v8                 | 20.6 ms                                                | 23.1 ms: 1.12x slower                                  |
| coverage                 | 71.4 ms                                                | 82.2 ms: 1.15x slower                                  |
| create_gc_cycles         | 1.09 ms                                                | 1.38 ms: 1.26x slower                                  |
| bench_mp_pool            | 10.8 ms                                                | 63.3 ms: 5.87x slower                                  |
| Geometric mean           | (ref)                                                  | 1.01x faster                                           |

Benchmark hidden because not significant (7): unpickle, html5lib, scimark_sparse_mat_mult, sqlglot_normalize, pylint, xml_etree_process, sqlite_synth
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.97% likely to be faster
- 90% likely to have a speedup of 1.01x
- 95% likely to have a speedup of 1.01x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x