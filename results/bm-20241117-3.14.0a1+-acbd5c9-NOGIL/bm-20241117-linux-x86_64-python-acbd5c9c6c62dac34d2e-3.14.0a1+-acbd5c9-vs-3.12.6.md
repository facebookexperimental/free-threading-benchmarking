# Results vs. 3.12.6

- fork: python
- ref: acbd5c9c6c62dac34d2e
- machine: linux-x86_64
- commit hash: acbd5c9
- commit date: 2024-11-17
- overall geometric mean: 1.41x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.29x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 653 ms: 1.43x slower                                                   |
| docutils       | 4.00 sec                                               | 4.64 sec: 1.16x slower                                                 |
| html5lib       | 88.9 ms                                                | 137 ms: 1.54x slower                                                   |
| Geometric mean | (ref)                                                  | 1.37x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|--------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_websockets | 748 ms                                                 | 721 ms: 1.04x faster                                                   |
| asyncio_tcp        | 923 ms                                                 | 1.05 sec: 1.13x slower                                                 |
| asyncio_tcp_ssl    | 2.81 sec                                               | 3.29 sec: 1.17x slower                                                 |
| async_generators   | 589 ms                                                 | 696 ms: 1.18x slower                                                   |
| coroutines         | 29.5 ms                                                | 39.9 ms: 1.35x slower                                                  |
| Geometric mean     | (ref)                                                  | 1.15x slower                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 182 ms: 1.48x slower                                                   |
| nbody          | 119 ms                                                 | 261 ms: 2.20x slower                                                   |
| Geometric mean | (ref)                                                  | 1.48x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.73 ms: 1.08x faster                                                  |
| regex_v8       | 32.5 ms                                                | 34.5 ms: 1.06x slower                                                  |
| regex_dna      | 278 ms                                                 | 307 ms: 1.10x slower                                                   |
| regex_compile  | 187 ms                                                 | 271 ms: 1.45x slower                                                   |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 45.8 us: 1.15x faster                                                  |
| xml_etree_parse      | 241 ms                                                 | 211 ms: 1.14x faster                                                   |
| xml_etree_iterparse  | 169 ms                                                 | 159 ms: 1.07x faster                                                   |
| unpickle_list        | 6.83 us                                                | 7.52 us: 1.10x slower                                                  |
| xml_etree_generate   | 127 ms                                                 | 163 ms: 1.28x slower                                                   |
| json_dumps           | 14.3 ms                                                | 19.5 ms: 1.36x slower                                                  |
| tomli_loads          | 2.88 sec                                               | 4.08 sec: 1.41x slower                                                 |
| xml_etree_process    | 83.7 ms                                                | 125 ms: 1.49x slower                                                   |
| unpickle_pure_python | 300 us                                                 | 553 us: 1.85x slower                                                   |
| pickle_pure_python   | 436 us                                                 | 811 us: 1.86x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.17x slower                                                           |

Benchmark hidden because not significant (4): pickle, pickle_list, unpickle, json_loads

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 19.0 ms: 1.08x slower                                                  |
| python_startup         | 23.7 ms                                                | 27.9 ms: 1.18x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.13x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 121 ms: 1.80x slower                                                   |
| genshi_text     | 30.2 ms                                                | 55.5 ms: 1.84x slower                                                  |
| django_template | 44.9 ms                                                | 85.2 ms: 1.90x slower                                                  |
| mako            | 15.7 ms                                                | 30.1 ms: 1.91x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.86x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241117-linux-x86_64-python-acbd5c9c6c62dac34d2e-3.14.0a1+-acbd5c9 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| gc_traversal             | 5.86 ms                                                | 3.88 ms: 1.51x faster                                                  |
| pickle_dict              | 52.7 us                                                | 45.8 us: 1.15x faster                                                  |
| xml_etree_parse          | 241 ms                                                 | 211 ms: 1.14x faster                                                   |
| regex_effbot             | 5.13 ms                                                | 4.73 ms: 1.08x faster                                                  |
| xml_etree_iterparse      | 169 ms                                                 | 159 ms: 1.07x faster                                                   |
| asyncio_websockets       | 748 ms                                                 | 721 ms: 1.04x faster                                                   |
| pathlib                  | 31.6 ms                                                | 33.2 ms: 1.05x slower                                                  |
| regex_v8                 | 32.5 ms                                                | 34.5 ms: 1.06x slower                                                  |
| sqlite_synth             | 3.87 us                                                | 4.11 us: 1.06x slower                                                  |
| json                     | 6.85 ms                                                | 7.37 ms: 1.08x slower                                                  |
| python_startup_no_site   | 17.6 ms                                                | 19.0 ms: 1.08x slower                                                  |
| unpickle_list            | 6.83 us                                                | 7.52 us: 1.10x slower                                                  |
| regex_dna                | 278 ms                                                 | 307 ms: 1.10x slower                                                   |
| scimark_fft              | 500 ms                                                 | 555 ms: 1.11x slower                                                   |
| asyncio_tcp              | 923 ms                                                 | 1.05 sec: 1.13x slower                                                 |
| docutils                 | 4.00 sec                                               | 4.64 sec: 1.16x slower                                                 |
| pycparser                | 1.79 sec                                               | 2.08 sec: 1.16x slower                                                 |
| asyncio_tcp_ssl          | 2.81 sec                                               | 3.29 sec: 1.17x slower                                                 |
| python_startup           | 23.7 ms                                                | 27.9 ms: 1.18x slower                                                  |
| async_generators         | 589 ms                                                 | 696 ms: 1.18x slower                                                   |
| deepcopy                 | 468 us                                                 | 556 us: 1.19x slower                                                   |
| pylint                   | 465 ms                                                 | 561 ms: 1.21x slower                                                   |
| mdp                      | 3.97 sec                                               | 4.88 sec: 1.23x slower                                                 |
| scimark_sparse_mat_mult  | 6.70 ms                                                | 8.31 ms: 1.24x slower                                                  |
| meteor_contest           | 146 ms                                                 | 186 ms: 1.27x slower                                                   |
| xml_etree_generate       | 127 ms                                                 | 163 ms: 1.28x slower                                                   |
| generators               | 41.1 ms                                                | 53.0 ms: 1.29x slower                                                  |
| deepcopy_memo            | 52.4 us                                                | 69.3 us: 1.32x slower                                                  |
| crypto_pyaes             | 107 ms                                                 | 143 ms: 1.33x slower                                                   |
| bpe_tokeniser            | 6.59 sec                                               | 8.82 sec: 1.34x slower                                                 |
| dulwich_log              | 100 ms                                                 | 135 ms: 1.35x slower                                                   |
| coroutines               | 29.5 ms                                                | 39.9 ms: 1.35x slower                                                  |
| json_dumps               | 14.3 ms                                                | 19.5 ms: 1.36x slower                                                  |
| nqueens                  | 117 ms                                                 | 159 ms: 1.37x slower                                                   |
| fannkuch                 | 540 ms                                                 | 760 ms: 1.41x slower                                                   |
| comprehensions           | 27.1 us                                                | 38.2 us: 1.41x slower                                                  |
| tomli_loads              | 2.88 sec                                               | 4.08 sec: 1.41x slower                                                 |
| 2to3                     | 456 ms                                                 | 653 ms: 1.43x slower                                                   |
| telco                    | 9.59 ms                                                | 13.7 ms: 1.43x slower                                                  |
| sqlglot_normalize        | 157 ms                                                 | 227 ms: 1.45x slower                                                   |
| pyflate                  | 727 ms                                                 | 1.06 sec: 1.45x slower                                                 |
| regex_compile            | 187 ms                                                 | 271 ms: 1.45x slower                                                   |
| sympy_integrate          | 29.8 ms                                                | 43.8 ms: 1.47x slower                                                  |
| typing_runtime_protocols | 224 us                                                 | 331 us: 1.47x slower                                                   |
| float                    | 123 ms                                                 | 182 ms: 1.48x slower                                                   |
| xml_etree_process        | 83.7 ms                                                | 125 ms: 1.49x slower                                                   |
| spectral_norm            | 156 ms                                                 | 234 ms: 1.51x slower                                                   |
| coverage                 | 95.4 ms                                                | 144 ms: 1.51x slower                                                   |
| deepcopy_reduce          | 4.04 us                                                | 6.17 us: 1.53x slower                                                  |
| html5lib                 | 88.9 ms                                                | 137 ms: 1.54x slower                                                   |
| sqlglot_optimize         | 76.0 ms                                                | 121 ms: 1.59x slower                                                   |
| logging_simple           | 9.45 us                                                | 15.3 us: 1.62x slower                                                  |
| scimark_monte_carlo      | 96.4 ms                                                | 158 ms: 1.64x slower                                                   |
| thrift                   | 1.06 ms                                                | 1.75 ms: 1.65x slower                                                  |
| pprint_pformat           | 1.98 sec                                               | 3.28 sec: 1.66x slower                                                 |
| richards_super           | 72.8 ms                                                | 123 ms: 1.68x slower                                                   |
| sympy_str                | 385 ms                                                 | 650 ms: 1.69x slower                                                   |
| richards                 | 60.3 ms                                                | 103 ms: 1.70x slower                                                   |
| pprint_safe_repr         | 967 ms                                                 | 1.66 sec: 1.71x slower                                                 |
| chaos                    | 84.9 ms                                                | 151 ms: 1.78x slower                                                   |
| logging_format           | 9.59 us                                                | 17.1 us: 1.79x slower                                                  |
| genshi_xml               | 67.6 ms                                                | 121 ms: 1.80x slower                                                   |
| raytrace                 | 408 ms                                                 | 736 ms: 1.80x slower                                                   |
| genshi_text              | 30.2 ms                                                | 55.5 ms: 1.84x slower                                                  |
| unpickle_pure_python     | 300 us                                                 | 553 us: 1.85x slower                                                   |
| logging_silent           | 139 ns                                                 | 257 ns: 1.85x slower                                                   |
| pickle_pure_python       | 436 us                                                 | 811 us: 1.86x slower                                                   |
| django_template          | 44.9 ms                                                | 85.2 ms: 1.90x slower                                                  |
| hexiom                   | 8.27 ms                                                | 15.8 ms: 1.91x slower                                                  |
| mako                     | 15.7 ms                                                | 30.1 ms: 1.91x slower                                                  |
| scimark_lu               | 152 ms                                                 | 292 ms: 1.92x slower                                                   |
| sqlglot_transpile        | 2.34 ms                                                | 4.51 ms: 1.93x slower                                                  |
| go                       | 172 ms                                                 | 344 ms: 2.00x slower                                                   |
| scimark_sor              | 167 ms                                                 | 337 ms: 2.02x slower                                                   |
| sympy_sum                | 222 ms                                                 | 453 ms: 2.04x slower                                                   |
| sympy_expand             | 582 ms                                                 | 1.22 sec: 2.09x slower                                                 |
| sqlglot_parse            | 1.79 ms                                                | 3.79 ms: 2.12x slower                                                  |
| nbody                    | 119 ms                                                 | 261 ms: 2.20x slower                                                   |
| deltablue                | 4.27 ms                                                | 11.4 ms: 2.68x slower                                                  |
| bench_mp_pool            | 20.7 ms                                                | 58.0 ms: 2.80x slower                                                  |
| unpack_sequence          | 60.2 ns                                                | 190 ns: 3.15x slower                                                   |
| Geometric mean           | (ref)                                                  | 1.41x slower                                                           |

Benchmark hidden because not significant (7): bench_thread_pool, pickle, pickle_list, unpickle, pidigits, json_loads, create_gc_cycles
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.35x
- 95% likely to have a slowdown of 1.34x
- 99% likely to have a slowdown of 1.29x

# Memory
- memory change: 1.20x