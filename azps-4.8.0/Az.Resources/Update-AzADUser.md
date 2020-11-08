---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADUser.md
ms.openlocfilehash: b765e33479c6178d69fb670a2f18ef0169eadf35
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189357"
---
# <span data-ttu-id="a9109-101">Update-AzADUser</span><span class="sxs-lookup"><span data-stu-id="a9109-101">Update-AzADUser</span></span>

## <span data-ttu-id="a9109-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9109-102">SYNOPSIS</span></span>
<span data-ttu-id="a9109-103">Aggiorna un utente di Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="a9109-103">Updates an existing active directory user.</span></span>

## <span data-ttu-id="a9109-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9109-104">SYNTAX</span></span>

### <span data-ttu-id="a9109-105">UPNOrObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a9109-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9109-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9109-106">UPNParameterSet</span></span>
```
Update-AzADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9109-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9109-107">ObjectIdParameterSet</span></span>
```
Update-AzADUser -ObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9109-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9109-108">InputObjectParameterSet</span></span>
```
Update-AzADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9109-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9109-109">DESCRIPTION</span></span>
<span data-ttu-id="a9109-110">Aggiorna un utente di Active Directory esistente (account aziendale o dell'Istituto di istruzione noto anche come org-ID).</span><span class="sxs-lookup"><span data-stu-id="a9109-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="a9109-111">Per altre informazioni: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="a9109-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="a9109-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9109-112">EXAMPLES</span></span>

### <span data-ttu-id="a9109-113">Esempio 1: aggiornare il nome visualizzato di un utente con l'ID oggetto</span><span class="sxs-lookup"><span data-stu-id="a9109-113">Example 1: Update the display name of a user using object id</span></span>

```powershell
PS C:\> Update-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="a9109-114">Aggiorna il nome visualizzato dell'utente con l'ID oggetto "155a5c10-93A9-4941-a0df-96d83ab5ab24" in "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="a9109-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="a9109-115">Esempio 2: aggiornare il nome visualizzato di un utente con il nome dell'entità utente</span><span class="sxs-lookup"><span data-stu-id="a9109-115">Example 2: Update the display name of a user using user principal name</span></span>

```powershell
PS C:\> Update-AzADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="a9109-116">Aggiorna il nome visualizzato dell'utente con il nome dell'entità utente " foo@domain.com ' per essere" MyNewDisplayName ".</span><span class="sxs-lookup"><span data-stu-id="a9109-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="a9109-117">Esempio 3: aggiornare il nome visualizzato di un utente tramite piping</span><span class="sxs-lookup"><span data-stu-id="a9109-117">Example 3: Update the display name of a user using piping</span></span>

```powershell
PS C:\> Get-AzADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="a9109-118">Ottiene l'utente con l'ID oggetto "155a5c10-93A9-4941-a0df-96d83ab5ab24" e le pipe al cmdlet Update-AzADUser per aggiornare il nome visualizzato dell'utente in "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="a9109-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="a9109-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9109-119">PARAMETERS</span></span>

### <span data-ttu-id="a9109-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9109-120">-DefaultProfile</span></span>
<span data-ttu-id="a9109-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a9109-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9109-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a9109-122">-DisplayName</span></span>
<span data-ttu-id="a9109-123">Nuovo nome visualizzato per l'utente.</span><span class="sxs-lookup"><span data-stu-id="a9109-123">New display name for the user.</span></span>

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

### <span data-ttu-id="a9109-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="a9109-124">-EnableAccount</span></span>
<span data-ttu-id="a9109-125">true per l'abilitazione dell'account; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="a9109-125">true for enabling the account; otherwise, false.</span></span>

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

### <span data-ttu-id="a9109-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="a9109-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="a9109-127">Deve essere specificato se l'utente deve cambiare la password nell'accesso successivo riuscito.</span><span class="sxs-lookup"><span data-stu-id="a9109-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="a9109-128">Valido solo se la password viene aggiornata altrimenti verrà ignorata.</span><span class="sxs-lookup"><span data-stu-id="a9109-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="a9109-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9109-129">-InputObject</span></span>
<span data-ttu-id="a9109-130">Oggetto che rappresenta l'utente da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="a9109-130">The object representing the user to be updated.</span></span>

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

### <span data-ttu-id="a9109-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a9109-131">-ObjectId</span></span>
<span data-ttu-id="a9109-132">ID oggetto dell'utente da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="a9109-132">The object id of the user to be updated.</span></span>

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

### <span data-ttu-id="a9109-133">-Password</span><span class="sxs-lookup"><span data-stu-id="a9109-133">-Password</span></span>
<span data-ttu-id="a9109-134">Nuova password per l'utente.</span><span class="sxs-lookup"><span data-stu-id="a9109-134">New password for the user.</span></span>

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

### <span data-ttu-id="a9109-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="a9109-135">-UPNOrObjectId</span></span>
<span data-ttu-id="a9109-136">Nome dell'entità utente o ID oggetto dell'utente da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="a9109-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="a9109-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a9109-137">-UserPrincipalName</span></span>
<span data-ttu-id="a9109-138">Nome dell'entità utente dell'utente da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="a9109-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="a9109-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a9109-139">-Confirm</span></span>
<span data-ttu-id="a9109-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9109-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9109-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9109-141">-WhatIf</span></span>
<span data-ttu-id="a9109-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9109-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9109-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9109-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9109-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9109-144">CommonParameters</span></span>
<span data-ttu-id="a9109-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9109-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9109-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9109-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9109-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9109-147">INPUTS</span></span>

### <span data-ttu-id="a9109-148">System. String</span><span class="sxs-lookup"><span data-stu-id="a9109-148">System.String</span></span>

### <span data-ttu-id="a9109-149">Microsoft. Azure. Commands. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="a9109-149">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

### <span data-ttu-id="a9109-150">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a9109-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a9109-151">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="a9109-151">System.Security.SecureString</span></span>

## <span data-ttu-id="a9109-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9109-152">OUTPUTS</span></span>

### <span data-ttu-id="a9109-153">Microsoft. Azure. Commands. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="a9109-153">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="a9109-154">Note</span><span class="sxs-lookup"><span data-stu-id="a9109-154">NOTES</span></span>

## <span data-ttu-id="a9109-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9109-155">RELATED LINKS</span></span>
