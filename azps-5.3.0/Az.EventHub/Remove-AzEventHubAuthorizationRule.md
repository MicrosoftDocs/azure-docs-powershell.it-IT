---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 91c38686d8621f3bba521d738cc125e4b8473188
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476340"
---
# <span data-ttu-id="b3941-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b3941-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="b3941-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b3941-102">SYNOPSIS</span></span>
<span data-ttu-id="b3941-103">Rimuove la regola di autorizzazione dell'hub eventi specificata.</span><span class="sxs-lookup"><span data-stu-id="b3941-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="b3941-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b3941-104">SYNTAX</span></span>

### <span data-ttu-id="b3941-105">NamespaceAuthorizationRuleSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b3941-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3941-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="b3941-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3941-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3941-107">DESCRIPTION</span></span>
<span data-ttu-id="b3941-108">Il cmdlet Remove-AzEventHubAuthorizationRule rimuove ed elimina la regola di autorizzazione specificata dall'hub dell'evento specificato.</span><span class="sxs-lookup"><span data-stu-id="b3941-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="b3941-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b3941-109">EXAMPLES</span></span>

### <span data-ttu-id="b3941-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b3941-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="b3941-111">Rimuove la regola \` di autorizzazione MyAuthRuleName \` dallo spazio dei nomi MyNamespace \` \` .</span><span class="sxs-lookup"><span data-stu-id="b3941-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="b3941-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b3941-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="b3941-113">Rimuove la regola \` di autorizzazione MyAuthRuleName \` dall'hub dell'evento \` MyEventHubName \` .</span><span class="sxs-lookup"><span data-stu-id="b3941-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="b3941-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b3941-114">PARAMETERS</span></span>

### <span data-ttu-id="b3941-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3941-115">-DefaultProfile</span></span>
<span data-ttu-id="b3941-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b3941-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3941-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="b3941-117">-EventHub</span></span>
<span data-ttu-id="b3941-118">Nome EventHub</span><span class="sxs-lookup"><span data-stu-id="b3941-118">EventHub Name</span></span>

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

### <span data-ttu-id="b3941-119">-Force</span><span class="sxs-lookup"><span data-stu-id="b3941-119">-Force</span></span>
<span data-ttu-id="b3941-120">Non chiedere conferma</span><span class="sxs-lookup"><span data-stu-id="b3941-120">Do not ask for confirmation</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3941-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="b3941-121">-Name</span></span>
<span data-ttu-id="b3941-122">Nome AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="b3941-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="b3941-123">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b3941-123">-Namespace</span></span>
<span data-ttu-id="b3941-124">Nome dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b3941-124">Namespace Name</span></span>

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

### <span data-ttu-id="b3941-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3941-125">-PassThru</span></span>
<span data-ttu-id="b3941-126">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="b3941-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b3941-127">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="b3941-127">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3941-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3941-128">-ResourceGroupName</span></span>
<span data-ttu-id="b3941-129">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="b3941-129">Resource Group Name</span></span>

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

### <span data-ttu-id="b3941-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b3941-130">-Confirm</span></span>
<span data-ttu-id="b3941-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3941-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3941-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3941-132">-WhatIf</span></span>
<span data-ttu-id="b3941-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3941-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3941-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b3941-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3941-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3941-135">CommonParameters</span></span>
<span data-ttu-id="b3941-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3941-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3941-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3941-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3941-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b3941-138">INPUTS</span></span>

### <span data-ttu-id="b3941-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b3941-139">System.String</span></span>

## <span data-ttu-id="b3941-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b3941-140">OUTPUTS</span></span>

### <span data-ttu-id="b3941-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b3941-141">System.Boolean</span></span>

## <span data-ttu-id="b3941-142">Note</span><span class="sxs-lookup"><span data-stu-id="b3941-142">NOTES</span></span>

## <span data-ttu-id="b3941-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b3941-143">RELATED LINKS</span></span>
