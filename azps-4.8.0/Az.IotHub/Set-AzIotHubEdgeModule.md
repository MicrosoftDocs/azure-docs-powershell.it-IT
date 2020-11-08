---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubedgemodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubEdgeModule.md
ms.openlocfilehash: 5316b6bae6bfc64f791959bb6e236c861833ed4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94033063"
---
# <span data-ttu-id="59b46-101">Set-AzIotHubEdgeModule</span><span class="sxs-lookup"><span data-stu-id="59b46-101">Set-AzIotHubEdgeModule</span></span>

## <span data-ttu-id="59b46-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59b46-102">SYNOPSIS</span></span>
<span data-ttu-id="59b46-103">Impostare i moduli perimetrali in un singolo dispositivo Edge.</span><span class="sxs-lookup"><span data-stu-id="59b46-103">Set edge modules on a single edge device.</span></span>

## <span data-ttu-id="59b46-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59b46-104">SYNTAX</span></span>

### <span data-ttu-id="59b46-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="59b46-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubEdgeModule [-ResourceGroupName] <String> [-IotHubName] <String> -DeviceId <String>
 -ModulesContent <Hashtable> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59b46-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="59b46-106">InputObjectSet</span></span>
```
Set-AzIotHubEdgeModule [-InputObject] <PSIotHub> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59b46-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="59b46-107">ResourceIdSet</span></span>
```
Set-AzIotHubEdgeModule [-ResourceId] <String> -DeviceId <String> -ModulesContent <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59b46-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59b46-108">DESCRIPTION</span></span>
<span data-ttu-id="59b46-109">Applica il contenuto della configurazione dei moduli forniti al dispositivo Edge specificato.</span><span class="sxs-lookup"><span data-stu-id="59b46-109">Applies the provided modules configuration content to the specified edge device.</span></span>
<span data-ttu-id="59b46-110">Nota: dopo l'esecuzione, il comando emetterà la raccolta di moduli applicati al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="59b46-110">Note: Upon execution the command will output the collection of modules applied to the device.</span></span>

## <span data-ttu-id="59b46-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59b46-111">EXAMPLES</span></span>

### <span data-ttu-id="59b46-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="59b46-112">Example 1</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Set-AzIotHubEdgeModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myEdgeDevice1" -ModulesContent $content
```

<span data-ttu-id="59b46-113">Testare i moduli Edge durante lo sviluppo impostando i moduli in un dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="59b46-113">Test edge modules while in development by setting modules on a target device.</span></span>

## <span data-ttu-id="59b46-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59b46-114">PARAMETERS</span></span>

### <span data-ttu-id="59b46-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59b46-115">-DefaultProfile</span></span>
<span data-ttu-id="59b46-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="59b46-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59b46-117">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="59b46-117">-DeviceId</span></span>
<span data-ttu-id="59b46-118">ID dispositivo Edge di destinazione.</span><span class="sxs-lookup"><span data-stu-id="59b46-118">Target Edge Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b46-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59b46-119">-InputObject</span></span>
<span data-ttu-id="59b46-120">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="59b46-120">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59b46-121">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="59b46-121">-IotHubName</span></span>
<span data-ttu-id="59b46-122">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="59b46-122">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b46-123">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="59b46-123">-ModulesContent</span></span>
<span data-ttu-id="59b46-124">Contenuto di configurazione dei moduli per i dispositivi Edge molto.</span><span class="sxs-lookup"><span data-stu-id="59b46-124">Configuration content of modules for IoT Edge devices.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b46-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59b46-125">-ResourceGroupName</span></span>
<span data-ttu-id="59b46-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="59b46-126">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59b46-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59b46-127">-ResourceId</span></span>
<span data-ttu-id="59b46-128">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="59b46-128">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59b46-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="59b46-129">-Confirm</span></span>
<span data-ttu-id="59b46-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59b46-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59b46-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59b46-131">-WhatIf</span></span>
<span data-ttu-id="59b46-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59b46-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59b46-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59b46-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59b46-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59b46-134">CommonParameters</span></span>
<span data-ttu-id="59b46-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59b46-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59b46-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59b46-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59b46-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59b46-137">INPUTS</span></span>

### <span data-ttu-id="59b46-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="59b46-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="59b46-139">System. String</span><span class="sxs-lookup"><span data-stu-id="59b46-139">System.String</span></span>

## <span data-ttu-id="59b46-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59b46-140">OUTPUTS</span></span>

### <span data-ttu-id="59b46-141">Microsoft. Azure. Commands. Management. IotHub. Models. PSModules []</span><span class="sxs-lookup"><span data-stu-id="59b46-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="59b46-142">Note</span><span class="sxs-lookup"><span data-stu-id="59b46-142">NOTES</span></span>

## <span data-ttu-id="59b46-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59b46-143">RELATED LINKS</span></span>
