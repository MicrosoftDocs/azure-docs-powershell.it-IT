---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDevice.md
ms.openlocfilehash: e13cd1ba814bc5bea66a6a3d06506b9822dd38bd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189934"
---
# <span data-ttu-id="b61db-101">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="b61db-101">Add-AzIotHubDevice</span></span>

## <span data-ttu-id="b61db-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b61db-102">SYNOPSIS</span></span>
<span data-ttu-id="b61db-103">Creare un dispositivo in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="b61db-103">Create a device in an IoT Hub.</span></span>

## <span data-ttu-id="b61db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b61db-104">SYNTAX</span></span>

### <span data-ttu-id="b61db-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b61db-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled]
 [-Children <String[]>] [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b61db-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b61db-106">InputObjectSet</span></span>
```
Add-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b61db-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b61db-107">ResourceIdSet</span></span>
```
Add-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-EdgeEnabled] [-Children <String[]>]
 [-ParentDeviceId <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b61db-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b61db-108">DESCRIPTION</span></span>
<span data-ttu-id="b61db-109">Creare un dispositivo con un tipo di autorizzazione diverso in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="b61db-109">Create a device with different authorization type in an IoT Hub.</span></span>

## <span data-ttu-id="b61db-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b61db-110">EXAMPLES</span></span>

### <span data-ttu-id="b61db-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b61db-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled
```

<span data-ttu-id="b61db-112">Creare un dispositivo per gli spessori con autorizzazioni predefinite (chiave privata condivisa).</span><span class="sxs-lookup"><span data-stu-id="b61db-112">Create an edge enabled IoT device with default authorization (shared private key).</span></span>

### <span data-ttu-id="b61db-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b61db-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice2" -AuthMethod "x509_ca" -Status Disabled -StatusReason "Some Reason"
```

<span data-ttu-id="b61db-114">Creare un dispositivo con un sacco con l'autorizzazione della CA radice con lo stato e il motivo disabilitati.</span><span class="sxs-lookup"><span data-stu-id="b61db-114">Create an IoT device with root CA authorization with disabled status and reason.</span></span>

### <span data-ttu-id="b61db-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b61db-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -EdgeEnabled -Children device1,device2
```

<span data-ttu-id="b61db-116">Creare un dispositivo per gli elementi di Edge abilitato e aggiungere dispositivi secondari.</span><span class="sxs-lookup"><span data-stu-id="b61db-116">Create an edge enabled IoT device and add child devices to it.</span></span>

### <span data-ttu-id="b61db-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="b61db-117">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "shared_private_key" -ParentDeviceId parentDevice1
```

<span data-ttu-id="b61db-118">Creare un dispositivo molto e impostarne il dispositivo padre.</span><span class="sxs-lookup"><span data-stu-id="b61db-118">Create an IoT device and set its parent device.</span></span>

## <span data-ttu-id="b61db-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b61db-119">PARAMETERS</span></span>

### <span data-ttu-id="b61db-120">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="b61db-120">-AuthMethod</span></span>
<span data-ttu-id="b61db-121">Il tipo di autorizzazione con cui deve essere creata un'entità.</span><span class="sxs-lookup"><span data-stu-id="b61db-121">The authorization type an entity is to be created with.</span></span>

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

### <span data-ttu-id="b61db-122">-Bambini</span><span class="sxs-lookup"><span data-stu-id="b61db-122">-Children</span></span>
<span data-ttu-id="b61db-123">L'aggiunta di un elenco di dispositivi secondari (separati da virgole) include solo dispositivi non-Edge.</span><span class="sxs-lookup"><span data-stu-id="b61db-123">Add child device list (comma separated) includes only non-edge devices.</span></span>

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

### <span data-ttu-id="b61db-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b61db-124">-DefaultProfile</span></span>
<span data-ttu-id="b61db-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b61db-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b61db-126">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="b61db-126">-DeviceId</span></span>
<span data-ttu-id="b61db-127">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b61db-127">Target Device Id.</span></span>

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

### <span data-ttu-id="b61db-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="b61db-128">-EdgeEnabled</span></span>
<span data-ttu-id="b61db-129">Contrassegno che indica l'abilitazione del bordo.</span><span class="sxs-lookup"><span data-stu-id="b61db-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="b61db-130">-Force</span><span class="sxs-lookup"><span data-stu-id="b61db-130">-Force</span></span>
<span data-ttu-id="b61db-131">Sovrascrive il dispositivo padre del dispositivo non Edge.</span><span class="sxs-lookup"><span data-stu-id="b61db-131">Overwrites the non-edge device's parent device.</span></span>

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

### <span data-ttu-id="b61db-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b61db-132">-InputObject</span></span>
<span data-ttu-id="b61db-133">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="b61db-133">IotHub object</span></span>

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

### <span data-ttu-id="b61db-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b61db-134">-IotHubName</span></span>
<span data-ttu-id="b61db-135">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="b61db-135">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b61db-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="b61db-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="b61db-137">Identificazione personale del certificato autofirmato esplicito da usare per la chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="b61db-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

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

### <span data-ttu-id="b61db-138">-ParentDeviceId</span><span class="sxs-lookup"><span data-stu-id="b61db-138">-ParentDeviceId</span></span>
<span data-ttu-id="b61db-139">ID del dispositivo Edge.</span><span class="sxs-lookup"><span data-stu-id="b61db-139">Id of edge device.</span></span>

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

### <span data-ttu-id="b61db-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b61db-140">-ResourceGroupName</span></span>
<span data-ttu-id="b61db-141">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b61db-141">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b61db-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b61db-142">-ResourceId</span></span>
<span data-ttu-id="b61db-143">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="b61db-143">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b61db-144">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="b61db-144">-SecondaryThumbprint</span></span>
<span data-ttu-id="b61db-145">Identificazione personale del certificato autofirmato esplicito da usare per la chiave secondaria.</span><span class="sxs-lookup"><span data-stu-id="b61db-145">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

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

### <span data-ttu-id="b61db-146">-Stato</span><span class="sxs-lookup"><span data-stu-id="b61db-146">-Status</span></span>
<span data-ttu-id="b61db-147">Impostare lo stato del dispositivo al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="b61db-147">Set device status upon creation.</span></span>

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

### <span data-ttu-id="b61db-148">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="b61db-148">-StatusReason</span></span>
<span data-ttu-id="b61db-149">Descrizione per lo stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b61db-149">Description for device status.</span></span>

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

### <span data-ttu-id="b61db-150">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b61db-150">-Confirm</span></span>
<span data-ttu-id="b61db-151">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b61db-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b61db-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b61db-152">-WhatIf</span></span>
<span data-ttu-id="b61db-153">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b61db-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b61db-154">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b61db-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b61db-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b61db-155">CommonParameters</span></span>
<span data-ttu-id="b61db-156">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b61db-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b61db-157">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b61db-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b61db-158">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b61db-158">INPUTS</span></span>

### <span data-ttu-id="b61db-159">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b61db-159">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b61db-160">System. String</span><span class="sxs-lookup"><span data-stu-id="b61db-160">System.String</span></span>

## <span data-ttu-id="b61db-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b61db-161">OUTPUTS</span></span>

### <span data-ttu-id="b61db-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="b61db-162">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="b61db-163">Note</span><span class="sxs-lookup"><span data-stu-id="b61db-163">NOTES</span></span>

## <span data-ttu-id="b61db-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b61db-164">RELATED LINKS</span></span>
