---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/start-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
ms.openlocfilehash: 85fc0f0687ed3b32492f42f753f67ba1e85a4656
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177862"
---
# <span data-ttu-id="10b97-101">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="10b97-101">Start-AzCdnEndpoint</span></span>

## <span data-ttu-id="10b97-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10b97-102">SYNOPSIS</span></span>
<span data-ttu-id="10b97-103">Avvia un endpoint della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="10b97-103">Starts a CDN endpoint.</span></span>

## <span data-ttu-id="10b97-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10b97-104">SYNTAX</span></span>

### <span data-ttu-id="10b97-105">ByFieldsParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="10b97-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10b97-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10b97-106">ByObjectParameterSet</span></span>
```
Start-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10b97-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="10b97-107">DESCRIPTION</span></span>
<span data-ttu-id="10b97-108">Il cmdlet **Start-AzCdnEndpoint** avvia un endpoint della rete per la distribuzione di contenuti (CDN) di Azure.</span><span class="sxs-lookup"><span data-stu-id="10b97-108">The **Start-AzCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="10b97-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10b97-109">EXAMPLES</span></span>

## <span data-ttu-id="10b97-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10b97-110">PARAMETERS</span></span>

### <span data-ttu-id="10b97-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="10b97-111">-CdnEndpoint</span></span>
<span data-ttu-id="10b97-112">Specifica l'endpoint su cui viene avviato il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10b97-112">Specifies the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="10b97-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10b97-113">-DefaultProfile</span></span>
<span data-ttu-id="10b97-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="10b97-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="10b97-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="10b97-115">-EndpointName</span></span>
<span data-ttu-id="10b97-116">Specifica il nome dell'endpoint da cui viene avviato il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10b97-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="10b97-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="10b97-117">-PassThru</span></span>
<span data-ttu-id="10b97-118">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="10b97-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="10b97-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="10b97-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="10b97-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="10b97-120">-ProfileName</span></span>
<span data-ttu-id="10b97-121">Specifica il nome del profilo a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="10b97-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="10b97-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10b97-122">-ResourceGroupName</span></span>
<span data-ttu-id="10b97-123">Specifica il nome del gruppo di risorse a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="10b97-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="10b97-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10b97-124">-Confirm</span></span>
<span data-ttu-id="10b97-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10b97-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10b97-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10b97-126">-WhatIf</span></span>
<span data-ttu-id="10b97-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10b97-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10b97-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10b97-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10b97-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10b97-129">CommonParameters</span></span>
<span data-ttu-id="10b97-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10b97-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10b97-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="10b97-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10b97-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="10b97-132">INPUTS</span></span>

### <span data-ttu-id="10b97-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="10b97-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="10b97-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="10b97-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="10b97-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10b97-135">OUTPUTS</span></span>

### <span data-ttu-id="10b97-136">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="10b97-136">System.Boolean</span></span>

## <span data-ttu-id="10b97-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="10b97-137">NOTES</span></span>

## <span data-ttu-id="10b97-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10b97-138">RELATED LINKS</span></span>

[<span data-ttu-id="10b97-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="10b97-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="10b97-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="10b97-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="10b97-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="10b97-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="10b97-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="10b97-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="10b97-143">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="10b97-143">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


