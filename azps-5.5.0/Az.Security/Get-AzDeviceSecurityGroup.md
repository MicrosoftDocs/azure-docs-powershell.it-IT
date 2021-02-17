---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
ms.openlocfilehash: 3d43407c9f7e58d7a5d29ef56412f6d38c5c957b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197966"
---
# <span data-ttu-id="3417c-101">Get-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3417c-101">Get-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="3417c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3417c-102">SYNOPSIS</span></span>
<span data-ttu-id="3417c-103">Ottenere il gruppo di sicurezza del dispositivo (sicurezza dell'Hub IoT)</span><span class="sxs-lookup"><span data-stu-id="3417c-103">Get device security group (IoT Hub security)</span></span>

## <span data-ttu-id="3417c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3417c-104">SYNTAX</span></span>

### <span data-ttu-id="3417c-105">ResourceIdScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3417c-105">ResourceIdScope (Default)</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3417c-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="3417c-106">ResourceIdLevelResource</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3417c-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3417c-107">DESCRIPTION</span></span>
<span data-ttu-id="3417c-108">Il Get-AzDeviceSecurityGroup cmdlet di sicurezza del dispositivo restituisce un gruppo di sicurezza dei dispositivi definito nella soluzione di sicurezza iot</span><span class="sxs-lookup"><span data-stu-id="3417c-108">The Get-AzDeviceSecurityGroup cmdlet returns a device security group defined in iot security solution</span></span>

## <span data-ttu-id="3417c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3417c-109">EXAMPLES</span></span>

### <span data-ttu-id="3417c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3417c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" -Name "MySecurityGroup" 

Id: "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub/providers/Microsoft.Security/deviceSecurityGroups/MySecurityGroup"
Name: "MySecurityGroup"
Type: "Microsoft.Security/deviceSecurityGroups"
ThresholdRules: []
TimeWindowRules: [
            {
              RuleType: "ActiveConnectionsNotInAllowedRange"
              DisplayName: "Number of active connections is not in allowed range"
              Description: "Get an alert when the number of active connections of a device in the time window is not in the allowed range"
              IsEnabled: false
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT15M"
            }
            {
              RuleType: "AmqpC2DMessagesNotInAllowedRange"
              DisplayName: "Number of cloud to device messages (AMQP protocol) is not in allowed range"
              Description: "Get an alert when the number of cloud to device messages (AMQP protocol) in the time window is not in the allowed range"
              IsEnabled: false
              MinThreshold: 0
              MaxThreshold: 0
              TimeWindowSize: "PT15M"
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

<span data-ttu-id="3417c-111">Ottenere il gruppo di sicurezza "MySecurityGroup" nell'hub IoT con il nuovo ID di origine "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="3417c-111">Get device security group "MySecurityGroup" in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

### <span data-ttu-id="3417c-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3417c-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 

Array of security group items like the item returned in example 1
```

<span data-ttu-id="3417c-113">Ottenere l'elenco del gruppo di sicurezza dei dispositivi nell'hub IoT con id reasource "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="3417c-113">Get list of device security group in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="3417c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3417c-114">PARAMETERS</span></span>

### <span data-ttu-id="3417c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3417c-115">-DefaultProfile</span></span>
<span data-ttu-id="3417c-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3417c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3417c-117">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="3417c-117">-HubResourceId</span></span>
<span data-ttu-id="3417c-118">ID della risorsa di sicurezza su cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="3417c-118">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="3417c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3417c-119">-Name</span></span>
<span data-ttu-id="3417c-120">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="3417c-120">Resource name.</span></span>

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

### <span data-ttu-id="3417c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3417c-121">CommonParameters</span></span>
<span data-ttu-id="3417c-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3417c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3417c-123">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3417c-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3417c-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="3417c-124">INPUTS</span></span>

### <span data-ttu-id="3417c-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3417c-125">None</span></span>

## <span data-ttu-id="3417c-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3417c-126">OUTPUTS</span></span>

### <span data-ttu-id="3417c-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3417c-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="3417c-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="3417c-128">NOTES</span></span>

## <span data-ttu-id="3417c-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3417c-129">RELATED LINKS</span></span>
