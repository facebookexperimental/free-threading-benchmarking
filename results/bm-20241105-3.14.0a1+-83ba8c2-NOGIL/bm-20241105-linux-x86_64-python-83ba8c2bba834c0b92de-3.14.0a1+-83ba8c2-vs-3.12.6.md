# Results vs. 3.12.6

- fork: python
- ref: 83ba8c2bba834c0b92de
- machine: linux-x86_64
- commit hash: 83ba8c2
- commit date: 2024-11-05
- overall geometric mean: 1.58x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.46x slower
- Memory change: 1.19x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 704 ms: 1.54x slower                                                   |
| docutils       | 4.00 sec                                               | 5.08 sec: 1.27x slower                                                 |
| html5lib       | 88.9 ms                                                | 148 ms: 1.66x slower                                                   |
| Geometric mean | (ref)                                                  | 1.48x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|--------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_tcp        | 923 ms                                                 | 1.07 sec: 1.16x slower                                                 |
| asyncio_tcp_ssl    | 2.81 sec                                               | 3.31 sec: 1.18x slower                                                 |
| async_generators   | 589 ms                                                 | 769 ms: 1.31x slower                                                   |
| asyncio_websockets | 748 ms                                                 | 1.02 sec: 1.37x slower                                                 |
| coroutines         | 29.5 ms                                                | 41.5 ms: 1.41x slower                                                  |
| Geometric mean     | (ref)                                                  | 1.28x slower                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 230 ms: 1.87x slower                                                   |
| nbody          | 119 ms                                                 | 328 ms: 2.75x slower                                                   |
| Geometric mean | (ref)                                                  | 1.73x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_dna      | 278 ms                                                 | 303 ms: 1.09x slower                                                   |
| regex_v8       | 32.5 ms                                                | 35.9 ms: 1.11x slower                                                  |
| regex_compile  | 187 ms                                                 | 328 ms: 1.76x slower                                                   |
| Geometric mean | (ref)                                                  | 1.21x slower                                                           |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_list          | 6.97 us                                                | 6.00 us: 1.16x faster                                                  |
| pickle_dict          | 52.7 us                                                | 46.4 us: 1.14x faster                                                  |
| xml_etree_parse      | 241 ms                                                 | 222 ms: 1.09x faster                                                   |
| xml_etree_iterparse  | 169 ms                                                 | 184 ms: 1.09x slower                                                   |
| unpickle_list        | 6.83 us                                                | 8.17 us: 1.20x slower                                                  |
| unpickle             | 21.2 us                                                | 26.6 us: 1.25x slower                                                  |
| json_loads           | 37.9 us                                                | 48.5 us: 1.28x slower                                                  |
| xml_etree_generate   | 127 ms                                                 | 172 ms: 1.36x slower                                                   |
| json_dumps           | 14.3 ms                                                | 21.5 ms: 1.50x slower                                                  |
| tomli_loads          | 2.88 sec                                               | 4.45 sec: 1.54x slower                                                 |
| xml_etree_process    | 83.7 ms                                                | 140 ms: 1.67x slower                                                   |
| unpickle_pure_python | 300 us                                                 | 622 us: 2.07x slower                                                   |
| pickle_pure_python   | 436 us                                                 | 907 us: 2.08x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.28x slower                                                           |

Benchmark hidden because not significant (1): pickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 19.9 ms: 1.13x slower                                                  |
| python_startup         | 23.7 ms                                                | 29.2 ms: 1.23x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.18x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| django_template | 44.9 ms                                                | 92.0 ms: 2.05x slower                                                  |
| mako            | 15.7 ms                                                | 33.8 ms: 2.15x slower                                                  |
| genshi_xml      | 67.6 ms                                                | 147 ms: 2.18x slower                                                   |
| genshi_text     | 30.2 ms                                                | 67.2 ms: 2.22x slower                                                  |
| Geometric mean  | (ref)                                                  | 2.15x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241105-linux-x86_64-python-83ba8c2bba834c0b92de-3.14.0a1+-83ba8c2 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_list              | 6.97 us                                                | 6.00 us: 1.16x faster                                                  |
| pickle_dict              | 52.7 us                                                | 46.4 us: 1.14x faster                                                  |
| xml_etree_parse          | 241 ms                                                 | 222 ms: 1.09x faster                                                   |
| xml_etree_iterparse      | 169 ms                                                 | 184 ms: 1.09x slower                                                   |
| regex_dna                | 278 ms                                                 | 303 ms: 1.09x slower                                                   |
| regex_v8                 | 32.5 ms                                                | 35.9 ms: 1.11x slower                                                  |
| python_startup_no_site   | 17.6 ms                                                | 19.9 ms: 1.13x slower                                                  |
| pathlib                  | 31.6 ms                                                | 36.6 ms: 1.16x slower                                                  |
| asyncio_tcp              | 923 ms                                                 | 1.07 sec: 1.16x slower                                                 |
| asyncio_tcp_ssl          | 2.81 sec                                               | 3.31 sec: 1.18x slower                                                 |
| unpickle_list            | 6.83 us                                                | 8.17 us: 1.20x slower                                                  |
| sqlite_synth             | 3.87 us                                                | 4.74 us: 1.22x slower                                                  |
| scimark_fft              | 500 ms                                                 | 614 ms: 1.23x slower                                                   |
| python_startup           | 23.7 ms                                                | 29.2 ms: 1.23x slower                                                  |
| json                     | 6.85 ms                                                | 8.55 ms: 1.25x slower                                                  |
| unpickle                 | 21.2 us                                                | 26.6 us: 1.25x slower                                                  |
| mdp                      | 3.97 sec                                               | 4.99 sec: 1.26x slower                                                 |
| docutils                 | 4.00 sec                                               | 5.08 sec: 1.27x slower                                                 |
| json_loads               | 37.9 us                                                | 48.5 us: 1.28x slower                                                  |
| async_generators         | 589 ms                                                 | 769 ms: 1.31x slower                                                   |
| pylint                   | 465 ms                                                 | 610 ms: 1.31x slower                                                   |
| xml_etree_generate       | 127 ms                                                 | 172 ms: 1.36x slower                                                   |
| deepcopy                 | 468 us                                                 | 637 us: 1.36x slower                                                   |
| asyncio_websockets       | 748 ms                                                 | 1.02 sec: 1.37x slower                                                 |
| fannkuch                 | 540 ms                                                 | 761 ms: 1.41x slower                                                   |
| coroutines               | 29.5 ms                                                | 41.5 ms: 1.41x slower                                                  |
| scimark_sparse_mat_mult  | 6.70 ms                                                | 9.62 ms: 1.44x slower                                                  |
| dulwich_log              | 100 ms                                                 | 146 ms: 1.46x slower                                                   |
| pycparser                | 1.79 sec                                               | 2.63 sec: 1.47x slower                                                 |
| crypto_pyaes             | 107 ms                                                 | 158 ms: 1.47x slower                                                   |
| json_dumps               | 14.3 ms                                                | 21.5 ms: 1.50x slower                                                  |
| meteor_contest           | 146 ms                                                 | 220 ms: 1.51x slower                                                   |
| coverage                 | 95.4 ms                                                | 145 ms: 1.52x slower                                                   |
| tomli_loads              | 2.88 sec                                               | 4.45 sec: 1.54x slower                                                 |
| 2to3                     | 456 ms                                                 | 704 ms: 1.54x slower                                                   |
| nqueens                  | 117 ms                                                 | 181 ms: 1.55x slower                                                   |
| deepcopy_memo            | 52.4 us                                                | 81.5 us: 1.55x slower                                                  |
| deepcopy_reduce          | 4.04 us                                                | 6.30 us: 1.56x slower                                                  |
| pyflate                  | 727 ms                                                 | 1.14 sec: 1.56x slower                                                 |
| spectral_norm            | 156 ms                                                 | 244 ms: 1.57x slower                                                   |
| telco                    | 9.59 ms                                                | 15.2 ms: 1.58x slower                                                  |
| bpe_tokeniser            | 6.59 sec                                               | 10.5 sec: 1.59x slower                                                 |
| sympy_integrate          | 29.8 ms                                                | 47.3 ms: 1.59x slower                                                  |
| generators               | 41.1 ms                                                | 67.3 ms: 1.64x slower                                                  |
| html5lib                 | 88.9 ms                                                | 148 ms: 1.66x slower                                                   |
| xml_etree_process        | 83.7 ms                                                | 140 ms: 1.67x slower                                                   |
| comprehensions           | 27.1 us                                                | 45.7 us: 1.69x slower                                                  |
| scimark_monte_carlo      | 96.4 ms                                                | 164 ms: 1.70x slower                                                   |
| typing_runtime_protocols | 224 us                                                 | 385 us: 1.72x slower                                                   |
| sqlglot_normalize        | 157 ms                                                 | 271 ms: 1.72x slower                                                   |
| regex_compile            | 187 ms                                                 | 328 ms: 1.76x slower                                                   |
| logging_simple           | 9.45 us                                                | 16.9 us: 1.79x slower                                                  |
| pprint_pformat           | 1.98 sec                                               | 3.58 sec: 1.81x slower                                                 |
| thrift                   | 1.06 ms                                                | 1.93 ms: 1.82x slower                                                  |
| pprint_safe_repr         | 967 ms                                                 | 1.78 sec: 1.84x slower                                                 |
| sqlglot_optimize         | 76.0 ms                                                | 141 ms: 1.85x slower                                                   |
| sympy_str                | 385 ms                                                 | 721 ms: 1.87x slower                                                   |
| float                    | 123 ms                                                 | 230 ms: 1.87x slower                                                   |
| logging_silent           | 139 ns                                                 | 272 ns: 1.96x slower                                                   |
| richards_super           | 72.8 ms                                                | 144 ms: 1.97x slower                                                   |
| logging_format           | 9.59 us                                                | 19.5 us: 2.03x slower                                                  |
| django_template          | 44.9 ms                                                | 92.0 ms: 2.05x slower                                                  |
| unpickle_pure_python     | 300 us                                                 | 622 us: 2.07x slower                                                   |
| chaos                    | 84.9 ms                                                | 176 ms: 2.08x slower                                                   |
| pickle_pure_python       | 436 us                                                 | 907 us: 2.08x slower                                                   |
| richards                 | 60.3 ms                                                | 127 ms: 2.10x slower                                                   |
| raytrace                 | 408 ms                                                 | 872 ms: 2.14x slower                                                   |
| scimark_lu               | 152 ms                                                 | 326 ms: 2.14x slower                                                   |
| mako                     | 15.7 ms                                                | 33.8 ms: 2.15x slower                                                  |
| sympy_sum                | 222 ms                                                 | 476 ms: 2.15x slower                                                   |
| scimark_sor              | 167 ms                                                 | 358 ms: 2.15x slower                                                   |
| hexiom                   | 8.27 ms                                                | 17.9 ms: 2.16x slower                                                  |
| genshi_xml               | 67.6 ms                                                | 147 ms: 2.18x slower                                                   |
| genshi_text              | 30.2 ms                                                | 67.2 ms: 2.22x slower                                                  |
| sqlglot_transpile        | 2.34 ms                                                | 5.25 ms: 2.25x slower                                                  |
| sympy_expand             | 582 ms                                                 | 1.33 sec: 2.29x slower                                                 |
| go                       | 172 ms                                                 | 409 ms: 2.38x slower                                                   |
| sqlglot_parse            | 1.79 ms                                                | 4.35 ms: 2.43x slower                                                  |
| nbody                    | 119 ms                                                 | 328 ms: 2.75x slower                                                   |
| bench_mp_pool            | 20.7 ms                                                | 61.6 ms: 2.98x slower                                                  |
| deltablue                | 4.27 ms                                                | 12.8 ms: 3.01x slower                                                  |
| unpack_sequence          | 60.2 ns                                                | 227 ns: 3.77x slower                                                   |
| Geometric mean           | (ref)                                                  | 1.58x slower                                                           |

Benchmark hidden because not significant (6): pickle, pidigits, regex_effbot, create_gc_cycles, gc_traversal, bench_thread_pool
Ignored benchmarks (17) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative, tornado_http

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.50x
- 95% likely to have a slowdown of 1.49x
- 99% likely to have a slowdown of 1.46x

# Memory
- memory change: 1.19x