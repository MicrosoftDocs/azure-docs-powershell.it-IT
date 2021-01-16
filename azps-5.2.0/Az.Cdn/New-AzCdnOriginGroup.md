---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
ms.openlocfilehash: 9c499fe716df97edc4644729dc996bd4f9bae992
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362834"
---
# <span data-ttu-id="5c906-101">New-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="5c906-101">New-AzCdnOriginGroup</span></span>

## <span data-ttu-id="5c906-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5c906-102">SYNOPSIS</span></span>
<span data-ttu-id="5c906-103">Crea un nuovo gruppo di origini CDN</span><span class="sxs-lookup"><span data-stu-id="5c906-103">Creates a new CDN origin group</span></span>

## <span data-ttu-id="5c906-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c906-104">SYNTAX</span></span>

### <span data-ttu-id="5c906-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5c906-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5c906-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c906-106">ByObjectParameterSet</span></span>
```
New-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c906-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c906-107">DESCRIPTION</span></span>
<span data-ttu-id="5c906-108">La New-AzCdnOriginGroup creerà un nuovo gruppo di origine all'interno dell'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="5c906-108">The New-AzCdnOriginGroup will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="5c906-109">Se si tratta del primo gruppo di origine per endpoint, deve essere impostata anche la proprietà DefaultOriginGroup.</span><span class="sxs-lookup"><span data-stu-id="5c906-109">If this is the first origin group for endpoint, then the DefaultOriginGroup property must also be set.</span></span>

## <span data-ttu-id="5c906-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c906-110">EXAMPLES</span></span>

### <span data-ttu-id="5c906-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5c906-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originId
```
<span data-ttu-id="5c906-112">Questo cmdlet creerà un nuovo gruppo di origini nell'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="5c906-112">This cmdlet will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="5c906-113">Utilizzerà gli ID di origine specificati come set di origini.</span><span class="sxs-lookup"><span data-stu-id="5c906-113">It will utilize the given origin ids as the set of origins.</span></span>

## <span data-ttu-id="5c906-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5c906-114">PARAMETERS</span></span>

### <span data-ttu-id="5c906-115">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="5c906-115">-CdnOriginGroup</span></span>
<span data-ttu-id="5c906-116">Oggetto gruppo origine CDN.</span><span class="sxs-lookup"><span data-stu-id="5c906-116">The CDN origin group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.OriginGroup.PSOriginGroup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c906-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c906-117">-DefaultProfile</span></span>
<span data-ttu-id="5c906-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5c906-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c906-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="5c906-119">-EndpointName</span></span>
<span data-ttu-id="5c906-120">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="5c906-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="5c906-121">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="5c906-121">-OriginGroupName</span></span>
<span data-ttu-id="5c906-122">Nome del gruppo origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="5c906-122">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="5c906-123">-OriginId</span><span class="sxs-lookup"><span data-stu-id="5c906-123">-OriginId</span></span>
<span data-ttu-id="5c906-124">ID del gruppo di origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="5c906-124">Azure CDN origin group ids.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c906-125">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="5c906-125">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="5c906-126">Numero di secondi tra le sonde di integrità.</span><span class="sxs-lookup"><span data-stu-id="5c906-126">The number of seconds between health probes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c906-127">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="5c906-127">-ProbePath</span></span>
<span data-ttu-id="5c906-128">Il percorso relativo all'origine che viene usato per determinare lo stato dell'origine.</span><span class="sxs-lookup"><span data-stu-id="5c906-128">The path relative to the origin that is used to determine the health of the origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c906-129">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="5c906-129">-ProbeProtocol</span></span>
<span data-ttu-id="5c906-130">Protocollo da usare per la sonda integrità.</span><span class="sxs-lookup"><span data-stu-id="5c906-130">Protocol to use for health probe.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c906-131">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="5c906-131">-ProbeRequestType</span></span>
<span data-ttu-id="5c906-132">Tipo di richiesta di probe di integrità effettuata.</span><span class="sxs-lookup"><span data-stu-id="5c906-132">The type of health probe request that is made.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c906-133">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="5c906-133">-ProfileName</span></span>
<span data-ttu-id="5c906-134">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="5c906-134">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="5c906-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c906-135">-ResourceGroupName</span></span>
<span data-ttu-id="5c906-136">Gruppo risorse del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="5c906-136">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="5c906-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5c906-137">-Confirm</span></span>
<span data-ttu-id="5c906-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c906-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c906-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c906-139">-WhatIf</span></span>
<span data-ttu-id="5c906-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c906-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5c906-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c906-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c906-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c906-142">CommonParameters</span></span>
<span data-ttu-id="5c906-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c906-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c906-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c906-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c906-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5c906-145">INPUTS</span></span>

### <span data-ttu-id="5c906-146">System. Object</span><span class="sxs-lookup"><span data-stu-id="5c906-146">System.Object</span></span>

## <span data-ttu-id="5c906-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c906-147">OUTPUTS</span></span>

### <span data-ttu-id="5c906-148">System. Object</span><span class="sxs-lookup"><span data-stu-id="5c906-148">System.Object</span></span>

## <span data-ttu-id="5c906-149">Note</span><span class="sxs-lookup"><span data-stu-id="5c906-149">NOTES</span></span>

## <span data-ttu-id="5c906-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c906-150">RELATED LINKS</span></span>
