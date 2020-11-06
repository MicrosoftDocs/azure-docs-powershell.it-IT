---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusTopic.md
ms.openlocfilehash: 356140c964280634f469dd9b9955adaf62130090
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510312"
---
# <span data-ttu-id="5fa7d-101">Remove-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="5fa7d-101">Remove-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="5fa7d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5fa7d-102">SYNOPSIS</span></span>
<span data-ttu-id="5fa7d-103">Rimuove l'argomento dallo spazio dei nomi di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="5fa7d-103">Removes the topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fa7d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5fa7d-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5fa7d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5fa7d-105">DESCRIPTION</span></span>
<span data-ttu-id="5fa7d-106">Il cmdlet **Remove-AzureRmServiceBusTopic** rimuove l'argomento dallo spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="5fa7d-106">The **Remove-AzureRmServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="5fa7d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5fa7d-107">EXAMPLES</span></span>

### <span data-ttu-id="5fa7d-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5fa7d-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="5fa7d-109">Rimuove l'argomento `SB-Topic_exampl1` dallo spazio dei nomi `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="5fa7d-109">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="5fa7d-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5fa7d-110">PARAMETERS</span></span>

### <span data-ttu-id="5fa7d-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5fa7d-111">-Confirm</span></span>
<span data-ttu-id="5fa7d-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fa7d-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fa7d-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fa7d-113">-WhatIf</span></span>
<span data-ttu-id="5fa7d-114">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5fa7d-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fa7d-115">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5fa7d-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fa7d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fa7d-116">-DefaultProfile</span></span>
<span data-ttu-id="5fa7d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5fa7d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fa7d-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="5fa7d-118">-Name</span></span>
<span data-ttu-id="5fa7d-119">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="5fa7d-119">Topic Name.</span></span>

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

### <span data-ttu-id="5fa7d-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5fa7d-120">-Namespace</span></span>
<span data-ttu-id="5fa7d-121">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="5fa7d-121">Namespace Name.</span></span>

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

### <span data-ttu-id="5fa7d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fa7d-122">-ResourceGroupName</span></span>
<span data-ttu-id="5fa7d-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="5fa7d-123">The name of the resource group</span></span>

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

### <span data-ttu-id="5fa7d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fa7d-124">CommonParameters</span></span>
<span data-ttu-id="5fa7d-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fa7d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fa7d-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fa7d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fa7d-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5fa7d-127">INPUTS</span></span>

### <span data-ttu-id="5fa7d-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5fa7d-128">-ResourceGroup</span></span>
 <span data-ttu-id="5fa7d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5fa7d-129">System.String</span></span>

### <span data-ttu-id="5fa7d-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="5fa7d-130">-NamespaceName</span></span>
 <span data-ttu-id="5fa7d-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5fa7d-131">System.String</span></span>

### <span data-ttu-id="5fa7d-132">-TopicName</span><span class="sxs-lookup"><span data-stu-id="5fa7d-132">-TopicName</span></span>
 <span data-ttu-id="5fa7d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="5fa7d-133">System.String</span></span>

## <span data-ttu-id="5fa7d-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5fa7d-134">OUTPUTS</span></span>

### <span data-ttu-id="5fa7d-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="5fa7d-135">System.Object</span></span>

## <span data-ttu-id="5fa7d-136">Note</span><span class="sxs-lookup"><span data-stu-id="5fa7d-136">NOTES</span></span>

## <span data-ttu-id="5fa7d-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5fa7d-137">RELATED LINKS</span></span>

