---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 7e2a655810c885245d3694fb63caa44c5b4119e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686364"
---
# <span data-ttu-id="4d519-101">Get-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="4d519-101">Get-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="4d519-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d519-102">SYNOPSIS</span></span>
<span data-ttu-id="4d519-103">Ottiene le impostazioni dell'area di lavoro di sicurezza configurate in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4d519-103">Gets the configured security workspace settings on a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d519-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d519-104">SYNTAX</span></span>

### <span data-ttu-id="4d519-105">SubscriptionScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4d519-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d519-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="4d519-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4d519-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d519-107">ResourceId</span></span>
```
Get-AzureRmSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d519-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d519-108">DESCRIPTION</span></span>
<span data-ttu-id="4d519-109">Questo cmdlet consente di individuare l'area di lavoro configurata che conterrà i dati di sicurezza raccolti dall'agente di sicurezza installato in VM all'interno di questo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4d519-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="4d519-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d519-110">EXAMPLES</span></span>

### <span data-ttu-id="4d519-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4d519-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="4d519-112">Ottiene le impostazioni dell'area di lavoro per un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4d519-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="4d519-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d519-113">PARAMETERS</span></span>

### <span data-ttu-id="4d519-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d519-114">-DefaultProfile</span></span>
<span data-ttu-id="4d519-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d519-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d519-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d519-116">-Name</span></span>
<span data-ttu-id="4d519-117">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="4d519-117">Resource name.</span></span>

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

### <span data-ttu-id="4d519-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d519-118">-ResourceId</span></span>
<span data-ttu-id="4d519-119">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="4d519-119">Resource ID.</span></span>

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

### <span data-ttu-id="4d519-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d519-120">CommonParameters</span></span>
<span data-ttu-id="4d519-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d519-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d519-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d519-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d519-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d519-123">INPUTS</span></span>

### <span data-ttu-id="4d519-124">System. String</span><span class="sxs-lookup"><span data-stu-id="4d519-124">System.String</span></span>

## <span data-ttu-id="4d519-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d519-125">OUTPUTS</span></span>

### <span data-ttu-id="4d519-126">Microsoft. Azure. Commands. Security. Models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="4d519-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="4d519-127">Note</span><span class="sxs-lookup"><span data-stu-id="4d519-127">NOTES</span></span>

## <span data-ttu-id="4d519-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d519-128">RELATED LINKS</span></span>
