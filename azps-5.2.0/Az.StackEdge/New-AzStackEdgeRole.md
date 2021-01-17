---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeRole.md
ms.openlocfilehash: f2244bc1d0471924ad7f69ff600e70e92fdc809a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335395"
---
# <span data-ttu-id="102b2-101">New-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="102b2-101">New-AzStackEdgeRole</span></span>

## <span data-ttu-id="102b2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="102b2-102">SYNOPSIS</span></span>
<span data-ttu-id="102b2-103">Crea un nuovo ruolo per un dispositivo</span><span class="sxs-lookup"><span data-stu-id="102b2-103">Creates a new Role for a device</span></span>

## <span data-ttu-id="102b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="102b2-104">SYNTAX</span></span>

### <span data-ttu-id="102b2-105">ConnectionStringParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="102b2-105">ConnectionStringParameterSet (Default)</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-ConnectionString]
 -IotDeviceConnectionString <SecureString> -IotEdgeDeviceConnectionString <SecureString>
 -EncryptionKey <SecureString> -Platform <String> [-RoleStatus <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="102b2-106">IotParameterSet</span><span class="sxs-lookup"><span data-stu-id="102b2-106">IotParameterSet</span></span>
```
New-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-DeviceProperty]
 -IotDeviceId <String> -IotDeviceAccessKey <SecureString> -IotEdgeDeviceId <String>
 -IotEdgeDeviceAccessKey <SecureString> -IotHostHub <String> -EncryptionKey <SecureString> -Platform <String>
 [-RoleStatus <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="102b2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="102b2-107">DESCRIPTION</span></span>
<span data-ttu-id="102b2-108">Il cmdlet **New-AzStackEdgeRole** crea un nuovo ruolo per un dispositivo Edge dello stack.</span><span class="sxs-lookup"><span data-stu-id="102b2-108">The **New-AzStackEdgeRole** cmdlet creates a new Role for a Stack Edge device.</span></span>

## <span data-ttu-id="102b2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="102b2-109">EXAMPLES</span></span>

### <span data-ttu-id="102b2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="102b2-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName -Name iotrole -DeviceProperties
 -IotDeviceId iotDeviceId -IotDeviceAccessKey iotAccessKey -IotEdgeDeviceId iotEdgeDeviceId -IotEdgeDeviceAccessKey iotEdgeDeviceAccessKey
 -IotHostHub "ehub.azure-devices.net" -EncryptionKey @SecureString -Platform Linux -RoleStatus Enabled

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceId   iotDeviceId  resourceGroupName
```

## <span data-ttu-id="102b2-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="102b2-111">PARAMETERS</span></span>

### <span data-ttu-id="102b2-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="102b2-112">-AsJob</span></span>
<span data-ttu-id="102b2-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="102b2-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="102b2-114">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="102b2-114">-ConnectionString</span></span>
<span data-ttu-id="102b2-115">Per specificare stringhe di connessione</span><span class="sxs-lookup"><span data-stu-id="102b2-115">To Provide Connection Strings</span></span>

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

### <span data-ttu-id="102b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="102b2-116">-DefaultProfile</span></span>
<span data-ttu-id="102b2-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="102b2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="102b2-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="102b2-118">-DeviceName</span></span>
<span data-ttu-id="102b2-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="102b2-119">Device Name</span></span>

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

### <span data-ttu-id="102b2-120">-DeviceProperty</span><span class="sxs-lookup"><span data-stu-id="102b2-120">-DeviceProperty</span></span>
<span data-ttu-id="102b2-121">Per specificare le proprietà del dispositivo</span><span class="sxs-lookup"><span data-stu-id="102b2-121">To Provide Device Properties</span></span>

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

### <span data-ttu-id="102b2-122">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="102b2-122">-EncryptionKey</span></span>
<span data-ttu-id="102b2-123">Chiave di crittografia del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="102b2-123">Encryption key of the Edge device</span></span>

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

### <span data-ttu-id="102b2-124">-IotDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="102b2-124">-IotDeviceAccessKey</span></span>
<span data-ttu-id="102b2-125">Tasto di accesso del dispositivo</span><span class="sxs-lookup"><span data-stu-id="102b2-125">Iot Device Access Key</span></span>

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

### <span data-ttu-id="102b2-126">-IotDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="102b2-126">-IotDeviceConnectionString</span></span>
<span data-ttu-id="102b2-127">Fornisci la stringa di connessione del dispositivo per gli altri</span><span class="sxs-lookup"><span data-stu-id="102b2-127">Please provide connection string of IOT Device</span></span>

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

### <span data-ttu-id="102b2-128">-IotDeviceId</span><span class="sxs-lookup"><span data-stu-id="102b2-128">-IotDeviceId</span></span>
<span data-ttu-id="102b2-129">ID dispositivo del dispositivo per gli altri dispositivi</span><span class="sxs-lookup"><span data-stu-id="102b2-129">Device Id of the Iot Device</span></span>

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

### <span data-ttu-id="102b2-130">-IotEdgeDeviceAccessKey</span><span class="sxs-lookup"><span data-stu-id="102b2-130">-IotEdgeDeviceAccessKey</span></span>
<span data-ttu-id="102b2-131">Chiave di accesso del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="102b2-131">Access key of the Iot Edge device</span></span>

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

### <span data-ttu-id="102b2-132">-IotEdgeDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="102b2-132">-IotEdgeDeviceConnectionString</span></span>
<span data-ttu-id="102b2-133">Fornisci la stringa di connessione del dispositivo Edge</span><span class="sxs-lookup"><span data-stu-id="102b2-133">Please provide connection string of Edge Device</span></span>

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

### <span data-ttu-id="102b2-134">-IotEdgeDeviceId</span><span class="sxs-lookup"><span data-stu-id="102b2-134">-IotEdgeDeviceId</span></span>
<span data-ttu-id="102b2-135">ID del dispositivo Edge molto</span><span class="sxs-lookup"><span data-stu-id="102b2-135">Id of the Iot Edge Device</span></span>

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

### <span data-ttu-id="102b2-136">-IotHostHub</span><span class="sxs-lookup"><span data-stu-id="102b2-136">-IotHostHub</span></span>
<span data-ttu-id="102b2-137">Indirizzo Hosthub</span><span class="sxs-lookup"><span data-stu-id="102b2-137">Hosthub address</span></span>

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

### <span data-ttu-id="102b2-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="102b2-138">-Name</span></span>
<span data-ttu-id="102b2-139">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="102b2-139">Resource Name</span></span>

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

### <span data-ttu-id="102b2-140">-Platform</span><span class="sxs-lookup"><span data-stu-id="102b2-140">-Platform</span></span>
<span data-ttu-id="102b2-141">Fornisci la piattaforma, ad esempio: Linux</span><span class="sxs-lookup"><span data-stu-id="102b2-141">Provide the Platform, for ex: Linux</span></span>

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

### <span data-ttu-id="102b2-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="102b2-142">-ResourceGroupName</span></span>
<span data-ttu-id="102b2-143">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="102b2-143">Resource Group Name</span></span>

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

### <span data-ttu-id="102b2-144">-RoleStatus</span><span class="sxs-lookup"><span data-stu-id="102b2-144">-RoleStatus</span></span>
<span data-ttu-id="102b2-145">Specificare lo stato di attivazione/disattivazione</span><span class="sxs-lookup"><span data-stu-id="102b2-145">Provide the status enable/disable</span></span>

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

### <span data-ttu-id="102b2-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="102b2-146">-Confirm</span></span>
<span data-ttu-id="102b2-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="102b2-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="102b2-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="102b2-148">-WhatIf</span></span>
<span data-ttu-id="102b2-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="102b2-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="102b2-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="102b2-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="102b2-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="102b2-151">CommonParameters</span></span>
<span data-ttu-id="102b2-152">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="102b2-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="102b2-153">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="102b2-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="102b2-154">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="102b2-154">INPUTS</span></span>

### <span data-ttu-id="102b2-155">Nessuno</span><span class="sxs-lookup"><span data-stu-id="102b2-155">None</span></span>

## <span data-ttu-id="102b2-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="102b2-156">OUTPUTS</span></span>

### <span data-ttu-id="102b2-157">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="102b2-157">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="102b2-158">Note</span><span class="sxs-lookup"><span data-stu-id="102b2-158">NOTES</span></span>

## <span data-ttu-id="102b2-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="102b2-159">RELATED LINKS</span></span>
