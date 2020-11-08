---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubModule.md
ms.openlocfilehash: 3362fd6b1e60fa975277c97ea76a8e8c15ee29a4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201196"
---
# <span data-ttu-id="7fd34-101">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="7fd34-101">Remove-AzIotHubModule</span></span>

## <span data-ttu-id="7fd34-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7fd34-102">SYNOPSIS</span></span>
<span data-ttu-id="7fd34-103">Eliminare moduli in un dispositivo con un sacco di destinazione in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="7fd34-103">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="7fd34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7fd34-104">SYNTAX</span></span>

### <span data-ttu-id="7fd34-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7fd34-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fd34-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7fd34-106">InputObjectSet</span></span>
```
Remove-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fd34-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7fd34-107">ResourceIdSet</span></span>
```
Remove-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fd34-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7fd34-108">DESCRIPTION</span></span>
<span data-ttu-id="7fd34-109">Eliminare moduli in un dispositivo con un sacco di destinazione in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="7fd34-109">Delete module(s) on a target IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="7fd34-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7fd34-110">EXAMPLES</span></span>

### <span data-ttu-id="7fd34-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7fd34-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -PassThru

True
```

<span data-ttu-id="7fd34-112">Eliminare un modulo dispositivo di un sacco.</span><span class="sxs-lookup"><span data-stu-id="7fd34-112">Delete an Iot device module.</span></span>

### <span data-ttu-id="7fd34-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7fd34-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -PassThru

True
```

<span data-ttu-id="7fd34-114">Eliminare tutti i moduli di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7fd34-114">Delete all Iot device modules.</span></span>

## <span data-ttu-id="7fd34-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7fd34-115">PARAMETERS</span></span>

### <span data-ttu-id="7fd34-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fd34-116">-DefaultProfile</span></span>
<span data-ttu-id="7fd34-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7fd34-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fd34-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="7fd34-118">-DeviceId</span></span>
<span data-ttu-id="7fd34-119">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7fd34-119">Target Device Id.</span></span>

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

### <span data-ttu-id="7fd34-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fd34-120">-InputObject</span></span>
<span data-ttu-id="7fd34-121">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="7fd34-121">IotHub object</span></span>

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

### <span data-ttu-id="7fd34-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7fd34-122">-IotHubName</span></span>
<span data-ttu-id="7fd34-123">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="7fd34-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7fd34-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="7fd34-124">-ModuleId</span></span>
<span data-ttu-id="7fd34-125">ID modulo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7fd34-125">Target Module Id.</span></span>

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

### <span data-ttu-id="7fd34-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7fd34-126">-PassThru</span></span>
<span data-ttu-id="7fd34-127">Consente di restituire l'oggetto Boolean.</span><span class="sxs-lookup"><span data-stu-id="7fd34-127">Allows to return the boolean object.</span></span>
<span data-ttu-id="7fd34-128">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="7fd34-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7fd34-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fd34-129">-ResourceGroupName</span></span>
<span data-ttu-id="7fd34-130">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="7fd34-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7fd34-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fd34-131">-ResourceId</span></span>
<span data-ttu-id="7fd34-132">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="7fd34-132">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7fd34-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7fd34-133">-Confirm</span></span>
<span data-ttu-id="7fd34-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fd34-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fd34-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fd34-135">-WhatIf</span></span>
<span data-ttu-id="7fd34-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7fd34-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fd34-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7fd34-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fd34-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fd34-138">CommonParameters</span></span>
<span data-ttu-id="7fd34-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fd34-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fd34-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fd34-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fd34-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7fd34-141">INPUTS</span></span>

### <span data-ttu-id="7fd34-142">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7fd34-142">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7fd34-143">System. String</span><span class="sxs-lookup"><span data-stu-id="7fd34-143">System.String</span></span>

## <span data-ttu-id="7fd34-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7fd34-144">OUTPUTS</span></span>

### <span data-ttu-id="7fd34-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7fd34-145">System.Boolean</span></span>

## <span data-ttu-id="7fd34-146">Note</span><span class="sxs-lookup"><span data-stu-id="7fd34-146">NOTES</span></span>

## <span data-ttu-id="7fd34-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7fd34-147">RELATED LINKS</span></span>
