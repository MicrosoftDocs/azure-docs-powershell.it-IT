---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: bbb6841f615444175de93e59d4536a07461490de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687068"
---
# <span data-ttu-id="bb1a3-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb1a3-101">Get-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="bb1a3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bb1a3-102">SYNOPSIS</span></span>
<span data-ttu-id="bb1a3-103">Ottiene una configurazione di ripristino di sistema del server di database.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-103">Gets a database server system recovery configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb1a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb1a3-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bb1a3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb1a3-105">DESCRIPTION</span></span>
<span data-ttu-id="bb1a3-106">Il cmdlet **Get-AzureRmSqlServerDisasterRecoveryConfiguration** ottiene una configurazione di ripristino del sistema di database di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-106">The **Get-AzureRmSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="bb1a3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb1a3-107">EXAMPLES</span></span>

## <span data-ttu-id="bb1a3-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bb1a3-108">PARAMETERS</span></span>

### <span data-ttu-id="bb1a3-109">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb1a3-109">-ResourceGroupName</span></span>
<span data-ttu-id="bb1a3-110">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-110">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="bb1a3-111">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="bb1a3-111">-ServerName</span></span>
<span data-ttu-id="bb1a3-112">Specifica il nome del server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-112">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="bb1a3-113">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="bb1a3-113">-VirtualEndpointName</span></span>
<span data-ttu-id="bb1a3-114">Specifica il nome del punto finale virtuale.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-114">Specifies the name of the virtual end point.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb1a3-115">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bb1a3-115">-Confirm</span></span>
<span data-ttu-id="bb1a3-116">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb1a3-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb1a3-117">-WhatIf</span></span>
<span data-ttu-id="bb1a3-118">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb1a3-119">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb1a3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb1a3-120">-DefaultProfile</span></span>
<span data-ttu-id="bb1a3-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb1a3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb1a3-122">CommonParameters</span></span>
<span data-ttu-id="bb1a3-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb1a3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb1a3-124">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb1a3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb1a3-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bb1a3-125">INPUTS</span></span>

## <span data-ttu-id="bb1a3-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb1a3-126">OUTPUTS</span></span>

## <span data-ttu-id="bb1a3-127">Note</span><span class="sxs-lookup"><span data-stu-id="bb1a3-127">NOTES</span></span>

## <span data-ttu-id="bb1a3-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb1a3-128">RELATED LINKS</span></span>

[<span data-ttu-id="bb1a3-129">New-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb1a3-129">New-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="bb1a3-130">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb1a3-130">Remove-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="bb1a3-131">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="bb1a3-131">Set-AzureRmSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzureRmSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="bb1a3-132">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="bb1a3-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

