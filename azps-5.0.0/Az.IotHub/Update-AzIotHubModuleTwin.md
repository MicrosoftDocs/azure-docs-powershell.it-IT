---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubmoduletwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubModuleTwin.md
ms.openlocfilehash: fb2b984453f87422d7a5b9ec5d5178ca6b6c55d5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296893"
---
# <span data-ttu-id="a0d5e-101">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="a0d5e-101">Update-AzIotHubModuleTwin</span></span>

## <span data-ttu-id="a0d5e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0d5e-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d5e-103">Aggiorna i tag e le proprietà desiderate di un modulo per dispositivi molto Twin.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-103">Updates tags and desired properties of an IoT device module twin.</span></span>

## <span data-ttu-id="a0d5e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0d5e-104">SYNTAX</span></span>

### <span data-ttu-id="a0d5e-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a0d5e-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubModuleTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 -ModuleId <String> [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0d5e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a0d5e-106">InputObjectSet</span></span>
```
Update-AzIotHubModuleTwin [-InputObject] <PSIotHub> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a0d5e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a0d5e-107">ResourceIdSet</span></span>
```
Update-AzIotHubModuleTwin [-ResourceId] <String> [-DeviceId] <String> -ModuleId <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a0d5e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0d5e-108">DESCRIPTION</span></span>
<span data-ttu-id="a0d5e-109">Aggiorna o sostituisce un dispositivo Twin.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="a0d5e-110"> https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twinsPer altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-110">See https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-devguide-module-twins for more information.</span></span>

## <span data-ttu-id="a0d5e-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0d5e-111">EXAMPLES</span></span>

### <span data-ttu-id="a0d5e-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a0d5e-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="a0d5e-113">Restituisce l'oggetto Twin del modulo di dispositivo aggiornato.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-113">Returns the updated device module twin object.</span></span>

### <span data-ttu-id="a0d5e-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a0d5e-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="a0d5e-115">Restituisce l'oggetto Twin del modulo di dispositivo con le proprietà desiderate aggiornate.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-115">Returns the device module twin object with updated desired properties.</span></span>

### <span data-ttu-id="a0d5e-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a0d5e-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Partial
```

<span data-ttu-id="a0d5e-117">Restituisce l'oggetto Twin Device module con la proprietà Tags aggiornata.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-117">Returns the device module twin object with updated tags property.</span></span>

### <span data-ttu-id="a0d5e-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="a0d5e-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubModuleTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="a0d5e-119">Restituisce l'oggetto Twin Device module sostituito.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-119">Returns the replaced device module twin object.</span></span>

## <span data-ttu-id="a0d5e-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0d5e-120">PARAMETERS</span></span>

### <span data-ttu-id="a0d5e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0d5e-121">-DefaultProfile</span></span>
<span data-ttu-id="a0d5e-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0d5e-123">-Desiderato</span><span class="sxs-lookup"><span data-stu-id="a0d5e-123">-Desired</span></span>
<span data-ttu-id="a0d5e-124">Aggiungere o aggiornare la proprietà desiderata in un modulo Twin.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-124">Add or update the desired property in a module twin.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d5e-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="a0d5e-125">-DeviceId</span></span>
<span data-ttu-id="a0d5e-126">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-126">Target Device Id.</span></span>

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

### <span data-ttu-id="a0d5e-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a0d5e-127">-InputObject</span></span>
<span data-ttu-id="a0d5e-128">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="a0d5e-128">IotHub object</span></span>

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

### <span data-ttu-id="a0d5e-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a0d5e-129">-IotHubName</span></span>
<span data-ttu-id="a0d5e-130">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="a0d5e-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a0d5e-131">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="a0d5e-131">-ModuleId</span></span>
<span data-ttu-id="a0d5e-132">ID modulo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-132">Target Module Id.</span></span>

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

### <span data-ttu-id="a0d5e-133">-Parziale</span><span class="sxs-lookup"><span data-stu-id="a0d5e-133">-Partial</span></span>
<span data-ttu-id="a0d5e-134">Consente di aggiornare solo parzialmente i tag e le proprietà desiderate di un modulo Twin.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-134">Allows to only partially update the tags and desired properties of a module twin.</span></span>

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

### <span data-ttu-id="a0d5e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0d5e-135">-ResourceGroupName</span></span>
<span data-ttu-id="a0d5e-136">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a0d5e-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a0d5e-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0d5e-137">-ResourceId</span></span>
<span data-ttu-id="a0d5e-138">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="a0d5e-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a0d5e-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0d5e-139">-Tag</span></span>
<span data-ttu-id="a0d5e-140">Aggiungere o aggiornare la proprietà Tags in un modulo Twin.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-140">Add or update the tags property in a module twin.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d5e-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a0d5e-141">-Confirm</span></span>
<span data-ttu-id="a0d5e-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0d5e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0d5e-143">-WhatIf</span></span>
<span data-ttu-id="a0d5e-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0d5e-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0d5e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d5e-146">CommonParameters</span></span>
<span data-ttu-id="a0d5e-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0d5e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d5e-148">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0d5e-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d5e-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0d5e-149">INPUTS</span></span>

### <span data-ttu-id="a0d5e-150">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a0d5e-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a0d5e-151">System. String</span><span class="sxs-lookup"><span data-stu-id="a0d5e-151">System.String</span></span>

## <span data-ttu-id="a0d5e-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0d5e-152">OUTPUTS</span></span>

### <span data-ttu-id="a0d5e-153">Microsoft. Azure. Commands. Management. IotHub. Models. PSModuleTwin</span><span class="sxs-lookup"><span data-stu-id="a0d5e-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSModuleTwin</span></span>

## <span data-ttu-id="a0d5e-154">Note</span><span class="sxs-lookup"><span data-stu-id="a0d5e-154">NOTES</span></span>

## <span data-ttu-id="a0d5e-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0d5e-155">RELATED LINKS</span></span>
