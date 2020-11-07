---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverserviceobjective
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
ms.openlocfilehash: 5bcd5c6317688cc433d83b002cd3cb81ea790aaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685469"
---
# <span data-ttu-id="9bb26-101">Get-AzureRmSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="9bb26-101">Get-AzureRmSqlServerServiceObjective</span></span>

## <span data-ttu-id="9bb26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9bb26-102">SYNOPSIS</span></span>
<span data-ttu-id="9bb26-103">Ottiene gli obiettivi di servizio per un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="9bb26-103">Gets service objectives for an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bb26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9bb26-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ServerName] <String>
 [[-DatabaseName] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bb26-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bb26-105">DESCRIPTION</span></span>
<span data-ttu-id="9bb26-106">Il cmdlet **Get-AzureRmSqlServerServiceObjective** ottiene gli obiettivi di servizio disponibili per un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="9bb26-106">The **Get-AzureRmSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="9bb26-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9bb26-107">EXAMPLES</span></span>

### <span data-ttu-id="9bb26-108">Esempio 1: ottenere gli obiettivi di servizio</span><span class="sxs-lookup"><span data-stu-id="9bb26-108">Example 1: Get service objectives</span></span>
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

<span data-ttu-id="9bb26-109">Questo comando consente di ottenere gli obiettivi di servizio per il server denominato Server01 e il database denominato Database01.</span><span class="sxs-lookup"><span data-stu-id="9bb26-109">This command gets the service objectives for the server named Server01 and the database named Database01.</span></span>

## <span data-ttu-id="9bb26-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9bb26-110">PARAMETERS</span></span>

### <span data-ttu-id="9bb26-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9bb26-111">-DatabaseName</span></span>
<span data-ttu-id="9bb26-112">Nome database SQL.</span><span class="sxs-lookup"><span data-stu-id="9bb26-112">SQL Database name.</span></span>
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

### <span data-ttu-id="9bb26-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bb26-113">-DefaultProfile</span></span>
<span data-ttu-id="9bb26-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9bb26-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9bb26-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bb26-115">-ResourceGroupName</span></span>
<span data-ttu-id="9bb26-116">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9bb26-116">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9bb26-117">Questo cmdlet ottiene gli obiettivi di servizio per un server di database SQL assegnato alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="9bb26-117">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

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

### <span data-ttu-id="9bb26-118">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="9bb26-118">-ServerName</span></span>
<span data-ttu-id="9bb26-119">Specifica il nome di un server di database SQL di database SQL.</span><span class="sxs-lookup"><span data-stu-id="9bb26-119">Specifies the name of a SQL Database SQL Database server.</span></span>

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

### <span data-ttu-id="9bb26-120">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="9bb26-120">-ServiceObjectiveName</span></span>
<span data-ttu-id="9bb26-121">Specifica il nome di un obiettivo di servizio per un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="9bb26-121">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="9bb26-122">I valori accettabili per questo parametro sono: Basic, S0, S1, S2, P1, P2 e P3.</span><span class="sxs-lookup"><span data-stu-id="9bb26-122">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

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

### <span data-ttu-id="9bb26-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9bb26-123">-Confirm</span></span>
<span data-ttu-id="9bb26-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bb26-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bb26-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bb26-125">-WhatIf</span></span>
<span data-ttu-id="9bb26-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9bb26-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bb26-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9bb26-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bb26-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bb26-128">CommonParameters</span></span>
<span data-ttu-id="9bb26-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bb26-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bb26-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bb26-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bb26-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9bb26-131">INPUTS</span></span>

### <span data-ttu-id="9bb26-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9bb26-132">None</span></span>
<span data-ttu-id="9bb26-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="9bb26-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9bb26-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9bb26-134">OUTPUTS</span></span>

### <span data-ttu-id="9bb26-135">Microsoft. Azure. Commands. SQL. ServiceObjective. Model. AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="9bb26-135">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="9bb26-136">Note</span><span class="sxs-lookup"><span data-stu-id="9bb26-136">NOTES</span></span>

## <span data-ttu-id="9bb26-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9bb26-137">RELATED LINKS</span></span>

[<span data-ttu-id="9bb26-138">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="9bb26-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


