---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
ms.openlocfilehash: 0f2e7cd2abc61cde9f060eaabf6634385b6ec258
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997917"
---
# <span data-ttu-id="35567-101">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="35567-101">Add-AzIotHubDevice</span></span>

## <span data-ttu-id="35567-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35567-102">SYNOPSIS</span></span>
<span data-ttu-id="35567-103">Creare un dispositivo in un hub IoT.</span><span class="sxs-lookup"><span data-stu-id="35567-103">Create a device in an IoT Hub.</span></span>

## <span data-ttu-id="35567-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35567-104">SYNTAX</span></span>

### <span data-ttu-id="35567-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="35567-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled]
 [-Children <String[]>] [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35567-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="35567-106">InputObjectSet</span></span>
```
Add-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="35567-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="35567-107">ResourceIdSet</span></span>
```
Add-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="35567-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="35567-108">DESCRIPTION</span></span>
<span data-ttu-id="35567-109">Creare un dispositivo con un tipo di autorizzazione diverso in un Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="35567-109">Create a device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="35567-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35567-110">EXAMPLES</span></span>

### <span data-ttu-id="35567-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="35567-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled
```

<span data-ttu-id="35567-112">Creare un dispositivo IoT abilitato per edge con l'autorizzazione predefinita (chiave privata condivisa).</span><span class="sxs-lookup"><span data-stu-id="35567-112">Create an edge enabled IoT device with default authorization (shared private key).</span></span>

### <span data-ttu-id="35567-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="35567-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -AuthMethod "x509_ca" -Status Disabled -StatusReason "Some Reason"
```

<span data-ttu-id="35567-114">Creare un dispositivo IoT con autorizzazione CA radice con stato e motivo disabilitati.</span><span class="sxs-lookup"><span data-stu-id="35567-114">Create an IoT device with root CA authorization with disabled status and reason.</span></span>

### <span data-ttu-id="35567-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="35567-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled -Children device1,device2
```

<span data-ttu-id="35567-116">Creare un dispositivo IoT abilitato per Edge e aggiungerne i dispositivi figlio.</span><span class="sxs-lookup"><span data-stu-id="35567-116">Create an edge enabled IoT device and add child devices to it.</span></span>

### <span data-ttu-id="35567-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="35567-117">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -ParentDeviceId parentDevice1
```

<span data-ttu-id="35567-118">Creare un dispositivo IoT e impostarne il dispositivo padre.</span><span class="sxs-lookup"><span data-stu-id="35567-118">Create an IoT device and set its parent device.</span></span>

## <span data-ttu-id="35567-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35567-119">PARAMETERS</span></span>

### <span data-ttu-id="35567-120">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="35567-120">-AuthMethod</span></span>
<span data-ttu-id="35567-121">Tipo di autorizzazione con cui deve essere creata un'entità.</span><span class="sxs-lookup"><span data-stu-id="35567-121">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: (All)
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35567-122">-Bambini</span><span class="sxs-lookup"><span data-stu-id="35567-122">-Children</span></span>
<span data-ttu-id="35567-123">L'elenco di dispositivi secondari (separati da virgola) include solo i dispositivi non perimetrali.</span><span class="sxs-lookup"><span data-stu-id="35567-123">Add child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="35567-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35567-124">-DefaultProfile</span></span>
<span data-ttu-id="35567-125">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35567-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35567-126">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="35567-126">-DeviceId</span></span>
<span data-ttu-id="35567-127">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="35567-127">Target Device Id.</span></span>

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

### <span data-ttu-id="35567-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="35567-128">-EdgeEnabled</span></span>
<span data-ttu-id="35567-129">Flag che indica l'abilitazione del bordo.</span><span class="sxs-lookup"><span data-stu-id="35567-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="35567-130">-Force</span><span class="sxs-lookup"><span data-stu-id="35567-130">-Force</span></span>
<span data-ttu-id="35567-131">Sovrascrive il dispositivo padre del dispositivo non perimetrale.</span><span class="sxs-lookup"><span data-stu-id="35567-131">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="35567-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35567-132">-InputObject</span></span>
<span data-ttu-id="35567-133">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="35567-133">IotHub object</span></span>

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

### <span data-ttu-id="35567-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="35567-134">-IotHubName</span></span>
<span data-ttu-id="35567-135">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="35567-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="35567-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="35567-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="35567-137">Thumbprint del certificato autofirmato esplicito da usare per la chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="35567-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="35567-138">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="35567-138">-ParentDeviceId</span></span>
<span data-ttu-id="35567-139">ID del dispositivo perimetrale.</span><span class="sxs-lookup"><span data-stu-id="35567-139">Id of edge device.</span></span>

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

### <span data-ttu-id="35567-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35567-140">-ResourceGroupName</span></span>
<span data-ttu-id="35567-141">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="35567-141">Name of the Resource Group</span></span>

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

### <span data-ttu-id="35567-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35567-142">-ResourceId</span></span>
<span data-ttu-id="35567-143">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="35567-143">IotHub Resource Id</span></span>

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

### <span data-ttu-id="35567-144">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="35567-144">-SecondaryThumbprint</span></span>
<span data-ttu-id="35567-145">Thumbprint del certificato autofirmato esplicito da usare per la chiave secondaria.</span><span class="sxs-lookup"><span data-stu-id="35567-145">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="35567-146">-Stato</span><span class="sxs-lookup"><span data-stu-id="35567-146">-Status</span></span>
<span data-ttu-id="35567-147">Imposta lo stato del dispositivo al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="35567-147">Set device status upon creation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35567-148">-Status S.p.A.P.:</span><span class="sxs-lookup"><span data-stu-id="35567-148">-StatusReason</span></span>
<span data-ttu-id="35567-149">Descrizione dello stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="35567-149">Description for device status.</span></span>

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

### <span data-ttu-id="35567-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35567-150">-Confirm</span></span>
<span data-ttu-id="35567-151">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35567-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35567-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35567-152">-WhatIf</span></span>
<span data-ttu-id="35567-153">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35567-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35567-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35567-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35567-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35567-155">CommonParameters</span></span>
<span data-ttu-id="35567-156">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35567-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35567-157">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35567-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35567-158">INPUT</span><span class="sxs-lookup"><span data-stu-id="35567-158">INPUTS</span></span>

### <span data-ttu-id="35567-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="35567-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="35567-160">System.String</span><span class="sxs-lookup"><span data-stu-id="35567-160">System.String</span></span>

## <span data-ttu-id="35567-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35567-161">OUTPUTS</span></span>

### <span data-ttu-id="35567-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevaso</span><span class="sxs-lookup"><span data-stu-id="35567-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="35567-163">NOTE</span><span class="sxs-lookup"><span data-stu-id="35567-163">NOTES</span></span>

## <span data-ttu-id="35567-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35567-164">RELATED LINKS</span></span>
