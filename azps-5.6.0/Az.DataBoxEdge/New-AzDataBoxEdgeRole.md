---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
ms.openlocfilehash: 0158116440ae7ffc1638ce08c6561e80ca034ae8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978621"
---
# <span data-ttu-id="020d6-101">New-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="020d6-101">New-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="020d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="020d6-102">SYNOPSIS</span></span>
<span data-ttu-id="020d6-103">Crea un nuovo ruolo per un dispositivo</span><span class="sxs-lookup"><span data-stu-id="020d6-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="020d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="020d6-104">SYNTAX</span></span>

### <span data-ttu-id="020d6-105">ConnectionStringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="020d6-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> -RoleStatus <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="020d6-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="020d6-106">IotParameterSet</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 -RoleStatus <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="020d6-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="020d6-107">DESCRIPTION</span></span>
<span data-ttu-id="020d6-108">Il cmdlet **New-AzDataBoxEdgeRole** crea un nuovo ruolo per un dispositivo Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="020d6-108">The **New-AzDataBoxEdgeRole** cmdlet creates a new Role for a Data Box Edge device.</span></span>

## <span data-ttu-id="020d6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="020d6-109">EXAMPLES</span></span>

### <span data-ttu-id="020d6-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="020d6-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="020d6-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="020d6-111">PARAMETERS</span></span>

### <span data-ttu-id="020d6-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="020d6-112">-AsJob</span></span>
<span data-ttu-id="020d6-113">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="020d6-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="020d6-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="020d6-114">-ConnectionString</span></span>
<span data-ttu-id="020d6-115">Per fornire stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="020d6-115">To Provide Connection Strings</span></span>

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

### <span data-ttu-id="020d6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="020d6-116">-DefaultProfile</span></span>
<span data-ttu-id="020d6-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="020d6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="020d6-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="020d6-118">-DeviceName</span></span>
<span data-ttu-id="020d6-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="020d6-119">Device Name</span></span>

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

### <span data-ttu-id="020d6-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="020d6-120">-DeviceProperty</span></span>
<span data-ttu-id="020d6-121">Per fornire le proprietà del dispositivo</span><span class="sxs-lookup"><span data-stu-id="020d6-121">To Provide Device Properties</span></span>

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

### <span data-ttu-id="020d6-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="020d6-122">-EncryptionKey</span></span>
<span data-ttu-id="020d6-123">Chiave di crittografia del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="020d6-123">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="020d6-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="020d6-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="020d6-125">Iot Device Access Key</span><span class="sxs-lookup"><span data-stu-id="020d6-125">Iot Device Access Key</span></span>

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

### <span data-ttu-id="020d6-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="020d6-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="020d6-127">Specifica la stringa di connessione del dispositivo IOT</span><span class="sxs-lookup"><span data-stu-id="020d6-127">Please provide connection string of IOT Device</span></span>

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

### <span data-ttu-id="020d6-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="020d6-128">-IotDeviceId</span></span>
<span data-ttu-id="020d6-129">ID dispositivo del dispositivo Iot</span><span class="sxs-lookup"><span data-stu-id="020d6-129">Device Id of the Iot Device</span></span>

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

### <span data-ttu-id="020d6-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="020d6-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="020d6-131">Tasto di scelta del dispositivo Iot Edge</span><span class="sxs-lookup"><span data-stu-id="020d6-131">Access key of the Iot Edge device</span></span>

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

### <span data-ttu-id="020d6-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="020d6-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="020d6-133">Specifica la stringa di connessione del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="020d6-133">Please provide connection string of Edge Device</span></span>

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

### <span data-ttu-id="020d6-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="020d6-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="020d6-135">ID del dispositivo Iot Edge</span><span class="sxs-lookup"><span data-stu-id="020d6-135">Id of the Iot Edge Device</span></span>

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

### <span data-ttu-id="020d6-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="020d6-136">-IotHostHub</span></span>
<span data-ttu-id="020d6-137">Indirizzo Hosthub</span><span class="sxs-lookup"><span data-stu-id="020d6-137">Hosthub address</span></span>

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

### <span data-ttu-id="020d6-138">-Name</span><span class="sxs-lookup"><span data-stu-id="020d6-138">-Name</span></span>
<span data-ttu-id="020d6-139">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="020d6-139">Resource Name</span></span>

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

### <span data-ttu-id="020d6-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="020d6-140">-Platform</span></span>
<span data-ttu-id="020d6-141">Fornisci la piattaforma, ad esempio: Linux</span><span class="sxs-lookup"><span data-stu-id="020d6-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="020d6-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="020d6-142">-ResourceGroupName</span></span>
<span data-ttu-id="020d6-143">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="020d6-143">Resource Group Name</span></span>

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

### <span data-ttu-id="020d6-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="020d6-144">-RoleStatus</span></span>
<span data-ttu-id="020d6-145">Fornire l'abilitazione/disabilitazione dello stato</span><span class="sxs-lookup"><span data-stu-id="020d6-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="020d6-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="020d6-146">-Confirm</span></span>
<span data-ttu-id="020d6-147">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="020d6-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="020d6-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="020d6-148">-WhatIf</span></span>
<span data-ttu-id="020d6-149">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="020d6-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="020d6-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="020d6-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="020d6-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="020d6-151">CommonParameters</span></span>
<span data-ttu-id="020d6-152">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="020d6-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="020d6-153">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="020d6-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="020d6-154">INPUT</span><span class="sxs-lookup"><span data-stu-id="020d6-154">INPUTS</span></span>

### <span data-ttu-id="020d6-155">Nessuno</span><span class="sxs-lookup"><span data-stu-id="020d6-155">None</span></span>

## <span data-ttu-id="020d6-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="020d6-156">OUTPUTS</span></span>

### <span data-ttu-id="020d6-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="020d6-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="020d6-158">NOTE</span><span class="sxs-lookup"><span data-stu-id="020d6-158">NOTES</span></span>

## <span data-ttu-id="020d6-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="020d6-159">RELATED LINKS</span></span>
