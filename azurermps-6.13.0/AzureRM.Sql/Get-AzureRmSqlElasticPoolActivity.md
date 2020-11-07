---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: f5e7455a253c86fe363b72c5d4c0e8ff47b96f56
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686888"
---
# <span data-ttu-id="440d7-101">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="440d7-101">Get-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="440d7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="440d7-102">SYNOPSIS</span></span>
<span data-ttu-id="440d7-103">Ottiene lo stato delle operazioni in un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="440d7-103">Gets the status of operations on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="440d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="440d7-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="440d7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="440d7-105">DESCRIPTION</span></span>
<span data-ttu-id="440d7-106">Il cmdlet **Get-AzureRmSqlElasticPoolActivity** ottiene lo stato delle operazioni in un pool elastico per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="440d7-106">The **Get-AzureRmSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="440d7-107">Puoi vedere lo stato della creazione del pool e degli aggiornamenti della configurazione.</span><span class="sxs-lookup"><span data-stu-id="440d7-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="440d7-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="440d7-108">EXAMPLES</span></span>

### <span data-ttu-id="440d7-109">Esempio 1: ottenere lo stato delle operazioni per un pool elastico</span><span class="sxs-lookup"><span data-stu-id="440d7-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="440d7-110">Questo comando consente di ottenere lo stato delle operazioni per il pool elastico denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="440d7-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="440d7-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="440d7-111">PARAMETERS</span></span>

### <span data-ttu-id="440d7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="440d7-112">-DefaultProfile</span></span>
<span data-ttu-id="440d7-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="440d7-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="440d7-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="440d7-114">-ElasticPoolName</span></span>
<span data-ttu-id="440d7-115">Specifica il nome di un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="440d7-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="440d7-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="440d7-116">-OperationId</span></span>
<span data-ttu-id="440d7-117">ID dell'operazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="440d7-117">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="440d7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="440d7-118">-ResourceGroupName</span></span>
<span data-ttu-id="440d7-119">Specifica il nome di un gruppo di risorse a cui è assegnato il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="440d7-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="440d7-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="440d7-120">-ServerName</span></span>
<span data-ttu-id="440d7-121">Specifica il nome di un server che contiene un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="440d7-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="440d7-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="440d7-122">-Confirm</span></span>
<span data-ttu-id="440d7-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="440d7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="440d7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="440d7-124">-WhatIf</span></span>
<span data-ttu-id="440d7-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="440d7-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="440d7-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="440d7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="440d7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="440d7-127">CommonParameters</span></span>
<span data-ttu-id="440d7-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="440d7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="440d7-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="440d7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="440d7-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="440d7-130">INPUTS</span></span>

### <span data-ttu-id="440d7-131">System. String</span><span class="sxs-lookup"><span data-stu-id="440d7-131">System.String</span></span>

### <span data-ttu-id="440d7-132">System. Nullable ' 1 [[System. Guid, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="440d7-132">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="440d7-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="440d7-133">OUTPUTS</span></span>

### <span data-ttu-id="440d7-134">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="440d7-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="440d7-135">Note</span><span class="sxs-lookup"><span data-stu-id="440d7-135">NOTES</span></span>

## <span data-ttu-id="440d7-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="440d7-136">RELATED LINKS</span></span>

[<span data-ttu-id="440d7-137">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="440d7-137">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="440d7-138">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="440d7-138">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="440d7-139">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="440d7-139">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="440d7-140">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="440d7-140">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="440d7-141">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="440d7-141">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


