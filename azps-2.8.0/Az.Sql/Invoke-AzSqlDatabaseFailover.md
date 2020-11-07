---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/invoke-azsqldatabasefailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Invoke-AzSqlDatabaseFailover.md
ms.openlocfilehash: 5832b263f87ee0122dbc49c6dc765e7e54287311
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857418"
---
# <span data-ttu-id="0d83d-101">Invoke-AzSqlDatabaseFailover</span><span class="sxs-lookup"><span data-stu-id="0d83d-101">Invoke-AzSqlDatabaseFailover</span></span>

## <span data-ttu-id="0d83d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d83d-102">SYNOPSIS</span></span>
<span data-ttu-id="0d83d-103">Failover di un database.</span><span class="sxs-lookup"><span data-stu-id="0d83d-103">Failovers a database.</span></span>

## <span data-ttu-id="0d83d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d83d-104">SYNTAX</span></span>

```
Invoke-AzSqlDatabaseFailover [-DatabaseName] <String> [-AsJob] [-PassThru] [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d83d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d83d-105">DESCRIPTION</span></span>
<span data-ttu-id="0d83d-106">Il cmdlet Invoke-AzSqlDatabaseFailover failover di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="0d83d-106">The Invoke-AzSqlDatabaseFailover cmdlet failovers an Azure SQL database.</span></span> <span data-ttu-id="0d83d-107">Se il database si trova in un pool elastico, questo comando eseguirà il failover del database specifico senza influire sugli altri database nello stesso pool Elastic.</span><span class="sxs-lookup"><span data-stu-id="0d83d-107">If the database is in an elastic pool, this command will failover the given database without affecting the other databases in the same elastic pool.</span></span>

## <span data-ttu-id="0d83d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d83d-108">EXAMPLES</span></span>

### <span data-ttu-id="0d83d-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0d83d-109">Example 1</span></span>
```powershell
PS C:\> Invoke-AzSqlDatabaseFailover -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="0d83d-110">Questo comando eseguirà il failover del database denominato "Database01" nel server denominato "Server01"</span><span class="sxs-lookup"><span data-stu-id="0d83d-110">This command will failover the database named "Database01" on the server named "Server01"</span></span>

## <span data-ttu-id="0d83d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d83d-111">PARAMETERS</span></span>

### <span data-ttu-id="0d83d-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d83d-112">-AsJob</span></span>
<span data-ttu-id="0d83d-113">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0d83d-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d83d-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0d83d-114">-DatabaseName</span></span>
<span data-ttu-id="0d83d-115">Nome del database SQL di Azure in failover.</span><span class="sxs-lookup"><span data-stu-id="0d83d-115">The name of the Azure SQL Database to failover.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d83d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d83d-116">-DefaultProfile</span></span>
<span data-ttu-id="0d83d-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0d83d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d83d-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0d83d-118">-Force</span></span>
<span data-ttu-id="0d83d-119">Ignorare il messaggio di conferma per l'esecuzione dell'azione</span><span class="sxs-lookup"><span data-stu-id="0d83d-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0d83d-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d83d-120">-PassThru</span></span>
<span data-ttu-id="0d83d-121">Per l'esecuzione corretta, restituisce vero.</span><span class="sxs-lookup"><span data-stu-id="0d83d-121">On Successful execution, returns true.</span></span>  <span data-ttu-id="0d83d-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="0d83d-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0d83d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d83d-123">-ResourceGroupName</span></span>
<span data-ttu-id="0d83d-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0d83d-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="0d83d-125">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="0d83d-125">-ServerName</span></span>
<span data-ttu-id="0d83d-126">Nome del server di database SQL di Azure in cui si trova il database.</span><span class="sxs-lookup"><span data-stu-id="0d83d-126">The name of the Azure SQL Database Server the database is in.</span></span>

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

### <span data-ttu-id="0d83d-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0d83d-127">-Confirm</span></span>
<span data-ttu-id="0d83d-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d83d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d83d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d83d-129">-WhatIf</span></span>
<span data-ttu-id="0d83d-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d83d-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0d83d-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d83d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d83d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d83d-132">CommonParameters</span></span>
<span data-ttu-id="0d83d-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d83d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d83d-134">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0d83d-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d83d-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d83d-135">INPUTS</span></span>

### <span data-ttu-id="0d83d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="0d83d-136">System.String</span></span>

## <span data-ttu-id="0d83d-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d83d-137">OUTPUTS</span></span>

## <span data-ttu-id="0d83d-138">Note</span><span class="sxs-lookup"><span data-stu-id="0d83d-138">NOTES</span></span>

## <span data-ttu-id="0d83d-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d83d-139">RELATED LINKS</span></span>

[<span data-ttu-id="0d83d-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0d83d-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="0d83d-141">Invoke-AzSqlElasticPoolFailover</span><span class="sxs-lookup"><span data-stu-id="0d83d-141">Invoke-AzSqlElasticPoolFailover</span></span>](./Invoke-AzSqlElasticPoolFailover.md)

[<span data-ttu-id="0d83d-142">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0d83d-142">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="0d83d-143">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0d83d-143">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="0d83d-144">Curriculum vitae-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0d83d-144">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="0d83d-145">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0d83d-145">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="0d83d-146">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="0d83d-146">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="0d83d-147">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="0d83d-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
