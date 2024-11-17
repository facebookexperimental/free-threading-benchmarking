# Results vs. 3.12.6

- fork: python
- ref: acbd5c9c6c62dac34d2e
- machine: linux-x86_64
- commit hash: acbd5c9
- commit date: 2024-11-17
- overall geometric mean: 1.56x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.39x slower
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 418 ms: 1.59x slower                                                   |
| docutils       | 2.64 sec                                               | 3.43 sec: 1.30x slower                                                 |
| html5lib       | 63.6 ms                                                | 107 ms: 1.69x slower                                                   |
| Geometric mean | (ref)                                                  | 1.52x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_tcp      | 519 ms                                                 | 583 ms: 1.12x slower                                                   |
| asyncio_tcp_ssl  | 1.51 sec                                               | 1.81 sec: 1.20x slower                                                 |
| async_generators | 384 ms                                                 | 492 ms: 1.28x slower                                                   |
| coroutines       | 23.9 ms                                                | 32.0 ms: 1.34x slower                                                  |
| Geometric mean   | (ref)                                                  | 1.18x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 216 ms: 1.17x slower                                                   |
| float          | 80.8 ms                                                | 153 ms: 1.90x slower                                                   |
| nbody          | 89.3 ms                                                | 207 ms: 2.32x slower                                                   |
| Geometric mean | (ref)                                                  | 1.73x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.11 ms: 1.02x faster                                                  |
| regex_dna      | 168 ms                                                 | 182 ms: 1.09x slower                                                   |
| regex_v8       | 20.6 ms                                                | 24.9 ms: 1.21x slower                                                  |
| regex_compile  | 142 ms                                                 | 231 ms: 1.62x slower                                                   |
| Geometric mean | (ref)                                                  | 1.20x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 133 ms: 1.04x faster                                                   |
| pickle_dict          | 31.8 us                                                | 32.5 us: 1.02x slower                                                  |
| unpickle             | 14.1 us                                                | 14.7 us: 1.04x slower                                                  |
| json_loads           | 26.5 us                                                | 28.4 us: 1.07x slower                                                  |
| pickle_list          | 4.77 us                                                | 5.20 us: 1.09x slower                                                  |
| unpickle_list        | 4.67 us                                                | 5.20 us: 1.11x slower                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 109 ms: 1.13x slower                                                   |
| pickle               | 10.9 us                                                | 12.5 us: 1.14x slower                                                  |
| xml_etree_generate   | 85.2 ms                                                | 115 ms: 1.35x slower                                                   |
| json_dumps           | 10.4 ms                                                | 15.4 ms: 1.49x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 3.28 sec: 1.56x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 94.1 ms: 1.60x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 432 us: 1.96x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 635 us: 2.06x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.29x slower                                                           |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.59x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.51x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 83.2 ms: 1.66x slower                                                  |
| genshi_text     | 22.8 ms                                                | 40.6 ms: 1.78x slower                                                  |
| django_template | 34.7 ms                                                | 65.3 ms: 1.88x slower                                                  |
| mako            | 11.0 ms                                                | 20.9 ms: 1.90x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.80x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-vultr-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                | 2.58 ms: 1.34x faster                                                  |
| xml_etree_parse          | 139 ms                                                 | 133 ms: 1.04x faster                                                   |
| regex_effbot             | 3.17 ms                                                | 3.11 ms: 1.02x faster                                                  |
| pickle_dict              | 31.8 us                                                | 32.5 us: 1.02x slower                                                  |
| pathlib                  | 21.5 ms                                                | 22.1 ms: 1.03x slower                                                  |
| create_gc_cycles         | 1.09 ms                                                | 1.13 ms: 1.03x slower                                                  |
| unpickle                 | 14.1 us                                                | 14.7 us: 1.04x slower                                                  |
| json                     | 5.02 ms                                                | 5.26 ms: 1.05x slower                                                  |
| json_loads               | 26.5 us                                                | 28.4 us: 1.07x slower                                                  |
| regex_dna                | 168 ms                                                 | 182 ms: 1.09x slower                                                   |
| pickle_list              | 4.77 us                                                | 5.20 us: 1.09x slower                                                  |
| unpickle_list            | 4.67 us                                                | 5.20 us: 1.11x slower                                                  |
| asyncio_tcp              | 519 ms                                                 | 583 ms: 1.12x slower                                                   |
| sqlite_synth             | 2.20 us                                                | 2.48 us: 1.12x slower                                                  |
| xml_etree_iterparse      | 96.7 ms                                                | 109 ms: 1.13x slower                                                   |
| pickle                   | 10.9 us                                                | 12.5 us: 1.14x slower                                                  |
| pidigits                 | 184 ms                                                 | 216 ms: 1.17x slower                                                   |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.81 sec: 1.20x slower                                                 |
| regex_v8                 | 20.6 ms                                                | 24.9 ms: 1.21x slower                                                  |
| scimark_fft              | 342 ms                                                 | 418 ms: 1.22x slower                                                   |
| deepcopy                 | 352 us                                                 | 438 us: 1.24x slower                                                   |
| async_generators         | 384 ms                                                 | 492 ms: 1.28x slower                                                   |
| generators               | 32.2 ms                                                | 41.5 ms: 1.29x slower                                                  |
| docutils                 | 2.64 sec                                               | 3.43 sec: 1.30x slower                                                 |
| mdp                      | 2.42 sec                                               | 3.14 sec: 1.30x slower                                                 |
| bpe_tokeniser            | 4.74 sec                                               | 6.18 sec: 1.30x slower                                                 |
| pylint                   | 319 ms                                                 | 423 ms: 1.33x slower                                                   |
| dulwich_log              | 78.9 ms                                                | 105 ms: 1.34x slower                                                   |
| coroutines               | 23.9 ms                                                | 32.0 ms: 1.34x slower                                                  |
| meteor_contest           | 104 ms                                                 | 139 ms: 1.35x slower                                                   |
| xml_etree_generate       | 85.2 ms                                                | 115 ms: 1.35x slower                                                   |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 5.94 ms: 1.35x slower                                                  |
| deepcopy_memo            | 40.3 us                                                | 54.7 us: 1.36x slower                                                  |
| crypto_pyaes             | 76.6 ms                                                | 109 ms: 1.42x slower                                                   |
| telco                    | 6.53 ms                                                | 9.27 ms: 1.42x slower                                                  |
| python_startup_no_site   | 7.16 ms                                                | 10.3 ms: 1.44x slower                                                  |
| coverage                 | 71.4 ms                                                | 103 ms: 1.44x slower                                                   |
| nqueens                  | 80.1 ms                                                | 115 ms: 1.44x slower                                                   |
| deepcopy_reduce          | 3.08 us                                                | 4.53 us: 1.47x slower                                                  |
| spectral_norm            | 110 ms                                                 | 163 ms: 1.48x slower                                                   |
| pycparser                | 1.17 sec                                               | 1.74 sec: 1.49x slower                                                 |
| json_dumps               | 10.4 ms                                                | 15.4 ms: 1.49x slower                                                  |
| fannkuch                 | 372 ms                                                 | 571 ms: 1.53x slower                                                   |
| typing_runtime_protocols | 163 us                                                 | 253 us: 1.55x slower                                                   |
| tomli_loads              | 2.11 sec                                               | 3.28 sec: 1.56x slower                                                 |
| comprehensions           | 19.8 us                                                | 31.0 us: 1.56x slower                                                  |
| python_startup           | 9.93 ms                                                | 15.7 ms: 1.59x slower                                                  |
| 2to3                     | 264 ms                                                 | 418 ms: 1.59x slower                                                   |
| xml_etree_process        | 59.0 ms                                                | 94.1 ms: 1.60x slower                                                  |
| regex_compile            | 142 ms                                                 | 231 ms: 1.62x slower                                                   |
| sympy_integrate          | 20.5 ms                                                | 33.4 ms: 1.63x slower                                                  |
| thrift                   | 791 us                                                 | 1.30 ms: 1.64x slower                                                  |
| genshi_xml               | 50.2 ms                                                | 83.2 ms: 1.66x slower                                                  |
| html5lib                 | 63.6 ms                                                | 107 ms: 1.69x slower                                                   |
| sqlglot_normalize        | 107 ms                                                 | 182 ms: 1.70x slower                                                   |
| sqlglot_optimize         | 53.3 ms                                                | 90.9 ms: 1.71x slower                                                  |
| pyflate                  | 448 ms                                                 | 797 ms: 1.78x slower                                                   |
| genshi_text              | 22.8 ms                                                | 40.6 ms: 1.78x slower                                                  |
| pprint_safe_repr         | 743 ms                                                 | 1.34 sec: 1.81x slower                                                 |
| pprint_pformat           | 1.52 sec                                               | 2.77 sec: 1.82x slower                                                 |
| sympy_str                | 292 ms                                                 | 544 ms: 1.87x slower                                                   |
| logging_simple           | 6.63 us                                                | 12.4 us: 1.87x slower                                                  |
| django_template          | 34.7 ms                                                | 65.3 ms: 1.88x slower                                                  |
| scimark_monte_carlo      | 68.4 ms                                                | 129 ms: 1.88x slower                                                   |
| logging_format           | 7.35 us                                                | 13.9 us: 1.89x slower                                                  |
| float                    | 80.8 ms                                                | 153 ms: 1.90x slower                                                   |
| mako                     | 11.0 ms                                                | 20.9 ms: 1.90x slower                                                  |
| unpickle_pure_python     | 221 us                                                 | 432 us: 1.96x slower                                                   |
| chaos                    | 62.8 ms                                                | 123 ms: 1.96x slower                                                   |
| sqlglot_transpile        | 1.67 ms                                                | 3.35 ms: 2.00x slower                                                  |
| logging_silent           | 109 ns                                                 | 222 ns: 2.04x slower                                                   |
| hexiom                   | 6.17 ms                                                | 12.7 ms: 2.05x slower                                                  |
| pickle_pure_python       | 308 us                                                 | 635 us: 2.06x slower                                                   |
| richards                 | 45.9 ms                                                | 96.0 ms: 2.09x slower                                                  |
| scimark_sor              | 130 ms                                                 | 273 ms: 2.11x slower                                                   |
| sqlglot_parse            | 1.36 ms                                                | 2.89 ms: 2.13x slower                                                  |
| raytrace                 | 299 ms                                                 | 640 ms: 2.14x slower                                                   |
| richards_super           | 51.9 ms                                                | 112 ms: 2.16x slower                                                   |
| scimark_lu               | 114 ms                                                 | 248 ms: 2.17x slower                                                   |
| go                       | 139 ms                                                 | 303 ms: 2.18x slower                                                   |
| sympy_expand             | 468 ms                                                 | 1.06 sec: 2.27x slower                                                 |
| sympy_sum                | 166 ms                                                 | 383 ms: 2.31x slower                                                   |
| nbody                    | 89.3 ms                                                | 207 ms: 2.32x slower                                                   |
| deltablue                | 3.45 ms                                                | 9.33 ms: 2.71x slower                                                  |
| unpack_sequence          | 52.1 ns                                                | 151 ns: 2.90x slower                                                   |
| bench_thread_pool        | 941 us                                                 | 3.49 ms: 3.70x slower                                                  |
| bench_mp_pool            | 10.8 ms                                                | 72.7 ms: 6.73x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.56x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.46x
- 95% likely to have a slowdown of 1.44x
- 99% likely to have a slowdown of 1.39x

# Memory
- memory change: 1.23x