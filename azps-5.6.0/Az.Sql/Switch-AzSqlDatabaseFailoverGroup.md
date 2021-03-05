---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a8ad9a3925ccf1c0f56ce9be6a962d667f122307
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992304"
---
# <span data-ttu-id="5376d-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5376d-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="5376d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5376d-102">SYNOPSIS</span></span>
<span data-ttu-id="5376d-103">Esegue il failover di un gruppo di failover del SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="5376d-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="5376d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5376d-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5376d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5376d-105">DESCRIPTION</span></span>
<span data-ttu-id="5376d-106">Questo comando scambia i ruoli dei server in un gruppo di failover e imposta tutti i database secondari sul ruolo principale.</span><span class="sxs-lookup"><span data-stu-id="5376d-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="5376d-107">Tutte le nuove sessioni TDS vengono automaticamente ri instradate al server secondario dopo l'aggiornamento della cache del client DNS.</span><span class="sxs-lookup"><span data-stu-id="5376d-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="5376d-108">Quando il server principale originale sarà di nuovo online, tutti i database primari in precedenza in esso contenuti verranno tornati al ruolo secondario.</span><span class="sxs-lookup"><span data-stu-id="5376d-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="5376d-109">Per eseguire questo comando, è necessario usare il server secondario del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="5376d-109">The Failover Group's secondary server must be used to execute this command.</span></span>
<span data-ttu-id="5376d-110">Se il parametro AllowDataLoss non è specificato, questo comando attende finché non si passa a entrambi i ruoli.</span><span class="sxs-lookup"><span data-stu-id="5376d-110">If the AllowDataLoss parameter is not specified, this command waits until both roles are switched.</span></span> <span data-ttu-id="5376d-111">Se si specifica il parametro AllowDataLoss, il comando attende solo finché il nuovo nome principale non assume il proprio ruolo.</span><span class="sxs-lookup"><span data-stu-id="5376d-111">If the AllowDataLoss parameter is specified, the command only waits until the new primary assumes its role.</span></span>

## <span data-ttu-id="5376d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5376d-112">EXAMPLES</span></span>

### <span data-ttu-id="5376d-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5376d-113">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="5376d-114">Eseguire un'operazione di failover che consente la perdita di dati tramite piping nel gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="5376d-114">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="5376d-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5376d-115">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="5376d-116">Eseguire un'operazione di failover che ha esito positivo senza perdere dati oppure eseguire il rollback.</span><span class="sxs-lookup"><span data-stu-id="5376d-116">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="5376d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5376d-117">PARAMETERS</span></span>

### <span data-ttu-id="5376d-118">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="5376d-118">-AllowDataLoss</span></span>
<span data-ttu-id="5376d-119">Completare il failover anche in questo caso può causare la perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="5376d-119">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="5376d-120">In questo modo il failover può proseguire anche se un database primario non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="5376d-120">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5376d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5376d-121">-AsJob</span></span>
<span data-ttu-id="5376d-122">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5376d-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5376d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5376d-123">-DefaultProfile</span></span>
<span data-ttu-id="5376d-124">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5376d-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5376d-125">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="5376d-125">-FailoverGroupName</span></span>
<span data-ttu-id="5376d-126">Nome del gruppo di failover del database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5376d-126">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="5376d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5376d-127">-ResourceGroupName</span></span>
<span data-ttu-id="5376d-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5376d-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="5376d-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5376d-129">-ServerName</span></span>
<span data-ttu-id="5376d-130">Nome del server di database SQL Azure secondario del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="5376d-130">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="5376d-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5376d-131">-Confirm</span></span>
<span data-ttu-id="5376d-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5376d-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5376d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5376d-133">-WhatIf</span></span>
<span data-ttu-id="5376d-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5376d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5376d-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5376d-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5376d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5376d-136">CommonParameters</span></span>
<span data-ttu-id="5376d-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5376d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5376d-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5376d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5376d-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="5376d-139">INPUTS</span></span>

### <span data-ttu-id="5376d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5376d-140">System.String</span></span>

## <span data-ttu-id="5376d-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5376d-141">OUTPUTS</span></span>

### <span data-ttu-id="5376d-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="5376d-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="5376d-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="5376d-143">NOTES</span></span>

## <span data-ttu-id="5376d-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5376d-144">RELATED LINKS</span></span>

[<span data-ttu-id="5376d-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5376d-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5376d-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5376d-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5376d-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5376d-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5376d-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5376d-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="5376d-149">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5376d-149">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="5376d-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="5376d-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="5376d-151">documentazione SQL database</span><span class="sxs-lookup"><span data-stu-id="5376d-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
