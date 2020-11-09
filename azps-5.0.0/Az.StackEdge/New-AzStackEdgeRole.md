---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
ms.openlocfilehash: f2244bc1d0471924ad7f69ff600e70e92fdc809a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302376"
---
# <span data-ttu-id="1ddf5-101">New-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="1ddf5-101">New-AzStackEdgeRole</span></span>

## <span data-ttu-id="1ddf5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1ddf5-102">SYNOPSIS</span></span>
<span data-ttu-id="1ddf5-103">Crea un nuovo ruolo per un dispositivo</span><span class="sxs-lookup"><span data-stu-id="1ddf5-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="1ddf5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1ddf5-104">SYNTAX</span></span>

### <span data-ttu-id="1ddf5-105">ConnectionStringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1ddf5-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> [-RoleStatus <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ddf5-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ddf5-106">IotParameterSet</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 [-RoleStatus <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1ddf5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ddf5-107">DESCRIPTION</span></span>
<span data-ttu-id="1ddf5-108">Il cmdlet **New-AzStackEdgeRole** crea un nuovo ruolo per un dispositivo Edge dello stack.</span><span class="sxs-lookup"><span data-stu-id="1ddf5-108">The **New-AzStackEdgeRole** cmdlet creates a new Role for a Stack Edge device.</span></span>

## <span data-ttu-id="1ddf5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1ddf5-109">EXAMPLES</span></span>

### <span data-ttu-id="1ddf5-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1ddf5-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="1ddf5-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1ddf5-111">PARAMETERS</span></span>

### <span data-ttu-id="1ddf5-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ddf5-112">-AsJob</span></span>
<span data-ttu-id="1ddf5-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1ddf5-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ddf5-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="1ddf5-114">-ConnectionString</span></span>
<span data-ttu-id="1ddf5-115">Per specificare stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="1ddf5-115">To Provide Connection Strings</span></span>

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

### <span data-ttu-id="1ddf5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ddf5-116">-DefaultProfile</span></span>
<span data-ttu-id="1ddf5-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1ddf5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ddf5-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1ddf5-118">-DeviceName</span></span>
<span data-ttu-id="1ddf5-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="1ddf5-119">Device Name</span></span>

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

### <span data-ttu-id="1ddf5-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="1ddf5-120">-DeviceProperty</span></span>
<span data-ttu-id="1ddf5-121">Per specificare le proprietà del dispositivo</span><span class="sxs-lookup"><span data-stu-id="1ddf5-121">To Provide Device Properties</span></span>

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

### <span data-ttu-id="1ddf5-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="1ddf5-122">-EncryptionKey</span></span>
<span data-ttu-id="1ddf5-123">Chiave di crittografia del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="1ddf5-123">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="1ddf5-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="1ddf5-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="1ddf5-125">Tasto di accesso del dispositivo</span><span class="sxs-lookup"><span data-stu-id="1ddf5-125">Iot Device Access Key</span></span>

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

### <span data-ttu-id="1ddf5-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="1ddf5-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="1ddf5-127">Fornisci la stringa di connessione del dispositivo per gli altri</span><span class="sxs-lookup"><span data-stu-id="1ddf5-127">Please provide connection string of IOT Device</span></span>

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

### <span data-ttu-id="1ddf5-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="1ddf5-128">-IotDeviceId</span></span>
<span data-ttu-id="1ddf5-129">ID dispositivo del dispositivo per gli altri dispositivi</span><span class="sxs-lookup"><span data-stu-id="1ddf5-129">Device Id of the Iot Device</span></span>

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

### <span data-ttu-id="1ddf5-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="1ddf5-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="1ddf5-131">Chiave di accesso del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="1ddf5-131">Access key of the Iot Edge device</span></span>

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

### <span data-ttu-id="1ddf5-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="1ddf5-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="1ddf5-133">Fornisci la stringa di connessione del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="1ddf5-133">Please provide connection string of Edge Device</span></span>

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

### <span data-ttu-id="1ddf5-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="1ddf5-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="1ddf5-135">ID del dispositivo Edge molto</span><span class="sxs-lookup"><span data-stu-id="1ddf5-135">Id of the Iot Edge Device</span></span>

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

### <span data-ttu-id="1ddf5-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="1ddf5-136">-IotHostHub</span></span>
<span data-ttu-id="1ddf5-137">Indirizzo Hosthub</span><span class="sxs-lookup"><span data-stu-id="1ddf5-137">Hosthub address</span></span>

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

### <span data-ttu-id="1ddf5-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="1ddf5-138">-Name</span></span>
<span data-ttu-id="1ddf5-139">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="1ddf5-139">Resource Name</span></span>

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

### <span data-ttu-id="1ddf5-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="1ddf5-140">-Platform</span></span>
<span data-ttu-id="1ddf5-141">Fornisci la piattaforma, ad esempio: Linux</span><span class="sxs-lookup"><span data-stu-id="1ddf5-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="1ddf5-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ddf5-142">-ResourceGroupName</span></span>
<span data-ttu-id="1ddf5-143">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="1ddf5-143">Resource Group Name</span></span>

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

### <span data-ttu-id="1ddf5-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="1ddf5-144">-RoleStatus</span></span>
<span data-ttu-id="1ddf5-145">Specificare lo stato di attivazione/disattivazione</span><span class="sxs-lookup"><span data-stu-id="1ddf5-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="1ddf5-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1ddf5-146">-Confirm</span></span>
<span data-ttu-id="1ddf5-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ddf5-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ddf5-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ddf5-148">-WhatIf</span></span>
<span data-ttu-id="1ddf5-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ddf5-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ddf5-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1ddf5-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ddf5-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ddf5-151">CommonParameters</span></span>
<span data-ttu-id="1ddf5-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ddf5-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ddf5-153">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ddf5-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ddf5-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1ddf5-154">INPUTS</span></span>

### <span data-ttu-id="1ddf5-155">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1ddf5-155">None</span></span>

## <span data-ttu-id="1ddf5-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1ddf5-156">OUTPUTS</span></span>

### <span data-ttu-id="1ddf5-157">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="1ddf5-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="1ddf5-158">Note</span><span class="sxs-lookup"><span data-stu-id="1ddf5-158">NOTES</span></span>

## <span data-ttu-id="1ddf5-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1ddf5-159">RELATED LINKS</span></span>
