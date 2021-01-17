---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzDeviceSecurityGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzDeviceSecurityGroup.md
ms.openlocfilehash: 3d43407c9f7e58d7a5d29ef56412f6d38c5c957b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486408"
---
# <span data-ttu-id="12f15-101">Get-AzDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="12f15-101">Get-AzDeviceSecurityGroup</span></span>

## <span data-ttu-id="12f15-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12f15-102">SYNOPSIS</span></span>
<span data-ttu-id="12f15-103">Ottenere un gruppo di sicurezza del dispositivo (sicurezza Hub molto)</span><span class="sxs-lookup"><span data-stu-id="12f15-103">Get device security group (IoT Hub security)</span></span>

## <span data-ttu-id="12f15-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12f15-104">SYNTAX</span></span>

### <span data-ttu-id="12f15-105">ResourceIdScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="12f15-105">ResourceIdScope (Default)</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="12f15-106">ResourceIdLevelResource</span><span class="sxs-lookup"><span data-stu-id="12f15-106">ResourceIdLevelResource</span></span>
```
Get-AzDeviceSecurityGroup -HubResourceId <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="12f15-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12f15-107">DESCRIPTION</span></span>
<span data-ttu-id="12f15-108">Il cmdlet Get-AzDeviceSecurityGroup restituisce un gruppo di sicurezza dei dispositivi definito nella soluzione di sicurezza degli Stati</span><span class="sxs-lookup"><span data-stu-id="12f15-108">The Get-AzDeviceSecurityGroup cmdlet returns a device security group defined in iot security solution</span></span>

## <span data-ttu-id="12f15-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12f15-109">EXAMPLES</span></span>

### <span data-ttu-id="12f15-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="12f15-110">Example 1</span></span>
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

<span data-ttu-id="12f15-111">Ottenere il gruppo di sicurezza dei dispositivi "MySecurityGroup" nell'hub degli molto con l'ID risorse "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="12f15-111">Get device security group "MySecurityGroup" in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

### <span data-ttu-id="12f15-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="12f15-112">Example 2</span></span>
```powershell
PS C:\> Get-AzDeviceSecurityGroup -HubResourceId "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub" 

Array of security group items like the item returned in example 1
```

<span data-ttu-id="12f15-113">Ottenere un elenco di gruppi di sicurezza dei dispositivi nell'hub degli molto con l'ID risorse "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span><span class="sxs-lookup"><span data-stu-id="12f15-113">Get list of device security group in IoT Hub with reasource Id "/subscriptions/XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Devices/IotHubs/MyHub"</span></span>

## <span data-ttu-id="12f15-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12f15-114">PARAMETERS</span></span>

### <span data-ttu-id="12f15-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12f15-115">-DefaultProfile</span></span>
<span data-ttu-id="12f15-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12f15-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12f15-117">-HubResourceId</span><span class="sxs-lookup"><span data-stu-id="12f15-117">-HubResourceId</span></span>
<span data-ttu-id="12f15-118">ID della risorsa di sicurezza a cui si vuole richiamare il comando.</span><span class="sxs-lookup"><span data-stu-id="12f15-118">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="12f15-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="12f15-119">-Name</span></span>
<span data-ttu-id="12f15-120">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="12f15-120">Resource name.</span></span>

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

### <span data-ttu-id="12f15-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12f15-121">CommonParameters</span></span>
<span data-ttu-id="12f15-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12f15-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12f15-123">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12f15-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12f15-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12f15-124">INPUTS</span></span>

### <span data-ttu-id="12f15-125">Nessuno</span><span class="sxs-lookup"><span data-stu-id="12f15-125">None</span></span>

## <span data-ttu-id="12f15-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12f15-126">OUTPUTS</span></span>

### <span data-ttu-id="12f15-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="12f15-127">Microsoft.Azure.Commands.Security.Models.DeviceSecurityGroups.PSDeviceSecurityGroup</span></span>

## <span data-ttu-id="12f15-128">Note</span><span class="sxs-lookup"><span data-stu-id="12f15-128">NOTES</span></span>

## <span data-ttu-id="12f15-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12f15-129">RELATED LINKS</span></span>
