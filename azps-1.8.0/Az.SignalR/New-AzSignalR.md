---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 8c8240ed1df30dface1bdb2ce0b649bacf17d08a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677051"
---
# <span data-ttu-id="94d1e-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="94d1e-101">New-AzSignalR</span></span>

## <span data-ttu-id="94d1e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="94d1e-102">SYNOPSIS</span></span>
<span data-ttu-id="94d1e-103">Creare un servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="94d1e-103">Create a SignalR service.</span></span>

## <span data-ttu-id="94d1e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94d1e-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94d1e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94d1e-105">DESCRIPTION</span></span>
<span data-ttu-id="94d1e-106">Creare un servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="94d1e-106">Create a SignalR service.</span></span>
<span data-ttu-id="94d1e-107">I valori seguenti verranno usati per i parametri se non sono specificati:</span><span class="sxs-lookup"><span data-stu-id="94d1e-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="94d1e-108">`ResourceGroupName`: gruppo di risorse predefinito impostato da `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="94d1e-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="94d1e-109">`Location`: la posizione del gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="94d1e-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="94d1e-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="94d1e-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="94d1e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94d1e-111">EXAMPLES</span></span>

### <span data-ttu-id="94d1e-112">Creare un serivce di segnalazione</span><span class="sxs-lookup"><span data-stu-id="94d1e-112">Create a SignalR serivce</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0-preview
```

## <span data-ttu-id="94d1e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="94d1e-113">PARAMETERS</span></span>

### <span data-ttu-id="94d1e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94d1e-114">-AsJob</span></span>
<span data-ttu-id="94d1e-115">Eseguire il cmdlet in un processo in background.</span><span class="sxs-lookup"><span data-stu-id="94d1e-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="94d1e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94d1e-116">-DefaultProfile</span></span>
<span data-ttu-id="94d1e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="94d1e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94d1e-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="94d1e-118">-Location</span></span>
<span data-ttu-id="94d1e-119">Posizione del servizio di segnalazione.</span><span class="sxs-lookup"><span data-stu-id="94d1e-119">The SignalR service location.</span></span> <span data-ttu-id="94d1e-120">Il percorso del gruppo di risorse verrà usato se non specificato.</span><span class="sxs-lookup"><span data-stu-id="94d1e-120">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="94d1e-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="94d1e-121">-Name</span></span>
<span data-ttu-id="94d1e-122">Nome del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="94d1e-122">The SignalR service name.</span></span>

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

### <span data-ttu-id="94d1e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94d1e-123">-ResourceGroupName</span></span>
<span data-ttu-id="94d1e-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="94d1e-124">The resource group name.</span></span> <span data-ttu-id="94d1e-125">Verrà usato quello predefinito se non specificato.</span><span class="sxs-lookup"><span data-stu-id="94d1e-125">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="94d1e-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="94d1e-126">-Sku</span></span>
<span data-ttu-id="94d1e-127">SKU del servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="94d1e-127">The SignalR service SKU.</span></span>

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

### <span data-ttu-id="94d1e-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="94d1e-128">-Tag</span></span>
<span data-ttu-id="94d1e-129">Tag per il servizio SignalR.</span><span class="sxs-lookup"><span data-stu-id="94d1e-129">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="94d1e-130">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="94d1e-130">-UnitCount</span></span>
<span data-ttu-id="94d1e-131">Numero di unità di servizio del segnalatore, da 1 a 10.</span><span class="sxs-lookup"><span data-stu-id="94d1e-131">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="94d1e-132">Impostazione predefinita su 1.</span><span class="sxs-lookup"><span data-stu-id="94d1e-132">Default to 1.</span></span>

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

### <span data-ttu-id="94d1e-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="94d1e-133">-Confirm</span></span>
<span data-ttu-id="94d1e-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94d1e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94d1e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94d1e-135">-WhatIf</span></span>
<span data-ttu-id="94d1e-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94d1e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94d1e-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94d1e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94d1e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d1e-138">CommonParameters</span></span>
<span data-ttu-id="94d1e-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94d1e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94d1e-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94d1e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d1e-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="94d1e-141">INPUTS</span></span>

### <span data-ttu-id="94d1e-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="94d1e-142">None</span></span>

## <span data-ttu-id="94d1e-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94d1e-143">OUTPUTS</span></span>

### <span data-ttu-id="94d1e-144">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="94d1e-144">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="94d1e-145">Note</span><span class="sxs-lookup"><span data-stu-id="94d1e-145">NOTES</span></span>

## <span data-ttu-id="94d1e-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94d1e-146">RELATED LINKS</span></span>
