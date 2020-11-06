---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 08f7f33138ddf9d5226cfc93f263fdec65de3388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512971"
---
# <span data-ttu-id="9f546-101">Remove-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9f546-101">Remove-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="9f546-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9f546-102">SYNOPSIS</span></span>
<span data-ttu-id="9f546-103">Rimuove la regola di autorizzazione di uno spazio dei nomi Service Bus dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="9f546-103">Removes the authorization rule of a Service Bus namespace from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f546-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9f546-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroupName <String> -Namespace <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f546-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9f546-105">DESCRIPTION</span></span>
<span data-ttu-id="9f546-106">Il cmdlet **Remove-AzureRmServiceBusNamespaceAuthorizationRule** rimuove la regola di autorizzazione di uno spazio dei nomi Service Bus per il gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="9f546-106">The **Remove-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace for the specified resource group.</span></span>

## <span data-ttu-id="9f546-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9f546-107">EXAMPLES</span></span>

### <span data-ttu-id="9f546-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9f546-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="9f546-109">Rimuove la regola `SBAuthoRule1` di autorizzazione dello spazio dei nomi `SB-Example1` dal gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="9f546-109">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

## <span data-ttu-id="9f546-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9f546-110">PARAMETERS</span></span>

### <span data-ttu-id="9f546-111">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9f546-111">-Confirm</span></span>
<span data-ttu-id="9f546-112">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f546-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f546-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f546-113">-WhatIf</span></span>
<span data-ttu-id="9f546-114">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f546-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f546-115">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9f546-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f546-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f546-116">-DefaultProfile</span></span>
<span data-ttu-id="9f546-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9f546-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9f546-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="9f546-118">-Name</span></span>
<span data-ttu-id="9f546-119">Nome AuthorizationRule dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="9f546-119">Namespace AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="9f546-120">-Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="9f546-120">-Namespace</span></span>
<span data-ttu-id="9f546-121">Nome dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="9f546-121">Namespace Name.</span></span>

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

### <span data-ttu-id="9f546-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f546-122">-ResourceGroupName</span></span>
<span data-ttu-id="9f546-123">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="9f546-123">The name of the resource group</span></span>

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

### <span data-ttu-id="9f546-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f546-124">CommonParameters</span></span>
<span data-ttu-id="9f546-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f546-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f546-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f546-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f546-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9f546-127">INPUTS</span></span>

### <span data-ttu-id="9f546-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9f546-128">-ResourceGroup</span></span>
 <span data-ttu-id="9f546-129">System. String</span><span class="sxs-lookup"><span data-stu-id="9f546-129">System.String</span></span>

### <span data-ttu-id="9f546-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="9f546-130">-NamespaceName</span></span>
 <span data-ttu-id="9f546-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9f546-131">System.String</span></span>

### <span data-ttu-id="9f546-132">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="9f546-132">-AuthorizationRuleName</span></span>
 <span data-ttu-id="9f546-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9f546-133">System.String</span></span>

## <span data-ttu-id="9f546-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9f546-134">OUTPUTS</span></span>

### <span data-ttu-id="9f546-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9f546-135">System.Boolean</span></span>

## <span data-ttu-id="9f546-136">Note</span><span class="sxs-lookup"><span data-stu-id="9f546-136">NOTES</span></span>

## <span data-ttu-id="9f546-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9f546-137">RELATED LINKS</span></span>

