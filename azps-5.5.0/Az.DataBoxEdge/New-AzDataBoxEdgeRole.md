---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
ms.openlocfilehash: aa44399adcfd5e39d956215b7ca824e5ef9abd60
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204506"
---
# <span data-ttu-id="d38ae-101">New-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="d38ae-101">New-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="d38ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d38ae-102">SYNOPSIS</span></span>
<span data-ttu-id="d38ae-103">Crea un nuovo ruolo per un dispositivo</span><span class="sxs-lookup"><span data-stu-id="d38ae-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="d38ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d38ae-104">SYNTAX</span></span>

### <span data-ttu-id="d38ae-105">ConnectionStringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d38ae-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> -RoleStatus <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d38ae-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="d38ae-106">IotParameterSet</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 -RoleStatus <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d38ae-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d38ae-107">DESCRIPTION</span></span>
<span data-ttu-id="d38ae-108">Il cmdlet **New-AzDataBoxEdgeRole** crea un nuovo ruolo per un dispositivo Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="d38ae-108">The **New-AzDataBoxEdgeRole** cmdlet creates a new Role for a Data Box Edge device.</span></span>

## <span data-ttu-id="d38ae-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d38ae-109">EXAMPLES</span></span>

### <span data-ttu-id="d38ae-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d38ae-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="d38ae-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d38ae-111">PARAMETERS</span></span>

### <span data-ttu-id="d38ae-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d38ae-112">-AsJob</span></span>
<span data-ttu-id="d38ae-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d38ae-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d38ae-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="d38ae-114">-ConnectionString</span></span>
<span data-ttu-id="d38ae-115">Per fornire stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="d38ae-115">To Provide Connection Strings</span></span>

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

### <span data-ttu-id="d38ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d38ae-116">-DefaultProfile</span></span>
<span data-ttu-id="d38ae-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d38ae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d38ae-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d38ae-118">-DeviceName</span></span>
<span data-ttu-id="d38ae-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="d38ae-119">Device Name</span></span>

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

### <span data-ttu-id="d38ae-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="d38ae-120">-DeviceProperty</span></span>
<span data-ttu-id="d38ae-121">Per fornire le proprietà del dispositivo</span><span class="sxs-lookup"><span data-stu-id="d38ae-121">To Provide Device Properties</span></span>

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

### <span data-ttu-id="d38ae-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="d38ae-122">-EncryptionKey</span></span>
<span data-ttu-id="d38ae-123">Chiave di crittografia del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="d38ae-123">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="d38ae-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="d38ae-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="d38ae-125">Iot Device Access Key</span><span class="sxs-lookup"><span data-stu-id="d38ae-125">Iot Device Access Key</span></span>

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

### <span data-ttu-id="d38ae-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="d38ae-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="d38ae-127">Specifica la stringa di connessione del dispositivo IOT</span><span class="sxs-lookup"><span data-stu-id="d38ae-127">Please provide connection string of IOT Device</span></span>

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

### <span data-ttu-id="d38ae-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="d38ae-128">-IotDeviceId</span></span>
<span data-ttu-id="d38ae-129">ID dispositivo del dispositivo Iot</span><span class="sxs-lookup"><span data-stu-id="d38ae-129">Device Id of the Iot Device</span></span>

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

### <span data-ttu-id="d38ae-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="d38ae-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="d38ae-131">Tasto di scelta del dispositivo Iot Edge</span><span class="sxs-lookup"><span data-stu-id="d38ae-131">Access key of the Iot Edge device</span></span>

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

### <span data-ttu-id="d38ae-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="d38ae-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="d38ae-133">Specifica la stringa di connessione del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="d38ae-133">Please provide connection string of Edge Device</span></span>

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

### <span data-ttu-id="d38ae-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="d38ae-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="d38ae-135">ID del dispositivo Iot Edge</span><span class="sxs-lookup"><span data-stu-id="d38ae-135">Id of the Iot Edge Device</span></span>

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

### <span data-ttu-id="d38ae-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="d38ae-136">-IotHostHub</span></span>
<span data-ttu-id="d38ae-137">Indirizzo Hosthub</span><span class="sxs-lookup"><span data-stu-id="d38ae-137">Hosthub address</span></span>

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

### <span data-ttu-id="d38ae-138">-Name</span><span class="sxs-lookup"><span data-stu-id="d38ae-138">-Name</span></span>
<span data-ttu-id="d38ae-139">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="d38ae-139">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38ae-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="d38ae-140">-Platform</span></span>
<span data-ttu-id="d38ae-141">Fornisci la piattaforma, ad esempio: Linux</span><span class="sxs-lookup"><span data-stu-id="d38ae-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="d38ae-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d38ae-142">-ResourceGroupName</span></span>
<span data-ttu-id="d38ae-143">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d38ae-143">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d38ae-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="d38ae-144">-RoleStatus</span></span>
<span data-ttu-id="d38ae-145">Fornire l'abilitazione/disabilitazione dello stato</span><span class="sxs-lookup"><span data-stu-id="d38ae-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="d38ae-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d38ae-146">-Confirm</span></span>
<span data-ttu-id="d38ae-147">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d38ae-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d38ae-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d38ae-148">-WhatIf</span></span>
<span data-ttu-id="d38ae-149">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d38ae-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d38ae-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d38ae-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d38ae-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d38ae-151">CommonParameters</span></span>
<span data-ttu-id="d38ae-152">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d38ae-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d38ae-153">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d38ae-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d38ae-154">INPUT</span><span class="sxs-lookup"><span data-stu-id="d38ae-154">INPUTS</span></span>

### <span data-ttu-id="d38ae-155">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d38ae-155">None</span></span>

## <span data-ttu-id="d38ae-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d38ae-156">OUTPUTS</span></span>

### <span data-ttu-id="d38ae-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="d38ae-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="d38ae-158">NOTE</span><span class="sxs-lookup"><span data-stu-id="d38ae-158">NOTES</span></span>

## <span data-ttu-id="d38ae-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d38ae-159">RELATED LINKS</span></span>
