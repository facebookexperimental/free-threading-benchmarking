# Results vs. 3.12.6

- fork: python
- ref: ac3a2c8abceeec448486
- machine: linux-x86_64
- commit hash: ac3a2c8
- commit date: 2024-10-31
- overall geometric mean: 1.00x slower
- HPT reliability: 99.33%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 254 ms: 1.04x faster                                                   |
| docutils       | 2.64 sec                                               | 2.60 sec: 1.01x faster                                                 |
| html5lib       | 63.6 ms                                                | 65.3 ms: 1.03x slower                                                  |
| tornado_http   | 119 ms                                                 | 114 ms: 1.04x faster                                                   |
| Geometric mean | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|--------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_generators   | 384 ms                                                 | 372 ms: 1.03x faster                                                   |
| asyncio_tcp        | 519 ms                                                 | 506 ms: 1.02x faster                                                   |
| coroutines         | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                  |
| asyncio_websockets | 517 ms                                                 | 521 ms: 1.01x slower                                                   |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.52 sec: 1.01x slower                                                 |
| Geometric mean     | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 80.8 ms                                                | 80.1 ms: 1.01x faster                                                  |
| nbody          | 89.3 ms                                                | 94.7 ms: 1.06x slower                                                  |
| pidigits       | 184 ms                                                 | 218 ms: 1.18x slower                                                   |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 131 ms: 1.08x faster                                                   |
| regex_effbot   | 3.17 ms                                                | 3.27 ms: 1.03x slower                                                  |
| regex_dna      | 168 ms                                                 | 180 ms: 1.07x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.1 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle             | 14.1 us                                                | 13.4 us: 1.05x faster                                                  |
| pickle_dict          | 31.8 us                                                | 30.5 us: 1.04x faster                                                  |
| json_loads           | 26.5 us                                                | 26.0 us: 1.02x faster                                                  |
| xml_etree_parse      | 139 ms                                                 | 136 ms: 1.02x faster                                                   |
| unpickle_pure_python | 221 us                                                 | 217 us: 1.02x faster                                                   |
| xml_etree_iterparse  | 96.7 ms                                                | 95.7 ms: 1.01x faster                                                  |
| xml_etree_generate   | 85.2 ms                                                | 84.6 ms: 1.01x faster                                                  |
| tomli_loads          | 2.11 sec                                               | 2.09 sec: 1.01x faster                                                 |
| unpickle_list        | 4.67 us                                                | 4.66 us: 1.00x faster                                                  |
| pickle_list          | 4.77 us                                                | 4.90 us: 1.03x slower                                                  |
| json_dumps           | 10.4 ms                                                | 11.5 ms: 1.11x slower                                                  |
| Geometric mean       | (ref)                                                  | 1.00x faster                                                           |

Benchmark hidden because not significant (3): pickle, pickle_pure_python, xml_etree_process

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.45 ms: 1.04x slower                                                  |
| python_startup         | 9.93 ms                                                | 11.1 ms: 1.12x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.08x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.3 ms: 1.02x faster                                                  |
| django_template | 34.7 ms                                                | 35.2 ms: 1.01x slower                                                  |
| mako            | 11.0 ms                                                | 11.7 ms: 1.07x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (1): genshi_xml

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241031-vultr-x86_64-python-ac3a2c8abceeec448486-3.14.0a1+-ac3a2c8 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy_memo            | 40.3 us                                                | 30.1 us: 1.34x faster                                                  |
| deepcopy                 | 352 us                                                 | 266 us: 1.32x faster                                                   |
| pathlib                  | 21.5 ms                                                | 18.4 ms: 1.17x faster                                                  |
| deepcopy_reduce          | 3.08 us                                                | 2.64 us: 1.16x faster                                                  |
| comprehensions           | 19.8 us                                                | 17.1 us: 1.16x faster                                                  |
| go                       | 139 ms                                                 | 120 ms: 1.16x faster                                                   |
| crypto_pyaes             | 76.6 ms                                                | 67.2 ms: 1.14x faster                                                  |
| raytrace                 | 299 ms                                                 | 264 ms: 1.13x faster                                                   |
| logging_simple           | 6.63 us                                                | 6.01 us: 1.10x faster                                                  |
| generators               | 32.2 ms                                                | 29.3 ms: 1.10x faster                                                  |
| regex_compile            | 142 ms                                                 | 131 ms: 1.08x faster                                                   |
| logging_format           | 7.35 us                                                | 6.80 us: 1.08x faster                                                  |
| gc_traversal             | 3.46 ms                                                | 3.20 ms: 1.08x faster                                                  |
| bpe_tokeniser            | 4.74 sec                                               | 4.39 sec: 1.08x faster                                                 |
| chaos                    | 62.8 ms                                                | 58.5 ms: 1.07x faster                                                  |
| sympy_str                | 292 ms                                                 | 272 ms: 1.07x faster                                                   |
| sympy_sum                | 166 ms                                                 | 155 ms: 1.07x faster                                                   |
| deltablue                | 3.45 ms                                                | 3.24 ms: 1.06x faster                                                  |
| unpickle                 | 14.1 us                                                | 13.4 us: 1.05x faster                                                  |
| thrift                   | 791 us                                                 | 757 us: 1.05x faster                                                   |
| scimark_monte_carlo      | 68.4 ms                                                | 65.5 ms: 1.04x faster                                                  |
| tornado_http             | 119 ms                                                 | 114 ms: 1.04x faster                                                   |
| pickle_dict              | 31.8 us                                                | 30.5 us: 1.04x faster                                                  |
| logging_silent           | 109 ns                                                 | 105 ns: 1.04x faster                                                   |
| hexiom                   | 6.17 ms                                                | 5.92 ms: 1.04x faster                                                  |
| dulwich_log              | 78.9 ms                                                | 75.7 ms: 1.04x faster                                                  |
| sqlglot_transpile        | 1.67 ms                                                | 1.61 ms: 1.04x faster                                                  |
| pprint_safe_repr         | 743 ms                                                 | 715 ms: 1.04x faster                                                   |
| 2to3                     | 264 ms                                                 | 254 ms: 1.04x faster                                                   |
| sqlglot_parse            | 1.36 ms                                                | 1.30 ms: 1.04x faster                                                  |
| unpack_sequence          | 52.1 ns                                                | 50.1 ns: 1.04x faster                                                  |
| async_generators         | 384 ms                                                 | 372 ms: 1.03x faster                                                   |
| pycparser                | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                 |
| scimark_lu               | 114 ms                                                 | 111 ms: 1.03x faster                                                   |
| pprint_pformat           | 1.52 sec                                               | 1.47 sec: 1.03x faster                                                 |
| sympy_integrate          | 20.5 ms                                                | 19.9 ms: 1.03x faster                                                  |
| typing_runtime_protocols | 163 us                                                 | 159 us: 1.03x faster                                                   |
| meteor_contest           | 104 ms                                                 | 101 ms: 1.03x faster                                                   |
| asyncio_tcp              | 519 ms                                                 | 506 ms: 1.02x faster                                                   |
| json_loads               | 26.5 us                                                | 26.0 us: 1.02x faster                                                  |
| genshi_text              | 22.8 ms                                                | 22.3 ms: 1.02x faster                                                  |
| nqueens                  | 80.1 ms                                                | 78.5 ms: 1.02x faster                                                  |
| xml_etree_parse          | 139 ms                                                 | 136 ms: 1.02x faster                                                   |
| unpickle_pure_python     | 221 us                                                 | 217 us: 1.02x faster                                                   |
| json                     | 5.02 ms                                                | 4.94 ms: 1.02x faster                                                  |
| sympy_expand             | 468 ms                                                 | 461 ms: 1.02x faster                                                   |
| docutils                 | 2.64 sec                                               | 2.60 sec: 1.01x faster                                                 |
| coroutines               | 23.9 ms                                                | 23.7 ms: 1.01x faster                                                  |
| xml_etree_iterparse      | 96.7 ms                                                | 95.7 ms: 1.01x faster                                                  |
| float                    | 80.8 ms                                                | 80.1 ms: 1.01x faster                                                  |
| xml_etree_generate       | 85.2 ms                                                | 84.6 ms: 1.01x faster                                                  |
| tomli_loads              | 2.11 sec                                               | 2.09 sec: 1.01x faster                                                 |
| sqlite_synth             | 2.20 us                                                | 2.19 us: 1.01x faster                                                  |
| unpickle_list            | 4.67 us                                                | 4.66 us: 1.00x faster                                                  |
| sqlglot_normalize        | 107 ms                                                 | 107 ms: 1.01x slower                                                   |
| asyncio_websockets       | 517 ms                                                 | 521 ms: 1.01x slower                                                   |
| sqlglot_optimize         | 53.3 ms                                                | 53.7 ms: 1.01x slower                                                  |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.52 sec: 1.01x slower                                                 |
| django_template          | 34.7 ms                                                | 35.2 ms: 1.01x slower                                                  |
| html5lib                 | 63.6 ms                                                | 65.3 ms: 1.03x slower                                                  |
| pickle_list              | 4.77 us                                                | 4.90 us: 1.03x slower                                                  |
| regex_effbot             | 3.17 ms                                                | 3.27 ms: 1.03x slower                                                  |
| mdp                      | 2.42 sec                                               | 2.50 sec: 1.03x slower                                                 |
| python_startup_no_site   | 7.16 ms                                                | 7.45 ms: 1.04x slower                                                  |
| scimark_sor              | 130 ms                                                 | 136 ms: 1.05x slower                                                   |
| spectral_norm            | 110 ms                                                 | 116 ms: 1.05x slower                                                   |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 4.63 ms: 1.05x slower                                                  |
| nbody                    | 89.3 ms                                                | 94.7 ms: 1.06x slower                                                  |
| mako                     | 11.0 ms                                                | 11.7 ms: 1.07x slower                                                  |
| regex_dna                | 168 ms                                                 | 180 ms: 1.07x slower                                                   |
| bench_thread_pool        | 941 us                                                 | 1.01 ms: 1.07x slower                                                  |
| json_dumps               | 10.4 ms                                                | 11.5 ms: 1.11x slower                                                  |
| python_startup           | 9.93 ms                                                | 11.1 ms: 1.12x slower                                                  |
| regex_v8                 | 20.6 ms                                                | 23.1 ms: 1.12x slower                                                  |
| telco                    | 6.53 ms                                                | 7.34 ms: 1.13x slower                                                  |
| coverage                 | 71.4 ms                                                | 81.3 ms: 1.14x slower                                                  |
| pidigits                 | 184 ms                                                 | 218 ms: 1.18x slower                                                   |
| create_gc_cycles         | 1.09 ms                                                | 1.38 ms: 1.26x slower                                                  |
| bench_mp_pool            | 10.8 ms                                                | 63.7 ms: 5.90x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.00x slower                                                           |

Benchmark hidden because not significant (10): pickle, scimark_fft, pyflate, pickle_pure_python, richards, genshi_xml, richards_super, fannkuch, pylint, xml_etree_process
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 99.33% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x