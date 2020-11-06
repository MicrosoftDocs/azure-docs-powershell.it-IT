---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncSchema.md
ms.openlocfilehash: 38e56102ba544bc56384f0d3ff59bdc8091bdd54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520597"
---
# <span data-ttu-id="5e485-101">Get-AzureRmSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="5e485-101">Get-AzureRmSqlSyncSchema</span></span>

## <span data-ttu-id="5e485-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e485-102">SYNOPSIS</span></span>
<span data-ttu-id="5e485-103">Restituisce informazioni sullo schema di sincronizzazione di un database di membri o di un database hub.</span><span class="sxs-lookup"><span data-stu-id="5e485-103">Returns information about the sync schema of a member database or a hub database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e485-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e485-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5e485-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e485-105">DESCRIPTION</span></span>
<span data-ttu-id="5e485-106">Il cmdlet **Get-AzureRmSqlSyncSchema** restituisce informazioni sullo schema di sincronizzazione di un database di membri o di un database hub.</span><span class="sxs-lookup"><span data-stu-id="5e485-106">The **Get-AzureRmSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="5e485-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e485-107">EXAMPLES</span></span>

### <span data-ttu-id="5e485-108">Esempio 1,1: ottenere lo schema di sincronizzazione per un database hub</span><span class="sxs-lookup"><span data-stu-id="5e485-108">Example 1.1: Get the sync schema for a hub database</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="5e485-109">Questo comando ottiene lo schema di sincronizzazione per il database hub nel gruppo di sincronizzazione syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="5e485-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="5e485-110">Esempio 1,2: ottenere lo schema di sincronizzazione per un database hub ed espandere tabelle</span><span class="sxs-lookup"><span data-stu-id="5e485-110">Example 1.2: Get the sync schema for a hub database, and expand Tables</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"  | select -ExpandProperty Tables
Columns    : {column1, column2}
ErrorId    : Schema_TableHasNoPrimaryKey
HasError   : True
Name       : dbo.Table_1
QuotedName : [dbo].[Table_1]

Columns    : {column2, column4}
ErrorId    : Schema_TableHasNoPrimaryKey
HasError   : True
Name       : dbo.Table_2
QuotedName : [dbo].[Table_2]
```

<span data-ttu-id="5e485-111">Questo comando consente di ottenere lo schema di sincronizzazione per il database hub nella proprietà gruppo di sincronizzazione syncGroup01 ed Espandi tabelle.</span><span class="sxs-lookup"><span data-stu-id="5e485-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="5e485-112">Esempio 2: ottenere lo schema di sincronizzazione per un database di membri</span><span class="sxs-lookup"><span data-stu-id="5e485-112">Example 2: Get the sync schema for a member database</span></span>
```
PS C:\>Get-AzureRmSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="5e485-113">Questo comando ottiene lo schema di sincronizzazione per il database del membro nel syncMember01 membro di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="5e485-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="5e485-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e485-114">PARAMETERS</span></span>

### <span data-ttu-id="5e485-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5e485-115">-DatabaseName</span></span>
<span data-ttu-id="5e485-116">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="5e485-116">The name of the Azure SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e485-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e485-117">-DefaultProfile</span></span>
<span data-ttu-id="5e485-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5e485-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e485-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e485-119">-ResourceGroupName</span></span>
<span data-ttu-id="5e485-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5e485-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e485-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="5e485-121">-ServerName</span></span>
<span data-ttu-id="5e485-122">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5e485-122">The name of the Azure SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e485-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="5e485-123">-SyncGroupName</span></span>
<span data-ttu-id="5e485-124">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="5e485-124">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e485-125">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="5e485-125">-SyncMemberName</span></span>
<span data-ttu-id="5e485-126">Il nome del membro della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="5e485-126">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e485-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e485-127">CommonParameters</span></span>
<span data-ttu-id="5e485-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e485-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e485-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e485-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e485-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e485-130">INPUTS</span></span>

### <span data-ttu-id="5e485-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5e485-131">System.String</span></span>

## <span data-ttu-id="5e485-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e485-132">OUTPUTS</span></span>

### <span data-ttu-id="5e485-133">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncFullSchemaModel</span><span class="sxs-lookup"><span data-stu-id="5e485-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

## <span data-ttu-id="5e485-134">Note</span><span class="sxs-lookup"><span data-stu-id="5e485-134">NOTES</span></span>

## <span data-ttu-id="5e485-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e485-135">RELATED LINKS</span></span>
