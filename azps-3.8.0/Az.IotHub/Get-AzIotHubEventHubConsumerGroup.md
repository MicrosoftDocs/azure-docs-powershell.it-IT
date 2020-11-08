---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubEventHubConsumerGroup.md
ms.openlocfilehash: dc401fc74aff737b92cfe7164c19862678a3e1c6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020947"
---
# <span data-ttu-id="d78f4-101">Get-AzIotHubEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="d78f4-101">Get-AzIotHubEventHubConsumerGroup</span></span>

## <span data-ttu-id="d78f4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d78f4-102">SYNOPSIS</span></span>
<span data-ttu-id="d78f4-103">Ottiene tutte le consumergroups eventhub.</span><span class="sxs-lookup"><span data-stu-id="d78f4-103">Gets all the eventhub consumergroups.</span></span>

## <span data-ttu-id="d78f4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d78f4-104">SYNTAX</span></span>

```
Get-AzIotHubEventHubConsumerGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d78f4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d78f4-105">DESCRIPTION</span></span>
<span data-ttu-id="d78f4-106">Ottiene tutte le consumergroups eventhub per i diversi EventHubs usati da IotHub.</span><span class="sxs-lookup"><span data-stu-id="d78f4-106">Gets all the eventhub consumergroups for the different EventHubs used by IotHub.</span></span>

## <span data-ttu-id="d78f4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d78f4-107">EXAMPLES</span></span>

### <span data-ttu-id="d78f4-108">L'esempio 1 restituisce tutte le consumergroups eventhub per la eventhub di telemetria</span><span class="sxs-lookup"><span data-stu-id="d78f4-108">Example 1 Gets all the eventhub consumergroups for the telemetry eventhub</span></span>
```
PS C:\> Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

<span data-ttu-id="d78f4-109">Ottiene tutte le consumergroups eventhub per il eventhub di telemetria per il iothub denominato myiothub</span><span class="sxs-lookup"><span data-stu-id="d78f4-109">Gets all the eventhub consumergroups for the telemetry eventhub for the iothub named myiothub</span></span>

## <span data-ttu-id="d78f4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d78f4-110">PARAMETERS</span></span>

### <span data-ttu-id="d78f4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d78f4-111">-DefaultProfile</span></span>
<span data-ttu-id="d78f4-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d78f4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d78f4-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="d78f4-113">-Name</span></span>
<span data-ttu-id="d78f4-114">Nome del IotHub</span><span class="sxs-lookup"><span data-stu-id="d78f4-114">Name of the IotHub</span></span>

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

### <span data-ttu-id="d78f4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d78f4-115">-ResourceGroupName</span></span>
<span data-ttu-id="d78f4-116">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="d78f4-116">Resource Group Name</span></span>

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

### <span data-ttu-id="d78f4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d78f4-117">CommonParameters</span></span>
<span data-ttu-id="d78f4-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d78f4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d78f4-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d78f4-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d78f4-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d78f4-120">INPUTS</span></span>

### <span data-ttu-id="d78f4-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d78f4-121">System.String</span></span>

## <span data-ttu-id="d78f4-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d78f4-122">OUTPUTS</span></span>

### <span data-ttu-id="d78f4-123">Microsoft. Azure. Commands. Management. IotHub. Models. PSEventHubConsumerGroupInfo</span><span class="sxs-lookup"><span data-stu-id="d78f4-123">Microsoft.Azure.Commands.Management.IotHub.Models.PSEventHubConsumerGroupInfo</span></span>

## <span data-ttu-id="d78f4-124">Note</span><span class="sxs-lookup"><span data-stu-id="d78f4-124">NOTES</span></span>

## <span data-ttu-id="d78f4-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d78f4-125">RELATED LINKS</span></span>
