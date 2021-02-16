---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: d713675e3e73f32a4579d801a4dc1577cebd4cf0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178358"
---
# <span data-ttu-id="d98ae-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d98ae-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="d98ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d98ae-102">SYNOPSIS</span></span>
<span data-ttu-id="d98ae-103">Imposta un database secondario come primario per avviare il failover.</span><span class="sxs-lookup"><span data-stu-id="d98ae-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="d98ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d98ae-104">SYNTAX</span></span>

### <span data-ttu-id="d98ae-105">NoOptionsSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d98ae-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d98ae-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="d98ae-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d98ae-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d98ae-107">DESCRIPTION</span></span>
<span data-ttu-id="d98ae-108">Il cmdlet **Set-AzSqlDatabaseSecondary** imposta un database secondario come principale per avviare il failover.</span><span class="sxs-lookup"><span data-stu-id="d98ae-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="d98ae-109">Questo cmdlet è progettato come comando di configurazione generale, ma attualmente è limitato all'avvio del failover.</span><span class="sxs-lookup"><span data-stu-id="d98ae-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="d98ae-110">Specificare il *parametro AllowDataLoss* per avviare un failover di forzatura durante un'interruzione.</span><span class="sxs-lookup"><span data-stu-id="d98ae-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="d98ae-111">Non è necessario specificare questo parametro quando si esegue un'operazione pianificata, ad esempio il drill-down di ripristino.</span><span class="sxs-lookup"><span data-stu-id="d98ae-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="d98ae-112">Nell'ultimo caso, il database secondario viene sincronizzato con il database primario prima del passaggio.</span><span class="sxs-lookup"><span data-stu-id="d98ae-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="d98ae-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d98ae-113">EXAMPLES</span></span>

### <span data-ttu-id="d98ae-114">Esempio 1: Avviare un failover pianificato</span><span class="sxs-lookup"><span data-stu-id="d98ae-114">Example 1: Initiate a planned failover</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### <span data-ttu-id="d98ae-115">Esempio 2: Avviare un failover forzato (con potenziali perdite di dati)</span><span class="sxs-lookup"><span data-stu-id="d98ae-115">Example 2: Initiate a forced failover (with potential data loss)</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## <span data-ttu-id="d98ae-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d98ae-116">PARAMETERS</span></span>

### <span data-ttu-id="d98ae-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="d98ae-117">-AllowDataLoss</span></span>
<span data-ttu-id="d98ae-118">Indica che questa operazione di failover consente la perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="d98ae-118">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d98ae-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d98ae-119">-AsJob</span></span>
<span data-ttu-id="d98ae-120">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d98ae-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d98ae-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d98ae-121">-DatabaseName</span></span>
<span data-ttu-id="d98ae-122">Specifica il nome del database secondario SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d98ae-122">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="d98ae-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d98ae-123">-DefaultProfile</span></span>
<span data-ttu-id="d98ae-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="d98ae-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d98ae-125">-Failover</span><span class="sxs-lookup"><span data-stu-id="d98ae-125">-Failover</span></span>
<span data-ttu-id="d98ae-126">Indica che l'operazione è un failover.</span><span class="sxs-lookup"><span data-stu-id="d98ae-126">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d98ae-127">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d98ae-127">-PartnerResourceGroupName</span></span>
<span data-ttu-id="d98ae-128">Specifica il nome del gruppo di risorse a cui è assegnato il partner Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="d98ae-128">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d98ae-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d98ae-129">-ResourceGroupName</span></span>
<span data-ttu-id="d98ae-130">Specifica il nome del gruppo di risorse a cui è assegnato il database secondario SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d98ae-130">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="d98ae-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d98ae-131">-ServerName</span></span>
<span data-ttu-id="d98ae-132">Specifica il nome della cartella di SQL Server che ospita il database secondario SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="d98ae-132">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="d98ae-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d98ae-133">-Confirm</span></span>
<span data-ttu-id="d98ae-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d98ae-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d98ae-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d98ae-135">-WhatIf</span></span>
<span data-ttu-id="d98ae-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d98ae-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d98ae-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d98ae-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d98ae-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d98ae-138">CommonParameters</span></span>
<span data-ttu-id="d98ae-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d98ae-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d98ae-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d98ae-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d98ae-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="d98ae-141">INPUTS</span></span>

### <span data-ttu-id="d98ae-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d98ae-142">System.String</span></span>

## <span data-ttu-id="d98ae-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d98ae-143">OUTPUTS</span></span>

### <span data-ttu-id="d98ae-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="d98ae-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="d98ae-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="d98ae-145">NOTES</span></span>

## <span data-ttu-id="d98ae-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d98ae-146">RELATED LINKS</span></span>

[<span data-ttu-id="d98ae-147">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d98ae-147">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="d98ae-148">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d98ae-148">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="d98ae-149">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="d98ae-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
