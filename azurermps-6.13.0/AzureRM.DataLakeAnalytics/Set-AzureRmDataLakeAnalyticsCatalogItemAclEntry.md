---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: b728f53c34120fb0612f42491007c9d58998da0b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687604"
---
# <span data-ttu-id="69b9d-101">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="69b9d-101">Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="69b9d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69b9d-102">SYNOPSIS</span></span>
<span data-ttu-id="69b9d-103">Modifica una voce nell'ACL di un catalogo o di un elemento di catalogo in data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="69b9d-103">Modifies an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69b9d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69b9d-104">SYNTAX</span></span>

### <span data-ttu-id="69b9d-105">SetCatalogAclEntryForUser (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="69b9d-105">SetCatalogAclEntryForUser (Default)</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69b9d-106">SetCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="69b9d-106">SetCatalogItemAclEntryForUser</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69b9d-107">SetCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="69b9d-107">SetCatalogAclEntryForGroup</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69b9d-108">SetCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="69b9d-108">SetCatalogItemAclEntryForGroup</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -ItemType <String> -Path <CatalogPathInstance> -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69b9d-109">SetCatalogAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="69b9d-109">SetCatalogAclEntryForOther</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69b9d-110">SetCatalogItemAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="69b9d-110">SetCatalogItemAclEntryForOther</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69b9d-111">SetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="69b9d-111">SetCatalogAclEntryForUserOwner</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69b9d-112">SetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="69b9d-112">SetCatalogItemAclEntryForUserOwner</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69b9d-113">SetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="69b9d-113">SetCatalogAclEntryForGroupOwner</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69b9d-114">SetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="69b9d-114">SetCatalogItemAclEntryForGroupOwner</span></span>
```
Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69b9d-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69b9d-115">DESCRIPTION</span></span>
<span data-ttu-id="69b9d-116">Il cmdlet **set-AzureRmDataLakeAnalyticsCatalogItemAclEntry** aggiunge o modifica una voce (ACE) nell'elenco di controllo di accesso (ACL) di un catalogo o di un elemento di catalogo in data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="69b9d-116">The **Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry** cmdlet adds or modifies an entry (ACE) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="69b9d-117">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69b9d-117">EXAMPLES</span></span>

### <span data-ttu-id="69b9d-118">Esempio 1: modificare le autorizzazioni utente per un catalogo</span><span class="sxs-lookup"><span data-stu-id="69b9d-118">Example 1: Modify user permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").Id -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="69b9d-119">Questo comando consente di modificare l'ACE del catalogo per Patti Fuller per avere le autorizzazioni di lettura.</span><span class="sxs-lookup"><span data-stu-id="69b9d-119">This command modifies the catalog ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="69b9d-120">Esempio 2: modificare le autorizzazioni utente per un database</span><span class="sxs-lookup"><span data-stu-id="69b9d-120">Example 2: Modify user Permissions for a database</span></span>
```powershell
PS C:\> Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="69b9d-121">Questo comando modifica la voce di database ACE per Patti Fuller per avere le autorizzazioni di lettura.</span><span class="sxs-lookup"><span data-stu-id="69b9d-121">This command modifies the database ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="69b9d-122">Esempio 3: modificare altre autorizzazioni per un catalogo</span><span class="sxs-lookup"><span data-stu-id="69b9d-122">Example 3: Modify other permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="69b9d-123">Questo comando consente di modificare l'ACE del catalogo per altre autorizzazioni di lettura.</span><span class="sxs-lookup"><span data-stu-id="69b9d-123">This command modifies the catalog ACE for other to have read permissions.</span></span>

### <span data-ttu-id="69b9d-124">Esempio 4: modificare altre autorizzazioni per un database</span><span class="sxs-lookup"><span data-stu-id="69b9d-124">Example 4: Modify other Permissions for a database</span></span>
```powershell
PS C:\> Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

### <span data-ttu-id="69b9d-125">Esempio 5: modificare le autorizzazioni del proprietario utente per un catalogo</span><span class="sxs-lookup"><span data-stu-id="69b9d-125">Example 5: Modify user owner permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -Permissions Read

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="69b9d-126">Questo comando imposta l'autorizzazione proprietario per l'account da leggere.</span><span class="sxs-lookup"><span data-stu-id="69b9d-126">This command sets the owner permission for the account to Read.</span></span>

### <span data-ttu-id="69b9d-127">Esempio 6: modificare le autorizzazioni del proprietario utente per un database</span><span class="sxs-lookup"><span data-stu-id="69b9d-127">Example 6: Modify user owner Permissions for a database</span></span>
```powershell
PS C:\> Set-AzureRmDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName" -Permissions Read

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="69b9d-128">Questo comando imposta l'autorizzazione proprietario per il database da leggere.</span><span class="sxs-lookup"><span data-stu-id="69b9d-128">This command sets the owner permission for the database to Read.</span></span>

## <span data-ttu-id="69b9d-129">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69b9d-129">PARAMETERS</span></span>

### <span data-ttu-id="69b9d-130">-Account</span><span class="sxs-lookup"><span data-stu-id="69b9d-130">-Account</span></span>
<span data-ttu-id="69b9d-131">Specifica il nome dell'account analisi dati lago.</span><span class="sxs-lookup"><span data-stu-id="69b9d-131">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="69b9d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69b9d-132">-DefaultProfile</span></span>
<span data-ttu-id="69b9d-133">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="69b9d-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69b9d-134">-Gruppo</span><span class="sxs-lookup"><span data-stu-id="69b9d-134">-Group</span></span>
<span data-ttu-id="69b9d-135">Impostare l'immissione di ACL del catalogo per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="69b9d-135">Set ACL entry of catalog for group.</span></span>

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

### <span data-ttu-id="69b9d-136">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="69b9d-136">-GroupOwner</span></span>
<span data-ttu-id="69b9d-137">Impostare l'immissione di ACL del catalogo per il proprietario del gruppo.</span><span class="sxs-lookup"><span data-stu-id="69b9d-137">Set ACL entry of catalog for group owner.</span></span>

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

### <span data-ttu-id="69b9d-138">-ItemType</span><span class="sxs-lookup"><span data-stu-id="69b9d-138">-ItemType</span></span>
<span data-ttu-id="69b9d-139">Specifica il tipo di catalogo o degli elementi del catalogo.</span><span class="sxs-lookup"><span data-stu-id="69b9d-139">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="69b9d-140">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="69b9d-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="69b9d-141">Catalogo</span><span class="sxs-lookup"><span data-stu-id="69b9d-141">Catalog</span></span>
- <span data-ttu-id="69b9d-142">Database</span><span class="sxs-lookup"><span data-stu-id="69b9d-142">Database</span></span>

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

### <span data-ttu-id="69b9d-143">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="69b9d-143">-ObjectId</span></span>
<span data-ttu-id="69b9d-144">Identità dell'utente da impostare.</span><span class="sxs-lookup"><span data-stu-id="69b9d-144">The identity of the user to set.</span></span>

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

### <span data-ttu-id="69b9d-145">-Altro</span><span class="sxs-lookup"><span data-stu-id="69b9d-145">-Other</span></span>
<span data-ttu-id="69b9d-146">Impostare l'immissione di ACL del catalogo per altri.</span><span class="sxs-lookup"><span data-stu-id="69b9d-146">Set ACL entry of catalog for other.</span></span>

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

### <span data-ttu-id="69b9d-147">-Path</span><span class="sxs-lookup"><span data-stu-id="69b9d-147">-Path</span></span>
<span data-ttu-id="69b9d-148">Specifica il percorso di analisi dei dati del Lago di un catalogo o un elemento del catalogo.</span><span class="sxs-lookup"><span data-stu-id="69b9d-148">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="69b9d-149">Le parti del percorso devono essere separate da un punto (.).</span><span class="sxs-lookup"><span data-stu-id="69b9d-149">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="69b9d-150">-Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="69b9d-150">-Permissions</span></span>
<span data-ttu-id="69b9d-151">Specifica le autorizzazioni per l'ACE.</span><span class="sxs-lookup"><span data-stu-id="69b9d-151">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="69b9d-152">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="69b9d-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="69b9d-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="69b9d-153">None</span></span>
- <span data-ttu-id="69b9d-154">Leggere</span><span class="sxs-lookup"><span data-stu-id="69b9d-154">Read</span></span>
- <span data-ttu-id="69b9d-155">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="69b9d-155">ReadWrite</span></span>

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

### <span data-ttu-id="69b9d-156">-Utente</span><span class="sxs-lookup"><span data-stu-id="69b9d-156">-User</span></span>
<span data-ttu-id="69b9d-157">Impostare l'immissione di ACL del catalogo per l'utente.</span><span class="sxs-lookup"><span data-stu-id="69b9d-157">Set ACL entry of catalog for user.</span></span>

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

### <span data-ttu-id="69b9d-158">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="69b9d-158">-UserOwner</span></span>
<span data-ttu-id="69b9d-159">Impostare l'immissione di ACL del catalogo per il proprietario dell'utente.</span><span class="sxs-lookup"><span data-stu-id="69b9d-159">Set ACL entry of catalog for user owner.</span></span>

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

### <span data-ttu-id="69b9d-160">-Confermare</span><span class="sxs-lookup"><span data-stu-id="69b9d-160">-Confirm</span></span>
<span data-ttu-id="69b9d-161">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69b9d-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69b9d-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69b9d-162">-WhatIf</span></span>
<span data-ttu-id="69b9d-163">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69b9d-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69b9d-164">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69b9d-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69b9d-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69b9d-165">CommonParameters</span></span>
<span data-ttu-id="69b9d-166">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69b9d-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69b9d-167">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69b9d-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69b9d-168">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69b9d-168">INPUTS</span></span>

### <span data-ttu-id="69b9d-169">System. String</span><span class="sxs-lookup"><span data-stu-id="69b9d-169">System.String</span></span>

### <span data-ttu-id="69b9d-170">System. Guid</span><span class="sxs-lookup"><span data-stu-id="69b9d-170">System.Guid</span></span>

### <span data-ttu-id="69b9d-171">Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="69b9d-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

### <span data-ttu-id="69b9d-172">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsEnums + PermissionType</span><span class="sxs-lookup"><span data-stu-id="69b9d-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span></span>

## <span data-ttu-id="69b9d-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69b9d-173">OUTPUTS</span></span>

### <span data-ttu-id="69b9d-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="69b9d-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="69b9d-175">Note</span><span class="sxs-lookup"><span data-stu-id="69b9d-175">NOTES</span></span>

## <span data-ttu-id="69b9d-176">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69b9d-176">RELATED LINKS</span></span>

[<span data-ttu-id="69b9d-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="69b9d-177">Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="69b9d-178">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="69b9d-178">Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzureRmDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="69b9d-179">U-SQL offre ora il controllo di accesso a livello di database</span><span class="sxs-lookup"><span data-stu-id="69b9d-179">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)
