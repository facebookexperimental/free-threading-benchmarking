# Results vs. 3.12.6

- fork: python
- ref: d0bfff47fb2aea9272b5
- machine: linux-x86_64
- commit hash: d0bfff4
- commit date: 2024-10-21
- overall geometric mean: 1.51x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.41x slower
- Memory change: 1.17x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| 2to3           | 456 ms                                                 | 691 ms: 1.51x slower                                                   |
| docutils       | 4.00 sec                                               | 4.96 sec: 1.24x slower                                                 |
| html5lib       | 88.9 ms                                                | 155 ms: 1.75x slower                                                   |
| tornado_http   | 266 ms                                                 | 409 ms: 1.54x slower                                                   |
| Geometric mean | (ref)                                                  | 1.50x slower                                                           |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|--------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| asyncio_websockets | 748 ms                                                 | 775 ms: 1.04x slower                                                   |
| asyncio_tcp_ssl    | 2.81 sec                                               | 3.37 sec: 1.20x slower                                                 |
| async_generators   | 589 ms                                                 | 754 ms: 1.28x slower                                                   |
| asyncio_tcp        | 923 ms                                                 | 1.22 sec: 1.32x slower                                                 |
| coroutines         | 29.5 ms                                                | 41.3 ms: 1.40x slower                                                  |
| Geometric mean     | (ref)                                                  | 1.24x slower                                                           |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| float          | 123 ms                                                 | 190 ms: 1.54x slower                                                   |
| nbody          | 119 ms                                                 | 290 ms: 2.43x slower                                                   |
| Geometric mean | (ref)                                                  | 1.55x slower                                                           |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| regex_effbot   | 5.13 ms                                                | 4.70 ms: 1.09x faster                                                  |
| regex_v8       | 32.5 ms                                                | 34.8 ms: 1.07x slower                                                  |
| regex_compile  | 187 ms                                                 | 291 ms: 1.56x slower                                                   |
| Geometric mean | (ref)                                                  | 1.12x slower                                                           |

Benchmark hidden because not significant (1): regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|----------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_dict          | 52.7 us                                                | 46.6 us: 1.13x faster                                                  |
| pickle_list          | 6.97 us                                                | 6.40 us: 1.09x faster                                                  |
| pickle               | 16.4 us                                                | 15.2 us: 1.07x faster                                                  |
| json_loads           | 37.9 us                                                | 40.4 us: 1.07x slower                                                  |
| unpickle_list        | 6.83 us                                                | 7.86 us: 1.15x slower                                                  |
| unpickle             | 21.2 us                                                | 25.1 us: 1.18x slower                                                  |
| xml_etree_generate   | 127 ms                                                 | 164 ms: 1.29x slower                                                   |
| json_dumps           | 14.3 ms                                                | 21.2 ms: 1.48x slower                                                  |
| tomli_loads          | 2.88 sec                                               | 4.36 sec: 1.51x slower                                                 |
| xml_etree_process    | 83.7 ms                                                | 131 ms: 1.57x slower                                                   |
| pickle_pure_python   | 436 us                                                 | 777 us: 1.78x slower                                                   |
| unpickle_pure_python | 300 us                                                 | 563 us: 1.88x slower                                                   |
| Geometric mean       | (ref)                                                  | 1.23x slower                                                           |

Benchmark hidden because not significant (2): xml_etree_parse, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| python_startup_no_site | 17.6 ms                                                | 20.6 ms: 1.17x slower                                                  |
| python_startup         | 23.7 ms                                                | 33.6 ms: 1.42x slower                                                  |
| Geometric mean         | (ref)                                                  | 1.29x slower                                                           |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|-----------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| genshi_xml      | 67.6 ms                                                | 110 ms: 1.62x slower                                                   |
| django_template | 44.9 ms                                                | 82.2 ms: 1.83x slower                                                  |
| genshi_text     | 30.2 ms                                                | 60.5 ms: 2.00x slower                                                  |
| mako            | 15.7 ms                                                | 32.3 ms: 2.05x slower                                                  |
| Geometric mean  | (ref)                                                  | 1.87x slower                                                           |

All benchmarks:
===============

| Benchmark                | bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b | bm-20241021-linux-x86_64-python-d0bfff47fb2aea9272b5-3.14.0a1+-d0bfff4 |
|--------------------------|:------------------------------------------------------:|:----------------------------------------------------------------------:|
| pickle_dict              | 52.7 us                                                | 46.6 us: 1.13x faster                                                  |
| regex_effbot             | 5.13 ms                                                | 4.70 ms: 1.09x faster                                                  |
| pickle_list              | 6.97 us                                                | 6.40 us: 1.09x faster                                                  |
| pickle                   | 16.4 us                                                | 15.2 us: 1.07x faster                                                  |
| asyncio_websockets       | 748 ms                                                 | 775 ms: 1.04x slower                                                   |
| json_loads               | 37.9 us                                                | 40.4 us: 1.07x slower                                                  |
| regex_v8                 | 32.5 ms                                                | 34.8 ms: 1.07x slower                                                  |
| json                     | 6.85 ms                                                | 7.43 ms: 1.09x slower                                                  |
| bench_thread_pool        | 3.48 ms                                                | 3.93 ms: 1.13x slower                                                  |
| sqlite_synth             | 3.87 us                                                | 4.46 us: 1.15x slower                                                  |
| unpickle_list            | 6.83 us                                                | 7.86 us: 1.15x slower                                                  |
| pathlib                  | 31.6 ms                                                | 36.6 ms: 1.16x slower                                                  |
| python_startup_no_site   | 17.6 ms                                                | 20.6 ms: 1.17x slower                                                  |
| unpickle                 | 21.2 us                                                | 25.1 us: 1.18x slower                                                  |
| asyncio_tcp_ssl          | 2.81 sec                                               | 3.37 sec: 1.20x slower                                                 |
| deepcopy                 | 468 us                                                 | 564 us: 1.21x slower                                                   |
| docutils                 | 4.00 sec                                               | 4.96 sec: 1.24x slower                                                 |
| mdp                      | 3.97 sec                                               | 5.07 sec: 1.28x slower                                                 |
| pycparser                | 1.79 sec                                               | 2.29 sec: 1.28x slower                                                 |
| async_generators         | 589 ms                                                 | 754 ms: 1.28x slower                                                   |
| xml_etree_generate       | 127 ms                                                 | 164 ms: 1.29x slower                                                   |
| scimark_fft              | 500 ms                                                 | 658 ms: 1.32x slower                                                   |
| asyncio_tcp              | 923 ms                                                 | 1.22 sec: 1.32x slower                                                 |
| generators               | 41.1 ms                                                | 54.5 ms: 1.33x slower                                                  |
| pylint                   | 465 ms                                                 | 618 ms: 1.33x slower                                                   |
| crypto_pyaes             | 107 ms                                                 | 145 ms: 1.35x slower                                                   |
| deepcopy_memo            | 52.4 us                                                | 72.0 us: 1.37x slower                                                  |
| nqueens                  | 117 ms                                                 | 163 ms: 1.40x slower                                                   |
| coroutines               | 29.5 ms                                                | 41.3 ms: 1.40x slower                                                  |
| python_startup           | 23.7 ms                                                | 33.6 ms: 1.42x slower                                                  |
| scimark_sparse_mat_mult  | 6.70 ms                                                | 9.53 ms: 1.42x slower                                                  |
| comprehensions           | 27.1 us                                                | 39.0 us: 1.44x slower                                                  |
| fannkuch                 | 540 ms                                                 | 790 ms: 1.46x slower                                                   |
| deepcopy_reduce          | 4.04 us                                                | 5.93 us: 1.47x slower                                                  |
| dulwich_log              | 100 ms                                                 | 148 ms: 1.48x slower                                                   |
| json_dumps               | 14.3 ms                                                | 21.2 ms: 1.48x slower                                                  |
| telco                    | 9.59 ms                                                | 14.2 ms: 1.49x slower                                                  |
| sqlglot_normalize        | 157 ms                                                 | 235 ms: 1.50x slower                                                   |
| tomli_loads              | 2.88 sec                                               | 4.36 sec: 1.51x slower                                                 |
| 2to3                     | 456 ms                                                 | 691 ms: 1.51x slower                                                   |
| coverage                 | 95.4 ms                                                | 146 ms: 1.53x slower                                                   |
| tornado_http             | 266 ms                                                 | 409 ms: 1.54x slower                                                   |
| bpe_tokeniser            | 6.59 sec                                               | 10.2 sec: 1.54x slower                                                 |
| float                    | 123 ms                                                 | 190 ms: 1.54x slower                                                   |
| sympy_integrate          | 29.8 ms                                                | 46.2 ms: 1.55x slower                                                  |
| pyflate                  | 727 ms                                                 | 1.13 sec: 1.56x slower                                                 |
| regex_compile            | 187 ms                                                 | 291 ms: 1.56x slower                                                   |
| thrift                   | 1.06 ms                                                | 1.66 ms: 1.56x slower                                                  |
| xml_etree_process        | 83.7 ms                                                | 131 ms: 1.57x slower                                                   |
| typing_runtime_protocols | 224 us                                                 | 352 us: 1.57x slower                                                   |
| meteor_contest           | 146 ms                                                 | 230 ms: 1.57x slower                                                   |
| genshi_xml               | 67.6 ms                                                | 110 ms: 1.62x slower                                                   |
| sqlglot_optimize         | 76.0 ms                                                | 125 ms: 1.65x slower                                                   |
| spectral_norm            | 156 ms                                                 | 257 ms: 1.65x slower                                                   |
| logging_simple           | 9.45 us                                                | 15.7 us: 1.66x slower                                                  |
| richards_super           | 72.8 ms                                                | 126 ms: 1.73x slower                                                   |
| html5lib                 | 88.9 ms                                                | 155 ms: 1.75x slower                                                   |
| richards                 | 60.3 ms                                                | 106 ms: 1.75x slower                                                   |
| pickle_pure_python       | 436 us                                                 | 777 us: 1.78x slower                                                   |
| sympy_str                | 385 ms                                                 | 690 ms: 1.79x slower                                                   |
| django_template          | 44.9 ms                                                | 82.2 ms: 1.83x slower                                                  |
| pprint_pformat           | 1.98 sec                                               | 3.63 sec: 1.83x slower                                                 |
| logging_format           | 9.59 us                                                | 17.6 us: 1.84x slower                                                  |
| logging_silent           | 139 ns                                                 | 258 ns: 1.85x slower                                                   |
| unpickle_pure_python     | 300 us                                                 | 563 us: 1.88x slower                                                   |
| scimark_monte_carlo      | 96.4 ms                                                | 186 ms: 1.93x slower                                                   |
| pprint_safe_repr         | 967 ms                                                 | 1.88 sec: 1.95x slower                                                 |
| chaos                    | 84.9 ms                                                | 166 ms: 1.96x slower                                                   |
| raytrace                 | 408 ms                                                 | 811 ms: 1.99x slower                                                   |
| genshi_text              | 30.2 ms                                                | 60.5 ms: 2.00x slower                                                  |
| mako                     | 15.7 ms                                                | 32.3 ms: 2.05x slower                                                  |
| scimark_lu               | 152 ms                                                 | 313 ms: 2.06x slower                                                   |
| sqlglot_transpile        | 2.34 ms                                                | 4.99 ms: 2.14x slower                                                  |
| hexiom                   | 8.27 ms                                                | 18.0 ms: 2.18x slower                                                  |
| sympy_sum                | 222 ms                                                 | 488 ms: 2.20x slower                                                   |
| go                       | 172 ms                                                 | 381 ms: 2.21x slower                                                   |
| scimark_sor              | 167 ms                                                 | 373 ms: 2.24x slower                                                   |
| sqlglot_parse            | 1.79 ms                                                | 4.06 ms: 2.27x slower                                                  |
| sympy_expand             | 582 ms                                                 | 1.36 sec: 2.33x slower                                                 |
| nbody                    | 119 ms                                                 | 290 ms: 2.43x slower                                                   |
| deltablue                | 4.27 ms                                                | 11.5 ms: 2.68x slower                                                  |
| bench_mp_pool            | 20.7 ms                                                | 62.2 ms: 3.01x slower                                                  |
| unpack_sequence          | 60.2 ns                                                | 193 ns: 3.21x slower                                                   |
| Geometric mean           | (ref)                                                  | 1.51x slower                                                           |

Benchmark hidden because not significant (6): pidigits, gc_traversal, create_gc_cycles, regex_dna, xml_etree_parse, xml_etree_iterparse
Ignored benchmarks (16) of results/bm-20240906-3.12.6-a4a2d2b/bm-20240906-linux-x86_64-python-v3.12.6-3.12.6-a4a2d2b.json: aiohttp, async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, chameleon, dask, flaskblogging, gunicorn, mypy2, sqlalchemy_declarative, sqlalchemy_imperative

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.48x
- 95% likely to have a slowdown of 1.46x
- 99% likely to have a slowdown of 1.41x

# Memory
- memory change: 1.17x