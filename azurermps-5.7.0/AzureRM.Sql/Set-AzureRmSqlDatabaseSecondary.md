---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 2c1853de6eb11c304014ac45b5469c5699105824
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512152"
---
# <span data-ttu-id="94c2f-101">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="94c2f-101">Set-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="94c2f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="94c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="94c2f-103">Commuta un database secondario come primario per avviare il failover.</span><span class="sxs-lookup"><span data-stu-id="94c2f-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="94c2f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="94c2f-104">SYNTAX</span></span>

### <span data-ttu-id="94c2f-105">NoOptionsSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="94c2f-105">NoOptionsSet (Default)</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94c2f-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="94c2f-106">ByFailoverParams</span></span>
```
Set-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94c2f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="94c2f-107">DESCRIPTION</span></span>
<span data-ttu-id="94c2f-108">Il cmdlet **set-AzureRmSqlDatabaseSecondary** passa un database secondario come primario per avviare il failover.</span><span class="sxs-lookup"><span data-stu-id="94c2f-108">The **Set-AzureRmSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="94c2f-109">Questo cmdlet è progettato come comando di configurazione generale, ma attualmente è limitato all'avvio del failover.</span><span class="sxs-lookup"><span data-stu-id="94c2f-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="94c2f-110">Specifica il parametro *AllowDataLoss* per avviare un failover della forza durante un'interruzione.</span><span class="sxs-lookup"><span data-stu-id="94c2f-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="94c2f-111">Non è necessario specificare questo parametro quando si esegue un'operazione pianificata, ad esempio esercitazione di ripristino.</span><span class="sxs-lookup"><span data-stu-id="94c2f-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="94c2f-112">In quest'ultimo caso, il database secondario viene sincronizzato con il principale prima che venga attivato.</span><span class="sxs-lookup"><span data-stu-id="94c2f-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="94c2f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="94c2f-113">EXAMPLES</span></span>

## <span data-ttu-id="94c2f-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="94c2f-114">PARAMETERS</span></span>

### <span data-ttu-id="94c2f-115">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="94c2f-115">-AllowDataLoss</span></span>
<span data-ttu-id="94c2f-116">Indica che questa operazione di failover consente la perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="94c2f-116">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c2f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94c2f-117">-AsJob</span></span>
<span data-ttu-id="94c2f-118">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="94c2f-118">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="94c2f-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="94c2f-119">-DatabaseName</span></span>
<span data-ttu-id="94c2f-120">Specifica il nome del database SQL di Azure secondario.</span><span class="sxs-lookup"><span data-stu-id="94c2f-120">Specifies the name of the Azure SQL Database Secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94c2f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94c2f-121">-DefaultProfile</span></span>
<span data-ttu-id="94c2f-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="94c2f-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94c2f-123">-Failover</span><span class="sxs-lookup"><span data-stu-id="94c2f-123">-Failover</span></span>
<span data-ttu-id="94c2f-124">Indica che questa operazione è un failover.</span><span class="sxs-lookup"><span data-stu-id="94c2f-124">Indicates that this operation is a failover.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94c2f-125">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94c2f-125">-PartnerResourceGroupName</span></span>
<span data-ttu-id="94c2f-126">Specifica il nome del gruppo di risorse a cui è assegnato il database SQL di Azure partner.</span><span class="sxs-lookup"><span data-stu-id="94c2f-126">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94c2f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94c2f-127">-ResourceGroupName</span></span>
<span data-ttu-id="94c2f-128">Specifica il nome del gruppo di risorse a cui è assegnato il database SQL di Azure secondario.</span><span class="sxs-lookup"><span data-stu-id="94c2f-128">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="94c2f-129">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="94c2f-129">-ServerName</span></span>
<span data-ttu-id="94c2f-130">Specifica il nome di SQL Server che ospita il database SQL di Azure secondario.</span><span class="sxs-lookup"><span data-stu-id="94c2f-130">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="94c2f-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="94c2f-131">-Confirm</span></span>
<span data-ttu-id="94c2f-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94c2f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94c2f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94c2f-133">-WhatIf</span></span>
<span data-ttu-id="94c2f-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94c2f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94c2f-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="94c2f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94c2f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94c2f-136">CommonParameters</span></span>
<span data-ttu-id="94c2f-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94c2f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94c2f-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94c2f-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94c2f-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="94c2f-139">INPUTS</span></span>

###  
<span data-ttu-id="94c2f-140">È possibile eseguire il failover delle istanze dell'oggetto di **database** per il database secondario e impostare il database primario su questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94c2f-140">You can pipe instances of the **Database** object for the secondary database to fail over and make the primary database to this cmdlet.</span></span>

## <span data-ttu-id="94c2f-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="94c2f-141">OUTPUTS</span></span>

###  
<span data-ttu-id="94c2f-142">Questo cmdlet restituisce un **ReplicationLink**.</span><span class="sxs-lookup"><span data-stu-id="94c2f-142">This cmdlet returns a **ReplicationLink**.</span></span>

## <span data-ttu-id="94c2f-143">Note</span><span class="sxs-lookup"><span data-stu-id="94c2f-143">NOTES</span></span>

## <span data-ttu-id="94c2f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="94c2f-144">RELATED LINKS</span></span>

[<span data-ttu-id="94c2f-145">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="94c2f-145">New-AzureRmSqlDatabaseSecondary</span></span>](./New-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="94c2f-146">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="94c2f-146">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="94c2f-147">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="94c2f-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
