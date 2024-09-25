# Results vs. 3.13.0rc1+

- fork: python
- ref: ef4b69d2becf49daaea2
- machine: linux-x86_64
- commit hash: ef4b69d
- commit date: 2024-09-06
- overall geometric mean: 1.43x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.29x slower
- Memory change: 1.15x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 442 ms                                                  | 719 ms: 1.63x slower                                                  |
| docutils       | 4.01 sec                                                | 4.96 sec: 1.24x slower                                                |
| html5lib       | 98.1 ms                                                 | 139 ms: 1.41x slower                                                  |
| tornado_http   | 248 ms                                                  | 350 ms: 1.41x slower                                                  |
| Geometric mean | (ref)                                                   | 1.42x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark               | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|-------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| async_tree_io_tg        | 1.46 sec                                                | 1.17 sec: 1.24x faster                                                |
| asyncio_websockets      | 772 ms                                                  | 747 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed | 899 ms                                                  | 952 ms: 1.06x slower                                                  |
| async_tree_none         | 576 ms                                                  | 610 ms: 1.06x slower                                                  |
| asyncio_tcp             | 985 ms                                                  | 1.22 sec: 1.24x slower                                                |
| async_generators        | 592 ms                                                  | 734 ms: 1.24x slower                                                  |
| asyncio_tcp_ssl         | 2.79 sec                                                | 3.56 sec: 1.28x slower                                                |
| coroutines              | 29.2 ms                                                 | 41.7 ms: 1.43x slower                                                 |
| Geometric mean          | (ref)                                                   | 1.07x slower                                                          |

Benchmark hidden because not significant (5): async_tree_io, async_tree_memoization_tg, async_tree_none_tg, async_tree_memoization, async_tree_cpu_io_mixed_tg

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| float          | 115 ms                                                  | 204 ms: 1.78x slower                                                  |
| nbody          | 124 ms                                                  | 300 ms: 2.43x slower                                                  |
| Geometric mean | (ref)                                                   | 1.63x slower                                                          |

Benchmark hidden because not significant (1): pidigits

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_v8       | 32.4 ms                                                 | 37.7 ms: 1.16x slower                                                 |
| regex_compile  | 177 ms                                                  | 284 ms: 1.60x slower                                                  |
| Geometric mean | (ref)                                                   | 1.18x slower                                                          |

Benchmark hidden because not significant (2): regex_effbot, regex_dna

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|----------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 46.5 us                                                 | 40.9 us: 1.14x faster                                                 |
| xml_etree_parse      | 236 ms                                                  | 215 ms: 1.10x faster                                                  |
| unpickle_list        | 6.67 us                                                 | 7.20 us: 1.08x slower                                                 |
| json_dumps           | 14.9 ms                                                 | 18.1 ms: 1.21x slower                                                 |
| json_loads           | 36.1 us                                                 | 44.0 us: 1.22x slower                                                 |
| xml_etree_generate   | 129 ms                                                  | 163 ms: 1.26x slower                                                  |
| xml_etree_process    | 86.5 ms                                                 | 128 ms: 1.48x slower                                                  |
| tomli_loads          | 2.80 sec                                                | 4.30 sec: 1.53x slower                                                |
| unpickle_pure_python | 296 us                                                  | 550 us: 1.86x slower                                                  |
| pickle_pure_python   | 417 us                                                  | 870 us: 2.09x slower                                                  |
| Geometric mean       | (ref)                                                   | 1.20x slower                                                          |

Benchmark hidden because not significant (4): pickle_list, xml_etree_iterparse, pickle, unpickle

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 14.6 ms                                                 | 21.5 ms: 1.47x slower                                                 |
| python_startup         | 22.0 ms                                                 | 32.8 ms: 1.49x slower                                                 |
| Geometric mean         | (ref)                                                   | 1.48x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|-----------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_text     | 31.7 ms                                                 | 55.1 ms: 1.74x slower                                                 |
| django_template | 46.9 ms                                                 | 85.9 ms: 1.83x slower                                                 |
| mako            | 16.1 ms                                                 | 30.1 ms: 1.87x slower                                                 |
| genshi_xml      | 68.3 ms                                                 | 129 ms: 1.90x slower                                                  |
| Geometric mean  | (ref)                                                   | 1.83x slower                                                          |

All benchmarks:
===============

| Benchmark                | bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1 | bm-20240906-linux-x86_64-python-ef4b69d2becf49daaea2-3.14.0a0-ef4b69d |
|--------------------------|:-------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal             | 5.91 ms                                                 | 4.60 ms: 1.28x faster                                                 |
| async_tree_io_tg         | 1.46 sec                                                | 1.17 sec: 1.24x faster                                                |
| create_gc_cycles         | 2.46 ms                                                 | 2.12 ms: 1.16x faster                                                 |
| pickle_dict              | 46.5 us                                                 | 40.9 us: 1.14x faster                                                 |
| xml_etree_parse          | 236 ms                                                  | 215 ms: 1.10x faster                                                  |
| asyncio_websockets       | 772 ms                                                  | 747 ms: 1.03x faster                                                  |
| async_tree_cpu_io_mixed  | 899 ms                                                  | 952 ms: 1.06x slower                                                  |
| async_tree_none          | 576 ms                                                  | 610 ms: 1.06x slower                                                  |
| unpickle_list            | 6.67 us                                                 | 7.20 us: 1.08x slower                                                 |
| sqlite_synth             | 4.07 us                                                 | 4.60 us: 1.13x slower                                                 |
| regex_v8                 | 32.4 ms                                                 | 37.7 ms: 1.16x slower                                                 |
| deepcopy                 | 484 us                                                  | 568 us: 1.17x slower                                                  |
| json_dumps               | 14.9 ms                                                 | 18.1 ms: 1.21x slower                                                 |
| json_loads               | 36.1 us                                                 | 44.0 us: 1.22x slower                                                 |
| asyncio_tcp              | 985 ms                                                  | 1.22 sec: 1.24x slower                                                |
| json                     | 6.55 ms                                                 | 8.10 ms: 1.24x slower                                                 |
| docutils                 | 4.01 sec                                                | 4.96 sec: 1.24x slower                                                |
| bench_mp_pool            | 19.4 ms                                                 | 24.0 ms: 1.24x slower                                                 |
| async_generators         | 592 ms                                                  | 734 ms: 1.24x slower                                                  |
| scimark_sparse_mat_mult  | 6.98 ms                                                 | 8.80 ms: 1.26x slower                                                 |
| xml_etree_generate       | 129 ms                                                  | 163 ms: 1.26x slower                                                  |
| meteor_contest           | 157 ms                                                  | 199 ms: 1.27x slower                                                  |
| pathlib                  | 29.3 ms                                                 | 37.2 ms: 1.27x slower                                                 |
| asyncio_tcp_ssl          | 2.79 sec                                                | 3.56 sec: 1.28x slower                                                |
| telco                    | 11.4 ms                                                 | 14.7 ms: 1.29x slower                                                 |
| deepcopy_memo            | 51.7 us                                                 | 67.4 us: 1.30x slower                                                 |
| pylint                   | 472 ms                                                  | 625 ms: 1.32x slower                                                  |
| mdp                      | 3.80 sec                                                | 5.18 sec: 1.37x slower                                                |
| scimark_fft              | 477 ms                                                  | 652 ms: 1.37x slower                                                  |
| pycparser                | 1.57 sec                                                | 2.18 sec: 1.39x slower                                                |
| generators               | 39.2 ms                                                 | 54.6 ms: 1.39x slower                                                 |
| deepcopy_reduce          | 4.27 us                                                 | 5.97 us: 1.40x slower                                                 |
| tornado_http             | 248 ms                                                  | 350 ms: 1.41x slower                                                  |
| html5lib                 | 98.1 ms                                                 | 139 ms: 1.41x slower                                                  |
| coverage                 | 110 ms                                                  | 157 ms: 1.42x slower                                                  |
| coroutines               | 29.2 ms                                                 | 41.7 ms: 1.43x slower                                                 |
| python_startup_no_site   | 14.6 ms                                                 | 21.5 ms: 1.47x slower                                                 |
| xml_etree_process        | 86.5 ms                                                 | 128 ms: 1.48x slower                                                  |
| python_startup           | 22.0 ms                                                 | 32.8 ms: 1.49x slower                                                 |
| dulwich_log              | 100.0 ms                                                | 152 ms: 1.52x slower                                                  |
| thrift                   | 1.11 ms                                                 | 1.70 ms: 1.53x slower                                                 |
| fannkuch                 | 543 ms                                                  | 831 ms: 1.53x slower                                                  |
| tomli_loads              | 2.80 sec                                                | 4.30 sec: 1.53x slower                                                |
| crypto_pyaes             | 99.8 ms                                                 | 156 ms: 1.56x slower                                                  |
| spectral_norm            | 159 ms                                                  | 249 ms: 1.56x slower                                                  |
| regex_compile            | 177 ms                                                  | 284 ms: 1.60x slower                                                  |
| nqueens                  | 108 ms                                                  | 174 ms: 1.61x slower                                                  |
| richards_super           | 76.3 ms                                                 | 123 ms: 1.61x slower                                                  |
| 2to3                     | 442 ms                                                  | 719 ms: 1.63x slower                                                  |
| sympy_integrate          | 29.7 ms                                                 | 48.3 ms: 1.63x slower                                                 |
| pyflate                  | 661 ms                                                  | 1.08 sec: 1.63x slower                                                |
| typing_runtime_protocols | 216 us                                                  | 353 us: 1.63x slower                                                  |
| logging_format           | 9.48 us                                                 | 15.5 us: 1.63x slower                                                 |
| bpe_tokeniser            | 6.25 sec                                                | 10.2 sec: 1.64x slower                                                |
| sqlglot_normalize        | 146 ms                                                  | 240 ms: 1.65x slower                                                  |
| sqlglot_optimize         | 76.2 ms                                                 | 130 ms: 1.71x slower                                                  |
| genshi_text              | 31.7 ms                                                 | 55.1 ms: 1.74x slower                                                 |
| pprint_pformat           | 2.00 sec                                                | 3.48 sec: 1.74x slower                                                |
| richards                 | 65.8 ms                                                 | 114 ms: 1.74x slower                                                  |
| pprint_safe_repr         | 959 ms                                                  | 1.68 sec: 1.75x slower                                                |
| bench_thread_pool        | 3.06 ms                                                 | 5.45 ms: 1.78x slower                                                 |
| float                    | 115 ms                                                  | 204 ms: 1.78x slower                                                  |
| scimark_monte_carlo      | 89.9 ms                                                 | 160 ms: 1.78x slower                                                  |
| comprehensions           | 20.9 us                                                 | 37.3 us: 1.78x slower                                                 |
| django_template          | 46.9 ms                                                 | 85.9 ms: 1.83x slower                                                 |
| go                       | 195 ms                                                  | 361 ms: 1.85x slower                                                  |
| unpickle_pure_python     | 296 us                                                  | 550 us: 1.86x slower                                                  |
| mako                     | 16.1 ms                                                 | 30.1 ms: 1.87x slower                                                 |
| genshi_xml               | 68.3 ms                                                 | 129 ms: 1.90x slower                                                  |
| sympy_str                | 367 ms                                                  | 696 ms: 1.90x slower                                                  |
| sqlglot_transpile        | 2.30 ms                                                 | 4.43 ms: 1.93x slower                                                 |
| hexiom                   | 8.35 ms                                                 | 16.4 ms: 1.97x slower                                                 |
| scimark_sor              | 172 ms                                                  | 340 ms: 1.97x slower                                                  |
| logging_simple           | 8.98 us                                                 | 17.7 us: 1.97x slower                                                 |
| scimark_lu               | 154 ms                                                  | 305 ms: 1.98x slower                                                  |
| logging_silent           | 130 ns                                                  | 260 ns: 2.00x slower                                                  |
| sqlglot_parse            | 1.80 ms                                                 | 3.72 ms: 2.07x slower                                                 |
| chaos                    | 84.7 ms                                                 | 176 ms: 2.08x slower                                                  |
| pickle_pure_python       | 417 us                                                  | 870 us: 2.09x slower                                                  |
| sympy_expand             | 631 ms                                                  | 1.33 sec: 2.11x slower                                                |
| raytrace                 | 350 ms                                                  | 751 ms: 2.15x slower                                                  |
| sympy_sum                | 213 ms                                                  | 492 ms: 2.31x slower                                                  |
| nbody                    | 124 ms                                                  | 300 ms: 2.43x slower                                                  |
| unpack_sequence          | 73.9 ns                                                 | 180 ns: 2.43x slower                                                  |
| deltablue                | 4.56 ms                                                 | 11.3 ms: 2.49x slower                                                 |
| Geometric mean           | (ref)                                                   | 1.43x slower                                                          |

Benchmark hidden because not significant (12): pickle_list, xml_etree_iterparse, async_tree_io, async_tree_memoization_tg, async_tree_none_tg, pickle, pidigits, async_tree_memoization, regex_effbot, async_tree_cpu_io_mixed_tg, unpickle, regex_dna
Ignored benchmarks (5) of results/bm-20240814-3.13.0rc1+-79452b1/bm-20240814-linux-x86_64-python-3.13-3.13.0rc1+-79452b1.json: aiohttp, chameleon, dask, flaskblogging, gunicorn

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.37x
- 95% likely to have a slowdown of 1.36x
- 99% likely to have a slowdown of 1.29x

# Memory
- memory change: 1.15x