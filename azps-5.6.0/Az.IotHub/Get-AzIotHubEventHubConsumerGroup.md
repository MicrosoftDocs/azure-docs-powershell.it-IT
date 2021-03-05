---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: f4a722ad01cf354cc49b3441c03ec8aaca2e5e57
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988005"
---
# <span data-ttu-id="12ac8-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="12ac8-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="12ac8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12ac8-102">SYNOPSIS</span></span>
<span data-ttu-id="12ac8-103">Ottiene tutti i gruppi consumer di eventhub.</span><span class="sxs-lookup"><span data-stu-id="12ac8-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="12ac8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12ac8-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="12ac8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="12ac8-105">DESCRIPTION</span></span>
<span data-ttu-id="12ac8-106">Ottiene tutti i gruppi consumer di eventhub per i diversi EventHub usati da IotHub.</span><span class="sxs-lookup"><span data-stu-id="12ac8-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="12ac8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12ac8-107">EXAMPLES</span></span>

### <span data-ttu-id="12ac8-108">Esempio 1 ottiene tutti i gruppi consumer di eventhub per il eventhub di telemetria</span><span class="sxs-lookup"><span data-stu-id="12ac8-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="12ac8-109">Ottiene tutti i gruppi consumer di eventhub per la telemetria eventhub per il iothub denominato myiothub</span><span class="sxs-lookup"><span data-stu-id="12ac8-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="12ac8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12ac8-110">PARAMETERS</span></span>

### <span data-ttu-id="12ac8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12ac8-111">-DefaultProfile</span></span>
<span data-ttu-id="12ac8-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="12ac8-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12ac8-113">-Name</span><span class="sxs-lookup"><span data-stu-id="12ac8-113">-Name</span></span>
<span data-ttu-id="12ac8-114">Nome del file IotHub</span><span class="sxs-lookup"><span data-stu-id="12ac8-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="12ac8-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12ac8-115">-ResourceGroupName</span></span>
<span data-ttu-id="12ac8-116">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="12ac8-116">Resource Group Name</span></span>

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

### <span data-ttu-id="12ac8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12ac8-117">CommonParameters</span></span>
<span data-ttu-id="12ac8-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12ac8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12ac8-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12ac8-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12ac8-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="12ac8-120">INPUTS</span></span>

### <span data-ttu-id="12ac8-121">System.String</span><span class="sxs-lookup"><span data-stu-id="12ac8-121">System.String</span></span>

## <span data-ttu-id="12ac8-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12ac8-122">OUTPUTS</span></span>

### <span data-ttu-id="12ac8-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="12ac8-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="12ac8-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="12ac8-124">NOTES</span></span>

## <span data-ttu-id="12ac8-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12ac8-125">RELATED LINKS</span></span>
