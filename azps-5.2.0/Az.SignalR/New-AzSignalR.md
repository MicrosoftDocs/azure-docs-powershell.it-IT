---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 222a40c101d0491a6d9409a7404e6731d739a2ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323187"
---
# <span data-ttu-id="17bda-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="17bda-101">New-AzSignalR</span></span>

## <span data-ttu-id="17bda-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="17bda-102">SYNOPSIS</span></span>
<span data-ttu-id="17bda-103">Creare un servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="17bda-103">Create a SignalR service.</span></span>

## <span data-ttu-id="17bda-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="17bda-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-ServiceMode <String>] [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17bda-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="17bda-105">DESCRIPTION</span></span>
<span data-ttu-id="17bda-106">Creare un servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="17bda-106">Create a SignalR service.</span></span>
<span data-ttu-id="17bda-107">I valori seguenti verranno usati per i parametri se non sono specificati:</span><span class="sxs-lookup"><span data-stu-id="17bda-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="17bda-108">`ResourceGroupName`: gruppo di risorse predefinito impostato da `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="17bda-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="17bda-109">`Location`: la posizione del gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="17bda-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="17bda-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="17bda-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="17bda-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="17bda-111">EXAMPLES</span></span>

### <span data-ttu-id="17bda-112">Creare un servizio di segnalazione</span><span class="sxs-lookup"><span data-stu-id="17bda-112">Create a SignalR service</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="17bda-113">Specificare ServiceMode e AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="17bda-113">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -Location eastus -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="17bda-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="17bda-114">PARAMETERS</span></span>

### <span data-ttu-id="17bda-115">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="17bda-115">-AllowedOrigin</span></span>
<span data-ttu-id="17bda-116">Origini consentite per il servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="17bda-116">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="17bda-117">Per consentire a tutti, USA "\*" e Rimuovi tutte le altre origini dall'elenco.</span><span class="sxs-lookup"><span data-stu-id="17bda-117">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="17bda-118">Le barre non sono consentite come parte del dominio o dopo il TLD</span><span class="sxs-lookup"><span data-stu-id="17bda-118">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="17bda-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="17bda-119">-AsJob</span></span>
<span data-ttu-id="17bda-120">Eseguire il cmdlet in un processo in background.</span><span class="sxs-lookup"><span data-stu-id="17bda-120">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="17bda-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17bda-121">-DefaultProfile</span></span>
<span data-ttu-id="17bda-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="17bda-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17bda-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="17bda-123">-Location</span></span>
<span data-ttu-id="17bda-124">Posizione del servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="17bda-124">The SignalR service location.</span></span> <span data-ttu-id="17bda-125">Il percorso del gruppo di risorse verrà usato se non specificato.</span><span class="sxs-lookup"><span data-stu-id="17bda-125">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="17bda-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="17bda-126">-Name</span></span>
<span data-ttu-id="17bda-127">Nome del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="17bda-127">The SignalR service name.</span></span>

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

### <span data-ttu-id="17bda-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17bda-128">-ResourceGroupName</span></span>
<span data-ttu-id="17bda-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="17bda-129">The resource group name.</span></span> <span data-ttu-id="17bda-130">Verrà usato quello predefinito se non specificato.</span><span class="sxs-lookup"><span data-stu-id="17bda-130">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="17bda-131">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="17bda-131">-ServiceMode</span></span>
<span data-ttu-id="17bda-132">Modalità di servizio per il servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="17bda-132">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="17bda-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="17bda-133">-Sku</span></span>
<span data-ttu-id="17bda-134">SKU del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="17bda-134">The SignalR service SKU.</span></span>

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

### <span data-ttu-id="17bda-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="17bda-135">-Tag</span></span>
<span data-ttu-id="17bda-136">Tag per il servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="17bda-136">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="17bda-137">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="17bda-137">-UnitCount</span></span>
<span data-ttu-id="17bda-138">Numero di unità di servizio del segnalatore, da 1 a 10.</span><span class="sxs-lookup"><span data-stu-id="17bda-138">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="17bda-139">Impostazione predefinita su 1.</span><span class="sxs-lookup"><span data-stu-id="17bda-139">Default to 1.</span></span>

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

### <span data-ttu-id="17bda-140">-Confermare</span><span class="sxs-lookup"><span data-stu-id="17bda-140">-Confirm</span></span>
<span data-ttu-id="17bda-141">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17bda-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17bda-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17bda-142">-WhatIf</span></span>
<span data-ttu-id="17bda-143">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="17bda-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17bda-144">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="17bda-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17bda-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17bda-145">CommonParameters</span></span>
<span data-ttu-id="17bda-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17bda-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17bda-147">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="17bda-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17bda-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="17bda-148">INPUTS</span></span>

### <span data-ttu-id="17bda-149">System. String</span><span class="sxs-lookup"><span data-stu-id="17bda-149">System.String</span></span>

## <span data-ttu-id="17bda-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="17bda-150">OUTPUTS</span></span>

### <span data-ttu-id="17bda-151">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="17bda-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="17bda-152">Note</span><span class="sxs-lookup"><span data-stu-id="17bda-152">NOTES</span></span>

## <span data-ttu-id="17bda-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="17bda-153">RELATED LINKS</span></span>
