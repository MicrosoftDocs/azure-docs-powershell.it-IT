---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: d02db6e59c688a79b0088c3b3b42fde0cbc13bb8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955357"
---
# <span data-ttu-id="ab064-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="ab064-101">Update-AzSignalR</span></span>

## <span data-ttu-id="ab064-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab064-102">SYNOPSIS</span></span>
<span data-ttu-id="ab064-103">Aggiorna un servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="ab064-103">Update a SignalR service.</span></span>

## <span data-ttu-id="ab064-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab064-104">SYNTAX</span></span>

### <span data-ttu-id="ab064-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ab064-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab064-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab064-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab064-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab064-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab064-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ab064-108">DESCRIPTION</span></span>
<span data-ttu-id="ab064-109">Aggiorna un servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="ab064-109">Update a SignalR service.</span></span>
<span data-ttu-id="ab064-110">Se non viene specificato, verranno usati i valori seguenti per i parametri:</span><span class="sxs-lookup"><span data-stu-id="ab064-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="ab064-111">`ResourceGroupName`: il gruppo di risorse predefinito impostato `Set-AzDefault -ResourceGroupName` da.</span><span class="sxs-lookup"><span data-stu-id="ab064-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="ab064-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="ab064-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="ab064-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab064-113">EXAMPLES</span></span>

### <span data-ttu-id="ab064-114">Aggiorna un servizio SignalR specifico.</span><span class="sxs-lookup"><span data-stu-id="ab064-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="ab064-115">Specificare ServiceMode e AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="ab064-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="ab064-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab064-116">PARAMETERS</span></span>

### <span data-ttu-id="ab064-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="ab064-117">-AllowedOrigin</span></span>
<span data-ttu-id="ab064-118">Origini consentite per il servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="ab064-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="ab064-119">Per consentire tutti, usare "\*" e rimuovere tutte le altre origini dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="ab064-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="ab064-120">Le barre non sono consentite come parte del dominio o dopo TLD</span><span class="sxs-lookup"><span data-stu-id="ab064-120">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="ab064-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ab064-121">-AsJob</span></span>
<span data-ttu-id="ab064-122">Eseguire il cmdlet in un processo in background.</span><span class="sxs-lookup"><span data-stu-id="ab064-122">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="ab064-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab064-123">-DefaultProfile</span></span>
<span data-ttu-id="ab064-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ab064-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab064-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab064-125">-InputObject</span></span>
<span data-ttu-id="ab064-126">Oggetto risorsa SignalR.</span><span class="sxs-lookup"><span data-stu-id="ab064-126">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab064-127">-Name</span><span class="sxs-lookup"><span data-stu-id="ab064-127">-Name</span></span>
<span data-ttu-id="ab064-128">Nome del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="ab064-128">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab064-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab064-129">-ResourceGroupName</span></span>
<span data-ttu-id="ab064-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ab064-130">The resource group name.</span></span>
<span data-ttu-id="ab064-131">Se non è specificato, verrà usato quello predefinito.</span><span class="sxs-lookup"><span data-stu-id="ab064-131">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab064-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab064-132">-ResourceId</span></span>
<span data-ttu-id="ab064-133">ID risorsa servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="ab064-133">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab064-134">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="ab064-134">-ServiceMode</span></span>
<span data-ttu-id="ab064-135">Modalità di servizio per il servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="ab064-135">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="ab064-136">-SKU</span><span class="sxs-lookup"><span data-stu-id="ab064-136">-Sku</span></span>
<span data-ttu-id="ab064-137">SKU del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="ab064-137">The SignalR service SKU.</span></span>
<span data-ttu-id="ab064-138">L'impostazione predefinita è "Standard_S1".</span><span class="sxs-lookup"><span data-stu-id="ab064-138">Default to "Standard_S1".</span></span>

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

### <span data-ttu-id="ab064-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="ab064-139">-Tag</span></span>
<span data-ttu-id="ab064-140">I tag per il servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="ab064-140">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="ab064-141">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="ab064-141">-UnitCount</span></span>
<span data-ttu-id="ab064-142">Il numero di unità di servizio SignalR, valore solo da {1, 2, 5, 10, 20, 50, 100}.</span><span class="sxs-lookup"><span data-stu-id="ab064-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="ab064-143">Il valore predefinito è 1.</span><span class="sxs-lookup"><span data-stu-id="ab064-143">Default to 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab064-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab064-144">-Confirm</span></span>
<span data-ttu-id="ab064-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab064-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab064-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab064-146">-WhatIf</span></span>
<span data-ttu-id="ab064-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab064-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab064-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab064-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab064-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab064-149">CommonParameters</span></span>
<span data-ttu-id="ab064-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab064-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab064-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ab064-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab064-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="ab064-152">INPUTS</span></span>

### <span data-ttu-id="ab064-153">System.String</span><span class="sxs-lookup"><span data-stu-id="ab064-153">System.String</span></span>

### <span data-ttu-id="ab064-154">Microsoft.Azure.Commands.Signalr.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="ab064-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="ab064-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab064-155">OUTPUTS</span></span>

### <span data-ttu-id="ab064-156">Microsoft.Azure.Commands.Signalr.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="ab064-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="ab064-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="ab064-157">NOTES</span></span>

## <span data-ttu-id="ab064-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab064-158">RELATED LINKS</span></span>
