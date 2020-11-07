---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 0082918e09c0f42910ead42d03319577d4b4c9c8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676689"
---
# <span data-ttu-id="6a12f-101">Stop-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="6a12f-101">Stop-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="6a12f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a12f-102">SYNOPSIS</span></span>
<span data-ttu-id="6a12f-103">Annulla l'operazione di aggiornamento asincrono in un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="6a12f-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="6a12f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a12f-104">SYNTAX</span></span>

```
Stop-AzSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a12f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a12f-105">DESCRIPTION</span></span>
<span data-ttu-id="6a12f-106">Il cmdlet **Stop-AzSqlElasticPoolActivity** Annulla l'operazione di aggiornamento asincrono in un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="6a12f-106">The **Stop-AzSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="6a12f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a12f-107">EXAMPLES</span></span>

### <span data-ttu-id="6a12f-108">Esempio 1: annullare l'operazione di aggiornamento asincrono in un pool elastico</span><span class="sxs-lookup"><span data-stu-id="6a12f-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

OperationId     : af97005d-9243-4f8a-844e-402d1cc855f5
ServerName      : Server01
DatabaseName    : ElasticPool01
State           : CANCELLED
Operation       : UpdateLogicalElasticPool
ErrorCode       :
ErrorMessage    :
ErrorSeverity   :
StartTime       : 10/15/2017 02:49:42 PM
EndTime         : 10/15/2017 02:49:43 PM
PercentComplete :
```

<span data-ttu-id="6a12f-109">Questo comando Annulla l'operazione di aggiornamento asincrono sul pool elastico.</span><span class="sxs-lookup"><span data-stu-id="6a12f-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="6a12f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a12f-110">PARAMETERS</span></span>

### <span data-ttu-id="6a12f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a12f-111">-DefaultProfile</span></span>
<span data-ttu-id="6a12f-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a12f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a12f-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="6a12f-113">-ElasticPoolName</span></span>
<span data-ttu-id="6a12f-114">Il nome del pool di Azure SQL elastico.</span><span class="sxs-lookup"><span data-stu-id="6a12f-114">The name of the Azure SQL Elastic Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a12f-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="6a12f-115">-OperationId</span></span>
<span data-ttu-id="6a12f-116">ID dell'operazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="6a12f-116">The ID of the operation to retrieve.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a12f-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a12f-117">-PassThru</span></span>
<span data-ttu-id="6a12f-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="6a12f-118">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a12f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a12f-119">-ResourceGroupName</span></span>
<span data-ttu-id="6a12f-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6a12f-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="6a12f-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="6a12f-121">-ServerName</span></span>
<span data-ttu-id="6a12f-122">Nome di Azure SQL Server in cui è presente il pool di elastici.</span><span class="sxs-lookup"><span data-stu-id="6a12f-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="6a12f-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6a12f-123">-Confirm</span></span>
<span data-ttu-id="6a12f-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a12f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a12f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a12f-125">-WhatIf</span></span>
<span data-ttu-id="6a12f-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a12f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a12f-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a12f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a12f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a12f-128">CommonParameters</span></span>
<span data-ttu-id="6a12f-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a12f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a12f-130">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a12f-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a12f-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a12f-131">INPUTS</span></span>

### <span data-ttu-id="6a12f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="6a12f-132">System.String</span></span>

### <span data-ttu-id="6a12f-133">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6a12f-133">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6a12f-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a12f-134">OUTPUTS</span></span>

### <span data-ttu-id="6a12f-135">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="6a12f-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="6a12f-136">Note</span><span class="sxs-lookup"><span data-stu-id="6a12f-136">NOTES</span></span>

## <span data-ttu-id="6a12f-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a12f-137">RELATED LINKS</span></span>
