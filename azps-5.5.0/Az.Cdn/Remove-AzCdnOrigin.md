---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
ms.openlocfilehash: 8198d189d9619528bdc7fb80d30285ce9126dfed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200758"
---
# <span data-ttu-id="722dd-101">Remove-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="722dd-101">Remove-AzCdnOrigin</span></span>

## <span data-ttu-id="722dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="722dd-102">SYNOPSIS</span></span>
<span data-ttu-id="722dd-103">Rimuove un'origine CDN</span><span class="sxs-lookup"><span data-stu-id="722dd-103">Removes a CDN origin</span></span>

## <span data-ttu-id="722dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="722dd-104">SYNTAX</span></span>

### <span data-ttu-id="722dd-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="722dd-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOrigin -OriginName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="722dd-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="722dd-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOrigin -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="722dd-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="722dd-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOrigin [-PassThru] -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="722dd-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="722dd-108">DESCRIPTION</span></span>
<span data-ttu-id="722dd-109">Remove-AzCdnOrigin eliminerà un'origine CDN dall'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="722dd-109">Remove-AzCdnOrigin will delete a CDN origin from the given endpoint.</span></span> <span data-ttu-id="722dd-110">Se l'origine è l'unica origine all'interno dell'endpoint specificato, l'eliminazione non riuscirà perché è necessaria almeno un'origine.</span><span class="sxs-lookup"><span data-stu-id="722dd-110">If the origin is the only origin within the specified endpoint, then the deletion will fail since at least 1 origin is needed.</span></span> 

## <span data-ttu-id="722dd-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="722dd-111">EXAMPLES</span></span>

### <span data-ttu-id="722dd-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="722dd-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName 
```
<span data-ttu-id="722dd-113">Questo cmdlet rimuoverà l'origine specificata dall'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="722dd-113">This cmdlet will remove the specified origin from the given endpoint.</span></span> 

## <span data-ttu-id="722dd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="722dd-114">PARAMETERS</span></span>

### <span data-ttu-id="722dd-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="722dd-115">-CdnOrigin</span></span>
<span data-ttu-id="722dd-116">Oggetto origine CDN.</span><span class="sxs-lookup"><span data-stu-id="722dd-116">The CDN origin object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="722dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="722dd-117">-DefaultProfile</span></span>
<span data-ttu-id="722dd-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="722dd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="722dd-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="722dd-119">-EndpointName</span></span>
<span data-ttu-id="722dd-120">Nome dell'endpoint della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="722dd-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="722dd-121">-OriginName</span><span class="sxs-lookup"><span data-stu-id="722dd-121">-OriginName</span></span>
<span data-ttu-id="722dd-122">Nome di origine della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="722dd-122">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="722dd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="722dd-123">-PassThru</span></span>
<span data-ttu-id="722dd-124">Oggetto restituito, se specificato.</span><span class="sxs-lookup"><span data-stu-id="722dd-124">Return object if specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="722dd-125">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="722dd-125">-ProfileName</span></span>
<span data-ttu-id="722dd-126">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="722dd-126">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="722dd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="722dd-127">-ResourceGroupName</span></span>
<span data-ttu-id="722dd-128">Gruppo di risorse del profilo della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="722dd-128">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="722dd-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="722dd-129">-ResourceId</span></span>
<span data-ttu-id="722dd-130">ID risorsa dell'origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="722dd-130">The resource id of the Azure CDN origin.</span></span>

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

### <span data-ttu-id="722dd-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="722dd-131">-Confirm</span></span>
<span data-ttu-id="722dd-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="722dd-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="722dd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="722dd-133">-WhatIf</span></span>
<span data-ttu-id="722dd-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="722dd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="722dd-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="722dd-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="722dd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="722dd-136">CommonParameters</span></span>
<span data-ttu-id="722dd-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="722dd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="722dd-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="722dd-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="722dd-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="722dd-139">INPUTS</span></span>

### <span data-ttu-id="722dd-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="722dd-140">None</span></span>

## <span data-ttu-id="722dd-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="722dd-141">OUTPUTS</span></span>

### <span data-ttu-id="722dd-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="722dd-142">System.Boolean</span></span>

## <span data-ttu-id="722dd-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="722dd-143">NOTES</span></span>

## <span data-ttu-id="722dd-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="722dd-144">RELATED LINKS</span></span>
