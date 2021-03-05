---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 63e0f3622ea7ae83f805688e4634b30c38cb601d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964766"
---
# <span data-ttu-id="e3538-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e3538-101">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="e3538-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3538-102">SYNOPSIS</span></span>
<span data-ttu-id="e3538-103">Ottiene una voce nell'elenco di controllo di accesso di un catalogo o di un elemento del catalogo in Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e3538-103">Gets an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="e3538-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e3538-104">SYNTAX</span></span>

### <span data-ttu-id="e3538-105">GetCatalogAclEntry (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e3538-105">GetCatalogAclEntry (Default)</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e3538-106">GetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="e3538-106">GetCatalogAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3538-107">GetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="e3538-107">GetCatalogAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3538-108">GetCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e3538-108">GetCatalogItemAclEntry</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> -ItemType <String> -Path <CatalogPathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3538-109">GetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="e3538-109">GetCatalogItemAclEntryForUserOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e3538-110">GetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="e3538-110">GetCatalogItemAclEntryForGroupOwner</span></span>
```
Get-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e3538-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e3538-111">DESCRIPTION</span></span>
<span data-ttu-id="e3538-112">Il cmdlet **Get-AzDataLakeAnalyticsCatalogItemAclEntry** ottiene un elenco di voci (ACL) nell'elenco di controllo di accesso (ACL) di un catalogo o di un elemento del catalogo in Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e3538-112">The **Get-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet gets a list of entries (ACEs) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="e3538-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e3538-113">EXAMPLES</span></span>

### <span data-ttu-id="e3538-114">Esempio 1: Ottenere l'ACL per un catalogo</span><span class="sxs-lookup"><span data-stu-id="e3538-114">Example 1: Get the ACL for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="e3538-115">Questo comando ottiene l'ACL per il catalogo dell'account Data Lake Analytics specificato</span><span class="sxs-lookup"><span data-stu-id="e3538-115">This command gets the ACL for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="e3538-116">Esempio 2: Ottenere la voce ACL del proprietario dell'utente per un catalogo</span><span class="sxs-lookup"><span data-stu-id="e3538-116">Example 2: Get the ACL entry of user owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="e3538-117">Questo comando recupera l'immissione ACL del proprietario dell'utente per il catalogo dell'account Data Lake Analytics specificato</span><span class="sxs-lookup"><span data-stu-id="e3538-117">This command gets ACL entry of the user owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="e3538-118">Esempio 3: Ottenere la voce ACL del proprietario del gruppo per un catalogo</span><span class="sxs-lookup"><span data-stu-id="e3538-118">Example 3: Get the ACL entry of group owner for a catalog</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="e3538-119">Questo comando recupera l'immissione ACL del proprietario del gruppo per il catalogo dell'account Data Lake Analytics specificato</span><span class="sxs-lookup"><span data-stu-id="e3538-119">This command gets ACL entry of the group owner for the catalog of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="e3538-120">Esempio 4: Ottenere l'ACL per un database</span><span class="sxs-lookup"><span data-stu-id="e3538-120">Example 4: Get the ACL for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -ItemType Database -Path "databaseName"

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
```

<span data-ttu-id="e3538-121">Questo comando ottiene l'ACL per il database dell'account Data Lake Analytics specificato</span><span class="sxs-lookup"><span data-stu-id="e3538-121">This command gets the ACL for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="e3538-122">Esempio 5: Ottenere la voce ACL del proprietario dell'utente per un database</span><span class="sxs-lookup"><span data-stu-id="e3538-122">Example 5: Get the ACL entry of user owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName"

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="e3538-123">Questo comando recupera la voce ACL del proprietario utente per il database dell'account Data Lake Analytics specificato</span><span class="sxs-lookup"><span data-stu-id="e3538-123">This command gets the ACL entry of the user owner for the database of the specified Data Lake Analytics account</span></span>

### <span data-ttu-id="e3538-124">Esempio 6: Ottenere la voce ACL del proprietario del gruppo per un database</span><span class="sxs-lookup"><span data-stu-id="e3538-124">Example 6: Get the ACL entry of group owner for a database</span></span>
```powershell
PS C:\> Get-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -GroupOwner -ItemType Database -Path "databaseName"

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc   ReadWrite
```

<span data-ttu-id="e3538-125">Questo comando recupera la voce ACL del proprietario del gruppo per il database dell'account Data Lake Analytics specificato</span><span class="sxs-lookup"><span data-stu-id="e3538-125">This command gets the ACL entry of the group owner for the database of the specified Data Lake Analytics account</span></span>

## <span data-ttu-id="e3538-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3538-126">PARAMETERS</span></span>

### <span data-ttu-id="e3538-127">-Account</span><span class="sxs-lookup"><span data-stu-id="e3538-127">-Account</span></span>
<span data-ttu-id="e3538-128">Specifica il nome dell'account Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="e3538-128">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="e3538-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3538-129">-DefaultProfile</span></span>
<span data-ttu-id="e3538-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e3538-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3538-131">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="e3538-131">-GroupOwner</span></span>
<span data-ttu-id="e3538-132">Ottenere la voce ACL del catalogo per il proprietario del gruppo</span><span class="sxs-lookup"><span data-stu-id="e3538-132">Get ACL entry of catalog for group owner</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForGroupOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3538-133">-ItemType</span><span class="sxs-lookup"><span data-stu-id="e3538-133">-ItemType</span></span>
<span data-ttu-id="e3538-134">Specifica il tipo di catalogo o di elementi del catalogo.</span><span class="sxs-lookup"><span data-stu-id="e3538-134">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="e3538-135">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="e3538-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e3538-136">Catalogo</span><span class="sxs-lookup"><span data-stu-id="e3538-136">Catalog</span></span>
- <span data-ttu-id="e3538-137">Database</span><span class="sxs-lookup"><span data-stu-id="e3538-137">Database</span></span>

```yaml
Type: System.String
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3538-138">-Path</span><span class="sxs-lookup"><span data-stu-id="e3538-138">-Path</span></span>
<span data-ttu-id="e3538-139">Specifica il percorso Data Lake Analytics di un catalogo o di un elemento del catalogo.</span><span class="sxs-lookup"><span data-stu-id="e3538-139">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="e3538-140">Le parti del percorso devono essere separate da un punto (.).</span><span class="sxs-lookup"><span data-stu-id="e3538-140">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: GetCatalogItemAclEntry, GetCatalogItemAclEntryForUserOwner, GetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3538-141">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="e3538-141">-UserOwner</span></span>
<span data-ttu-id="e3538-142">Ottenere la voce ACL del catalogo per il proprietario dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e3538-142">Get ACL entry of catalog for user owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetCatalogAclEntryForUserOwner, GetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e3538-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3538-143">CommonParameters</span></span>
<span data-ttu-id="e3538-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3538-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3538-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3538-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3538-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="e3538-146">INPUTS</span></span>

### <span data-ttu-id="e3538-147">System.String</span><span class="sxs-lookup"><span data-stu-id="e3538-147">System.String</span></span>

### <span data-ttu-id="e3538-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="e3538-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="e3538-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e3538-149">OUTPUTS</span></span>

### <span data-ttu-id="e3538-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="e3538-150">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="e3538-151">NOTE</span><span class="sxs-lookup"><span data-stu-id="e3538-151">NOTES</span></span>

## <span data-ttu-id="e3538-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e3538-152">RELATED LINKS</span></span>

[<span data-ttu-id="e3538-153">U-SQL offre ora il controllo dell'accesso a livello di database</span><span class="sxs-lookup"><span data-stu-id="e3538-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="e3538-154">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e3538-154">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="e3538-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="e3538-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)
