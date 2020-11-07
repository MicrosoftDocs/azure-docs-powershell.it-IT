---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F9B2691-BB3F-4644-BD95-6D74777D1E99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADUser.md
ms.openlocfilehash: 2dc9a0d3d41ca1bccb131e92cf514fd2f814943b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856354"
---
# <span data-ttu-id="1abdb-101">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="1abdb-101">Remove-AzADUser</span></span>

## <span data-ttu-id="1abdb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1abdb-102">SYNOPSIS</span></span>
<span data-ttu-id="1abdb-103">Elimina un utente di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="1abdb-103">Deletes an active directory user.</span></span>

## <span data-ttu-id="1abdb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1abdb-104">SYNTAX</span></span>

### <span data-ttu-id="1abdb-105">UPNOrObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1abdb-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Remove-AzADUser -UPNOrObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1abdb-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="1abdb-106">UPNParameterSet</span></span>
```
Remove-AzADUser -UserPrincipalName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1abdb-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1abdb-107">ObjectIdParameterSet</span></span>
```
Remove-AzADUser -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1abdb-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1abdb-108">DisplayNameParameterSet</span></span>
```
Remove-AzADUser -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1abdb-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1abdb-109">InputObjectParameterSet</span></span>
```
Remove-AzADUser -InputObject <PSADUser> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1abdb-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1abdb-110">DESCRIPTION</span></span>
<span data-ttu-id="1abdb-111">Elimina un utente di Active Directory (account aziendale o dell'Istituto di istruzione noto anche come org-ID).</span><span class="sxs-lookup"><span data-stu-id="1abdb-111">Deletes an active directory user (work/school account also popularly known as org-id).</span></span>

## <span data-ttu-id="1abdb-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1abdb-112">EXAMPLES</span></span>

### <span data-ttu-id="1abdb-113">Esempio 1-rimuovere un utente in base al nome dell'entità utente</span><span class="sxs-lookup"><span data-stu-id="1abdb-113">Example 1 - Remove a user by user principal name</span></span>

```
PS C:\> Remove-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="1abdb-114">Rimuove l'utente con il nome dell'entità utente " foo@domain.com " dal tenant.</span><span class="sxs-lookup"><span data-stu-id="1abdb-114">Removes the user with user principal name "foo@domain.com" from the tenant.</span></span>

### <span data-ttu-id="1abdb-115">Esempio 2-rimuovere un utente per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="1abdb-115">Example 2 - Remove a user by object id</span></span>

```
PS C:\> Remove-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69
```

<span data-ttu-id="1abdb-116">Rimuove l'utente con l'ID oggetto "7a9582cf-88c4-4319-842b-7a5d60967a69" dal tenant.</span><span class="sxs-lookup"><span data-stu-id="1abdb-116">Removes the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' from the tenant.</span></span>

### <span data-ttu-id="1abdb-117">Esempio 3-rimuovere un utente tramite pipe</span><span class="sxs-lookup"><span data-stu-id="1abdb-117">Example 3 - Remove a user by piping</span></span>

```
PS C:\> Get-AzADUser -ObjectId 7a9582cf-88c4-4319-842b-7a5d60967a69 | Remove-AzADUser
```

<span data-ttu-id="1abdb-118">Ottiene l'utente con l'ID oggetto "7a9582cf-88c4-4319-842b-7a5d60967a69" e convoglia il cmdlet Remove-AzADUser per rimuovere l'utente dal tenant.</span><span class="sxs-lookup"><span data-stu-id="1abdb-118">Gets the user with object id '7a9582cf-88c4-4319-842b-7a5d60967a69' and pipes that to the Remove-AzADUser cmdlet to remove the user from the tenant.</span></span>

## <span data-ttu-id="1abdb-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1abdb-119">PARAMETERS</span></span>

### <span data-ttu-id="1abdb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1abdb-120">-DefaultProfile</span></span>
<span data-ttu-id="1abdb-121">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1abdb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1abdb-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1abdb-122">-DisplayName</span></span>
<span data-ttu-id="1abdb-123">Nome visualizzato dell'utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="1abdb-123">The display name of the user to be deleted.</span></span>

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

### <span data-ttu-id="1abdb-124">-Force</span><span class="sxs-lookup"><span data-stu-id="1abdb-124">-Force</span></span>
<span data-ttu-id="1abdb-125">Se specificato, non chiede conferma per l'eliminazione dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1abdb-125">If specified, doesn't ask for confirmation for deleting the user.</span></span>

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

### <span data-ttu-id="1abdb-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1abdb-126">-InputObject</span></span>
<span data-ttu-id="1abdb-127">L'oggetto utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="1abdb-127">The user object to be deleted.</span></span>

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

### <span data-ttu-id="1abdb-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1abdb-128">-ObjectId</span></span>
<span data-ttu-id="1abdb-129">ID oggetto dell'utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="1abdb-129">The object id of the user to be deleted.</span></span>

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

### <span data-ttu-id="1abdb-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1abdb-130">-PassThru</span></span>
<span data-ttu-id="1abdb-131">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="1abdb-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1abdb-132">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="1abdb-132">-UPNOrObjectId</span></span>
<span data-ttu-id="1abdb-133">Nome dell'entità utente o objectId dell'utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="1abdb-133">The user principal name or the objectId of the user to be deleted.</span></span>

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

### <span data-ttu-id="1abdb-134">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="1abdb-134">-UserPrincipalName</span></span>
<span data-ttu-id="1abdb-135">Nome dell'entità utente dell'utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="1abdb-135">The user principal name of the user to be deleted.</span></span>

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

### <span data-ttu-id="1abdb-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1abdb-136">-Confirm</span></span>
<span data-ttu-id="1abdb-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1abdb-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1abdb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1abdb-138">-WhatIf</span></span>
<span data-ttu-id="1abdb-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1abdb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1abdb-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1abdb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1abdb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1abdb-141">CommonParameters</span></span>
<span data-ttu-id="1abdb-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1abdb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1abdb-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1abdb-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1abdb-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1abdb-144">INPUTS</span></span>

### <span data-ttu-id="1abdb-145">System. String</span><span class="sxs-lookup"><span data-stu-id="1abdb-145">System.String</span></span>

### <span data-ttu-id="1abdb-146">Microsoft. Azure. Commands. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="1abdb-146">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="1abdb-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1abdb-147">OUTPUTS</span></span>

### <span data-ttu-id="1abdb-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1abdb-148">System.Boolean</span></span>

## <span data-ttu-id="1abdb-149">Note</span><span class="sxs-lookup"><span data-stu-id="1abdb-149">NOTES</span></span>

## <span data-ttu-id="1abdb-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1abdb-150">RELATED LINKS</span></span>

[<span data-ttu-id="1abdb-151">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="1abdb-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="1abdb-152">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="1abdb-152">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="1abdb-153">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="1abdb-153">Set-AzADUser</span></span>](./Set-AzADUser.md)

