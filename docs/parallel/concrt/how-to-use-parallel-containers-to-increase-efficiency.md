---
title: '방법: 병렬 컨테이너를 사용 하 여 효율성을 높이기 위해 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-concrt
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- increasing efficiency with parallel containers [Concurrency Runtime]
- concurrent_queue class, examples
- concurrent_vector class, examples
ms.assetid: bd00046d-e9b6-4ae1-b661-3995f671b867
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 71a4aee5664864b5a9c803ac5048e8e5b5eacf0a
ms.sourcegitcommit: 799f9b976623a375203ad8b2ad5147bd6a2212f0
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 09/19/2018
ms.locfileid: "46383313"
---
# <a name="how-to-use-parallel-containers-to-increase-efficiency"></a>방법: 병렬 컨테이너를 사용하여 효율성 향상

이 항목에서는 병렬 컨테이너를 사용 하 여 효율적으로 저장 하 고 병렬로 데이터를 액세스 하는 방법을 보여 줍니다.

예제 코드를 소수 및 병렬로 카마이클 숫자 집합을 계산합니다. 그런 다음 각 카마이클 번호에 대 한 코드는 해당 숫자의 소수를 계산합니다.

## <a name="example"></a>예제

다음 예제와 합니다 `is_prime` 입력된 값을 소수 인지를 결정 하는 함수 및 `is_carmichael` 입력된 값이 카마이클 수 있는지 여부를 결정 하는 함수입니다.

[!code-cpp[concrt-carmichael-primes#1](../../parallel/concrt/codesnippet/cpp/how-to-use-parallel-containers-to-increase-efficiency_1.cpp)]

## <a name="example"></a>예제

다음 예제에서는 합니다 `is_prime` 및 `is_carmichael` 소수 집합과 카마이클 수를 계산 하는 함수입니다. 이 예제에서는 사용 합니다 [concurrency:: parallel_invoke](reference/concurrency-namespace-functions.md#parallel_invoke) 및 [concurrency:: parallel_for](reference/concurrency-namespace-functions.md#parallel_for) 병렬에서 알고리즘 각 계산을 설정 합니다. 병렬 알고리즘에 대 한 자세한 내용은 참조 하세요. [병렬 알고리즘](../../parallel/concrt/parallel-algorithms.md)합니다.

사용 하 여이 예제는 [concurrency::concurrent_queue](../../parallel/concrt/reference/concurrent-queue-class.md) 카마이클 집합을 보유 하는 개체는 작업 큐로 해당 개체를 나중에 사용할가 있기 때문에 숫자입니다. 사용 된 [concurrency:: concurrent_vector](../../parallel/concrt/reference/concurrent-vector-class.md) 이 나중에 반복 됩니다이 소수를 찾도록 설정 때문에 소수 집합을 보유 하는 개체입니다.

[!code-cpp[concrt-carmichael-primes#2](../../parallel/concrt/codesnippet/cpp/how-to-use-parallel-containers-to-increase-efficiency_2.cpp)]

## <a name="example"></a>예제

다음 예제와 `prime_factors_of` 함수를 평가판 나누기를 사용 하 여 지정된 된 값의 모든 소수를 찾습니다.

이 함수를 사용 합니다 [concurrency:: parallel_for_each](reference/concurrency-namespace-functions.md#parallel_for_each) 소수의 컬렉션을 반복 하는 알고리즘입니다. `concurrent_vector` 개체 병렬 루프를 동시에 결과를 소수를 추가할 수 있습니다.

[!code-cpp[concrt-carmichael-primes#3](../../parallel/concrt/codesnippet/cpp/how-to-use-parallel-containers-to-increase-efficiency_3.cpp)]

## <a name="example"></a>예제

이 예제에서는 호출 하 여 각 요소 카마이클 수의 큐에 처리를 `prime_factors_of` 해당 소수 요인 계산 하는 함수입니다. 작업 그룹을 사용 하 여이 작업을 병렬로 수행. 작업 그룹에 대 한 자세한 내용은 참조 하세요. [작업 병렬 처리](../../parallel/concrt/task-parallelism-concurrency-runtime.md)합니다.

이 예에서는 숫자에서 소수 4 개 요소 경우 각 카마이클 번호에 대 한 주요 요소를 인쇄 합니다.

[!code-cpp[concrt-carmichael-primes#4](../../parallel/concrt/codesnippet/cpp/how-to-use-parallel-containers-to-increase-efficiency_4.cpp)]

## <a name="example"></a>예제

다음 코드에 병렬 컨테이너를 사용 하 여 카마이클 숫자의 소수를 계산 하는 전체 예제를 보여 줍니다.

[!code-cpp[concrt-carmichael-primes#5](../../parallel/concrt/codesnippet/cpp/how-to-use-parallel-containers-to-increase-efficiency_5.cpp)]

이 예제에서는 다음 샘플 출력을 생성합니다.

```Output
Prime factors of 9890881 are: 7 11 13 41 241.
Prime factors of 825265 are: 5 7 17 19 73.
Prime factors of 1050985 are: 5 13 19 23 37.
```

## <a name="compiling-the-code"></a>코드 컴파일

예제 코드를 복사 하 고 Visual Studio 프로젝트에 붙여 넣습니다 또는 라는 파일에 붙여 `carmichael-primes.cpp` Visual Studio 명령 프롬프트 창에서 다음 명령을 실행 합니다.

**cl.exe /EHsc 카마이클 primes.cpp**

## <a name="see-also"></a>참고 항목

[병렬 컨테이너 및 개체](../../parallel/concrt/parallel-containers-and-objects.md)<br/>
[작업 병렬 처리](../../parallel/concrt/task-parallelism-concurrency-runtime.md)<br/>
[concurrent_vector 클래스](../../parallel/concrt/reference/concurrent-vector-class.md)<br/>
[concurrent_queue 클래스](../../parallel/concrt/reference/concurrent-queue-class.md)<br/>
[parallel_invoke 함수](reference/concurrency-namespace-functions.md#parallel_invoke)<br/>
[parallel_for 함수](reference/concurrency-namespace-functions.md#parallel_for)<br/>
[task_group 클래스](reference/task-group-class.md)
