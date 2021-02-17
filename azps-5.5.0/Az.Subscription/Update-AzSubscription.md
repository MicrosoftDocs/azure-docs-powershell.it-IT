---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/update-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
ms.openlocfilehash: 77e7904a83b7d14fac1379532a619547888d5542
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182854"
---
# <span data-ttu-id="fef37-101">Update-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="fef37-101">Update-AzSubscription</span></span>

## <span data-ttu-id="fef37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fef37-102">SYNOPSIS</span></span>
<span data-ttu-id="fef37-103">Aggiorna una sottoscrizione di Azure</span><span class="sxs-lookup"><span data-stu-id="fef37-103">Updates an Azure Subscription</span></span>

## <span data-ttu-id="fef37-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fef37-104">SYNTAX</span></span>

```
Update-AzSubscription -SubscriptionId <String> -Action <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fef37-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fef37-105">DESCRIPTION</span></span>
<span data-ttu-id="fef37-106">Il cmdlet **Update-AzSubscription** aggiorna una sottoscrizione di Azure</span><span class="sxs-lookup"><span data-stu-id="fef37-106">The **Update-AzSubscription** cmdlet updates an Azure subscription</span></span>

## <span data-ttu-id="fef37-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fef37-107">EXAMPLES</span></span>

### <span data-ttu-id="fef37-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fef37-108">Example 1</span></span>
```powershell
PS C:\> Update-AzSubscription -SubscriptionId "86869d42-1782-4337-98b0-c905fb937d46" -Action "Cancel"

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="fef37-109">Aggiorna l'abbonamento</span><span class="sxs-lookup"><span data-stu-id="fef37-109">Updates the subscription</span></span>

## <span data-ttu-id="fef37-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fef37-110">PARAMETERS</span></span>

### <span data-ttu-id="fef37-111">-Action</span><span class="sxs-lookup"><span data-stu-id="fef37-111">-Action</span></span>
<span data-ttu-id="fef37-112">Azione da eseguire sull'abbonamento</span><span class="sxs-lookup"><span data-stu-id="fef37-112">Action to perform on subscription</span></span>

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

### <span data-ttu-id="fef37-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fef37-113">-AsJob</span></span>
<span data-ttu-id="fef37-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="fef37-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fef37-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fef37-115">-DefaultProfile</span></span>
<span data-ttu-id="fef37-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fef37-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fef37-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fef37-117">-Name</span></span>
<span data-ttu-id="fef37-118">Nome dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="fef37-118">Name of the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fef37-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fef37-119">-SubscriptionId</span></span>
<span data-ttu-id="fef37-120">ID abbonamento da aggiornare</span><span class="sxs-lookup"><span data-stu-id="fef37-120">Subscription Id to update</span></span>

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

### <span data-ttu-id="fef37-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fef37-121">-Confirm</span></span>
<span data-ttu-id="fef37-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fef37-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fef37-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fef37-123">-WhatIf</span></span>
<span data-ttu-id="fef37-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fef37-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fef37-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fef37-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fef37-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fef37-126">CommonParameters</span></span>
<span data-ttu-id="fef37-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fef37-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fef37-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fef37-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fef37-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="fef37-129">INPUTS</span></span>

### <span data-ttu-id="fef37-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fef37-130">None</span></span>

## <span data-ttu-id="fef37-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fef37-131">OUTPUTS</span></span>

### <span data-ttu-id="fef37-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="fef37-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="fef37-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="fef37-133">NOTES</span></span>

## <span data-ttu-id="fef37-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fef37-134">RELATED LINKS</span></span>
