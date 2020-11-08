---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzDeviceSecurityGroup.md
ms.openlocfilehash: 269d333c9b74ed0e3e959ef609531bcea41b724c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188852"
---
# <span data-ttu-id="32171-101">Set-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="32171-101">Set-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="32171-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32171-102">SYNOPSIS</span></span>
<span data-ttu-id="32171-103">Creare o aggiornare un gruppo di sicurezza del dispositivo</span><span class="sxs-lookup"><span data-stu-id="32171-103">Create or update device security group</span></span>

## <span data-ttu-id="32171-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32171-104">SYNTAX</span></span>

### <span data-ttu-id="32171-105">ResourceIdLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="32171-105">ResourceIdLevelResource (Default)</span></span>
```
Set-AzDeviceSecurityGroup -Name <String> -HubResourceId <String>
 [-ThresholdRule <PSThresholdCustomAlertRule[]>] [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>]
 [-AllowlistRule <PSAllowlistCustomAlertRule[]>] [-DenylistRule <PSDenylistCustomAlertRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32171-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="32171-106">InputObject</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -InputObject <PSDeviceSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32171-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="32171-107">ResourceId</span></span>
```
Set-AzDeviceSecurityGroup [-ThresholdRule <PSThresholdCustomAlertRule[]>]
 [-TimeWindowRule <PSTimeWindowCustomAlertRule[]>] [-AllowlistRule <PSAllowlistCustomAlertRule[]>]
 [-DenylistRule <PSDenylistCustomAlertRule[]>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32171-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32171-108">DESCRIPTION</span></span>
<span data-ttu-id="32171-109">Il cmdlet Set-AzDeviceSecurityGroup crea o aggiorna un gruppo di sicurezza dei dispositivi definito nella soluzione di sicurezza degli altri.</span><span class="sxs-lookup"><span data-stu-id="32171-109">The Set-AzDeviceSecurityGroup cmdlet creates or updates a device security group defined in iot security solution.</span></span>

## <span data-ttu-id="32171-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32171-110">EXAMPLES</span></span>

### <span data-ttu-id="32171-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="32171-111">Example 1</span></span>
```powershell
PS C:\> $TimeWindowSize = New-TimeSpan -Minutes 5
PS C:\> $TimeWindowRule = New-AzDeviceSecurityGroupTimeWindowRuleObject -Type "ActiveConnectionsNotInAllowedRange" -Enabled $true 
-MaxThreshold 30 -MinThreshold 0 -TimeWindowSize $TimeWindowSize
PS C:\> Set-AzDeviceSecurityGroup -Name "MySecurityGroup" 
-HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 
-TimeWindowRule $TimeWindowRules

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub/providers/Microsoft.Security/deviceSecurityGroups/MySecurityGroup"
Name: "MySecurityGroup"
Type: "Microsoft.Security/deviceSecurityGroups"
ThresholdRules: []
TimeWindowRules: [
            {
              RuleType: "ActiveConnectionsNotInAllowedRange"
              DisplayName: "Number of active connections is not in allowed range"
              Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
              IsEnabled: true
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT5M"
            }]
AllowlistRules: [
            {
              RuleType": "ConnectionToIpNotAllowed",
              DisplayName: "Outbound connection to an ip that isn't allowed"
              Description: "Get an alert when an outbound connection is created between your device and an ip that isn't allowed"
              IsEnabled: false
              ValueType: "IpCidr"
              AllowlistValues: []
            },
            {
              RuleType: "LocalUserNotAllowed"
              DisplayName: "Login by a local user that isn't allowed"
              Description: "Get an alert when a local user that isn't allowed logins to the device"
              IsEnabled: false
              ValueType: "String"
              AllowlistValues: []
            }]
DenylistRules: []
```

<span data-ttu-id="32171-112">Aggiornare il gruppo di sicurezza dei dispositivi esistente dall'hub "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" con il tipo di regola "ActiveConnectionsNotInAllowedRange"</span><span class="sxs-lookup"><span data-stu-id="32171-112">Update existing device security group from IoT Hub "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" with rule type "ActiveConnectionsNotInAllowedRange"</span></span>

## <span data-ttu-id="32171-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32171-113">PARAMETERS</span></span>

### <span data-ttu-id="32171-114">-AllowlistRule</span><span class="sxs-lookup"><span data-stu-id="32171-114">-AllowlistRule</span></span>
<span data-ttu-id="32171-115">Regole Consenti elenco.</span><span class="sxs-lookup"><span data-stu-id="32171-115">Allow list rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32171-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32171-116">-DefaultProfile</span></span>
<span data-ttu-id="32171-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32171-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32171-118">-DenylistRule</span><span class="sxs-lookup"><span data-stu-id="32171-118">-DenylistRule</span></span>
<span data-ttu-id="32171-119">Nega regole elenco.</span><span class="sxs-lookup"><span data-stu-id="32171-119">Deny list rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32171-120">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="32171-120">-HubResourceId</span></span>
<span data-ttu-id="32171-121">ID risorsa Hub di un sacco.</span><span class="sxs-lookup"><span data-stu-id="32171-121">IoT Hub resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32171-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32171-122">-InputObject</span></span>
<span data-ttu-id="32171-123">Oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="32171-123">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32171-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="32171-124">-Name</span></span>
<span data-ttu-id="32171-125">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="32171-125">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32171-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="32171-126">-ResourceId</span></span>
<span data-ttu-id="32171-127">ID della risorsa di sicurezza a cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="32171-127">ID of the security resource that you want to invoke the command on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32171-128">-ThresholdRule</span><span class="sxs-lookup"><span data-stu-id="32171-128">-ThresholdRule</span></span>
<span data-ttu-id="32171-129">Regole di soglia.</span><span class="sxs-lookup"><span data-stu-id="32171-129">Threshold rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32171-130">-TimeWindowRule</span><span class="sxs-lookup"><span data-stu-id="32171-130">-TimeWindowRule</span></span>
<span data-ttu-id="32171-131">Regole della finestra ora.</span><span class="sxs-lookup"><span data-stu-id="32171-131">Time window rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]
Parameter Sets: ResourceIdLevelResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]
Parameter Sets: InputObject, ResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32171-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="32171-132">-Confirm</span></span>
<span data-ttu-id="32171-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32171-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32171-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32171-134">-WhatIf</span></span>
<span data-ttu-id="32171-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32171-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32171-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32171-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32171-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32171-137">CommonParameters</span></span>
<span data-ttu-id="32171-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32171-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32171-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32171-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32171-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32171-140">INPUTS</span></span>

### <span data-ttu-id="32171-141">Microsoft. Azure. Commands. Security. Models. DeviceSecurityGroups. PSThresholdCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="32171-141">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSThresholdCustomAlertRule[]</span></span>

### <span data-ttu-id="32171-142">Microsoft. Azure. Commands. Security. Models. DeviceSecurityGroups. PSTimeWindowCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="32171-142">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSTimeWindowCustomAlertRule[]</span></span>

### <span data-ttu-id="32171-143">Microsoft. Azure. Commands. Security. Models. DeviceSecurityGroups. PSAllowlistCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="32171-143">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSAllowlistCustomAlertRule[]</span></span>

### <span data-ttu-id="32171-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule []</span><span class="sxs-lookup"><span data-stu-id="32171-144">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDenylistCustomAlertRule[]</span></span>

### <span data-ttu-id="32171-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="32171-145">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

### <span data-ttu-id="32171-146">System. String</span><span class="sxs-lookup"><span data-stu-id="32171-146">System.String</span></span>

## <span data-ttu-id="32171-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32171-147">OUTPUTS</span></span>

### <span data-ttu-id="32171-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="32171-148">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="32171-149">Note</span><span class="sxs-lookup"><span data-stu-id="32171-149">NOTES</span></span>

## <span data-ttu-id="32171-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32171-150">RELATED LINKS</span></span>
