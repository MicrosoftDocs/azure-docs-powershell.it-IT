---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/powershell/module/az.cdn/stop-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
ms.openlocfilehash: 93b1c0869793c30b6f733699029aca7bba9d613e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952813"
---
# <span data-ttu-id="e6cba-101">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6cba-101">Stop-AzCdnEndpoint</span></span>

## <span data-ttu-id="e6cba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6cba-102">SYNOPSIS</span></span>
<span data-ttu-id="e6cba-103">Interrompe l'endpoint della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="e6cba-103">Stops the CDN endpoint.</span></span>

## <span data-ttu-id="e6cba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6cba-104">SYNTAX</span></span>

### <span data-ttu-id="e6cba-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e6cba-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6cba-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6cba-106">ByObjectParameterSet</span></span>
```
Stop-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6cba-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e6cba-107">DESCRIPTION</span></span>
<span data-ttu-id="e6cba-108">Il cmdlet **Stop-AzCdnEndpoint** interrompe l'endpoint della rete per la distribuzione di contenuti (CDN) di Azure.</span><span class="sxs-lookup"><span data-stu-id="e6cba-108">The **Stop-AzCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="e6cba-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6cba-109">EXAMPLES</span></span>

## <span data-ttu-id="e6cba-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e6cba-110">PARAMETERS</span></span>

### <span data-ttu-id="e6cba-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6cba-111">-CdnEndpoint</span></span>
<span data-ttu-id="e6cba-112">Specifica l'oggetto endpoint interrotto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6cba-112">Specifies the endpoint object that this cmdlet stops.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6cba-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6cba-113">-DefaultProfile</span></span>
<span data-ttu-id="e6cba-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e6cba-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6cba-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="e6cba-115">-EndpointName</span></span>
<span data-ttu-id="e6cba-116">Specifica il nome dell'endpoint a cui il cmdlet si arresta.</span><span class="sxs-lookup"><span data-stu-id="e6cba-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="e6cba-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e6cba-117">-PassThru</span></span>
<span data-ttu-id="e6cba-118">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="e6cba-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e6cba-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="e6cba-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e6cba-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e6cba-120">-ProfileName</span></span>
<span data-ttu-id="e6cba-121">Specifica il nome del profilo a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="e6cba-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="e6cba-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6cba-122">-ResourceGroupName</span></span>
<span data-ttu-id="e6cba-123">Specifica il nome del gruppo di risorse a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="e6cba-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="e6cba-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6cba-124">-Confirm</span></span>
<span data-ttu-id="e6cba-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6cba-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cba-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6cba-126">-WhatIf</span></span>
<span data-ttu-id="e6cba-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6cba-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6cba-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6cba-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6cba-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6cba-129">CommonParameters</span></span>
<span data-ttu-id="e6cba-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6cba-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6cba-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e6cba-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6cba-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="e6cba-132">INPUTS</span></span>

### <span data-ttu-id="e6cba-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6cba-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="e6cba-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e6cba-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e6cba-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6cba-135">OUTPUTS</span></span>

### <span data-ttu-id="e6cba-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e6cba-136">System.Boolean</span></span>

## <span data-ttu-id="e6cba-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="e6cba-137">NOTES</span></span>

## <span data-ttu-id="e6cba-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6cba-138">RELATED LINKS</span></span>

[<span data-ttu-id="e6cba-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6cba-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="e6cba-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6cba-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="e6cba-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6cba-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="e6cba-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6cba-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="e6cba-143">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="e6cba-143">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)


