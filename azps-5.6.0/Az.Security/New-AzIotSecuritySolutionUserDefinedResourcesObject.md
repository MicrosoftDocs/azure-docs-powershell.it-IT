---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/New-AzIotSecuritySolutionUserDefinedResourcesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
ms.openlocfilehash: 2b524234b18e84247c3789119fbfe1d214514fec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984142"
---
# <span data-ttu-id="b56f1-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span><span class="sxs-lookup"><span data-stu-id="b56f1-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span></span>

## <span data-ttu-id="b56f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b56f1-102">SYNOPSIS</span></span>
<span data-ttu-id="b56f1-103">Creare nuove risorse definite dall'utente per una soluzione di sicurezza iot</span><span class="sxs-lookup"><span data-stu-id="b56f1-103">Create new user defined resources for iot security solution</span></span>

## <span data-ttu-id="b56f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b56f1-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionUserDefinedResourcesObject -Query <String> -QuerySubscriptionList <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b56f1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b56f1-105">DESCRIPTION</span></span>
<span data-ttu-id="b56f1-106">Il cmdlet AzIotSecuritySolutionUserDefinedResourcesObject crea un nuovo oggetto risorse definito dall'utente per la soluzione di sicurezza iot.</span><span class="sxs-lookup"><span data-stu-id="b56f1-106">The AzIotSecuritySolutionUserDefinedResourcesObject cmdlet creates a new user defined resources object for the iot security solution.</span></span>

## <span data-ttu-id="b56f1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b56f1-107">EXAMPLES</span></span>

### <span data-ttu-id="b56f1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b56f1-108">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")

Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
QuerySubscriptions: ["XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX"]
```

<span data-ttu-id="b56f1-109">Creare nuove risorse definite dall'utente</span><span class="sxs-lookup"><span data-stu-id="b56f1-109">Create new user defined resources</span></span>

## <span data-ttu-id="b56f1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b56f1-110">PARAMETERS</span></span>

### <span data-ttu-id="b56f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b56f1-111">-DefaultProfile</span></span>
<span data-ttu-id="b56f1-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b56f1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b56f1-113">-Query</span><span class="sxs-lookup"><span data-stu-id="b56f1-113">-Query</span></span>
<span data-ttu-id="b56f1-114">Query.</span><span class="sxs-lookup"><span data-stu-id="b56f1-114">Query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56f1-115">-QuerySubscriptionList</span><span class="sxs-lookup"><span data-stu-id="b56f1-115">-QuerySubscriptionList</span></span>
<span data-ttu-id="b56f1-116">Sottoscrizioni di query.</span><span class="sxs-lookup"><span data-stu-id="b56f1-116">Query subscriptions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56f1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b56f1-117">CommonParameters</span></span>
<span data-ttu-id="b56f1-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b56f1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b56f1-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b56f1-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b56f1-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="b56f1-120">INPUTS</span></span>

### <span data-ttu-id="b56f1-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b56f1-121">None</span></span>

## <span data-ttu-id="b56f1-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b56f1-122">OUTPUTS</span></span>

### <span data-ttu-id="b56f1-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="b56f1-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

## <span data-ttu-id="b56f1-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="b56f1-124">NOTES</span></span>

## <span data-ttu-id="b56f1-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b56f1-125">RELATED LINKS</span></span>
