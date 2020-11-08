---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncSchema.md
ms.openlocfilehash: 7dc07f1064837b710c246e4aafb4ceb008019e4e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191189"
---
# <span data-ttu-id="9306f-101">Get-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="9306f-101">Get-AzSqlSyncSchema</span></span>

## <span data-ttu-id="9306f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9306f-102">SYNOPSIS</span></span>
<span data-ttu-id="9306f-103">Restituisce informazioni sullo schema di sincronizzazione di un database di membri o di un database hub.</span><span class="sxs-lookup"><span data-stu-id="9306f-103">Returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="9306f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9306f-104">SYNTAX</span></span>

```
Get-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9306f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9306f-105">DESCRIPTION</span></span>
<span data-ttu-id="9306f-106">Il cmdlet **Get-AzSqlSyncSchema** restituisce informazioni sullo schema di sincronizzazione di un database di membri o di un database hub.</span><span class="sxs-lookup"><span data-stu-id="9306f-106">The **Get-AzSqlSyncSchema** cmdlet returns information about the sync schema of a member database or a hub database.</span></span>

## <span data-ttu-id="9306f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9306f-107">EXAMPLES</span></span>

### <span data-ttu-id="9306f-108">Esempio 1: ottenere lo schema di sincronizzazione per un database hub</span><span class="sxs-lookup"><span data-stu-id="9306f-108">Example 1: Get the sync schema for a hub database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
Tables                     LastUpdateTime
------                     --------------
{dbo.Table_1, dbo.Table_2} 6/13/2017 10:03:44 AM
```

<span data-ttu-id="9306f-109">Questo comando ottiene lo schema di sincronizzazione per il database hub nel gruppo di sincronizzazione syncGroup01.</span><span class="sxs-lookup"><span data-stu-id="9306f-109">This command gets the sync schema for the hub database in the sync group syncGroup01.</span></span>

### <span data-ttu-id="9306f-110">Esempio 2: ottenere lo schema di sincronizzazione per un database hub ed espandere tabelle</span><span class="sxs-lookup"><span data-stu-id="9306f-110">Example 2: Get the sync schema for a hub database, and expand Tables</span></span>
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

<span data-ttu-id="9306f-111">Questo comando consente di ottenere lo schema di sincronizzazione per il database hub nella proprietà gruppo di sincronizzazione syncGroup01 ed Espandi tabelle.</span><span class="sxs-lookup"><span data-stu-id="9306f-111">This command gets the sync schema for the hub database in the sync group syncGroup01 and expand Tables property.</span></span>

### <span data-ttu-id="9306f-112">Esempio 3: ottenere lo schema di sincronizzazione per un database di membri</span><span class="sxs-lookup"><span data-stu-id="9306f-112">Example 3: Get the sync schema for a member database</span></span>
```powershell
PS C:\>Get-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
The schema payload is the same as Example 1.
```

<span data-ttu-id="9306f-113">Questo comando ottiene lo schema di sincronizzazione per il database del membro nel syncMember01 membro di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="9306f-113">This command gets the sync schema for the member database in the sync member syncMember01.</span></span>

## <span data-ttu-id="9306f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9306f-114">PARAMETERS</span></span>

### <span data-ttu-id="9306f-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9306f-115">-DatabaseName</span></span>
<span data-ttu-id="9306f-116">Nome del database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="9306f-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="9306f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9306f-117">-DefaultProfile</span></span>
<span data-ttu-id="9306f-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9306f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9306f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9306f-119">-ResourceGroupName</span></span>
<span data-ttu-id="9306f-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9306f-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="9306f-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="9306f-121">-ServerName</span></span>
<span data-ttu-id="9306f-122">Nome di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9306f-122">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="9306f-123">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="9306f-123">-SyncGroupName</span></span>
<span data-ttu-id="9306f-124">Nome del gruppo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="9306f-124">The sync group name.</span></span>

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

### <span data-ttu-id="9306f-125">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="9306f-125">-SyncMemberName</span></span>
<span data-ttu-id="9306f-126">Il nome del membro della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="9306f-126">The sync member name.</span></span>

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

### <span data-ttu-id="9306f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9306f-127">CommonParameters</span></span>
<span data-ttu-id="9306f-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9306f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9306f-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9306f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9306f-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9306f-130">INPUTS</span></span>

### <span data-ttu-id="9306f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="9306f-131">System.String</span></span>

## <span data-ttu-id="9306f-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9306f-132">OUTPUTS</span></span>

### <span data-ttu-id="9306f-133">Microsoft. Azure. Commands. SQL. datasync. Model. AzureSqlSyncFullSchemaModel</span><span class="sxs-lookup"><span data-stu-id="9306f-133">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncFullSchemaModel</span></span>

## <span data-ttu-id="9306f-134">Note</span><span class="sxs-lookup"><span data-stu-id="9306f-134">NOTES</span></span>

## <span data-ttu-id="9306f-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9306f-135">RELATED LINKS</span></span>
