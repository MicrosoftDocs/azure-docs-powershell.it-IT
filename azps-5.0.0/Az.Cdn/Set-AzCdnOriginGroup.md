---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: 58a9d45c29a9a11b31bff510e6b4e1c63844dd5d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201101"
---
# <span data-ttu-id="9bd5b-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="9bd5b-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="9bd5b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9bd5b-102">SYNOPSIS</span></span>
<span data-ttu-id="9bd5b-103">Aggiorna il gruppo origine CDN</span><span class="sxs-lookup"><span data-stu-id="9bd5b-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="9bd5b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9bd5b-104">SYNTAX</span></span>

### <span data-ttu-id="9bd5b-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9bd5b-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9bd5b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bd5b-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bd5b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bd5b-107">DESCRIPTION</span></span>
<span data-ttu-id="9bd5b-108">Set-AzCdnOriginGroup aggiornerà il gruppo di origine specificato nell'endpoint specificato.</span><span class="sxs-lookup"><span data-stu-id="9bd5b-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="9bd5b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9bd5b-109">EXAMPLES</span></span>

### <span data-ttu-id="9bd5b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9bd5b-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="9bd5b-111">Questo cmdlet aggiornerà la proprietà ProbeIntervalInSeconds nel gruppo Origin.</span><span class="sxs-lookup"><span data-stu-id="9bd5b-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="9bd5b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9bd5b-112">PARAMETERS</span></span>

### <span data-ttu-id="9bd5b-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="9bd5b-113">-CdnOriginGroup</span></span>
<span data-ttu-id="9bd5b-114">Oggetto gruppo origine CDN.</span><span class="sxs-lookup"><span data-stu-id="9bd5b-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="9bd5b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bd5b-115">-DefaultProfile</span></span>
<span data-ttu-id="9bd5b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9bd5b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bd5b-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="9bd5b-117">-EndpointName</span></span>
<span data-ttu-id="9bd5b-118">Nome dell'endpoint CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="9bd5b-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="9bd5b-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="9bd5b-119">-OriginGroupName</span></span>
<span data-ttu-id="9bd5b-120">Nome del gruppo origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="9bd5b-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="9bd5b-121">-OriginId</span><span class="sxs-lookup"><span data-stu-id="9bd5b-121">-OriginId</span></span>
<span data-ttu-id="9bd5b-122">ID del gruppo di origine CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="9bd5b-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="9bd5b-123">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="9bd5b-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="9bd5b-124">Numero di secondi tra le sonde di integrità.</span><span class="sxs-lookup"><span data-stu-id="9bd5b-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="9bd5b-125">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="9bd5b-125">-ProbePath</span></span>
<span data-ttu-id="9bd5b-126">Il percorso relativo all'origine che viene usato per determinare lo stato dell'origine.</span><span class="sxs-lookup"><span data-stu-id="9bd5b-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="9bd5b-127">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="9bd5b-127">-ProbeProtocol</span></span>
<span data-ttu-id="9bd5b-128">Protocollo da usare per la sonda integrità.</span><span class="sxs-lookup"><span data-stu-id="9bd5b-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="9bd5b-129">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="9bd5b-129">-ProbeRequestType</span></span>
<span data-ttu-id="9bd5b-130">Tipo di richiesta di probe di integrità effettuata.</span><span class="sxs-lookup"><span data-stu-id="9bd5b-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="9bd5b-131">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="9bd5b-131">-ProfileName</span></span>
<span data-ttu-id="9bd5b-132">Nome del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="9bd5b-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="9bd5b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bd5b-133">-ResourceGroupName</span></span>
<span data-ttu-id="9bd5b-134">Gruppo risorse del profilo CDN di Azure.</span><span class="sxs-lookup"><span data-stu-id="9bd5b-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="9bd5b-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9bd5b-135">-Confirm</span></span>
<span data-ttu-id="9bd5b-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bd5b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bd5b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bd5b-137">-WhatIf</span></span>
<span data-ttu-id="9bd5b-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9bd5b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bd5b-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9bd5b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bd5b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bd5b-140">CommonParameters</span></span>
<span data-ttu-id="9bd5b-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bd5b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bd5b-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9bd5b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bd5b-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9bd5b-143">INPUTS</span></span>

### <span data-ttu-id="9bd5b-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="9bd5b-144">System.Object</span></span>

## <span data-ttu-id="9bd5b-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9bd5b-145">OUTPUTS</span></span>

### <span data-ttu-id="9bd5b-146">System. Object</span><span class="sxs-lookup"><span data-stu-id="9bd5b-146">System.Object</span></span>

## <span data-ttu-id="9bd5b-147">Note</span><span class="sxs-lookup"><span data-stu-id="9bd5b-147">NOTES</span></span>

## <span data-ttu-id="9bd5b-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9bd5b-148">RELATED LINKS</span></span>
