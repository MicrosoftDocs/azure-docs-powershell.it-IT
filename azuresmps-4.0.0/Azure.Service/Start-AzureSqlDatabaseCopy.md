---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc350cdf117ebbf72b023f64895f4c563e73566b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023803"
---
# <span data-ttu-id="b1493-101">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b1493-101">Start-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="b1493-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b1493-102">SYNOPSIS</span></span>
<span data-ttu-id="b1493-103">Avvia un'operazione di copia di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="b1493-103">Starts a copy operation of an Azure SQL Database.</span></span>

## <span data-ttu-id="b1493-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b1493-104">SYNTAX</span></span>

### <span data-ttu-id="b1493-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b1493-105">ByInputObject</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1493-106">ByInputObjectContinuous</span><span class="sxs-lookup"><span data-stu-id="b1493-106">ByInputObjectContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1493-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="b1493-107">ByDatabaseName</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1493-108">ByDatabaseNameContinuous</span><span class="sxs-lookup"><span data-stu-id="b1493-108">ByDatabaseNameContinuous</span></span>
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1493-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b1493-109">DESCRIPTION</span></span>
<span data-ttu-id="b1493-110">Il cmdlet **Start-AzureSqlDatabaseCopy** avvia un'operazione di copia unica o un'operazione di copia continua di un database SQL di Azure specifico.</span><span class="sxs-lookup"><span data-stu-id="b1493-110">The **Start-AzureSqlDatabaseCopy** cmdlet starts a one-time copy operation or a continuous copy operation of a specific Azure SQL Database.</span></span>
<span data-ttu-id="b1493-111">Questo cmdlet non è transazionale.</span><span class="sxs-lookup"><span data-stu-id="b1493-111">This cmdlet is not transactional.</span></span>

<span data-ttu-id="b1493-112">Il database originale è il database di origine.</span><span class="sxs-lookup"><span data-stu-id="b1493-112">The original database is the source database.</span></span>
<span data-ttu-id="b1493-113">La copia è il database secondario o di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b1493-113">The copy is the secondary or target database.</span></span>
<span data-ttu-id="b1493-114">Per una copia continua, i database di origine e di destinazione non possono trovarsi nello stesso server e i server che ospitano i database di origine e di destinazione devono far parte della stessa sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="b1493-114">For a continuous copy, the source and target databases cannot reside on the same server, and the servers that host the source and target databases must be part of the same subscription.</span></span>

<span data-ttu-id="b1493-115">Se non specifichi il parametro *ContinuousCopy* , questo cmdlet crea una copia unica del database di origine.</span><span class="sxs-lookup"><span data-stu-id="b1493-115">If you do not specify the *ContinuousCopy* parameter, this cmdlet creates a one-time copy of the source database.</span></span>
<span data-ttu-id="b1493-116">Quando la risposta viene ricevuta, l'operazione può essere ancora in corso.</span><span class="sxs-lookup"><span data-stu-id="b1493-116">When the response is received, the operation can still be in progress.</span></span>
<span data-ttu-id="b1493-117">Puoi monitorare l'operazione usando il cmdlet Get-AzureSqlDatabaseCopy o Get-AzureSqlDatabaseOperation.</span><span class="sxs-lookup"><span data-stu-id="b1493-117">You can monitor the operation by using the Get-AzureSqlDatabaseCopy or Get-AzureSqlDatabaseOperation cmdlet.</span></span>

<span data-ttu-id="b1493-118">Se specifichi *ContinuousCopy* , questo cmdlet crea una copia continua del database di origine.</span><span class="sxs-lookup"><span data-stu-id="b1493-118">If you specify *ContinuousCopy* , this cmdlet creates a continuous copy of the source database.</span></span>
<span data-ttu-id="b1493-119">Quando la risposta viene ricevuta, l'operazione sarà in corso.</span><span class="sxs-lookup"><span data-stu-id="b1493-119">When the response is received, the operation will be in progress.</span></span>
<span data-ttu-id="b1493-120">Puoi monitorare l'operazione usando **Get-AzureSqlDatabaseCopy** o **Get-AzureSqlDatabaseOperation**.</span><span class="sxs-lookup"><span data-stu-id="b1493-120">You can monitor the operation by using **Get-AzureSqlDatabaseCopy** or **Get-AzureSqlDatabaseOperation**.</span></span>

<span data-ttu-id="b1493-121">È possibile creare una copia continua come database online o offline.</span><span class="sxs-lookup"><span data-stu-id="b1493-121">You can create a continuous copy as an online or offline database.</span></span>
<span data-ttu-id="b1493-122">La copia continua online viene usata per configurare Active Geo-Replication for Azure SQL database https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ .</span><span class="sxs-lookup"><span data-stu-id="b1493-122">The online continuous copy is used to configure Active Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/.</span></span>
<span data-ttu-id="b1493-123">La copia continua offline viene usata per configurare Geo-Replication standard per il database SQL di Azure https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ .</span><span class="sxs-lookup"><span data-stu-id="b1493-123">The offline continuous copy is used to configure Standard Geo-Replication for Azure SQL Databasehttps://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/.</span></span>

## <span data-ttu-id="b1493-124">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b1493-124">EXAMPLES</span></span>

### <span data-ttu-id="b1493-125">Esempio 1: pianificare una copia di un database continuo</span><span class="sxs-lookup"><span data-stu-id="b1493-125">Example 1: Schedule a continuous database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

<span data-ttu-id="b1493-126">Questo comando Pianifica una copia continua del database denominata Orders sul server denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="b1493-126">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="b1493-127">Il comando crea un database di destinazione nel server denominato bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="b1493-127">The command creates a target database on the server named bk0b8kf658.</span></span>

### <span data-ttu-id="b1493-128">Esempio 2: creare una copia unica nello stesso server</span><span class="sxs-lookup"><span data-stu-id="b1493-128">Example 2: Create a one-time copy on the same server</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

<span data-ttu-id="b1493-129">Questo comando crea una copia unica del database denominata Orders sul server denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="b1493-129">This command creates a one-time copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="b1493-130">Il comando crea una copia denominata OrdersCopy nello stesso server.</span><span class="sxs-lookup"><span data-stu-id="b1493-130">The command creates a copy named OrdersCopy on the same server.</span></span>

### <span data-ttu-id="b1493-131">Esempio 3: pianificare una copia del database offline continua</span><span class="sxs-lookup"><span data-stu-id="b1493-131">Example 3: Schedule a continuous offline database copy</span></span>
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

<span data-ttu-id="b1493-132">Questo comando Pianifica una copia continua del database denominata Orders sul server denominato lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="b1493-132">This command schedules a continuous copy of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="b1493-133">Questo comando crea un database di destinazione offline nel server denominato bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="b1493-133">This command creates an offline target database on the server named bk0b8kf658.</span></span>

## <span data-ttu-id="b1493-134">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b1493-134">PARAMETERS</span></span>

### <span data-ttu-id="b1493-135">-ContinuousCopy</span><span class="sxs-lookup"><span data-stu-id="b1493-135">-ContinuousCopy</span></span>
<span data-ttu-id="b1493-136">Indica che la copia del database sarà una copia continua (un database di replica).</span><span class="sxs-lookup"><span data-stu-id="b1493-136">Indicates that the database copy will be a continuous-copy (a replica database).</span></span>
<span data-ttu-id="b1493-137">La copia continua non è supportata nello stesso server.</span><span class="sxs-lookup"><span data-stu-id="b1493-137">Continuous copy is not supported within the same server.</span></span>
<span data-ttu-id="b1493-138">Se questo parametro non viene specificato, viene eseguita una copia unica.</span><span class="sxs-lookup"><span data-stu-id="b1493-138">If this parameter is not specified, then a one-time copy is performed.</span></span>
<span data-ttu-id="b1493-139">Per una copia unica, i database di origine e partner devono essere nello stesso server.</span><span class="sxs-lookup"><span data-stu-id="b1493-139">For a one-time copy, the source and partner databases must be on the same server.</span></span>

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

### <span data-ttu-id="b1493-140">-Database</span><span class="sxs-lookup"><span data-stu-id="b1493-140">-Database</span></span>
<span data-ttu-id="b1493-141">Specifica un oggetto che rappresenta il database SQL di Azure di origine.</span><span class="sxs-lookup"><span data-stu-id="b1493-141">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="b1493-142">Questo parametro accetta l'input della pipeline.</span><span class="sxs-lookup"><span data-stu-id="b1493-142">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="b1493-143">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b1493-143">-DatabaseName</span></span>
<span data-ttu-id="b1493-144">Specifica il nome del database di origine.</span><span class="sxs-lookup"><span data-stu-id="b1493-144">Specifies the name of the source database.</span></span>

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

### <span data-ttu-id="b1493-145">-Force</span><span class="sxs-lookup"><span data-stu-id="b1493-145">-Force</span></span>
<span data-ttu-id="b1493-146">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="b1493-146">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b1493-147">-OfflineSecondary</span><span class="sxs-lookup"><span data-stu-id="b1493-147">-OfflineSecondary</span></span>
<span data-ttu-id="b1493-148">Specifica che una copia continua è una copia passiva anziché una copia attiva.</span><span class="sxs-lookup"><span data-stu-id="b1493-148">Specifies that a continuous copy is a passive copy rather than an active copy.</span></span>
<span data-ttu-id="b1493-149">Se il database di origine è un database Standard Edition, questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b1493-149">If the source database is a Standard edition database, then this parameter is required.</span></span>
<span data-ttu-id="b1493-150">Se questo parametro viene specificato, deve essere specificato anche *ContinuousCopy* .</span><span class="sxs-lookup"><span data-stu-id="b1493-150">If this parameter is specified then *ContinuousCopy* must also be specified.</span></span>

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

### <span data-ttu-id="b1493-151">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="b1493-151">-PartnerDatabase</span></span>
<span data-ttu-id="b1493-152">Specifica il nome del database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b1493-152">Specifies name of the target database.</span></span>
<span data-ttu-id="b1493-153">Se specifichi il parametro *ContinuousCopy* , il valore di *PartnerDatabase* deve corrispondere al nome del database di origine.</span><span class="sxs-lookup"><span data-stu-id="b1493-153">If you specify the *ContinuousCopy* parameter, the value for *PartnerDatabase* must match the name of the source database.</span></span>
<span data-ttu-id="b1493-154">Se non specifichi *ContinuousCopy* , devi specificare un nome per il database di destinazione, che può essere diverso dal nome del database di origine.</span><span class="sxs-lookup"><span data-stu-id="b1493-154">If you do not specify *ContinuousCopy* , you must specify a name for the target database, which can be different from the source database name.</span></span>

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

### <span data-ttu-id="b1493-155">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="b1493-155">-PartnerServer</span></span>
<span data-ttu-id="b1493-156">Specifica il nome del server che ospita il database di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b1493-156">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="b1493-157">Questo server deve essere nella stessa sottoscrizione di Azure del server di database di origine.</span><span class="sxs-lookup"><span data-stu-id="b1493-157">This server must be in the same Azure subscription as the source database server.</span></span>

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

### <span data-ttu-id="b1493-158">-Profile</span><span class="sxs-lookup"><span data-stu-id="b1493-158">-Profile</span></span>
<span data-ttu-id="b1493-159">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1493-159">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b1493-160">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="b1493-160">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b1493-161">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b1493-161">-ServerName</span></span>
<span data-ttu-id="b1493-162">Specifica il nome del server in cui risiede il database di origine.</span><span class="sxs-lookup"><span data-stu-id="b1493-162">Specifies the name of the server on which the source database resides.</span></span>

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

### <span data-ttu-id="b1493-163">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b1493-163">-Confirm</span></span>
<span data-ttu-id="b1493-164">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1493-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1493-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1493-165">-WhatIf</span></span>
<span data-ttu-id="b1493-166">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1493-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1493-167">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b1493-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1493-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1493-168">CommonParameters</span></span>
<span data-ttu-id="b1493-169">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1493-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1493-170">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1493-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1493-171">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b1493-171">INPUTS</span></span>

### <span data-ttu-id="b1493-172">Microsoft. WindowsAzure. Commands. SqlDatabase. Services. Server. database</span><span class="sxs-lookup"><span data-stu-id="b1493-172">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="b1493-173">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b1493-173">OUTPUTS</span></span>

### <span data-ttu-id="b1493-174">Microsoft. WindowsAzure. Commands. SqlDatabase. Model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b1493-174">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="b1493-175">Note</span><span class="sxs-lookup"><span data-stu-id="b1493-175">NOTES</span></span>
* <span data-ttu-id="b1493-176">Autenticazione: questo cmdlet richiede l'autenticazione basata su certificati.</span><span class="sxs-lookup"><span data-stu-id="b1493-176">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="b1493-177">Per un esempio di come usare l'autenticazione basata su certificati per impostare la sottoscrizione corrente, vedere cmdlet New-AzureSqlDatabaseServerContext.</span><span class="sxs-lookup"><span data-stu-id="b1493-177">For an example of how to use certificate-based authentication to set the current subscription, see New-AzureSqlDatabaseServerContext cmdlet.</span></span>
* <span data-ttu-id="b1493-178">Monitoraggio: per verificare lo stato di una o più relazioni di copia continue attive nel server, usare il cmdlet **Get-AzureSqlDatabaseCopy** .</span><span class="sxs-lookup"><span data-stu-id="b1493-178">Monitoring: To check for the status of one or more continuous copy relationships that are active on the server, use the **Get-AzureSqlDatabaseCopy** cmdlet.</span></span> <span data-ttu-id="b1493-179">Per verificare lo stato delle operazioni sia per l'origine che per la destinazione della relazione di copia continua, usare il cmdlet **Get-AzureSqlDatabaseOperation** .</span><span class="sxs-lookup"><span data-stu-id="b1493-179">To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="b1493-180">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b1493-180">RELATED LINKS</span></span>

[<span data-ttu-id="b1493-181">Database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="b1493-181">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="b1493-182">Operazioni per i database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="b1493-182">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="b1493-183">Avviare la copia del database</span><span class="sxs-lookup"><span data-stu-id="b1493-183">Start Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)

[<span data-ttu-id="b1493-184">Cmdlet di database SQL di Azure</span><span class="sxs-lookup"><span data-stu-id="b1493-184">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="b1493-185">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b1493-185">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="b1493-186">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="b1493-186">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


