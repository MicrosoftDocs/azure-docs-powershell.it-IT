---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticPool.md
ms.openlocfilehash: d751954a5c66d9220513017aa62b6797f8f1ea6f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191864"
---
# <span data-ttu-id="9083c-101">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="9083c-101">Remove-AzSqlElasticPool</span></span>

## <span data-ttu-id="9083c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9083c-102">SYNOPSIS</span></span>
<span data-ttu-id="9083c-103">Elimina un pool di database elastici.</span><span class="sxs-lookup"><span data-stu-id="9083c-103">Deletes an elastic database pool.</span></span>

## <span data-ttu-id="9083c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9083c-104">SYNTAX</span></span>

```
Remove-AzSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9083c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9083c-105">DESCRIPTION</span></span>
<span data-ttu-id="9083c-106">Il cmdlet **Remove-AzSqlElasticPool** Elimina un pool di dati di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="9083c-106">The **Remove-AzSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="9083c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9083c-107">EXAMPLES</span></span>

### <span data-ttu-id="9083c-108">Esempio 1: eliminare un pool elastico</span><span class="sxs-lookup"><span data-stu-id="9083c-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="9083c-109">Questo comando Elimina un pool elastico denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="9083c-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="9083c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9083c-110">PARAMETERS</span></span>

### <span data-ttu-id="9083c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9083c-111">-DefaultProfile</span></span>
<span data-ttu-id="9083c-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9083c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9083c-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="9083c-113">-ElasticPoolName</span></span>
<span data-ttu-id="9083c-114">Specifica il nome del pool elastico eliminato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9083c-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9083c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9083c-115">-Force</span></span>
<span data-ttu-id="9083c-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="9083c-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9083c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9083c-117">-ResourceGroupName</span></span>
<span data-ttu-id="9083c-118">Specifica il nome del gruppo di risorse a cui è assegnato il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="9083c-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="9083c-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="9083c-119">-ServerName</span></span>
<span data-ttu-id="9083c-120">Specifica il nome del server che ospita il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="9083c-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="9083c-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9083c-121">-Confirm</span></span>
<span data-ttu-id="9083c-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9083c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9083c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9083c-123">-WhatIf</span></span>
<span data-ttu-id="9083c-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9083c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9083c-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9083c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9083c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9083c-126">CommonParameters</span></span>
<span data-ttu-id="9083c-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9083c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9083c-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9083c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9083c-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9083c-129">INPUTS</span></span>

### <span data-ttu-id="9083c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9083c-130">System.String</span></span>

## <span data-ttu-id="9083c-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9083c-131">OUTPUTS</span></span>

### <span data-ttu-id="9083c-132">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="9083c-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="9083c-133">Note</span><span class="sxs-lookup"><span data-stu-id="9083c-133">NOTES</span></span>

## <span data-ttu-id="9083c-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9083c-134">RELATED LINKS</span></span>

[<span data-ttu-id="9083c-135">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="9083c-135">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="9083c-136">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="9083c-136">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="9083c-137">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="9083c-137">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="9083c-138">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="9083c-138">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="9083c-139">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="9083c-139">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="9083c-140">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="9083c-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

