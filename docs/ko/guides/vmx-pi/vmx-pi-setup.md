---
title: VMX-Pi Setup
---

## VMX-Pi 이미지 다운로드

아래 링크에서 VMX-Pi 이미지를 다운로드하세요. 임시 링크이므로 주소가 변경될 수 있습니다.

[VMX-Pi 이미지 다운로드](https://naver.me/GuCcHhMS)

## 저장 장치에 이미지 기록하기

Raspberry Pi Imager를 사용해 다운로드한 이미지를 SD 카드 또는 사용할 저장 장치에 기록합니다. 아래 스크린샷은 Raspberry Pi 4와 14.8 GB 저장 장치로 진행한 예시입니다. 실제 환경에서는 장치 이름, 용량, 이미지 파일명이 다를 수 있습니다.

1. 사용 중인 하드웨어와 같은 Raspberry Pi 모델을 선택합니다. 아래 예시는 Raspberry Pi 4입니다.

   ![Raspberry Pi 4가 선택된 Raspberry Pi Imager 장치 선택 화면](../../../assets/vmx-pi-setup/01-select-device.png)

2. 운영체제 목록을 열고 **Use custom**을 선택합니다.

   ![Use custom 항목이 강조된 Raspberry Pi Imager 운영체제 목록](../../../assets/vmx-pi-setup/02-select-os.png)

3. 앞에서 다운로드한 VMX-Pi 이미지 파일을 선택합니다. 캡처 예시에는 `WPILib 2027.iso` 파일이 표시되어 있습니다.

   ![다운로드한 이미지 파일을 선택하는 Raspberry Pi Imager 파일 선택 화면](../../../assets/vmx-pi-setup/03-choose-image.png)

4. 이미지를 기록할 SD 카드 또는 저장 장치를 선택합니다. 다음 단계로 넘어가기 전에 장치 이름과 용량을 확인하세요.

   ![Raspberry Pi Imager 저장 장치 선택 화면](../../../assets/vmx-pi-setup/04-select-storage.png)

5. 선택한 장치를 확인한 뒤 기록을 진행합니다. **이미지를 기록하면 선택한 장치의 모든 데이터가 삭제되며 되돌릴 수 없습니다.** 진행하기 전에 올바른 장치를 선택했는지 꼭 확인하세요.

   ![Raspberry Pi Imager의 데이터 삭제 및 기록 확인 창](../../../assets/vmx-pi-setup/05-erase-confirmation.png)

6. 이미지 기록이 끝날 때까지 기다립니다. 작업 중에는 저장 장치를 연결된 상태로 두세요.

   ![이미지를 기록 중인 Raspberry Pi Imager 화면](../../../assets/vmx-pi-setup/06-writing.png)

7. 기록이 끝난 뒤 검증도 완료될 때까지 기다립니다. 기록 또는 검증 중에는 장치를 분리하지 마세요.

   ![기록한 이미지를 검증 중인 Raspberry Pi Imager 화면](../../../assets/vmx-pi-setup/07-verifying.png)

8. **Write complete**가 표시되면 저장 장치를 사용할 수 있습니다. 예시에서는 장치가 자동으로 꺼내졌으며, 안전하게 분리할 수 있다고 표시됩니다.

   ![기록 완료를 표시하는 Raspberry Pi Imager 화면](../../../assets/vmx-pi-setup/08-complete.png)

## 초기 로그인

처음 로그인할 때 다음 정보를 사용하세요.

| 사용자 이름 | 비밀번호 |
|---|---|
| `ubuntu` | `password` |
