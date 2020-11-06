---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/switch-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Switch-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Switch-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: b11478e02baa515fdbd3f3625392616245f2b935
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519831"
---
# <span data-ttu-id="9b859-101">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9b859-101">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="9b859-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9b859-102">SYNOPSIS</span></span>
<span data-ttu-id="9b859-103">Esegue un failover di un gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="9b859-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b859-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b859-104">SYNTAX</span></span>

```
Switch-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b859-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b859-105">DESCRIPTION</span></span>
<span data-ttu-id="9b859-106">Questo comando scambia i ruoli dei server in un gruppo di failover e passa tutti i database secondari al ruolo principale.</span><span class="sxs-lookup"><span data-stu-id="9b859-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="9b859-107">Tutte le nuove sessioni TDS vengono reinstradate automaticamente al server secondario dopo l'aggiornamento della cache del client DNS.</span><span class="sxs-lookup"><span data-stu-id="9b859-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="9b859-108">Quando il server primario originale è di nuovo online, tutti i database primari in precedenza verranno passati al ruolo secondario.</span><span class="sxs-lookup"><span data-stu-id="9b859-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>

<span data-ttu-id="9b859-109">Il server secondario del gruppo di failover deve essere usato per eseguire questo comando.</span><span class="sxs-lookup"><span data-stu-id="9b859-109">The Failover Group's secondary server must be used to execute this command.</span></span>

## <span data-ttu-id="9b859-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b859-110">EXAMPLES</span></span>

### <span data-ttu-id="9b859-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9b859-111">Example 1</span></span>
```
C:\> Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzureRmSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="9b859-112">Eseguire un'operazione di failover per consentire la perdita dei dati tramite piping nel gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="9b859-112">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="9b859-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9b859-113">Example 2</span></span>
```
C:\> Switch-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="9b859-114">Eseguire un'operazione di failover ottimale dello sforzo che avrà esito positivo senza perdere dati o non riesce e ripristinare il rollback.</span><span class="sxs-lookup"><span data-stu-id="9b859-114">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="9b859-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9b859-115">PARAMETERS</span></span>

### <span data-ttu-id="9b859-116">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="9b859-116">-AllowDataLoss</span></span>
<span data-ttu-id="9b859-117">Completare il failover anche se tale operazione può causare una perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="9b859-117">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="9b859-118">In questo modo il failover verrà continuato anche se un database primario non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="9b859-118">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b859-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b859-119">-AsJob</span></span>
<span data-ttu-id="9b859-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9b859-120">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="9b859-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b859-121">-DefaultProfile</span></span>
<span data-ttu-id="9b859-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9b859-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b859-123">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="9b859-123">-FailoverGroupName</span></span>
<span data-ttu-id="9b859-124">Nome del gruppo di failover di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="9b859-124">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b859-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b859-125">-ResourceGroupName</span></span>
<span data-ttu-id="9b859-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9b859-126">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b859-127">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="9b859-127">-ServerName</span></span>
<span data-ttu-id="9b859-128">Nome del server di database SQL di Azure secondario del gruppo di failover.</span><span class="sxs-lookup"><span data-stu-id="9b859-128">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b859-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9b859-129">-Confirm</span></span>
<span data-ttu-id="9b859-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b859-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b859-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b859-131">-WhatIf</span></span>
<span data-ttu-id="9b859-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b859-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b859-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b859-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b859-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b859-134">CommonParameters</span></span>
<span data-ttu-id="9b859-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b859-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b859-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b859-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b859-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9b859-137">INPUTS</span></span>

### <span data-ttu-id="9b859-138">System. String</span><span class="sxs-lookup"><span data-stu-id="9b859-138">System.String</span></span>

## <span data-ttu-id="9b859-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b859-139">OUTPUTS</span></span>

### <span data-ttu-id="9b859-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="9b859-140">System.Object</span></span>

## <span data-ttu-id="9b859-141">Note</span><span class="sxs-lookup"><span data-stu-id="9b859-141">NOTES</span></span>

## <span data-ttu-id="9b859-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b859-142">RELATED LINKS</span></span>

[<span data-ttu-id="9b859-143">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9b859-143">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9b859-144">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9b859-144">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9b859-145">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9b859-145">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9b859-146">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9b859-146">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="9b859-147">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9b859-147">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="9b859-148">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="9b859-148">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="9b859-149">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="9b859-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
