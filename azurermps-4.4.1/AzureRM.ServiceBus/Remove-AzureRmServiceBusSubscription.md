---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
ms.openlocfilehash: c3d4ca61f0bbdc5dcea2eb41a9da0f5de1112719
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512955"
---
# <span data-ttu-id="187b0-101">Remove-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="187b0-101">Remove-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="187b0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="187b0-102">SYNOPSIS</span></span>
<span data-ttu-id="187b0-103">Rimuove la sottoscrizione a un argomento dallo spazio dei nomi di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="187b0-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="187b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="187b0-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="187b0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="187b0-105">DESCRIPTION</span></span>
<span data-ttu-id="187b0-106">Il cmdlet **Remove-AzureRmServiceBusSubscription** rimuove la sottoscrizione a un argomento dallo spazio dei nomi di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="187b0-106">The **Remove-AzureRmServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="187b0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="187b0-107">EXAMPLES</span></span>

### <span data-ttu-id="187b0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="187b0-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="187b0-109">Rimuove la sottoscrizione `SB-TopicSubscription-Example1` all'argomento `SB-Topic_exampl1` nello spazio dei nomi Service Bus specificato `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="187b0-109">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="187b0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="187b0-110">PARAMETERS</span></span>

### <span data-ttu-id="187b0-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="187b0-111">-Confirm</span></span>
<span data-ttu-id="187b0-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="187b0-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187b0-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="187b0-113">-WhatIf</span></span>
<span data-ttu-id="187b0-114">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="187b0-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="187b0-115">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="187b0-115">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187b0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="187b0-116">-DefaultProfile</span></span>
<span data-ttu-id="187b0-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="187b0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="187b0-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="187b0-118">-Name</span></span>
<span data-ttu-id="187b0-119">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="187b0-119">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="187b0-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="187b0-120">-Namespace</span></span>
<span data-ttu-id="187b0-121">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="187b0-121">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="187b0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="187b0-122">-ResourceGroupName</span></span>
<span data-ttu-id="187b0-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="187b0-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="187b0-124">-Topic</span><span class="sxs-lookup"><span data-stu-id="187b0-124">-Topic</span></span>
<span data-ttu-id="187b0-125">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="187b0-125">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="187b0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="187b0-126">CommonParameters</span></span>
<span data-ttu-id="187b0-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="187b0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="187b0-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="187b0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="187b0-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="187b0-129">INPUTS</span></span>

### <span data-ttu-id="187b0-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="187b0-130">-ResourceGroup</span></span>
 <span data-ttu-id="187b0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="187b0-131">System.String</span></span>

### <span data-ttu-id="187b0-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="187b0-132">-NamespaceName</span></span>
 <span data-ttu-id="187b0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="187b0-133">System.String</span></span>

### <span data-ttu-id="187b0-134">-TopicName</span><span class="sxs-lookup"><span data-stu-id="187b0-134">-TopicName</span></span>
 <span data-ttu-id="187b0-135">System. String</span><span class="sxs-lookup"><span data-stu-id="187b0-135">System.String</span></span>

### <span data-ttu-id="187b0-136">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="187b0-136">-SubscriptionName</span></span>
 <span data-ttu-id="187b0-137">System. String</span><span class="sxs-lookup"><span data-stu-id="187b0-137">System.String</span></span>

## <span data-ttu-id="187b0-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="187b0-138">OUTPUTS</span></span>

### <span data-ttu-id="187b0-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="187b0-139">System.Boolean</span></span>

## <span data-ttu-id="187b0-140">Note</span><span class="sxs-lookup"><span data-stu-id="187b0-140">NOTES</span></span>

## <span data-ttu-id="187b0-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="187b0-141">RELATED LINKS</span></span>

