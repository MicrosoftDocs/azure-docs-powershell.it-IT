---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeviceChildren.md
ms.openlocfilehash: 8d22b5923b59ef5807419fac4486cd64d5d2b86e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203889"
---
# <span data-ttu-id="266eb-101">Remove-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="266eb-101">Remove-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="266eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="266eb-102">SYNOPSIS</span></span>
<span data-ttu-id="266eb-103">Rimuovere i dispositivi non perimetrali come figli dal dispositivo perimetrale specificato.</span><span class="sxs-lookup"><span data-stu-id="266eb-103">Remove non edge devices as children from specified edge device.</span></span>

## <span data-ttu-id="266eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="266eb-104">SYNTAX</span></span>

### <span data-ttu-id="266eb-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="266eb-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Children <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="266eb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="266eb-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="266eb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="266eb-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId] <String> [-Children <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="266eb-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="266eb-108">DESCRIPTION</span></span>
<span data-ttu-id="266eb-109">Rimuovi tutti i dispositivi non perimetrali o menzionati come dispositivi perimetrali specificati per i bambini.</span><span class="sxs-lookup"><span data-stu-id="266eb-109">Remove all or mentioned non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="266eb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="266eb-110">EXAMPLES</span></span>

### <span data-ttu-id="266eb-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="266eb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Children device1,device2 -Passthru

True
```

<span data-ttu-id="266eb-112">Rimuovi i dispositivi menzionati come figli del dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="266eb-112">Remove mentioned devices as children of specified device.</span></span>

### <span data-ttu-id="266eb-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="266eb-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Passthru

True
```

<span data-ttu-id="266eb-114">Rimuovere tutti i dispositivi non perimetrali come dispositivi perimetrali figlio specificati.</span><span class="sxs-lookup"><span data-stu-id="266eb-114">Remove all non-edge devices as children specified edge device.</span></span>

## <span data-ttu-id="266eb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="266eb-115">PARAMETERS</span></span>

### <span data-ttu-id="266eb-116">-Bambini</span><span class="sxs-lookup"><span data-stu-id="266eb-116">-Children</span></span>
<span data-ttu-id="266eb-117">L'elenco di dispositivi figlio (separati da virgola) include solo i dispositivi non perimetrali.</span><span class="sxs-lookup"><span data-stu-id="266eb-117">Child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="266eb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="266eb-118">-DefaultProfile</span></span>
<span data-ttu-id="266eb-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="266eb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="266eb-120">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="266eb-120">-DeviceId</span></span>
<span data-ttu-id="266eb-121">ID del dispositivo perimetrale.</span><span class="sxs-lookup"><span data-stu-id="266eb-121">Id of edge device.</span></span>

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

### <span data-ttu-id="266eb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="266eb-122">-InputObject</span></span>
<span data-ttu-id="266eb-123">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="266eb-123">IotHub object</span></span>

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

### <span data-ttu-id="266eb-124">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="266eb-124">-IotHubName</span></span>
<span data-ttu-id="266eb-125">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="266eb-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="266eb-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="266eb-126">-PassThru</span></span>
<span data-ttu-id="266eb-127">Consente di restituire l'oggetto booleano.</span><span class="sxs-lookup"><span data-stu-id="266eb-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="266eb-128">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="266eb-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="266eb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="266eb-129">-ResourceGroupName</span></span>
<span data-ttu-id="266eb-130">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="266eb-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="266eb-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="266eb-131">-ResourceId</span></span>
<span data-ttu-id="266eb-132">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="266eb-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="266eb-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="266eb-133">-Confirm</span></span>
<span data-ttu-id="266eb-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="266eb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="266eb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="266eb-135">-WhatIf</span></span>
<span data-ttu-id="266eb-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="266eb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="266eb-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="266eb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="266eb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="266eb-138">CommonParameters</span></span>
<span data-ttu-id="266eb-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="266eb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="266eb-140">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="266eb-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="266eb-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="266eb-141">INPUTS</span></span>

### <span data-ttu-id="266eb-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="266eb-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="266eb-143">System.String</span><span class="sxs-lookup"><span data-stu-id="266eb-143">System.String</span></span>

## <span data-ttu-id="266eb-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="266eb-144">OUTPUTS</span></span>

### <span data-ttu-id="266eb-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="266eb-145">System.Boolean</span></span>

## <span data-ttu-id="266eb-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="266eb-146">NOTES</span></span>

## <span data-ttu-id="266eb-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="266eb-147">RELATED LINKS</span></span>
