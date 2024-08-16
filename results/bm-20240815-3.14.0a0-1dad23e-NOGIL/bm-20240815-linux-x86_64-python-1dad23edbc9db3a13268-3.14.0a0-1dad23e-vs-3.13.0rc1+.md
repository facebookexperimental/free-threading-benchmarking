# Results vs. 3.13.0rc1+

- fork: python
- ref: 1dad23edbc9db3a13268
- machine: linux-x86_64
- commit hash: 1dad23e
- commit date: 2024-08-15
- overall geometric mean: 1.44x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.32x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 442 ms                                                  | 687 ms: 1.56x slower                                                  |
| docutils       | 4.01 sec                                                | 5.35 sec: 1.34x slower                                                |
| html5lib       | 98.1 ms                                                 | 147 ms: 1.50x slower                                                  |
| tornado_http   | 248 ms                                                  | 350 ms: 1.41x slower                                                  |
| Geometric mean | (ref)                                                   | 1.45x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|--------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg   | 1.46 sec                                                | 1.14 sec: 1.28x faster                                                |
| async_tree_io      | 1.38 sec                                                | 1.28 sec: 1.08x faster                                                |
| async_tree_none_tg | 521 ms                                                  | 490 ms: 1.06x faster                                                  |
| async_tree_none    | 576 ms                                                  | 626 ms: 1.09x slower                                                  |
| asyncio_tcp        | 985 ms                                                  | 1.16 sec: 1.17x slower                                                |
| async_generators   | 592 ms                                                  | 731 ms: 1.24x slower                                                  |
| asyncio_tcp_ssl    | 2.79 sec                                                | 3.47 sec: 1.24x slower                                                |
| coroutines         | 29.2 ms                                                 | 42.9 ms: 1.47x slower                                                 |
| Geometric mean     | (ref)                                                   | 1.06x slower                                                          |

Benchmark hidden because not significant (5): async_tree_cpu_io_mixed_tg, async_tree_memoization_tg, asyncio_websockets, async_tree_cpu_io_mixed, async_tree_memoization

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 115 ms                                                  | 195 ms: 1.70x slower                                                  |
| nbody          | 124 ms                                                  | 307 ms: 2.48x slower                                                  |
| Geometric mean | (ref)                                                   | 1.62x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_dna      | 288 ms                                                  | 300 ms: 1.04x slower                                                  |
| regex_v8       | 32.4 ms                                                 | 36.8 ms: 1.13x slower                                                 |
| regex_compile  | 177 ms                                                  | 310 ms: 1.75x slower                                                  |
| Geometric mean | (ref)                                                   | 1.21x slower                                                          |

Benchmark hidden because not significant (1): regex_effbot

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|----------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle               | 15.4 us                                                 | 13.8 us: 1.11x faster                                                 |
| pickle_dict          | 46.5 us                                                 | 42.2 us: 1.10x faster                                                 |
| unpickle             | 21.4 us                                                 | 23.4 us: 1.10x slower                                                 |
| unpickle_list        | 6.67 us                                                 | 7.89 us: 1.18x slower                                                 |
| json_loads           | 36.1 us                                                 | 44.8 us: 1.24x slower                                                 |
| json_dumps           | 14.9 ms                                                 | 19.0 ms: 1.27x slower                                                 |
| xml_etree_generate   | 129 ms                                                  | 167 ms: 1.29x slower                                                  |
| xml_etree_process    | 86.5 ms                                                 | 130 ms: 1.50x slower                                                  |
| tomli_loads          | 2.80 sec                                                | 4.23 sec: 1.51x slower                                                |
| pickle_pure_python   | 417 us                                                  | 783 us: 1.88x slower                                                  |
| unpickle_pure_python | 296 us                                                  | 578 us: 1.95x slower                                                  |
| Geometric mean       | (ref)                                                   | 1.23x slower                                                          |

Benchmark hidden because not significant (3): xml_etree_parse, pickle_list, xml_etree_iterparse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup         | 22.0 ms                                                 | 30.8 ms: 1.40x slower                                                 |
| python_startup_no_site | 14.6 ms                                                 | 20.9 ms: 1.43x slower                                                 |
| Geometric mean         | (ref)                                                   | 1.41x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|-----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                 | 55.2 ms: 1.74x slower                                                 |
| genshi_xml      | 68.3 ms                                                 | 124 ms: 1.82x slower                                                  |
| django_template | 46.9 ms                                                 | 87.7 ms: 1.87x slower                                                 |
| mako            | 16.1 ms                                                 | 31.5 ms: 1.96x slower                                                 |
| Geometric mean  | (ref)                                                   | 1.85x slower                                                          |

All benchmarks:
===============

| Benchmark                | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240815-linux-x86_64-python-1dad23edbc9db3a13268-3.14.0a0-1dad23e |
|--------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| create_gc_cycles         | 2.46 ms                                                 | 1.87 ms: 1.31x faster                                                 |
| async_tree_io_tg         | 1.46 sec                                                | 1.14 sec: 1.28x faster                                                |
| gc_traversal             | 5.91 ms                                                 | 5.05 ms: 1.17x faster                                                 |
| pickle                   | 15.4 us                                                 | 13.8 us: 1.11x faster                                                 |
| pickle_dict              | 46.5 us                                                 | 42.2 us: 1.10x faster                                                 |
| async_tree_io            | 1.38 sec                                                | 1.28 sec: 1.08x faster                                                |
| async_tree_none_tg       | 521 ms                                                  | 490 ms: 1.06x faster                                                  |
| regex_dna                | 288 ms                                                  | 300 ms: 1.04x slower                                                  |
| sqlite_synth             | 4.07 us                                                 | 4.29 us: 1.05x slower                                                 |
| async_tree_none          | 576 ms                                                  | 626 ms: 1.09x slower                                                  |
| unpickle                 | 21.4 us                                                 | 23.4 us: 1.10x slower                                                 |
| regex_v8                 | 32.4 ms                                                 | 36.8 ms: 1.13x slower                                                 |
| asyncio_tcp              | 985 ms                                                  | 1.16 sec: 1.17x slower                                                |
| unpickle_list            | 6.67 us                                                 | 7.89 us: 1.18x slower                                                 |
| telco                    | 11.4 ms                                                 | 13.7 ms: 1.20x slower                                                 |
| async_generators         | 592 ms                                                  | 731 ms: 1.24x slower                                                  |
| json_loads               | 36.1 us                                                 | 44.8 us: 1.24x slower                                                 |
| asyncio_tcp_ssl          | 2.79 sec                                                | 3.47 sec: 1.24x slower                                                |
| json_dumps               | 14.9 ms                                                 | 19.0 ms: 1.27x slower                                                 |
| pathlib                  | 29.3 ms                                                 | 37.4 ms: 1.27x slower                                                 |
| pylint                   | 472 ms                                                  | 606 ms: 1.28x slower                                                  |
| meteor_contest           | 157 ms                                                  | 202 ms: 1.29x slower                                                  |
| xml_etree_generate       | 129 ms                                                  | 167 ms: 1.29x slower                                                  |
| deepcopy                 | 484 us                                                  | 626 us: 1.29x slower                                                  |
| json                     | 6.55 ms                                                 | 8.59 ms: 1.31x slower                                                 |
| docutils                 | 4.01 sec                                                | 5.35 sec: 1.34x slower                                                |
| scimark_sparse_mat_mult  | 6.98 ms                                                 | 9.49 ms: 1.36x slower                                                 |
| scimark_fft              | 477 ms                                                  | 657 ms: 1.38x slower                                                  |
| mdp                      | 3.80 sec                                                | 5.24 sec: 1.38x slower                                                |
| python_startup           | 22.0 ms                                                 | 30.8 ms: 1.40x slower                                                 |
| tornado_http             | 248 ms                                                  | 350 ms: 1.41x slower                                                  |
| pycparser                | 1.57 sec                                                | 2.23 sec: 1.42x slower                                                |
| python_startup_no_site   | 14.6 ms                                                 | 20.9 ms: 1.43x slower                                                 |
| coverage                 | 110 ms                                                  | 159 ms: 1.44x slower                                                  |
| coroutines               | 29.2 ms                                                 | 42.9 ms: 1.47x slower                                                 |
| generators               | 39.2 ms                                                 | 58.2 ms: 1.48x slower                                                 |
| thrift                   | 1.11 ms                                                 | 1.66 ms: 1.49x slower                                                 |
| deepcopy_memo            | 51.7 us                                                 | 77.4 us: 1.50x slower                                                 |
| fannkuch                 | 543 ms                                                  | 814 ms: 1.50x slower                                                  |
| html5lib                 | 98.1 ms                                                 | 147 ms: 1.50x slower                                                  |
| xml_etree_process        | 86.5 ms                                                 | 130 ms: 1.50x slower                                                  |
| tomli_loads              | 2.80 sec                                                | 4.23 sec: 1.51x slower                                                |
| nqueens                  | 108 ms                                                  | 164 ms: 1.52x slower                                                  |
| sympy_integrate          | 29.7 ms                                                 | 45.4 ms: 1.53x slower                                                 |
| deepcopy_reduce          | 4.27 us                                                 | 6.61 us: 1.55x slower                                                 |
| spectral_norm            | 159 ms                                                  | 247 ms: 1.55x slower                                                  |
| 2to3                     | 442 ms                                                  | 687 ms: 1.56x slower                                                  |
| typing_runtime_protocols | 216 us                                                  | 342 us: 1.58x slower                                                  |
| sqlglot_optimize         | 76.2 ms                                                 | 122 ms: 1.60x slower                                                  |
| sqlglot_normalize        | 146 ms                                                  | 235 ms: 1.61x slower                                                  |
| crypto_pyaes             | 99.8 ms                                                 | 161 ms: 1.61x slower                                                  |
| richards                 | 65.8 ms                                                 | 107 ms: 1.62x slower                                                  |
| logging_simple           | 8.98 us                                                 | 14.9 us: 1.66x slower                                                 |
| pyflate                  | 661 ms                                                  | 1.12 sec: 1.69x slower                                                |
| float                    | 115 ms                                                  | 195 ms: 1.70x slower                                                  |
| bpe_tokeniser            | 6.25 sec                                                | 10.7 sec: 1.71x slower                                                |
| bench_thread_pool        | 3.06 ms                                                 | 5.33 ms: 1.74x slower                                                 |
| genshi_text              | 31.7 ms                                                 | 55.2 ms: 1.74x slower                                                 |
| regex_compile            | 177 ms                                                  | 310 ms: 1.75x slower                                                  |
| richards_super           | 76.3 ms                                                 | 133 ms: 1.75x slower                                                  |
| scimark_monte_carlo      | 89.9 ms                                                 | 161 ms: 1.79x slower                                                  |
| pprint_pformat           | 2.00 sec                                                | 3.62 sec: 1.81x slower                                                |
| genshi_xml               | 68.3 ms                                                 | 124 ms: 1.82x slower                                                  |
| logging_format           | 9.48 us                                                 | 17.3 us: 1.82x slower                                                 |
| django_template          | 46.9 ms                                                 | 87.7 ms: 1.87x slower                                                 |
| pprint_safe_repr         | 959 ms                                                  | 1.80 sec: 1.87x slower                                                |
| comprehensions           | 20.9 us                                                 | 39.2 us: 1.87x slower                                                 |
| pickle_pure_python       | 417 us                                                  | 783 us: 1.88x slower                                                  |
| sympy_str                | 367 ms                                                  | 697 ms: 1.90x slower                                                  |
| unpickle_pure_python     | 296 us                                                  | 578 us: 1.95x slower                                                  |
| mako                     | 16.1 ms                                                 | 31.5 ms: 1.96x slower                                                 |
| sympy_expand             | 631 ms                                                  | 1.26 sec: 1.99x slower                                                |
| sqlglot_transpile        | 2.30 ms                                                 | 4.65 ms: 2.02x slower                                                 |
| hexiom                   | 8.35 ms                                                 | 16.9 ms: 2.03x slower                                                 |
| logging_silent           | 130 ns                                                  | 266 ns: 2.05x slower                                                  |
| scimark_sor              | 172 ms                                                  | 355 ms: 2.06x slower                                                  |
| scimark_lu               | 154 ms                                                  | 319 ms: 2.07x slower                                                  |
| sqlglot_parse            | 1.80 ms                                                 | 3.77 ms: 2.09x slower                                                 |
| chaos                    | 84.7 ms                                                 | 177 ms: 2.09x slower                                                  |
| sympy_sum                | 213 ms                                                  | 462 ms: 2.17x slower                                                  |
| go                       | 195 ms                                                  | 440 ms: 2.25x slower                                                  |
| raytrace                 | 350 ms                                                  | 789 ms: 2.25x slower                                                  |
| nbody                    | 124 ms                                                  | 307 ms: 2.48x slower                                                  |
| deltablue                | 4.56 ms                                                 | 11.8 ms: 2.59x slower                                                 |
| unpack_sequence          | 73.9 ns                                                 | 212 ns: 2.87x slower                                                  |
| Geometric mean           | (ref)                                                   | 1.44x slower                                                          |

Benchmark hidden because not significant (11): bench_mp_pool, xml_etree_parse, async_tree_cpu_io_mixed_tg, pickle_list, xml_etree_iterparse, async_tree_memoization_tg, asyncio_websockets, pidigits, async_tree_cpu_io_mixed, regex_effbot, async_tree_memoization
Ignored benchmarks (6) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, dulwich_log, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.40x
- 95% likely to have a slowdown of 1.39x
- 99% likely to have a slowdown of 1.32x

# Memory
- memory change: 1.15x