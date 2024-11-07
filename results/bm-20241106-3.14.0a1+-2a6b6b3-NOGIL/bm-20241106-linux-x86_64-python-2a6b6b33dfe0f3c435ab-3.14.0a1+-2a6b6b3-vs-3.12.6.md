# Results vs. 3.12.6

- fork: python
- ref: 2a6b6b33dfe0f3c435ab
- machine: linux-x86_64
- commit hash: 2a6b6b3
- commit date: 2024-11-06
- overall geometric mean: 1.42x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.32x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 659 ms: 1.44x slower                                                   |
| docutils       | 4.00 sec                                               | 4.71 sec: 1.18x slower                                                 |
| html5lib       | 88.9 ms                                                | 130 ms: 1.46x slower                                                   |
| Geometric mean | (ref)                                                  | 1.35x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_tcp      | 923 ms                                                 | 1.02 sec: 1.11x slower                                                 |
| asyncio_tcp_ssl  | 2.81 sec                                               | 3.30 sec: 1.18x slower                                                 |
| async_generators | 589 ms                                                 | 723 ms: 1.23x slower                                                   |
| coroutines       | 29.5 ms                                                | 41.8 ms: 1.42x slower                                                  |
| Geometric mean   | (ref)                                                  | 1.18x slower                                                           |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 186 ms: 1.51x slower                                                   |
| nbody          | 119 ms                                                 | 263 ms: 2.21x slower                                                   |
| Geometric mean | (ref)                                                  | 1.50x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.74 ms: 1.08x faster                                                  |
| regex_dna      | 278 ms                                                 | 297 ms: 1.07x slower                                                   |
| regex_v8       | 32.5 ms                                                | 36.2 ms: 1.12x slower                                                  |
| regex_compile  | 187 ms                                                 | 288 ms: 1.54x slower                                                   |
| Geometric mean | (ref)                                                  | 1.14x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_list          | 6.97 us                                                | 5.87 us: 1.19x faster                                                  |
| pickle               | 16.4 us                                                | 13.9 us: 1.18x faster                                                  |
| pickle_dict          | 52.7 us                                                | 45.6 us: 1.16x faster                                                  |
| xml_etree_parse      | 241 ms                                                 | 216 ms: 1.11x faster                                                   |
| unpickle_list        | 6.83 us                                                | 7.39 us: 1.08x slower                                                  |
| json_loads           | 37.9 us                                                | 41.5 us: 1.09x slower                                                  |
| unpickle             | 21.2 us                                                | 23.3 us: 1.10x slower                                                  |
| xml_etree_generate   | 127 ms                                                 | 156 ms: 1.23x slower                                                   |
| json_dumps           | 14.3 ms                                                | 19.5 ms: 1.36x slower                                                  |
| tomli_loads          | 2.88 sec                                               | 4.11 sec: 1.42x slower                                                 |
| xml_etree_process    | 83.7 ms                                                | 133 ms: 1.58x slower                                                   |
| unpickle_pure_python | 300 us                                                 | 520 us: 1.74x slower                                                   |
| pickle_pure_python   | 436 us                                                 | 797 us: 1.83x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.16x slower                                                           |

Benchmark hidden because not significant (1): xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 18.9 ms: 1.07x slower                                                  |
| python_startup         | 23.7 ms                                                | 27.5 ms: 1.16x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 79.1 ms: 1.76x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 119 ms: 1.77x slower                                                   |
| genshi_text     | 30.2 ms                                                | 55.5 ms: 1.84x slower                                                  |
| mako            | 15.7 ms                                                | 29.1 ms: 1.85x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.80x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241106-linux-x86_64-python-2a6b6b33dfe0f3c435ab-3.14.0a1+-2a6b6b3 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 5.86 ms                                                | 4.11 ms: 1.43x faster                                                  |
| pickle_list              | 6.97 us                                                | 5.87 us: 1.19x faster                                                  |
| pickle                   | 16.4 us                                                | 13.9 us: 1.18x faster                                                  |
| pickle_dict              | 52.7 us                                                | 45.6 us: 1.16x faster                                                  |
| xml_etree_parse          | 241 ms                                                 | 216 ms: 1.11x faster                                                   |
| regex_effbot             | 5.13 ms                                                | 4.74 ms: 1.08x faster                                                  |
| create_gc_cycles         | 1.94 ms                                                | 1.85 ms: 1.05x faster                                                  |
| regex_dna                | 278 ms                                                 | 297 ms: 1.07x slower                                                   |
| python_startup_no_site   | 17.6 ms                                                | 18.9 ms: 1.07x slower                                                  |
| unpickle_list            | 6.83 us                                                | 7.39 us: 1.08x slower                                                  |
| sqlite_synth             | 3.87 us                                                | 4.23 us: 1.09x slower                                                  |
| json_loads               | 37.9 us                                                | 41.5 us: 1.09x slower                                                  |
| unpickle                 | 21.2 us                                                | 23.3 us: 1.10x slower                                                  |
| asyncio_tcp              | 923 ms                                                 | 1.02 sec: 1.11x slower                                                 |
| regex_v8                 | 32.5 ms                                                | 36.2 ms: 1.12x slower                                                  |
| scimark_fft              | 500 ms                                                 | 562 ms: 1.12x slower                                                   |
| pycparser                | 1.79 sec                                               | 2.06 sec: 1.15x slower                                                 |
| python_startup           | 23.7 ms                                                | 27.5 ms: 1.16x slower                                                  |
| asyncio_tcp_ssl          | 2.81 sec                                               | 3.30 sec: 1.18x slower                                                 |
| docutils                 | 4.00 sec                                               | 4.71 sec: 1.18x slower                                                 |
| deepcopy                 | 468 us                                                 | 555 us: 1.19x slower                                                   |
| mdp                      | 3.97 sec                                               | 4.71 sec: 1.19x slower                                                 |
| xml_etree_generate       | 127 ms                                                 | 156 ms: 1.23x slower                                                   |
| async_generators         | 589 ms                                                 | 723 ms: 1.23x slower                                                   |
| pylint                   | 465 ms                                                 | 576 ms: 1.24x slower                                                   |
| scimark_sparse_mat_mult  | 6.70 ms                                                | 8.50 ms: 1.27x slower                                                  |
| json                     | 6.85 ms                                                | 8.70 ms: 1.27x slower                                                  |
| dulwich_log              | 100 ms                                                 | 130 ms: 1.29x slower                                                   |
| nqueens                  | 117 ms                                                 | 152 ms: 1.30x slower                                                   |
| generators               | 41.1 ms                                                | 53.6 ms: 1.30x slower                                                  |
| meteor_contest           | 146 ms                                                 | 192 ms: 1.31x slower                                                   |
| deepcopy_memo            | 52.4 us                                                | 70.8 us: 1.35x slower                                                  |
| json_dumps               | 14.3 ms                                                | 19.5 ms: 1.36x slower                                                  |
| comprehensions           | 27.1 us                                                | 37.0 us: 1.37x slower                                                  |
| bpe_tokeniser            | 6.59 sec                                               | 9.01 sec: 1.37x slower                                                 |
| pyflate                  | 727 ms                                                 | 1.01 sec: 1.39x slower                                                 |
| telco                    | 9.59 ms                                                | 13.3 ms: 1.39x slower                                                  |
| fannkuch                 | 540 ms                                                 | 759 ms: 1.41x slower                                                   |
| crypto_pyaes             | 107 ms                                                 | 151 ms: 1.41x slower                                                   |
| spectral_norm            | 156 ms                                                 | 220 ms: 1.41x slower                                                   |
| coroutines               | 29.5 ms                                                | 41.8 ms: 1.42x slower                                                  |
| tomli_loads              | 2.88 sec                                               | 4.11 sec: 1.42x slower                                                 |
| 2to3                     | 456 ms                                                 | 659 ms: 1.44x slower                                                   |
| html5lib                 | 88.9 ms                                                | 130 ms: 1.46x slower                                                   |
| deepcopy_reduce          | 4.04 us                                                | 5.92 us: 1.47x slower                                                  |
| typing_runtime_protocols | 224 us                                                 | 336 us: 1.50x slower                                                   |
| float                    | 123 ms                                                 | 186 ms: 1.51x slower                                                   |
| sqlglot_normalize        | 157 ms                                                 | 238 ms: 1.52x slower                                                   |
| coverage                 | 95.4 ms                                                | 145 ms: 1.52x slower                                                   |
| sympy_integrate          | 29.8 ms                                                | 45.5 ms: 1.53x slower                                                  |
| regex_compile            | 187 ms                                                 | 288 ms: 1.54x slower                                                   |
| logging_simple           | 9.45 us                                                | 14.9 us: 1.58x slower                                                  |
| xml_etree_process        | 83.7 ms                                                | 133 ms: 1.58x slower                                                   |
| scimark_monte_carlo      | 96.4 ms                                                | 155 ms: 1.61x slower                                                   |
| thrift                   | 1.06 ms                                                | 1.72 ms: 1.62x slower                                                  |
| sqlglot_optimize         | 76.0 ms                                                | 127 ms: 1.68x slower                                                   |
| pprint_pformat           | 1.98 sec                                               | 3.34 sec: 1.69x slower                                                 |
| pprint_safe_repr         | 967 ms                                                 | 1.65 sec: 1.70x slower                                                 |
| sympy_str                | 385 ms                                                 | 660 ms: 1.71x slower                                                   |
| unpickle_pure_python     | 300 us                                                 | 520 us: 1.74x slower                                                   |
| richards                 | 60.3 ms                                                | 105 ms: 1.74x slower                                                   |
| django_template          | 44.9 ms                                                | 79.1 ms: 1.76x slower                                                  |
| logging_format           | 9.59 us                                                | 16.9 us: 1.76x slower                                                  |
| genshi_xml               | 67.6 ms                                                | 119 ms: 1.77x slower                                                   |
| pickle_pure_python       | 436 us                                                 | 797 us: 1.83x slower                                                   |
| richards_super           | 72.8 ms                                                | 133 ms: 1.83x slower                                                   |
| genshi_text              | 30.2 ms                                                | 55.5 ms: 1.84x slower                                                  |
| raytrace                 | 408 ms                                                 | 749 ms: 1.84x slower                                                   |
| mako                     | 15.7 ms                                                | 29.1 ms: 1.85x slower                                                  |
| logging_silent           | 139 ns                                                 | 260 ns: 1.86x slower                                                   |
| chaos                    | 84.9 ms                                                | 166 ms: 1.95x slower                                                   |
| scimark_lu               | 152 ms                                                 | 300 ms: 1.97x slower                                                   |
| hexiom                   | 8.27 ms                                                | 16.3 ms: 1.97x slower                                                  |
| sqlglot_transpile        | 2.34 ms                                                | 4.86 ms: 2.08x slower                                                  |
| go                       | 172 ms                                                 | 362 ms: 2.10x slower                                                   |
| scimark_sor              | 167 ms                                                 | 351 ms: 2.11x slower                                                   |
| sympy_sum                | 222 ms                                                 | 468 ms: 2.11x slower                                                   |
| sqlglot_parse            | 1.79 ms                                                | 3.81 ms: 2.13x slower                                                  |
| nbody                    | 119 ms                                                 | 263 ms: 2.21x slower                                                   |
| sympy_expand             | 582 ms                                                 | 1.29 sec: 2.21x slower                                                 |
| deltablue                | 4.27 ms                                                | 11.0 ms: 2.59x slower                                                  |
| bench_mp_pool            | 20.7 ms                                                | 60.0 ms: 2.90x slower                                                  |
| unpack_sequence          | 60.2 ns                                                | 199 ns: 3.31x slower                                                   |
| Geometric mean           | (ref)                                                  | 1.42x slower                                                           |

Benchmark hidden because not significant (5): xml_etree_iterparse, bench_thread_pool, pathlib, asyncio_websockets, pidigits
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.37x
- 95% likely to have a slowdown of 1.37x
- 99% likely to have a slowdown of 1.32x

# Memory
- memory change: 1.20x