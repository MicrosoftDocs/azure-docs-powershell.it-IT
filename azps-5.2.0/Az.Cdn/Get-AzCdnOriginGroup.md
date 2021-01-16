---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: 98c41f8e9e1592cf0405f42701fc19f3badd9553
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364573"
---
# <span data-ttu-id="8ad14-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="8ad14-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="8ad14-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8ad14-102">SYNOPSIS</span></span>
<span data-ttu-id="8ad14-103">Ottiene un gruppo di origini CDN</span><span class="sxs-lookup"><span data-stu-id="8ad14-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="8ad14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ad14-104">SYNTAX</span></span>

### <span data-ttu-id="8ad14-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8ad14-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ad14-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ad14-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ad14-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ad14-107">DESCRIPTION</span></span>
<span data-ttu-id="8ad14-108">Il cmdlet Get-AzCdnOriginGroup recupera un gruppo di origini CDN.</span><span class="sxs-lookup"><span data-stu-id="8ad14-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="8ad14-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ad14-109">EXAMPLES</span></span>

### <span data-ttu-id="8ad14-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8ad14-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="8ad14-111">Questo comando otterrà il gruppo di origine nell'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="8ad14-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="8ad14-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8ad14-112">PARAMETERS</span></span>

### <span data-ttu-id="8ad14-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ad14-113">-DefaultProfile</span></span>
<span data-ttu-id="8ad14-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8ad14-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ad14-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="8ad14-115">-EndpointName</span></span>
<span data-ttu-id="8ad14-116">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="8ad14-116">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="8ad14-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="8ad14-117">-OriginGroupName</span></span>
<span data-ttu-id="8ad14-118">Nome del gruppo origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="8ad14-118">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="8ad14-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="8ad14-119">-ProfileName</span></span>
<span data-ttu-id="8ad14-120">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="8ad14-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="8ad14-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ad14-121">-ResourceGroupName</span></span>
<span data-ttu-id="8ad14-122">Gruppo risorse del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="8ad14-122">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="8ad14-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ad14-123">-ResourceId</span></span>
<span data-ttu-id="8ad14-124">ID risorsa per il gruppo origine</span><span class="sxs-lookup"><span data-stu-id="8ad14-124">Resource Id for the the origin group</span></span>

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

### <span data-ttu-id="8ad14-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ad14-125">CommonParameters</span></span>
<span data-ttu-id="8ad14-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ad14-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ad14-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ad14-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ad14-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8ad14-128">INPUTS</span></span>

### <span data-ttu-id="8ad14-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8ad14-129">None</span></span>

## <span data-ttu-id="8ad14-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ad14-130">OUTPUTS</span></span>

### <span data-ttu-id="8ad14-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="8ad14-131">System.Object</span></span>

## <span data-ttu-id="8ad14-132">Note</span><span class="sxs-lookup"><span data-stu-id="8ad14-132">NOTES</span></span>

## <span data-ttu-id="8ad14-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ad14-133">RELATED LINKS</span></span>
