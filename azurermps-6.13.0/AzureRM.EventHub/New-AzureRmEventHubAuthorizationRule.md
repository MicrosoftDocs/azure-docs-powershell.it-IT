---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 63da2be82f8af6339a68eab580c6871b05f2d884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687593"
---
# <span data-ttu-id="b3a1c-101">New-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b3a1c-101">New-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="b3a1c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a1c-103">Crea una nuova regola di autorizzazione Hub eventi per namespace o eventhub.</span><span class="sxs-lookup"><span data-stu-id="b3a1c-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3a1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3a1c-104">SYNTAX</span></span>

### <span data-ttu-id="b3a1c-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b3a1c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3a1c-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b3a1c-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3a1c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3a1c-107">DESCRIPTION</span></span>
<span data-ttu-id="b3a1c-108">Il cmdlet New-AzureRmEventHubAuthorizationRule crea una nuova regola di autorizzazione Hub eventi.</span><span class="sxs-lookup"><span data-stu-id="b3a1c-108">The New-AzureRmEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="b3a1c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3a1c-109">EXAMPLES</span></span>

### <span data-ttu-id="b3a1c-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b3a1c-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="b3a1c-111">Crea una regola \` di autorizzazione MyAuthRuleName \` concedendo i diritti Listen e Send allo spazio dei nomi MyNamespace \` \` , con il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="b3a1c-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b3a1c-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b3a1c-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="b3a1c-113">Crea una regola \` di autorizzazione MyAuthRuleName \` concedendo i diritti di ascolto e invio all'hub dell'evento \` MyEventHubName \` nello spazio dei nomi MyNamespace \` \` , con il gruppo di risorse \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="b3a1c-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b3a1c-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3a1c-114">PARAMETERS</span></span>

### <span data-ttu-id="b3a1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a1c-115">-DefaultProfile</span></span>
<span data-ttu-id="b3a1c-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3a1c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3a1c-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="b3a1c-117">-EventHub</span></span>
<span data-ttu-id="b3a1c-118">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="b3a1c-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a1c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3a1c-119">-Name</span></span>
<span data-ttu-id="b3a1c-120">Nome AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b3a1c-120">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a1c-121">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b3a1c-121">-Namespace</span></span>
<span data-ttu-id="b3a1c-122">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b3a1c-122">Namespace Name</span></span>

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

### <span data-ttu-id="b3a1c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3a1c-123">-ResourceGroupName</span></span>
<span data-ttu-id="b3a1c-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b3a1c-124">Resource Group Name</span></span>

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

### <span data-ttu-id="b3a1c-125">-Diritti</span><span class="sxs-lookup"><span data-stu-id="b3a1c-125">-Rights</span></span>
<span data-ttu-id="b3a1c-126">Diritti, ad esempio "ascolta", "Invia", "Gestisci"</span><span class="sxs-lookup"><span data-stu-id="b3a1c-126">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3a1c-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b3a1c-127">-Confirm</span></span>
<span data-ttu-id="b3a1c-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3a1c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3a1c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3a1c-129">-WhatIf</span></span>
<span data-ttu-id="b3a1c-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3a1c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3a1c-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3a1c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3a1c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a1c-132">CommonParameters</span></span>
<span data-ttu-id="b3a1c-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3a1c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a1c-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3a1c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a1c-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3a1c-135">INPUTS</span></span>

### <span data-ttu-id="b3a1c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b3a1c-136">System.String</span></span>

### <span data-ttu-id="b3a1c-137">System. String []</span><span class="sxs-lookup"><span data-stu-id="b3a1c-137">System.String[]</span></span>

## <span data-ttu-id="b3a1c-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3a1c-138">OUTPUTS</span></span>

### <span data-ttu-id="b3a1c-139">Microsoft. Azure. Commands. EventHub. Models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="b3a1c-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="b3a1c-140">Note</span><span class="sxs-lookup"><span data-stu-id="b3a1c-140">NOTES</span></span>

## <span data-ttu-id="b3a1c-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3a1c-141">RELATED LINKS</span></span>
