---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
ms.openlocfilehash: 39413c8279b84bb75d3e86bbf41ff40afe05ad06
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192634"
---
# <span data-ttu-id="bdba5-101">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="bdba5-101">Remove-AzADUser</span></span>

## <span data-ttu-id="bdba5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bdba5-102">SYNOPSIS</span></span>
<span data-ttu-id="bdba5-103">Elimina un utente di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="bdba5-103">Deletes an active directory user.</span></span>

## <span data-ttu-id="bdba5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bdba5-104">SYNTAX</span></span>

### <span data-ttu-id="bdba5-105">UPNOrObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bdba5-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdba5-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdba5-106">UPNParameterSet</span></span>
```
Remove-AzADUser -UserPrincipalName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdba5-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdba5-107">ObjectIdParameterSet</span></span>
```
Remove-AzADUser -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdba5-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdba5-108">DisplayNameParameterSet</span></span>
```
Remove-AzADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdba5-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdba5-109">InputObjectParameterSet</span></span>
```
Remove-AzADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdba5-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bdba5-110">DESCRIPTION</span></span>
<span data-ttu-id="bdba5-111">Elimina un utente di Active Directory (account aziendale o dell'Istituto di istruzione noto anche come org-ID).</span><span class="sxs-lookup"><span data-stu-id="bdba5-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="bdba5-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bdba5-112">EXAMPLES</span></span>

### <span data-ttu-id="bdba5-113">Esempio 1: rimuovere un utente in base al nome dell'entità utente</span><span class="sxs-lookup"><span data-stu-id="bdba5-113">Example 1: Remove a user by user principal name</span></span>

```powershell
PS C:\> Remove-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="bdba5-114">Rimuove l'utente con il nome dell'entità utente " foo@domain.com " dal tenant.</span><span class="sxs-lookup"><span data-stu-id="bdba5-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="bdba5-115">Esempio 2: rimuovere un utente per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="bdba5-115">Example 2: Remove a user by object id</span></span>

```powershell
PS C:\> Remove-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="bdba5-116">Rimuove l'utente con l'ID oggetto "7a9582cf-88c4-4319-842b-7a5d60967a69" dal tenant.</span><span class="sxs-lookup"><span data-stu-id="bdba5-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="bdba5-117">Esempio 3: rimuovere un utente tramite pipe</span><span class="sxs-lookup"><span data-stu-id="bdba5-117">Example 3: Remove a user by piping</span></span>

```powershell
PS C:\> Get-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzADUser
```

<span data-ttu-id="bdba5-118">Ottiene l'utente con l'ID oggetto "7a9582cf-88c4-4319-842b-7a5d60967a69" e convoglia il cmdlet Remove-AzADUser per rimuovere l'utente dal tenant.</span><span class="sxs-lookup"><span data-stu-id="bdba5-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="bdba5-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bdba5-119">PARAMETERS</span></span>

### <span data-ttu-id="bdba5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdba5-120">-DefaultProfile</span></span>
<span data-ttu-id="bdba5-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bdba5-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdba5-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="bdba5-122">-DisplayName</span></span>
<span data-ttu-id="bdba5-123">Nome visualizzato dell'utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="bdba5-123">The display name of the user to be deleted.</span></span>

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

### <span data-ttu-id="bdba5-124">-Force</span><span class="sxs-lookup"><span data-stu-id="bdba5-124">-Force</span></span>
<span data-ttu-id="bdba5-125">Se specificato, non chiede conferma per l'eliminazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bdba5-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="bdba5-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdba5-126">-InputObject</span></span>
<span data-ttu-id="bdba5-127">L'oggetto utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="bdba5-127">The user object to be deleted.</span></span>

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

### <span data-ttu-id="bdba5-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="bdba5-128">-ObjectId</span></span>
<span data-ttu-id="bdba5-129">ID oggetto dell'utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="bdba5-129">The object id of the user to be deleted.</span></span>

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

### <span data-ttu-id="bdba5-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bdba5-130">-PassThru</span></span>
<span data-ttu-id="bdba5-131">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="bdba5-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="bdba5-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="bdba5-132">-UPNOrObjectId</span></span>
<span data-ttu-id="bdba5-133">Nome dell'entità utente o objectId dell'utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="bdba5-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="bdba5-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="bdba5-134">-UserPrincipalName</span></span>
<span data-ttu-id="bdba5-135">Nome dell'entità utente dell'utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="bdba5-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="bdba5-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bdba5-136">-Confirm</span></span>
<span data-ttu-id="bdba5-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdba5-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdba5-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdba5-138">-WhatIf</span></span>
<span data-ttu-id="bdba5-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bdba5-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdba5-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bdba5-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdba5-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdba5-141">CommonParameters</span></span>
<span data-ttu-id="bdba5-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdba5-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdba5-143">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdba5-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdba5-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bdba5-144">INPUTS</span></span>

### <span data-ttu-id="bdba5-145">System. String</span><span class="sxs-lookup"><span data-stu-id="bdba5-145">System.String</span></span>

### <span data-ttu-id="bdba5-146">Microsoft. Azure. Commands. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="bdba5-146">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="bdba5-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bdba5-147">OUTPUTS</span></span>

### <span data-ttu-id="bdba5-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bdba5-148">System.Boolean</span></span>

## <span data-ttu-id="bdba5-149">Note</span><span class="sxs-lookup"><span data-stu-id="bdba5-149">NOTES</span></span>

## <span data-ttu-id="bdba5-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bdba5-150">RELATED LINKS</span></span>

[<span data-ttu-id="bdba5-151">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="bdba5-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="bdba5-152">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="bdba5-152">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="bdba5-153">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="bdba5-153">Update-AzADUser</span></span>](./Update-AzADUser.md)
