---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzContext.md
ms.openlocfilehash: 49805dee2bff967da294fda228b5426e2652e209
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178119"
---
# <span data-ttu-id="ca658-101">Set-AzContext</span><span class="sxs-lookup"><span data-stu-id="ca658-101">Set-AzContext</span></span>

## <span data-ttu-id="ca658-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca658-102">SYNOPSIS</span></span>
<span data-ttu-id="ca658-103">Imposta il tenant, la sottoscrizione e l'ambiente da usare per i cmdlet nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="ca658-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="ca658-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca658-104">SYNTAX</span></span>

### <span data-ttu-id="ca658-105">Contesto (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ca658-105">Context (Default)</span></span>
```
Set-AzContext [-Context] <PSAzureContext>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca658-106">TenantObject</span><span class="sxs-lookup"><span data-stu-id="ca658-106">TenantObject</span></span>
```
Set-AzContext [-TenantObject] <PSAzureTenant>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca658-107">SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="ca658-107">SubscriptionObject</span></span>
```
Set-AzContext [-SubscriptionObject] <PSAzureSubscription>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca658-108">Abbonamento</span><span class="sxs-lookup"><span data-stu-id="ca658-108">Subscription</span></span>
```
Set-AzContext [-Tenant <String>] [-Subscription] <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca658-109">TenantNameOnly</span><span class="sxs-lookup"><span data-stu-id="ca658-109">TenantNameOnly</span></span>
```
Set-AzContext -Tenant <String>
 [-ExtendedProperty <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-Name <String>]
 [-Force] [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca658-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ca658-110">DESCRIPTION</span></span>
<span data-ttu-id="ca658-111">Il Set-AzContext cmdlet configura le informazioni di autenticazione per i cmdlet eseguiti nella sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="ca658-111">The Set-AzContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="ca658-112">Il contesto include informazioni su tenant, abbonamento e ambiente.</span><span class="sxs-lookup"><span data-stu-id="ca658-112">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="ca658-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca658-113">EXAMPLES</span></span>

### <span data-ttu-id="ca658-114">Esempio 1: Impostare il contesto dell'abbonamento</span><span class="sxs-lookup"><span data-stu-id="ca658-114">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzContext -Subscription "xxxx-xxxx-xxxx-xxxx"

Name    Account             SubscriptionName    Environment         TenantId
----    -------             ----------------    -----------         --------
Work    test@outlook.com    Subscription1       AzureCloud          xxxxxxxx-x...
```

<span data-ttu-id="ca658-115">Questo comando imposta il contesto in modo che usi la sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="ca658-115">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="ca658-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca658-116">PARAMETERS</span></span>

### <span data-ttu-id="ca658-117">-Context</span><span class="sxs-lookup"><span data-stu-id="ca658-117">-Context</span></span>
<span data-ttu-id="ca658-118">Specifica il contesto per la sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="ca658-118">Specifies the context for the current session.</span></span>

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

### <span data-ttu-id="ca658-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca658-119">-DefaultProfile</span></span>
<span data-ttu-id="ca658-120">Le credenziali, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca658-120">The credentials, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca658-121">-ExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="ca658-121">-ExtendedProperty</span></span>
<span data-ttu-id="ca658-122">Altre proprietà di contesto</span><span class="sxs-lookup"><span data-stu-id="ca658-122">Additional context properties</span></span>

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

### <span data-ttu-id="ca658-123">-Force</span><span class="sxs-lookup"><span data-stu-id="ca658-123">-Force</span></span>
<span data-ttu-id="ca658-124">Sovrascrivere il contesto esistente con lo stesso nome, se presente.</span><span class="sxs-lookup"><span data-stu-id="ca658-124">Overwrite the existing context with the same name, if any.</span></span>

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

### <span data-ttu-id="ca658-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ca658-125">-Name</span></span>
<span data-ttu-id="ca658-126">Nome del contesto</span><span class="sxs-lookup"><span data-stu-id="ca658-126">Name of the context</span></span>

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

### <span data-ttu-id="ca658-127">-Scope</span><span class="sxs-lookup"><span data-stu-id="ca658-127">-Scope</span></span>
<span data-ttu-id="ca658-128">Determina l'ambito delle modifiche di contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="ca658-128">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="ca658-129">-Abbonamento</span><span class="sxs-lookup"><span data-stu-id="ca658-129">-Subscription</span></span>
<span data-ttu-id="ca658-130">Nome o ID della sottoscrizione su cui deve essere impostato il contesto.</span><span class="sxs-lookup"><span data-stu-id="ca658-130">The name or id of the subscription that the context should be set to.</span></span> <span data-ttu-id="ca658-131">Questo parametro ha alias di -SubscriptionName e -SubscriptionId, quindi, per chiarezza, è possibile usare una di queste due opzioni invece di -Subscription quando si specificano rispettivamente nome e ID.</span><span class="sxs-lookup"><span data-stu-id="ca658-131">This parameter has aliases to -SubscriptionName and -SubscriptionId, so, for clarity, either of these can be used instead of -Subscription when specifying name and id, respectively.</span></span>

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

### <span data-ttu-id="ca658-132">-SubscriptionObject</span><span class="sxs-lookup"><span data-stu-id="ca658-132">-SubscriptionObject</span></span>
<span data-ttu-id="ca658-133">Oggetto abbonamento</span><span class="sxs-lookup"><span data-stu-id="ca658-133">A subscription object</span></span>

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

### <span data-ttu-id="ca658-134">-Tenant</span><span class="sxs-lookup"><span data-stu-id="ca658-134">-Tenant</span></span>
<span data-ttu-id="ca658-135">Nome o ID tenant</span><span class="sxs-lookup"><span data-stu-id="ca658-135">Tenant name or ID</span></span>

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

### <span data-ttu-id="ca658-136">-TenantObject</span><span class="sxs-lookup"><span data-stu-id="ca658-136">-TenantObject</span></span>
<span data-ttu-id="ca658-137">Oggetto tenant</span><span class="sxs-lookup"><span data-stu-id="ca658-137">A Tenant Object</span></span>

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

### <span data-ttu-id="ca658-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca658-138">-Confirm</span></span>
<span data-ttu-id="ca658-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca658-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca658-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca658-140">-WhatIf</span></span>
<span data-ttu-id="ca658-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca658-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca658-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca658-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca658-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca658-143">CommonParameters</span></span>
<span data-ttu-id="ca658-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca658-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca658-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca658-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca658-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="ca658-146">INPUTS</span></span>

### <span data-ttu-id="ca658-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="ca658-147">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

### <span data-ttu-id="ca658-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="ca658-148">Microsoft.Azure.Commands.Profile.Models.PSAzureTenant</span></span>

### <span data-ttu-id="ca658-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="ca658-149">Microsoft.Azure.Commands.Profile.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="ca658-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca658-150">OUTPUTS</span></span>

### <span data-ttu-id="ca658-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="ca658-151">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="ca658-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="ca658-152">NOTES</span></span>

## <span data-ttu-id="ca658-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca658-153">RELATED LINKS</span></span>

[<span data-ttu-id="ca658-154">Get-AzContext</span><span class="sxs-lookup"><span data-stu-id="ca658-154">Get-AzContext</span></span>](./Get-AzContext.md)

