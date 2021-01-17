---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
ms.openlocfilehash: 49805dee2bff967da294fda228b5426e2652e209
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476004"
---
# <span data-ttu-id="33574-101">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="33574-101">Set-AzContext</span></span>

## <span data-ttu-id="33574-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="33574-102">SYNOPSIS</span></span>
<span data-ttu-id="33574-103">Imposta il tenant, l'abbonamento e l'ambiente per i cmdlet da usare nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="33574-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="33574-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33574-104">SYNTAX</span></span>

### <span data-ttu-id="33574-105">Context (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="33574-105">Context (Default)</span></span>
```
Set-AzContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33574-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="33574-106">TenantObject</span></span>
```
Set-AzContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33574-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="33574-107">SubscriptionObject</span></span>
```
Set-AzContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33574-108">Abbonamento</span><span class="sxs-lookup"><span data-stu-id="33574-108">Subscription</span></span>
```
Set-AzContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33574-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="33574-109">TenantNameOnly</span></span>
```
Set-AzContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33574-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33574-110">DESCRIPTION</span></span>
<span data-ttu-id="33574-111">Il cmdlet Set-AzContext imposta le informazioni di autenticazione per i cmdlet eseguiti nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="33574-111">The Set-AzContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="33574-112">Il contesto include informazioni su tenant, abbonamenti e ambiente.</span><span class="sxs-lookup"><span data-stu-id="33574-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="33574-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33574-113">EXAMPLES</span></span>

### <span data-ttu-id="33574-114">Esempio 1: impostare il contesto di sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="33574-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzContext -Subscription "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="33574-115">Questo comando imposta il contesto per l'uso della sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="33574-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="33574-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="33574-116">PARAMETERS</span></span>

### <span data-ttu-id="33574-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="33574-117">-Context</span></span>
<span data-ttu-id="33574-118">Specifica il contesto per la sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="33574-118">Specifies the context for the current session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: Context
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33574-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33574-119">-DefaultProfile</span></span>
<span data-ttu-id="33574-120">Le credenziali, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="33574-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33574-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="33574-121">-ExtendedProperty</span></span>
<span data-ttu-id="33574-122">Proprietà di contesto aggiuntive</span><span class="sxs-lookup"><span data-stu-id="33574-122">Additional context properties</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33574-123">-Force</span><span class="sxs-lookup"><span data-stu-id="33574-123">-Force</span></span>
<span data-ttu-id="33574-124">Sovrascrivere il contesto esistente con lo stesso nome, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="33574-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="33574-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="33574-125">-Name</span></span>
<span data-ttu-id="33574-126">Nome del contesto</span><span class="sxs-lookup"><span data-stu-id="33574-126">Name of the context</span></span>

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

### <span data-ttu-id="33574-127">-Ambito</span><span class="sxs-lookup"><span data-stu-id="33574-127">-Scope</span></span>
<span data-ttu-id="33574-128">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="33574-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="33574-129">-Sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="33574-129">-Subscription</span></span>
<span data-ttu-id="33574-130">Nome o ID dell'abbonamento a cui deve essere impostato il contesto.</span><span class="sxs-lookup"><span data-stu-id="33574-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="33574-131">Questo parametro include alias per-Subscriptionname e-SubscriptionId, quindi, per chiarezza, è possibile usare una di queste opzioni anziché-Subscription quando specifichi rispettivamente nome e ID.</span><span class="sxs-lookup"><span data-stu-id="33574-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: SubscriptionId, SubscriptionName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33574-132">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="33574-132">-SubscriptionObject</span></span>
<span data-ttu-id="33574-133">Un oggetto Subscription</span><span class="sxs-lookup"><span data-stu-id="33574-133">A subscription object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription
Parameter Sets: SubscriptionObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33574-134">-Tenant</span><span class="sxs-lookup"><span data-stu-id="33574-134">-Tenant</span></span>
<span data-ttu-id="33574-135">Nome del tenant o ID</span><span class="sxs-lookup"><span data-stu-id="33574-135">Tenant name or ID</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases: Domain, TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TenantNameOnly
Aliases: Domain, TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33574-136">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="33574-136">-TenantObject</span></span>
<span data-ttu-id="33574-137">Un oggetto tenant</span><span class="sxs-lookup"><span data-stu-id="33574-137">A Tenant Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureTenant
Parameter Sets: TenantObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33574-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="33574-138">-Confirm</span></span>
<span data-ttu-id="33574-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33574-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33574-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33574-140">-WhatIf</span></span>
<span data-ttu-id="33574-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="33574-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33574-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="33574-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33574-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33574-143">CommonParameters</span></span>
<span data-ttu-id="33574-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33574-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33574-145">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33574-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33574-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="33574-146">INPUTS</span></span>

### <span data-ttu-id="33574-147">Microsoft. Azure. Commands. profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="33574-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

### <span data-ttu-id="33574-148">Microsoft. Azure. Commands. profile. Models. PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="33574-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

### <span data-ttu-id="33574-149">Microsoft. Azure. Commands. profile. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="33574-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="33574-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33574-150">OUTPUTS</span></span>

### <span data-ttu-id="33574-151">Microsoft. Azure. Commands. profile. Models. Core. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="33574-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="33574-152">Note</span><span class="sxs-lookup"><span data-stu-id="33574-152">NOTES</span></span>

## <span data-ttu-id="33574-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33574-153">RELATED LINKS</span></span>

[<span data-ttu-id="33574-154">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="33574-154">Get-AzContext</span></span>](./Get-AzContext.md)

