---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 08631f5705a3a0255c42ac3d146cef45de1b4e56
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486347"
---
# <span data-ttu-id="56161-101">Get-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="56161-101">Get-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="56161-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56161-102">SYNOPSIS</span></span>
<span data-ttu-id="56161-103">Ottiene le impostazioni di provisioning automatico della sicurezza</span><span class="sxs-lookup"><span data-stu-id="56161-103">Gets the security automatic provisioning settings</span></span>

## <span data-ttu-id="56161-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56161-104">SYNTAX</span></span>

### <span data-ttu-id="56161-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="56161-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56161-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="56161-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="56161-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="56161-107">ResourceId</span></span>
```
Get-AzSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56161-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56161-108">DESCRIPTION</span></span>
<span data-ttu-id="56161-109">Le impostazioni di provisioning automatico consentono di decidere se si vuole che Azure Security Center provisiona automaticamente un agente di sicurezza che verrà installato nella propria VM.</span><span class="sxs-lookup"><span data-stu-id="56161-109">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="56161-110">L'agente di sicurezza controllerà la VM per creare avvisi di sicurezza e monitorare la conformità della sicurezza della VM.</span><span class="sxs-lookup"><span data-stu-id="56161-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="56161-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56161-111">EXAMPLES</span></span>

### <span data-ttu-id="56161-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="56161-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="56161-113">Ottiene l'impostazione di provisioning automatico per l'abbonamento</span><span class="sxs-lookup"><span data-stu-id="56161-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="56161-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56161-114">PARAMETERS</span></span>

### <span data-ttu-id="56161-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56161-115">-DefaultProfile</span></span>
<span data-ttu-id="56161-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56161-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56161-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="56161-117">-Name</span></span>
<span data-ttu-id="56161-118">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="56161-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56161-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56161-119">-ResourceId</span></span>
<span data-ttu-id="56161-120">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="56161-120">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56161-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56161-121">CommonParameters</span></span>
<span data-ttu-id="56161-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56161-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56161-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56161-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56161-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56161-124">INPUTS</span></span>

### <span data-ttu-id="56161-125">System. String</span><span class="sxs-lookup"><span data-stu-id="56161-125">System.String</span></span>

## <span data-ttu-id="56161-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56161-126">OUTPUTS</span></span>

### <span data-ttu-id="56161-127">Microsoft. Azure. Commands. Security. Models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="56161-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="56161-128">Note</span><span class="sxs-lookup"><span data-stu-id="56161-128">NOTES</span></span>

## <span data-ttu-id="56161-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56161-129">RELATED LINKS</span></span>
