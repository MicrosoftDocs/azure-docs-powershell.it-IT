---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
ms.openlocfilehash: cb898921b7fdfddddc95fc88d49dade4654c7ad2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94200901"
---
# <span data-ttu-id="270ab-101">Set-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="270ab-101">Set-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="270ab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="270ab-102">SYNOPSIS</span></span>
<span data-ttu-id="270ab-103">Aggiorna il gruppo di utenti hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="270ab-103">Updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="270ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="270ab-104">SYNTAX</span></span>

```
Set-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="270ab-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="270ab-105">DESCRIPTION</span></span>
<span data-ttu-id="270ab-106">Il cmdlet Set-AzEventHubConsumerGroup aggiorna il gruppo di utenti hub eventi specificato.</span><span class="sxs-lookup"><span data-stu-id="270ab-106">The Set-AzEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="270ab-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="270ab-107">EXAMPLES</span></span>

### <span data-ttu-id="270ab-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="270ab-108">Example 1</span></span>
```
PS C:\> Set-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="270ab-109">Imposta i metadati utente del gruppo Consumer \` MyConsumerGroupName \` su "testing".</span><span class="sxs-lookup"><span data-stu-id="270ab-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="270ab-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="270ab-110">PARAMETERS</span></span>

### <span data-ttu-id="270ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="270ab-111">-DefaultProfile</span></span>
<span data-ttu-id="270ab-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="270ab-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="270ab-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="270ab-113">-EventHub</span></span>
<span data-ttu-id="270ab-114">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="270ab-114">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270ab-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="270ab-115">-Name</span></span>
<span data-ttu-id="270ab-116">Nome ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="270ab-116">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270ab-117">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="270ab-117">-Namespace</span></span>
<span data-ttu-id="270ab-118">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="270ab-118">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270ab-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="270ab-119">-ResourceGroupName</span></span>
<span data-ttu-id="270ab-120">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="270ab-120">Resource Group Name</span></span>

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

### <span data-ttu-id="270ab-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="270ab-121">-UserMetadata</span></span>
<span data-ttu-id="270ab-122">Metadati utente per ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="270ab-122">User Metadata for ConsumerGroup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="270ab-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="270ab-123">-Confirm</span></span>
<span data-ttu-id="270ab-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="270ab-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="270ab-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="270ab-125">-WhatIf</span></span>
<span data-ttu-id="270ab-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="270ab-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="270ab-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="270ab-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="270ab-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="270ab-128">CommonParameters</span></span>
<span data-ttu-id="270ab-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="270ab-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="270ab-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="270ab-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="270ab-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="270ab-131">INPUTS</span></span>

### <span data-ttu-id="270ab-132">System. String</span><span class="sxs-lookup"><span data-stu-id="270ab-132">System.String</span></span>

## <span data-ttu-id="270ab-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="270ab-133">OUTPUTS</span></span>

### <span data-ttu-id="270ab-134">Microsoft. Azure. Commands. EventHub. Models. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="270ab-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="270ab-135">Note</span><span class="sxs-lookup"><span data-stu-id="270ab-135">NOTES</span></span>

## <span data-ttu-id="270ab-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="270ab-136">RELATED LINKS</span></span>
