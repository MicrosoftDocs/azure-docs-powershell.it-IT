---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/update-aziothubdevicetwin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Update-AzIotHubDeviceTwin.md
ms.openlocfilehash: 16c3ab31959268aa998d50290180d4d8b3231ccf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189847"
---
# <span data-ttu-id="8ee05-101">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="8ee05-101">Update-AzIotHubDeviceTwin</span></span>

## <span data-ttu-id="8ee05-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8ee05-102">SYNOPSIS</span></span>
<span data-ttu-id="8ee05-103">Aggiorna i tag e le proprietà desiderate di un dispositivo Twin.</span><span class="sxs-lookup"><span data-stu-id="8ee05-103">Updates tags and desired properties of a device twin.</span></span>

## <span data-ttu-id="8ee05-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8ee05-104">SYNTAX</span></span>

### <span data-ttu-id="8ee05-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8ee05-105">ResourceSet (Default)</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Tag <Hashtable>] [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ee05-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8ee05-106">InputObjectSet</span></span>
```
Update-AzIotHubDeviceTwin [-InputObject] <PSIotHub> [-DeviceId] <String> [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ee05-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8ee05-107">ResourceIdSet</span></span>
```
Update-AzIotHubDeviceTwin [-ResourceId] <String> [-DeviceId] <String> [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-Partial] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ee05-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ee05-108">DESCRIPTION</span></span>
<span data-ttu-id="8ee05-109">Aggiorna o sostituisce un dispositivo Twin.</span><span class="sxs-lookup"><span data-stu-id="8ee05-109">Updates or replaces a device twin.</span></span> <span data-ttu-id="8ee05-110"> https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twinsPer altre informazioni, vedere.</span><span class="sxs-lookup"><span data-stu-id="8ee05-110">See https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-device-twins for more information.</span></span>

## <span data-ttu-id="8ee05-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8ee05-111">EXAMPLES</span></span>

### <span data-ttu-id="8ee05-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8ee05-112">Example 1</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired -Partial
```

<span data-ttu-id="8ee05-113">Restituisce l'oggetto Twin del dispositivo aggiornato.</span><span class="sxs-lookup"><span data-stu-id="8ee05-113">Returns the updated device twin object.</span></span>

### <span data-ttu-id="8ee05-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8ee05-114">Example 2</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Desired $updatedDesired -Partial
```

<span data-ttu-id="8ee05-115">Restituisce l'oggetto Twin del dispositivo con le proprietà desiderate aggiornate.</span><span class="sxs-lookup"><span data-stu-id="8ee05-115">Returns the device twin object with updated desired properties.</span></span>

### <span data-ttu-id="8ee05-116">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="8ee05-116">Example 3</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Partial
```

<span data-ttu-id="8ee05-117">Restituisce il dispositivo Twin Object con la proprietà Tags aggiornata.</span><span class="sxs-lookup"><span data-stu-id="8ee05-117">Returns the device twin object with updated tags property.</span></span>

### <span data-ttu-id="8ee05-118">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="8ee05-118">Example 4</span></span>
```powershell
PS C:\> Update-AzIotHubDeviceTwin -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Tag $updatedTag -Desired $updatedDesired
```

<span data-ttu-id="8ee05-119">Restituisce l'oggetto Twin del dispositivo sostituito.</span><span class="sxs-lookup"><span data-stu-id="8ee05-119">Returns the replaced device twin object.</span></span>

## <span data-ttu-id="8ee05-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8ee05-120">PARAMETERS</span></span>

### <span data-ttu-id="8ee05-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ee05-121">-DefaultProfile</span></span>
<span data-ttu-id="8ee05-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8ee05-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ee05-123">-Desiderato</span><span class="sxs-lookup"><span data-stu-id="8ee05-123">-Desired</span></span>
<span data-ttu-id="8ee05-124">Aggiungere o aggiornare la proprietà desiderata in un dispositivo Twin.</span><span class="sxs-lookup"><span data-stu-id="8ee05-124">Add or update the desired property in a device twin.</span></span>

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

### <span data-ttu-id="8ee05-125">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="8ee05-125">-DeviceId</span></span>
<span data-ttu-id="8ee05-126">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8ee05-126">Target Device Id.</span></span>

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

### <span data-ttu-id="8ee05-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ee05-127">-InputObject</span></span>
<span data-ttu-id="8ee05-128">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="8ee05-128">IotHub object</span></span>

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

### <span data-ttu-id="8ee05-129">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8ee05-129">-IotHubName</span></span>
<span data-ttu-id="8ee05-130">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="8ee05-130">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8ee05-131">-Parziale</span><span class="sxs-lookup"><span data-stu-id="8ee05-131">-Partial</span></span>
<span data-ttu-id="8ee05-132">Consente di aggiornare solo parzialmente i tag e le proprietà desiderate di un dispositivo Twin.</span><span class="sxs-lookup"><span data-stu-id="8ee05-132">Allows to only partially update the tags and desired properties of a device twin.</span></span>

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

### <span data-ttu-id="8ee05-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ee05-133">-ResourceGroupName</span></span>
<span data-ttu-id="8ee05-134">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8ee05-134">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8ee05-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ee05-135">-ResourceId</span></span>
<span data-ttu-id="8ee05-136">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="8ee05-136">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8ee05-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="8ee05-137">-Tag</span></span>
<span data-ttu-id="8ee05-138">Aggiungere o aggiornare la proprietà Tags in un dispositivo Twin.</span><span class="sxs-lookup"><span data-stu-id="8ee05-138">Add or update the tags property in a device twin.</span></span>

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

### <span data-ttu-id="8ee05-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8ee05-139">-Confirm</span></span>
<span data-ttu-id="8ee05-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ee05-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ee05-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ee05-141">-WhatIf</span></span>
<span data-ttu-id="8ee05-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ee05-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ee05-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8ee05-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ee05-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ee05-144">CommonParameters</span></span>
<span data-ttu-id="8ee05-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ee05-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ee05-146">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ee05-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ee05-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8ee05-147">INPUTS</span></span>

### <span data-ttu-id="8ee05-148">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8ee05-148">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8ee05-149">System. String</span><span class="sxs-lookup"><span data-stu-id="8ee05-149">System.String</span></span>

## <span data-ttu-id="8ee05-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8ee05-150">OUTPUTS</span></span>

### <span data-ttu-id="8ee05-151">System. String</span><span class="sxs-lookup"><span data-stu-id="8ee05-151">System.String</span></span>

## <span data-ttu-id="8ee05-152">Note</span><span class="sxs-lookup"><span data-stu-id="8ee05-152">NOTES</span></span>

## <span data-ttu-id="8ee05-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8ee05-153">RELATED LINKS</span></span>