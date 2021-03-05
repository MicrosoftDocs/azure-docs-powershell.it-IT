---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: a4569f8ce570a537896c4c39b916aca271111f06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991435"
---
# <span data-ttu-id="9cc86-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="9cc86-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="9cc86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cc86-102">SYNOPSIS</span></span>
<span data-ttu-id="9cc86-103">Modifica una voce nell'ACL di un catalogo o di un elemento del catalogo in Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9cc86-103">Modifies an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="9cc86-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9cc86-104">SYNTAX</span></span>

### <span data-ttu-id="9cc86-105">SetCatalogAclEntryForUser (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9cc86-105">SetCatalogAclEntryForUser (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9cc86-106">SetCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="9cc86-106">SetCatalogItemAclEntryForUser</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cc86-107">SetCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="9cc86-107">SetCatalogAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9cc86-108">SetCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="9cc86-108">SetCatalogItemAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cc86-109">SetCatalogAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="9cc86-109">SetCatalogAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cc86-110">SetCatalogItemAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="9cc86-110">SetCatalogItemAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cc86-111">SetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="9cc86-111">SetCatalogAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cc86-112">SetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="9cc86-112">SetCatalogItemAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cc86-113">SetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="9cc86-113">SetCatalogAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cc86-114">SetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="9cc86-114">SetCatalogItemAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cc86-115">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9cc86-115">DESCRIPTION</span></span>
<span data-ttu-id="9cc86-116">Il cmdlet **Set-AzDataLakeAnalyticsCatalogItemAclEntry** aggiunge o modifica una voce (ACE) nell'elenco di controllo di accesso (ACL) di un catalogo o di un elemento del catalogo in Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9cc86-116">The **Set-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet adds or modifies an entry (ACE) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="9cc86-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9cc86-117">EXAMPLES</span></span>

### <span data-ttu-id="9cc86-118">Esempio 1: Modificare le autorizzazioni utente per un catalogo</span><span class="sxs-lookup"><span data-stu-id="9cc86-118">Example 1: Modify user permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="9cc86-119">Questo comando modifica l'ACE del catalogo per fare in modo che Patti Fuller abbia le autorizzazioni di lettura.</span><span class="sxs-lookup"><span data-stu-id="9cc86-119">This command modifies the catalog ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="9cc86-120">Esempio 2: Modificare le autorizzazioni utente per un database</span><span class="sxs-lookup"><span data-stu-id="9cc86-120">Example 2: Modify user Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="9cc86-121">Questo comando modifica l'ACE del database per fare in modo che Patti Fuller abbia le autorizzazioni di lettura.</span><span class="sxs-lookup"><span data-stu-id="9cc86-121">This command modifies the database ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="9cc86-122">Esempio 3: Modificare altre autorizzazioni per un catalogo</span><span class="sxs-lookup"><span data-stu-id="9cc86-122">Example 3: Modify other permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="9cc86-123">Questo comando modifica l'elenco di accesso (ACE) del catalogo per concedere ad altri utenti le autorizzazioni di lettura.</span><span class="sxs-lookup"><span data-stu-id="9cc86-123">This command modifies the catalog ACE for other to have read permissions.</span></span>

### <span data-ttu-id="9cc86-124">Esempio 4: Modificare altre autorizzazioni per un database</span><span class="sxs-lookup"><span data-stu-id="9cc86-124">Example 4: Modify other Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

### <span data-ttu-id="9cc86-125">Esempio 5: Modificare le autorizzazioni di proprietario utente per un catalogo</span><span class="sxs-lookup"><span data-stu-id="9cc86-125">Example 5: Modify user owner permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -Permissions Read

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="9cc86-126">Questo comando imposta l'autorizzazione di proprietario per l'account su Lettura.</span><span class="sxs-lookup"><span data-stu-id="9cc86-126">This command sets the owner permission for the account to Read.</span></span>

### <span data-ttu-id="9cc86-127">Esempio 6: Modificare le autorizzazioni di proprietario utente per un database</span><span class="sxs-lookup"><span data-stu-id="9cc86-127">Example 6: Modify user owner Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName" -Permissions Read

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="9cc86-128">Questo comando imposta l'autorizzazione di proprietario per il database su Lettura.</span><span class="sxs-lookup"><span data-stu-id="9cc86-128">This command sets the owner permission for the database to Read.</span></span>

## <span data-ttu-id="9cc86-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cc86-129">PARAMETERS</span></span>

### <span data-ttu-id="9cc86-130">-Account</span><span class="sxs-lookup"><span data-stu-id="9cc86-130">-Account</span></span>
<span data-ttu-id="9cc86-131">Specifica il nome dell'account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9cc86-131">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc86-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cc86-132">-DefaultProfile</span></span>
<span data-ttu-id="9cc86-133">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9cc86-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cc86-134">-Group</span><span class="sxs-lookup"><span data-stu-id="9cc86-134">-Group</span></span>
<span data-ttu-id="9cc86-135">Impostare la voce ACL del catalogo per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="9cc86-135">Set ACL entry of catalog for group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForGroup, SetCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc86-136">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="9cc86-136">-GroupOwner</span></span>
<span data-ttu-id="9cc86-137">Impostare la voce ACL del catalogo per il proprietario del gruppo.</span><span class="sxs-lookup"><span data-stu-id="9cc86-137">Set ACL entry of catalog for group owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForGroupOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc86-138">-ItemType</span><span class="sxs-lookup"><span data-stu-id="9cc86-138">-ItemType</span></span>
<span data-ttu-id="9cc86-139">Specifica il tipo di catalogo o di elementi del catalogo.</span><span class="sxs-lookup"><span data-stu-id="9cc86-139">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="9cc86-140">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="9cc86-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9cc86-141">Catalogo</span><span class="sxs-lookup"><span data-stu-id="9cc86-141">Catalog</span></span>
- <span data-ttu-id="9cc86-142">Database</span><span class="sxs-lookup"><span data-stu-id="9cc86-142">Database</span></span>

```yaml
Type: System.String
Parameter Sets: SetCatalogItemAclEntryForUser, SetCatalogItemAclEntryForGroup, SetCatalogItemAclEntryForOther, SetCatalogItemAclEntryForUserOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc86-143">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9cc86-143">-ObjectId</span></span>
<span data-ttu-id="9cc86-144">Identità dell'utente da impostare.</span><span class="sxs-lookup"><span data-stu-id="9cc86-144">The identity of the user to set.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SetCatalogAclEntryForUser, SetCatalogItemAclEntryForUser, SetCatalogAclEntryForGroup, SetCatalogItemAclEntryForGroup
Aliases: Id, UserId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc86-145">-Altro</span><span class="sxs-lookup"><span data-stu-id="9cc86-145">-Other</span></span>
<span data-ttu-id="9cc86-146">Impostare l'Immissione ACL del catalogo per altri elementi.</span><span class="sxs-lookup"><span data-stu-id="9cc86-146">Set ACL entry of catalog for other.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForOther, SetCatalogItemAclEntryForOther
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc86-147">-Path</span><span class="sxs-lookup"><span data-stu-id="9cc86-147">-Path</span></span>
<span data-ttu-id="9cc86-148">Specifica il percorso Data Lake Analytics di un catalogo o di un elemento del catalogo.</span><span class="sxs-lookup"><span data-stu-id="9cc86-148">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="9cc86-149">Le parti del percorso devono essere separate da un punto (.).</span><span class="sxs-lookup"><span data-stu-id="9cc86-149">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: SetCatalogItemAclEntryForUser, SetCatalogItemAclEntryForGroup, SetCatalogItemAclEntryForOther, SetCatalogItemAclEntryForUserOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc86-150">-Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="9cc86-150">-Permissions</span></span>
<span data-ttu-id="9cc86-151">Specifica le autorizzazioni per l'elenco di controllo di accesso.</span><span class="sxs-lookup"><span data-stu-id="9cc86-151">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="9cc86-152">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="9cc86-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9cc86-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9cc86-153">None</span></span>
- <span data-ttu-id="9cc86-154">Lettura</span><span class="sxs-lookup"><span data-stu-id="9cc86-154">Read</span></span>
- <span data-ttu-id="9cc86-155">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9cc86-155">ReadWrite</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, ReadWrite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9cc86-156">-Utente</span><span class="sxs-lookup"><span data-stu-id="9cc86-156">-User</span></span>
<span data-ttu-id="9cc86-157">Impostare la voce ACL del catalogo per l'utente.</span><span class="sxs-lookup"><span data-stu-id="9cc86-157">Set ACL entry of catalog for user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForUser, SetCatalogItemAclEntryForUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc86-158">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="9cc86-158">-UserOwner</span></span>
<span data-ttu-id="9cc86-159">Impostare la voce ACL del catalogo per il proprietario dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9cc86-159">Set ACL entry of catalog for user owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForUserOwner, SetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9cc86-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9cc86-160">-Confirm</span></span>
<span data-ttu-id="9cc86-161">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cc86-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cc86-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cc86-162">-WhatIf</span></span>
<span data-ttu-id="9cc86-163">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9cc86-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cc86-164">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9cc86-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cc86-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cc86-165">CommonParameters</span></span>
<span data-ttu-id="9cc86-166">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cc86-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cc86-167">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cc86-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cc86-168">INPUT</span><span class="sxs-lookup"><span data-stu-id="9cc86-168">INPUTS</span></span>

### <span data-ttu-id="9cc86-169">System.String</span><span class="sxs-lookup"><span data-stu-id="9cc86-169">System.String</span></span>

### <span data-ttu-id="9cc86-170">System.Guid</span><span class="sxs-lookup"><span data-stu-id="9cc86-170">System.Guid</span></span>

### <span data-ttu-id="9cc86-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="9cc86-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

### <span data-ttu-id="9cc86-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span><span class="sxs-lookup"><span data-stu-id="9cc86-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span></span>

## <span data-ttu-id="9cc86-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9cc86-173">OUTPUTS</span></span>

### <span data-ttu-id="9cc86-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="9cc86-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="9cc86-175">NOTE</span><span class="sxs-lookup"><span data-stu-id="9cc86-175">NOTES</span></span>

## <span data-ttu-id="9cc86-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9cc86-176">RELATED LINKS</span></span>

[<span data-ttu-id="9cc86-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="9cc86-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="9cc86-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="9cc86-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="9cc86-179">U-SQL offre ora il controllo dell'accesso a livello di database</span><span class="sxs-lookup"><span data-stu-id="9cc86-179">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)
