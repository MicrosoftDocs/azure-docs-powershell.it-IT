---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 7af5736e2f66b8bf428815456ba95b3c5b4b6182
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685804"
---
# <span data-ttu-id="9aa77-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="9aa77-101">Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="9aa77-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9aa77-102">SYNOPSIS</span></span>
<span data-ttu-id="9aa77-103">Modifica lo stato di esecuzione automatica di un consulente di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="9aa77-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9aa77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9aa77-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> -DatabaseName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9aa77-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9aa77-105">DESCRIPTION</span></span>
<span data-ttu-id="9aa77-106">Il cmdlet **set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** modifica la proprietà di esecuzione automatica per un consulente di database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="9aa77-106">The **Set-AzureRmSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="9aa77-107">Attualmente, questo cmdlet supporta i valori enabled, disabled e default.</span><span class="sxs-lookup"><span data-stu-id="9aa77-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="9aa77-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9aa77-108">EXAMPLES</span></span>

### <span data-ttu-id="9aa77-109">Esempio 1: abilitare l'esecuzione automatica per un consulente</span><span class="sxs-lookup"><span data-stu-id="9aa77-109">Example 1: Enable auto execute for an advisor</span></span>
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

<span data-ttu-id="9aa77-110">Questo comando modifica lo stato di esecuzione automatica di un consulente denominato CreateIndex in Enabled.</span><span class="sxs-lookup"><span data-stu-id="9aa77-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="9aa77-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9aa77-111">PARAMETERS</span></span>

### <span data-ttu-id="9aa77-112">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="9aa77-112">-AdvisorName</span></span>
<span data-ttu-id="9aa77-113">Specifica il nome del consulente per il quale questo cmdlet modifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="9aa77-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="9aa77-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="9aa77-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="9aa77-115">Specifica il valore per lo stato.</span><span class="sxs-lookup"><span data-stu-id="9aa77-115">Specifies the value for the status.</span></span>
<span data-ttu-id="9aa77-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="9aa77-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9aa77-117">Abilitato</span><span class="sxs-lookup"><span data-stu-id="9aa77-117">Enabled</span></span> 
- <span data-ttu-id="9aa77-118">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="9aa77-118">Disabled</span></span> 
- <span data-ttu-id="9aa77-119">Predefinita</span><span class="sxs-lookup"><span data-stu-id="9aa77-119">Default</span></span>

```yaml
Type: AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aa77-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9aa77-120">-DatabaseName</span></span>
<span data-ttu-id="9aa77-121">Specifica il nome del database per cui questo cmdlet modifica lo stato.</span><span class="sxs-lookup"><span data-stu-id="9aa77-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="9aa77-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aa77-122">-DefaultProfile</span></span>
<span data-ttu-id="9aa77-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9aa77-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9aa77-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9aa77-124">-ResourceGroupName</span></span>
<span data-ttu-id="9aa77-125">Specifica il nome del gruppo di risorse del server che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="9aa77-125">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="9aa77-126">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="9aa77-126">-ServerName</span></span>
<span data-ttu-id="9aa77-127">Specifica il nome del server per il database.</span><span class="sxs-lookup"><span data-stu-id="9aa77-127">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="9aa77-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9aa77-128">-Confirm</span></span>
<span data-ttu-id="9aa77-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9aa77-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa77-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9aa77-130">-WhatIf</span></span>
<span data-ttu-id="9aa77-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9aa77-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9aa77-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9aa77-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa77-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aa77-133">CommonParameters</span></span>
<span data-ttu-id="9aa77-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9aa77-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aa77-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9aa77-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aa77-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9aa77-136">INPUTS</span></span>

### <span data-ttu-id="9aa77-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9aa77-137">None</span></span>
<span data-ttu-id="9aa77-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="9aa77-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9aa77-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9aa77-139">OUTPUTS</span></span>

### <span data-ttu-id="9aa77-140">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="9aa77-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>
<span data-ttu-id="9aa77-141">Questo cmdlet restituisce un oggetto **AzureSqlDatabaseAdvisorModel** .</span><span class="sxs-lookup"><span data-stu-id="9aa77-141">This cmdlet returns an **AzureSqlDatabaseAdvisorModel** object.</span></span>

## <span data-ttu-id="9aa77-142">Note</span><span class="sxs-lookup"><span data-stu-id="9aa77-142">NOTES</span></span>

## <span data-ttu-id="9aa77-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9aa77-143">RELATED LINKS</span></span>

[<span data-ttu-id="9aa77-144">Get-AzureRmSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="9aa77-144">Get-AzureRmSqlDatabaseAdvisor</span></span>](./Get-AzureRmSqlDatabaseAdvisor.md)

[<span data-ttu-id="9aa77-145">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="9aa77-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

