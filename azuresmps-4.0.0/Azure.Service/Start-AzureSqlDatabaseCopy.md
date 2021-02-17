---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35e29655e8447644b6c5449309424595e45ca187
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413065"
---
# <span data-ttu-id="74eb1-101">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="74eb1-101">Start-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="74eb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="74eb1-103">Avvia un'operazione di copia di un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="74eb1-103">Starts a copy operation of an Azure SQL Database.</span></span>

## <span data-ttu-id="74eb1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74eb1-104">SYNTAX</span></span>

### <span data-ttu-id="74eb1-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="74eb1-105">ByInputObject</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74eb1-106">ByInputObjectContinuous</span><span class="sxs-lookup"><span data-stu-id="74eb1-106">ByInputObjectContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74eb1-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="74eb1-107">ByDatabaseName</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74eb1-108">ByDatabaseNameContinuous</span><span class="sxs-lookup"><span data-stu-id="74eb1-108">ByDatabaseNameContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74eb1-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="74eb1-109">DESCRIPTION</span></span>
<span data-ttu-id="74eb1-110">Il cmdlet **Start-AzureSqlDatabaseCopy** avvia un'operazione di copia unica o di copia continua di uno specifico database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="74eb1-110">The **Start-AzureSqlDatabaseCopy** cmdlet starts a one-time copy operation or a continuous copy operation of a specific Azure SQL Database.</span></span>
<span data-ttu-id="74eb1-111">Questo cmdlet non è transazionale.</span><span class="sxs-lookup"><span data-stu-id="74eb1-111">This cmdlet is not transactional.</span></span>

<span data-ttu-id="74eb1-112">Il database originale è il database di origine.</span><span class="sxs-lookup"><span data-stu-id="74eb1-112">The original database is the source database.</span></span>
<span data-ttu-id="74eb1-113">La copia è il database secondario o di destinazione.</span><span class="sxs-lookup"><span data-stu-id="74eb1-113">The copy is the secondary or target database.</span></span>
<span data-ttu-id="74eb1-114">Per una copia continua, i database di origine e di destinazione non possono trovarsi nello stesso server e i server che ospitano i database di origine e di destinazione devono far parte della stessa sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="74eb1-114">For a continuous copy, the source and target databases cannot reside on the same server, and the servers that host the source and target databases must be part of the same subscription.</span></span>

<span data-ttu-id="74eb1-115">Se non si specifica il parametro *ContinuousCopy,* questo cmdlet crea una copia unica del database di origine.</span><span class="sxs-lookup"><span data-stu-id="74eb1-115">If you do not specify the *ContinuousCopy* parameter, this cmdlet creates a one-time copy of the source database.</span></span>
<span data-ttu-id="74eb1-116">Una volta ricevuta la risposta, l'operazione può essere ancora in corso.</span><span class="sxs-lookup"><span data-stu-id="74eb1-116">When the response is received, the operation can still be in progress.</span></span>
<span data-ttu-id="74eb1-117">È possibile monitorare l'operazione usando Get-AzureSqlDatabaseCopy o Get-AzureSqlDatabaseOperation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74eb1-117">You can monitor the operation by using the Get-AzureSqlDatabaseCopy or Get-AzureSqlDatabaseOperation cmdlet.</span></span>

<span data-ttu-id="74eb1-118">Se si specifica *ContinuaCopia,* questo cmdlet crea una copia continua del database di origine.</span><span class="sxs-lookup"><span data-stu-id="74eb1-118">If you specify *ContinuousCopy*, this cmdlet creates a continuous copy of the source database.</span></span>
<span data-ttu-id="74eb1-119">Una volta ricevuta la risposta, l'operazione è in corso.</span><span class="sxs-lookup"><span data-stu-id="74eb1-119">When the response is received, the operation will be in progress.</span></span>
<span data-ttu-id="74eb1-120">È possibile monitorare l'operazione usando **Get-AzureSqlDatabaseCopy** **o Get-AzureSqlDatabaseOperation.**</span><span class="sxs-lookup"><span data-stu-id="74eb1-120">You can monitor the operation by using **Get-AzureSqlDatabaseCopy** or **Get-AzureSqlDatabaseOperation**.</span></span>

<span data-ttu-id="74eb1-121">È possibile creare una copia continua come database online o offline.</span><span class="sxs-lookup"><span data-stu-id="74eb1-121">You can create a continuous copy as an online or offline database.</span></span>
<span data-ttu-id="74eb1-122">La copia continua online viene usata per configurare Active Geo-Replication per il database SQL https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ Azure.</span><span class="sxs-lookup"><span data-stu-id="74eb1-122">The online continuous copy is used to configure Active Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/.</span></span>
<span data-ttu-id="74eb1-123">La copia continua offline viene usata per configurare il servizio Geo-Replication per il database SQL https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ Azure.</span><span class="sxs-lookup"><span data-stu-id="74eb1-123">The offline continuous copy is used to configure Standard Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/.</span></span>

## <span data-ttu-id="74eb1-124">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74eb1-124">EXAMPLES</span></span>

### <span data-ttu-id="74eb1-125">Esempio 1: Pianificare una copia continua del database</span><span class="sxs-lookup"><span data-stu-id="74eb1-125">Example 1: Schedule a continuous database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

<span data-ttu-id="74eb1-126">Questo comando pianifica una copia continua del database denominato Ordini nel server denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="74eb1-126">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="74eb1-127">Il comando crea un database di destinazione nel server denominato bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="74eb1-127">The command creates a target database on the server named bk0b8kf658.</span></span>

### <span data-ttu-id="74eb1-128">Esempio 2: Creare una copia unica nello stesso server</span><span class="sxs-lookup"><span data-stu-id="74eb1-128">Example 2: Create a one-time copy on the same server</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

<span data-ttu-id="74eb1-129">Questo comando crea una copia unica del database denominato Ordini nel server denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="74eb1-129">This command creates a one-time copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="74eb1-130">Il comando crea una copia denominata OrdersCopy nello stesso server.</span><span class="sxs-lookup"><span data-stu-id="74eb1-130">The command creates a copy named OrdersCopy on the same server.</span></span>

### <span data-ttu-id="74eb1-131">Esempio 3: Pianificare una copia continua del database offline</span><span class="sxs-lookup"><span data-stu-id="74eb1-131">Example 3: Schedule a continuous offline database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

<span data-ttu-id="74eb1-132">Questo comando pianifica una copia continua del database denominato Ordini nel server denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="74eb1-132">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="74eb1-133">Questo comando crea un database di destinazione offline nel server denominato bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="74eb1-133">This command creates an offline target database on the server named bk0b8kf658.</span></span>

## <span data-ttu-id="74eb1-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74eb1-134">PARAMETERS</span></span>

### <span data-ttu-id="74eb1-135">-ContinuousCopy</span><span class="sxs-lookup"><span data-stu-id="74eb1-135">-ContinuousCopy</span></span>
<span data-ttu-id="74eb1-136">Indica che la copia del database sarà una copia continua (un database di replica).</span><span class="sxs-lookup"><span data-stu-id="74eb1-136">Indicates that the database copy will be a continuous-copy (a replica database).</span></span>
<span data-ttu-id="74eb1-137">La copia continua non è supportata all'interno dello stesso server.</span><span class="sxs-lookup"><span data-stu-id="74eb1-137">Continuous copy is not supported within the same server.</span></span>
<span data-ttu-id="74eb1-138">Se questo parametro non è specificato, viene eseguita una copia unica.</span><span class="sxs-lookup"><span data-stu-id="74eb1-138">If this parameter is not specified, then a one-time copy is performed.</span></span>
<span data-ttu-id="74eb1-139">Per una copia unica, i database di origine e partner devono essere nello stesso server.</span><span class="sxs-lookup"><span data-stu-id="74eb1-139">For a one-time copy, the source and partner databases must be on the same server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74eb1-140">-Database</span><span class="sxs-lookup"><span data-stu-id="74eb1-140">-Database</span></span>
<span data-ttu-id="74eb1-141">Specifica un oggetto che rappresenta l'origine SQL database di Azure.</span><span class="sxs-lookup"><span data-stu-id="74eb1-141">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="74eb1-142">Questo parametro accetta l'input della pipeline.</span><span class="sxs-lookup"><span data-stu-id="74eb1-142">This parameter accepts pipeline input.</span></span>

```yaml
Type: Database
Parameter Sets: ByInputObject, ByInputObjectContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74eb1-143">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="74eb1-143">-DatabaseName</span></span>
<span data-ttu-id="74eb1-144">Specifica il nome del database di origine.</span><span class="sxs-lookup"><span data-stu-id="74eb1-144">Specifies the name of the source database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabaseName, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74eb1-145">-Force</span><span class="sxs-lookup"><span data-stu-id="74eb1-145">-Force</span></span>
<span data-ttu-id="74eb1-146">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="74eb1-146">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74eb1-147">-OfflineSecondary</span><span class="sxs-lookup"><span data-stu-id="74eb1-147">-OfflineSecondary</span></span>
<span data-ttu-id="74eb1-148">Specifica che una copia continua è una copia passiva anziché una copia attiva.</span><span class="sxs-lookup"><span data-stu-id="74eb1-148">Specifies that a continuous copy is a passive copy rather than an active copy.</span></span>
<span data-ttu-id="74eb1-149">Se il database di origine è un database Standard Edition, questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="74eb1-149">If the source database is a Standard edition database, then this parameter is required.</span></span>
<span data-ttu-id="74eb1-150">Se si specifica questo parametro, *deve essere specificata anche* la copia continua.</span><span class="sxs-lookup"><span data-stu-id="74eb1-150">If this parameter is specified then *ContinuousCopy* must also be specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74eb1-151">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="74eb1-151">-PartnerDatabase</span></span>
<span data-ttu-id="74eb1-152">Specifica il nome del database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="74eb1-152">Specifies name of the target database.</span></span>
<span data-ttu-id="74eb1-153">Se si specifica il *parametro ContinuousCopy,* il valore di *PartnerDatabase* deve corrispondere al nome del database di origine.</span><span class="sxs-lookup"><span data-stu-id="74eb1-153">If you specify the *ContinuousCopy* parameter, the value for *PartnerDatabase* must match the name of the source database.</span></span>
<span data-ttu-id="74eb1-154">Se non si specifica *ContinuousCopy,* è necessario specificare un nome per il database di destinazione, che può essere diverso dal nome del database di origine.</span><span class="sxs-lookup"><span data-stu-id="74eb1-154">If you do not specify *ContinuousCopy*, you must specify a name for the target database, which can be different from the source database name.</span></span>

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74eb1-155">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="74eb1-155">-PartnerServer</span></span>
<span data-ttu-id="74eb1-156">Specifica il nome del server che ospita il database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="74eb1-156">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="74eb1-157">Questo server deve essere nella stessa sottoscrizione di Azure del server di database di origine.</span><span class="sxs-lookup"><span data-stu-id="74eb1-157">This server must be in the same Azure subscription as the source database server.</span></span>

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74eb1-158">-Profile</span><span class="sxs-lookup"><span data-stu-id="74eb1-158">-Profile</span></span>
<span data-ttu-id="74eb1-159">Specifica il profilo di Azure da cui viene letto questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74eb1-159">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="74eb1-160">Se non si specifica un profilo, questo cmdlet legge dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="74eb1-160">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74eb1-161">-ServerName</span><span class="sxs-lookup"><span data-stu-id="74eb1-161">-ServerName</span></span>
<span data-ttu-id="74eb1-162">Specifica il nome del server in cui si trova il database di origine.</span><span class="sxs-lookup"><span data-stu-id="74eb1-162">Specifies the name of the server on which the source database resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="74eb1-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74eb1-163">-Confirm</span></span>
<span data-ttu-id="74eb1-164">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74eb1-164">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74eb1-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74eb1-165">-WhatIf</span></span>
<span data-ttu-id="74eb1-166">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74eb1-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74eb1-167">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="74eb1-167">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74eb1-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74eb1-168">CommonParameters</span></span>
<span data-ttu-id="74eb1-169">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74eb1-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74eb1-170">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74eb1-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74eb1-171">INPUT</span><span class="sxs-lookup"><span data-stu-id="74eb1-171">INPUTS</span></span>

### <span data-ttu-id="74eb1-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="74eb1-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="74eb1-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74eb1-173">OUTPUTS</span></span>

### <span data-ttu-id="74eb1-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="74eb1-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="74eb1-175">NOTE</span><span class="sxs-lookup"><span data-stu-id="74eb1-175">NOTES</span></span>
* <span data-ttu-id="74eb1-176">Autenticazione: questo cmdlet richiede l'autenticazione basata su certificato.</span><span class="sxs-lookup"><span data-stu-id="74eb1-176">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="74eb1-177">Per un esempio su come usare l'autenticazione basata su certificato per impostare l'abbonamento corrente, vedere New-AzureSqlDatabaseServerContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74eb1-177">For an example of how to use certificate-based authentication to set the current subscription, see New-AzureSqlDatabaseServerContext cmdlet.</span></span>
* <span data-ttu-id="74eb1-178">Monitoraggio: per verificare lo stato di una o più relazioni di copia continue attive nel server, usare il cmdlet **Get-AzureSqlDatabaseCopy.**</span><span class="sxs-lookup"><span data-stu-id="74eb1-178">Monitoring: To check for the status of one or more continuous copy relationships that are active on the server, use the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span> <span data-ttu-id="74eb1-179">Per verificare lo stato delle operazioni sia nell'origine che nella destinazione della relazione di copia continua, usare il cmdlet **Get-AzureSqlDatabaseOperation.**</span><span class="sxs-lookup"><span data-stu-id="74eb1-179">To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="74eb1-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74eb1-180">RELATED LINKS</span></span>

[<span data-ttu-id="74eb1-181">Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="74eb1-181">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="74eb1-182">Operazioni per i database SQL Azure</span><span class="sxs-lookup"><span data-stu-id="74eb1-182">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="74eb1-183">Avvia copia database</span><span class="sxs-lookup"><span data-stu-id="74eb1-183">Start Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)



[<span data-ttu-id="74eb1-184">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="74eb1-184">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="74eb1-185">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="74eb1-185">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


