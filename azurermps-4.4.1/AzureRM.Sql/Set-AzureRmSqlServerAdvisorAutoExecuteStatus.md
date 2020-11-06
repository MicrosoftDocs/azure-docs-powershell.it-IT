---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 6006D3AC-48E1-44A0-8BD5-CE996B8957A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAdvisorAutoExecuteStatus.md
ms.openlocfilehash: f483d3deb6c4e4ee6fb5c091dffc9b7969766d6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518279"
---
# <span data-ttu-id="b76a7-101">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b76a7-101">Set-AzureRmSqlServerAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="b76a7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b76a7-102">SYNOPSIS</span></span>
<span data-ttu-id="b76a7-103">Aggiorna lo stato di esecuzione automatica di un consulente di Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b76a7-103">Updates the auto execute status of an Azure SQL Server Advisor.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b76a7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b76a7-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAdvisorAutoExecuteStatus -AdvisorName <String>
 -AutoExecuteStatus <AdvisorAutoExecuteStatus> -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b76a7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b76a7-105">DESCRIPTION</span></span>
<span data-ttu-id="b76a7-106">Il cmdlet **set-AzureRmSqlServerAdvisorAutoExecuteStatus** imposta la proprietà di esecuzione automatica per un programma di gestione di SQL Server di Azure.</span><span class="sxs-lookup"><span data-stu-id="b76a7-106">The **Set-AzureRmSqlServerAdvisorAutoExecuteStatus** cmdlet sets the auto execute property for an Azure SQL Server Advisor.</span></span>

## <span data-ttu-id="b76a7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b76a7-107">EXAMPLES</span></span>

### <span data-ttu-id="b76a7-108">Esempio 1: abilitare l'esecuzione automatica per un consulente</span><span class="sxs-lookup"><span data-stu-id="b76a7-108">Example 1: Enable auto execute for an Advisor</span></span>
```
PS C:\>Set-AzureRmSqlServerAdvisorAutoExecuteStatus -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Server
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="b76a7-109">Questo comando Abilita lo stato di esecuzione automatica di un consulente denominato CreateIndex.</span><span class="sxs-lookup"><span data-stu-id="b76a7-109">This command enables the auto execute status of an Advisor named CreateIndex.</span></span>

## <span data-ttu-id="b76a7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b76a7-110">PARAMETERS</span></span>

### <span data-ttu-id="b76a7-111">-Advisorname</span><span class="sxs-lookup"><span data-stu-id="b76a7-111">-AdvisorName</span></span>
<span data-ttu-id="b76a7-112">Specifica il nome del consulente per il quale questo cmdlet aggiorna lo stato di esecuzione automatica.</span><span class="sxs-lookup"><span data-stu-id="b76a7-112">Specifies the name of the advisor for which this cmdlet updates the auto execute status.</span></span>

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

### <span data-ttu-id="b76a7-113">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="b76a7-113">-AutoExecuteStatus</span></span>
<span data-ttu-id="b76a7-114">Specifica il valore a cui questo cmdlet aggiorna lo stato di esecuzione automatica.</span><span class="sxs-lookup"><span data-stu-id="b76a7-114">Specifies the value to which this cmdlet updates the auto execute status.</span></span>

<span data-ttu-id="b76a7-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b76a7-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b76a7-116">Abilitato</span><span class="sxs-lookup"><span data-stu-id="b76a7-116">Enabled</span></span>
- <span data-ttu-id="b76a7-117">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="b76a7-117">Disabled</span></span>
- <span data-ttu-id="b76a7-118">Predefinita</span><span class="sxs-lookup"><span data-stu-id="b76a7-118">Default</span></span>

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

### <span data-ttu-id="b76a7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b76a7-119">-ResourceGroupName</span></span>
<span data-ttu-id="b76a7-120">Specifica il nome del gruppo di risorse del server.</span><span class="sxs-lookup"><span data-stu-id="b76a7-120">Specifies the name of the resource group of the server.</span></span>

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

### <span data-ttu-id="b76a7-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b76a7-121">-ServerName</span></span>
<span data-ttu-id="b76a7-122">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="b76a7-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="b76a7-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b76a7-123">-Confirm</span></span>
<span data-ttu-id="b76a7-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b76a7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b76a7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b76a7-125">-WhatIf</span></span>
<span data-ttu-id="b76a7-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b76a7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b76a7-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b76a7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b76a7-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b76a7-128">-DefaultProfile</span></span>
<span data-ttu-id="b76a7-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b76a7-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b76a7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b76a7-130">CommonParameters</span></span>
<span data-ttu-id="b76a7-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b76a7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b76a7-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b76a7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b76a7-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b76a7-133">INPUTS</span></span>

## <span data-ttu-id="b76a7-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b76a7-134">OUTPUTS</span></span>

### <span data-ttu-id="b76a7-135">Microsoft. Azure. Commands. SQL. Advisor. Model. AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="b76a7-135">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="b76a7-136">Note</span><span class="sxs-lookup"><span data-stu-id="b76a7-136">NOTES</span></span>
* <span data-ttu-id="b76a7-137">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, server, MSSQL, Advisor</span><span class="sxs-lookup"><span data-stu-id="b76a7-137">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="b76a7-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b76a7-138">RELATED LINKS</span></span>

[<span data-ttu-id="b76a7-139">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="b76a7-139">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="b76a7-140">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="b76a7-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
