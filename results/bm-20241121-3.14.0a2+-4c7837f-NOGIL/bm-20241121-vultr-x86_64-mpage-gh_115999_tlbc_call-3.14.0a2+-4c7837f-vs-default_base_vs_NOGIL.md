# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 4c7837f
- commit date: 2024-11-21
- overall geometric mean: 1.56x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.41x slower
- Memory change: 1.34x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 256 ms                                                                 | 411 ms: 1.61x slower                                                 |
| docutils       | 2.63 sec                                                               | 3.32 sec: 1.27x slower                                               |
| html5lib       | 66.9 ms                                                                | 106 ms: 1.59x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.48x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark        | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| async_generators | 378 ms                                                                 | 481 ms: 1.27x slower                                                 |
| coroutines       | 22.6 ms                                                                | 29.2 ms: 1.30x slower                                                |
| Geometric mean   | (ref)                                                                  | 1.18x slower                                                         |

Benchmark hidden because not significant (1): asyncio_websockets

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 217 ms                                                                 | 183 ms: 1.18x faster                                                 |
| float          | 78.8 ms                                                                | 148 ms: 1.88x slower                                                 |
| nbody          | 95.9 ms                                                                | 200 ms: 2.09x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.49x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 2.86 ms                                                                | 2.81 ms: 1.02x faster                                                |
| regex_dna      | 177 ms                                                                 | 185 ms: 1.05x slower                                                 |
| regex_v8       | 23.6 ms                                                                | 25.0 ms: 1.06x slower                                                |
| regex_compile  | 135 ms                                                                 | 219 ms: 1.62x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.15x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| xml_etree_parse      | 137 ms                                                                 | 133 ms: 1.03x faster                                                 |
| xml_etree_iterparse  | 96.1 ms                                                                | 105 ms: 1.10x slower                                                 |
| json_loads           | 25.0 us                                                                | 28.3 us: 1.13x slower                                                |
| xml_etree_generate   | 86.2 ms                                                                | 110 ms: 1.27x slower                                                 |
| json_dumps           | 11.3 ms                                                                | 15.5 ms: 1.36x slower                                                |
| tomli_loads          | 2.15 sec                                                               | 3.16 sec: 1.47x slower                                               |
| xml_etree_process    | 60.2 ms                                                                | 90.0 ms: 1.50x slower                                                |
| unpickle_pure_python | 217 us                                                                 | 388 us: 1.79x slower                                                 |
| pickle_pure_python   | 320 us                                                                 | 598 us: 1.87x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.35x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.41 ms                                                                | 10.3 ms: 1.39x slower                                                |
| python_startup         | 11.1 ms                                                                | 17.6 ms: 1.59x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.49x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| mako            | 12.0 ms                                                                | 19.2 ms: 1.60x slower                                                |
| genshi_xml      | 50.3 ms                                                                | 81.0 ms: 1.61x slower                                                |
| django_template | 35.7 ms                                                                | 62.3 ms: 1.74x slower                                                |
| genshi_text     | 21.9 ms                                                                | 39.2 ms: 1.79x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.68x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf | bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits                 | 217 ms                                                                 | 183 ms: 1.18x faster                                                 |
| gc_traversal             | 3.63 ms                                                                | 3.50 ms: 1.04x faster                                                |
| xml_etree_parse          | 137 ms                                                                 | 133 ms: 1.03x faster                                                 |
| regex_effbot             | 2.86 ms                                                                | 2.81 ms: 1.02x faster                                                |
| regex_dna                | 177 ms                                                                 | 185 ms: 1.05x slower                                                 |
| regex_v8                 | 23.6 ms                                                                | 25.0 ms: 1.06x slower                                                |
| sqlite_synth             | 2.24 us                                                                | 2.42 us: 1.08x slower                                                |
| xml_etree_iterparse      | 96.1 ms                                                                | 105 ms: 1.10x slower                                                 |
| json                     | 4.61 ms                                                                | 5.17 ms: 1.12x slower                                                |
| json_loads               | 25.0 us                                                                | 28.3 us: 1.13x slower                                                |
| pathlib                  | 18.6 ms                                                                | 21.6 ms: 1.16x slower                                                |
| scimark_fft              | 337 ms                                                                 | 417 ms: 1.24x slower                                                 |
| coverage                 | 80.2 ms                                                                | 101 ms: 1.25x slower                                                 |
| docutils                 | 2.63 sec                                                               | 3.32 sec: 1.27x slower                                               |
| xml_etree_generate       | 86.2 ms                                                                | 110 ms: 1.27x slower                                                 |
| async_generators         | 378 ms                                                                 | 481 ms: 1.27x slower                                                 |
| mdp                      | 2.36 sec                                                               | 3.03 sec: 1.28x slower                                               |
| coroutines               | 22.6 ms                                                                | 29.2 ms: 1.30x slower                                                |
| telco                    | 7.22 ms                                                                | 9.46 ms: 1.31x slower                                                |
| bpe_tokeniser            | 4.34 sec                                                               | 5.69 sec: 1.31x slower                                               |
| scimark_sparse_mat_mult  | 4.48 ms                                                                | 5.92 ms: 1.32x slower                                                |
| dulwich_log              | 75.9 ms                                                                | 103 ms: 1.36x slower                                                 |
| json_dumps               | 11.3 ms                                                                | 15.5 ms: 1.36x slower                                                |
| create_gc_cycles         | 1.34 ms                                                                | 1.83 ms: 1.37x slower                                                |
| spectral_norm            | 113 ms                                                                 | 158 ms: 1.39x slower                                                 |
| python_startup_no_site   | 7.41 ms                                                                | 10.3 ms: 1.39x slower                                                |
| generators               | 29.2 ms                                                                | 41.1 ms: 1.41x slower                                                |
| meteor_contest           | 100 ms                                                                 | 143 ms: 1.42x slower                                                 |
| nqueens                  | 79.2 ms                                                                | 113 ms: 1.43x slower                                                 |
| pycparser                | 1.14 sec                                                               | 1.67 sec: 1.47x slower                                               |
| tomli_loads              | 2.15 sec                                                               | 3.16 sec: 1.47x slower                                               |
| fannkuch                 | 371 ms                                                                 | 551 ms: 1.48x slower                                                 |
| xml_etree_process        | 60.2 ms                                                                | 90.0 ms: 1.50x slower                                                |
| typing_runtime_protocols | 160 us                                                                 | 243 us: 1.52x slower                                                 |
| pylint                   | 272 ms                                                                 | 416 ms: 1.53x slower                                                 |
| deepcopy                 | 266 us                                                                 | 413 us: 1.55x slower                                                 |
| python_startup           | 11.1 ms                                                                | 17.6 ms: 1.59x slower                                                |
| crypto_pyaes             | 67.9 ms                                                                | 108 ms: 1.59x slower                                                 |
| html5lib                 | 66.9 ms                                                                | 106 ms: 1.59x slower                                                 |
| sqlglot_optimize         | 53.9 ms                                                                | 85.9 ms: 1.59x slower                                                |
| deepcopy_memo            | 30.3 us                                                                | 48.4 us: 1.59x slower                                                |
| mako                     | 12.0 ms                                                                | 19.2 ms: 1.60x slower                                                |
| 2to3                     | 256 ms                                                                 | 411 ms: 1.61x slower                                                 |
| genshi_xml               | 50.3 ms                                                                | 81.0 ms: 1.61x slower                                                |
| sqlglot_normalize        | 108 ms                                                                 | 174 ms: 1.61x slower                                                 |
| regex_compile            | 135 ms                                                                 | 219 ms: 1.62x slower                                                 |
| sympy_integrate          | 20.0 ms                                                                | 32.6 ms: 1.63x slower                                                |
| deepcopy_reduce          | 2.65 us                                                                | 4.33 us: 1.63x slower                                                |
| thrift                   | 752 us                                                                 | 1.26 ms: 1.67x slower                                                |
| pyflate                  | 448 ms                                                                 | 752 ms: 1.68x slower                                                 |
| comprehensions           | 17.3 us                                                                | 29.5 us: 1.70x slower                                                |
| django_template          | 35.7 ms                                                                | 62.3 ms: 1.74x slower                                                |
| pprint_safe_repr         | 716 ms                                                                 | 1.25 sec: 1.75x slower                                               |
| bench_mp_pool            | 63.6 ms                                                                | 111 ms: 1.75x slower                                                 |
| pprint_pformat           | 1.48 sec                                                               | 2.60 sec: 1.75x slower                                               |
| genshi_text              | 21.9 ms                                                                | 39.2 ms: 1.79x slower                                                |
| unpickle_pure_python     | 217 us                                                                 | 388 us: 1.79x slower                                                 |
| pickle_pure_python       | 320 us                                                                 | 598 us: 1.87x slower                                                 |
| float                    | 78.8 ms                                                                | 148 ms: 1.88x slower                                                 |
| logging_format           | 6.99 us                                                                | 13.1 us: 1.88x slower                                                |
| logging_simple           | 6.30 us                                                                | 11.9 us: 1.90x slower                                                |
| logging_silent           | 109 ns                                                                 | 208 ns: 1.91x slower                                                 |
| scimark_monte_carlo      | 65.4 ms                                                                | 125 ms: 1.91x slower                                                 |
| richards                 | 45.9 ms                                                                | 88.1 ms: 1.92x slower                                                |
| sympy_str                | 275 ms                                                                 | 533 ms: 1.94x slower                                                 |
| scimark_sor              | 136 ms                                                                 | 267 ms: 1.96x slower                                                 |
| hexiom                   | 5.96 ms                                                                | 11.8 ms: 1.98x slower                                                |
| chaos                    | 59.0 ms                                                                | 117 ms: 1.99x slower                                                 |
| richards_super           | 52.0 ms                                                                | 106 ms: 2.04x slower                                                 |
| sqlglot_transpile        | 1.59 ms                                                                | 3.30 ms: 2.07x slower                                                |
| scimark_lu               | 113 ms                                                                 | 236 ms: 2.09x slower                                                 |
| nbody                    | 95.9 ms                                                                | 200 ms: 2.09x slower                                                 |
| sqlglot_parse            | 1.30 ms                                                                | 2.80 ms: 2.15x slower                                                |
| sympy_expand             | 460 ms                                                                 | 1.04 sec: 2.26x slower                                               |
| raytrace                 | 264 ms                                                                 | 602 ms: 2.28x slower                                                 |
| go                       | 122 ms                                                                 | 291 ms: 2.39x slower                                                 |
| sympy_sum                | 153 ms                                                                 | 379 ms: 2.47x slower                                                 |
| deltablue                | 3.25 ms                                                                | 8.79 ms: 2.70x slower                                                |
| bench_thread_pool        | 1.02 ms                                                                | 3.50 ms: 3.44x slower                                                |
| Geometric mean           | (ref)                                                                  | 1.56x slower                                                         |

Benchmark hidden because not significant (1): asyncio_websockets
Ignored benchmarks (8) of results/bm-20241120-3.14.0a2+-32428cf/bm-20241120-vultr-x86_64-python-32428cf9ea03bce6d64c-3.14.0a2+-32428cf.json: asyncio_tcp, asyncio_tcp_ssl, pickle, pickle_dict, pickle_list, unpack_sequence, unpickle, unpickle_list
Ignored benchmarks (14) of results/bm-20241121-3.14.0a2+-4c7837f-NOGIL/bm-20241121-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a2+-4c7837f.json: async_tree_cpu_io_mixed, async_tree_cpu_io_mixed_tg, async_tree_io, async_tree_io_tg, async_tree_memoization, async_tree_memoization_tg, async_tree_none, async_tree_none_tg, connected_components, k_core, many_optionals, shortest_path, sphinx, subparsers

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.46x
- 95% likely to have a slowdown of 1.45x
- 99% likely to have a slowdown of 1.41x

# Memory
- memory change: 1.34x