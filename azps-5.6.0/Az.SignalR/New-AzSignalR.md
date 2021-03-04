---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 62beafd5546a52bd8e9cc61fae8ff90f7cd2ed1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955485"
---
# <span data-ttu-id="d55b1-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="d55b1-101">New-AzSignalR</span></span>

## <span data-ttu-id="d55b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d55b1-102">SYNOPSIS</span></span>
<span data-ttu-id="d55b1-103">Crea un servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="d55b1-103">Create a SignalR service.</span></span>

## <span data-ttu-id="d55b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d55b1-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-ServiceMode <String>] [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d55b1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d55b1-105">DESCRIPTION</span></span>
<span data-ttu-id="d55b1-106">Crea un servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="d55b1-106">Create a SignalR service.</span></span>
<span data-ttu-id="d55b1-107">Se non viene specificato, verranno usati i valori seguenti per i parametri:</span><span class="sxs-lookup"><span data-stu-id="d55b1-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="d55b1-108">`ResourceGroupName`: il gruppo di risorse predefinito impostato `Set-AzDefault -ResourceGroupName` da.</span><span class="sxs-lookup"><span data-stu-id="d55b1-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="d55b1-109">`Location`: posizione del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d55b1-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="d55b1-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="d55b1-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="d55b1-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d55b1-111">EXAMPLES</span></span>

### <span data-ttu-id="d55b1-112">Creare un servizio SignalR</span><span class="sxs-lookup"><span data-stu-id="d55b1-112">Create a SignalR service</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="d55b1-113">Specificare ServiceMode e AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="d55b1-113">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -Location eastus -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="d55b1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d55b1-114">PARAMETERS</span></span>

### <span data-ttu-id="d55b1-115">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="d55b1-115">-AllowedOrigin</span></span>
<span data-ttu-id="d55b1-116">Origini consentite per il servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="d55b1-116">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="d55b1-117">Per consentire tutti, usare "\*" e rimuovere tutte le altre origini dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="d55b1-117">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="d55b1-118">Le barre non sono consentite come parte del dominio o dopo TLD</span><span class="sxs-lookup"><span data-stu-id="d55b1-118">Slashes are not allowed as part of domain or after TLD</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d55b1-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d55b1-119">-AsJob</span></span>
<span data-ttu-id="d55b1-120">Eseguire il cmdlet nel processo in background.</span><span class="sxs-lookup"><span data-stu-id="d55b1-120">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="d55b1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d55b1-121">-DefaultProfile</span></span>
<span data-ttu-id="d55b1-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d55b1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d55b1-123">-Location</span><span class="sxs-lookup"><span data-stu-id="d55b1-123">-Location</span></span>
<span data-ttu-id="d55b1-124">Posizione del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="d55b1-124">The SignalR service location.</span></span> <span data-ttu-id="d55b1-125">Se non viene specificato, verrà usata la posizione del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d55b1-125">The resource group location will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d55b1-126">-Name</span><span class="sxs-lookup"><span data-stu-id="d55b1-126">-Name</span></span>
<span data-ttu-id="d55b1-127">Nome del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="d55b1-127">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d55b1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d55b1-128">-ResourceGroupName</span></span>
<span data-ttu-id="d55b1-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d55b1-129">The resource group name.</span></span> <span data-ttu-id="d55b1-130">Se non viene specificato, verrà usato quello predefinito.</span><span class="sxs-lookup"><span data-stu-id="d55b1-130">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d55b1-131">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="d55b1-131">-ServiceMode</span></span>
<span data-ttu-id="d55b1-132">Modalità di servizio per il servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="d55b1-132">The service mode for the SignalR service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d55b1-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="d55b1-133">-Sku</span></span>
<span data-ttu-id="d55b1-134">SKU del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="d55b1-134">The SignalR service SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Standard_S1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d55b1-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="d55b1-135">-Tag</span></span>
<span data-ttu-id="d55b1-136">I tag per il servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="d55b1-136">The tags for the SignalR service.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d55b1-137">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="d55b1-137">-UnitCount</span></span>
<span data-ttu-id="d55b1-138">Il numero di unità di servizio SignalR, da 1 a 10.</span><span class="sxs-lookup"><span data-stu-id="d55b1-138">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="d55b1-139">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="d55b1-139">Default to 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d55b1-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d55b1-140">-Confirm</span></span>
<span data-ttu-id="d55b1-141">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d55b1-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d55b1-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d55b1-142">-WhatIf</span></span>
<span data-ttu-id="d55b1-143">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d55b1-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d55b1-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d55b1-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d55b1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d55b1-145">CommonParameters</span></span>
<span data-ttu-id="d55b1-146">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d55b1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d55b1-147">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d55b1-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d55b1-148">INPUT</span><span class="sxs-lookup"><span data-stu-id="d55b1-148">INPUTS</span></span>

### <span data-ttu-id="d55b1-149">System.String</span><span class="sxs-lookup"><span data-stu-id="d55b1-149">System.String</span></span>

## <span data-ttu-id="d55b1-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d55b1-150">OUTPUTS</span></span>

### <span data-ttu-id="d55b1-151">Microsoft.Azure.Commands.Signalr.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="d55b1-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="d55b1-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="d55b1-152">NOTES</span></span>

## <span data-ttu-id="d55b1-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d55b1-153">RELATED LINKS</span></span>
