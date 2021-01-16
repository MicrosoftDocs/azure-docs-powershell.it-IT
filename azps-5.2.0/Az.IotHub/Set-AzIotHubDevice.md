---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDevice.md
ms.openlocfilehash: 0779403a23a36c972a0d5597d40231b5cc026b37
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354955"
---
# <span data-ttu-id="8723a-101">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="8723a-101">Set-AzIotHubDevice</span></span>

## <span data-ttu-id="8723a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8723a-102">SYNOPSIS</span></span>
<span data-ttu-id="8723a-103">Aggiornare un dispositivo hub molto.</span><span class="sxs-lookup"><span data-stu-id="8723a-103">Update an IoT Hub device.</span></span>

## <span data-ttu-id="8723a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8723a-104">SYNTAX</span></span>

### <span data-ttu-id="8723a-105">ResourceSetForStatus (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8723a-105">ResourceSetForStatus (Default)</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-Status <PSDeviceStatus>] [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8723a-106">InputObjectSetForAuth</span><span class="sxs-lookup"><span data-stu-id="8723a-106">InputObjectSetForAuth</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8723a-107">InputObjectSetForStatus</span><span class="sxs-lookup"><span data-stu-id="8723a-107">InputObjectSetForStatus</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8723a-108">InputObjectSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="8723a-108">InputObjectSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8723a-109">ResourceSetForAuth</span><span class="sxs-lookup"><span data-stu-id="8723a-109">ResourceSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-AuthMethod <PSDeviceAuthType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8723a-110">ResourceSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="8723a-110">ResourceSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-EdgeEnabled <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8723a-111">ResourceIdSetForAuth</span><span class="sxs-lookup"><span data-stu-id="8723a-111">ResourceIdSetForAuth</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-AuthMethod <PSDeviceAuthType>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8723a-112">ResourceIdSetForStatus</span><span class="sxs-lookup"><span data-stu-id="8723a-112">ResourceIdSetForStatus</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-Status <PSDeviceStatus>]
 [-StatusReason <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8723a-113">ResourceIdSetForEdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="8723a-113">ResourceIdSetForEdgeEnabled</span></span>
```
Set-AzIotHubDevice [-ResourceId] <String> [-DeviceId] <String> [-EdgeEnabled <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8723a-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8723a-114">DESCRIPTION</span></span>
<span data-ttu-id="8723a-115">Aggiornare un dispositivo hub molto.</span><span class="sxs-lookup"><span data-stu-id="8723a-115">Update an IoT Hub device.</span></span>

## <span data-ttu-id="8723a-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8723a-116">EXAMPLES</span></span>

### <span data-ttu-id="8723a-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8723a-117">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -EdgeEnabled
```

<span data-ttu-id="8723a-118">Attivare le funzionalità di Edge per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8723a-118">Turn on edge capabilities for device.</span></span>

### <span data-ttu-id="8723a-119">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8723a-119">Example 2</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -Status Disabled
```

<span data-ttu-id="8723a-120">Disabilitare lo stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8723a-120">Disable device status.</span></span>

### <span data-ttu-id="8723a-121">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="8723a-121">Example 3</span></span>
```powershell
PS C:\> Set-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -AuthMethod "x509_ca"
```

<span data-ttu-id="8723a-122">Aggiornare il tipo di autorizzazione di un dispositivo hub molto.</span><span class="sxs-lookup"><span data-stu-id="8723a-122">Update authorization type of an Iot Hub device.</span></span>

## <span data-ttu-id="8723a-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8723a-123">PARAMETERS</span></span>

### <span data-ttu-id="8723a-124">-AuthMethod</span><span class="sxs-lookup"><span data-stu-id="8723a-124">-AuthMethod</span></span>
<span data-ttu-id="8723a-125">Il tipo di autorizzazione con cui deve essere creata un'entità.</span><span class="sxs-lookup"><span data-stu-id="8723a-125">The authorization type an entity is to be created with.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceAuthType
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:
Accepted values: shared_private_key, x509_thumbprint, x509_ca

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8723a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8723a-126">-DefaultProfile</span></span>
<span data-ttu-id="8723a-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8723a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8723a-128">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="8723a-128">-DeviceId</span></span>
<span data-ttu-id="8723a-129">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8723a-129">Target Device Id.</span></span>

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

### <span data-ttu-id="8723a-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="8723a-130">-EdgeEnabled</span></span>
<span data-ttu-id="8723a-131">Contrassegno che indica l'abilitazione del bordo.</span><span class="sxs-lookup"><span data-stu-id="8723a-131">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: InputObjectSetForEdgeEnabled, ResourceSetForEdgeEnabled, ResourceIdSetForEdgeEnabled
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8723a-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8723a-132">-InputObject</span></span>
<span data-ttu-id="8723a-133">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="8723a-133">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSetForAuth, InputObjectSetForStatus, InputObjectSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8723a-134">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8723a-134">-IotHubName</span></span>
<span data-ttu-id="8723a-135">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="8723a-135">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, ResourceSetForAuth, ResourceSetForEdgeEnabled
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8723a-136">-PrimaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="8723a-136">-PrimaryThumbprint</span></span>
<span data-ttu-id="8723a-137">Identificazione personale del certificato autofirmato esplicito da usare per la chiave primaria.</span><span class="sxs-lookup"><span data-stu-id="8723a-137">Explicit self-signed certificate thumbprint to use for primary key.</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8723a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8723a-138">-ResourceGroupName</span></span>
<span data-ttu-id="8723a-139">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8723a-139">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, ResourceSetForAuth, ResourceSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8723a-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8723a-140">-ResourceId</span></span>
<span data-ttu-id="8723a-141">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="8723a-141">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSetForAuth, ResourceIdSetForStatus, ResourceIdSetForEdgeEnabled
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8723a-142">-SecondaryThumbprint</span><span class="sxs-lookup"><span data-stu-id="8723a-142">-SecondaryThumbprint</span></span>
<span data-ttu-id="8723a-143">Identificazione personale del certificato autofirmato esplicito da usare per la chiave secondaria.</span><span class="sxs-lookup"><span data-stu-id="8723a-143">Explicit self-signed certificate thumbprint to use for secondary key.</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectSetForAuth, ResourceSetForAuth, ResourceIdSetForAuth
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8723a-144">-Stato</span><span class="sxs-lookup"><span data-stu-id="8723a-144">-Status</span></span>
<span data-ttu-id="8723a-145">Impostare lo stato del dispositivo al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="8723a-145">Set device status upon creation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceStatus
Parameter Sets: ResourceSetForStatus, InputObjectSetForStatus, ResourceIdSetForStatus
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8723a-146">-StatusReason</span><span class="sxs-lookup"><span data-stu-id="8723a-146">-StatusReason</span></span>
<span data-ttu-id="8723a-147">Descrizione per lo stato del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8723a-147">Description for device status.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSetForStatus, InputObjectSetForStatus, ResourceIdSetForStatus
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8723a-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8723a-148">-Confirm</span></span>
<span data-ttu-id="8723a-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8723a-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8723a-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8723a-150">-WhatIf</span></span>
<span data-ttu-id="8723a-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8723a-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8723a-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8723a-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8723a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8723a-153">CommonParameters</span></span>
<span data-ttu-id="8723a-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8723a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8723a-155">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8723a-155">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8723a-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8723a-156">INPUTS</span></span>

### <span data-ttu-id="8723a-157">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8723a-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8723a-158">System. String</span><span class="sxs-lookup"><span data-stu-id="8723a-158">System.String</span></span>

## <span data-ttu-id="8723a-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8723a-159">OUTPUTS</span></span>

### <span data-ttu-id="8723a-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="8723a-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

## <span data-ttu-id="8723a-161">Note</span><span class="sxs-lookup"><span data-stu-id="8723a-161">NOTES</span></span>

## <span data-ttu-id="8723a-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8723a-162">RELATED LINKS</span></span>
