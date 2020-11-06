---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 93efa23e802c3470d1bd1470cadd0f070cc34422
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512963"
---
# <span data-ttu-id="e3304-101">Remove-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e3304-101">Remove-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="e3304-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e3304-102">SYNOPSIS</span></span>
<span data-ttu-id="e3304-103">Rimuove la regola di autorizzazione di una coda dallo spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="e3304-103">Removes the authorization rule of a queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e3304-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3304-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3304-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3304-105">DESCRIPTION</span></span>
<span data-ttu-id="e3304-106">Il cmdlet **Remove-AzureRmServiceBusQueueAuthorizationRule** rimuove la regola di autorizzazione di una coda dallo spazio dei nomi Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="e3304-106">The **Remove-AzureRmServiceBusQueueAuthorizationRule** cmdlet removes the authorization rule of a queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="e3304-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3304-107">EXAMPLES</span></span>

### <span data-ttu-id="e3304-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e3304-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="e3304-109">Rimuove la regola `SBAuthoRule1` di autorizzazione della coda `SB-Queue_exampl1` dallo spazio dei nomi `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="e3304-109">Removes the authorization rule `SBAuthoRule1` of the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="e3304-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e3304-110">PARAMETERS</span></span>

### <span data-ttu-id="e3304-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e3304-111">-ResourceGroup</span></span>
<span data-ttu-id="e3304-112">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e3304-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="e3304-113">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e3304-113">-Confirm</span></span>
<span data-ttu-id="e3304-114">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3304-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3304-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3304-115">-WhatIf</span></span>
<span data-ttu-id="e3304-116">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3304-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3304-117">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e3304-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3304-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3304-118">-DefaultProfile</span></span>
<span data-ttu-id="e3304-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3304-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3304-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="e3304-120">-Name</span></span>
<span data-ttu-id="e3304-121">Nome AuthorizationRule coda.</span><span class="sxs-lookup"><span data-stu-id="e3304-121">Queue AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3304-122">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e3304-122">-Namespace</span></span>
<span data-ttu-id="e3304-123">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="e3304-123">Namespace Name.</span></span>

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

### <span data-ttu-id="e3304-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="e3304-124">-Queue</span></span>
<span data-ttu-id="e3304-125">Nome coda.</span><span class="sxs-lookup"><span data-stu-id="e3304-125">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3304-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3304-126">CommonParameters</span></span>
<span data-ttu-id="e3304-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3304-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3304-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3304-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3304-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e3304-129">INPUTS</span></span>

### <span data-ttu-id="e3304-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e3304-130">-ResourceGroup</span></span>
 <span data-ttu-id="e3304-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e3304-131">System.String</span></span>

### <span data-ttu-id="e3304-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="e3304-132">-NamespaceName</span></span>
 <span data-ttu-id="e3304-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e3304-133">System.String</span></span>

### <span data-ttu-id="e3304-134">-QueueName</span><span class="sxs-lookup"><span data-stu-id="e3304-134">-QueueName</span></span>
 <span data-ttu-id="e3304-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e3304-135">System.String</span></span>

### <span data-ttu-id="e3304-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="e3304-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="e3304-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e3304-137">System.String</span></span>

## <span data-ttu-id="e3304-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3304-138">OUTPUTS</span></span>

### <span data-ttu-id="e3304-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="e3304-139">System.Object</span></span>

## <span data-ttu-id="e3304-140">Note</span><span class="sxs-lookup"><span data-stu-id="e3304-140">NOTES</span></span>

## <span data-ttu-id="e3304-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3304-141">RELATED LINKS</span></span>

