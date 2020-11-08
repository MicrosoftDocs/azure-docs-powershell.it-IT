---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
ms.openlocfilehash: 8d22b5923b59ef5807419fac4486cd64d5d2b86e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193284"
---
# <span data-ttu-id="b784e-101">Remove-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="b784e-101">Remove-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="b784e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b784e-102">SYNOPSIS</span></span>
<span data-ttu-id="b784e-103">Rimuovere i dispositivi non Edge come elementi figlio dal dispositivo Edge specificato.</span><span class="sxs-lookup"><span data-stu-id="b784e-103">Remove non edge devices as children from specified edge device.</span></span>

## <span data-ttu-id="b784e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b784e-104">SYNTAX</span></span>

### <span data-ttu-id="b784e-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b784e-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b784e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b784e-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b784e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b784e-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b784e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b784e-108">DESCRIPTION</span></span>
<span data-ttu-id="b784e-109">Rimuovere tutti i dispositivi non-Edge menzionati come elementi figlio specificati in Edge Device.</span><span class="sxs-lookup"><span data-stu-id="b784e-109">Remove all or mentioned non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="b784e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b784e-110">EXAMPLES</span></span>

### <span data-ttu-id="b784e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b784e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2 -Passthru

True
```

<span data-ttu-id="b784e-112">Rimuovere i dispositivi menzionati come elementi figlio del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="b784e-112">Remove mentioned devices as children of specified device.</span></span>

### <span data-ttu-id="b784e-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b784e-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Passthru

True
```

<span data-ttu-id="b784e-114">Rimuovere tutti i dispositivi non-Edge come elementi figlio del dispositivo Edge specificato.</span><span class="sxs-lookup"><span data-stu-id="b784e-114">Remove all non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="b784e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b784e-115">PARAMETERS</span></span>

### <span data-ttu-id="b784e-116">-Bambini</span><span class="sxs-lookup"><span data-stu-id="b784e-116">-Children</span></span>
<span data-ttu-id="b784e-117">L'elenco dei dispositivi secondari (separati da virgole) include solo dispositivi non-Edge.</span><span class="sxs-lookup"><span data-stu-id="b784e-117">Child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="b784e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b784e-118">-DefaultProfile</span></span>
<span data-ttu-id="b784e-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b784e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b784e-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="b784e-120">-DeviceId</span></span>
<span data-ttu-id="b784e-121">ID del dispositivo Edge.</span><span class="sxs-lookup"><span data-stu-id="b784e-121">Id of edge device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b784e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b784e-122">-InputObject</span></span>
<span data-ttu-id="b784e-123">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="b784e-123">IotHub object</span></span>

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

### <span data-ttu-id="b784e-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b784e-124">-IotHubName</span></span>
<span data-ttu-id="b784e-125">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="b784e-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b784e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b784e-126">-PassThru</span></span>
<span data-ttu-id="b784e-127">Consente di restituire l'oggetto Boolean.</span><span class="sxs-lookup"><span data-stu-id="b784e-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="b784e-128">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b784e-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b784e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b784e-129">-ResourceGroupName</span></span>
<span data-ttu-id="b784e-130">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b784e-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b784e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b784e-131">-ResourceId</span></span>
<span data-ttu-id="b784e-132">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="b784e-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b784e-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b784e-133">-Confirm</span></span>
<span data-ttu-id="b784e-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b784e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b784e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b784e-135">-WhatIf</span></span>
<span data-ttu-id="b784e-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b784e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b784e-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b784e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b784e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b784e-138">CommonParameters</span></span>
<span data-ttu-id="b784e-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b784e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b784e-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b784e-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b784e-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b784e-141">INPUTS</span></span>

### <span data-ttu-id="b784e-142">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b784e-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b784e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="b784e-143">System.String</span></span>

## <span data-ttu-id="b784e-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b784e-144">OUTPUTS</span></span>

### <span data-ttu-id="b784e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b784e-145">System.Boolean</span></span>

## <span data-ttu-id="b784e-146">Note</span><span class="sxs-lookup"><span data-stu-id="b784e-146">NOTES</span></span>

## <span data-ttu-id="b784e-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b784e-147">RELATED LINKS</span></span>
