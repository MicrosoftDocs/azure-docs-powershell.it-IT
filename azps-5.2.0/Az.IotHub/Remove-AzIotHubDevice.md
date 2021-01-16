---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDevice.md
ms.openlocfilehash: 3d137f93c32b77afd29a833086ff5c55823bc104
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335656"
---
# <span data-ttu-id="9ab34-101">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="9ab34-101">Remove-AzIotHubDevice</span></span>

## <span data-ttu-id="9ab34-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9ab34-102">SYNOPSIS</span></span>
<span data-ttu-id="9ab34-103">Eliminare un dispositivo hub molto.</span><span class="sxs-lookup"><span data-stu-id="9ab34-103">Delete an IoT Hub device.</span></span>

## <span data-ttu-id="9ab34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9ab34-104">SYNTAX</span></span>

### <span data-ttu-id="9ab34-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9ab34-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ab34-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9ab34-106">InputObjectSet</span></span>
```
Remove-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ab34-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9ab34-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ab34-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9ab34-108">DESCRIPTION</span></span>
<span data-ttu-id="9ab34-109">Eliminare tutti i dispositivi o un dispositivo specifico da un hub molto.</span><span class="sxs-lookup"><span data-stu-id="9ab34-109">Delete all devices or a specific device from an Iot Hub.</span></span>

## <span data-ttu-id="9ab34-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9ab34-110">EXAMPLES</span></span>

### <span data-ttu-id="9ab34-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9ab34-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"
```

<span data-ttu-id="9ab34-112">Eliminare tutti i dispositivi hub.</span><span class="sxs-lookup"><span data-stu-id="9ab34-112">Delete all Iot Hub devices.</span></span>

### <span data-ttu-id="9ab34-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9ab34-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="9ab34-114">Eliminare un dispositivo hub molto.</span><span class="sxs-lookup"><span data-stu-id="9ab34-114">Delete an Iot Hub device.</span></span>

## <span data-ttu-id="9ab34-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9ab34-115">PARAMETERS</span></span>

### <span data-ttu-id="9ab34-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ab34-116">-DefaultProfile</span></span>
<span data-ttu-id="9ab34-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9ab34-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ab34-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="9ab34-118">-DeviceId</span></span>
<span data-ttu-id="9ab34-119">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9ab34-119">Target Device Id.</span></span>

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

### <span data-ttu-id="9ab34-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9ab34-120">-InputObject</span></span>
<span data-ttu-id="9ab34-121">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="9ab34-121">IotHub object</span></span>

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

### <span data-ttu-id="9ab34-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="9ab34-122">-IotHubName</span></span>
<span data-ttu-id="9ab34-123">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="9ab34-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="9ab34-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ab34-124">-PassThru</span></span>
<span data-ttu-id="9ab34-125">Consente di restituire l'oggetto Boolean.</span><span class="sxs-lookup"><span data-stu-id="9ab34-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="9ab34-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="9ab34-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9ab34-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ab34-127">-ResourceGroupName</span></span>
<span data-ttu-id="9ab34-128">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="9ab34-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9ab34-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ab34-129">-ResourceId</span></span>
<span data-ttu-id="9ab34-130">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="9ab34-130">IotHub Resource Id</span></span>

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

### <span data-ttu-id="9ab34-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9ab34-131">-Confirm</span></span>
<span data-ttu-id="9ab34-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ab34-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ab34-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ab34-133">-WhatIf</span></span>
<span data-ttu-id="9ab34-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9ab34-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ab34-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9ab34-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ab34-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ab34-136">CommonParameters</span></span>
<span data-ttu-id="9ab34-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ab34-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ab34-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ab34-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ab34-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9ab34-139">INPUTS</span></span>

### <span data-ttu-id="9ab34-140">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="9ab34-140">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="9ab34-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9ab34-141">System.String</span></span>

## <span data-ttu-id="9ab34-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9ab34-142">OUTPUTS</span></span>

### <span data-ttu-id="9ab34-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9ab34-143">System.Boolean</span></span>

## <span data-ttu-id="9ab34-144">Note</span><span class="sxs-lookup"><span data-stu-id="9ab34-144">NOTES</span></span>

## <span data-ttu-id="9ab34-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9ab34-145">RELATED LINKS</span></span>
