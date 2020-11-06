---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
ms.openlocfilehash: 57f5f656f3c85e9d1c0d29c07a602a303208e7f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518288"
---
# <span data-ttu-id="56107-101">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="56107-101">Remove-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="56107-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56107-102">SYNOPSIS</span></span>
<span data-ttu-id="56107-103">Elimina un pool di database elastici.</span><span class="sxs-lookup"><span data-stu-id="56107-103">Deletes an elastic database pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56107-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56107-104">SYNTAX</span></span>

```
Remove-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="56107-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56107-105">DESCRIPTION</span></span>
<span data-ttu-id="56107-106">Il cmdlet **Remove-AzureRmSqlElasticPool** Elimina un pool di dati di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="56107-106">The **Remove-AzureRmSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="56107-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56107-107">EXAMPLES</span></span>

### <span data-ttu-id="56107-108">Esempio 1: eliminare un pool elastico</span><span class="sxs-lookup"><span data-stu-id="56107-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="56107-109">Questo comando Elimina un pool elastico denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="56107-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="56107-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56107-110">PARAMETERS</span></span>

### <span data-ttu-id="56107-111">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="56107-111">-ElasticPoolName</span></span>
<span data-ttu-id="56107-112">Specifica il nome del pool elastico eliminato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56107-112">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="56107-113">-Force</span><span class="sxs-lookup"><span data-stu-id="56107-113">-Force</span></span>
<span data-ttu-id="56107-114">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="56107-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="56107-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56107-115">-ResourceGroupName</span></span>
<span data-ttu-id="56107-116">Specifica il nome del gruppo di risorse a cui è assegnato il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="56107-116">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="56107-117">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="56107-117">-ServerName</span></span>
<span data-ttu-id="56107-118">Specifica il nome del server che ospita il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="56107-118">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="56107-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="56107-119">-Confirm</span></span>
<span data-ttu-id="56107-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56107-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56107-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56107-121">-WhatIf</span></span>
<span data-ttu-id="56107-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56107-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56107-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56107-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56107-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56107-124">-DefaultProfile</span></span>
<span data-ttu-id="56107-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56107-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56107-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56107-126">CommonParameters</span></span>
<span data-ttu-id="56107-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56107-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56107-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56107-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56107-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56107-129">INPUTS</span></span>

### <span data-ttu-id="56107-130">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="56107-130">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="56107-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56107-131">OUTPUTS</span></span>

### <span data-ttu-id="56107-132">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="56107-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="56107-133">Note</span><span class="sxs-lookup"><span data-stu-id="56107-133">NOTES</span></span>

## <span data-ttu-id="56107-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56107-134">RELATED LINKS</span></span>

[<span data-ttu-id="56107-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="56107-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="56107-136">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="56107-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="56107-137">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="56107-137">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="56107-138">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="56107-138">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="56107-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="56107-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="56107-140">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="56107-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


