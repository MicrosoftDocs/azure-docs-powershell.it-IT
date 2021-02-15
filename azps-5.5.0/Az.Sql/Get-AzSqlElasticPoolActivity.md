---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolActivity.md
ms.openlocfilehash: 2e0768b14337f4504df1e6cdf9565533584e0339
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188942"
---
# <span data-ttu-id="21beb-101">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="21beb-101">Get-AzSqlElasticPoolActivity</span></span>

## <span data-ttu-id="21beb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21beb-102">SYNOPSIS</span></span>
<span data-ttu-id="21beb-103">Ottiene lo stato delle operazioni in un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="21beb-103">Gets the status of operations on an elastic pool.</span></span>

## <span data-ttu-id="21beb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21beb-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String> [-OperationId <Guid>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="21beb-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="21beb-105">DESCRIPTION</span></span>
<span data-ttu-id="21beb-106">Il cmdlet **Get-AzSqlElasticPoolActivity** ottiene lo stato delle operazioni in un pool elastico per un database SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="21beb-106">The **Get-AzSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="21beb-107">È possibile visualizzare lo stato degli aggiornamenti di configurazione e creazione del pool.</span><span class="sxs-lookup"><span data-stu-id="21beb-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="21beb-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21beb-108">EXAMPLES</span></span>

### <span data-ttu-id="21beb-109">Esempio 1: Ottenere lo stato delle operazioni per un pool elastico</span><span class="sxs-lookup"><span data-stu-id="21beb-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="21beb-110">Questo comando ottiene lo stato delle operazioni per il pool elastico denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="21beb-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="21beb-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21beb-111">PARAMETERS</span></span>

### <span data-ttu-id="21beb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21beb-112">-DefaultProfile</span></span>
<span data-ttu-id="21beb-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="21beb-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21beb-114">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="21beb-114">-ElasticPoolName</span></span>
<span data-ttu-id="21beb-115">Specifica il nome di un pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="21beb-115">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="21beb-116">-OperationId</span><span class="sxs-lookup"><span data-stu-id="21beb-116">-OperationId</span></span>
<span data-ttu-id="21beb-117">ID dell'operazione da recuperare.</span><span class="sxs-lookup"><span data-stu-id="21beb-117">The ID of the operation to retrieve.</span></span>

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

### <span data-ttu-id="21beb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21beb-118">-ResourceGroupName</span></span>
<span data-ttu-id="21beb-119">Specifica il nome di un gruppo di risorse a cui è assegnato il pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="21beb-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="21beb-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="21beb-120">-ServerName</span></span>
<span data-ttu-id="21beb-121">Specifica il nome di un server che contiene un pool flessibile.</span><span class="sxs-lookup"><span data-stu-id="21beb-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="21beb-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21beb-122">-Confirm</span></span>
<span data-ttu-id="21beb-123">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21beb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21beb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21beb-124">-WhatIf</span></span>
<span data-ttu-id="21beb-125">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21beb-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21beb-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="21beb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21beb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21beb-127">CommonParameters</span></span>
<span data-ttu-id="21beb-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21beb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21beb-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="21beb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21beb-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="21beb-130">INPUTS</span></span>

### <span data-ttu-id="21beb-131">System.String</span><span class="sxs-lookup"><span data-stu-id="21beb-131">System.String</span></span>

### <span data-ttu-id="21beb-132">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="21beb-132">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="21beb-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21beb-133">OUTPUTS</span></span>

### <span data-ttu-id="21beb-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="21beb-134">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="21beb-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="21beb-135">NOTES</span></span>

## <span data-ttu-id="21beb-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21beb-136">RELATED LINKS</span></span>

[<span data-ttu-id="21beb-137">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="21beb-137">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="21beb-138">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="21beb-138">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="21beb-139">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="21beb-139">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="21beb-140">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="21beb-140">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="21beb-141">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="21beb-141">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


