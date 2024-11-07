# Results vs. 3.12.6

- fork: python
- ref: 2a6b6b33dfe0f3c435ab
- machine: linux-x86_64
- commit hash: 2a6b6b3
- commit date: 2024-11-06
- overall geometric mean: 1.55x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.38x slower
- Memory change: 1.23x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 264 ms                                                 | 417 ms: 1.58x slower                                                   |
| docutils       | 2.64 sec                                               | 3.41 sec: 1.29x slower                                                 |
| html5lib       | 63.6 ms                                                | 107 ms: 1.68x slower                                                   |
| Geometric mean | (ref)                                                  | 1.51x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|--------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_websockets | 517 ms                                                 | 516 ms: 1.00x faster                                                   |
| asyncio_tcp        | 519 ms                                                 | 584 ms: 1.13x slower                                                   |
| asyncio_tcp_ssl    | 1.51 sec                                               | 1.84 sec: 1.22x slower                                                 |
| async_generators   | 384 ms                                                 | 499 ms: 1.30x slower                                                   |
| coroutines         | 23.9 ms                                                | 31.2 ms: 1.30x slower                                                  |
| Geometric mean     | (ref)                                                  | 1.18x slower                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 184 ms                                                 | 188 ms: 1.02x slower                                                   |
| float          | 80.8 ms                                                | 152 ms: 1.88x slower                                                   |
| nbody          | 89.3 ms                                                | 205 ms: 2.30x slower                                                   |
| Geometric mean | (ref)                                                  | 1.64x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 3.17 ms                                                | 3.19 ms: 1.01x slower                                                  |
| regex_dna      | 168 ms                                                 | 189 ms: 1.13x slower                                                   |
| regex_v8       | 20.6 ms                                                | 25.2 ms: 1.22x slower                                                  |
| regex_compile  | 142 ms                                                 | 233 ms: 1.63x slower                                                   |
| Geometric mean | (ref)                                                  | 1.23x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| xml_etree_parse      | 139 ms                                                 | 134 ms: 1.03x faster                                                   |
| pickle_dict          | 31.8 us                                                | 31.4 us: 1.01x faster                                                  |
| pickle_list          | 4.77 us                                                | 4.73 us: 1.01x faster                                                  |
| unpickle_list        | 4.67 us                                                | 4.91 us: 1.05x slower                                                  |
| unpickle             | 14.1 us                                                | 14.9 us: 1.06x slower                                                  |
| json_loads           | 26.5 us                                                | 29.9 us: 1.13x slower                                                  |
| xml_etree_iterparse  | 96.7 ms                                                | 110 ms: 1.13x slower                                                   |
| xml_etree_generate   | 85.2 ms                                                | 114 ms: 1.34x slower                                                   |
| json_dumps           | 10.4 ms                                                | 15.2 ms: 1.47x slower                                                  |
| tomli_loads          | 2.11 sec                                               | 3.22 sec: 1.53x slower                                                 |
| xml_etree_process    | 59.0 ms                                                | 94.9 ms: 1.61x slower                                                  |
| unpickle_pure_python | 221 us                                                 | 417 us: 1.89x slower                                                   |
| pickle_pure_python   | 308 us                                                 | 627 us: 2.04x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.26x slower                                                           |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                  |
| python_startup         | 9.93 ms                                                | 15.7 ms: 1.59x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.51x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 50.2 ms                                                | 82.2 ms: 1.64x slower                                                  |
| genshi_text     | 22.8 ms                                                | 40.3 ms: 1.77x slower                                                  |
| django_template | 34.7 ms                                                | 64.9 ms: 1.87x slower                                                  |
| mako            | 11.0 ms                                                | 20.6 ms: 1.88x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.79x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-vultr-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 3.46 ms                                                | 2.47 ms: 1.40x faster                                                  |
| xml_etree_parse          | 139 ms                                                 | 134 ms: 1.03x faster                                                   |
| pickle_dict              | 31.8 us                                                | 31.4 us: 1.01x faster                                                  |
| pickle_list              | 4.77 us                                                | 4.73 us: 1.01x faster                                                  |
| asyncio_websockets       | 517 ms                                                 | 516 ms: 1.00x faster                                                   |
| regex_effbot             | 3.17 ms                                                | 3.19 ms: 1.01x slower                                                  |
| pidigits                 | 184 ms                                                 | 188 ms: 1.02x slower                                                   |
| pathlib                  | 21.5 ms                                                | 22.3 ms: 1.04x slower                                                  |
| create_gc_cycles         | 1.09 ms                                                | 1.13 ms: 1.04x slower                                                  |
| unpickle_list            | 4.67 us                                                | 4.91 us: 1.05x slower                                                  |
| unpickle                 | 14.1 us                                                | 14.9 us: 1.06x slower                                                  |
| json                     | 5.02 ms                                                | 5.46 ms: 1.09x slower                                                  |
| sqlite_synth             | 2.20 us                                                | 2.48 us: 1.12x slower                                                  |
| regex_dna                | 168 ms                                                 | 189 ms: 1.13x slower                                                   |
| asyncio_tcp              | 519 ms                                                 | 584 ms: 1.13x slower                                                   |
| json_loads               | 26.5 us                                                | 29.9 us: 1.13x slower                                                  |
| xml_etree_iterparse      | 96.7 ms                                                | 110 ms: 1.13x slower                                                   |
| asyncio_tcp_ssl          | 1.51 sec                                               | 1.84 sec: 1.22x slower                                                 |
| regex_v8                 | 20.6 ms                                                | 25.2 ms: 1.22x slower                                                  |
| scimark_fft              | 342 ms                                                 | 418 ms: 1.22x slower                                                   |
| deepcopy                 | 352 us                                                 | 437 us: 1.24x slower                                                   |
| docutils                 | 2.64 sec                                               | 3.41 sec: 1.29x slower                                                 |
| bpe_tokeniser            | 4.74 sec                                               | 6.14 sec: 1.30x slower                                                 |
| async_generators         | 384 ms                                                 | 499 ms: 1.30x slower                                                   |
| coroutines               | 23.9 ms                                                | 31.2 ms: 1.30x slower                                                  |
| mdp                      | 2.42 sec                                               | 3.16 sec: 1.31x slower                                                 |
| generators               | 32.2 ms                                                | 42.5 ms: 1.32x slower                                                  |
| deepcopy_memo            | 40.3 us                                                | 53.1 us: 1.32x slower                                                  |
| dulwich_log              | 78.9 ms                                                | 104 ms: 1.32x slower                                                   |
| pylint                   | 319 ms                                                 | 424 ms: 1.33x slower                                                   |
| meteor_contest           | 104 ms                                                 | 138 ms: 1.33x slower                                                   |
| xml_etree_generate       | 85.2 ms                                                | 114 ms: 1.34x slower                                                   |
| scimark_sparse_mat_mult  | 4.39 ms                                                | 6.10 ms: 1.39x slower                                                  |
| crypto_pyaes             | 76.6 ms                                                | 108 ms: 1.40x slower                                                   |
| coverage                 | 71.4 ms                                                | 102 ms: 1.43x slower                                                   |
| nqueens                  | 80.1 ms                                                | 115 ms: 1.43x slower                                                   |
| python_startup_no_site   | 7.16 ms                                                | 10.3 ms: 1.43x slower                                                  |
| telco                    | 6.53 ms                                                | 9.36 ms: 1.43x slower                                                  |
| json_dumps               | 10.4 ms                                                | 15.2 ms: 1.47x slower                                                  |
| deepcopy_reduce          | 3.08 us                                                | 4.55 us: 1.48x slower                                                  |
| pycparser                | 1.17 sec                                               | 1.74 sec: 1.49x slower                                                 |
| spectral_norm            | 110 ms                                                 | 166 ms: 1.51x slower                                                   |
| fannkuch                 | 372 ms                                                 | 565 ms: 1.52x slower                                                   |
| tomli_loads              | 2.11 sec                                               | 3.22 sec: 1.53x slower                                                 |
| typing_runtime_protocols | 163 us                                                 | 251 us: 1.54x slower                                                   |
| comprehensions           | 19.8 us                                                | 30.8 us: 1.55x slower                                                  |
| 2to3                     | 264 ms                                                 | 417 ms: 1.58x slower                                                   |
| python_startup           | 9.93 ms                                                | 15.7 ms: 1.59x slower                                                  |
| xml_etree_process        | 59.0 ms                                                | 94.9 ms: 1.61x slower                                                  |
| sympy_integrate          | 20.5 ms                                                | 33.2 ms: 1.62x slower                                                  |
| regex_compile            | 142 ms                                                 | 233 ms: 1.63x slower                                                   |
| genshi_xml               | 50.2 ms                                                | 82.2 ms: 1.64x slower                                                  |
| thrift                   | 791 us                                                 | 1.30 ms: 1.64x slower                                                  |
| html5lib                 | 63.6 ms                                                | 107 ms: 1.68x slower                                                   |
| sqlglot_normalize        | 107 ms                                                 | 181 ms: 1.70x slower                                                   |
| sqlglot_optimize         | 53.3 ms                                                | 90.9 ms: 1.71x slower                                                  |
| pyflate                  | 448 ms                                                 | 775 ms: 1.73x slower                                                   |
| genshi_text              | 22.8 ms                                                | 40.3 ms: 1.77x slower                                                  |
| pprint_safe_repr         | 743 ms                                                 | 1.33 sec: 1.78x slower                                                 |
| pprint_pformat           | 1.52 sec                                               | 2.75 sec: 1.81x slower                                                 |
| sympy_str                | 292 ms                                                 | 543 ms: 1.86x slower                                                   |
| django_template          | 34.7 ms                                                | 64.9 ms: 1.87x slower                                                  |
| scimark_monte_carlo      | 68.4 ms                                                | 128 ms: 1.87x slower                                                   |
| logging_format           | 7.35 us                                                | 13.8 us: 1.87x slower                                                  |
| mako                     | 11.0 ms                                                | 20.6 ms: 1.88x slower                                                  |
| float                    | 80.8 ms                                                | 152 ms: 1.88x slower                                                   |
| unpickle_pure_python     | 221 us                                                 | 417 us: 1.89x slower                                                   |
| logging_simple           | 6.63 us                                                | 12.6 us: 1.89x slower                                                  |
| chaos                    | 62.8 ms                                                | 123 ms: 1.96x slower                                                   |
| logging_silent           | 109 ns                                                 | 214 ns: 1.96x slower                                                   |
| richards                 | 45.9 ms                                                | 90.6 ms: 1.97x slower                                                  |
| sqlglot_transpile        | 1.67 ms                                                | 3.34 ms: 2.00x slower                                                  |
| hexiom                   | 6.17 ms                                                | 12.4 ms: 2.02x slower                                                  |
| pickle_pure_python       | 308 us                                                 | 627 us: 2.04x slower                                                   |
| scimark_sor              | 130 ms                                                 | 275 ms: 2.12x slower                                                   |
| sqlglot_parse            | 1.36 ms                                                | 2.87 ms: 2.12x slower                                                  |
| raytrace                 | 299 ms                                                 | 635 ms: 2.12x slower                                                   |
| richards_super           | 51.9 ms                                                | 111 ms: 2.13x slower                                                   |
| go                       | 139 ms                                                 | 299 ms: 2.15x slower                                                   |
| scimark_lu               | 114 ms                                                 | 248 ms: 2.18x slower                                                   |
| sympy_expand             | 468 ms                                                 | 1.06 sec: 2.26x slower                                                 |
| nbody                    | 89.3 ms                                                | 205 ms: 2.30x slower                                                   |
| sympy_sum                | 166 ms                                                 | 382 ms: 2.30x slower                                                   |
| deltablue                | 3.45 ms                                                | 9.22 ms: 2.68x slower                                                  |
| unpack_sequence          | 52.1 ns                                                | 153 ns: 2.94x slower                                                   |
| bench_thread_pool        | 941 us                                                 | 3.49 ms: 3.71x slower                                                  |
| bench_mp_pool            | 10.8 ms                                                | 72.6 ms: 6.72x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.55x slower                                                           |

Benchmark hidden because not significant (1): pickle
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-vultr-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.46x
- 95% likely to have a slowdown of 1.43x
- 99% likely to have a slowdown of 1.38x

# Memory
- memory change: 1.23x