---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 588954527c76bb0f5394afe4df9e19b37c10fe0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509595"
---
# <span data-ttu-id="85038-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="85038-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="85038-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85038-102">SYNOPSIS</span></span>
<span data-ttu-id="85038-103">Modifica una configurazione di ripristino del server di database.</span><span class="sxs-lookup"><span data-stu-id="85038-103">Modifies a database server recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85038-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85038-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85038-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85038-105">DESCRIPTION</span></span>
<span data-ttu-id="85038-106">Il cmdlet **set-AzureRmSqlServerDisasterRecoveryConfiguration** modifica una configurazione di ripristino di database di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="85038-106">The **Set-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="85038-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85038-107">EXAMPLES</span></span>

## <span data-ttu-id="85038-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85038-108">PARAMETERS</span></span>

### <span data-ttu-id="85038-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="85038-109">-AllowDataLoss</span></span>
<span data-ttu-id="85038-110">Indica che l'operazione di failover consente la perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="85038-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="85038-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85038-111">-AsJob</span></span>
<span data-ttu-id="85038-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="85038-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85038-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85038-113">-DefaultProfile</span></span>
<span data-ttu-id="85038-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="85038-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85038-115">-Failover</span><span class="sxs-lookup"><span data-stu-id="85038-115">-Failover</span></span>
<span data-ttu-id="85038-116">Indica che questa operazione è un failover.</span><span class="sxs-lookup"><span data-stu-id="85038-116">Indicates that this operation is a failover.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85038-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85038-117">-ResourceGroupName</span></span>
<span data-ttu-id="85038-118">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="85038-118">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="85038-119">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="85038-119">-ServerName</span></span>
<span data-ttu-id="85038-120">Specifica il nome di un server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="85038-120">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="85038-121">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="85038-121">-VirtualEndpointName</span></span>
<span data-ttu-id="85038-122">Specifica il nome di un punto finale virtuale.</span><span class="sxs-lookup"><span data-stu-id="85038-122">Specifies the name of a virtual end point.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85038-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="85038-123">-Confirm</span></span>
<span data-ttu-id="85038-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85038-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85038-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85038-125">-WhatIf</span></span>
<span data-ttu-id="85038-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85038-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85038-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="85038-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85038-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85038-128">CommonParameters</span></span>
<span data-ttu-id="85038-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85038-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85038-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85038-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85038-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85038-131">INPUTS</span></span>

### <span data-ttu-id="85038-132">Nessuno</span><span class="sxs-lookup"><span data-stu-id="85038-132">None</span></span>
<span data-ttu-id="85038-133">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="85038-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="85038-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85038-134">OUTPUTS</span></span>

## <span data-ttu-id="85038-135">Note</span><span class="sxs-lookup"><span data-stu-id="85038-135">NOTES</span></span>

## <span data-ttu-id="85038-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85038-136">RELATED LINKS</span></span>

[<span data-ttu-id="85038-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="85038-137">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="85038-138">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="85038-138">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="85038-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="85038-139">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="85038-140">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="85038-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
