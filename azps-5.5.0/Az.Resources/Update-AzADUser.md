---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
ms.openlocfilehash: b765e33479c6178d69fb670a2f18ef0169eadf35
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205954"
---
# <span data-ttu-id="10e98-101">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="10e98-101">Update-AzADUser</span></span>

## <span data-ttu-id="10e98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10e98-102">SYNOPSIS</span></span>
<span data-ttu-id="10e98-103">Aggiorna un utente active directory esistente.</span><span class="sxs-lookup"><span data-stu-id="10e98-103">Updates an existing active directory user.</span></span>

## <span data-ttu-id="10e98-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10e98-104">SYNTAX</span></span>

### <span data-ttu-id="10e98-105">UPNOrObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="10e98-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10e98-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="10e98-106">UPNParameterSet</span></span>
```
Update-AzADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10e98-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10e98-107">ObjectIdParameterSet</span></span>
```
Update-AzADUser -ObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="10e98-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10e98-108">InputObjectParameterSet</span></span>
```
Update-AzADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="10e98-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="10e98-109">DESCRIPTION</span></span>
<span data-ttu-id="10e98-110">Aggiorna un utente active directory esistente (account aziendale o dell'istituto di istruzione noto anche come org-id).</span><span class="sxs-lookup"><span data-stu-id="10e98-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="10e98-111">Per altre informazioni: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="10e98-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="10e98-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10e98-112">EXAMPLES</span></span>

### <span data-ttu-id="10e98-113">Esempio 1: Aggiornare il nome visualizzato di un utente usando l'ID oggetto</span><span class="sxs-lookup"><span data-stu-id="10e98-113">Example 1: Update the display name of a user using object id</span></span>

```powershell
PS C:\> Update-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="10e98-114">Aggiorna il nome visualizzato dell'utente il cui ID oggetto '155a5c10-93a9-4941-a0df-96d83ab5ab24' sarà "NomeVisualizzazioneNuovo".</span><span class="sxs-lookup"><span data-stu-id="10e98-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="10e98-115">Esempio 2: Aggiornare il nome visualizzato di un utente usando il nome dell'entità utente</span><span class="sxs-lookup"><span data-stu-id="10e98-115">Example 2: Update the display name of a user using user principal name</span></span>

```powershell
PS C:\> Update-AzADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="10e98-116">Aggiorna il nome visualizzato dell'utente con il nome dell'entità utente foo@domain.com ' ' da 'MyNewDisplayName'.</span><span class="sxs-lookup"><span data-stu-id="10e98-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="10e98-117">Esempio 3: Aggiornare il nome visualizzato di un utente tramite piping</span><span class="sxs-lookup"><span data-stu-id="10e98-117">Example 3: Update the display name of a user using piping</span></span>

```powershell
PS C:\> Get-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="10e98-118">Recupera l'utente con ID oggetto '155a5c10-93a9-4941-a0df-96d83ab5ab24' e pipe che al cmdlet di Update-AzADUser per aggiornare il nome visualizzato dell'utente in "NomeVisualizzazioneElizza".</span><span class="sxs-lookup"><span data-stu-id="10e98-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="10e98-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="10e98-119">PARAMETERS</span></span>

### <span data-ttu-id="10e98-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10e98-120">-DefaultProfile</span></span>
<span data-ttu-id="10e98-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="10e98-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10e98-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="10e98-122">-DisplayName</span></span>
<span data-ttu-id="10e98-123">Nuovo nome visualizzato per l'utente.</span><span class="sxs-lookup"><span data-stu-id="10e98-123">New display name for the user.</span></span>

```yaml
Type: System.String
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10e98-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="10e98-124">-EnableAccount</span></span>
<span data-ttu-id="10e98-125">true per abilitare l'account; in caso contrario false.</span><span class="sxs-lookup"><span data-stu-id="10e98-125">true for enabling the account; otherwise, false.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10e98-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="10e98-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="10e98-127">Deve essere specificato se l'utente deve cambiare la password al successivo accesso riuscito.</span><span class="sxs-lookup"><span data-stu-id="10e98-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="10e98-128">Valido solo se la password viene aggiornata, altrimenti verrà ignorata.</span><span class="sxs-lookup"><span data-stu-id="10e98-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="10e98-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="10e98-129">-InputObject</span></span>
<span data-ttu-id="10e98-130">Oggetto che rappresenta l'utente da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="10e98-130">The object representing the user to be updated.</span></span>

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

### <span data-ttu-id="10e98-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="10e98-131">-ObjectId</span></span>
<span data-ttu-id="10e98-132">ID oggetto dell'utente da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="10e98-132">The object id of the user to be updated.</span></span>

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

### <span data-ttu-id="10e98-133">-Password</span><span class="sxs-lookup"><span data-stu-id="10e98-133">-Password</span></span>
<span data-ttu-id="10e98-134">Nuova password per l'utente.</span><span class="sxs-lookup"><span data-stu-id="10e98-134">New password for the user.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: UPNOrObjectIdParameterSet, UPNParameterSet, ObjectIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10e98-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="10e98-135">-UPNOrObjectId</span></span>
<span data-ttu-id="10e98-136">Il nome dell'entità utente o l'ID oggetto dell'utente da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="10e98-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="10e98-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="10e98-137">-UserPrincipalName</span></span>
<span data-ttu-id="10e98-138">Il nome dell'entità utente dell'utente da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="10e98-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="10e98-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="10e98-139">-Confirm</span></span>
<span data-ttu-id="10e98-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10e98-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10e98-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10e98-141">-WhatIf</span></span>
<span data-ttu-id="10e98-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10e98-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10e98-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="10e98-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10e98-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10e98-144">CommonParameters</span></span>
<span data-ttu-id="10e98-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10e98-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10e98-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="10e98-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10e98-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="10e98-147">INPUTS</span></span>

### <span data-ttu-id="10e98-148">System.String</span><span class="sxs-lookup"><span data-stu-id="10e98-148">System.String</span></span>

### <span data-ttu-id="10e98-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="10e98-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

### <span data-ttu-id="10e98-150">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="10e98-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="10e98-151">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="10e98-151">System.Security.SecureString</span></span>

## <span data-ttu-id="10e98-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10e98-152">OUTPUTS</span></span>

### <span data-ttu-id="10e98-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="10e98-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="10e98-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="10e98-154">NOTES</span></span>

## <span data-ttu-id="10e98-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10e98-155">RELATED LINKS</span></span>
