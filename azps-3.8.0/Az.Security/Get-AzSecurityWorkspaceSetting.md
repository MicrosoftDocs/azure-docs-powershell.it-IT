---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 5b905083668392ce026bfa416252eb1371ebb640
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019547"
---
# <span data-ttu-id="93870-101">Get-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="93870-101">Get-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="93870-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93870-102">SYNOPSIS</span></span>
<span data-ttu-id="93870-103">Ottiene le impostazioni dell'area di lavoro di sicurezza configurate in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="93870-103">Gets the configured security workspace settings on a subscription.</span></span>

## <span data-ttu-id="93870-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93870-104">SYNTAX</span></span>

### <span data-ttu-id="93870-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="93870-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93870-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="93870-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="93870-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="93870-107">ResourceId</span></span>
```
Get-AzSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93870-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93870-108">DESCRIPTION</span></span>
<span data-ttu-id="93870-109">Questo cmdlet consente di individuare l'area di lavoro configurata che conterrà i dati di sicurezza raccolti dall'agente di sicurezza installato in VM all'interno di questo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="93870-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="93870-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93870-110">EXAMPLES</span></span>

### <span data-ttu-id="93870-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="93870-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="93870-112">Ottiene le impostazioni dell'area di lavoro per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="93870-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="93870-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93870-113">PARAMETERS</span></span>

### <span data-ttu-id="93870-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93870-114">-DefaultProfile</span></span>
<span data-ttu-id="93870-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="93870-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93870-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="93870-116">-Name</span></span>
<span data-ttu-id="93870-117">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="93870-117">Resource name.</span></span>

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

### <span data-ttu-id="93870-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93870-118">-ResourceId</span></span>
<span data-ttu-id="93870-119">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="93870-119">Resource ID.</span></span>

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

### <span data-ttu-id="93870-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93870-120">CommonParameters</span></span>
<span data-ttu-id="93870-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93870-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93870-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93870-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93870-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93870-123">INPUTS</span></span>

### <span data-ttu-id="93870-124">System. String</span><span class="sxs-lookup"><span data-stu-id="93870-124">System.String</span></span>

## <span data-ttu-id="93870-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93870-125">OUTPUTS</span></span>

### <span data-ttu-id="93870-126">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="93870-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="93870-127">Note</span><span class="sxs-lookup"><span data-stu-id="93870-127">NOTES</span></span>

## <span data-ttu-id="93870-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93870-128">RELATED LINKS</span></span>
