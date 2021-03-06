---

copyright:

  years: 2018
lastupdated: "2018-04-13"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}

# 영역 판별
{: #determinespaces}

조직 내에서 영역은 추가 레벨의 경계 적용 및 추출을 제공합니다.

영역은 사용자가 앱 및 서비스를 개발하고 실행할 수 있는 조직에서 예약된 영역입니다. 조직에서 임의의 수의 영역을 작성할 수 있으며 영역에 액세스할 수 있는 사용자를 제어할 수 있습니다. 세부사항은  [영역](/docs/account/orgs_spaces.html#orgsspacesusers)을 참조하십시오.

많은 영역을 정의하려는 경우 영역을 관리하는 데 도움이 되도록 애플리케이션을 작성할 수 있습니다. 영역의 수가 60을 초과하는 경우 다른 조직 정의를 고려할 수 있습니다.

## 단일 조직과 다중 조직의 영역
{: #spaceconsiderations}

단일 조직 아키텍처를 채택하는 경우 분리 및 추출 레벨이 조직 내에 정의한 영역에서 제공됩니다. 영역을 정의할 때 다음 지침을 고려하십시오.

* 조직에서 한 번만 프로비저닝하고 구성해야 하는 서비스를 호스팅할 영역을 정의하십시오. 
* 전달 라이프사이클을 기반으로 영역을 정의하십시오.
  예를 들어, 개발 중인 앱을 위한 하나 이상의 영역, 테스트 단계에 있는 앱을 위한 하나 이상의 영역, 프로덕션 상태의 앱을 위한 하나 이상의 영역을 정의할 수 있습니다.
* 전달 라이프사이클 경계가 충분하지 않은 경우 LOB 및 전달 단계마다 하나 이상의 영역을 정의하여 추가 분리할 수 있습니다.
* 여러 사용자 그룹에 대한 경계를 적용해야 하는지 식별하십시오.
  예를 들어, 개발자는 애플리케이션을 개발하고 테스트할 수 없습니다. 애플리케이션을 테스트하려면 다른 사용자 세트가 필요합니다. 이 시나리오에서는 두 개의 영역, 즉 애플리케이션 개발자를 위한 영역과 애플리케이션 테스터를 위한 영역을 작성합니다. 그런 다음 각 사용자 세트에 올바른 영역에 대한 액세스 권한을 부여합니다.

다중 조직 아키텍처를 구현하는 경우 LOB, 전달 라이프사이클 또는 둘 다를 통해 각 조직을 분리할 수 있습니다. 그런 다음 회사의 동일한 부서에서 전달되는 앱 또는 프로젝트의 수를 기반으로 하는 여러 영역을 정의할 수 있습니다. 조직에서 영역을 계획할 때 다음 지침을 고려하십시오.

* 조직에서 한 번만 프로비저닝하고 구성해야 하는 서비스를 호스팅하기 위한 영역을 정의하십시오.
* 애플리케이션마다, 관련 앱 그룹마다 또는 특정 프로젝트에 대해 영역을 정의하십시오.
* 여러 사용자의 경계를 적용해야 하는 경우 각 사용자 세트에 대한 영역을 정의하십시오. 사용자에게 영역의 개발자 역할이 부여된 경우 해당 사용자에는 이 영역에서 프로비저닝되어 실행 중인 임의의 소스 및 {{site.data.keyword.Bluemix_notm}} 서비스에 대한 전체 액세스가 있습니다. 사용자가 모든 리소스를 제어하지 못하도록 하기 위해 더 강력한 보안을 적용해야 하는 경우 여러 영역을 정의해 보십시오. 이러한 영역 내에서, 해당 영역에서 실행 중인 앱에서 사용되는 {{site.data.keyword.Bluemix_notm}} 서비스를 프로비저닝할 수 있습니다.

## 영역 이름 지정, 제한사항 및 관리
{: #spaceadmin}

클라우드 조직에 대한 여러 영역을 정의하려면 다음 지침을 고려하십시오.

* 이름 지정 규칙을 정의하고 적용하십시오. 예를 들어, 영역 이름에 조직의 위치 및 클라우드의 유형에 대한 정보가 포함된 이름 지정 규칙을 정의하십시오. 영역 이름 작성 후 변경할 수 있습니다. 영역 이름이 변경되면 모든 영역 팀 구성원에게 변경에 대해 알리십시오.
* 영역에 적용되는 제한사항을 정의하십시오. 예를 들어, 각 영역에서 개발, 관리 및 배치될 수 있는 앱의 유형을 정의하십시오.
* 영역의 관리자를 식별하십시오. 둘 이상의 사용자에게 영역 관리를 위임할 수 있습니다.
