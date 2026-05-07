# AI
AI 관련 딥러닝, 머신러닝 등 각종 아르피셜 인텔리전스를 학습한 내용을 담는 리포지터리.

# AI Study Repository

이 리포지터리는 인공지능, 딥러닝, 컴퓨터 비전 모델을 학습하고 실습한 내용을 정리하기 위한 공간입니다.  
현재는 **MobileViT와 CNN의 구조적 차이 및 성능 비교**를 중심으로 정리하고 있습니다.

## 📌 Repository Overview

| 항목 | 내용 |
|---|---|
| Repository | AI |
| Main Topic | MobileViT vs CNN |
| File | `mobilevit_vs_cnn.ipynb` |
| Environment | Google Colab / Jupyter Notebook |
| Study Area | Computer Vision, Deep Learning, Vision Transformer |

## 📂 Main Notebook

- [`mobilevit_vs_cnn.ipynb`](./mobilevit_vs_cnn.ipynb)

해당 노트북에서는 MobileViT와 CNN의 기본 개념을 비교하고, 이미지 분류 모델 관점에서 두 구조가 어떤 차이를 가지는지 정리합니다.

## 🧠 Key Concepts

### 1. CNN

**CNN(Convolutional Neural Network)**은 이미지 데이터를 처리하는 데 많이 사용되는 딥러닝 모델입니다.  
이미지의 작은 영역을 필터로 훑으면서 선, 모서리, 질감, 형태와 같은 특징을 단계적으로 추출합니다.

CNN은 다음과 같은 특징을 가집니다.

- 이미지의 **지역적 특징(local feature)**을 잘 추출함
- 합성곱 연산을 통해 공간 정보를 효율적으로 처리함
- 이미지 분류, 객체 탐지, 의료 영상 분석 등에 널리 사용됨
- 비교적 구조가 직관적이고 안정적인 성능을 보임

대표적인 CNN 기반 모델로는 LeNet, AlexNet, VGG, ResNet, MobileNet 등이 있습니다.

## 2. Vision Transformer

**Vision Transformer(ViT)**는 자연어 처리에서 주로 사용되던 Transformer 구조를 이미지 처리에 적용한 모델입니다.  
이미지를 작은 패치 단위로 나누고, 각 패치 사이의 관계를 self-attention 방식으로 학습합니다.

ViT는 다음과 같은 특징을 가집니다.

- 이미지 전체의 **전역적 관계(global context)**를 파악하는 데 강점이 있음
- Self-Attention을 통해 멀리 떨어진 영역 간의 관계도 학습할 수 있음
- 큰 데이터셋과 충분한 연산 자원이 있을 때 강력한 성능을 보임
- 일반 CNN보다 학습 비용이 높을 수 있음

## 3. MobileViT

**MobileViT**는 모바일 환경에서도 사용할 수 있도록 설계된 경량 Vision Transformer 모델입니다.  
CNN의 장점인 지역 특징 추출 능력과 Transformer의 장점인 전역 문맥 이해 능력을 결합한 구조입니다.

MobileViT의 핵심 아이디어는 다음과 같습니다.

- CNN을 통해 이미지의 기본적인 지역 특징을 추출함
- Transformer를 통해 이미지 전체의 관계를 학습함
- 모바일 기기에서도 사용할 수 있도록 가볍고 효율적인 구조를 지향함
- CNN과 ViT의 장점을 모두 활용하려는 하이브리드 모델임

즉, MobileViT는 단순히 Transformer를 작게 만든 모델이라기보다,  
**CNN과 Transformer의 역할을 조합한 모바일 친화적 컴퓨터 비전 모델**이라고 볼 수 있습니다.

## 🔍 MobileViT vs CNN

| 비교 항목 | CNN | MobileViT |
|---|---|---|
| 주요 구조 | Convolution 중심 | CNN + Transformer |
| 강점 | 지역 특징 추출 | 지역 특징 + 전역 관계 학습 |
| 이미지 이해 방식 | 가까운 픽셀 관계 중심 | 이미지 전체 문맥까지 고려 |
| 연산 효율성 | 비교적 효율적 | 경량화를 목표로 설계 |
| 활용 분야 | 이미지 분류, 객체 탐지 등 | 모바일 비전, 경량 AI 모델 |
| 한계 | 전역 문맥 파악이 약할 수 있음 | 구조가 CNN보다 복잡함 |

## 🧩 Why Compare MobileViT and CNN?

CNN은 오랫동안 컴퓨터 비전 분야에서 핵심적인 역할을 해 온 모델입니다.  
하지만 CNN은 기본적으로 가까운 영역의 특징을 중심으로 이미지를 이해하기 때문에, 이미지 전체의 문맥을 파악하는 데 한계가 있을 수 있습니다.

반면 Transformer 기반 모델은 self-attention을 통해 이미지 전체의 관계를 학습할 수 있습니다.  
그러나 일반적인 Vision Transformer는 연산량이 크고 모바일 환경에서 사용하기 어려울 수 있습니다.

MobileViT는 이러한 문제를 해결하기 위해 등장한 모델입니다.  
따라서 MobileViT와 CNN을 비교하는 것은 다음과 같은 의미가 있습니다.

- 기존 CNN 구조의 장점과 한계를 이해할 수 있음
- Transformer가 컴퓨터 비전에 적용되는 방식을 이해할 수 있음
- 모바일 환경에서 AI 모델을 효율적으로 설계하는 방법을 생각해 볼 수 있음
- 경량 딥러닝 모델의 필요성을 이해할 수 있음

## 🚀 How to Use

GitHub에서 노트북 파일을 열거나, Google Colab에서 실행할 수 있습니다.

### Open in Colab

아래 링크를 통해 Colab에서 노트북을 실행할 수 있습니다.

[Open in Colab](https://colab.research.google.com/github/VisualStudy/AI/blob/main/mobilevit_vs_cnn.ipynb)

또는 노트북 상단에 다음 배지를 추가할 수 있습니다.

```html
<a href="https://colab.research.google.com/github/VisualStudy/AI/blob/main/mobilevit_vs_cnn.ipynb" target="_parent">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>
