---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: c70c08ad88491d7624b078babb5e62437c22e116
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985331"
---
# <span data-ttu-id="1d64d-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="1d64d-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="1d64d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d64d-102">SYNOPSIS</span></span>
<span data-ttu-id="1d64d-103">Aggiorna il gruppo di origine della rete CDN</span><span class="sxs-lookup"><span data-stu-id="1d64d-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="1d64d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d64d-104">SYNTAX</span></span>

### <span data-ttu-id="1d64d-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1d64d-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1d64d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1d64d-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d64d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1d64d-107">DESCRIPTION</span></span>
<span data-ttu-id="1d64d-108">Set-AzCdnOriginGroup aggiornerà il gruppo di origine specificato all'interno dell'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="1d64d-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="1d64d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d64d-109">EXAMPLES</span></span>

### <span data-ttu-id="1d64d-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1d64d-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="1d64d-111">Questo cmdlet aggiornerà la proprietàIntervalInSeconds nel gruppo di origine.</span><span class="sxs-lookup"><span data-stu-id="1d64d-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="1d64d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d64d-112">PARAMETERS</span></span>

### <span data-ttu-id="1d64d-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="1d64d-113">-CdnOriginGroup</span></span>
<span data-ttu-id="1d64d-114">Oggetto gruppo origine CDN.</span><span class="sxs-lookup"><span data-stu-id="1d64d-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="1d64d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d64d-115">-DefaultProfile</span></span>
<span data-ttu-id="1d64d-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d64d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d64d-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="1d64d-117">-EndpointName</span></span>
<span data-ttu-id="1d64d-118">Nome dell'endpoint della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="1d64d-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="1d64d-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="1d64d-119">-OriginGroupName</span></span>
<span data-ttu-id="1d64d-120">Nome del gruppo di origine della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="1d64d-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="1d64d-121">-OriginId</span><span class="sxs-lookup"><span data-stu-id="1d64d-121">-OriginId</span></span>
<span data-ttu-id="1d64d-122">ID gruppo di origine della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="1d64d-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="1d64d-123">-MillisecondIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="1d64d-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="1d64d-124">Il numero di secondi tra l'integrità.</span><span class="sxs-lookup"><span data-stu-id="1d64d-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="1d64d-125">-Path</span><span class="sxs-lookup"><span data-stu-id="1d64d-125">-ProbePath</span></span>
<span data-ttu-id="1d64d-126">Percorso relativo all'origine usato per determinare l'integrità dell'origine.</span><span class="sxs-lookup"><span data-stu-id="1d64d-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="1d64d-127">-Sempreprotocol</span><span class="sxs-lookup"><span data-stu-id="1d64d-127">-ProbeProtocol</span></span>
<span data-ttu-id="1d64d-128">Protocollo da usare per l'integrità.</span><span class="sxs-lookup"><span data-stu-id="1d64d-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="1d64d-129">-RequestType</span><span class="sxs-lookup"><span data-stu-id="1d64d-129">-ProbeRequestType</span></span>
<span data-ttu-id="1d64d-130">Tipo di richiesta di integrità richiesta.</span><span class="sxs-lookup"><span data-stu-id="1d64d-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="1d64d-131">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="1d64d-131">-ProfileName</span></span>
<span data-ttu-id="1d64d-132">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="1d64d-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="1d64d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d64d-133">-ResourceGroupName</span></span>
<span data-ttu-id="1d64d-134">Gruppo di risorse del profilo della rete CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="1d64d-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="1d64d-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1d64d-135">-Confirm</span></span>
<span data-ttu-id="1d64d-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d64d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d64d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d64d-137">-WhatIf</span></span>
<span data-ttu-id="1d64d-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d64d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d64d-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1d64d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d64d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d64d-140">CommonParameters</span></span>
<span data-ttu-id="1d64d-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d64d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d64d-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1d64d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d64d-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="1d64d-143">INPUTS</span></span>

### <span data-ttu-id="1d64d-144">System.Object</span><span class="sxs-lookup"><span data-stu-id="1d64d-144">System.Object</span></span>

## <span data-ttu-id="1d64d-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d64d-145">OUTPUTS</span></span>

### <span data-ttu-id="1d64d-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="1d64d-146">System.Object</span></span>

## <span data-ttu-id="1d64d-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="1d64d-147">NOTES</span></span>

## <span data-ttu-id="1d64d-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d64d-148">RELATED LINKS</span></span>
