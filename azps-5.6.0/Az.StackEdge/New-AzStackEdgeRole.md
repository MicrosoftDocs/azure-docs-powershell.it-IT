---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/new-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
ms.openlocfilehash: 785c092333d0e083ed3ee356a0c4e76d6188b96b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005262"
---
# <span data-ttu-id="863d0-101">New-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="863d0-101">New-AzStackEdgeRole</span></span>

## <span data-ttu-id="863d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="863d0-102">SYNOPSIS</span></span>
<span data-ttu-id="863d0-103">Crea un nuovo ruolo per un dispositivo</span><span class="sxs-lookup"><span data-stu-id="863d0-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="863d0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="863d0-104">SYNTAX</span></span>

### <span data-ttu-id="863d0-105">ConnectionStringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="863d0-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> [-RoleStatus <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="863d0-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="863d0-106">IotParameterSet</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 [-RoleStatus <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="863d0-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="863d0-107">DESCRIPTION</span></span>
<span data-ttu-id="863d0-108">Il cmdlet **New-AzStackEdgeRole** crea un nuovo ruolo per un dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="863d0-108">The **New-AzStackEdgeRole** cmdlet creates a new Role for a Stack Edge device.</span></span>

## <span data-ttu-id="863d0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="863d0-109">EXAMPLES</span></span>

### <span data-ttu-id="863d0-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="863d0-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="863d0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="863d0-111">PARAMETERS</span></span>

### <span data-ttu-id="863d0-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="863d0-112">-AsJob</span></span>
<span data-ttu-id="863d0-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="863d0-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="863d0-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="863d0-114">-ConnectionString</span></span>
<span data-ttu-id="863d0-115">Per fornire stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="863d0-115">To Provide Connection Strings</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="863d0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="863d0-116">-DefaultProfile</span></span>
<span data-ttu-id="863d0-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="863d0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="863d0-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="863d0-118">-DeviceName</span></span>
<span data-ttu-id="863d0-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="863d0-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="863d0-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="863d0-120">-DeviceProperty</span></span>
<span data-ttu-id="863d0-121">Per fornire le proprietà del dispositivo</span><span class="sxs-lookup"><span data-stu-id="863d0-121">To Provide Device Properties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IotParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="863d0-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="863d0-122">-EncryptionKey</span></span>
<span data-ttu-id="863d0-123">Chiave di crittografia del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="863d0-123">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="863d0-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="863d0-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="863d0-125">Iot Device Access Key</span><span class="sxs-lookup"><span data-stu-id="863d0-125">Iot Device Access Key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="863d0-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="863d0-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="863d0-127">Specifica la stringa di connessione del dispositivo IOT</span><span class="sxs-lookup"><span data-stu-id="863d0-127">Please provide connection string of IOT Device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="863d0-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="863d0-128">-IotDeviceId</span></span>
<span data-ttu-id="863d0-129">ID dispositivo del dispositivo Iot</span><span class="sxs-lookup"><span data-stu-id="863d0-129">Device Id of the Iot Device</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="863d0-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="863d0-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="863d0-131">Tasto di scelta del dispositivo Iot Edge</span><span class="sxs-lookup"><span data-stu-id="863d0-131">Access key of the Iot Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="863d0-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="863d0-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="863d0-133">Specifica la stringa di connessione del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="863d0-133">Please provide connection string of Edge Device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ConnectionStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="863d0-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="863d0-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="863d0-135">ID del dispositivo Iot Edge</span><span class="sxs-lookup"><span data-stu-id="863d0-135">Id of the Iot Edge Device</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="863d0-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="863d0-136">-IotHostHub</span></span>
<span data-ttu-id="863d0-137">Indirizzo Hosthub</span><span class="sxs-lookup"><span data-stu-id="863d0-137">Hosthub address</span></span>

```yaml
Type: System.String
Parameter Sets: IotParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="863d0-138">-Name</span><span class="sxs-lookup"><span data-stu-id="863d0-138">-Name</span></span>
<span data-ttu-id="863d0-139">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="863d0-139">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="863d0-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="863d0-140">-Platform</span></span>
<span data-ttu-id="863d0-141">Fornisci la piattaforma, ad esempio: Linux</span><span class="sxs-lookup"><span data-stu-id="863d0-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="863d0-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="863d0-142">-ResourceGroupName</span></span>
<span data-ttu-id="863d0-143">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="863d0-143">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="863d0-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="863d0-144">-RoleStatus</span></span>
<span data-ttu-id="863d0-145">Fornire l'abilitazione/disabilitazione dello stato</span><span class="sxs-lookup"><span data-stu-id="863d0-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="863d0-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="863d0-146">-Confirm</span></span>
<span data-ttu-id="863d0-147">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="863d0-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="863d0-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="863d0-148">-WhatIf</span></span>
<span data-ttu-id="863d0-149">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="863d0-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="863d0-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="863d0-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="863d0-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="863d0-151">CommonParameters</span></span>
<span data-ttu-id="863d0-152">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="863d0-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="863d0-153">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="863d0-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="863d0-154">INPUT</span><span class="sxs-lookup"><span data-stu-id="863d0-154">INPUTS</span></span>

### <span data-ttu-id="863d0-155">Nessuno</span><span class="sxs-lookup"><span data-stu-id="863d0-155">None</span></span>

## <span data-ttu-id="863d0-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="863d0-156">OUTPUTS</span></span>

### <span data-ttu-id="863d0-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="863d0-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="863d0-158">NOTE</span><span class="sxs-lookup"><span data-stu-id="863d0-158">NOTES</span></span>

## <span data-ttu-id="863d0-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="863d0-159">RELATED LINKS</span></span>
