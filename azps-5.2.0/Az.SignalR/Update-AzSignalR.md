---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: 632f271a085df8384a100392e8ed74ad7b5d0762
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329092"
---
# <span data-ttu-id="14768-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="14768-101">Update-AzSignalR</span></span>

## <span data-ttu-id="14768-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="14768-102">SYNOPSIS</span></span>
<span data-ttu-id="14768-103">Aggiornare un servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="14768-103">Update a SignalR service.</span></span>

## <span data-ttu-id="14768-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14768-104">SYNTAX</span></span>

### <span data-ttu-id="14768-105">ResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="14768-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14768-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14768-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14768-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14768-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14768-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14768-108">DESCRIPTION</span></span>
<span data-ttu-id="14768-109">Aggiornare un servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="14768-109">Update a SignalR service.</span></span>
<span data-ttu-id="14768-110">I valori seguenti verranno usati per i parametri se non sono specificati:</span><span class="sxs-lookup"><span data-stu-id="14768-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="14768-111">`ResourceGroupName`: gruppo di risorse predefinito impostato da `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="14768-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="14768-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="14768-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="14768-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14768-113">EXAMPLES</span></span>

### <span data-ttu-id="14768-114">Aggiornare un servizio di segnalazione specifico.</span><span class="sxs-lookup"><span data-stu-id="14768-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="14768-115">Specificare ServiceMode e AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="14768-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="14768-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="14768-116">PARAMETERS</span></span>

### <span data-ttu-id="14768-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="14768-117">-AllowedOrigin</span></span>
<span data-ttu-id="14768-118">Origini consentite per il servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="14768-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="14768-119">Per consentire a tutti, USA "\*" e Rimuovi tutte le altre origini dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="14768-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="14768-120">Le barre non sono consentite come parte del dominio o dopo il TLD</span><span class="sxs-lookup"><span data-stu-id="14768-120">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="14768-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14768-121">-AsJob</span></span>
<span data-ttu-id="14768-122">Eseguire il cmdlet in un processo in background.</span><span class="sxs-lookup"><span data-stu-id="14768-122">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="14768-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14768-123">-DefaultProfile</span></span>
<span data-ttu-id="14768-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14768-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14768-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14768-125">-InputObject</span></span>
<span data-ttu-id="14768-126">Oggetto risorsa SignalR.</span><span class="sxs-lookup"><span data-stu-id="14768-126">The SignalR resource object.</span></span>

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

### <span data-ttu-id="14768-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="14768-127">-Name</span></span>
<span data-ttu-id="14768-128">Nome del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="14768-128">The SignalR service name.</span></span>

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

### <span data-ttu-id="14768-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14768-129">-ResourceGroupName</span></span>
<span data-ttu-id="14768-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="14768-130">The resource group name.</span></span>
<span data-ttu-id="14768-131">Verrà usato quello predefinito se non specificato.</span><span class="sxs-lookup"><span data-stu-id="14768-131">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="14768-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14768-132">-ResourceId</span></span>
<span data-ttu-id="14768-133">ID risorsa del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="14768-133">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="14768-134">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="14768-134">-ServiceMode</span></span>
<span data-ttu-id="14768-135">Modalità di servizio per il servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="14768-135">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="14768-136">-SKU</span><span class="sxs-lookup"><span data-stu-id="14768-136">-Sku</span></span>
<span data-ttu-id="14768-137">SKU del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="14768-137">The SignalR service SKU.</span></span>
<span data-ttu-id="14768-138">Impostazione predefinita per "Standard_S1".</span><span class="sxs-lookup"><span data-stu-id="14768-138">Default to "Standard_S1".</span></span>

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

### <span data-ttu-id="14768-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="14768-139">-Tag</span></span>
<span data-ttu-id="14768-140">Tag per il servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="14768-140">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="14768-141">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="14768-141">-UnitCount</span></span>
<span data-ttu-id="14768-142">Conteggio unità di servizio del segnalatore, valore solo da {1, 2, 5, 10, 20, 50, 100}.</span><span class="sxs-lookup"><span data-stu-id="14768-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="14768-143">Impostazione predefinita su 1.</span><span class="sxs-lookup"><span data-stu-id="14768-143">Default to 1.</span></span>

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

### <span data-ttu-id="14768-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="14768-144">-Confirm</span></span>
<span data-ttu-id="14768-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14768-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14768-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14768-146">-WhatIf</span></span>
<span data-ttu-id="14768-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14768-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14768-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="14768-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14768-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14768-149">CommonParameters</span></span>
<span data-ttu-id="14768-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14768-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14768-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14768-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14768-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="14768-152">INPUTS</span></span>

### <span data-ttu-id="14768-153">System. String</span><span class="sxs-lookup"><span data-stu-id="14768-153">System.String</span></span>

### <span data-ttu-id="14768-154">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="14768-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="14768-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14768-155">OUTPUTS</span></span>

### <span data-ttu-id="14768-156">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="14768-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="14768-157">Note</span><span class="sxs-lookup"><span data-stu-id="14768-157">NOTES</span></span>

## <span data-ttu-id="14768-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14768-158">RELATED LINKS</span></span>
