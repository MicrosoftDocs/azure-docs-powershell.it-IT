---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: 98c41f8e9e1592cf0405f42701fc19f3badd9553
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205114"
---
# <span data-ttu-id="561d7-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="561d7-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="561d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="561d7-102">SYNOPSIS</span></span>
<span data-ttu-id="561d7-103">Ottiene un gruppo di origini CDN</span><span class="sxs-lookup"><span data-stu-id="561d7-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="561d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="561d7-104">SYNTAX</span></span>

### <span data-ttu-id="561d7-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="561d7-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="561d7-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="561d7-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="561d7-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="561d7-107">DESCRIPTION</span></span>
<span data-ttu-id="561d7-108">Il cmdlet Get-AzCdnOriginGroup recupera un gruppo di origine CDN.</span><span class="sxs-lookup"><span data-stu-id="561d7-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="561d7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="561d7-109">EXAMPLES</span></span>

### <span data-ttu-id="561d7-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="561d7-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="561d7-111">Questo comando otterrà il gruppo di origini all'interno dell'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="561d7-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="561d7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="561d7-112">PARAMETERS</span></span>

### <span data-ttu-id="561d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="561d7-113">-DefaultProfile</span></span>
<span data-ttu-id="561d7-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="561d7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="561d7-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="561d7-115">-EndpointName</span></span>
<span data-ttu-id="561d7-116">Nome dell'endpoint della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="561d7-116">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="561d7-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="561d7-117">-OriginGroupName</span></span>
<span data-ttu-id="561d7-118">Nome del gruppo di origine della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="561d7-118">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="561d7-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="561d7-119">-ProfileName</span></span>
<span data-ttu-id="561d7-120">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="561d7-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="561d7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="561d7-121">-ResourceGroupName</span></span>
<span data-ttu-id="561d7-122">Gruppo di risorse del profilo della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="561d7-122">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="561d7-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="561d7-123">-ResourceId</span></span>
<span data-ttu-id="561d7-124">ID risorsa per il gruppo di origine</span><span class="sxs-lookup"><span data-stu-id="561d7-124">Resource Id for the the origin group</span></span>

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

### <span data-ttu-id="561d7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="561d7-125">CommonParameters</span></span>
<span data-ttu-id="561d7-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="561d7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="561d7-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="561d7-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="561d7-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="561d7-128">INPUTS</span></span>

### <span data-ttu-id="561d7-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="561d7-129">None</span></span>

## <span data-ttu-id="561d7-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="561d7-130">OUTPUTS</span></span>

### <span data-ttu-id="561d7-131">System.Object</span><span class="sxs-lookup"><span data-stu-id="561d7-131">System.Object</span></span>

## <span data-ttu-id="561d7-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="561d7-132">NOTES</span></span>

## <span data-ttu-id="561d7-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="561d7-133">RELATED LINKS</span></span>
