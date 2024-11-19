# Results vs. default_base_vs_NOGIL

- fork: mpage
- ref: gh_115999_tlbc_call_
- machine: linux-x86_64
- commit hash: e051157
- commit date: 2024-11-18
- overall geometric mean: 1.55x slower
- HPT reliability: 100.00%
- HPT 99th percentile: 1.41x slower
- Memory change: 1.20x

Benchmarks with tag 'apps':
===========================

| Benchmark      | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| 2to3           | 254 ms                                                                 | 417 ms: 1.64x slower                                                  |
| docutils       | 2.60 sec                                                               | 3.38 sec: 1.30x slower                                                |
| html5lib       | 63.7 ms                                                                | 105 ms: 1.65x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.52x slower                                                          |

Benchmarks with tag 'asyncio':
==============================

| Benchmark          | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|--------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| asyncio_websockets | 520 ms                                                                 | 518 ms: 1.00x faster                                                  |
| asyncio_tcp        | 504 ms                                                                 | 584 ms: 1.16x slower                                                  |
| asyncio_tcp_ssl    | 1.52 sec                                                               | 1.82 sec: 1.20x slower                                                |
| async_generators   | 383 ms                                                                 | 490 ms: 1.28x slower                                                  |
| coroutines         | 22.8 ms                                                                | 31.5 ms: 1.38x slower                                                 |
| Geometric mean     | (ref)                                                                  | 1.20x slower                                                          |

Benchmarks with tag 'math':
===========================

| Benchmark      | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pidigits       | 186 ms                                                                 | 185 ms: 1.01x faster                                                  |
| float          | 78.6 ms                                                                | 153 ms: 1.94x slower                                                  |
| nbody          | 96.2 ms                                                                | 205 ms: 2.14x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.60x slower                                                          |

Benchmarks with tag 'regex':
============================

| Benchmark      | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| regex_effbot   | 3.28 ms                                                                | 2.99 ms: 1.10x faster                                                 |
| regex_dna      | 181 ms                                                                 | 189 ms: 1.04x slower                                                  |
| regex_v8       | 23.1 ms                                                                | 24.7 ms: 1.07x slower                                                 |
| regex_compile  | 131 ms                                                                 | 229 ms: 1.76x slower                                                  |
| Geometric mean | (ref)                                                                  | 1.16x slower                                                          |

Benchmarks with tag 'serialize':
================================

| Benchmark            | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|----------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| pickle_dict          | 33.7 us                                                                | 32.0 us: 1.05x faster                                                 |
| pickle_list          | 5.28 us                                                                | 5.23 us: 1.01x faster                                                 |
| unpickle_list        | 4.73 us                                                                | 5.06 us: 1.07x slower                                                 |
| unpickle             | 13.6 us                                                                | 14.6 us: 1.08x slower                                                 |
| pickle               | 12.2 us                                                                | 13.5 us: 1.11x slower                                                 |
| json_loads           | 25.1 us                                                                | 28.6 us: 1.14x slower                                                 |
| xml_etree_iterparse  | 95.5 ms                                                                | 109 ms: 1.14x slower                                                  |
| xml_etree_generate   | 86.1 ms                                                                | 113 ms: 1.32x slower                                                  |
| json_dumps           | 11.5 ms                                                                | 15.3 ms: 1.33x slower                                                 |
| tomli_loads          | 2.11 sec                                                               | 3.24 sec: 1.54x slower                                                |
| xml_etree_process    | 60.0 ms                                                                | 93.4 ms: 1.56x slower                                                 |
| unpickle_pure_python | 215 us                                                                 | 423 us: 1.97x slower                                                  |
| pickle_pure_python   | 315 us                                                                 | 622 us: 1.98x slower                                                  |
| Geometric mean       | (ref)                                                                  | 1.26x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

Benchmarks with tag 'startup':
==============================

| Benchmark              | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| python_startup_no_site | 7.46 ms                                                                | 10.3 ms: 1.38x slower                                                 |
| python_startup         | 11.1 ms                                                                | 15.7 ms: 1.42x slower                                                 |
| Geometric mean         | (ref)                                                                  | 1.40x slower                                                          |

Benchmarks with tag 'template':
===============================

| Benchmark       | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|-----------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| genshi_xml      | 50.8 ms                                                                | 82.9 ms: 1.63x slower                                                 |
| mako            | 11.9 ms                                                                | 20.8 ms: 1.76x slower                                                 |
| django_template | 35.7 ms                                                                | 64.9 ms: 1.82x slower                                                 |
| genshi_text     | 22.2 ms                                                                | 41.0 ms: 1.84x slower                                                 |
| Geometric mean  | (ref)                                                                  | 1.76x slower                                                          |

All benchmarks:
===============

| Benchmark                | bm-20241117-vultr-x86_64-python-9d6366b60d01305fc5e4-3.14.0a1+-9d6366b | bm-20241118-vultr-x86_64-mpage-gh_115999_tlbc_call_-3.14.0a1+-e051157 |
|--------------------------|:----------------------------------------------------------------------:|:---------------------------------------------------------------------:|
| gc_traversal             | 3.20 ms                                                                | 2.38 ms: 1.34x faster                                                 |
| create_gc_cycles         | 1.37 ms                                                                | 1.15 ms: 1.19x faster                                                 |
| regex_effbot             | 3.28 ms                                                                | 2.99 ms: 1.10x faster                                                 |
| pickle_dict              | 33.7 us                                                                | 32.0 us: 1.05x faster                                                 |
| pickle_list              | 5.28 us                                                                | 5.23 us: 1.01x faster                                                 |
| pidigits                 | 186 ms                                                                 | 185 ms: 1.01x faster                                                  |
| asyncio_websockets       | 520 ms                                                                 | 518 ms: 1.00x faster                                                  |
| regex_dna                | 181 ms                                                                 | 189 ms: 1.04x slower                                                  |
| unpickle_list            | 4.73 us                                                                | 5.06 us: 1.07x slower                                                 |
| regex_v8                 | 23.1 ms                                                                | 24.7 ms: 1.07x slower                                                 |
| unpickle                 | 13.6 us                                                                | 14.6 us: 1.08x slower                                                 |
| pickle                   | 12.2 us                                                                | 13.5 us: 1.11x slower                                                 |
| sqlite_synth             | 2.19 us                                                                | 2.47 us: 1.13x slower                                                 |
| json                     | 4.66 ms                                                                | 5.30 ms: 1.14x slower                                                 |
| bench_mp_pool            | 63.7 ms                                                                | 72.7 ms: 1.14x slower                                                 |
| json_loads               | 25.1 us                                                                | 28.6 us: 1.14x slower                                                 |
| xml_etree_iterparse      | 95.5 ms                                                                | 109 ms: 1.14x slower                                                  |
| asyncio_tcp              | 504 ms                                                                 | 584 ms: 1.16x slower                                                  |
| pathlib                  | 18.2 ms                                                                | 21.7 ms: 1.19x slower                                                 |
| asyncio_tcp_ssl          | 1.52 sec                                                               | 1.82 sec: 1.20x slower                                                |
| coverage                 | 81.0 ms                                                                | 102 ms: 1.26x slower                                                  |
| scimark_fft              | 335 ms                                                                 | 425 ms: 1.27x slower                                                  |
| async_generators         | 383 ms                                                                 | 490 ms: 1.28x slower                                                  |
| telco                    | 7.18 ms                                                                | 9.29 ms: 1.29x slower                                                 |
| docutils                 | 2.60 sec                                                               | 3.38 sec: 1.30x slower                                                |
| xml_etree_generate       | 86.1 ms                                                                | 113 ms: 1.32x slower                                                  |
| pylint                   | 319 ms                                                                 | 422 ms: 1.32x slower                                                  |
| json_dumps               | 11.5 ms                                                                | 15.3 ms: 1.33x slower                                                 |
| mdp                      | 2.35 sec                                                               | 3.16 sec: 1.34x slower                                                |
| python_startup_no_site   | 7.46 ms                                                                | 10.3 ms: 1.38x slower                                                 |
| coroutines               | 22.8 ms                                                                | 31.5 ms: 1.38x slower                                                 |
| meteor_contest           | 99.0 ms                                                                | 137 ms: 1.38x slower                                                  |
| dulwich_log              | 75.2 ms                                                                | 105 ms: 1.39x slower                                                  |
| scimark_sparse_mat_mult  | 4.34 ms                                                                | 6.05 ms: 1.39x slower                                                 |
| bpe_tokeniser            | 4.35 sec                                                               | 6.16 sec: 1.42x slower                                                |
| python_startup           | 11.1 ms                                                                | 15.7 ms: 1.42x slower                                                 |
| generators               | 29.3 ms                                                                | 41.5 ms: 1.42x slower                                                 |
| spectral_norm            | 110 ms                                                                 | 159 ms: 1.46x slower                                                  |
| nqueens                  | 78.9 ms                                                                | 116 ms: 1.47x slower                                                  |
| fannkuch                 | 369 ms                                                                 | 564 ms: 1.53x slower                                                  |
| pycparser                | 1.13 sec                                                               | 1.73 sec: 1.53x slower                                                |
| tomli_loads              | 2.11 sec                                                               | 3.24 sec: 1.54x slower                                                |
| xml_etree_process        | 60.0 ms                                                                | 93.4 ms: 1.56x slower                                                 |
| typing_runtime_protocols | 158 us                                                                 | 252 us: 1.60x slower                                                  |
| crypto_pyaes             | 66.9 ms                                                                | 109 ms: 1.62x slower                                                  |
| genshi_xml               | 50.8 ms                                                                | 82.9 ms: 1.63x slower                                                 |
| deepcopy                 | 265 us                                                                 | 433 us: 1.64x slower                                                  |
| 2to3                     | 254 ms                                                                 | 417 ms: 1.64x slower                                                  |
| html5lib                 | 63.7 ms                                                                | 105 ms: 1.65x slower                                                  |
| sympy_integrate          | 19.9 ms                                                                | 33.3 ms: 1.68x slower                                                 |
| sqlglot_optimize         | 53.9 ms                                                                | 91.3 ms: 1.69x slower                                                 |
| sqlglot_normalize        | 107 ms                                                                 | 182 ms: 1.71x slower                                                  |
| deepcopy_reduce          | 2.69 us                                                                | 4.59 us: 1.71x slower                                                 |
| thrift                   | 752 us                                                                 | 1.30 ms: 1.73x slower                                                 |
| regex_compile            | 131 ms                                                                 | 229 ms: 1.76x slower                                                  |
| mako                     | 11.9 ms                                                                | 20.8 ms: 1.76x slower                                                 |
| pyflate                  | 445 ms                                                                 | 786 ms: 1.77x slower                                                  |
| deepcopy_memo            | 30.3 us                                                                | 53.6 us: 1.77x slower                                                 |
| comprehensions           | 17.3 us                                                                | 30.6 us: 1.77x slower                                                 |
| django_template          | 35.7 ms                                                                | 64.9 ms: 1.82x slower                                                 |
| genshi_text              | 22.2 ms                                                                | 41.0 ms: 1.84x slower                                                 |
| pprint_safe_repr         | 716 ms                                                                 | 1.33 sec: 1.86x slower                                                |
| pprint_pformat           | 1.47 sec                                                               | 2.77 sec: 1.89x slower                                                |
| float                    | 78.6 ms                                                                | 153 ms: 1.94x slower                                                  |
| logging_simple           | 6.25 us                                                                | 12.2 us: 1.95x slower                                                 |
| logging_format           | 6.95 us                                                                | 13.6 us: 1.96x slower                                                 |
| unpickle_pure_python     | 215 us                                                                 | 423 us: 1.97x slower                                                  |
| pickle_pure_python       | 315 us                                                                 | 622 us: 1.98x slower                                                  |
| scimark_monte_carlo      | 65.4 ms                                                                | 130 ms: 1.98x slower                                                  |
| sympy_str                | 274 ms                                                                 | 543 ms: 1.98x slower                                                  |
| scimark_sor              | 135 ms                                                                 | 270 ms: 1.99x slower                                                  |
| richards                 | 45.6 ms                                                                | 91.6 ms: 2.01x slower                                                 |
| logging_silent           | 106 ns                                                                 | 216 ns: 2.04x slower                                                  |
| sqlglot_transpile        | 1.60 ms                                                                | 3.33 ms: 2.08x slower                                                 |
| hexiom                   | 5.94 ms                                                                | 12.5 ms: 2.10x slower                                                 |
| chaos                    | 58.9 ms                                                                | 124 ms: 2.10x slower                                                  |
| nbody                    | 96.2 ms                                                                | 205 ms: 2.14x slower                                                  |
| richards_super           | 51.7 ms                                                                | 113 ms: 2.19x slower                                                  |
| scimark_lu               | 113 ms                                                                 | 248 ms: 2.20x slower                                                  |
| sqlglot_parse            | 1.30 ms                                                                | 2.88 ms: 2.21x slower                                                 |
| sympy_expand             | 460 ms                                                                 | 1.06 sec: 2.30x slower                                                |
| raytrace                 | 263 ms                                                                 | 647 ms: 2.46x slower                                                  |
| go                       | 121 ms                                                                 | 301 ms: 2.50x slower                                                  |
| sympy_sum                | 152 ms                                                                 | 382 ms: 2.51x slower                                                  |
| deltablue                | 3.27 ms                                                                | 9.26 ms: 2.83x slower                                                 |
| unpack_sequence          | 46.6 ns                                                                | 142 ns: 3.04x slower                                                  |
| bench_thread_pool        | 1.01 ms                                                                | 3.49 ms: 3.45x slower                                                 |
| Geometric mean           | (ref)                                                                  | 1.55x slower                                                          |

Benchmark hidden because not significant (1): xml_etree_parse

# HPT report

- Reliability score: 100.00% likely to be slow
- 90% likely to have a slowdown of 1.47x
- 95% likely to have a slowdown of 1.44x
- 99% likely to have a slowdown of 1.41x

# Memory
- memory change: 1.20x