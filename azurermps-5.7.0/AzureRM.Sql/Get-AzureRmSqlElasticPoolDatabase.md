---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14620FBD-4B10-4366-94F7-891BC01B893F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpooldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolDatabase.md
ms.openlocfilehash: 3068b3a406414eb7302d76d5d053658dcf0e6245
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686293"
---
# <span data-ttu-id="5faed-101">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="5faed-101">Get-AzureRmSqlElasticPoolDatabase</span></span>

## <span data-ttu-id="5faed-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5faed-102">SYNOPSIS</span></span>
<span data-ttu-id="5faed-103">Ottiene i database elastici in un pool elastico e i relativi valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="5faed-103">Gets elastic databases in an elastic pool and their property values.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5faed-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5faed-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolDatabase [-ElasticPoolName] <String> [-DatabaseName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5faed-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5faed-105">DESCRIPTION</span></span>
<span data-ttu-id="5faed-106">Il cmdlet **Get-AzureRmSqlElasticPoolDatabase** ottiene i database elastici in un pool elastico e i relativi valori di proprietà.</span><span class="sxs-lookup"><span data-stu-id="5faed-106">The **Get-AzureRmSqlElasticPoolDatabase** cmdlet gets elastic databases in an elastic pool and their property values.</span></span>
<span data-ttu-id="5faed-107">Puoi specificare il nome di un database elastico in Azure SQL database per visualizzare i valori delle proprietà solo per il database.</span><span class="sxs-lookup"><span data-stu-id="5faed-107">You can specify the name of an elastic database in Azure SQL Database to see the property values for only that database.</span></span>

## <span data-ttu-id="5faed-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5faed-108">EXAMPLES</span></span>

### <span data-ttu-id="5faed-109">Esempio 1: ottenere tutti i database in un pool elastico</span><span class="sxs-lookup"><span data-stu-id="5faed-109">Example 1: Get all databases in an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="5faed-110">Questo comando consente di ottenere tutti i database in un pool elastico denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="5faed-110">This command gets all databases in an elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="5faed-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5faed-111">PARAMETERS</span></span>

### <span data-ttu-id="5faed-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5faed-112">-DatabaseName</span></span>
<span data-ttu-id="5faed-113">Specifica il nome del database SQL ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5faed-113">Specifies the name of the SQL Database that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5faed-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5faed-114">-DefaultProfile</span></span>
<span data-ttu-id="5faed-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5faed-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5faed-116">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="5faed-116">-ElasticPoolName</span></span>
<span data-ttu-id="5faed-117">Specifica il nome di un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="5faed-117">Specifies the name of an elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5faed-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5faed-118">-ResourceGroupName</span></span>
<span data-ttu-id="5faed-119">Specifica il nome di un gruppo di risorse a cui è assegnato il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="5faed-119">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="5faed-120">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="5faed-120">-ServerName</span></span>
<span data-ttu-id="5faed-121">Specifica il nome di un server che contiene un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="5faed-121">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="5faed-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5faed-122">-Confirm</span></span>
<span data-ttu-id="5faed-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5faed-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5faed-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5faed-124">-WhatIf</span></span>
<span data-ttu-id="5faed-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5faed-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5faed-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5faed-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5faed-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5faed-127">CommonParameters</span></span>
<span data-ttu-id="5faed-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5faed-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5faed-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5faed-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5faed-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5faed-130">INPUTS</span></span>

### <span data-ttu-id="5faed-131">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5faed-131">None</span></span>
<span data-ttu-id="5faed-132">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="5faed-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5faed-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5faed-133">OUTPUTS</span></span>

### <span data-ttu-id="5faed-134">Microsoft. Azure. Commands. SQL. database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5faed-134">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="5faed-135">Note</span><span class="sxs-lookup"><span data-stu-id="5faed-135">NOTES</span></span>

## <span data-ttu-id="5faed-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5faed-136">RELATED LINKS</span></span>

[<span data-ttu-id="5faed-137">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5faed-137">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="5faed-138">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="5faed-138">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="5faed-139">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5faed-139">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="5faed-140">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5faed-140">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="5faed-141">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="5faed-141">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

