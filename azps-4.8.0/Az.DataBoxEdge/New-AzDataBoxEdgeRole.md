---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeRole.md
ms.openlocfilehash: aa44399adcfd5e39d956215b7ca824e5ef9abd60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190510"
---
# <span data-ttu-id="b18e8-101">New-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="b18e8-101">New-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="b18e8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b18e8-102">SYNOPSIS</span></span>
<span data-ttu-id="b18e8-103">Crea un nuovo ruolo per un dispositivo</span><span class="sxs-lookup"><span data-stu-id="b18e8-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="b18e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b18e8-104">SYNTAX</span></span>

### <span data-ttu-id="b18e8-105">ConnectionStringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b18e8-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> -RoleStatus <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b18e8-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="b18e8-106">IotParameterSet</span></span>
```
New-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 -RoleStatus <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b18e8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b18e8-107">DESCRIPTION</span></span>
<span data-ttu-id="b18e8-108">Il cmdlet **New-AzDataBoxEdgeRole** crea un nuovo ruolo per un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="b18e8-108">The **New-AzDataBoxEdgeRole** cmdlet creates a new Role for a Data Box Edge device.</span></span>

## <span data-ttu-id="b18e8-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b18e8-109">EXAMPLES</span></span>

### <span data-ttu-id="b18e8-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b18e8-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="b18e8-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b18e8-111">PARAMETERS</span></span>

### <span data-ttu-id="b18e8-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b18e8-112">-AsJob</span></span>
<span data-ttu-id="b18e8-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b18e8-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b18e8-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="b18e8-114">-ConnectionString</span></span>
<span data-ttu-id="b18e8-115">Per specificare stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="b18e8-115">To Provide Connection Strings</span></span>

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

### <span data-ttu-id="b18e8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b18e8-116">-DefaultProfile</span></span>
<span data-ttu-id="b18e8-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b18e8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b18e8-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="b18e8-118">-DeviceName</span></span>
<span data-ttu-id="b18e8-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="b18e8-119">Device Name</span></span>

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

### <span data-ttu-id="b18e8-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="b18e8-120">-DeviceProperty</span></span>
<span data-ttu-id="b18e8-121">Per specificare le proprietà del dispositivo</span><span class="sxs-lookup"><span data-stu-id="b18e8-121">To Provide Device Properties</span></span>

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

### <span data-ttu-id="b18e8-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="b18e8-122">-EncryptionKey</span></span>
<span data-ttu-id="b18e8-123">Chiave di crittografia del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="b18e8-123">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="b18e8-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="b18e8-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="b18e8-125">Tasto di accesso del dispositivo</span><span class="sxs-lookup"><span data-stu-id="b18e8-125">Iot Device Access Key</span></span>

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

### <span data-ttu-id="b18e8-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="b18e8-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="b18e8-127">Fornisci la stringa di connessione del dispositivo per gli altri</span><span class="sxs-lookup"><span data-stu-id="b18e8-127">Please provide connection string of IOT Device</span></span>

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

### <span data-ttu-id="b18e8-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="b18e8-128">-IotDeviceId</span></span>
<span data-ttu-id="b18e8-129">ID dispositivo del dispositivo per gli altri dispositivi</span><span class="sxs-lookup"><span data-stu-id="b18e8-129">Device Id of the Iot Device</span></span>

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

### <span data-ttu-id="b18e8-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="b18e8-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="b18e8-131">Chiave di accesso del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="b18e8-131">Access key of the Iot Edge device</span></span>

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

### <span data-ttu-id="b18e8-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="b18e8-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="b18e8-133">Fornisci la stringa di connessione del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="b18e8-133">Please provide connection string of Edge Device</span></span>

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

### <span data-ttu-id="b18e8-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="b18e8-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="b18e8-135">ID del dispositivo Edge molto</span><span class="sxs-lookup"><span data-stu-id="b18e8-135">Id of the Iot Edge Device</span></span>

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

### <span data-ttu-id="b18e8-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="b18e8-136">-IotHostHub</span></span>
<span data-ttu-id="b18e8-137">Indirizzo Hosthub</span><span class="sxs-lookup"><span data-stu-id="b18e8-137">Hosthub address</span></span>

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

### <span data-ttu-id="b18e8-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="b18e8-138">-Name</span></span>
<span data-ttu-id="b18e8-139">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="b18e8-139">Resource Name</span></span>

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

### <span data-ttu-id="b18e8-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="b18e8-140">-Platform</span></span>
<span data-ttu-id="b18e8-141">Fornisci la piattaforma, ad esempio: Linux</span><span class="sxs-lookup"><span data-stu-id="b18e8-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="b18e8-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b18e8-142">-ResourceGroupName</span></span>
<span data-ttu-id="b18e8-143">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b18e8-143">Resource Group Name</span></span>

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

### <span data-ttu-id="b18e8-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="b18e8-144">-RoleStatus</span></span>
<span data-ttu-id="b18e8-145">Specificare lo stato di attivazione/disattivazione</span><span class="sxs-lookup"><span data-stu-id="b18e8-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="b18e8-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b18e8-146">-Confirm</span></span>
<span data-ttu-id="b18e8-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b18e8-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b18e8-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b18e8-148">-WhatIf</span></span>
<span data-ttu-id="b18e8-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b18e8-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b18e8-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b18e8-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b18e8-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b18e8-151">CommonParameters</span></span>
<span data-ttu-id="b18e8-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b18e8-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b18e8-153">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b18e8-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b18e8-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b18e8-154">INPUTS</span></span>

### <span data-ttu-id="b18e8-155">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b18e8-155">None</span></span>

## <span data-ttu-id="b18e8-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b18e8-156">OUTPUTS</span></span>

### <span data-ttu-id="b18e8-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="b18e8-157">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="b18e8-158">Note</span><span class="sxs-lookup"><span data-stu-id="b18e8-158">NOTES</span></span>

## <span data-ttu-id="b18e8-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b18e8-159">RELATED LINKS</span></span>