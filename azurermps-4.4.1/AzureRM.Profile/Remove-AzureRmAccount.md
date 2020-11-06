---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmAccount.md
ms.openlocfilehash: d1b401c1ae806d48b9cb9969c36ef72d104076eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516104"
---
# <span data-ttu-id="0b651-101">Remove-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="0b651-101">Remove-AzureRmAccount</span></span>

## <span data-ttu-id="0b651-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0b651-102">SYNOPSIS</span></span>
<span data-ttu-id="0b651-103">Rimuovere tutte le credenziali e i contesti associati all'account specifico.</span><span class="sxs-lookup"><span data-stu-id="0b651-103">Remove all credentials and contexts associated with the given account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b651-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b651-104">SYNTAX</span></span>

### <span data-ttu-id="0b651-105">ContextName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0b651-105">ContextName (Default)</span></span>
```
Remove-AzureRmAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b651-106">UserId</span><span class="sxs-lookup"><span data-stu-id="0b651-106">UserId</span></span>
```
Remove-AzureRmAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b651-107">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0b651-107">ServicePrincipal</span></span>
```
Remove-AzureRmAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b651-108">AccountObject</span><span class="sxs-lookup"><span data-stu-id="0b651-108">AccountObject</span></span>
```
Remove-AzureRmAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b651-109">ContextObject</span><span class="sxs-lookup"><span data-stu-id="0b651-109">ContextObject</span></span>
```
Remove-AzureRmAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b651-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b651-110">DESCRIPTION</span></span>
<span data-ttu-id="0b651-111">Rimuovere tutte le credenziali e i contesti (informazioni sull'abbonamento e sul tenant) associati all'account specifico.</span><span class="sxs-lookup"><span data-stu-id="0b651-111">Remove all credentials, and contexts (subscription and tenant information) associated with the given account.</span></span>  <span data-ttu-id="0b651-112">Dopo aver eseguito questo cmdlet, sarà necessario eseguire di nuovo l'accesso usando Add-AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="0b651-112">After executing this cmdlet, you will need to login again using Add-AzureRmAccount</span></span>

## <span data-ttu-id="0b651-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b651-113">EXAMPLES</span></span>

### <span data-ttu-id="0b651-114">Disconnettere l'account di curent</span><span class="sxs-lookup"><span data-stu-id="0b651-114">Log out the curent account</span></span>
```
PS C:\> Remove-AzureRmAccount
```

<span data-ttu-id="0b651-115">Disconnette l'account associato al contesto corrente.</span><span class="sxs-lookup"><span data-stu-id="0b651-115">Logs out the account associated with the current context.</span></span>

### <span data-ttu-id="0b651-116">Disconnettere l'account associato a un particolare contesto</span><span class="sxs-lookup"><span data-stu-id="0b651-116">Log out the account associated with a particular context</span></span>
```
PS C:\> Get-AzureRmContext "Work" | Remove-AzureRmAccount -Scope CurrentUser
```

<span data-ttu-id="0b651-117">Disconnette l'account associato al contesto indicato (denominato "lavoro").</span><span class="sxs-lookup"><span data-stu-id="0b651-117">Logs out the account associated with the given context (named 'Work').</span></span> <span data-ttu-id="0b651-118">Poiché viene usato l'ambito "CurrentUser", tutte le credenziali e i contesti verranno eliminati definitivamente.</span><span class="sxs-lookup"><span data-stu-id="0b651-118">Because this uses the 'CurrentUser' scope, all credentials and contexts will be permanently deleted.</span></span>

### <span data-ttu-id="0b651-119">Disconnettersi da un determinato utente</span><span class="sxs-lookup"><span data-stu-id="0b651-119">Log out a particular user</span></span>
```
PS C:\> Remove-AzureRmAccount -Username 'user1@contoso.org'
```

<span data-ttu-id="0b651-120">Disconnette l'utente " user1@contoso.org -tutte le credenziali e tutti i contesti associati a questo utente verranno rimossi.</span><span class="sxs-lookup"><span data-stu-id="0b651-120">Logs out the 'user1@contoso.org' user - all credentials and all contexts associated with this user will be removed.</span></span>

## <span data-ttu-id="0b651-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0b651-121">PARAMETERS</span></span>

### <span data-ttu-id="0b651-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="0b651-122">-ApplicationId</span></span>
<span data-ttu-id="0b651-123">ID ServicePrincipal (ID univoco globale)</span><span class="sxs-lookup"><span data-stu-id="0b651-123">ServicePrincipal id (globally unique id)</span></span>

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

### <span data-ttu-id="0b651-124">-AzureContext</span><span class="sxs-lookup"><span data-stu-id="0b651-124">-AzureContext</span></span>
<span data-ttu-id="0b651-125">Contesto</span><span class="sxs-lookup"><span data-stu-id="0b651-125">Context</span></span>

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

### <span data-ttu-id="0b651-126">-ContextName</span><span class="sxs-lookup"><span data-stu-id="0b651-126">-ContextName</span></span>
<span data-ttu-id="0b651-127">Nome del contesto in cui disconnettersi</span><span class="sxs-lookup"><span data-stu-id="0b651-127">Name of the context to log out of</span></span>

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

### <span data-ttu-id="0b651-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b651-128">-DefaultProfile</span></span>
<span data-ttu-id="0b651-129">Credenziali, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0b651-129">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b651-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0b651-130">-InputObject</span></span>
<span data-ttu-id="0b651-131">Oggetto account da rimuovere</span><span class="sxs-lookup"><span data-stu-id="0b651-131">The account object to remove</span></span>

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

### <span data-ttu-id="0b651-132">-Ambito</span><span class="sxs-lookup"><span data-stu-id="0b651-132">-Scope</span></span>
<span data-ttu-id="0b651-133">Determina l'ambito delle modifiche al contesto, ad esempio se le modifiche si applicano solo al processo corrente o a tutte le sessioni avviate da questo utente.</span><span class="sxs-lookup"><span data-stu-id="0b651-133">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="0b651-134">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="0b651-134">-TenantId</span></span>
<span data-ttu-id="0b651-135">ID tenant (ID univoco globale)</span><span class="sxs-lookup"><span data-stu-id="0b651-135">Tenant id (globally unique id)</span></span>

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

### <span data-ttu-id="0b651-136">-Username</span><span class="sxs-lookup"><span data-stu-id="0b651-136">-Username</span></span>
<span data-ttu-id="0b651-137">Nome utente della maschera user@contoso.org</span><span class="sxs-lookup"><span data-stu-id="0b651-137">User name of the form 'user@contoso.org'</span></span>

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

### <span data-ttu-id="0b651-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0b651-138">-Confirm</span></span>
<span data-ttu-id="0b651-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b651-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b651-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b651-140">-WhatIf</span></span>
<span data-ttu-id="0b651-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b651-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b651-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b651-142">The cmdlet is not executed.</span></span>

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

### <span data-ttu-id="0b651-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b651-143">CommonParameters</span></span>
<span data-ttu-id="0b651-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b651-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b651-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b651-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b651-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0b651-146">INPUTS</span></span>

### <span data-ttu-id="0b651-147">Microsoft. Azure. Commands. profile. Models. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="0b651-147">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

### <span data-ttu-id="0b651-148">Microsoft. Azure. Commands. profile. Models. PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="0b651-148">Microsoft.Azure.Commands.Profile.Models.PSAzureContext</span></span>

## <span data-ttu-id="0b651-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b651-149">OUTPUTS</span></span>

### <span data-ttu-id="0b651-150">Microsoft. Azure. Commands. profile. Models. PSAzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="0b651-150">Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount</span></span>

## <span data-ttu-id="0b651-151">Note</span><span class="sxs-lookup"><span data-stu-id="0b651-151">NOTES</span></span>

## <span data-ttu-id="0b651-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b651-152">RELATED LINKS</span></span>

