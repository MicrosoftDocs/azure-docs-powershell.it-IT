---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
ms.openlocfilehash: e5fbecea64a15569fbd6319f3f3be5ff4102153e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688059"
---
# <span data-ttu-id="c8b03-101">Disconnect-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="c8b03-101">Disconnect-AzureRmAccount</span></span>

## <span data-ttu-id="c8b03-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c8b03-102">SYNOPSIS</span></span>
<span data-ttu-id="c8b03-103">Disconnette un account Azure connesso e rimuove tutte le credenziali e i contesti associati a tale account.</span><span class="sxs-lookup"><span data-stu-id="c8b03-103">Disconnects a connected Azure account and removes all credentials and contexts associated with that account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8b03-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c8b03-104">SYNTAX</span></span>

### <span data-ttu-id="c8b03-105">ContextName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c8b03-105">ContextName (Default)</span></span>
```
Disconnect-AzureRmAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8b03-106">UserId</span><span class="sxs-lookup"><span data-stu-id="c8b03-106">UserId</span></span>
```
Disconnect-AzureRmAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8b03-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c8b03-107">ServicePrincipal</span></span>
```
Disconnect-AzureRmAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8b03-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="c8b03-108">AccountObject</span></span>
```
Disconnect-AzureRmAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8b03-109">ContextObject</span><span class="sxs-lookup"><span data-stu-id="c8b03-109">ContextObject</span></span>
```
Disconnect-AzureRmAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8b03-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c8b03-110">DESCRIPTION</span></span>
<span data-ttu-id="c8b03-111">Il cmdlet Disconnect-AzureRmAccount disconnette un account di Azure connesso e rimuove tutte le credenziali e i contesti (informazioni sull'abbonamento e il tenant) associati all'account.</span><span class="sxs-lookup"><span data-stu-id="c8b03-111">The Disconnect-AzureRmAccount cmdlet disconnects a connected Azure account and removes all credentials and contexts (subscription and tenant information) associated with that account.</span></span>
<span data-ttu-id="c8b03-112">Dopo l'esecuzione di questo cmdlet, sarà necessario eseguire di nuovo l'accesso usando Connect-AzureRmAccount.</span><span class="sxs-lookup"><span data-stu-id="c8b03-112">After executing this cmdlet, you will need to login again using Connect-AzureRmAccount.</span></span>

## <span data-ttu-id="c8b03-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c8b03-113">EXAMPLES</span></span>

### <span data-ttu-id="c8b03-114">Disconnessione dell'account corrente</span><span class="sxs-lookup"><span data-stu-id="c8b03-114">Logout of the current account</span></span>
```
PS C:\> Disconnect-AzureRmAccount
```

<span data-ttu-id="c8b03-115">Disconnettersi dall'account di Azure associato al contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="c8b03-115">Logs out of the Azure account associated with the current context.</span></span>

### <span data-ttu-id="c8b03-116">Logout dell'account associato a un contesto specifico</span><span class="sxs-lookup"><span data-stu-id="c8b03-116">Logout of the account associated with a particular context</span></span>
```
PS C:\> Get-AzureRmContext "Work" | Disconnect-AzureRmAccount -Scope CurrentUser
```

<span data-ttu-id="c8b03-117">Disconnette l'account associato al contesto indicato (denominato "lavoro").</span><span class="sxs-lookup"><span data-stu-id="c8b03-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="c8b03-118">Poiché viene usato l'ambito "CurrentUser", tutte le credenziali e i contesti verranno eliminati definitivamente.</span><span class="sxs-lookup"><span data-stu-id="c8b03-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="c8b03-119">Disconnettersi da un determinato utente</span><span class="sxs-lookup"><span data-stu-id="c8b03-119">Log out a particular user</span></span>
```
PS C:\> Disconnect-AzureRmAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="c8b03-120">Disconnette l'utente " user1@contoso.org -tutte le credenziali e tutti i contesti associati a questo utente verranno rimossi.</span><span class="sxs-lookup"><span data-stu-id="c8b03-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="c8b03-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c8b03-121">PARAMETERS</span></span>

### <span data-ttu-id="c8b03-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c8b03-122">-ApplicationId</span></span>
<span data-ttu-id="c8b03-123">ID ServicePrincipal (ID univoco globale)</span><span class="sxs-lookup"><span data-stu-id="c8b03-123">ServicePrincipal id (globally unique id)</span></span>

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

### <span data-ttu-id="c8b03-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="c8b03-124">-AzureContext</span></span>
<span data-ttu-id="c8b03-125">Contesto</span><span class="sxs-lookup"><span data-stu-id="c8b03-125">Context</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureContext
Parameter Sets: ContextObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c8b03-126">-ContextName</span><span class="sxs-lookup"><span data-stu-id="c8b03-126">-ContextName</span></span>
<span data-ttu-id="c8b03-127">Nome del contesto in cui disconnettersi</span><span class="sxs-lookup"><span data-stu-id="c8b03-127">Name of the context to log out of</span></span>

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

### <span data-ttu-id="c8b03-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8b03-128">-DefaultProfile</span></span>
<span data-ttu-id="c8b03-129">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c8b03-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8b03-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8b03-130">-InputObject</span></span>
<span data-ttu-id="c8b03-131">Oggetto account da rimuovere</span><span class="sxs-lookup"><span data-stu-id="c8b03-131">The account object to remove</span></span>

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

### <span data-ttu-id="c8b03-132">-Ambito</span><span class="sxs-lookup"><span data-stu-id="c8b03-132">-Scope</span></span>
<span data-ttu-id="c8b03-133">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="c8b03-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="c8b03-134">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="c8b03-134">-TenantId</span></span>
<span data-ttu-id="c8b03-135">ID tenant (ID univoco globale)</span><span class="sxs-lookup"><span data-stu-id="c8b03-135">Tenant id (globally unique id)</span></span>

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

### <span data-ttu-id="c8b03-136">-Username</span><span class="sxs-lookup"><span data-stu-id="c8b03-136">-Username</span></span>
<span data-ttu-id="c8b03-137">Nome utente della maschera user@contoso.org</span><span class="sxs-lookup"><span data-stu-id="c8b03-137">User name of the form 'user@contoso.org'</span></span>

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

### <span data-ttu-id="c8b03-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c8b03-138">-Confirm</span></span>
<span data-ttu-id="c8b03-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8b03-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8b03-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8b03-140">-WhatIf</span></span>
<span data-ttu-id="c8b03-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8b03-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8b03-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c8b03-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="c8b03-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8b03-143">CommonParameters</span></span>
<span data-ttu-id="c8b03-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8b03-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8b03-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8b03-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8b03-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c8b03-146">INPUTS</span></span>

### <span data-ttu-id="c8b03-147">Microsoft. Azure. Commands. profile. Models. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="c8b03-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>
<span data-ttu-id="c8b03-148">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c8b03-148">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c8b03-149">Microsoft. Azure. Commands. profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="c8b03-149">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>
<span data-ttu-id="c8b03-150">Parametri: AzureContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c8b03-150">Parameters: AzureContext (ByValue)</span></span>

## <span data-ttu-id="c8b03-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c8b03-151">OUTPUTS</span></span>

### <span data-ttu-id="c8b03-152">Microsoft. Azure. Commands. profile. Models. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="c8b03-152">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="c8b03-153">Note</span><span class="sxs-lookup"><span data-stu-id="c8b03-153">NOTES</span></span>

## <span data-ttu-id="c8b03-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c8b03-154">RELATED LINKS</span></span>
