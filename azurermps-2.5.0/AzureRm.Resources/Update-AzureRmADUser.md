---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/update-azurermaduser
schema: 2.0.0
ms.openlocfilehash: 504ce8bd2c7ae5dce3fe859d678b27ad829b2932
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866192"
---
# <span data-ttu-id="0150a-101">Update-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="0150a-101">Update-AzureRmADUser</span></span>

## <span data-ttu-id="0150a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0150a-102">SYNOPSIS</span></span>
<span data-ttu-id="0150a-103">Aggiorna un utente di Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="0150a-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0150a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0150a-104">SYNTAX</span></span>

### <span data-ttu-id="0150a-105">UPNOrObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0150a-105">UPNOrObjectIdParameterSet (Default)</span></span>
```
Update-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0150a-106">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0150a-106">UPNParameterSet</span></span>
```
Update-AzureRmADUser -UserPrincipalName <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0150a-107">ObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0150a-107">ObjectIdParameterSet</span></span>
```
Update-AzureRmADUser -ObjectId <Guid> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0150a-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0150a-108">InputObjectParameterSet</span></span>
```
Update-AzureRmADUser -InputObject <PSADUser> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0150a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0150a-109">DESCRIPTION</span></span>
<span data-ttu-id="0150a-110">Aggiorna un utente di Active Directory esistente (account aziendale o dell'Istituto di istruzione noto anche come org-ID).</span><span class="sxs-lookup"><span data-stu-id="0150a-110">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="0150a-111">Per altre informazioni: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="0150a-111">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="0150a-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0150a-112">EXAMPLES</span></span>

### <span data-ttu-id="0150a-113">Esempio 1-aggiornare il nome visualizzato di un utente con l'ID oggetto</span><span class="sxs-lookup"><span data-stu-id="0150a-113">Example 1 - Update the display name of a user using object id</span></span>

```
PS C:\> Update-AzureRmADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 -DisplayName MyNewDisplayName
```

<span data-ttu-id="0150a-114">Aggiorna il nome visualizzato dell'utente con l'ID oggetto "155a5c10-93A9-4941-a0df-96d83ab5ab24" in "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="0150a-114">Updates the display name of the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="0150a-115">Esempio 2-aggiornare il nome visualizzato di un utente con il nome dell'entità utente</span><span class="sxs-lookup"><span data-stu-id="0150a-115">Example 2 - Update the display name of a user using user principal name</span></span>

```
PS C:\> Update-AzureRmADUser -UserPrincipalName foo@domain.com -DisplayName MyNewDisplayName
```

<span data-ttu-id="0150a-116">Aggiorna il nome visualizzato dell'utente con il nome dell'entità utente " foo@domain.com ' per essere" MyNewDisplayName ".</span><span class="sxs-lookup"><span data-stu-id="0150a-116">Updates the display name of the user with user principal name 'foo@domain.com' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="0150a-117">Esempio 3-aggiornare il nome visualizzato di un utente tramite piping</span><span class="sxs-lookup"><span data-stu-id="0150a-117">Example 3 - Update the display name of a user using piping</span></span>

```
PS C:\> Get-AzureRmADUser -ObjectId 155a5c10-93a9-4941-a0df-96d83ab5ab24 | Update-AzureRmADUser -DisplayName MyNewDisplayName
```

<span data-ttu-id="0150a-118">Ottiene l'utente con l'ID oggetto "155a5c10-93A9-4941-a0df-96d83ab5ab24" e le pipe al cmdlet Update-AzureRmADUser per aggiornare il nome visualizzato dell'utente in "MyNewDisplayName".</span><span class="sxs-lookup"><span data-stu-id="0150a-118">Gets the user with object id '155a5c10-93a9-4941-a0df-96d83ab5ab24' and pipes that to the Update-AzureRmADUser cmdlet to update the display name of that user to 'MyNewDisplayName'.</span></span>

## <span data-ttu-id="0150a-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0150a-119">PARAMETERS</span></span>

### <span data-ttu-id="0150a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0150a-120">-DefaultProfile</span></span>
<span data-ttu-id="0150a-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0150a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0150a-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0150a-122">-DisplayName</span></span>
<span data-ttu-id="0150a-123">Nuovo nome visualizzato per l'utente.</span><span class="sxs-lookup"><span data-stu-id="0150a-123">New display name for the user.</span></span>

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

### <span data-ttu-id="0150a-124">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="0150a-124">-EnableAccount</span></span>
<span data-ttu-id="0150a-125">true per l'abilitazione dell'account; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="0150a-125">true for enabling the account; otherwise, false.</span></span>

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

### <span data-ttu-id="0150a-126">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="0150a-126">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="0150a-127">Deve essere specificato se l'utente deve cambiare la password nell'accesso successivo riuscito.</span><span class="sxs-lookup"><span data-stu-id="0150a-127">It must be specified if the user should change the password on the next successful login.</span></span>
<span data-ttu-id="0150a-128">Valido solo se la password viene aggiornata altrimenti verrà ignorata.</span><span class="sxs-lookup"><span data-stu-id="0150a-128">Only valid if password is updated otherwise it will be ignored.</span></span>

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

### <span data-ttu-id="0150a-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0150a-129">-InputObject</span></span>
<span data-ttu-id="0150a-130">Oggetto che rappresenta l'utente da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="0150a-130">The object representing the user to be updated.</span></span>

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

### <span data-ttu-id="0150a-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0150a-131">-ObjectId</span></span>
<span data-ttu-id="0150a-132">ID oggetto dell'utente da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="0150a-132">The object id of the user to be updated.</span></span>

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

### <span data-ttu-id="0150a-133">-Password</span><span class="sxs-lookup"><span data-stu-id="0150a-133">-Password</span></span>
<span data-ttu-id="0150a-134">Nuova password per l'utente.</span><span class="sxs-lookup"><span data-stu-id="0150a-134">New password for the user.</span></span>

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

### <span data-ttu-id="0150a-135">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="0150a-135">-UPNOrObjectId</span></span>
<span data-ttu-id="0150a-136">Nome dell'entità utente o ID oggetto dell'utente da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="0150a-136">The user principal name or object id of the user to be updated.</span></span>

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

### <span data-ttu-id="0150a-137">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="0150a-137">-UserPrincipalName</span></span>
<span data-ttu-id="0150a-138">Nome dell'entità utente dell'utente da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="0150a-138">The user principal name of the user to be updated.</span></span>

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

### <span data-ttu-id="0150a-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0150a-139">-Confirm</span></span>
<span data-ttu-id="0150a-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0150a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0150a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0150a-141">-WhatIf</span></span>
<span data-ttu-id="0150a-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0150a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0150a-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0150a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0150a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0150a-144">CommonParameters</span></span>
<span data-ttu-id="0150a-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0150a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0150a-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0150a-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0150a-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0150a-147">INPUTS</span></span>

### <span data-ttu-id="0150a-148">System. String</span><span class="sxs-lookup"><span data-stu-id="0150a-148">System.String</span></span>

### <span data-ttu-id="0150a-149">System. Guid</span><span class="sxs-lookup"><span data-stu-id="0150a-149">System.Guid</span></span>

### <span data-ttu-id="0150a-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="0150a-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>
<span data-ttu-id="0150a-151">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0150a-151">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0150a-152">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="0150a-152">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="0150a-153">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="0150a-153">System.Security.SecureString</span></span>

## <span data-ttu-id="0150a-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0150a-154">OUTPUTS</span></span>

### <span data-ttu-id="0150a-155">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="0150a-155">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="0150a-156">Note</span><span class="sxs-lookup"><span data-stu-id="0150a-156">NOTES</span></span>

## <span data-ttu-id="0150a-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0150a-157">RELATED LINKS</span></span>
