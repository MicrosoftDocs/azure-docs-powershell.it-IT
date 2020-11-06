---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
ms.openlocfilehash: a6b5b21b8911aa8d156ced40476d1b0ecadad361
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512215"
---
# <span data-ttu-id="4f62b-101">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4f62b-101">Remove-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="4f62b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4f62b-102">SYNOPSIS</span></span>
<span data-ttu-id="4f62b-103">Elimina un pool di database elastici.</span><span class="sxs-lookup"><span data-stu-id="4f62b-103">Deletes an elastic database pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f62b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f62b-104">SYNTAX</span></span>

```
Remove-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4f62b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f62b-105">DESCRIPTION</span></span>
<span data-ttu-id="4f62b-106">Il cmdlet **Remove-AzureRmSqlElasticPool** Elimina un pool di dati di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="4f62b-106">The **Remove-AzureRmSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="4f62b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f62b-107">EXAMPLES</span></span>

### <span data-ttu-id="4f62b-108">Esempio 1: eliminare un pool elastico</span><span class="sxs-lookup"><span data-stu-id="4f62b-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="4f62b-109">Questo comando Elimina un pool elastico denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="4f62b-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="4f62b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4f62b-110">PARAMETERS</span></span>

### <span data-ttu-id="4f62b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f62b-111">-DefaultProfile</span></span>
<span data-ttu-id="4f62b-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4f62b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f62b-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="4f62b-113">-ElasticPoolName</span></span>
<span data-ttu-id="4f62b-114">Specifica il nome del pool elastico eliminato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f62b-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f62b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4f62b-115">-Force</span></span>
<span data-ttu-id="4f62b-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4f62b-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f62b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f62b-117">-ResourceGroupName</span></span>
<span data-ttu-id="4f62b-118">Specifica il nome del gruppo di risorse a cui è assegnato il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="4f62b-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="4f62b-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="4f62b-119">-ServerName</span></span>
<span data-ttu-id="4f62b-120">Specifica il nome del server che ospita il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="4f62b-120">Specifies the name of the server that hosts the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f62b-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4f62b-121">-Confirm</span></span>
<span data-ttu-id="4f62b-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f62b-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f62b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f62b-123">-WhatIf</span></span>
<span data-ttu-id="4f62b-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f62b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f62b-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f62b-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f62b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f62b-126">CommonParameters</span></span>
<span data-ttu-id="4f62b-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f62b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f62b-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f62b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f62b-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4f62b-129">INPUTS</span></span>

### <span data-ttu-id="4f62b-130">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="4f62b-130">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="4f62b-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f62b-131">OUTPUTS</span></span>

### <span data-ttu-id="4f62b-132">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="4f62b-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="4f62b-133">Note</span><span class="sxs-lookup"><span data-stu-id="4f62b-133">NOTES</span></span>

## <span data-ttu-id="4f62b-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f62b-134">RELATED LINKS</span></span>

[<span data-ttu-id="4f62b-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4f62b-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="4f62b-136">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="4f62b-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="4f62b-137">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="4f62b-137">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="4f62b-138">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4f62b-138">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="4f62b-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="4f62b-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="4f62b-140">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="4f62b-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


