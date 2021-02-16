---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
ms.openlocfilehash: 7dc07f1064837b710c246e4aafb4ceb008019e4e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201470"
---
# <span data-ttu-id="e90d5-101">Get-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="e90d5-101">Get-AzSqlSyncSchema</span></span>

## <span data-ttu-id="e90d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e90d5-102">SYNOPSIS</span></span>
<span data-ttu-id="e90d5-103">Restituisce informazioni sullo schema di sincronizzazione di un database membro o di un database hub.</span><span class="sxs-lookup"><span data-stu-id="e90d5-103">Returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="e90d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e90d5-104">SYNTAX</span></span>

```
Get-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e90d5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e90d5-105">DESCRIPTION</span></span>
<span data-ttu-id="e90d5-106">Il cmdlet **Get-AzSqlSyncSchema** restituisce informazioni sullo schema di sincronizzazione di un database membro o di un database hub.</span><span class="sxs-lookup"><span data-stu-id="e90d5-106">The **Get-AzSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="e90d5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e90d5-107">EXAMPLES</span></span>

### <span data-ttu-id="e90d5-108">Esempio 1: Ottenere lo schema di sincronizzazione per un database hub</span><span class="sxs-lookup"><span data-stu-id="e90d5-108">Example 1: Get the sync schema for a hub database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="e90d5-109">Questo comando recupera lo schema di sincronizzazione per il database hub nel gruppo di sincronizzazione syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="e90d5-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="e90d5-110">Esempio 2: Ottenere lo schema di sincronizzazione per un database hub ed espandere Tabelle</span><span class="sxs-lookup"><span data-stu-id="e90d5-110">Example 2: Get the sync schema for a hub database, and expand Tables</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"  | select -ExpandProperty Tables
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

<span data-ttu-id="e90d5-111">Questo comando recupera lo schema di sincronizzazione per il database hub nel gruppo di sincronizzazione syncGroup01 ed espande la proprietà Tables.</span><span class="sxs-lookup"><span data-stu-id="e90d5-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="e90d5-112">Esempio 3: Ottenere lo schema di sincronizzazione per un database membro</span><span class="sxs-lookup"><span data-stu-id="e90d5-112">Example 3: Get the sync schema for a member database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="e90d5-113">Questo comando ottiene lo schema di sincronizzazione per il database dei membri nel membro di sincronizzazione syncMember01.</span><span class="sxs-lookup"><span data-stu-id="e90d5-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="e90d5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e90d5-114">PARAMETERS</span></span>

### <span data-ttu-id="e90d5-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e90d5-115">-DatabaseName</span></span>
<span data-ttu-id="e90d5-116">Nome del database di SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e90d5-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="e90d5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e90d5-117">-DefaultProfile</span></span>
<span data-ttu-id="e90d5-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="e90d5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e90d5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e90d5-119">-ResourceGroupName</span></span>
<span data-ttu-id="e90d5-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e90d5-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="e90d5-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e90d5-121">-ServerName</span></span>
<span data-ttu-id="e90d5-122">Il nome dell'account Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e90d5-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="e90d5-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="e90d5-123">-SyncGroupName</span></span>
<span data-ttu-id="e90d5-124">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e90d5-124">The sync group name.</span></span>

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

### <span data-ttu-id="e90d5-125">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="e90d5-125">-SyncMemberName</span></span>
<span data-ttu-id="e90d5-126">Nome del membro di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="e90d5-126">The sync member name.</span></span>

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

### <span data-ttu-id="e90d5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e90d5-127">CommonParameters</span></span>
<span data-ttu-id="e90d5-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e90d5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e90d5-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e90d5-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e90d5-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="e90d5-130">INPUTS</span></span>

### <span data-ttu-id="e90d5-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e90d5-131">System.String</span></span>

## <span data-ttu-id="e90d5-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e90d5-132">OUTPUTS</span></span>

### <span data-ttu-id="e90d5-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span><span class="sxs-lookup"><span data-stu-id="e90d5-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

## <span data-ttu-id="e90d5-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="e90d5-134">NOTES</span></span>

## <span data-ttu-id="e90d5-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e90d5-135">RELATED LINKS</span></span>
