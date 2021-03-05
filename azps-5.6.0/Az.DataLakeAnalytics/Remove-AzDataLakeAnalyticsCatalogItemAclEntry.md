---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 968acf65d0f3e045614b5ade094bb50c90acac46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963134"
---
# <span data-ttu-id="39cb2-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="39cb2-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="39cb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39cb2-102">SYNOPSIS</span></span>
<span data-ttu-id="39cb2-103">Elimina una voce dall'ACL di un catalogo o di un elemento del catalogo in Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="39cb2-103">Deletes an entry from the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="39cb2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="39cb2-104">SYNTAX</span></span>

### <span data-ttu-id="39cb2-105">RemoveCatalogAclEntryForUser (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="39cb2-105">RemoveCatalogAclEntryForUser (Default)</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39cb2-106">RemoveCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="39cb2-106">RemoveCatalogItemAclEntryForUser</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39cb2-107">RemoveCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="39cb2-107">RemoveCatalogAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39cb2-108">RemoveCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="39cb2-108">RemoveCatalogItemAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39cb2-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="39cb2-109">DESCRIPTION</span></span>
<span data-ttu-id="39cb2-110">Il cmdlet **Remove-AzDataLakeAnalyticsCatalogItemAclEntry** rimuove una voce (ACE) dall'elenco di controllo di accesso (ACL) di un catalogo o di un elemento del catalogo in Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="39cb2-110">The **Remove-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="39cb2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="39cb2-111">EXAMPLES</span></span>

### <span data-ttu-id="39cb2-112">Esempio 1: Rimuovere l'ACL dell'utente per un catalogo</span><span class="sxs-lookup"><span data-stu-id="39cb2-112">Example 1: Remove the user ACL for a catalog</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id
```

<span data-ttu-id="39cb2-113">Questo comando rimuove l'ACL del catalogo per Patti Fuller dell'account contosoadla.</span><span class="sxs-lookup"><span data-stu-id="39cb2-113">This command removes the catalog ACL for Patti Fuller of the contosoadla account.</span></span>

### <span data-ttu-id="39cb2-114">Esempio 2: Rimuovere l'ACL dell'utente per un database</span><span class="sxs-lookup"><span data-stu-id="39cb2-114">Example 2: Remove the user ACL for a database</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName"
```

<span data-ttu-id="39cb2-115">Questo comando rimuove l'ACL di database per Patti Fuller dell'account contosoadla.</span><span class="sxs-lookup"><span data-stu-id="39cb2-115">This command removes the database ACL for Patti Fuller of the contosoadla account.</span></span>

## <span data-ttu-id="39cb2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39cb2-116">PARAMETERS</span></span>

### <span data-ttu-id="39cb2-117">-Account</span><span class="sxs-lookup"><span data-stu-id="39cb2-117">-Account</span></span>
<span data-ttu-id="39cb2-118">Specifica il nome dell'account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="39cb2-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="39cb2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39cb2-119">-DefaultProfile</span></span>
<span data-ttu-id="39cb2-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="39cb2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39cb2-121">-Group</span><span class="sxs-lookup"><span data-stu-id="39cb2-121">-Group</span></span>
<span data-ttu-id="39cb2-122">Rimuovere la voce ACL del catalogo per il gruppo.</span><span class="sxs-lookup"><span data-stu-id="39cb2-122">Remove ACL entry of catalog for group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveCatalogAclEntryForGroup, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39cb2-123">-ItemType</span><span class="sxs-lookup"><span data-stu-id="39cb2-123">-ItemType</span></span>
<span data-ttu-id="39cb2-124">Specifica il tipo di catalogo o di elementi del catalogo.</span><span class="sxs-lookup"><span data-stu-id="39cb2-124">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="39cb2-125">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="39cb2-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="39cb2-126">Catalogo</span><span class="sxs-lookup"><span data-stu-id="39cb2-126">Catalog</span></span>
- <span data-ttu-id="39cb2-127">Database</span><span class="sxs-lookup"><span data-stu-id="39cb2-127">Database</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveCatalogItemAclEntryForUser, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39cb2-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="39cb2-128">-ObjectId</span></span>
<span data-ttu-id="39cb2-129">Identità dell'utente da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="39cb2-129">The identity of the user to remove.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: Id, UserId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39cb2-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39cb2-130">-PassThru</span></span>
<span data-ttu-id="39cb2-131">Indica che deve essere restituita una risposta booleana che indica il risultato dell'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="39cb2-131">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="39cb2-132">-Path</span><span class="sxs-lookup"><span data-stu-id="39cb2-132">-Path</span></span>
<span data-ttu-id="39cb2-133">Specifica il percorso Data Lake Analytics di un catalogo o di un elemento del catalogo.</span><span class="sxs-lookup"><span data-stu-id="39cb2-133">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="39cb2-134">Le parti del percorso devono essere separate da un punto (.).</span><span class="sxs-lookup"><span data-stu-id="39cb2-134">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: RemoveCatalogItemAclEntryForUser, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39cb2-135">-Utente</span><span class="sxs-lookup"><span data-stu-id="39cb2-135">-User</span></span>
<span data-ttu-id="39cb2-136">Rimuovere la voce ACL del catalogo per l'utente.</span><span class="sxs-lookup"><span data-stu-id="39cb2-136">Remove ACL entry of catalog for user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveCatalogAclEntryForUser, RemoveCatalogItemAclEntryForUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39cb2-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="39cb2-137">-Confirm</span></span>
<span data-ttu-id="39cb2-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39cb2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39cb2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39cb2-139">-WhatIf</span></span>
<span data-ttu-id="39cb2-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39cb2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39cb2-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="39cb2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39cb2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39cb2-142">CommonParameters</span></span>
<span data-ttu-id="39cb2-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39cb2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39cb2-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39cb2-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39cb2-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="39cb2-145">INPUTS</span></span>

### <span data-ttu-id="39cb2-146">System.String</span><span class="sxs-lookup"><span data-stu-id="39cb2-146">System.String</span></span>

### <span data-ttu-id="39cb2-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="39cb2-147">System.Guid</span></span>

### <span data-ttu-id="39cb2-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="39cb2-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="39cb2-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="39cb2-149">OUTPUTS</span></span>

### <span data-ttu-id="39cb2-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="39cb2-150">System.Boolean</span></span>

## <span data-ttu-id="39cb2-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="39cb2-151">NOTES</span></span>

## <span data-ttu-id="39cb2-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="39cb2-152">RELATED LINKS</span></span>

[<span data-ttu-id="39cb2-153">U-SQL offre ora il controllo dell'accesso a livello di database</span><span class="sxs-lookup"><span data-stu-id="39cb2-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="39cb2-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="39cb2-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="39cb2-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="39cb2-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)
