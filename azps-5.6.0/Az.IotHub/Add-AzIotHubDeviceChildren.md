---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeviceChildren.md
ms.openlocfilehash: e41030f30e3c5651aca3ddf716af99c919e6e6f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997903"
---
# <span data-ttu-id="2cdfe-101">Add-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="2cdfe-101">Add-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="2cdfe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cdfe-102">SYNOPSIS</span></span>
<span data-ttu-id="2cdfe-103">Aggiungi dispositivi non perimetrali come bambini al dispositivo edge.</span><span class="sxs-lookup"><span data-stu-id="2cdfe-103">Add non-edge devices as a children to the edge device.</span></span>

## <span data-ttu-id="2cdfe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2cdfe-104">SYNTAX</span></span>

### <span data-ttu-id="2cdfe-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2cdfe-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2cdfe-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2cdfe-106">InputObjectSet</span></span>
```
Add-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2cdfe-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2cdfe-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children] <String[]> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2cdfe-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2cdfe-108">DESCRIPTION</span></span>
<span data-ttu-id="2cdfe-109">Aggiungere l'elenco specificato con valori delimitati da virgole degli ID dispositivo non edge come figli del dispositivo perimetrale specificato.</span><span class="sxs-lookup"><span data-stu-id="2cdfe-109">Add specified comma-separated list of non edge device ids as children of specified edge device.</span></span>

## <span data-ttu-id="2cdfe-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2cdfe-110">EXAMPLES</span></span>

### <span data-ttu-id="2cdfe-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2cdfe-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="2cdfe-112">Aggiungi dispositivi non perimetrali come bambini al dispositivo edge.</span><span class="sxs-lookup"><span data-stu-id="2cdfe-112">Add non-edge devices as a children to the edge device.</span></span>

### <span data-ttu-id="2cdfe-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2cdfe-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -Children "device1,device2" -Force

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice2 {device1, device2}
```

<span data-ttu-id="2cdfe-114">Aggiungere dispositivi non perimetrali come figli al dispositivo perimetrale indipendentemente dal fatto che il dispositivo non perimetrale sia già un figlio di un altro dispositivo perimetrale.</span><span class="sxs-lookup"><span data-stu-id="2cdfe-114">Add non-edge devices as a children to the edge device irrespectively the non-edge device is already a child of other edge device.</span></span>

## <span data-ttu-id="2cdfe-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2cdfe-115">PARAMETERS</span></span>

### <span data-ttu-id="2cdfe-116">-Bambini</span><span class="sxs-lookup"><span data-stu-id="2cdfe-116">-Children</span></span>
<span data-ttu-id="2cdfe-117">L'elenco di dispositivi figlio (separati da virgola) include solo i dispositivi non perimetrali.</span><span class="sxs-lookup"><span data-stu-id="2cdfe-117">Child device list (comma separated) includes only non-edge devices.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2cdfe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cdfe-118">-DefaultProfile</span></span>
<span data-ttu-id="2cdfe-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2cdfe-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cdfe-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="2cdfe-120">-DeviceId</span></span>
<span data-ttu-id="2cdfe-121">ID del dispositivo perimetrale.</span><span class="sxs-lookup"><span data-stu-id="2cdfe-121">Id of edge device.</span></span>

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

### <span data-ttu-id="2cdfe-122">-Force</span><span class="sxs-lookup"><span data-stu-id="2cdfe-122">-Force</span></span>
<span data-ttu-id="2cdfe-123">Sovrascrive il dispositivo padre del dispositivo non perimetrale.</span><span class="sxs-lookup"><span data-stu-id="2cdfe-123">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="2cdfe-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2cdfe-124">-InputObject</span></span>
<span data-ttu-id="2cdfe-125">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="2cdfe-125">IotHub object</span></span>

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

### <span data-ttu-id="2cdfe-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="2cdfe-126">-IotHubName</span></span>
<span data-ttu-id="2cdfe-127">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="2cdfe-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="2cdfe-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cdfe-128">-ResourceGroupName</span></span>
<span data-ttu-id="2cdfe-129">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2cdfe-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2cdfe-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2cdfe-130">-ResourceId</span></span>
<span data-ttu-id="2cdfe-131">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="2cdfe-131">IotHub Resource Id</span></span>

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

### <span data-ttu-id="2cdfe-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2cdfe-132">-Confirm</span></span>
<span data-ttu-id="2cdfe-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2cdfe-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cdfe-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cdfe-134">-WhatIf</span></span>
<span data-ttu-id="2cdfe-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2cdfe-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cdfe-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2cdfe-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cdfe-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cdfe-137">CommonParameters</span></span>
<span data-ttu-id="2cdfe-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cdfe-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cdfe-139">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cdfe-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cdfe-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="2cdfe-140">INPUTS</span></span>

### <span data-ttu-id="2cdfe-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2cdfe-141">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2cdfe-142">System.String</span><span class="sxs-lookup"><span data-stu-id="2cdfe-142">System.String</span></span>

## <span data-ttu-id="2cdfe-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2cdfe-143">OUTPUTS</span></span>

### <span data-ttu-id="2cdfe-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice Avi</span><span class="sxs-lookup"><span data-stu-id="2cdfe-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

## <span data-ttu-id="2cdfe-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="2cdfe-145">NOTES</span></span>

## <span data-ttu-id="2cdfe-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2cdfe-146">RELATED LINKS</span></span>
