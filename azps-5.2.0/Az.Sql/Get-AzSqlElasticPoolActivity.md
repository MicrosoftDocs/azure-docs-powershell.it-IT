---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 2e0768b14337f4504df1e6cdf9565533584e0339
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360678"
---
# <span data-ttu-id="eab5c-101">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="eab5c-101">Get-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="eab5c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="eab5c-102">SYNOPSIS</span></span>
<span data-ttu-id="eab5c-103">Ottiene lo stato delle operazioni in un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="eab5c-103">Gets the status of operations on an elastic pool.</span></span>

## <span data-ttu-id="eab5c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="eab5c-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eab5c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eab5c-105">DESCRIPTION</span></span>
<span data-ttu-id="eab5c-106">Il cmdlet **Get-AzSqlElasticPoolActivity** ottiene lo stato delle operazioni in un pool elastico per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="eab5c-106">The **Get-AzSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="eab5c-107">Puoi vedere lo stato della creazione del pool e degli aggiornamenti della configurazione.</span><span class="sxs-lookup"><span data-stu-id="eab5c-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="eab5c-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="eab5c-108">EXAMPLES</span></span>

### <span data-ttu-id="eab5c-109">Esempio 1: ottenere lo stato delle operazioni per un pool elastico</span><span class="sxs-lookup"><span data-stu-id="eab5c-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="eab5c-110">Questo comando consente di ottenere lo stato delle operazioni per il pool elastico denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="eab5c-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="eab5c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="eab5c-111">PARAMETERS</span></span>

### <span data-ttu-id="eab5c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eab5c-112">-DefaultProfile</span></span>
<span data-ttu-id="eab5c-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="eab5c-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eab5c-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="eab5c-114">-ElasticPoolName</span></span>
<span data-ttu-id="eab5c-115">Specifica il nome di un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="eab5c-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="eab5c-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="eab5c-116">-OperationId</span></span>
<span data-ttu-id="eab5c-117">ID dell'operazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="eab5c-117">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="eab5c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eab5c-118">-ResourceGroupName</span></span>
<span data-ttu-id="eab5c-119">Specifica il nome di un gruppo di risorse a cui è assegnato il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="eab5c-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="eab5c-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="eab5c-120">-ServerName</span></span>
<span data-ttu-id="eab5c-121">Specifica il nome di un server che contiene un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="eab5c-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="eab5c-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="eab5c-122">-Confirm</span></span>
<span data-ttu-id="eab5c-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eab5c-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eab5c-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eab5c-124">-WhatIf</span></span>
<span data-ttu-id="eab5c-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eab5c-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eab5c-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="eab5c-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eab5c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eab5c-127">CommonParameters</span></span>
<span data-ttu-id="eab5c-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eab5c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eab5c-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="eab5c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eab5c-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="eab5c-130">INPUTS</span></span>

### <span data-ttu-id="eab5c-131">System. String</span><span class="sxs-lookup"><span data-stu-id="eab5c-131">System.String</span></span>

### <span data-ttu-id="eab5c-132">System. Nullable ' 1 [[System. Guid, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="eab5c-132">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="eab5c-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="eab5c-133">OUTPUTS</span></span>

### <span data-ttu-id="eab5c-134">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="eab5c-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="eab5c-135">Note</span><span class="sxs-lookup"><span data-stu-id="eab5c-135">NOTES</span></span>

## <span data-ttu-id="eab5c-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="eab5c-136">RELATED LINKS</span></span>

[<span data-ttu-id="eab5c-137">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="eab5c-137">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="eab5c-138">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="eab5c-138">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="eab5c-139">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="eab5c-139">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="eab5c-140">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="eab5c-140">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="eab5c-141">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="eab5c-141">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


