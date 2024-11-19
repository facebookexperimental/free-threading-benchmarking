# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_tlbc_call
- machine: linux-x86_64
- commit hash: 6a24958
- commit date: 2024-11-18
- overall geometric mean: 1.49x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.36x slower
- Memory change: 1.21x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| 2to3           | 254 ms                                                                 | 406 ms: 1.60x slower                                                 |
| docutils       | 2.60 sec                                                               | 3.29 sec: 1.26x slower                                               |
| html5lib       | 63.7 ms                                                                | 104 ms: 1.63x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.49x slower                                                         |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|--------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| asyncio_websockets | 520 ms                                                                 | 516 ms: 1.01x faster                                                 |
| asyncio_tcp        | 504 ms                                                                 | 581 ms: 1.15x slower                                                 |
| asyncio_tcp_ssl    | 1.52 sec                                                               | 1.83 sec: 1.21x slower                                               |
| async_generators   | 383 ms                                                                 | 482 ms: 1.26x slower                                                 |
| coroutines         | 22.8 ms                                                                | 29.4 ms: 1.29x slower                                                |
| Geometric mean     | (ref)                                                                  | 1.18x slower                                                         |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pidigits       | 186 ms                                                                 | 183 ms: 1.01x faster                                                 |
| float          | 78.6 ms                                                                | 147 ms: 1.87x slower                                                 |
| nbody          | 96.2 ms                                                                | 198 ms: 2.06x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.56x slower                                                         |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| regex_effbot   | 3.28 ms                                                                | 3.11 ms: 1.05x faster                                                |
| regex_dna      | 181 ms                                                                 | 185 ms: 1.03x slower                                                 |
| regex_v8       | 23.1 ms                                                                | 25.0 ms: 1.08x slower                                                |
| regex_compile  | 131 ms                                                                 | 212 ms: 1.63x slower                                                 |
| Geometric mean | (ref)                                                                  | 1.14x slower                                                         |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|----------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| pickle_dict          | 33.7 us                                                                | 31.8 us: 1.06x faster                                                |
| xml_etree_parse      | 136 ms                                                                 | 133 ms: 1.02x faster                                                 |
| pickle_list          | 5.28 us                                                                | 5.19 us: 1.02x faster                                                |
| unpickle_list        | 4.73 us                                                                | 4.95 us: 1.05x slower                                                |
| unpickle             | 13.6 us                                                                | 14.8 us: 1.09x slower                                                |
| xml_etree_iterparse  | 95.5 ms                                                                | 106 ms: 1.11x slower                                                 |
| json_loads           | 25.1 us                                                                | 28.5 us: 1.14x slower                                                |
| pickle               | 12.2 us                                                                | 14.1 us: 1.16x slower                                                |
| xml_etree_generate   | 86.1 ms                                                                | 108 ms: 1.26x slower                                                 |
| json_dumps           | 11.5 ms                                                                | 15.0 ms: 1.30x slower                                                |
| tomli_loads          | 2.11 sec                                                               | 3.10 sec: 1.47x slower                                               |
| xml_etree_process    | 60.0 ms                                                                | 88.5 ms: 1.48x slower                                                |
| unpickle_pure_python | 215 us                                                                 | 384 us: 1.79x slower                                                 |
| pickle_pure_python   | 315 us                                                                 | 577 us: 1.83x slower                                                 |
| Geometric mean       | (ref)                                                                  | 1.23x slower                                                         |

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| python_startup_no_site | 7.46 ms                                                                | 10.2 ms: 1.37x slower                                                |
| python_startup         | 11.1 ms                                                                | 15.7 ms: 1.41x slower                                                |
| Geometric mean         | (ref)                                                                  | 1.39x slower                                                         |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|-----------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| genshi_xml      | 50.8 ms                                                                | 79.6 ms: 1.57x slower                                                |
| mako            | 11.9 ms                                                                | 18.8 ms: 1.59x slower                                                |
| django_template | 35.7 ms                                                                | 61.3 ms: 1.72x slower                                                |
| genshi_text     | 22.2 ms                                                                | 39.0 ms: 1.75x slower                                                |
| Geometric mean  | (ref)                                                                  | 1.65x slower                                                         |

All benchmarks:
===============

| Benchmark                | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call-3.14.0a1+-6a24958 |
|--------------------------|:----------------------------------------------------------------------:|:--------------------------------------------------------------------:|
| gc_traversal             | 3.20 ms                                                                | 2.58 ms: 1.24x faster                                                |
| create_gc_cycles         | 1.37 ms                                                                | 1.13 ms: 1.21x faster                                                |
| pickle_dict              | 33.7 us                                                                | 31.8 us: 1.06x faster                                                |
| regex_effbot             | 3.28 ms                                                                | 3.11 ms: 1.05x faster                                                |
| xml_etree_parse          | 136 ms                                                                 | 133 ms: 1.02x faster                                                 |
| pickle_list              | 5.28 us                                                                | 5.19 us: 1.02x faster                                                |
| pidigits                 | 186 ms                                                                 | 183 ms: 1.01x faster                                                 |
| asyncio_websockets       | 520 ms                                                                 | 516 ms: 1.01x faster                                                 |
| regex_dna                | 181 ms                                                                 | 185 ms: 1.03x slower                                                 |
| unpickle_list            | 4.73 us                                                                | 4.95 us: 1.05x slower                                                |
| regex_v8                 | 23.1 ms                                                                | 25.0 ms: 1.08x slower                                                |
| unpickle                 | 13.6 us                                                                | 14.8 us: 1.09x slower                                                |
| sqlite_synth             | 2.19 us                                                                | 2.39 us: 1.09x slower                                                |
| xml_etree_iterparse      | 95.5 ms                                                                | 106 ms: 1.11x slower                                                 |
| json                     | 4.66 ms                                                                | 5.21 ms: 1.12x slower                                                |
| bench_mp_pool            | 63.7 ms                                                                | 71.9 ms: 1.13x slower                                                |
| json_loads               | 25.1 us                                                                | 28.5 us: 1.14x slower                                                |
| asyncio_tcp              | 504 ms                                                                 | 581 ms: 1.15x slower                                                 |
| pickle                   | 12.2 us                                                                | 14.1 us: 1.16x slower                                                |
| scimark_fft              | 335 ms                                                                 | 404 ms: 1.20x slower                                                 |
| asyncio_tcp_ssl          | 1.52 sec                                                               | 1.83 sec: 1.21x slower                                               |
| pathlib                  | 18.2 ms                                                                | 22.0 ms: 1.21x slower                                                |
| coverage                 | 81.0 ms                                                                | 100 ms: 1.24x slower                                                 |
| xml_etree_generate       | 86.1 ms                                                                | 108 ms: 1.26x slower                                                 |
| async_generators         | 383 ms                                                                 | 482 ms: 1.26x slower                                                 |
| docutils                 | 2.60 sec                                                               | 3.29 sec: 1.26x slower                                               |
| pylint                   | 319 ms                                                                 | 411 ms: 1.29x slower                                                 |
| coroutines               | 22.8 ms                                                                | 29.4 ms: 1.29x slower                                                |
| telco                    | 7.18 ms                                                                | 9.33 ms: 1.30x slower                                                |
| bpe_tokeniser            | 4.35 sec                                                               | 5.66 sec: 1.30x slower                                               |
| mdp                      | 2.35 sec                                                               | 3.06 sec: 1.30x slower                                               |
| json_dumps               | 11.5 ms                                                                | 15.0 ms: 1.30x slower                                                |
| scimark_sparse_mat_mult  | 4.34 ms                                                                | 5.80 ms: 1.34x slower                                                |
| dulwich_log              | 75.2 ms                                                                | 103 ms: 1.37x slower                                                 |
| python_startup_no_site   | 7.46 ms                                                                | 10.2 ms: 1.37x slower                                                |
| meteor_contest           | 99.0 ms                                                                | 136 ms: 1.38x slower                                                 |
| nqueens                  | 78.9 ms                                                                | 111 ms: 1.40x slower                                                 |
| spectral_norm            | 110 ms                                                                 | 154 ms: 1.40x slower                                                 |
| python_startup           | 11.1 ms                                                                | 15.7 ms: 1.41x slower                                                |
| generators               | 29.3 ms                                                                | 41.9 ms: 1.43x slower                                                |
| pycparser                | 1.13 sec                                                               | 1.65 sec: 1.46x slower                                               |
| tomli_loads              | 2.11 sec                                                               | 3.10 sec: 1.47x slower                                               |
| xml_etree_process        | 60.0 ms                                                                | 88.5 ms: 1.48x slower                                                |
| fannkuch                 | 369 ms                                                                 | 545 ms: 1.48x slower                                                 |
| deepcopy                 | 265 us                                                                 | 404 us: 1.53x slower                                                 |
| typing_runtime_protocols | 158 us                                                                 | 242 us: 1.53x slower                                                 |
| genshi_xml               | 50.8 ms                                                                | 79.6 ms: 1.57x slower                                                |
| deepcopy_reduce          | 2.69 us                                                                | 4.23 us: 1.57x slower                                                |
| crypto_pyaes             | 66.9 ms                                                                | 105 ms: 1.57x slower                                                 |
| sqlglot_optimize         | 53.9 ms                                                                | 85.1 ms: 1.58x slower                                                |
| deepcopy_memo            | 30.3 us                                                                | 47.9 us: 1.58x slower                                                |
| mako                     | 11.9 ms                                                                | 18.8 ms: 1.59x slower                                                |
| sqlglot_normalize        | 107 ms                                                                 | 170 ms: 1.59x slower                                                 |
| 2to3                     | 254 ms                                                                 | 406 ms: 1.60x slower                                                 |
| sympy_integrate          | 19.9 ms                                                                | 31.9 ms: 1.61x slower                                                |
| regex_compile            | 131 ms                                                                 | 212 ms: 1.63x slower                                                 |
| html5lib                 | 63.7 ms                                                                | 104 ms: 1.63x slower                                                 |
| pyflate                  | 445 ms                                                                 | 734 ms: 1.65x slower                                                 |
| thrift                   | 752 us                                                                 | 1.26 ms: 1.68x slower                                                |
| comprehensions           | 17.3 us                                                                | 29.0 us: 1.68x slower                                                |
| pprint_safe_repr         | 716 ms                                                                 | 1.22 sec: 1.71x slower                                               |
| django_template          | 35.7 ms                                                                | 61.3 ms: 1.72x slower                                                |
| pprint_pformat           | 1.47 sec                                                               | 2.53 sec: 1.73x slower                                               |
| genshi_text              | 22.2 ms                                                                | 39.0 ms: 1.75x slower                                                |
| unpickle_pure_python     | 215 us                                                                 | 384 us: 1.79x slower                                                 |
| pickle_pure_python       | 315 us                                                                 | 577 us: 1.83x slower                                                 |
| richards                 | 45.6 ms                                                                | 85.0 ms: 1.87x slower                                                |
| float                    | 78.6 ms                                                                | 147 ms: 1.87x slower                                                 |
| scimark_monte_carlo      | 65.4 ms                                                                | 123 ms: 1.87x slower                                                 |
| logging_simple           | 6.25 us                                                                | 11.8 us: 1.88x slower                                                |
| logging_format           | 6.95 us                                                                | 13.1 us: 1.89x slower                                                |
| logging_silent           | 106 ns                                                                 | 202 ns: 1.91x slower                                                 |
| chaos                    | 58.9 ms                                                                | 113 ms: 1.92x slower                                                 |
| sympy_str                | 274 ms                                                                 | 527 ms: 1.92x slower                                                 |
| hexiom                   | 5.94 ms                                                                | 11.5 ms: 1.93x slower                                                |
| scimark_sor              | 135 ms                                                                 | 263 ms: 1.94x slower                                                 |
| sqlglot_transpile        | 1.60 ms                                                                | 3.20 ms: 2.00x slower                                                |
| richards_super           | 51.7 ms                                                                | 106 ms: 2.05x slower                                                 |
| nbody                    | 96.2 ms                                                                | 198 ms: 2.06x slower                                                 |
| scimark_lu               | 113 ms                                                                 | 236 ms: 2.09x slower                                                 |
| sqlglot_parse            | 1.30 ms                                                                | 2.78 ms: 2.14x slower                                                |
| raytrace                 | 263 ms                                                                 | 574 ms: 2.18x slower                                                 |
| sympy_expand             | 460 ms                                                                 | 1.03 sec: 2.25x slower                                               |
| go                       | 121 ms                                                                 | 284 ms: 2.35x slower                                                 |
| sympy_sum                | 152 ms                                                                 | 376 ms: 2.47x slower                                                 |
| deltablue                | 3.27 ms                                                                | 8.67 ms: 2.65x slower                                                |
| unpack_sequence          | 46.6 ns                                                                | 147 ns: 3.15x slower                                                 |
| bench_thread_pool        | 1.01 ms                                                                | 3.47 ms: 3.42x slower                                                |
| Geometric mean           | (ref)                                                                  | 1.49x slower                                                         |

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.42x
- 95% likely to have a slowdown of 1.40x
- 99% likely to have a slowdown of 1.36x

# Memory
- memory change: 1.21x