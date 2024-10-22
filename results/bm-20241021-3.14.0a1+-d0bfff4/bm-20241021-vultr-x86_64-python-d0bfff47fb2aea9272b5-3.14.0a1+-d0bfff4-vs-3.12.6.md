# Results vs. 3.12.6

- fork: python
- ref: d0bfff47fb2aea9272b5
- machine: linux-x86_64
- commit hash: d0bfff4
- commit date: 2024-10-21
- overall geometric mean: 1.01x slower
- HPT reliability: 80.88%
- HPT 99th percentile: 1.00x faster
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 254 ms: 1.04x faster                                                   |
| docutils       | 2.64 sec                                               | 2.63 sec: 1.00x faster                                                 |
| html5lib       | 63.6 ms                                                | 65.7 ms: 1.03x slower                                                  |
| tornado_http   | 119 ms                                                 | 114 ms: 1.05x faster                                                   |
| Geometric mean | (ref)                                                  | 1.01x faster                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|--------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| coroutines         | 23.9 ms                                                | 22.3 ms: 1.07x faster                                                  |
| async_generators   | 384 ms                                                 | 374 ms: 1.03x faster                                                   |
| asyncio_tcp        | 519 ms                                                 | 505 ms: 1.03x faster                                                   |
| asyncio_websockets | 517 ms                                                 | 520 ms: 1.01x slower                                                   |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.52 sec: 1.01x slower                                                 |
| Geometric mean     | (ref)                                                  | 1.02x faster                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 186 ms: 1.01x slower                                                   |
| nbody          | 89.3 ms                                                | 98.0 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.03x slower                                                           |

Benchmark hidden because not significant (1): float

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_compile  | 142 ms                                                 | 130 ms: 1.09x faster                                                   |
| regex_dna      | 168 ms                                                 | 174 ms: 1.04x slower                                                   |
| regex_v8       | 20.6 ms                                                | 23.0 ms: 1.12x slower                                                  |
| Geometric mean | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark           | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|---------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| unpickle            | 14.1 us                                                | 13.6 us: 1.03x faster                                                  |
| json_loads          | 26.5 us                                                | 26.2 us: 1.01x faster                                                  |
| xml_etree_parse     | 139 ms                                                 | 137 ms: 1.01x faster                                                   |
| xml_etree_iterparse | 96.7 ms                                                | 96.1 ms: 1.01x faster                                                  |
| tomli_loads         | 2.11 sec                                               | 2.12 sec: 1.01x slower                                                 |
| pickle_pure_python  | 308 us                                                 | 310 us: 1.01x slower                                                   |
| pickle_dict         | 31.8 us                                                | 32.3 us: 1.02x slower                                                  |
| xml_etree_generate  | 85.2 ms                                                | 86.6 ms: 1.02x slower                                                  |
| pickle_list         | 4.77 us                                                | 4.88 us: 1.02x slower                                                  |
| xml_etree_process   | 59.0 ms                                                | 60.6 ms: 1.03x slower                                                  |
| pickle              | 10.9 us                                                | 11.3 us: 1.03x slower                                                  |
| json_dumps          | 10.4 ms                                                | 11.7 ms: 1.13x slower                                                  |
| Geometric mean      | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (2): unpickle_list, unpickle_pure_python

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 7.42 ms: 1.04x slower                                                  |
| python_startup         | 9.93 ms                                                | 11.0 ms: 1.11x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_text     | 22.8 ms                                                | 22.5 ms: 1.01x faster                                                  |
| genshi_xml      | 50.2 ms                                                | 51.3 ms: 1.02x slower                                                  |
| django_template | 34.7 ms                                                | 35.9 ms: 1.04x slower                                                  |
| mako            | 11.0 ms                                                | 12.1 ms: 1.10x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.04x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-vultr-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| deepcopy                 | 352 us                                                 | 264 us: 1.33x faster                                                   |
| deepcopy_memo            | 40.3 us                                                | 31.2 us: 1.29x faster                                                  |
| pathlib                  | 21.5 ms                                                | 18.4 ms: 1.17x faster                                                  |
| comprehensions           | 19.8 us                                                | 17.0 us: 1.16x faster                                                  |
| deepcopy_reduce          | 3.08 us                                                | 2.66 us: 1.16x faster                                                  |
| go                       | 139 ms                                                 | 122 ms: 1.14x faster                                                   |
| crypto_pyaes             | 76.6 ms                                                | 67.6 ms: 1.13x faster                                                  |
| unpack_sequence          | 52.1 ns                                                | 46.8 ns: 1.11x faster                                                  |
| raytrace                 | 299 ms                                                 | 271 ms: 1.11x faster                                                   |
| generators               | 32.2 ms                                                | 29.4 ms: 1.10x faster                                                  |
| regex_compile            | 142 ms                                                 | 130 ms: 1.09x faster                                                   |
| logging_simple           | 6.63 us                                                | 6.14 us: 1.08x faster                                                  |
| bpe_tokeniser            | 4.74 sec                                               | 4.41 sec: 1.07x faster                                                 |
| coroutines               | 23.9 ms                                                | 22.3 ms: 1.07x faster                                                  |
| logging_format           | 7.35 us                                                | 6.85 us: 1.07x faster                                                  |
| sympy_sum                | 166 ms                                                 | 156 ms: 1.06x faster                                                   |
| gc_traversal             | 3.46 ms                                                | 3.25 ms: 1.06x faster                                                  |
| sympy_str                | 292 ms                                                 | 275 ms: 1.06x faster                                                   |
| dulwich_log              | 78.9 ms                                                | 75.3 ms: 1.05x faster                                                  |
| tornado_http             | 119 ms                                                 | 114 ms: 1.05x faster                                                   |
| deltablue                | 3.45 ms                                                | 3.29 ms: 1.05x faster                                                  |
| chaos                    | 62.8 ms                                                | 60.1 ms: 1.05x faster                                                  |
| thrift                   | 791 us                                                 | 759 us: 1.04x faster                                                   |
| json                     | 5.02 ms                                                | 4.83 ms: 1.04x faster                                                  |
| 2to3                     | 264 ms                                                 | 254 ms: 1.04x faster                                                   |
| sqlglot_parse            | 1.36 ms                                                | 1.31 ms: 1.04x faster                                                  |
| sqlglot_transpile        | 1.67 ms                                                | 1.61 ms: 1.04x faster                                                  |
| unpickle                 | 14.1 us                                                | 13.6 us: 1.03x faster                                                  |
| pprint_safe_repr         | 743 ms                                                 | 720 ms: 1.03x faster                                                   |
| typing_runtime_protocols | 163 us                                                 | 158 us: 1.03x faster                                                   |
| pycparser                | 1.17 sec                                               | 1.13 sec: 1.03x faster                                                 |
| async_generators         | 384 ms                                                 | 374 ms: 1.03x faster                                                   |
| asyncio_tcp              | 519 ms                                                 | 505 ms: 1.03x faster                                                   |
| mdp                      | 2.42 sec                                               | 2.37 sec: 1.02x faster                                                 |
| pprint_pformat           | 1.52 sec                                               | 1.49 sec: 1.02x faster                                                 |
| scimark_monte_carlo      | 68.4 ms                                                | 67.3 ms: 1.02x faster                                                  |
| sympy_integrate          | 20.5 ms                                                | 20.2 ms: 1.02x faster                                                  |
| genshi_text              | 22.8 ms                                                | 22.5 ms: 1.01x faster                                                  |
| json_loads               | 26.5 us                                                | 26.2 us: 1.01x faster                                                  |
| xml_etree_parse          | 139 ms                                                 | 137 ms: 1.01x faster                                                   |
| logging_silent           | 109 ns                                                 | 108 ns: 1.01x faster                                                   |
| hexiom                   | 6.17 ms                                                | 6.10 ms: 1.01x faster                                                  |
| sympy_expand             | 468 ms                                                 | 464 ms: 1.01x faster                                                   |
| xml_etree_iterparse      | 96.7 ms                                                | 96.1 ms: 1.01x faster                                                  |
| docutils                 | 2.64 sec                                               | 2.63 sec: 1.00x faster                                                 |
| sqlglot_normalize        | 107 ms                                                 | 107 ms: 1.00x slower                                                   |
| scimark_lu               | 114 ms                                                 | 115 ms: 1.00x slower                                                   |
| scimark_fft              | 342 ms                                                 | 344 ms: 1.01x slower                                                   |
| meteor_contest           | 104 ms                                                 | 104 ms: 1.01x slower                                                   |
| tomli_loads              | 2.11 sec                                               | 2.12 sec: 1.01x slower                                                 |
| asyncio_websockets       | 517 ms                                                 | 520 ms: 1.01x slower                                                   |
| spectral_norm            | 110 ms                                                 | 111 ms: 1.01x slower                                                   |
| pidigits                 | 184 ms                                                 | 186 ms: 1.01x slower                                                   |
| pickle_pure_python       | 308 us                                                 | 310 us: 1.01x slower                                                   |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.52 sec: 1.01x slower                                                 |
| pyflate                  | 448 ms                                                 | 453 ms: 1.01x slower                                                   |
| sqlglot_optimize         | 53.3 ms                                                | 54.0 ms: 1.01x slower                                                  |
| pickle_dict              | 31.8 us                                                | 32.3 us: 1.02x slower                                                  |
| richards_super           | 51.9 ms                                                | 52.7 ms: 1.02x slower                                                  |
| xml_etree_generate       | 85.2 ms                                                | 86.6 ms: 1.02x slower                                                  |
| genshi_xml               | 50.2 ms                                                | 51.3 ms: 1.02x slower                                                  |
| pickle_list              | 4.77 us                                                | 4.88 us: 1.02x slower                                                  |
| xml_etree_process        | 59.0 ms                                                | 60.6 ms: 1.03x slower                                                  |
| richards                 | 45.9 ms                                                | 47.2 ms: 1.03x slower                                                  |
| pickle                   | 10.9 us                                                | 11.3 us: 1.03x slower                                                  |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 4.54 ms: 1.03x slower                                                  |
| html5lib                 | 63.6 ms                                                | 65.7 ms: 1.03x slower                                                  |
| regex_dna                | 168 ms                                                 | 174 ms: 1.04x slower                                                   |
| python_startup_no_site   | 7.16 ms                                                | 7.42 ms: 1.04x slower                                                  |
| fannkuch                 | 372 ms                                                 | 386 ms: 1.04x slower                                                   |
| django_template          | 34.7 ms                                                | 35.9 ms: 1.04x slower                                                  |
| scimark_sor              | 130 ms                                                 | 137 ms: 1.05x slower                                                   |
| bench_thread_pool        | 941 us                                                 | 1.02 ms: 1.08x slower                                                  |
| nbody                    | 89.3 ms                                                | 98.0 ms: 1.10x slower                                                  |
| mako                     | 11.0 ms                                                | 12.1 ms: 1.10x slower                                                  |
| python_startup           | 9.93 ms                                                | 11.0 ms: 1.11x slower                                                  |
| regex_v8                 | 20.6 ms                                                | 23.0 ms: 1.12x slower                                                  |
| json_dumps               | 10.4 ms                                                | 11.7 ms: 1.13x slower                                                  |
| telco                    | 6.53 ms                                                | 7.41 ms: 1.14x slower                                                  |
| coverage                 | 71.4 ms                                                | 81.1 ms: 1.14x slower                                                  |
| create_gc_cycles         | 1.09 ms                                                | 1.35 ms: 1.24x slower                                                  |
| bench_mp_pool            | 10.8 ms                                                | 63.1 ms: 5.84x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.01x slower                                                           |

Benchmark hidden because not significant (7): nqueens, regex_effbot, pylint, float, unpickle_list, unpickle_pure_python, sqlite_synth
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 80.88% likely to be faster
- 90% likely to have a speedup of 1.00x
- 95% likely to have a speedup of 1.00x
- 99% likely to have a speedup of 1.00x

# Memory
- memory change: 1.02x