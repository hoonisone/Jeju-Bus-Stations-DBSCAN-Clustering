# Jeju-Bus-Stations-DBSCAN-Cluastering
**제주 버스 정류장 DBSCAN 기반 군집화 알고리즘**


## Idea
- ``유의미한 거시적인 기·종점 간 버스 통행수요 분석``을 위해 합리적인 단위의 기·종점 설정이 필요함.
  - 기·종점을 단순히 ``1개 정류장``으로 한정할 경우, 지나치게 미시적인 통행량 분석만 가능함.
  - 또, 기·종점을 ``행정동`` 또는 ``교통 존(TAZ)``으로 설정할 경우, 지나치게 거시적인 통행량 분석으로 이어질 것임.

- 이에 따라 본 알고리즘은 정류장을 합리적인 수준으로 군집화하여, 의미있는 단위의 기·종점을 설정할 수 있도록 고안됨.
  - 특히, 정류장의 분포가 기하학적으로 복잡한 형태에도 효과적이 군집화가 가능한 DBSCAN 방법을 기반으로 위 알고리즘을 구현함.
  - 이때, DBSCAN의 경우, 최적의 ``반경 크기(eps)``와 ``최소 데이터포인트 개수(minPts)``를 설정해야 함.
    - 제주시와 서귀포시의 교통 인프라가 다르므로, 시별로 군집화해야 하며, 시별로 ``eps``, ``minPts``를 설정해야 함.
      - 제주시: ``eps = 100m``, ``minPts ∈ [2, 3]``
      - 서귀포시: ``eps = 95m``, ``minPts ∈ [2, 3]``
    - ``eps`` 값 설정은 [Link]를 바탕으로 한 것임.

## Prerequisites
- Python 3.7.4
- Pandas 0.25.1
- Scikit-Learn 0.23.0

## Dataset
- ``station-final.csv``
  - 제주 지역 버스 정류장 데이터 (csv 파일)

## Results
- 

## Reference
- 
