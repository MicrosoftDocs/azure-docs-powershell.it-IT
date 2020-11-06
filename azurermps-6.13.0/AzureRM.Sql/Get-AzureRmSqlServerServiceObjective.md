---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
ms.openlocfilehash: 13ce7a2410f8231d4c5194fbd57d41074d0ca892
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509060"
---
# <span data-ttu-id="4b561-101">Get-AzureRmSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="4b561-101">Get-AzureRmSqlServerServiceObjective</span></span>

## <span data-ttu-id="4b561-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4b561-102">SYNOPSIS</span></span>
<span data-ttu-id="4b561-103">Ottiene gli obiettivi di servizio per un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b561-103">Gets service objectives for an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b561-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b561-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ServerName] <String>
 [[-DatabaseName] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b561-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b561-105">DESCRIPTION</span></span>
<span data-ttu-id="4b561-106">Il cmdlet **Get-AzureRmSqlServerServiceObjective** ottiene gli obiettivi di servizio disponibili per un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b561-106">The **Get-AzureRmSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="4b561-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b561-107">EXAMPLES</span></span>

### <span data-ttu-id="4b561-108">Esempio 1: ottenere gli obiettivi di servizio</span><span class="sxs-lookup"><span data-stu-id="4b561-108">Example 1: Get service objectives</span></span>
```
PS C:\>Get-AzureRmSqlServerServiceObjective -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ResourceGroupName ServerName ServiceObjectiveName Description Enabled IsDefault IsSystem
----------------- ---------- -------------------- ----------- ------- --------- --------
resourcegroup01   server01   ElasticPool                         True     False    False
resourcegroup01   server01   System                              True     False     True
resourcegroup01   server01   System0                             True     False     True
resourcegroup01   server01   System1                             True     False     True
resourcegroup01   server01   System2                             True      True     True
resourcegroup01   server01   Basic                               True      True    False
resourcegroup01   server01   S0                                  True      True    False
resourcegroup01   server01   S1                                  True     False    False
resourcegroup01   server01   S2                                  True     False    False
resourcegroup01   server01   S3                                  True     False    False
resourcegroup01   server01   P1                                  True      True    False
resourcegroup01   server01   P2                                  True     False    False
resourcegroup01   server01   P3                                  True     False    False
resourcegroup01   server01   P4                                  True     False    False
```

<span data-ttu-id="4b561-109">Questo comando consente di ottenere gli obiettivi di servizio per il server denominato Server01 e il database denominato Database01.</span><span class="sxs-lookup"><span data-stu-id="4b561-109">This command gets the service objectives for the server named Server01 and the database named Database01.</span></span>

## <span data-ttu-id="4b561-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4b561-110">PARAMETERS</span></span>

### <span data-ttu-id="4b561-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4b561-111">-DatabaseName</span></span>
<span data-ttu-id="4b561-112">Nome database SQL.</span><span class="sxs-lookup"><span data-stu-id="4b561-112">SQL Database name.</span></span>

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

### <span data-ttu-id="4b561-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b561-113">-DefaultProfile</span></span>
<span data-ttu-id="4b561-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4b561-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b561-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b561-115">-ResourceGroupName</span></span>
<span data-ttu-id="4b561-116">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="4b561-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="4b561-117">Questo cmdlet ottiene gli obiettivi di servizio per un server di database SQL assegnato alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="4b561-117">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

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

### <span data-ttu-id="4b561-118">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="4b561-118">-ServerName</span></span>
<span data-ttu-id="4b561-119">Specifica il nome di un server di database SQL di database SQL.</span><span class="sxs-lookup"><span data-stu-id="4b561-119">Specifies the name of a SQL Database SQL Database server.</span></span>

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

### <span data-ttu-id="4b561-120">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="4b561-120">-ServiceObjectiveName</span></span>
<span data-ttu-id="4b561-121">Specifica il nome di un obiettivo di servizio per un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b561-121">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="4b561-122">I valori accettabili per questo parametro sono: Basic, S0, S1, S2, P1, P2 e P3.</span><span class="sxs-lookup"><span data-stu-id="4b561-122">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

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

### <span data-ttu-id="4b561-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4b561-123">-Confirm</span></span>
<span data-ttu-id="4b561-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b561-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b561-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b561-125">-WhatIf</span></span>
<span data-ttu-id="4b561-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b561-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b561-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b561-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b561-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b561-128">CommonParameters</span></span>
<span data-ttu-id="4b561-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b561-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b561-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b561-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b561-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4b561-131">INPUTS</span></span>

### <span data-ttu-id="4b561-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4b561-132">System.String</span></span>

## <span data-ttu-id="4b561-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b561-133">OUTPUTS</span></span>

### <span data-ttu-id="4b561-134">Microsoft. Azure. Commands. SQL. ServiceObjective. Model. AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="4b561-134">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="4b561-135">Note</span><span class="sxs-lookup"><span data-stu-id="4b561-135">NOTES</span></span>

## <span data-ttu-id="4b561-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b561-136">RELATED LINKS</span></span>

[<span data-ttu-id="4b561-137">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="4b561-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


