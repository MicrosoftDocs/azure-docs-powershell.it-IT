---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusRule.md
ms.openlocfilehash: 08f3fb2654d4c0b64900a4f15bbb7816e6d44c6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517964"
---
# <span data-ttu-id="26cbe-101">Remove-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="26cbe-101">Remove-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="26cbe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="26cbe-102">SYNOPSIS</span></span>
<span data-ttu-id="26cbe-103">Rimuove la regola speficied di un abbonamento specifico.</span><span class="sxs-lookup"><span data-stu-id="26cbe-103">Removes the speficied rule of a given subscription .</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26cbe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="26cbe-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26cbe-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="26cbe-105">DESCRIPTION</span></span>
<span data-ttu-id="26cbe-106">Il cmdlet **Remove-AzureRmServiceBusRule** rimuove la regola di una sottoscrizione di un argomento specifico.</span><span class="sxs-lookup"><span data-stu-id="26cbe-106">The **Remove-AzureRmServiceBusRule** cmdlet removes the rule of a subscription of given topic.</span></span>

## <span data-ttu-id="26cbe-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="26cbe-107">EXAMPLES</span></span>

### <span data-ttu-id="26cbe-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="26cbe-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="26cbe-109">Rimuove la regola `SBRule` di sottoscrizione `SBSubscription` dell'argomento specificato `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="26cbe-109">Removes the rule `SBRule` of subscription `SBSubscription` of specified topic `SBTopic`.</span></span>

## <span data-ttu-id="26cbe-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="26cbe-110">PARAMETERS</span></span>

### <span data-ttu-id="26cbe-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26cbe-111">-DefaultProfile</span></span>
<span data-ttu-id="26cbe-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="26cbe-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26cbe-113">-Force</span><span class="sxs-lookup"><span data-stu-id="26cbe-113">-Force</span></span>
<span data-ttu-id="26cbe-114">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="26cbe-114">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26cbe-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="26cbe-115">-Name</span></span>
<span data-ttu-id="26cbe-116">Nome della regola.</span><span class="sxs-lookup"><span data-stu-id="26cbe-116">Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26cbe-117">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="26cbe-117">-Namespace</span></span>
<span data-ttu-id="26cbe-118">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="26cbe-118">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26cbe-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26cbe-119">-PassThru</span></span>
<span data-ttu-id="26cbe-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="26cbe-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26cbe-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26cbe-121">-ResourceGroupName</span></span>
<span data-ttu-id="26cbe-122">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="26cbe-122">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26cbe-123">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="26cbe-123">-Subscription</span></span>
<span data-ttu-id="26cbe-124">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="26cbe-124">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26cbe-125">-Topic</span><span class="sxs-lookup"><span data-stu-id="26cbe-125">-Topic</span></span>
<span data-ttu-id="26cbe-126">Nome argomento.</span><span class="sxs-lookup"><span data-stu-id="26cbe-126">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26cbe-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="26cbe-127">-Confirm</span></span>
<span data-ttu-id="26cbe-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26cbe-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26cbe-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26cbe-129">-WhatIf</span></span>
<span data-ttu-id="26cbe-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26cbe-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26cbe-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="26cbe-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26cbe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26cbe-132">CommonParameters</span></span>
<span data-ttu-id="26cbe-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26cbe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26cbe-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26cbe-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26cbe-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="26cbe-135">INPUTS</span></span>

### <span data-ttu-id="26cbe-136">System. String</span><span class="sxs-lookup"><span data-stu-id="26cbe-136">System.String</span></span>

## <span data-ttu-id="26cbe-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="26cbe-137">OUTPUTS</span></span>

### <span data-ttu-id="26cbe-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="26cbe-138">System.Boolean</span></span>

## <span data-ttu-id="26cbe-139">Note</span><span class="sxs-lookup"><span data-stu-id="26cbe-139">NOTES</span></span>

## <span data-ttu-id="26cbe-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="26cbe-140">RELATED LINKS</span></span>

