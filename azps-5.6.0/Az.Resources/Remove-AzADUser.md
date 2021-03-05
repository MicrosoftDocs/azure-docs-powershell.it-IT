---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
ms.openlocfilehash: 98d5433ca2a8d557c7ca1924b9edb6e4fdca2b2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970333"
---
# <span data-ttu-id="93e20-101">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="93e20-101">Remove-AzADUser</span></span>

## <span data-ttu-id="93e20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93e20-102">SYNOPSIS</span></span>
<span data-ttu-id="93e20-103">Elimina un utente di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="93e20-103">Deletes an active directory user.</span></span>

## <span data-ttu-id="93e20-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93e20-104">SYNTAX</span></span>

### <span data-ttu-id="93e20-105">UPNOrObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="93e20-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93e20-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="93e20-106">UPNParameterSet</span></span>
```
Remove-AzADUser -UserPrincipalName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93e20-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93e20-107">ObjectIdParameterSet</span></span>
```
Remove-AzADUser -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93e20-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="93e20-108">DisplayNameParameterSet</span></span>
```
Remove-AzADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93e20-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93e20-109">InputObjectParameterSet</span></span>
```
Remove-AzADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93e20-110">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="93e20-110">DESCRIPTION</span></span>
<span data-ttu-id="93e20-111">Elimina un utente di Active Directory (account aziendale o dell'istituto di istruzione noto anche come org-id).</span><span class="sxs-lookup"><span data-stu-id="93e20-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="93e20-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93e20-112">EXAMPLES</span></span>

### <span data-ttu-id="93e20-113">Esempio 1: Rimuovere un utente in base al nome dell'entità utente</span><span class="sxs-lookup"><span data-stu-id="93e20-113">Example 1: Remove a user by user principal name</span></span>

```powershell
PS C:\> Remove-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="93e20-114">Rimuove l'utente con il nome dell'entità foo@domain.com utente " " dal tenant.</span><span class="sxs-lookup"><span data-stu-id="93e20-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="93e20-115">Esempio 2: Rimuovere un utente in base all'ID oggetto</span><span class="sxs-lookup"><span data-stu-id="93e20-115">Example 2: Remove a user by object id</span></span>

```powershell
PS C:\> Remove-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="93e20-116">Rimuove l'utente con ID oggetto '7a9582cf-88c4-4319-842b-7a5d60967a69' dal tenant.</span><span class="sxs-lookup"><span data-stu-id="93e20-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="93e20-117">Esempio 3: Rimuovere un utente tramite piping</span><span class="sxs-lookup"><span data-stu-id="93e20-117">Example 3: Remove a user by piping</span></span>

```powershell
PS C:\> Get-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzADUser
```

<span data-ttu-id="93e20-118">Ottiene l'utente con ID oggetto '7a9582cf-88c4-4319-842b-7a5d60967a69' e pipe che al cmdlet di Remove-AzADUser per rimuovere l'utente dal tenant.</span><span class="sxs-lookup"><span data-stu-id="93e20-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="93e20-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93e20-119">PARAMETERS</span></span>

### <span data-ttu-id="93e20-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93e20-120">-DefaultProfile</span></span>
<span data-ttu-id="93e20-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="93e20-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93e20-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="93e20-122">-DisplayName</span></span>
<span data-ttu-id="93e20-123">Nome visualizzato dell'utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="93e20-123">The display name of the user to be deleted.</span></span>

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

### <span data-ttu-id="93e20-124">-Force</span><span class="sxs-lookup"><span data-stu-id="93e20-124">-Force</span></span>
<span data-ttu-id="93e20-125">Se specificato, non chiede conferma per l'eliminazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="93e20-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="93e20-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93e20-126">-InputObject</span></span>
<span data-ttu-id="93e20-127">Oggetto utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="93e20-127">The user object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADUser
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93e20-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="93e20-128">-ObjectId</span></span>
<span data-ttu-id="93e20-129">ID oggetto dell'utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="93e20-129">The object id of the user to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93e20-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93e20-130">-PassThru</span></span>
<span data-ttu-id="93e20-131">Se si specifica questo valore, viene restituito true se il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="93e20-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="93e20-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="93e20-132">-UPNOrObjectId</span></span>
<span data-ttu-id="93e20-133">Il nome dell'entità utente o l'id oggetto dell'utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="93e20-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="93e20-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="93e20-134">-UserPrincipalName</span></span>
<span data-ttu-id="93e20-135">Il nome dell'entità utente dell'utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="93e20-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="93e20-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93e20-136">-Confirm</span></span>
<span data-ttu-id="93e20-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93e20-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93e20-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93e20-138">-WhatIf</span></span>
<span data-ttu-id="93e20-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93e20-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93e20-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93e20-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93e20-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e20-141">CommonParameters</span></span>
<span data-ttu-id="93e20-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93e20-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e20-143">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="93e20-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e20-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="93e20-144">INPUTS</span></span>

### <span data-ttu-id="93e20-145">System.String</span><span class="sxs-lookup"><span data-stu-id="93e20-145">System.String</span></span>

### <span data-ttu-id="93e20-146">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="93e20-146">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="93e20-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93e20-147">OUTPUTS</span></span>

### <span data-ttu-id="93e20-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="93e20-148">System.Boolean</span></span>

## <span data-ttu-id="93e20-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="93e20-149">NOTES</span></span>

## <span data-ttu-id="93e20-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93e20-150">RELATED LINKS</span></span>

[<span data-ttu-id="93e20-151">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="93e20-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="93e20-152">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="93e20-152">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="93e20-153">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="93e20-153">Update-AzADUser</span></span>](./Update-AzADUser.md)

