---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: 999fd83af11422f1499e386f194fd75d9b99e152
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513320"
---
# <span data-ttu-id="56ed7-101">Stop-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="56ed7-101">Stop-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="56ed7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56ed7-102">SYNOPSIS</span></span>
<span data-ttu-id="56ed7-103">Annulla l'operazione di aggiornamento asincrono in un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="56ed7-103">Cancels the asynchronous update operation on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56ed7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56ed7-104">SYNTAX</span></span>

```
Stop-AzureRmSqlElasticPoolActivity [-PassThru] [-ServerName] <String> [-ElasticPoolName] <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56ed7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56ed7-105">DESCRIPTION</span></span>
<span data-ttu-id="56ed7-106">Il cmdlet **Stop-AzureRmSqlElasticPoolActivity** Annulla l'operazione di aggiornamento asincrono in un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="56ed7-106">The **Stop-AzureRmSqlElasticPoolActivity** cmdlet cancels the asynchronous update operation on an elastic pool.</span></span>

## <span data-ttu-id="56ed7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56ed7-107">EXAMPLES</span></span>

### <span data-ttu-id="56ed7-108">Esempio 1: annullare l'operazione di aggiornamento asincrono in un pool elastico</span><span class="sxs-lookup"><span data-stu-id="56ed7-108">Example 1: Cancel the asynchronous update operation on an elastic pool</span></span>
```
PS C:\> Stop-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -OperationId af97005d-9243-4f8a-844e-402d1cc855f5

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

<span data-ttu-id="56ed7-109">Questo comando Annulla l'operazione di aggiornamento asincrono sul pool elastico.</span><span class="sxs-lookup"><span data-stu-id="56ed7-109">This command cancels the asynchronous updates operation on the elastic pool.</span></span>

## <span data-ttu-id="56ed7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56ed7-110">PARAMETERS</span></span>

### <span data-ttu-id="56ed7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56ed7-111">-DefaultProfile</span></span>
<span data-ttu-id="56ed7-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56ed7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56ed7-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="56ed7-113">-ElasticPoolName</span></span>
<span data-ttu-id="56ed7-114">Il nome del pool di Azure SQL elastico.</span><span class="sxs-lookup"><span data-stu-id="56ed7-114">The name of the Azure SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="56ed7-115">-OperationId</span><span class="sxs-lookup"><span data-stu-id="56ed7-115">-OperationId</span></span>
<span data-ttu-id="56ed7-116">ID dell'operazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="56ed7-116">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="56ed7-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56ed7-117">-PassThru</span></span>
<span data-ttu-id="56ed7-118">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="56ed7-118">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="56ed7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56ed7-119">-ResourceGroupName</span></span>
<span data-ttu-id="56ed7-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="56ed7-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="56ed7-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="56ed7-121">-ServerName</span></span>
<span data-ttu-id="56ed7-122">Nome di Azure SQL Server in cui è presente il pool di elastici.</span><span class="sxs-lookup"><span data-stu-id="56ed7-122">The name of the Azure SQL Server the Elastic Pool is in.</span></span>

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

### <span data-ttu-id="56ed7-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="56ed7-123">-Confirm</span></span>
<span data-ttu-id="56ed7-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56ed7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56ed7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56ed7-125">-WhatIf</span></span>
<span data-ttu-id="56ed7-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56ed7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56ed7-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56ed7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56ed7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56ed7-128">CommonParameters</span></span>
<span data-ttu-id="56ed7-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56ed7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56ed7-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56ed7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56ed7-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56ed7-131">INPUTS</span></span>

### <span data-ttu-id="56ed7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="56ed7-132">System.String</span></span>

### <span data-ttu-id="56ed7-133">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="56ed7-133">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="56ed7-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56ed7-134">OUTPUTS</span></span>

### <span data-ttu-id="56ed7-135">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="56ed7-135">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="56ed7-136">Note</span><span class="sxs-lookup"><span data-stu-id="56ed7-136">NOTES</span></span>

## <span data-ttu-id="56ed7-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56ed7-137">RELATED LINKS</span></span>
