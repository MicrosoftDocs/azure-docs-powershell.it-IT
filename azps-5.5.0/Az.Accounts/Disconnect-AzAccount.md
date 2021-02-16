---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disconnect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
ms.openlocfilehash: 23689d4e84228d4eaeaae82e2efe53b6450d44f9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178127"
---
# <span data-ttu-id="cfe6b-101">Disconnect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="cfe6b-101">Disconnect-AzAccount</span></span>

## <span data-ttu-id="cfe6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfe6b-102">SYNOPSIS</span></span>
<span data-ttu-id="cfe6b-103">Disconnette un account Azure connesso e rimuove tutte le credenziali e i contesti associati all'account.</span><span class="sxs-lookup"><span data-stu-id="cfe6b-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

## <span data-ttu-id="cfe6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cfe6b-104">SYNTAX</span></span>

### <span data-ttu-id="cfe6b-105">ContextName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cfe6b-105">ContextName (Default)</span></span>
```
Disconnect-AzAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfe6b-106">UserId</span><span class="sxs-lookup"><span data-stu-id="cfe6b-106">UserId</span></span>
```
Disconnect-AzAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfe6b-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="cfe6b-107">ServicePrincipal</span></span>
```
Disconnect-AzAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfe6b-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="cfe6b-108">AccountObject</span></span>
```
Disconnect-AzAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cfe6b-109">ContextObject</span><span class="sxs-lookup"><span data-stu-id="cfe6b-109">ContextObject</span></span>
```
Disconnect-AzAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cfe6b-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cfe6b-110">DESCRIPTION</span></span>
<span data-ttu-id="cfe6b-111">Il cmdlet Disconnect-AzAccount disconnette un account Azure connesso e rimuove tutte le credenziali e i contesti (informazioni sull'abbonamento e sul tenant) associati all'account.</span><span class="sxs-lookup"><span data-stu-id="cfe6b-111">The Disconnect-AzAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>
<span data-ttu-id="cfe6b-112">Dopo aver eseguito questo cmdlet, è necessario eseguire di nuovo l'accesso con Connect-AzAccount.</span><span class="sxs-lookup"><span data-stu-id="cfe6b-112">After executing this cmdlet, you will need to login again using Connect-AzAccount.</span></span>

## <span data-ttu-id="cfe6b-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cfe6b-113">EXAMPLES</span></span>

### <span data-ttu-id="cfe6b-114">Esempio 1: Disconnettersi dall'account corrente</span><span class="sxs-lookup"><span data-stu-id="cfe6b-114">Example 1: Logout of the current account</span></span>
```powershell
PS C:\> Disconnect-AzAccount
```

<span data-ttu-id="cfe6b-115">Disconnette l'account di Azure associato al contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="cfe6b-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="cfe6b-116">Esempio 2: Disconnettersi dall'account associato a un contesto specifico</span><span class="sxs-lookup"><span data-stu-id="cfe6b-116">Example 2: Logout of the account associated with a particular context</span></span>
```powershell
PS C:\> Get-AzContext "Work" | Disconnect-AzAccount -Scope CurrentUser
```

<span data-ttu-id="cfe6b-117">Disconnette l'account associato al contesto specificato (denominato "Lavoro").</span><span class="sxs-lookup"><span data-stu-id="cfe6b-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="cfe6b-118">Poiché questo usa l'ambito "CurrentUser", tutte le credenziali e i contesti verranno eliminati definitivamente.</span><span class="sxs-lookup"><span data-stu-id="cfe6b-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="cfe6b-119">Esempio 3: Disconnettere un utente specifico</span><span class="sxs-lookup"><span data-stu-id="cfe6b-119">Example 3: Log out a particular user</span></span>
```powershell
PS C:\> Disconnect-AzAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="cfe6b-120">Disconnette user1@contoso.org l'utente ' ' - tutte le credenziali e tutti i contesti associati all'utente verranno rimossi.</span><span class="sxs-lookup"><span data-stu-id="cfe6b-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="cfe6b-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cfe6b-121">PARAMETERS</span></span>

### <span data-ttu-id="cfe6b-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="cfe6b-122">-ApplicationId</span></span>
<span data-ttu-id="cfe6b-123">ID ServicePrincipal (ID univoco globale)</span><span class="sxs-lookup"><span data-stu-id="cfe6b-123">ServicePrincipal id (globally unique id)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases: SPN, ServicePrincipal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfe6b-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="cfe6b-124">-AzureContext</span></span>
<span data-ttu-id="cfe6b-125">Contesto</span><span class="sxs-lookup"><span data-stu-id="cfe6b-125">Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: ContextObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfe6b-126">-ContextName</span><span class="sxs-lookup"><span data-stu-id="cfe6b-126">-ContextName</span></span>
<span data-ttu-id="cfe6b-127">Nome del contesto da cui disconnettersi</span><span class="sxs-lookup"><span data-stu-id="cfe6b-127">Name of the context to log out of</span></span>

```yaml
Type: System.String
Parameter Sets: ContextName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfe6b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfe6b-128">-DefaultProfile</span></span>
<span data-ttu-id="cfe6b-129">Le credenziali, il tenant e la sottoscrizione usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="cfe6b-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cfe6b-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cfe6b-130">-InputObject</span></span>
<span data-ttu-id="cfe6b-131">Oggetto account da rimuovere</span><span class="sxs-lookup"><span data-stu-id="cfe6b-131">The account object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cfe6b-132">-Scope</span><span class="sxs-lookup"><span data-stu-id="cfe6b-132">-Scope</span></span>
<span data-ttu-id="cfe6b-133">Determina l'ambito delle modifiche di contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate dall'utente.</span><span class="sxs-lookup"><span data-stu-id="cfe6b-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="cfe6b-134">-TenantId</span><span class="sxs-lookup"><span data-stu-id="cfe6b-134">-TenantId</span></span>
<span data-ttu-id="cfe6b-135">ID tenant (ID univoco globale)</span><span class="sxs-lookup"><span data-stu-id="cfe6b-135">Tenant id (globally unique id)</span></span>

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfe6b-136">-Username</span><span class="sxs-lookup"><span data-stu-id="cfe6b-136">-Username</span></span>
<span data-ttu-id="cfe6b-137">Nome utente del modulo ' user@contoso.org '</span><span class="sxs-lookup"><span data-stu-id="cfe6b-137">User name of the form 'user@contoso.org'</span></span>

```yaml
Type: System.String
Parameter Sets: UserId
Aliases: Id, UserId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfe6b-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cfe6b-138">-Confirm</span></span>
<span data-ttu-id="cfe6b-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cfe6b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfe6b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfe6b-140">-WhatIf</span></span>
<span data-ttu-id="cfe6b-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cfe6b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cfe6b-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cfe6b-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="cfe6b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfe6b-143">CommonParameters</span></span>
<span data-ttu-id="cfe6b-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfe6b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfe6b-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfe6b-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfe6b-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="cfe6b-146">INPUTS</span></span>

### <span data-ttu-id="cfe6b-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="cfe6b-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="cfe6b-148">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="cfe6b-148">Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext</span></span>

## <span data-ttu-id="cfe6b-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cfe6b-149">OUTPUTS</span></span>

### <span data-ttu-id="cfe6b-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="cfe6b-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="cfe6b-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="cfe6b-151">NOTES</span></span>

## <span data-ttu-id="cfe6b-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cfe6b-152">RELATED LINKS</span></span>
