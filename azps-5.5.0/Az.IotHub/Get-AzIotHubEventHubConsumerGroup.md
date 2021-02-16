---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: dc401fc74aff737b92cfe7164c19862678a3e1c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185702"
---
# <span data-ttu-id="b89b9-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b89b9-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="b89b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b89b9-102">SYNOPSIS</span></span>
<span data-ttu-id="b89b9-103">Ottiene tutti i gruppi consumer di eventhub.</span><span class="sxs-lookup"><span data-stu-id="b89b9-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="b89b9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b89b9-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b89b9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b89b9-105">DESCRIPTION</span></span>
<span data-ttu-id="b89b9-106">Ottiene tutti i gruppi consumer di eventhub per i diversi EventHub usati da IotHub.</span><span class="sxs-lookup"><span data-stu-id="b89b9-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="b89b9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b89b9-107">EXAMPLES</span></span>

### <span data-ttu-id="b89b9-108">Esempio 1 ottiene tutti i gruppi consumer di eventhub per il eventhub di telemetria</span><span class="sxs-lookup"><span data-stu-id="b89b9-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="b89b9-109">Ottiene tutti i gruppi consumer di eventhub per la telemetria eventhub per il iothub denominato myiothub</span><span class="sxs-lookup"><span data-stu-id="b89b9-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="b89b9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b89b9-110">PARAMETERS</span></span>

### <span data-ttu-id="b89b9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b89b9-111">-DefaultProfile</span></span>
<span data-ttu-id="b89b9-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="b89b9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b89b9-113">-Name</span><span class="sxs-lookup"><span data-stu-id="b89b9-113">-Name</span></span>
<span data-ttu-id="b89b9-114">Nome del file IotHub</span><span class="sxs-lookup"><span data-stu-id="b89b9-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="b89b9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b89b9-115">-ResourceGroupName</span></span>
<span data-ttu-id="b89b9-116">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b89b9-116">Resource Group Name</span></span>

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

### <span data-ttu-id="b89b9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b89b9-117">CommonParameters</span></span>
<span data-ttu-id="b89b9-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b89b9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b89b9-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b89b9-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b89b9-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="b89b9-120">INPUTS</span></span>

### <span data-ttu-id="b89b9-121">System.String</span><span class="sxs-lookup"><span data-stu-id="b89b9-121">System.String</span></span>

## <span data-ttu-id="b89b9-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b89b9-122">OUTPUTS</span></span>

### <span data-ttu-id="b89b9-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="b89b9-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="b89b9-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="b89b9-124">NOTES</span></span>

## <span data-ttu-id="b89b9-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b89b9-125">RELATED LINKS</span></span>
