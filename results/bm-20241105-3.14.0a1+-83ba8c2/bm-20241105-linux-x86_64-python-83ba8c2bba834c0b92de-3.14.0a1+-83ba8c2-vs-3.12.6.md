# Results vs. 3.12.6

- fork: python
- ref: 83ba8c2bba834c0b92de
- machine: linux-x86_64
- commit hash: 83ba8c2
- commit date: 2024-11-05
- overall geometric mean: 1.12x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.06x slower
- Memory change: 1.02x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 488 ms: 1.07x slower                                                   |
| docutils       | 4.00 sec                                               | 4.21 sec: 1.05x slower                                                 |
| html5lib       | 88.9 ms                                                | 97.6 ms: 1.10x slower                                                  |
| Geometric mean | (ref)                                                  | 1.07x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|--------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| async_generators   | 589 ms                                                 | 684 ms: 1.16x slower                                                   |
| coroutines         | 29.5 ms                                                | 34.7 ms: 1.17x slower                                                  |
| asyncio_websockets | 748 ms                                                 | 998 ms: 1.33x slower                                                   |
| Geometric mean     | (ref)                                                  | 1.12x slower                                                           |

Benchmark hidden because not significant (2): asyncio_tcp_ssl, asyncio_tcp

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pidigits       | 250 ms                                                 | 236 ms: 1.06x faster                                                   |
| float          | 123 ms                                                 | 147 ms: 1.20x slower                                                   |
| nbody          | 119 ms                                                 | 199 ms: 1.67x slower                                                   |
| Geometric mean | (ref)                                                  | 1.24x slower                                                           |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 5.43 ms: 1.06x slower                                                  |
| regex_compile  | 187 ms                                                 | 206 ms: 1.10x slower                                                   |
| regex_v8       | 32.5 ms                                                | 36.0 ms: 1.11x slower                                                  |
| Geometric mean | (ref)                                                  | 1.08x slower                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 44.6 us: 1.18x faster                                                  |
| xml_etree_parse      | 241 ms                                                 | 222 ms: 1.08x faster                                                   |
| tomli_loads          | 2.88 sec                                               | 3.06 sec: 1.06x slower                                                 |
| xml_etree_iterparse  | 169 ms                                                 | 180 ms: 1.06x slower                                                   |
| unpickle_pure_python | 300 us                                                 | 339 us: 1.13x slower                                                   |
| xml_etree_generate   | 127 ms                                                 | 144 ms: 1.14x slower                                                   |
| json_dumps           | 14.3 ms                                                | 16.4 ms: 1.14x slower                                                  |
| unpickle_list        | 6.83 us                                                | 7.84 us: 1.15x slower                                                  |
| xml_etree_process    | 83.7 ms                                                | 97.7 ms: 1.17x slower                                                  |
| pickle_pure_python   | 436 us                                                 | 533 us: 1.22x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.06x slower                                                           |

Benchmark hidden because not significant (4): json_loads, pickle_list, unpickle, pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 15.7 ms: 1.12x faster                                                  |
| python_startup         | 23.7 ms                                                | 22.0 ms: 1.08x faster                                                  |
| Geometric mean         | (ref)                                                  | 1.10x faster                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| mako            | 15.7 ms                                                | 19.8 ms: 1.26x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 87.2 ms: 1.29x slower                                                  |
| django_template | 44.9 ms                                                | 58.9 ms: 1.31x slower                                                  |
| genshi_text     | 30.2 ms                                                | 41.2 ms: 1.36x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.31x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| bench_thread_pool        | 3.48 ms                                                | 2.90 ms: 1.20x faster                                                  |
| pickle_dict              | 52.7 us                                                | 44.6 us: 1.18x faster                                                  |
| python_startup_no_site   | 17.6 ms                                                | 15.7 ms: 1.12x faster                                                  |
| deepcopy                 | 468 us                                                 | 427 us: 1.10x faster                                                   |
| pathlib                  | 31.6 ms                                                | 29.1 ms: 1.08x faster                                                  |
| xml_etree_parse          | 241 ms                                                 | 222 ms: 1.08x faster                                                   |
| python_startup           | 23.7 ms                                                | 22.0 ms: 1.08x faster                                                  |
| deepcopy_memo            | 52.4 us                                                | 49.2 us: 1.07x faster                                                  |
| pidigits                 | 250 ms                                                 | 236 ms: 1.06x faster                                                   |
| mdp                      | 3.97 sec                                               | 4.08 sec: 1.03x slower                                                 |
| json                     | 6.85 ms                                                | 7.17 ms: 1.05x slower                                                  |
| comprehensions           | 27.1 us                                                | 28.4 us: 1.05x slower                                                  |
| deepcopy_reduce          | 4.04 us                                                | 4.23 us: 1.05x slower                                                  |
| scimark_monte_carlo      | 96.4 ms                                                | 101 ms: 1.05x slower                                                   |
| meteor_contest           | 146 ms                                                 | 154 ms: 1.05x slower                                                   |
| docutils                 | 4.00 sec                                               | 4.21 sec: 1.05x slower                                                 |
| regex_effbot             | 5.13 ms                                                | 5.43 ms: 1.06x slower                                                  |
| sympy_str                | 385 ms                                                 | 408 ms: 1.06x slower                                                   |
| tomli_loads              | 2.88 sec                                               | 3.06 sec: 1.06x slower                                                 |
| xml_etree_iterparse      | 169 ms                                                 | 180 ms: 1.06x slower                                                   |
| logging_simple           | 9.45 us                                                | 10.1 us: 1.07x slower                                                  |
| 2to3                     | 456 ms                                                 | 488 ms: 1.07x slower                                                   |
| pprint_safe_repr         | 967 ms                                                 | 1.04 sec: 1.08x slower                                                 |
| dulwich_log              | 100 ms                                                 | 109 ms: 1.08x slower                                                   |
| sqlglot_transpile        | 2.34 ms                                                | 2.55 ms: 1.09x slower                                                  |
| bpe_tokeniser            | 6.59 sec                                               | 7.22 sec: 1.10x slower                                                 |
| html5lib                 | 88.9 ms                                                | 97.6 ms: 1.10x slower                                                  |
| generators               | 41.1 ms                                                | 45.2 ms: 1.10x slower                                                  |
| pylint                   | 465 ms                                                 | 511 ms: 1.10x slower                                                   |
| regex_compile            | 187 ms                                                 | 206 ms: 1.10x slower                                                   |
| regex_v8                 | 32.5 ms                                                | 36.0 ms: 1.11x slower                                                  |
| scimark_lu               | 152 ms                                                 | 169 ms: 1.11x slower                                                   |
| sympy_sum                | 222 ms                                                 | 247 ms: 1.11x slower                                                   |
| gc_traversal             | 5.86 ms                                                | 6.55 ms: 1.12x slower                                                  |
| chaos                    | 84.9 ms                                                | 95.4 ms: 1.12x slower                                                  |
| logging_format           | 9.59 us                                                | 10.8 us: 1.13x slower                                                  |
| unpickle_pure_python     | 300 us                                                 | 339 us: 1.13x slower                                                   |
| xml_etree_generate       | 127 ms                                                 | 144 ms: 1.14x slower                                                   |
| thrift                   | 1.06 ms                                                | 1.20 ms: 1.14x slower                                                  |
| raytrace                 | 408 ms                                                 | 465 ms: 1.14x slower                                                   |
| json_dumps               | 14.3 ms                                                | 16.4 ms: 1.14x slower                                                  |
| unpickle_list            | 6.83 us                                                | 7.84 us: 1.15x slower                                                  |
| go                       | 172 ms                                                 | 198 ms: 1.15x slower                                                   |
| pprint_pformat           | 1.98 sec                                               | 2.28 sec: 1.15x slower                                                 |
| scimark_sparse_mat_mult  | 6.70 ms                                                | 7.74 ms: 1.15x slower                                                  |
| typing_runtime_protocols | 224 us                                                 | 259 us: 1.15x slower                                                   |
| async_generators         | 589 ms                                                 | 684 ms: 1.16x slower                                                   |
| pycparser                | 1.79 sec                                               | 2.09 sec: 1.17x slower                                                 |
| xml_etree_process        | 83.7 ms                                                | 97.7 ms: 1.17x slower                                                  |
| coroutines               | 29.5 ms                                                | 34.7 ms: 1.17x slower                                                  |
| unpack_sequence          | 60.2 ns                                                | 70.7 ns: 1.17x slower                                                  |
| sqlglot_parse            | 1.79 ms                                                | 2.10 ms: 1.18x slower                                                  |
| hexiom                   | 8.27 ms                                                | 9.80 ms: 1.19x slower                                                  |
| logging_silent           | 139 ns                                                 | 165 ns: 1.19x slower                                                   |
| telco                    | 9.59 ms                                                | 11.4 ms: 1.19x slower                                                  |
| float                    | 123 ms                                                 | 147 ms: 1.20x slower                                                   |
| sympy_expand             | 582 ms                                                 | 698 ms: 1.20x slower                                                   |
| richards_super           | 72.8 ms                                                | 87.5 ms: 1.20x slower                                                  |
| spectral_norm            | 156 ms                                                 | 188 ms: 1.21x slower                                                   |
| richards                 | 60.3 ms                                                | 73.1 ms: 1.21x slower                                                  |
| coverage                 | 95.4 ms                                                | 116 ms: 1.21x slower                                                   |
| sqlglot_normalize        | 157 ms                                                 | 191 ms: 1.22x slower                                                   |
| pickle_pure_python       | 436 us                                                 | 533 us: 1.22x slower                                                   |
| sqlglot_optimize         | 76.0 ms                                                | 93.8 ms: 1.23x slower                                                  |
| scimark_sor              | 167 ms                                                 | 209 ms: 1.26x slower                                                   |
| mako                     | 15.7 ms                                                | 19.8 ms: 1.26x slower                                                  |
| genshi_xml               | 67.6 ms                                                | 87.2 ms: 1.29x slower                                                  |
| create_gc_cycles         | 1.94 ms                                                | 2.52 ms: 1.30x slower                                                  |
| django_template          | 44.9 ms                                                | 58.9 ms: 1.31x slower                                                  |
| asyncio_websockets       | 748 ms                                                 | 998 ms: 1.33x slower                                                   |
| deltablue                | 4.27 ms                                                | 5.74 ms: 1.35x slower                                                  |
| genshi_text              | 30.2 ms                                                | 41.2 ms: 1.36x slower                                                  |
| nbody                    | 119 ms                                                 | 199 ms: 1.67x slower                                                   |
| bench_mp_pool            | 20.7 ms                                                | 77.7 ms: 3.76x slower                                                  |
| Geometric mean           | (ref)                                                  | 1.12x slower                                                           |

Benchmark hidden because not significant (14): crypto_pyaes, asyncio_tcp_ssl, asyncio_tcp, json_loads, pickle_list, nqueens, sympy_integrate, scimark_fft, sqlite_synth, regex_dna, unpickle, fannkuch, pyflate, pickle
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.08x
- 95% likely to have a slowdown of 1.07x
- 99% likely to have a slowdown of 1.06x

# Memory
- memory change: 1.02x