---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 98adc5714f4a4abaeca9fe6723b1a56fe1d49fca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687266"
---
# <span data-ttu-id="ab3b3-101">Get-AzureRmSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="ab3b3-101">Get-AzureRmSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="ab3b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab3b3-102">SYNOPSIS</span></span>
<span data-ttu-id="ab3b3-103">Ottiene le impostazioni di provisioning automatico della sicurezza</span><span class="sxs-lookup"><span data-stu-id="ab3b3-103">Gets the security automatic provisioning settings</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab3b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab3b3-104">SYNTAX</span></span>

### <span data-ttu-id="ab3b3-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ab3b3-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab3b3-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="ab3b3-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ab3b3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab3b3-107">ResourceId</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab3b3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab3b3-108">DESCRIPTION</span></span>
<span data-ttu-id="ab3b3-109">Le impostazioni di provisioning automatico consentono di decidere se si vuole che in Azure Security Center proviosion automaticamente un agente di sicurezza che verrà installato nella propria VM.</span><span class="sxs-lookup"><span data-stu-id="ab3b3-109">Automatic Provisioning Settings let you decide whether you want Azure Security Cetner to automatically proviosion a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="ab3b3-110">L'agente di sicurezza controllerà la VM per creare avvisi di sicurezza e monitorare la conformità della sicurezza della VM.</span><span class="sxs-lookup"><span data-stu-id="ab3b3-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="ab3b3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab3b3-111">EXAMPLES</span></span>

### <span data-ttu-id="ab3b3-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ab3b3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="ab3b3-113">Ottiene l'impostazione di provisioning automatico per l'abbonamento</span><span class="sxs-lookup"><span data-stu-id="ab3b3-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="ab3b3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab3b3-114">PARAMETERS</span></span>

### <span data-ttu-id="ab3b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab3b3-115">-DefaultProfile</span></span>
<span data-ttu-id="ab3b3-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ab3b3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3b3-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab3b3-117">-Name</span></span>
<span data-ttu-id="ab3b3-118">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="ab3b3-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab3b3-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab3b3-119">-ResourceId</span></span>
<span data-ttu-id="ab3b3-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="ab3b3-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab3b3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab3b3-121">CommonParameters</span></span>
<span data-ttu-id="ab3b3-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab3b3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab3b3-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab3b3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab3b3-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab3b3-124">INPUTS</span></span>

### <span data-ttu-id="ab3b3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="ab3b3-125">System.String</span></span>

## <span data-ttu-id="ab3b3-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab3b3-126">OUTPUTS</span></span>

### <span data-ttu-id="ab3b3-127">Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="ab3b3-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="ab3b3-128">Note</span><span class="sxs-lookup"><span data-stu-id="ab3b3-128">NOTES</span></span>

## <span data-ttu-id="ab3b3-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab3b3-129">RELATED LINKS</span></span>
