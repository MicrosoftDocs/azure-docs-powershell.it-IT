---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 7ADF4CDE-638B-4E00-88B1-688702B084A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnEndpoint.md
ms.openlocfilehash: 780765ea56cd13ee7cbd09b64dc20db896234aec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200759"
---
# <span data-ttu-id="f0692-101">Remove-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f0692-101">Remove-AzCdnEndpoint</span></span>

## <span data-ttu-id="f0692-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0692-102">SYNOPSIS</span></span>
<span data-ttu-id="f0692-103">Rimuove un endpoint della rete CDN.</span><span class="sxs-lookup"><span data-stu-id="f0692-103">Removes a CDN endpoint.</span></span>

## <span data-ttu-id="f0692-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0692-104">SYNTAX</span></span>

### <span data-ttu-id="f0692-105">ByFieldsParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0692-105">ByFieldsParameterSet</span></span>
```
Remove-AzCdnEndpoint -EndpointName <String> -ProfileName <String> -ResourceGroupName <String> [-PassThru]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0692-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0692-106">ByObjectParameterSet</span></span>
```
Remove-AzCdnEndpoint -CdnEndpoint <PSEndpoint> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0692-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f0692-107">DESCRIPTION</span></span>
<span data-ttu-id="f0692-108">Il cmdlet **Remove-AzCdnEndpoint** rimuove un endpoint della rete per la distribuzione di contenuti (CDN) di Azure.</span><span class="sxs-lookup"><span data-stu-id="f0692-108">The **Remove-AzCdnEndpoint** cmdlet removes an Azure Content Delivery Network (CDN) endpoint.</span></span>

## <span data-ttu-id="f0692-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0692-109">EXAMPLES</span></span>

## <span data-ttu-id="f0692-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0692-110">PARAMETERS</span></span>

### <span data-ttu-id="f0692-111">-CdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f0692-111">-CdnEndpoint</span></span>
<span data-ttu-id="f0692-112">Specifica l'endpoint rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0692-112">Specifies the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f0692-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0692-113">-DefaultProfile</span></span>
<span data-ttu-id="f0692-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="f0692-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0692-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f0692-115">-EndpointName</span></span>
<span data-ttu-id="f0692-116">Specifica il nome dell'endpoint rimosso dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0692-116">Specifies the name of the endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f0692-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f0692-117">-Force</span></span>
<span data-ttu-id="f0692-118">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="f0692-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0692-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0692-119">-PassThru</span></span>
<span data-ttu-id="f0692-120">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="f0692-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f0692-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="f0692-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f0692-122">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="f0692-122">-ProfileName</span></span>
<span data-ttu-id="f0692-123">Specifica il nome del profilo a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="f0692-123">Specifies the name of the profile to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="f0692-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0692-124">-ResourceGroupName</span></span>
<span data-ttu-id="f0692-125">Specifica il nome del gruppo di risorse a cui appartiene l'endpoint.</span><span class="sxs-lookup"><span data-stu-id="f0692-125">Specifies the name of the resource group to which the endpoint belongs.</span></span>

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

### <span data-ttu-id="f0692-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0692-126">-Confirm</span></span>
<span data-ttu-id="f0692-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0692-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0692-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0692-128">-WhatIf</span></span>
<span data-ttu-id="f0692-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0692-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0692-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f0692-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0692-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0692-131">CommonParameters</span></span>
<span data-ttu-id="f0692-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0692-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0692-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f0692-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0692-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="f0692-134">INPUTS</span></span>

### <span data-ttu-id="f0692-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span><span class="sxs-lookup"><span data-stu-id="f0692-135">Microsoft.Azure.Commands.Cdn.Models.Endpoint.PSEndpoint</span></span>

### <span data-ttu-id="f0692-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f0692-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f0692-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0692-137">OUTPUTS</span></span>

### <span data-ttu-id="f0692-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f0692-138">System.Boolean</span></span>

## <span data-ttu-id="f0692-139">NOTE</span><span class="sxs-lookup"><span data-stu-id="f0692-139">NOTES</span></span>

## <span data-ttu-id="f0692-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0692-140">RELATED LINKS</span></span>

[<span data-ttu-id="f0692-141">Get-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f0692-141">Get-AzCdnEndpoint</span></span>](./Get-AzCdnEndpoint.md)

[<span data-ttu-id="f0692-142">New-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f0692-142">New-AzCdnEndpoint</span></span>](./New-AzCdnEndpoint.md)

[<span data-ttu-id="f0692-143">Set-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f0692-143">Set-AzCdnEndpoint</span></span>](./Set-AzCdnEndpoint.md)

[<span data-ttu-id="f0692-144">Start-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f0692-144">Start-AzCdnEndpoint</span></span>](./Start-AzCdnEndpoint.md)

[<span data-ttu-id="f0692-145">Stop-AzCdnEndpoint</span><span class="sxs-lookup"><span data-stu-id="f0692-145">Stop-AzCdnEndpoint</span></span>](./Stop-AzCdnEndpoint.md)


