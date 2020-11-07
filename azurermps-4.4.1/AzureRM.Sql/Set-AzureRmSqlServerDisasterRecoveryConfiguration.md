---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 44F8EFF4-8E3D-4657-9D17-2A3F49CEA515
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 196608c24e31daad500fbf9b8aae1945550bb3f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688501"
---
# <span data-ttu-id="55850-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="55850-101">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="55850-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="55850-102">SYNOPSIS</span></span>
<span data-ttu-id="55850-103">Modifica una configurazione di ripristino del server di database.</span><span class="sxs-lookup"><span data-stu-id="55850-103">Modifies a database server recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55850-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55850-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> [-Failover] [-AllowDataLoss]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55850-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55850-105">DESCRIPTION</span></span>
<span data-ttu-id="55850-106">Il cmdlet **set-AzureRmSqlServerDisasterRecoveryConfiguration** modifica una configurazione di ripristino di database di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="55850-106">The **Set-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet modifies a SQL database server recovery configuration.</span></span>

## <span data-ttu-id="55850-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55850-107">EXAMPLES</span></span>

## <span data-ttu-id="55850-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="55850-108">PARAMETERS</span></span>

### <span data-ttu-id="55850-109">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="55850-109">-AllowDataLoss</span></span>
<span data-ttu-id="55850-110">Indica che l'operazione di failover consente la perdita di dati.</span><span class="sxs-lookup"><span data-stu-id="55850-110">Indicates that the failover operation permits data loss.</span></span>

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

### <span data-ttu-id="55850-111">-Failover</span><span class="sxs-lookup"><span data-stu-id="55850-111">-Failover</span></span>
<span data-ttu-id="55850-112">Indica che questa operazione è un failover.</span><span class="sxs-lookup"><span data-stu-id="55850-112">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55850-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55850-113">-ResourceGroupName</span></span>
<span data-ttu-id="55850-114">Specifica il nome di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="55850-114">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="55850-115">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="55850-115">-ServerName</span></span>
<span data-ttu-id="55850-116">Specifica il nome di un server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="55850-116">Specifies the name of a SQL database server.</span></span>

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

### <span data-ttu-id="55850-117">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="55850-117">-VirtualEndpointName</span></span>
<span data-ttu-id="55850-118">Specifica il nome di un punto finale virtuale.</span><span class="sxs-lookup"><span data-stu-id="55850-118">Specifies the name of a virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55850-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="55850-119">-Confirm</span></span>
<span data-ttu-id="55850-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55850-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55850-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55850-121">-WhatIf</span></span>
<span data-ttu-id="55850-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="55850-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55850-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="55850-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55850-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55850-124">-DefaultProfile</span></span>
<span data-ttu-id="55850-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="55850-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="55850-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55850-126">CommonParameters</span></span>
<span data-ttu-id="55850-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55850-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55850-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55850-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55850-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="55850-129">INPUTS</span></span>

## <span data-ttu-id="55850-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55850-130">OUTPUTS</span></span>

## <span data-ttu-id="55850-131">Note</span><span class="sxs-lookup"><span data-stu-id="55850-131">NOTES</span></span>

## <span data-ttu-id="55850-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55850-132">RELATED LINKS</span></span>

[<span data-ttu-id="55850-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="55850-133">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="55850-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="55850-134">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="55850-135">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="55850-135">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="55850-136">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="55850-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
