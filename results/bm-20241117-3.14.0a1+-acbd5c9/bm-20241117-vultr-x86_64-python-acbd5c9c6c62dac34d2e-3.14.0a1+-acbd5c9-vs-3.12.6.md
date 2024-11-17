# Results vs. 3.12.6

- fork: python
- ref: acbd5c9c6c62dac34d2e
- machine: linux-x86_64
- commit hash: acbd5c9
- commit date: 2024-11-17
- overall geometric mean: 1.00x slower
- HPT reliability: 99.25%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 254 ms: 1.04x faster                                                   |
| docutils       | 2.64 sec                                               | 2.61 sec: 1.01x faster                                                 |
| html5lib       | 63.6 ms                                                | 64.9 ms: 1.02x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|--------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| coroutines         | 23.9 ms                                                | 22.5 ms: 1.06x faster                                                  |
| asyncio_tcp        | 519 ms                                                 | 507 ms: 1.02x faster                                                   |
| async_generators   | 384 ms                                                 | 376 ms: 1.02x faster                                                   |
| asyncio_websockets | 517 ms                                                 | 521 ms: 1.01x slower                                                   |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.52 sec: 1.01x slower                                                 |
| Geometric mean     | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 79.0 ms: 1.02x faster                                                  |
| pidigits       | 184 ms                                                 | 185 ms: 1.01x slower                                                   |
| nbody          | 89.3 ms                                                | 93.3 ms: 1.05x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 131 ms: 1.08x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 3.27 ms: 1.03x slower                                                  |
| regex_dna      | 168 ms                                                 | 182 ms: 1.09x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.0 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.04x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| json_loads           | 26.5 us                                                | 25.0 us: 1.06x faster                                                  |
| unpickle             | 14.1 us                                                | 13.3 us: 1.05x faster                                                  |
| unpickle_pure_python | 221 us                                                 | 215 us: 1.03x faster                                                   |
| xml_etree_parse      | 139 ms                                                 | 136 ms: 1.02x faster                                                   |
| pickle_dict          | 31.8 us                                                | 31.2 us: 1.02x faster                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 95.4 ms: 1.01x faster                                                  |
| xml_etree_process    | 59.0 ms                                                | 59.8 ms: 1.01x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 86.6 ms: 1.02x slower                                                  |
| pickle_pure_python   | 308 us                                                 | 319 us: 1.04x slower                                                   |
| pickle_list          | 4.77 us                                                | 5.10 us: 1.07x slower                                                  |
| pickle               | 10.9 us                                                | 12.1 us: 1.11x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.6 ms: 1.12x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (2): tomli_loads, unpickle_list

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.44 ms: 1.04x slower                                                  |
| python_startup         | 9.93 ms                                                | 11.0 ms: 1.11x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.3 ms: 1.02x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 50.9 ms: 1.01x slower                                                  |
| django_template | 34.7 ms                                                | 36.1 ms: 1.04x slower                                                  |
| mako            | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.03x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy_memo            | 40.3 us                                                | 29.8 us: 1.35x faster                                                  |
| deepcopy                 | 352 us                                                 | 261 us: 1.35x faster                                                   |
| unpack_sequence          | 52.1 ns                                                | 43.9 ns: 1.18x faster                                                  |
| pathlib                  | 21.5 ms                                                | 18.4 ms: 1.17x faster                                                  |
| comprehensions           | 19.8 us                                                | 17.0 us: 1.17x faster                                                  |
| go                       | 139 ms                                                 | 121 ms: 1.16x faster                                                   |
| raytrace                 | 299 ms                                                 | 260 ms: 1.15x faster                                                   |
| crypto_pyaes             | 76.6 ms                                                | 66.6 ms: 1.15x faster                                                  |
| deepcopy_reduce          | 3.08 us                                                | 2.73 us: 1.13x faster                                                  |
| generators               | 32.2 ms                                                | 28.8 ms: 1.12x faster                                                  |
| bpe_tokeniser            | 4.74 sec                                               | 4.32 sec: 1.10x faster                                                 |
| sympy_sum                | 166 ms                                                 | 153 ms: 1.09x faster                                                   |
| regex_compile            | 142 ms                                                 | 131 ms: 1.08x faster                                                   |
| deltablue                | 3.45 ms                                                | 3.20 ms: 1.08x faster                                                  |
| json                     | 5.02 ms                                                | 4.67 ms: 1.08x faster                                                  |
| logging_simple           | 6.63 us                                                | 6.19 us: 1.07x faster                                                  |
| logging_format           | 7.35 us                                                | 6.87 us: 1.07x faster                                                  |
| sympy_str                | 292 ms                                                 | 273 ms: 1.07x faster                                                   |
| chaos                    | 62.8 ms                                                | 58.9 ms: 1.07x faster                                                  |
| coroutines               | 23.9 ms                                                | 22.5 ms: 1.06x faster                                                  |
| json_loads               | 26.5 us                                                | 25.0 us: 1.06x faster                                                  |
| logging_silent           | 109 ns                                                 | 103 ns: 1.06x faster                                                   |
| thrift                   | 791 us                                                 | 749 us: 1.06x faster                                                   |
| scimark_monte_carlo      | 68.4 ms                                                | 64.8 ms: 1.06x faster                                                  |
| unpickle                 | 14.1 us                                                | 13.3 us: 1.05x faster                                                  |
| hexiom                   | 6.17 ms                                                | 5.92 ms: 1.04x faster                                                  |
| sqlglot_transpile        | 1.67 ms                                                | 1.60 ms: 1.04x faster                                                  |
| sqlglot_parse            | 1.36 ms                                                | 1.30 ms: 1.04x faster                                                  |
| dulwich_log              | 78.9 ms                                                | 76.0 ms: 1.04x faster                                                  |
| 2to3                     | 264 ms                                                 | 254 ms: 1.04x faster                                                   |
| pprint_safe_repr         | 743 ms                                                 | 716 ms: 1.04x faster                                                   |
| meteor_contest           | 104 ms                                                 | 99.9 ms: 1.04x faster                                                  |
| sympy_integrate          | 20.5 ms                                                | 19.9 ms: 1.03x faster                                                  |
| pycparser                | 1.17 sec                                               | 1.14 sec: 1.03x faster                                                 |
| typing_runtime_protocols | 163 us                                                 | 159 us: 1.03x faster                                                   |
| mdp                      | 2.42 sec                                               | 2.35 sec: 1.03x faster                                                 |
| unpickle_pure_python     | 221 us                                                 | 215 us: 1.03x faster                                                   |
| pprint_pformat           | 1.52 sec                                               | 1.48 sec: 1.03x faster                                                 |
| asyncio_tcp              | 519 ms                                                 | 507 ms: 1.02x faster                                                   |
| float                    | 80.8 ms                                                | 79.0 ms: 1.02x faster                                                  |
| async_generators         | 384 ms                                                 | 376 ms: 1.02x faster                                                   |
| genshi_text              | 22.8 ms                                                | 22.3 ms: 1.02x faster                                                  |
| xml_etree_parse          | 139 ms                                                 | 136 ms: 1.02x faster                                                   |
| pickle_dict              | 31.8 us                                                | 31.2 us: 1.02x faster                                                  |
| xml_etree_iterparse      | 96.7 ms                                                | 95.4 ms: 1.01x faster                                                  |
| docutils                 | 2.64 sec                                               | 2.61 sec: 1.01x faster                                                 |
| sympy_expand             | 468 ms                                                 | 463 ms: 1.01x faster                                                   |
| pyflate                  | 448 ms                                                 | 445 ms: 1.01x faster                                                   |
| pidigits                 | 184 ms                                                 | 185 ms: 1.01x slower                                                   |
| spectral_norm            | 110 ms                                                 | 111 ms: 1.01x slower                                                   |
| asyncio_websockets       | 517 ms                                                 | 521 ms: 1.01x slower                                                   |
| fannkuch                 | 372 ms                                                 | 375 ms: 1.01x slower                                                   |
| sqlglot_optimize         | 53.3 ms                                                | 53.8 ms: 1.01x slower                                                  |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.52 sec: 1.01x slower                                                 |
| sqlite_synth             | 2.20 us                                                | 2.23 us: 1.01x slower                                                  |
| xml_etree_process        | 59.0 ms                                                | 59.8 ms: 1.01x slower                                                  |
| genshi_xml               | 50.2 ms                                                | 50.9 ms: 1.01x slower                                                  |
| xml_etree_generate       | 85.2 ms                                                | 86.6 ms: 1.02x slower                                                  |
| html5lib                 | 63.6 ms                                                | 64.9 ms: 1.02x slower                                                  |
| regex_effbot             | 3.17 ms                                                | 3.27 ms: 1.03x slower                                                  |
| pickle_pure_python       | 308 us                                                 | 319 us: 1.04x slower                                                   |
| python_startup_no_site   | 7.16 ms                                                | 7.44 ms: 1.04x slower                                                  |
| django_template          | 34.7 ms                                                | 36.1 ms: 1.04x slower                                                  |
| scimark_sor              | 130 ms                                                 | 135 ms: 1.04x slower                                                   |
| nbody                    | 89.3 ms                                                | 93.3 ms: 1.05x slower                                                  |
| pickle_list              | 4.77 us                                                | 5.10 us: 1.07x slower                                                  |
| mako                     | 11.0 ms                                                | 11.8 ms: 1.07x slower                                                  |
| gc_traversal             | 3.46 ms                                                | 3.71 ms: 1.07x slower                                                  |
| bench_thread_pool        | 941 us                                                 | 1.02 ms: 1.08x slower                                                  |
| regex_dna                | 168 ms                                                 | 182 ms: 1.09x slower                                                   |
| pickle                   | 10.9 us                                                | 12.1 us: 1.11x slower                                                  |
| python_startup           | 9.93 ms                                                | 11.0 ms: 1.11x slower                                                  |
| regex_v8                 | 20.6 ms                                                | 23.0 ms: 1.12x slower                                                  |
| telco                    | 6.53 ms                                                | 7.30 ms: 1.12x slower                                                  |
| json_dumps               | 10.4 ms                                                | 11.6 ms: 1.12x slower                                                  |
| coverage                 | 71.4 ms                                                | 81.2 ms: 1.14x slower                                                  |
| create_gc_cycles         | 1.09 ms                                                | 1.36 ms: 1.24x slower                                                  |
| bench_mp_pool            | 10.8 ms                                                | 63.7 ms: 5.90x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (10): richards, richards_super, tomli_loads, scimark_fft, unpickle_list, pylint, nqueens, sqlglot_normalize, scimark_lu, scimark_sparse_mat_mult
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 99.25% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x