---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 1C45A450-CFD5-40CE-871C-1C2521A03073
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/stop-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Stop-AzCdnEndpoint.md
ms.openlocfilehash: e1afa87d1ab21222987a4eeecf68a3786934ef57
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477963"
---
# <span data-ttu-id="923d0-101">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="923d0-101">Stop-AzCdnEndpoint</span></span>

## <span data-ttu-id="923d0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="923d0-102">SYNOPSIS</span></span>
<span data-ttu-id="923d0-103">Interrompe l'endpoint della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="923d0-103">Stops the CDN endpoint.</span></span>

## <span data-ttu-id="923d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="923d0-104">SYNTAX</span></span>

### <span data-ttu-id="923d0-105">ByFieldsParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="923d0-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="923d0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="923d0-106">ByObjectParameterSet</span></span>
```
Stop-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="923d0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="923d0-107">DESCRIPTION</span></span>
<span data-ttu-id="923d0-108">Il cmdlet **Stop-AzCdnEndpoint** arresta l'endpoint della rete di distribuzione del contenuto di Azure (CDN).</span><span class="sxs-lookup"><span data-stu-id="923d0-108">The **Stop-AzCdnEndpoint** cmdlet stops the Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="923d0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="923d0-109">EXAMPLES</span></span>

## <span data-ttu-id="923d0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="923d0-110">PARAMETERS</span></span>

### <span data-ttu-id="923d0-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="923d0-111">-CdnEndpoint</span></span>
<span data-ttu-id="923d0-112">Specifica l'oggetto endpoint che questo cmdlet si arresta.</span><span class="sxs-lookup"><span data-stu-id="923d0-112">Specifies the endpoint object that this cmdlet stops.</span></span>

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

### <span data-ttu-id="923d0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="923d0-113">-DefaultProfile</span></span>
<span data-ttu-id="923d0-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="923d0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="923d0-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="923d0-115">-EndpointName</span></span>
<span data-ttu-id="923d0-116">Specifica il nome dell'endpoint interrotto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="923d0-116">Specifies the name of the endpoint that this cmdlet stops.</span></span>

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

### <span data-ttu-id="923d0-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="923d0-117">-PassThru</span></span>
<span data-ttu-id="923d0-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="923d0-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="923d0-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="923d0-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="923d0-120">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="923d0-120">-ProfileName</span></span>
<span data-ttu-id="923d0-121">Specifica il nome del profilo a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="923d0-121">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="923d0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="923d0-122">-ResourceGroupName</span></span>
<span data-ttu-id="923d0-123">Specifica il nome del gruppo di risorse a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="923d0-123">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="923d0-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="923d0-124">-Confirm</span></span>
<span data-ttu-id="923d0-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="923d0-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="923d0-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="923d0-126">-WhatIf</span></span>
<span data-ttu-id="923d0-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="923d0-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="923d0-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="923d0-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="923d0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="923d0-129">CommonParameters</span></span>
<span data-ttu-id="923d0-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="923d0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="923d0-131">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="923d0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="923d0-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="923d0-132">INPUTS</span></span>

### <span data-ttu-id="923d0-133">Microsoft. Azure. Commands. CDN. Models. endpoint. PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="923d0-133">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="923d0-134">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="923d0-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="923d0-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="923d0-135">OUTPUTS</span></span>

### <span data-ttu-id="923d0-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="923d0-136">System.Boolean</span></span>

## <span data-ttu-id="923d0-137">Note</span><span class="sxs-lookup"><span data-stu-id="923d0-137">NOTES</span></span>

## <span data-ttu-id="923d0-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="923d0-138">RELATED LINKS</span></span>

[<span data-ttu-id="923d0-139">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="923d0-139">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="923d0-140">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="923d0-140">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="923d0-141">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="923d0-141">Remove-AzCdnEndpoint</span></span>](./Remove-AzCdnEndpoint.md)

[<span data-ttu-id="923d0-142">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="923d0-142">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="923d0-143">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="923d0-143">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)


