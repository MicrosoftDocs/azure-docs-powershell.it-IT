---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/powershell/module/az.subscription/remove-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
ms.openlocfilehash: 2acca5ede1d6ef7e4a3767b87053fb356555993d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971646"
---
# <span data-ttu-id="bedc8-101">Remove-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="bedc8-101">Remove-AzSubscriptionAlias</span></span>

## <span data-ttu-id="bedc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bedc8-102">SYNOPSIS</span></span>
<span data-ttu-id="bedc8-103">Elimina l'alias dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="bedc8-103">Deletes the subscription alias</span></span>

## <span data-ttu-id="bedc8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bedc8-104">SYNTAX</span></span>

```
Remove-AzSubscriptionAlias -AliasName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bedc8-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bedc8-105">DESCRIPTION</span></span>
<span data-ttu-id="bedc8-106">Il cmdlet **Remove-AzSubscriptionAlias** rimuove l'alias di abbonamento</span><span class="sxs-lookup"><span data-stu-id="bedc8-106">The **Remove-AzSubscriptionAlias** cmdlet removes the subscription alias</span></span>

## <span data-ttu-id="bedc8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bedc8-107">EXAMPLES</span></span>

### <span data-ttu-id="bedc8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="bedc8-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="bedc8-109">Elimina l'alias dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="bedc8-109">Deletes the subscription alias</span></span>

## <span data-ttu-id="bedc8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bedc8-110">PARAMETERS</span></span>

### <span data-ttu-id="bedc8-111">-AliasName</span><span class="sxs-lookup"><span data-stu-id="bedc8-111">-AliasName</span></span>
<span data-ttu-id="bedc8-112">Alias per l'abbonamento</span><span class="sxs-lookup"><span data-stu-id="bedc8-112">Alias for the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bedc8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bedc8-113">-AsJob</span></span>
<span data-ttu-id="bedc8-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="bedc8-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bedc8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bedc8-115">-DefaultProfile</span></span>
<span data-ttu-id="bedc8-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bedc8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bedc8-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bedc8-117">-Confirm</span></span>
<span data-ttu-id="bedc8-118">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bedc8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bedc8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bedc8-119">-WhatIf</span></span>
<span data-ttu-id="bedc8-120">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bedc8-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bedc8-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bedc8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bedc8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bedc8-122">CommonParameters</span></span>
<span data-ttu-id="bedc8-123">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bedc8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bedc8-124">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bedc8-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bedc8-125">INPUT</span><span class="sxs-lookup"><span data-stu-id="bedc8-125">INPUTS</span></span>

### <span data-ttu-id="bedc8-126">Nessuno</span><span class="sxs-lookup"><span data-stu-id="bedc8-126">None</span></span>

## <span data-ttu-id="bedc8-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bedc8-127">OUTPUTS</span></span>

### <span data-ttu-id="bedc8-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="bedc8-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="bedc8-129">NOTE</span><span class="sxs-lookup"><span data-stu-id="bedc8-129">NOTES</span></span>

## <span data-ttu-id="bedc8-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bedc8-130">RELATED LINKS</span></span>
