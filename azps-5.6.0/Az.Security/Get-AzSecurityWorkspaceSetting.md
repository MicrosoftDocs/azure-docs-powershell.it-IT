---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: f0de174ac85fb4247ac8af55f8a8ab9cb64d6446
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973502"
---
# <span data-ttu-id="31dd7-101">Get-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="31dd7-101">Get-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="31dd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31dd7-102">SYNOPSIS</span></span>
<span data-ttu-id="31dd7-103">Recupera le impostazioni configurate dell'area di lavoro di sicurezza in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="31dd7-103">Gets the configured security workspace settings on a subscription.</span></span>

## <span data-ttu-id="31dd7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31dd7-104">SYNTAX</span></span>

### <span data-ttu-id="31dd7-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="31dd7-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31dd7-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="31dd7-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="31dd7-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="31dd7-107">ResourceId</span></span>
```
Get-AzSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="31dd7-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="31dd7-108">DESCRIPTION</span></span>
<span data-ttu-id="31dd7-109">Questo cmdlet consente di individuare l'area di lavoro configurata che contenerà i dati di sicurezza raccolti dall'agente di sicurezza installato nelle macchine virtuali all'interno di questa sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="31dd7-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="31dd7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31dd7-110">EXAMPLES</span></span>

### <span data-ttu-id="31dd7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="31dd7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="31dd7-112">Ottiene le impostazioni dell'area di lavoro per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="31dd7-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="31dd7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="31dd7-113">PARAMETERS</span></span>

### <span data-ttu-id="31dd7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31dd7-114">-DefaultProfile</span></span>
<span data-ttu-id="31dd7-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31dd7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31dd7-116">-Name</span><span class="sxs-lookup"><span data-stu-id="31dd7-116">-Name</span></span>
<span data-ttu-id="31dd7-117">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="31dd7-117">Resource name.</span></span>

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

### <span data-ttu-id="31dd7-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="31dd7-118">-ResourceId</span></span>
<span data-ttu-id="31dd7-119">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="31dd7-119">Resource ID.</span></span>

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

### <span data-ttu-id="31dd7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31dd7-120">CommonParameters</span></span>
<span data-ttu-id="31dd7-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31dd7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31dd7-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="31dd7-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31dd7-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="31dd7-123">INPUTS</span></span>

### <span data-ttu-id="31dd7-124">System.String</span><span class="sxs-lookup"><span data-stu-id="31dd7-124">System.String</span></span>

## <span data-ttu-id="31dd7-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31dd7-125">OUTPUTS</span></span>

### <span data-ttu-id="31dd7-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="31dd7-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="31dd7-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="31dd7-127">NOTES</span></span>

## <span data-ttu-id="31dd7-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31dd7-128">RELATED LINKS</span></span>
