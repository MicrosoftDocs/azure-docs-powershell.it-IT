---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 430c4cc1318d53ebb2671b9fb1dd0cea8655898d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676994"
---
# <span data-ttu-id="53ff7-101">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="53ff7-101">Get-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="53ff7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="53ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="53ff7-103">Ottiene o elenca i gruppi di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="53ff7-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

## <span data-ttu-id="53ff7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="53ff7-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53ff7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53ff7-105">DESCRIPTION</span></span>
<span data-ttu-id="53ff7-106">Ottiene un gruppo di failover di database SQL di Azure specifico o elenca i gruppi di failover in un server.</span><span class="sxs-lookup"><span data-stu-id="53ff7-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="53ff7-107">Per eseguire il comando, è possibile che venga usato un server nel gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="53ff7-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="53ff7-108">I valori restituiti riflettono lo stato del server specificato rispetto al gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="53ff7-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="53ff7-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="53ff7-109">EXAMPLES</span></span>

### <span data-ttu-id="53ff7-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="53ff7-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="53ff7-111">Elenca tutti i gruppi di failover in un server.</span><span class="sxs-lookup"><span data-stu-id="53ff7-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="53ff7-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="53ff7-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="53ff7-113">Ottenere un gruppo di failover specifico.</span><span class="sxs-lookup"><span data-stu-id="53ff7-113">Get a specific Failover Group.</span></span>

### <span data-ttu-id="53ff7-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="53ff7-114">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

<span data-ttu-id="53ff7-115">Ottenere tutti i gruppi di failover in un server che iniziano con "FG".</span><span class="sxs-lookup"><span data-stu-id="53ff7-115">Get all failover groups in a server that start with "fg".</span></span>

## <span data-ttu-id="53ff7-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="53ff7-116">PARAMETERS</span></span>

### <span data-ttu-id="53ff7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53ff7-117">-DefaultProfile</span></span>
<span data-ttu-id="53ff7-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="53ff7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53ff7-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="53ff7-119">-FailoverGroupName</span></span>
<span data-ttu-id="53ff7-120">Il nome del gruppo di failover di database SQL di Azure da recuperare.</span><span class="sxs-lookup"><span data-stu-id="53ff7-120">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="53ff7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53ff7-121">-ResourceGroupName</span></span>
<span data-ttu-id="53ff7-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="53ff7-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="53ff7-123">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="53ff7-123">-ServerName</span></span>
<span data-ttu-id="53ff7-124">Nome del server di database SQL di Azure da cui recuperare il gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="53ff7-124">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="53ff7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53ff7-125">CommonParameters</span></span>
<span data-ttu-id="53ff7-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53ff7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53ff7-127">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53ff7-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53ff7-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="53ff7-128">INPUTS</span></span>

### <span data-ttu-id="53ff7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="53ff7-129">System.String</span></span>

## <span data-ttu-id="53ff7-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="53ff7-130">OUTPUTS</span></span>

### <span data-ttu-id="53ff7-131">Microsoft. Azure. Commands. SQL. FailoverGroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="53ff7-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="53ff7-132">Note</span><span class="sxs-lookup"><span data-stu-id="53ff7-132">NOTES</span></span>

## <span data-ttu-id="53ff7-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="53ff7-133">RELATED LINKS</span></span>

[<span data-ttu-id="53ff7-134">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="53ff7-134">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="53ff7-135">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="53ff7-135">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="53ff7-136">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="53ff7-136">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="53ff7-137">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="53ff7-137">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="53ff7-138">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="53ff7-138">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="53ff7-139">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="53ff7-139">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="53ff7-140">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="53ff7-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
