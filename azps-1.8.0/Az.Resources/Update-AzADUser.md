---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
ms.openlocfilehash: 27d97a89aed930dad33cca0ba0382267a3f6d3fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677245"
---
# <span data-ttu-id="32e77-101">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="32e77-101">Update-AzADUser</span></span>

## <span data-ttu-id="32e77-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32e77-102">SYNOPSIS</span></span>
<span data-ttu-id="32e77-103">Aggiorna un utente di Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="32e77-103">Updates an existing active directory user.</span></span>

## <span data-ttu-id="32e77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32e77-104">SYNTAX</span></span>

### <span data-ttu-id="32e77-105">UPNOrObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="32e77-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32e77-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="32e77-106">UPNParameterSet</span></span>
```
Update-AzADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32e77-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="32e77-107">ObjectIdParameterSet</span></span>
```
Update-AzADUser -ObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32e77-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32e77-108">InputObjectParameterSet</span></span>
```
Update-AzADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32e77-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32e77-109">DESCRIPTION</span></span>
<span data-ttu-id="32e77-110">Aggiorna un utente di Active Directory esistente (account aziendale o dell'Istituto di istruzione noto anche come org-ID).</span><span class="sxs-lookup"><span data-stu-id="32e77-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="32e77-111">Per altre informazioni: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="32e77-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="32e77-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32e77-112">EXAMPLES</span></span>

### <span data-ttu-id="32e77-113">Esempio 1-aggiornare il nome visualizzato di un utente con l'ID oggetto</span><span class="sxs-lookup"><span data-stu-id="32e77-113">Example 1 - Update the display name of a user using object id</span></span>

```
PS C:\> Update-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="32e77-114">Aggiorna il nome visualizzato dell'utente con l'ID oggetto "155a5c10-93A9-4941-a0df-96d83ab5ab24" in "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="32e77-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="32e77-115">Esempio 2-aggiornare il nome visualizzato di un utente con il nome dell'entità utente</span><span class="sxs-lookup"><span data-stu-id="32e77-115">Example 2 - Update the display name of a user using user principal name</span></span>

```
PS C:\> Update-AzADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="32e77-116">Aggiorna il nome visualizzato dell'utente con il nome dell'entità utente " foo@domain.com ' per essere" MyNewDisplayName ".</span><span class="sxs-lookup"><span data-stu-id="32e77-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="32e77-117">Esempio 3-aggiornare il nome visualizzato di un utente tramite piping</span><span class="sxs-lookup"><span data-stu-id="32e77-117">Example 3 - Update the display name of a user using piping</span></span>

```
PS C:\> Get-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="32e77-118">Ottiene l'utente con l'ID oggetto "155a5c10-93A9-4941-a0df-96d83ab5ab24" e le pipe al cmdlet Update-AzADUser per aggiornare il nome visualizzato dell'utente in "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="32e77-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="32e77-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32e77-119">PARAMETERS</span></span>

### <span data-ttu-id="32e77-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32e77-120">-DefaultProfile</span></span>
<span data-ttu-id="32e77-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32e77-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32e77-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="32e77-122">-DisplayName</span></span>
<span data-ttu-id="32e77-123">Nuovo nome visualizzato per l'utente.</span><span class="sxs-lookup"><span data-stu-id="32e77-123">New display name for the user.</span></span>

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

### <span data-ttu-id="32e77-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="32e77-124">-EnableAccount</span></span>
<span data-ttu-id="32e77-125">true per l'abilitazione dell'account; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="32e77-125">true for enabling the account; otherwise, false.</span></span>

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

### <span data-ttu-id="32e77-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="32e77-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="32e77-127">Deve essere specificato se l'utente deve cambiare la password nell'accesso successivo riuscito.</span><span class="sxs-lookup"><span data-stu-id="32e77-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="32e77-128">Valido solo se la password viene aggiornata altrimenti verrà ignorata.</span><span class="sxs-lookup"><span data-stu-id="32e77-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="32e77-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32e77-129">-InputObject</span></span>
<span data-ttu-id="32e77-130">Oggetto che rappresenta l'utente da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="32e77-130">The object representing the user to be updated.</span></span>

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

### <span data-ttu-id="32e77-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="32e77-131">-ObjectId</span></span>
<span data-ttu-id="32e77-132">ID oggetto dell'utente da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="32e77-132">The object id of the user to be updated.</span></span>

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

### <span data-ttu-id="32e77-133">-Password</span><span class="sxs-lookup"><span data-stu-id="32e77-133">-Password</span></span>
<span data-ttu-id="32e77-134">Nuova password per l'utente.</span><span class="sxs-lookup"><span data-stu-id="32e77-134">New password for the user.</span></span>

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

### <span data-ttu-id="32e77-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="32e77-135">-UPNOrObjectId</span></span>
<span data-ttu-id="32e77-136">Nome dell'entità utente o ID oggetto dell'utente da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="32e77-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="32e77-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="32e77-137">-UserPrincipalName</span></span>
<span data-ttu-id="32e77-138">Nome dell'entità utente dell'utente da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="32e77-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="32e77-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="32e77-139">-Confirm</span></span>
<span data-ttu-id="32e77-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32e77-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32e77-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32e77-141">-WhatIf</span></span>
<span data-ttu-id="32e77-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32e77-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32e77-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32e77-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32e77-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32e77-144">CommonParameters</span></span>
<span data-ttu-id="32e77-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32e77-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32e77-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32e77-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32e77-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32e77-147">INPUTS</span></span>

### <span data-ttu-id="32e77-148">System. String</span><span class="sxs-lookup"><span data-stu-id="32e77-148">System.String</span></span>

### <span data-ttu-id="32e77-149">Microsoft. Azure. Commands. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="32e77-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

### <span data-ttu-id="32e77-150">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="32e77-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="32e77-151">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="32e77-151">System.Security.SecureString</span></span>

## <span data-ttu-id="32e77-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32e77-152">OUTPUTS</span></span>

### <span data-ttu-id="32e77-153">Microsoft. Azure. Commands. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="32e77-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="32e77-154">Note</span><span class="sxs-lookup"><span data-stu-id="32e77-154">NOTES</span></span>

## <span data-ttu-id="32e77-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32e77-155">RELATED LINKS</span></span>
