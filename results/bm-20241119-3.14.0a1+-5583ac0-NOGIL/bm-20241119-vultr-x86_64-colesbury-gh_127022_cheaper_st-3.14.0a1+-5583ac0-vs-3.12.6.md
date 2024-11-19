# Results vs. 3.12.6

- fork: colesbury
- ref: gh_127022_cheaper_st
- machine: linux-x86_64
- commit hash: 5583ac0
- commit date: 2024-11-19
- overall geometric mean: 1.53x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.37x slower
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 412 ms: 1.56x slower                                                      |
| docutils       | 2.64 sec                                               | 3.37 sec: 1.28x slower                                                    |
| html5lib       | 63.6 ms                                                | 106 ms: 1.66x slower                                                      |
| Geometric mean | (ref)                                                  | 1.49x slower                                                              |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| asyncio_tcp      | 519 ms                                                 | 580 ms: 1.12x slower                                                      |
| asyncio_tcp_ssl  | 1.51 sec                                               | 1.81 sec: 1.20x slower                                                    |
| async_generators | 384 ms                                                 | 493 ms: 1.28x slower                                                      |
| coroutines       | 23.9 ms                                                | 31.0 ms: 1.29x slower                                                     |
| Geometric mean   | (ref)                                                  | 1.17x slower                                                              |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 186 ms: 1.01x slower                                                      |
| float          | 80.8 ms                                                | 150 ms: 1.86x slower                                                      |
| nbody          | 89.3 ms                                                | 199 ms: 2.23x slower                                                      |
| Geometric mean | (ref)                                                  | 1.61x slower                                                              |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 2.82 ms: 1.12x faster                                                     |
| regex_dna      | 168 ms                                                 | 180 ms: 1.07x slower                                                      |
| regex_v8       | 20.6 ms                                                | 24.6 ms: 1.20x slower                                                     |
| regex_compile  | 142 ms                                                 | 228 ms: 1.60x slower                                                      |
| Geometric mean | (ref)                                                  | 1.16x slower                                                              |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|----------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 132 ms: 1.05x faster                                                      |
| pickle_dict          | 31.8 us                                                | 31.9 us: 1.00x slower                                                     |
| unpickle             | 14.1 us                                                | 14.6 us: 1.04x slower                                                     |
| json_loads           | 26.5 us                                                | 28.6 us: 1.08x slower                                                     |
| pickle_list          | 4.77 us                                                | 5.17 us: 1.09x slower                                                     |
| pickle               | 10.9 us                                                | 11.9 us: 1.09x slower                                                     |
| unpickle_list        | 4.67 us                                                | 5.20 us: 1.11x slower                                                     |
| xml_etree_iterparse  | 96.7 ms                                                | 109 ms: 1.13x slower                                                      |
| xml_etree_generate   | 85.2 ms                                                | 112 ms: 1.32x slower                                                      |
| json_dumps           | 10.4 ms                                                | 15.4 ms: 1.48x slower                                                     |
| tomli_loads          | 2.11 sec                                               | 3.18 sec: 1.51x slower                                                    |
| xml_etree_process    | 59.0 ms                                                | 91.8 ms: 1.56x slower                                                     |
| unpickle_pure_python | 221 us                                                 | 422 us: 1.91x slower                                                      |
| pickle_pure_python   | 308 us                                                 | 621 us: 2.02x slower                                                      |
| Geometric mean       | (ref)                                                  | 1.27x slower                                                              |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                     |
| python_startup         | 9.93 ms                                                | 15.6 ms: 1.58x slower                                                     |
| Geometric mean         | (ref)                                                  | 1.50x slower                                                              |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|-----------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 81.5 ms: 1.62x slower                                                     |
| genshi_text     | 22.8 ms                                                | 40.2 ms: 1.76x slower                                                     |
| django_template | 34.7 ms                                                | 64.4 ms: 1.86x slower                                                     |
| mako            | 11.0 ms                                                | 20.7 ms: 1.88x slower                                                     |
| Geometric mean  | (ref)                                                  | 1.78x slower                                                              |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241119-vultr-x86_64-colesbury-gh_127022_cheaper_st-3.14.0a1+-5583ac0 |
|--------------------------|:------------------------------------------------------:|:-------------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                | 2.36 ms: 1.46x faster                                                     |
| regex_effbot             | 3.17 ms                                                | 2.82 ms: 1.12x faster                                                     |
| xml_etree_parse          | 139 ms                                                 | 132 ms: 1.05x faster                                                      |
| pickle_dict              | 31.8 us                                                | 31.9 us: 1.00x slower                                                     |
| pathlib                  | 21.5 ms                                                | 21.7 ms: 1.01x slower                                                     |
| pidigits                 | 184 ms                                                 | 186 ms: 1.01x slower                                                      |
| create_gc_cycles         | 1.09 ms                                                | 1.13 ms: 1.03x slower                                                     |
| unpickle                 | 14.1 us                                                | 14.6 us: 1.04x slower                                                     |
| json                     | 5.02 ms                                                | 5.27 ms: 1.05x slower                                                     |
| regex_dna                | 168 ms                                                 | 180 ms: 1.07x slower                                                      |
| json_loads               | 26.5 us                                                | 28.6 us: 1.08x slower                                                     |
| pickle_list              | 4.77 us                                                | 5.17 us: 1.09x slower                                                     |
| pickle                   | 10.9 us                                                | 11.9 us: 1.09x slower                                                     |
| sqlite_synth             | 2.20 us                                                | 2.42 us: 1.10x slower                                                     |
| unpickle_list            | 4.67 us                                                | 5.20 us: 1.11x slower                                                     |
| asyncio_tcp              | 519 ms                                                 | 580 ms: 1.12x slower                                                      |
| xml_etree_iterparse      | 96.7 ms                                                | 109 ms: 1.13x slower                                                      |
| regex_v8                 | 20.6 ms                                                | 24.6 ms: 1.20x slower                                                     |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.81 sec: 1.20x slower                                                    |
| scimark_fft              | 342 ms                                                 | 417 ms: 1.22x slower                                                      |
| deepcopy                 | 352 us                                                 | 431 us: 1.22x slower                                                      |
| generators               | 32.2 ms                                                | 40.2 ms: 1.25x slower                                                     |
| mdp                      | 2.42 sec                                               | 3.05 sec: 1.26x slower                                                    |
| docutils                 | 2.64 sec                                               | 3.37 sec: 1.28x slower                                                    |
| async_generators         | 384 ms                                                 | 493 ms: 1.28x slower                                                      |
| coroutines               | 23.9 ms                                                | 31.0 ms: 1.29x slower                                                     |
| bpe_tokeniser            | 4.74 sec                                               | 6.13 sec: 1.30x slower                                                    |
| dulwich_log              | 78.9 ms                                                | 103 ms: 1.31x slower                                                      |
| deepcopy_memo            | 40.3 us                                                | 52.9 us: 1.31x slower                                                     |
| xml_etree_generate       | 85.2 ms                                                | 112 ms: 1.32x slower                                                      |
| pylint                   | 319 ms                                                 | 420 ms: 1.32x slower                                                      |
| meteor_contest           | 104 ms                                                 | 138 ms: 1.33x slower                                                      |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 5.95 ms: 1.35x slower                                                     |
| crypto_pyaes             | 76.6 ms                                                | 108 ms: 1.41x slower                                                      |
| python_startup_no_site   | 7.16 ms                                                | 10.2 ms: 1.43x slower                                                     |
| nqueens                  | 80.1 ms                                                | 115 ms: 1.43x slower                                                      |
| coverage                 | 71.4 ms                                                | 103 ms: 1.44x slower                                                      |
| deepcopy_reduce          | 3.08 us                                                | 4.43 us: 1.44x slower                                                     |
| telco                    | 6.53 ms                                                | 9.42 ms: 1.44x slower                                                     |
| pycparser                | 1.17 sec                                               | 1.69 sec: 1.45x slower                                                    |
| spectral_norm            | 110 ms                                                 | 161 ms: 1.46x slower                                                      |
| json_dumps               | 10.4 ms                                                | 15.4 ms: 1.48x slower                                                     |
| tomli_loads              | 2.11 sec                                               | 3.18 sec: 1.51x slower                                                    |
| typing_runtime_protocols | 163 us                                                 | 248 us: 1.52x slower                                                      |
| comprehensions           | 19.8 us                                                | 30.3 us: 1.53x slower                                                     |
| fannkuch                 | 372 ms                                                 | 572 ms: 1.54x slower                                                      |
| xml_etree_process        | 59.0 ms                                                | 91.8 ms: 1.56x slower                                                     |
| 2to3                     | 264 ms                                                 | 412 ms: 1.56x slower                                                      |
| python_startup           | 9.93 ms                                                | 15.6 ms: 1.58x slower                                                     |
| thrift                   | 791 us                                                 | 1.26 ms: 1.59x slower                                                     |
| regex_compile            | 142 ms                                                 | 228 ms: 1.60x slower                                                      |
| sympy_integrate          | 20.5 ms                                                | 33.1 ms: 1.61x slower                                                     |
| genshi_xml               | 50.2 ms                                                | 81.5 ms: 1.62x slower                                                     |
| html5lib                 | 63.6 ms                                                | 106 ms: 1.66x slower                                                      |
| sqlglot_normalize        | 107 ms                                                 | 180 ms: 1.69x slower                                                      |
| sqlglot_optimize         | 53.3 ms                                                | 90.7 ms: 1.70x slower                                                     |
| pyflate                  | 448 ms                                                 | 778 ms: 1.74x slower                                                      |
| genshi_text              | 22.8 ms                                                | 40.2 ms: 1.76x slower                                                     |
| pprint_safe_repr         | 743 ms                                                 | 1.32 sec: 1.77x slower                                                    |
| logging_simple           | 6.63 us                                                | 11.9 us: 1.79x slower                                                     |
| logging_format           | 7.35 us                                                | 13.2 us: 1.80x slower                                                     |
| pprint_pformat           | 1.52 sec                                               | 2.74 sec: 1.81x slower                                                    |
| scimark_monte_carlo      | 68.4 ms                                                | 126 ms: 1.85x slower                                                      |
| sympy_str                | 292 ms                                                 | 540 ms: 1.85x slower                                                      |
| django_template          | 34.7 ms                                                | 64.4 ms: 1.86x slower                                                     |
| float                    | 80.8 ms                                                | 150 ms: 1.86x slower                                                      |
| mako                     | 11.0 ms                                                | 20.7 ms: 1.88x slower                                                     |
| unpickle_pure_python     | 221 us                                                 | 422 us: 1.91x slower                                                      |
| chaos                    | 62.8 ms                                                | 121 ms: 1.92x slower                                                      |
| logging_silent           | 109 ns                                                 | 212 ns: 1.94x slower                                                      |
| sqlglot_transpile        | 1.67 ms                                                | 3.31 ms: 1.98x slower                                                     |
| richards                 | 45.9 ms                                                | 91.9 ms: 2.00x slower                                                     |
| hexiom                   | 6.17 ms                                                | 12.4 ms: 2.01x slower                                                     |
| pickle_pure_python       | 308 us                                                 | 621 us: 2.02x slower                                                      |
| raytrace                 | 299 ms                                                 | 618 ms: 2.07x slower                                                      |
| scimark_sor              | 130 ms                                                 | 269 ms: 2.07x slower                                                      |
| richards_super           | 51.9 ms                                                | 109 ms: 2.09x slower                                                      |
| sqlglot_parse            | 1.36 ms                                                | 2.84 ms: 2.10x slower                                                     |
| scimark_lu               | 114 ms                                                 | 247 ms: 2.16x slower                                                      |
| go                       | 139 ms                                                 | 303 ms: 2.17x slower                                                      |
| nbody                    | 89.3 ms                                                | 199 ms: 2.23x slower                                                      |
| sympy_expand             | 468 ms                                                 | 1.05 sec: 2.24x slower                                                    |
| sympy_sum                | 166 ms                                                 | 381 ms: 2.30x slower                                                      |
| deltablue                | 3.45 ms                                                | 9.10 ms: 2.64x slower                                                     |
| unpack_sequence          | 52.1 ns                                                | 147 ns: 2.82x slower                                                      |
| bench_thread_pool        | 941 us                                                 | 3.49 ms: 3.71x slower                                                     |
| bench_mp_pool            | 10.8 ms                                                | 72.5 ms: 6.71x slower                                                     |
| Geometric mean           | (ref)                                                  | 1.53x slower                                                              |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.44x
- 95% likely to have a slowdown of 1.43x
- 99% likely to have a slowdown of 1.37x

# Memory
- memory change: 1.23x