---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
ms.openlocfilehash: 8198d189d9619528bdc7fb80d30285ce9126dfed
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202558"
---
# <span data-ttu-id="8a2c3-101">Remove-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="8a2c3-101">Remove-AzCdnOrigin</span></span>

## <span data-ttu-id="8a2c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a2c3-102">SYNOPSIS</span></span>
<span data-ttu-id="8a2c3-103">Rimuove un'origine CDN</span><span class="sxs-lookup"><span data-stu-id="8a2c3-103">Removes a CDN origin</span></span>

## <span data-ttu-id="8a2c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a2c3-104">SYNTAX</span></span>

### <span data-ttu-id="8a2c3-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8a2c3-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOrigin -OriginName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8a2c3-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a2c3-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOrigin -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a2c3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a2c3-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOrigin [-PassThru] -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a2c3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a2c3-108">DESCRIPTION</span></span>
<span data-ttu-id="8a2c3-109">Remove-AzCdnOrigin eliminerà un'origine CDN dall'endpoint indicato.</span><span class="sxs-lookup"><span data-stu-id="8a2c3-109">Remove-AzCdnOrigin will delete a CDN origin from the given endpoint.</span></span> <span data-ttu-id="8a2c3-110">Se l'origine è l'unica origine all'interno dell'endpoint specificato, l'eliminazione avrà esito negativo perché è necessaria almeno 1 origine.</span><span class="sxs-lookup"><span data-stu-id="8a2c3-110">If the origin is the only origin within the specified endpoint, then the deletion will fail since at least 1 origin is needed.</span></span> 

## <span data-ttu-id="8a2c3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a2c3-111">EXAMPLES</span></span>

### <span data-ttu-id="8a2c3-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8a2c3-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName 
```
<span data-ttu-id="8a2c3-113">Questo cmdlet rimuoverà l'origine specificata dall'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="8a2c3-113">This cmdlet will remove the specified origin from the given endpoint.</span></span> 

## <span data-ttu-id="8a2c3-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a2c3-114">PARAMETERS</span></span>

### <span data-ttu-id="8a2c3-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="8a2c3-115">-CdnOrigin</span></span>
<span data-ttu-id="8a2c3-116">Oggetto origine CDN.</span><span class="sxs-lookup"><span data-stu-id="8a2c3-116">The CDN origin object.</span></span>

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

### <span data-ttu-id="8a2c3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a2c3-117">-DefaultProfile</span></span>
<span data-ttu-id="8a2c3-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8a2c3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a2c3-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="8a2c3-119">-EndpointName</span></span>
<span data-ttu-id="8a2c3-120">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="8a2c3-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="8a2c3-121">-Originname</span><span class="sxs-lookup"><span data-stu-id="8a2c3-121">-OriginName</span></span>
<span data-ttu-id="8a2c3-122">Nome origine di Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="8a2c3-122">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="8a2c3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a2c3-123">-PassThru</span></span>
<span data-ttu-id="8a2c3-124">Restituisce l'oggetto se specificato.</span><span class="sxs-lookup"><span data-stu-id="8a2c3-124">Return object if specified.</span></span>

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

### <span data-ttu-id="8a2c3-125">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="8a2c3-125">-ProfileName</span></span>
<span data-ttu-id="8a2c3-126">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="8a2c3-126">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="8a2c3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a2c3-127">-ResourceGroupName</span></span>
<span data-ttu-id="8a2c3-128">Gruppo risorse del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="8a2c3-128">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="8a2c3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a2c3-129">-ResourceId</span></span>
<span data-ttu-id="8a2c3-130">ID risorsa dell'origine della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="8a2c3-130">The resource id of the Azure CDN origin.</span></span>

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

### <span data-ttu-id="8a2c3-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8a2c3-131">-Confirm</span></span>
<span data-ttu-id="8a2c3-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a2c3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a2c3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a2c3-133">-WhatIf</span></span>
<span data-ttu-id="8a2c3-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a2c3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a2c3-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8a2c3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a2c3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a2c3-136">CommonParameters</span></span>
<span data-ttu-id="8a2c3-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a2c3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a2c3-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8a2c3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a2c3-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a2c3-139">INPUTS</span></span>

### <span data-ttu-id="8a2c3-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8a2c3-140">None</span></span>

## <span data-ttu-id="8a2c3-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a2c3-141">OUTPUTS</span></span>

### <span data-ttu-id="8a2c3-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8a2c3-142">System.Boolean</span></span>

## <span data-ttu-id="8a2c3-143">Note</span><span class="sxs-lookup"><span data-stu-id="8a2c3-143">NOTES</span></span>

## <span data-ttu-id="8a2c3-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a2c3-144">RELATED LINKS</span></span>
