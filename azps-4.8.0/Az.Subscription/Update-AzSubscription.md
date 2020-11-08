---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/update-azsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Update-AzSubscription.md
ms.openlocfilehash: b83d186089558b18cbd511cdc5d0b407a997f635
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189200"
---
# <span data-ttu-id="f9437-101">Update-AzSubscription</span><span class="sxs-lookup"><span data-stu-id="f9437-101">Update-AzSubscription</span></span>

## <span data-ttu-id="f9437-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f9437-102">SYNOPSIS</span></span>
<span data-ttu-id="f9437-103">Aggiorna un abbonamento a Azure</span><span class="sxs-lookup"><span data-stu-id="f9437-103">Updates an Azure Subscription</span></span>

## <span data-ttu-id="f9437-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9437-104">SYNTAX</span></span>

```
Update-AzSubscription -SubscriptionId <String> -Action <String> [-Name <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9437-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9437-105">DESCRIPTION</span></span>
<span data-ttu-id="f9437-106">Il cmdlet **Update-AzSubscription** aggiorna un abbonamento a Azure</span><span class="sxs-lookup"><span data-stu-id="f9437-106">The **Update-AzSubscription** cmdlet updates an Azure subscription</span></span>

## <span data-ttu-id="f9437-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9437-107">EXAMPLES</span></span>

### <span data-ttu-id="f9437-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f9437-108">Example 1</span></span>
```powershell
PS C:\> Update-AzSubscription -SubscriptionId "86869d42-1782-4337-98b0-c905fb937d46" -Action "Cancel"

Name        : My Subscription
Id          : 86869d42-1782-4337-98b0-c905fb937d46
TenantId    : a5dcb057-fd83-4384-9d49-5198004d33a5
State       : Enabled

```
<span data-ttu-id="f9437-109">Aggiorna l'abbonamento</span><span class="sxs-lookup"><span data-stu-id="f9437-109">Updates the subscription</span></span>

## <span data-ttu-id="f9437-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f9437-110">PARAMETERS</span></span>

### <span data-ttu-id="f9437-111">-Azione</span><span class="sxs-lookup"><span data-stu-id="f9437-111">-Action</span></span>
<span data-ttu-id="f9437-112">Azione da eseguire in abbonamento</span><span class="sxs-lookup"><span data-stu-id="f9437-112">Action to perform on subscription</span></span>

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

### <span data-ttu-id="f9437-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9437-113">-AsJob</span></span>
<span data-ttu-id="f9437-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f9437-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9437-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9437-115">-DefaultProfile</span></span>
<span data-ttu-id="f9437-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f9437-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9437-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f9437-117">-Name</span></span>
<span data-ttu-id="f9437-118">Nome dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="f9437-118">Name of the subscription</span></span>

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

### <span data-ttu-id="f9437-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f9437-119">-SubscriptionId</span></span>
<span data-ttu-id="f9437-120">ID sottoscrizione da aggiornare</span><span class="sxs-lookup"><span data-stu-id="f9437-120">Subscription Id to update</span></span>

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

### <span data-ttu-id="f9437-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f9437-121">-Confirm</span></span>
<span data-ttu-id="f9437-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9437-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9437-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9437-123">-WhatIf</span></span>
<span data-ttu-id="f9437-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9437-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9437-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9437-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9437-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9437-126">CommonParameters</span></span>
<span data-ttu-id="f9437-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9437-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9437-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9437-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9437-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f9437-129">INPUTS</span></span>

### <span data-ttu-id="f9437-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f9437-130">None</span></span>

## <span data-ttu-id="f9437-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9437-131">OUTPUTS</span></span>

### <span data-ttu-id="f9437-132">Microsoft. Azure. Commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="f9437-132">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="f9437-133">Note</span><span class="sxs-lookup"><span data-stu-id="f9437-133">NOTES</span></span>

## <span data-ttu-id="f9437-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9437-134">RELATED LINKS</span></span>
