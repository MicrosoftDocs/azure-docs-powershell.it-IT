---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0DB0B08A-F948-4F6E-9CF0-2FB5DD5064D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPoolActivity.md
ms.openlocfilehash: d78b2fafb6c633c8a0276193e9e42677de814ff3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685859"
---
# <span data-ttu-id="dafe9-101">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="dafe9-101">Get-AzureRmSqlElasticPoolActivity</span></span>

## <span data-ttu-id="dafe9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dafe9-102">SYNOPSIS</span></span>
<span data-ttu-id="dafe9-103">Ottiene lo stato delle operazioni in un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="dafe9-103">Gets the status of operations on an elastic pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dafe9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dafe9-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPoolActivity [-ServerName] <String> [-ElasticPoolName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dafe9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dafe9-105">DESCRIPTION</span></span>
<span data-ttu-id="dafe9-106">Il cmdlet **Get-AzureRmSqlElasticPoolActivity** ottiene lo stato delle operazioni in un pool elastico per un database SQL di Azure.</span><span class="sxs-lookup"><span data-stu-id="dafe9-106">The **Get-AzureRmSqlElasticPoolActivity** cmdlet gets the status of operations on an elastic pool for an Azure SQL Database.</span></span>
<span data-ttu-id="dafe9-107">Puoi vedere lo stato della creazione del pool e degli aggiornamenti della configurazione.</span><span class="sxs-lookup"><span data-stu-id="dafe9-107">You can see the status of both pool creation and configuration updates.</span></span>

## <span data-ttu-id="dafe9-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dafe9-108">EXAMPLES</span></span>

### <span data-ttu-id="dafe9-109">Esempio 1: ottenere lo stato delle operazioni per un pool elastico</span><span class="sxs-lookup"><span data-stu-id="dafe9-109">Example 1: Get the status of operations for an elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPoolActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="dafe9-110">Questo comando consente di ottenere lo stato delle operazioni per il pool elastico denominato ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="dafe9-110">This command gets the status of the operations for the elastic pool named ElasticPool01.</span></span>

## <span data-ttu-id="dafe9-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dafe9-111">PARAMETERS</span></span>

### <span data-ttu-id="dafe9-112">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="dafe9-112">-ElasticPoolName</span></span>
<span data-ttu-id="dafe9-113">Specifica il nome di un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="dafe9-113">Specifies the name of an elastic pool.</span></span>

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

### <span data-ttu-id="dafe9-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dafe9-114">-ResourceGroupName</span></span>
<span data-ttu-id="dafe9-115">Specifica il nome di un gruppo di risorse a cui è assegnato il pool elastico.</span><span class="sxs-lookup"><span data-stu-id="dafe9-115">Specifies the name of a resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="dafe9-116">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="dafe9-116">-ServerName</span></span>
<span data-ttu-id="dafe9-117">Specifica il nome di un server che contiene un pool elastico.</span><span class="sxs-lookup"><span data-stu-id="dafe9-117">Specifies the name of a server that contains an elastic pool.</span></span>

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

### <span data-ttu-id="dafe9-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="dafe9-118">-Confirm</span></span>
<span data-ttu-id="dafe9-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dafe9-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dafe9-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dafe9-120">-WhatIf</span></span>
<span data-ttu-id="dafe9-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dafe9-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dafe9-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dafe9-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dafe9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dafe9-123">-DefaultProfile</span></span>
<span data-ttu-id="dafe9-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dafe9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dafe9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dafe9-125">CommonParameters</span></span>
<span data-ttu-id="dafe9-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dafe9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dafe9-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dafe9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dafe9-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dafe9-128">INPUTS</span></span>

## <span data-ttu-id="dafe9-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dafe9-129">OUTPUTS</span></span>

### <span data-ttu-id="dafe9-130">Microsoft. Azure. Commands. SQL. ElasticPool. Model. AzureSqlElasticPoolActivityModel</span><span class="sxs-lookup"><span data-stu-id="dafe9-130">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolActivityModel</span></span>

## <span data-ttu-id="dafe9-131">Note</span><span class="sxs-lookup"><span data-stu-id="dafe9-131">NOTES</span></span>

## <span data-ttu-id="dafe9-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dafe9-132">RELATED LINKS</span></span>

[<span data-ttu-id="dafe9-133">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="dafe9-133">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="dafe9-134">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="dafe9-134">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="dafe9-135">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="dafe9-135">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="dafe9-136">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="dafe9-136">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="dafe9-137">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="dafe9-137">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)


