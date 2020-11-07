---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/select-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Select-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Select-AzContext.md
ms.openlocfilehash: c38be0f49e899379d93fc39a2531bcef219c3c29
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860170"
---
# <span data-ttu-id="c2865-101">Select-AzContext</span><span class="sxs-lookup"><span data-stu-id="c2865-101">Select-AzContext</span></span>

## <span data-ttu-id="c2865-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2865-102">SYNOPSIS</span></span>
<span data-ttu-id="c2865-103">Selezionare un abbonamento e un account per la destinazione nei cmdlet di PowerShell di Azure</span><span class="sxs-lookup"><span data-stu-id="c2865-103">Select a subscription and account to target in Azure PowerShell cmdlets</span></span>

## <span data-ttu-id="c2865-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2865-104">SYNTAX</span></span>

### <span data-ttu-id="c2865-105">SelectByInputObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c2865-105">SelectByInputObject (Default)</span></span>
```
Select-AzContext -InputObject <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2865-106">SelectByName</span><span class="sxs-lookup"><span data-stu-id="c2865-106">SelectByName</span></span>
```
Select-AzContext [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="c2865-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2865-107">DESCRIPTION</span></span>
<span data-ttu-id="c2865-108">Selezionare un abbonamento a destinazione (o account o tenant) nei cmdlet di PowerShell di Azure.</span><span class="sxs-lookup"><span data-stu-id="c2865-108">Select a  subscription to target (or account or tenant) in Azure PowerShell cmdlets.</span></span>  <span data-ttu-id="c2865-109">Dopo questo cmdlet, i futuri cmdlet verranno destinati al contesto selezionato.</span><span class="sxs-lookup"><span data-stu-id="c2865-109">After this cmdlet, future cmdlets will target the selected context.</span></span>

## <span data-ttu-id="c2865-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2865-110">EXAMPLES</span></span>

### <span data-ttu-id="c2865-111">Esempio 1: destinazione di un contesto denominato</span><span class="sxs-lookup"><span data-stu-id="c2865-111">Example 1 : Target a named context</span></span>
```
PS C:\> Select-AzContext "Work"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="c2865-112">I futuri cmdlet di PowerShell di Azure di destinazione per l'account, il tenant e l'abbonamento nel contesto "lavoro".</span><span class="sxs-lookup"><span data-stu-id="c2865-112">Target future Azure PowerShell cmdlets at the account, tenant, and subscription in the 'Work' context.</span></span>

## <span data-ttu-id="c2865-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2865-113">PARAMETERS</span></span>

### <span data-ttu-id="c2865-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2865-114">-DefaultProfile</span></span>
<span data-ttu-id="c2865-115">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c2865-115">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2865-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2865-116">-InputObject</span></span>
<span data-ttu-id="c2865-117">Oggetto context, in genere passato alla pipeline.</span><span class="sxs-lookup"><span data-stu-id="c2865-117">A context object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: SelectByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2865-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="c2865-118">-Name</span></span>
<span data-ttu-id="c2865-119">Nome del contesto</span><span class="sxs-lookup"><span data-stu-id="c2865-119">The name of the context</span></span>

```yaml
Type: System.String
Parameter Sets: SelectByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2865-120">-Ambito</span><span class="sxs-lookup"><span data-stu-id="c2865-120">-Scope</span></span>
<span data-ttu-id="c2865-121">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente</span><span class="sxs-lookup"><span data-stu-id="c2865-121">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2865-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c2865-122">-Confirm</span></span>
<span data-ttu-id="c2865-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2865-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2865-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2865-124">-WhatIf</span></span>
<span data-ttu-id="c2865-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2865-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2865-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c2865-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2865-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2865-127">CommonParameters</span></span>
<span data-ttu-id="c2865-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2865-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2865-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2865-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2865-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2865-130">INPUTS</span></span>

### <span data-ttu-id="c2865-131">Microsoft. Azure. Commands. profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="c2865-131">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="c2865-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2865-132">OUTPUTS</span></span>

### <span data-ttu-id="c2865-133">Microsoft. Azure. Commands. profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="c2865-133">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="c2865-134">Note</span><span class="sxs-lookup"><span data-stu-id="c2865-134">NOTES</span></span>

## <span data-ttu-id="c2865-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2865-135">RELATED LINKS</span></span>
