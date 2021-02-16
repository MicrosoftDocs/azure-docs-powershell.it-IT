---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
ms.openlocfilehash: 9c499fe716df97edc4644729dc996bd4f9bae992
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200815"
---
# <span data-ttu-id="7775a-101">New-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="7775a-101">New-AzCdnOriginGroup</span></span>

## <span data-ttu-id="7775a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7775a-102">SYNOPSIS</span></span>
<span data-ttu-id="7775a-103">Crea un nuovo gruppo origine CDN</span><span class="sxs-lookup"><span data-stu-id="7775a-103">Creates a new CDN origin group</span></span>

## <span data-ttu-id="7775a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7775a-104">SYNTAX</span></span>

### <span data-ttu-id="7775a-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7775a-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7775a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7775a-106">ByObjectParameterSet</span></span>
```
New-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7775a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7775a-107">DESCRIPTION</span></span>
<span data-ttu-id="7775a-108">LNew-AzCdnOriginGroup crea un nuovo gruppo di origini all'interno dell'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="7775a-108">The New-AzCdnOriginGroup will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="7775a-109">Se questo è il primo gruppo di origini per l'endpoint, deve essere impostata anche la proprietà DefaultOriginGroup.</span><span class="sxs-lookup"><span data-stu-id="7775a-109">If this is the first origin group for endpoint, then the DefaultOriginGroup property must also be set.</span></span>

## <span data-ttu-id="7775a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7775a-110">EXAMPLES</span></span>

### <span data-ttu-id="7775a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7775a-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originId
```
<span data-ttu-id="7775a-112">Questo cmdlet creerà un nuovo gruppo di origini all'interno dell'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="7775a-112">This cmdlet will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="7775a-113">Verrà utilizzato l'ID origine specificato come set di origini.</span><span class="sxs-lookup"><span data-stu-id="7775a-113">It will utilize the given origin ids as the set of origins.</span></span>

## <span data-ttu-id="7775a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7775a-114">PARAMETERS</span></span>

### <span data-ttu-id="7775a-115">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="7775a-115">-CdnOriginGroup</span></span>
<span data-ttu-id="7775a-116">Oggetto gruppo origine CDN.</span><span class="sxs-lookup"><span data-stu-id="7775a-116">The CDN origin group object.</span></span>

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

### <span data-ttu-id="7775a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7775a-117">-DefaultProfile</span></span>
<span data-ttu-id="7775a-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7775a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7775a-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="7775a-119">-EndpointName</span></span>
<span data-ttu-id="7775a-120">Nome dell'endpoint della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="7775a-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="7775a-121">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="7775a-121">-OriginGroupName</span></span>
<span data-ttu-id="7775a-122">Nome del gruppo di origine della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="7775a-122">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="7775a-123">-OriginId</span><span class="sxs-lookup"><span data-stu-id="7775a-123">-OriginId</span></span>
<span data-ttu-id="7775a-124">ID del gruppo di origine della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="7775a-124">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="7775a-125">-MillisecondIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="7775a-125">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="7775a-126">Il numero di secondi tra l'integrità.</span><span class="sxs-lookup"><span data-stu-id="7775a-126">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="7775a-127">-Path</span><span class="sxs-lookup"><span data-stu-id="7775a-127">-ProbePath</span></span>
<span data-ttu-id="7775a-128">Percorso relativo all'origine usato per determinare l'integrità dell'origine.</span><span class="sxs-lookup"><span data-stu-id="7775a-128">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="7775a-129">-Sempreprotocol</span><span class="sxs-lookup"><span data-stu-id="7775a-129">-ProbeProtocol</span></span>
<span data-ttu-id="7775a-130">Protocollo da usare per l'integrità.</span><span class="sxs-lookup"><span data-stu-id="7775a-130">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="7775a-131">-RequestType</span><span class="sxs-lookup"><span data-stu-id="7775a-131">-ProbeRequestType</span></span>
<span data-ttu-id="7775a-132">Tipo di richiesta di integrità richiesta.</span><span class="sxs-lookup"><span data-stu-id="7775a-132">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="7775a-133">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="7775a-133">-ProfileName</span></span>
<span data-ttu-id="7775a-134">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="7775a-134">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="7775a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7775a-135">-ResourceGroupName</span></span>
<span data-ttu-id="7775a-136">Gruppo di risorse del profilo della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="7775a-136">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="7775a-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7775a-137">-Confirm</span></span>
<span data-ttu-id="7775a-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7775a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7775a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7775a-139">-WhatIf</span></span>
<span data-ttu-id="7775a-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7775a-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7775a-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7775a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7775a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7775a-142">CommonParameters</span></span>
<span data-ttu-id="7775a-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7775a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7775a-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7775a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7775a-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="7775a-145">INPUTS</span></span>

### <span data-ttu-id="7775a-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="7775a-146">System.Object</span></span>

## <span data-ttu-id="7775a-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7775a-147">OUTPUTS</span></span>

### <span data-ttu-id="7775a-148">System.Object</span><span class="sxs-lookup"><span data-stu-id="7775a-148">System.Object</span></span>

## <span data-ttu-id="7775a-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="7775a-149">NOTES</span></span>

## <span data-ttu-id="7775a-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7775a-150">RELATED LINKS</span></span>
