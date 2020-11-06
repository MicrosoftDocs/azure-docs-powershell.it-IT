---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
ms.openlocfilehash: a9f86b9b316c14e40505932e0bf3b30fc66c55c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519671"
---
# <span data-ttu-id="c845f-101">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="c845f-101">Get-AzureRmSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="c845f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c845f-102">SYNOPSIS</span></span>
<span data-ttu-id="c845f-103">Ottiene i database elastici in un pool elastico e i relativi valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="c845f-103">Gets elastic databases in an elastic pool and their property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c845f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c845f-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c845f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c845f-105">DESCRIPTION</span></span>
<span data-ttu-id="c845f-106">Il cmdlet **Get-AzureRmSqlElasticPoolDatabase** ottiene i database elastici in un pool elastico e i relativi valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="c845f-106">The **Get-AzureRmSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="c845f-107">Puoi specificare il nome di un database elastico in Azure SQL database per visualizzare i valori delle proprietà solo per il database.</span><span class="sxs-lookup"><span data-stu-id="c845f-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="c845f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c845f-108">EXAMPLES</span></span>

### <span data-ttu-id="c845f-109">Esempio 1: ottenere tutti i database in un pool elastico</span><span class="sxs-lookup"><span data-stu-id="c845f-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="c845f-110">Questo comando consente di ottenere tutti i database in un pool elastico denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="c845f-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="c845f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c845f-111">PARAMETERS</span></span>

### <span data-ttu-id="c845f-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c845f-112">-DatabaseName</span></span>
<span data-ttu-id="c845f-113">Specifica il nome del database SQL ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c845f-113">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c845f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c845f-114">-DefaultProfile</span></span>
<span data-ttu-id="c845f-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c845f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c845f-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="c845f-116">-ElasticPoolName</span></span>
<span data-ttu-id="c845f-117">Specifica il nome di un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="c845f-117">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="c845f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c845f-118">-ResourceGroupName</span></span>
<span data-ttu-id="c845f-119">Specifica il nome di un gruppo di risorse a cui è assegnato il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="c845f-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="c845f-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="c845f-120">-ServerName</span></span>
<span data-ttu-id="c845f-121">Specifica il nome di un server che contiene un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="c845f-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="c845f-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c845f-122">-Confirm</span></span>
<span data-ttu-id="c845f-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c845f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c845f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c845f-124">-WhatIf</span></span>
<span data-ttu-id="c845f-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c845f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c845f-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c845f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c845f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c845f-127">CommonParameters</span></span>
<span data-ttu-id="c845f-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c845f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c845f-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c845f-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c845f-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c845f-130">INPUTS</span></span>

### <span data-ttu-id="c845f-131">System. String</span><span class="sxs-lookup"><span data-stu-id="c845f-131">System.String</span></span>

## <span data-ttu-id="c845f-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c845f-132">OUTPUTS</span></span>

### <span data-ttu-id="c845f-133">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="c845f-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="c845f-134">Note</span><span class="sxs-lookup"><span data-stu-id="c845f-134">NOTES</span></span>

## <span data-ttu-id="c845f-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c845f-135">RELATED LINKS</span></span>

[<span data-ttu-id="c845f-136">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c845f-136">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="c845f-137">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="c845f-137">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="c845f-138">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c845f-138">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="c845f-139">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c845f-139">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="c845f-140">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="c845f-140">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

