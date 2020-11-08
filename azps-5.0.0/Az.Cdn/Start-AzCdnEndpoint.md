---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 6477ADC3-0831-493D-8904-F1D787145DD3
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/start-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Start-AzCdnEndpoint.md
ms.openlocfilehash: 85fc0f0687ed3b32492f42f753f67ba1e85a4656
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201098"
---
# <span data-ttu-id="a8630-101">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8630-101">Start-AzCdnEndpoint</span></span>

## <span data-ttu-id="a8630-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8630-102">SYNOPSIS</span></span>
<span data-ttu-id="a8630-103">Avvia un endpoint CDN.</span><span class="sxs-lookup"><span data-stu-id="a8630-103">Starts a CDN endpoint.</span></span>

## <span data-ttu-id="a8630-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8630-104">SYNTAX</span></span>

### <span data-ttu-id="a8630-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a8630-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8630-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8630-106">ByObjectParameterSet</span></span>
```
Start-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8630-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8630-107">DESCRIPTION</span></span>
<span data-ttu-id="a8630-108">Il cmdlet **Start-AzCdnEndpoint** avvia un endpoint della rete CDN (Azure Content Delivery Network).</span><span class="sxs-lookup"><span data-stu-id="a8630-108">The **Start-AzCdnEndpoint** cmdlet starts an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="a8630-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8630-109">EXAMPLES</span></span>

## <span data-ttu-id="a8630-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8630-110">PARAMETERS</span></span>

### <span data-ttu-id="a8630-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8630-111">-CdnEndpoint</span></span>
<span data-ttu-id="a8630-112">Specifica l'endpoint avviato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8630-112">Specifies the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="a8630-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8630-113">-DefaultProfile</span></span>
<span data-ttu-id="a8630-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="a8630-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8630-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="a8630-115">-EndpointName</span></span>
<span data-ttu-id="a8630-116">Specifica il nome dell'endpoint avviato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8630-116">Specifies the name of the endpoint that this cmdlet starts.</span></span>

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

### <span data-ttu-id="a8630-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8630-117">-PassThru</span></span>
<span data-ttu-id="a8630-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="a8630-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a8630-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="a8630-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a8630-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a8630-120">-ProfileName</span></span>
<span data-ttu-id="a8630-121">Specifica il nome del profilo a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="a8630-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="a8630-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8630-122">-ResourceGroupName</span></span>
<span data-ttu-id="a8630-123">Specifica il nome del gruppo di risorse a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="a8630-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="a8630-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a8630-124">-Confirm</span></span>
<span data-ttu-id="a8630-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8630-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8630-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8630-126">-WhatIf</span></span>
<span data-ttu-id="a8630-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8630-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8630-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8630-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8630-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8630-129">CommonParameters</span></span>
<span data-ttu-id="a8630-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8630-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8630-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8630-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8630-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8630-132">INPUTS</span></span>

### <span data-ttu-id="a8630-133">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8630-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="a8630-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a8630-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a8630-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8630-135">OUTPUTS</span></span>

### <span data-ttu-id="a8630-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a8630-136">System.Boolean</span></span>

## <span data-ttu-id="a8630-137">Note</span><span class="sxs-lookup"><span data-stu-id="a8630-137">NOTES</span></span>

## <span data-ttu-id="a8630-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8630-138">RELATED LINKS</span></span>

[<span data-ttu-id="a8630-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8630-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="a8630-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8630-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="a8630-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8630-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="a8630-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8630-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="a8630-143">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="a8630-143">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


