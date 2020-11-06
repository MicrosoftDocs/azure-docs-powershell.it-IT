---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 149579bb6bbcd4ee5fe5fa192ad040e6e4c68b28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521949"
---
# <span data-ttu-id="59d73-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="59d73-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="59d73-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59d73-102">SYNOPSIS</span></span>
<span data-ttu-id="59d73-103">Modifica lo stato di esecuzione automatica di un consulente di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="59d73-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59d73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59d73-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -DatabaseName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="59d73-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59d73-105">DESCRIPTION</span></span>
<span data-ttu-id="59d73-106">Il cmdlet **set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** modifica la proprietà di esecuzione automatica per un consulente di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="59d73-106">The **Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="59d73-107">Attualmente, questo cmdlet supporta i valori enabled, disabled e default.</span><span class="sxs-lookup"><span data-stu-id="59d73-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="59d73-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59d73-108">EXAMPLES</span></span>

### <span data-ttu-id="59d73-109">Esempio 1: abilitare l'esecuzione automatica per un consulente</span><span class="sxs-lookup"><span data-stu-id="59d73-109">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -ResourceGroupName "ContosoRunnersProd" -ServerName "runner-australia-east" -DatabaseName "ContosoRunner" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
DatabaseName                   : ContosoRunner
ResourceGroupName              : ContosoRunnersProd
ServerName                     : runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="59d73-110">Questo comando modifica lo stato di esecuzione automatica di un consulente denominato CreateIndex in Enabled.</span><span class="sxs-lookup"><span data-stu-id="59d73-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="59d73-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59d73-111">PARAMETERS</span></span>

### <span data-ttu-id="59d73-112">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="59d73-112">-AdvisorName</span></span>
<span data-ttu-id="59d73-113">Specifica il nome del consulente per il quale questo cmdlet modifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="59d73-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="59d73-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="59d73-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="59d73-115">Specifica il valore per lo stato.</span><span class="sxs-lookup"><span data-stu-id="59d73-115">Specifies the value for the status.</span></span>
<span data-ttu-id="59d73-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="59d73-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="59d73-117">Abilitato</span><span class="sxs-lookup"><span data-stu-id="59d73-117">Enabled</span></span> 
- <span data-ttu-id="59d73-118">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="59d73-118">Disabled</span></span> 
- <span data-ttu-id="59d73-119">Predefinita</span><span class="sxs-lookup"><span data-stu-id="59d73-119">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59d73-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="59d73-120">-DatabaseName</span></span>
<span data-ttu-id="59d73-121">Specifica il nome del database per cui questo cmdlet modifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="59d73-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="59d73-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59d73-122">-ResourceGroupName</span></span>
<span data-ttu-id="59d73-123">Specifica il nome del gruppo di risorse del server che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="59d73-123">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="59d73-124">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="59d73-124">-ServerName</span></span>
<span data-ttu-id="59d73-125">Specifica il nome del server per il database.</span><span class="sxs-lookup"><span data-stu-id="59d73-125">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="59d73-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="59d73-126">-Confirm</span></span>
<span data-ttu-id="59d73-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59d73-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59d73-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59d73-128">-WhatIf</span></span>
<span data-ttu-id="59d73-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59d73-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59d73-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59d73-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59d73-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59d73-131">-DefaultProfile</span></span>
<span data-ttu-id="59d73-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="59d73-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59d73-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59d73-133">CommonParameters</span></span>
<span data-ttu-id="59d73-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59d73-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59d73-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59d73-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59d73-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59d73-136">INPUTS</span></span>

## <span data-ttu-id="59d73-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59d73-137">OUTPUTS</span></span>

### <span data-ttu-id="59d73-138">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="59d73-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>
<span data-ttu-id="59d73-139">Questo cmdlet restituisce un oggetto **AzureSqlDatabaseAdvisorModel** .</span><span class="sxs-lookup"><span data-stu-id="59d73-139">This cmdlet returns an **AzureSqlDatabaseAdvisorModel** object.</span></span>

## <span data-ttu-id="59d73-140">Note</span><span class="sxs-lookup"><span data-stu-id="59d73-140">NOTES</span></span>

## <span data-ttu-id="59d73-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59d73-141">RELATED LINKS</span></span>

[<span data-ttu-id="59d73-142">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="59d73-142">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="59d73-143">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="59d73-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

