---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: 98c41f8e9e1592cf0405f42701fc19f3badd9553
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478011"
---
# <span data-ttu-id="56db4-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="56db4-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="56db4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56db4-102">SYNOPSIS</span></span>
<span data-ttu-id="56db4-103">Ottiene un gruppo di origini CDN</span><span class="sxs-lookup"><span data-stu-id="56db4-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="56db4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56db4-104">SYNTAX</span></span>

### <span data-ttu-id="56db4-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="56db4-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56db4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="56db4-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56db4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56db4-107">DESCRIPTION</span></span>
<span data-ttu-id="56db4-108">Il cmdlet Get-AzCdnOriginGroup recupera un gruppo di origini CDN.</span><span class="sxs-lookup"><span data-stu-id="56db4-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="56db4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56db4-109">EXAMPLES</span></span>

### <span data-ttu-id="56db4-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="56db4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="56db4-111">Questo comando otterrà il gruppo di origine nell'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="56db4-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="56db4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56db4-112">PARAMETERS</span></span>

### <span data-ttu-id="56db4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56db4-113">-DefaultProfile</span></span>
<span data-ttu-id="56db4-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56db4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56db4-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="56db4-115">-EndpointName</span></span>
<span data-ttu-id="56db4-116">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="56db4-116">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56db4-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="56db4-117">-OriginGroupName</span></span>
<span data-ttu-id="56db4-118">Nome del gruppo origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="56db4-118">Azure CDN origin group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56db4-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="56db4-119">-ProfileName</span></span>
<span data-ttu-id="56db4-120">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="56db4-120">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56db4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56db4-121">-ResourceGroupName</span></span>
<span data-ttu-id="56db4-122">Gruppo risorse del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="56db4-122">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56db4-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56db4-123">-ResourceId</span></span>
<span data-ttu-id="56db4-124">ID risorsa per il gruppo origine</span><span class="sxs-lookup"><span data-stu-id="56db4-124">Resource Id for the the origin group</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56db4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56db4-125">CommonParameters</span></span>
<span data-ttu-id="56db4-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56db4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56db4-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="56db4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56db4-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56db4-128">INPUTS</span></span>

### <span data-ttu-id="56db4-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="56db4-129">None</span></span>

## <span data-ttu-id="56db4-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56db4-130">OUTPUTS</span></span>

### <span data-ttu-id="56db4-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="56db4-131">System.Object</span></span>

## <span data-ttu-id="56db4-132">Note</span><span class="sxs-lookup"><span data-stu-id="56db4-132">NOTES</span></span>

## <span data-ttu-id="56db4-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56db4-133">RELATED LINKS</span></span>
