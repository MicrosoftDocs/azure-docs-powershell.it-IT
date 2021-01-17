---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/update-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
ms.openlocfilehash: 77e7904a83b7d14fac1379532a619547888d5542
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367919"
---
# <span data-ttu-id="214a7-101">Update-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="214a7-101">Update-AzSubscription</span></span>

## <span data-ttu-id="214a7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="214a7-102">SYNOPSIS</span></span>
<span data-ttu-id="214a7-103">Aggiorna un abbonamento a Azure</span><span class="sxs-lookup"><span data-stu-id="214a7-103">Updates an Azure Subscription</span></span>

## <span data-ttu-id="214a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="214a7-104">SYNTAX</span></span>

```
Update-AzSubscription -SubscriptionId <String> -Action <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="214a7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="214a7-105">DESCRIPTION</span></span>
<span data-ttu-id="214a7-106">Il cmdlet **Update-AzSubscription** aggiorna un abbonamento a Azure</span><span class="sxs-lookup"><span data-stu-id="214a7-106">The **Update-AzSubscription** cmdlet updates an Azure subscription</span></span>

## <span data-ttu-id="214a7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="214a7-107">EXAMPLES</span></span>

### <span data-ttu-id="214a7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="214a7-108">Example 1</span></span>
```powershell
PS C:\> Update-AzSubscription -SubscriptionId "86869d42-1782-4337-98b0-c905fb937d46" -Action "Cancel"

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled
```

<span data-ttu-id="214a7-109">Aggiorna l'abbonamento</span><span class="sxs-lookup"><span data-stu-id="214a7-109">Updates the subscription</span></span>

## <span data-ttu-id="214a7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="214a7-110">PARAMETERS</span></span>

### <span data-ttu-id="214a7-111">-Azione</span><span class="sxs-lookup"><span data-stu-id="214a7-111">-Action</span></span>
<span data-ttu-id="214a7-112">Azione da eseguire in abbonamento</span><span class="sxs-lookup"><span data-stu-id="214a7-112">Action to perform on subscription</span></span>

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

### <span data-ttu-id="214a7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="214a7-113">-AsJob</span></span>
<span data-ttu-id="214a7-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="214a7-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="214a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="214a7-115">-DefaultProfile</span></span>
<span data-ttu-id="214a7-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="214a7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="214a7-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="214a7-117">-Name</span></span>
<span data-ttu-id="214a7-118">Nome dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="214a7-118">Name of the subscription</span></span>

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

### <span data-ttu-id="214a7-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="214a7-119">-SubscriptionId</span></span>
<span data-ttu-id="214a7-120">ID sottoscrizione da aggiornare</span><span class="sxs-lookup"><span data-stu-id="214a7-120">Subscription Id to update</span></span>

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

### <span data-ttu-id="214a7-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="214a7-121">-Confirm</span></span>
<span data-ttu-id="214a7-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="214a7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="214a7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="214a7-123">-WhatIf</span></span>
<span data-ttu-id="214a7-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="214a7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="214a7-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="214a7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="214a7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="214a7-126">CommonParameters</span></span>
<span data-ttu-id="214a7-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="214a7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="214a7-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="214a7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="214a7-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="214a7-129">INPUTS</span></span>

### <span data-ttu-id="214a7-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="214a7-130">None</span></span>

## <span data-ttu-id="214a7-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="214a7-131">OUTPUTS</span></span>

### <span data-ttu-id="214a7-132">Microsoft. Azure. Commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="214a7-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="214a7-133">Note</span><span class="sxs-lookup"><span data-stu-id="214a7-133">NOTES</span></span>

## <span data-ttu-id="214a7-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="214a7-134">RELATED LINKS</span></span>
