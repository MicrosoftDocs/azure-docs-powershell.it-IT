---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AC2D64B9-5BCD-45D3-8650-538633F5BBBC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerServiceObjective.md
ms.openlocfilehash: 5f0786c180461522d17d2697931f4a9887935f3d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687673"
---
# <span data-ttu-id="125d6-101">Get-AzureRmSqlServerServiceObjective</span><span class="sxs-lookup"><span data-stu-id="125d6-101">Get-AzureRmSqlServerServiceObjective</span></span>

## <span data-ttu-id="125d6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="125d6-102">SYNOPSIS</span></span>
<span data-ttu-id="125d6-103">Ottiene gli obiettivi di servizio per un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="125d6-103">Gets service objectives for an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="125d6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="125d6-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerServiceObjective [[-ServiceObjectiveName] <String>] [-ServerName] <String>
 [[-DatabaseName] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="125d6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="125d6-105">DESCRIPTION</span></span>
<span data-ttu-id="125d6-106">Il cmdlet **Get-AzureRmSqlServerServiceObjective** ottiene gli obiettivi di servizio disponibili per un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="125d6-106">The **Get-AzureRmSqlServerServiceObjective** cmdlet gets the available service objectives for an Azure SQL Database server.</span></span>

## <span data-ttu-id="125d6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="125d6-107">EXAMPLES</span></span>

### <span data-ttu-id="125d6-108">Esempio 1: ottenere gli obiettivi di servizio</span><span class="sxs-lookup"><span data-stu-id="125d6-108">Example 1: Get service objectives</span></span>
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

<span data-ttu-id="125d6-109">Questo comando consente di ottenere gli obiettivi di servizio per il server denominato Server01 e il database denominato Database01.</span><span class="sxs-lookup"><span data-stu-id="125d6-109">This command gets the service objectives for the server named Server01 and the database named Database01.</span></span>

## <span data-ttu-id="125d6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="125d6-110">PARAMETERS</span></span>

### <span data-ttu-id="125d6-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="125d6-111">-DatabaseName</span></span>
<span data-ttu-id="125d6-112">Specifica il nome di un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="125d6-112">Specifies the name of an Azure SQL Database.</span></span>

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

### <span data-ttu-id="125d6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="125d6-113">-ResourceGroupName</span></span>
<span data-ttu-id="125d6-114">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="125d6-114">Specifies the name of a resource group.</span></span>
<span data-ttu-id="125d6-115">Questo cmdlet ottiene gli obiettivi di servizio per un server di database SQL assegnato alla risorsa.</span><span class="sxs-lookup"><span data-stu-id="125d6-115">This cmdlet gets service objectives for a SQL Database server assigned to this resource.</span></span>

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

### <span data-ttu-id="125d6-116">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="125d6-116">-ServerName</span></span>
<span data-ttu-id="125d6-117">Specifica il nome di un server di database SQL di database SQL.</span><span class="sxs-lookup"><span data-stu-id="125d6-117">Specifies the name of a SQL Database SQL Database server.</span></span>

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

### <span data-ttu-id="125d6-118">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="125d6-118">-ServiceObjectiveName</span></span>
<span data-ttu-id="125d6-119">Specifica il nome di un obiettivo di servizio per un server di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="125d6-119">Specifies the name of a service objective for an Azure SQL Database server.</span></span>
<span data-ttu-id="125d6-120">I valori accettabili per questo parametro sono: Basic, S0, S1, S2, P1, P2 e P3.</span><span class="sxs-lookup"><span data-stu-id="125d6-120">The acceptable values for this parameter are: Basic, S0, S1, S2, P1, P2, and P3.</span></span>

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

### <span data-ttu-id="125d6-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="125d6-121">-Confirm</span></span>
<span data-ttu-id="125d6-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="125d6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="125d6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="125d6-123">-WhatIf</span></span>
<span data-ttu-id="125d6-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="125d6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="125d6-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="125d6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="125d6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="125d6-126">-DefaultProfile</span></span>
<span data-ttu-id="125d6-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="125d6-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="125d6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="125d6-128">CommonParameters</span></span>
<span data-ttu-id="125d6-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="125d6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="125d6-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="125d6-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="125d6-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="125d6-131">INPUTS</span></span>

## <span data-ttu-id="125d6-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="125d6-132">OUTPUTS</span></span>

### <span data-ttu-id="125d6-133">Microsoft. Azure. Commands. SQL. ServiceObjective. Model. AzureSqlServerServiceObjectiveModel</span><span class="sxs-lookup"><span data-stu-id="125d6-133">Microsoft.Azure.Commands.Sql.ServiceObjective.Model.AzureSqlServerServiceObjectiveModel</span></span>

## <span data-ttu-id="125d6-134">Note</span><span class="sxs-lookup"><span data-stu-id="125d6-134">NOTES</span></span>

## <span data-ttu-id="125d6-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="125d6-135">RELATED LINKS</span></span>

[<span data-ttu-id="125d6-136">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="125d6-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


