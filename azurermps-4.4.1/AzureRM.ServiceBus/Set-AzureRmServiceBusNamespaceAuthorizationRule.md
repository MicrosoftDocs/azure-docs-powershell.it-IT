---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: a56f9b27e19868d22eed94fbcf7717fbe1c68b39
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687978"
---
# <span data-ttu-id="72044-101">Set-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="72044-101">Set-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="72044-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72044-102">SYNOPSIS</span></span>
<span data-ttu-id="72044-103">Aggiorna la descrizione della regola di autorizzazione specificata per lo spazio dei nomi di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="72044-103">Updates the specified authorization rule description for the given Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72044-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72044-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusNamespaceAuthorizationRule [-ResourceGroup] <String> -Namespace <String>
 -InputObj <SharedAccessAuthorizationRuleAttributes> [-Name <String>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72044-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72044-105">DESCRIPTION</span></span>
<span data-ttu-id="72044-106">Il cmdlet **set-AzureRmServiceBusNamespaceAuthorizationRule** aggiorna la descrizione della regola di autorizzazione specificata nello spazio dei nomi di Service Bus specificato.</span><span class="sxs-lookup"><span data-stu-id="72044-106">The **Set-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace.</span></span>

## <span data-ttu-id="72044-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72044-107">EXAMPLES</span></span>

### <span data-ttu-id="72044-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="72044-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="72044-109">Rimuove **Manage** dai diritti di accesso della regola di autorizzazione `AuthoRule1` nello spazio dei nomi `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="72044-109">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

## <span data-ttu-id="72044-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72044-110">PARAMETERS</span></span>

### <span data-ttu-id="72044-111">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="72044-111">-ResourceGroup</span></span>
<span data-ttu-id="72044-112">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="72044-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="72044-113">-Diritti</span><span class="sxs-lookup"><span data-stu-id="72044-113">-Rights</span></span>
<span data-ttu-id="72044-114">Diritti ad esempio @ ("Listen", "Send", "Manage").</span><span class="sxs-lookup"><span data-stu-id="72044-114">Rights; for example @("Listen","Send","Manage").</span></span> <span data-ttu-id="72044-115">Obbligatorio se **AuthruleObj** non è specificato.</span><span class="sxs-lookup"><span data-stu-id="72044-115">Required if **AuthruleObj** is not specified.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72044-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="72044-116">-Confirm</span></span>
<span data-ttu-id="72044-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72044-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72044-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72044-118">-WhatIf</span></span>
<span data-ttu-id="72044-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72044-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72044-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="72044-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72044-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72044-121">-DefaultProfile</span></span>
<span data-ttu-id="72044-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72044-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72044-123">-InputObj</span><span class="sxs-lookup"><span data-stu-id="72044-123">-InputObj</span></span>
<span data-ttu-id="72044-124">Oggetto AuthorizationRule dello spazio dei nomi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="72044-124">ServiceBus NameSpace AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72044-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="72044-125">-Name</span></span>
<span data-ttu-id="72044-126">AuthorizationRule nome-obbligatorio se ' AuthruleObj ' non specificato.</span><span class="sxs-lookup"><span data-stu-id="72044-126">AuthorizationRule Name - Required if 'AuthruleObj' not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72044-127">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="72044-127">-Namespace</span></span>
<span data-ttu-id="72044-128">Nome dello spazio dei nomi ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="72044-128">ServiceBus Namespace Name.</span></span>

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

### <span data-ttu-id="72044-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72044-129">CommonParameters</span></span>
<span data-ttu-id="72044-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72044-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72044-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72044-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72044-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72044-132">INPUTS</span></span>

### <span data-ttu-id="72044-133">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="72044-133">-ResourceGroup</span></span>
 <span data-ttu-id="72044-134">System. String</span><span class="sxs-lookup"><span data-stu-id="72044-134">System.String</span></span>

### <span data-ttu-id="72044-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="72044-135">-NamespaceName</span></span>
 <span data-ttu-id="72044-136">System. String</span><span class="sxs-lookup"><span data-stu-id="72044-136">System.String</span></span>

### <span data-ttu-id="72044-137">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="72044-137">-AuthRuleObj</span></span>
 <span data-ttu-id="72044-138">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="72044-138">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="72044-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72044-139">OUTPUTS</span></span>

### <span data-ttu-id="72044-140">Microsoft. Azure. Commands. ServiceBus. Models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="72044-140">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="72044-141">ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 tipo: Microsoft. ServiceBus/AuthorizationRules Name: AuthoRule1 location: Tags: Rights: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="72044-141">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/AuthorizationRules/AuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : AuthoRule1 Location : Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="72044-142">Note</span><span class="sxs-lookup"><span data-stu-id="72044-142">NOTES</span></span>

## <span data-ttu-id="72044-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72044-143">RELATED LINKS</span></span>

