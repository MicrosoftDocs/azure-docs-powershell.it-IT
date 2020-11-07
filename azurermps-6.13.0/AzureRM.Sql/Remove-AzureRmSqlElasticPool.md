---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 47E8E8C1-A63D-4243-A004-ABD5CA1A559E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlElasticPool.md
ms.openlocfilehash: 3786dc0a9500dd07b332dacfbb026b5a44f0b550
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687252"
---
# <span data-ttu-id="45e35-101">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="45e35-101">Remove-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="45e35-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="45e35-102">SYNOPSIS</span></span>
<span data-ttu-id="45e35-103">Elimina un pool di database elastici.</span><span class="sxs-lookup"><span data-stu-id="45e35-103">Deletes an elastic database pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45e35-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45e35-104">SYNTAX</span></span>

```
Remove-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45e35-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45e35-105">DESCRIPTION</span></span>
<span data-ttu-id="45e35-106">Il cmdlet **Remove-AzureRmSqlElasticPool** Elimina un pool di dati di Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="45e35-106">The **Remove-AzureRmSqlElasticPool** cmdlet deletes an Azure SQL Database elastic pool.</span></span>

## <span data-ttu-id="45e35-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45e35-107">EXAMPLES</span></span>

### <span data-ttu-id="45e35-108">Esempio 1: eliminare un pool elastico</span><span class="sxs-lookup"><span data-stu-id="45e35-108">Example 1: Delete an elastic pool</span></span>
```
PS C:\>Remove-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="45e35-109">Questo comando Elimina un pool elastico denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="45e35-109">This command deletes an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="45e35-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="45e35-110">PARAMETERS</span></span>

### <span data-ttu-id="45e35-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45e35-111">-DefaultProfile</span></span>
<span data-ttu-id="45e35-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="45e35-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="45e35-113">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="45e35-113">-ElasticPoolName</span></span>
<span data-ttu-id="45e35-114">Specifica il nome del pool elastico eliminato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45e35-114">Specifies the name of the elastic pool that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="45e35-115">-Force</span><span class="sxs-lookup"><span data-stu-id="45e35-115">-Force</span></span>
<span data-ttu-id="45e35-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="45e35-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="45e35-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45e35-117">-ResourceGroupName</span></span>
<span data-ttu-id="45e35-118">Specifica il nome del gruppo di risorse a cui è assegnato il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="45e35-118">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="45e35-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="45e35-119">-ServerName</span></span>
<span data-ttu-id="45e35-120">Specifica il nome del server che ospita il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="45e35-120">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="45e35-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="45e35-121">-Confirm</span></span>
<span data-ttu-id="45e35-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45e35-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45e35-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45e35-123">-WhatIf</span></span>
<span data-ttu-id="45e35-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45e35-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45e35-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45e35-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45e35-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45e35-126">CommonParameters</span></span>
<span data-ttu-id="45e35-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45e35-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45e35-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45e35-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45e35-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="45e35-129">INPUTS</span></span>

### <span data-ttu-id="45e35-130">System. String</span><span class="sxs-lookup"><span data-stu-id="45e35-130">System.String</span></span>

## <span data-ttu-id="45e35-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45e35-131">OUTPUTS</span></span>

### <span data-ttu-id="45e35-132">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="45e35-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="45e35-133">Note</span><span class="sxs-lookup"><span data-stu-id="45e35-133">NOTES</span></span>

## <span data-ttu-id="45e35-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45e35-134">RELATED LINKS</span></span>

[<span data-ttu-id="45e35-135">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="45e35-135">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="45e35-136">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="45e35-136">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="45e35-137">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="45e35-137">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="45e35-138">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="45e35-138">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="45e35-139">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="45e35-139">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="45e35-140">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="45e35-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


