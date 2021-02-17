---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a2c7192fc1ce2055b05a4f943a0c04560f1e714e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197727"
---
# <span data-ttu-id="5e9d9-101">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5e9d9-101">Get-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="5e9d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e9d9-102">SYNOPSIS</span></span>
<span data-ttu-id="5e9d9-103">Ottiene o elenca i gruppi di failover SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

## <span data-ttu-id="5e9d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e9d9-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e9d9-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5e9d9-105">DESCRIPTION</span></span>
<span data-ttu-id="5e9d9-106">Ottiene un gruppo di failover del database SQL Azure o elenca i gruppi di failover in un server.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="5e9d9-107">Per eseguire il comando, è possibile usare uno dei server del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="5e9d9-108">I valori restituiti rifletteranno lo stato del server specificato rispetto al gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="5e9d9-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e9d9-109">EXAMPLES</span></span>

### <span data-ttu-id="5e9d9-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5e9d9-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="5e9d9-111">Elenca tutti i gruppi di failover in un server.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="5e9d9-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5e9d9-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="5e9d9-113">Ottenere un gruppo di failover specifico.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-113">Get a specific Failover Group.</span></span>

### <span data-ttu-id="5e9d9-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="5e9d9-114">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

<span data-ttu-id="5e9d9-115">Ottenere tutti i gruppi di failover in un server che inizia con "fg".</span><span class="sxs-lookup"><span data-stu-id="5e9d9-115">Get all failover groups in a server that start with "fg".</span></span>

## <span data-ttu-id="5e9d9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e9d9-116">PARAMETERS</span></span>

### <span data-ttu-id="5e9d9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e9d9-117">-DefaultProfile</span></span>
<span data-ttu-id="5e9d9-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="5e9d9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e9d9-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="5e9d9-119">-FailoverGroupName</span></span>
<span data-ttu-id="5e9d9-120">Nome del gruppo di failover del SQL database di Azure da recuperare.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-120">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e9d9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e9d9-121">-ResourceGroupName</span></span>
<span data-ttu-id="5e9d9-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="5e9d9-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5e9d9-123">-ServerName</span></span>
<span data-ttu-id="5e9d9-124">Nome del server di SQL Azure da cui recuperare il gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-124">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="5e9d9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e9d9-125">CommonParameters</span></span>
<span data-ttu-id="5e9d9-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e9d9-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5e9d9-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e9d9-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="5e9d9-128">INPUTS</span></span>

### <span data-ttu-id="5e9d9-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5e9d9-129">System.String</span></span>

## <span data-ttu-id="5e9d9-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e9d9-130">OUTPUTS</span></span>

### <span data-ttu-id="5e9d9-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="5e9d9-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="5e9d9-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="5e9d9-132">NOTES</span></span>

## <span data-ttu-id="5e9d9-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e9d9-133">RELATED LINKS</span></span>

[<span data-ttu-id="5e9d9-134">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5e9d9-134">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5e9d9-135">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5e9d9-135">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5e9d9-136">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5e9d9-136">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="5e9d9-137">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5e9d9-137">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="5e9d9-138">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5e9d9-138">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5e9d9-139">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5e9d9-139">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5e9d9-140">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="5e9d9-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
