---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a2c7192fc1ce2055b05a4f943a0c04560f1e714e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203065"
---
# <span data-ttu-id="7149e-101">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7149e-101">Get-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="7149e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7149e-102">SYNOPSIS</span></span>
<span data-ttu-id="7149e-103">Ottiene o elenca i gruppi di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="7149e-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

## <span data-ttu-id="7149e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7149e-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7149e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7149e-105">DESCRIPTION</span></span>
<span data-ttu-id="7149e-106">Ottiene un gruppo di failover di database SQL di Azure specifico o elenca i gruppi di failover in un server.</span><span class="sxs-lookup"><span data-stu-id="7149e-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="7149e-107">Per eseguire il comando, è possibile che venga usato un server nel gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="7149e-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="7149e-108">I valori restituiti riflettono lo stato del server specificato rispetto al gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="7149e-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="7149e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7149e-109">EXAMPLES</span></span>

### <span data-ttu-id="7149e-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7149e-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="7149e-111">Elenca tutti i gruppi di failover in un server.</span><span class="sxs-lookup"><span data-stu-id="7149e-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="7149e-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7149e-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="7149e-113">Ottenere un gruppo di failover specifico.</span><span class="sxs-lookup"><span data-stu-id="7149e-113">Get a specific Failover Group.</span></span>

### <span data-ttu-id="7149e-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="7149e-114">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

<span data-ttu-id="7149e-115">Ottenere tutti i gruppi di failover in un server che iniziano con "FG".</span><span class="sxs-lookup"><span data-stu-id="7149e-115">Get all failover groups in a server that start with "fg".</span></span>

## <span data-ttu-id="7149e-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7149e-116">PARAMETERS</span></span>

### <span data-ttu-id="7149e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7149e-117">-DefaultProfile</span></span>
<span data-ttu-id="7149e-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7149e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7149e-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="7149e-119">-FailoverGroupName</span></span>
<span data-ttu-id="7149e-120">Il nome del gruppo di failover di database SQL di Azure da recuperare.</span><span class="sxs-lookup"><span data-stu-id="7149e-120">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

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

### <span data-ttu-id="7149e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7149e-121">-ResourceGroupName</span></span>
<span data-ttu-id="7149e-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7149e-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="7149e-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="7149e-123">-ServerName</span></span>
<span data-ttu-id="7149e-124">Nome del server di database SQL di Azure da cui recuperare il gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="7149e-124">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="7149e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7149e-125">CommonParameters</span></span>
<span data-ttu-id="7149e-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7149e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7149e-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7149e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7149e-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7149e-128">INPUTS</span></span>

### <span data-ttu-id="7149e-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7149e-129">System.String</span></span>

## <span data-ttu-id="7149e-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7149e-130">OUTPUTS</span></span>

### <span data-ttu-id="7149e-131">Microsoft. Azure. Commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="7149e-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="7149e-132">Note</span><span class="sxs-lookup"><span data-stu-id="7149e-132">NOTES</span></span>

## <span data-ttu-id="7149e-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7149e-133">RELATED LINKS</span></span>

[<span data-ttu-id="7149e-134">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7149e-134">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="7149e-135">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7149e-135">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="7149e-136">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7149e-136">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="7149e-137">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7149e-137">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="7149e-138">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7149e-138">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="7149e-139">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7149e-139">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="7149e-140">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="7149e-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
