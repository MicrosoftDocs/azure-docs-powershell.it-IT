---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADUser.md
ms.openlocfilehash: 1b863b0bc9cb90caca4d7431ec6835cb75836609
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687271"
---
# <span data-ttu-id="00844-101">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="00844-101">Remove-AzureRmADUser</span></span>

## <span data-ttu-id="00844-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="00844-102">SYNOPSIS</span></span>
<span data-ttu-id="00844-103">Elimina un utente di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="00844-103">Deletes an active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00844-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="00844-104">SYNTAX</span></span>

### <span data-ttu-id="00844-105">UPNOrObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="00844-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00844-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="00844-106">UPNParameterSet</span></span>
```
Remove-AzureRmADUser -UserPrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00844-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00844-107">ObjectIdParameterSet</span></span>
```
Remove-AzureRmADUser -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00844-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="00844-108">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00844-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00844-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00844-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00844-110">DESCRIPTION</span></span>
<span data-ttu-id="00844-111">Elimina un utente di Active Directory (account aziendale o dell'Istituto di istruzione noto anche come org-ID).</span><span class="sxs-lookup"><span data-stu-id="00844-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="00844-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="00844-112">EXAMPLES</span></span>

### <span data-ttu-id="00844-113">Esempio 1-rimuovere un utente in base al nome dell'entità utente</span><span class="sxs-lookup"><span data-stu-id="00844-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzureRmADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="00844-114">Rimuove l'utente con il nome dell'entità utente " foo@domain.com " dal tenant.</span><span class="sxs-lookup"><span data-stu-id="00844-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="00844-115">Esempio 2-rimuovere un utente per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="00844-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzureRmADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="00844-116">Rimuove l'utente con l'ID oggetto "7a9582cf-88c4-4319-842b-7a5d60967a69" dal tenant.</span><span class="sxs-lookup"><span data-stu-id="00844-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="00844-117">Esempio 3-rimuovere un utente tramite pipe</span><span class="sxs-lookup"><span data-stu-id="00844-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzureRmADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzureRmADUser
```

<span data-ttu-id="00844-118">Ottiene l'utente con l'ID oggetto "7a9582cf-88c4-4319-842b-7a5d60967a69" e convoglia il cmdlet Remove-AzureRmADUser per rimuovere l'utente dal tenant.</span><span class="sxs-lookup"><span data-stu-id="00844-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzureRmADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="00844-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="00844-119">PARAMETERS</span></span>

### <span data-ttu-id="00844-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00844-120">-DefaultProfile</span></span>
<span data-ttu-id="00844-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="00844-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00844-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="00844-122">-DisplayName</span></span>
<span data-ttu-id="00844-123">Nome visualizzato dell'utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="00844-123">The display name of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00844-124">-Force</span><span class="sxs-lookup"><span data-stu-id="00844-124">-Force</span></span>
<span data-ttu-id="00844-125">Se specificato, non chiede conferma per l'eliminazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="00844-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="00844-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00844-126">-InputObject</span></span>
<span data-ttu-id="00844-127">L'oggetto utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="00844-127">The user object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00844-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="00844-128">-ObjectId</span></span>
<span data-ttu-id="00844-129">ID oggetto dell'utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="00844-129">The object id of the user to be deleted.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00844-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00844-130">-PassThru</span></span>
<span data-ttu-id="00844-131">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="00844-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="00844-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="00844-132">-UPNOrObjectId</span></span>
<span data-ttu-id="00844-133">Nome dell'entità utente o objectId dell'utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="00844-133">The user principal name or the objectId of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00844-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="00844-134">-UserPrincipalName</span></span>
<span data-ttu-id="00844-135">Nome dell'entità utente dell'utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="00844-135">The user principal name of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00844-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="00844-136">-Confirm</span></span>
<span data-ttu-id="00844-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00844-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00844-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00844-138">-WhatIf</span></span>
<span data-ttu-id="00844-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00844-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00844-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="00844-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00844-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00844-141">CommonParameters</span></span>
<span data-ttu-id="00844-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00844-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00844-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00844-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00844-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="00844-144">INPUTS</span></span>

### <span data-ttu-id="00844-145">System. String</span><span class="sxs-lookup"><span data-stu-id="00844-145">System.String</span></span>

### <span data-ttu-id="00844-146">System. Guid</span><span class="sxs-lookup"><span data-stu-id="00844-146">System.Guid</span></span>

### <span data-ttu-id="00844-147">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="00844-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="00844-148">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="00844-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="00844-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="00844-149">OUTPUTS</span></span>

### <span data-ttu-id="00844-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="00844-150">System.Boolean</span></span>

## <span data-ttu-id="00844-151">Note</span><span class="sxs-lookup"><span data-stu-id="00844-151">NOTES</span></span>

## <span data-ttu-id="00844-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="00844-152">RELATED LINKS</span></span>

[<span data-ttu-id="00844-153">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="00844-153">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="00844-154">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="00844-154">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="00844-155">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="00844-155">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

