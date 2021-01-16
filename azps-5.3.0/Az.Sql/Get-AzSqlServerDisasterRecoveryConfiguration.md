---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: C7F3E754-394A-4F93-A621-A07AF281EE45
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: b4cbf71dc4b9a04a3070bab22266ba28f88b2131
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476660"
---
# <span data-ttu-id="3cb18-101">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="3cb18-101">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="3cb18-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3cb18-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb18-103">Ottiene una configurazione di ripristino di sistema del server di database.</span><span class="sxs-lookup"><span data-stu-id="3cb18-103">Gets a database server system recovery configuration.</span></span>

## <span data-ttu-id="3cb18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3cb18-104">SYNTAX</span></span>

```
Get-AzSqlServerDisasterRecoveryConfiguration [-VirtualEndpointName <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3cb18-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3cb18-105">DESCRIPTION</span></span>
<span data-ttu-id="3cb18-106">Il cmdlet **Get-AzSqlServerDisasterRecoveryConfiguration** ottiene una configurazione di ripristino del sistema di database di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3cb18-106">The **Get-AzSqlServerDisasterRecoveryConfiguration** cmdlet gets a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="3cb18-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3cb18-107">EXAMPLES</span></span>

## <span data-ttu-id="3cb18-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3cb18-108">PARAMETERS</span></span>

### <span data-ttu-id="3cb18-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cb18-109">-DefaultProfile</span></span>
<span data-ttu-id="3cb18-110">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="3cb18-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cb18-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cb18-111">-ResourceGroupName</span></span>
<span data-ttu-id="3cb18-112">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3cb18-112">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3cb18-113">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="3cb18-113">-ServerName</span></span>
<span data-ttu-id="3cb18-114">Specifica il nome del server di database SQL.</span><span class="sxs-lookup"><span data-stu-id="3cb18-114">Specifies the name of SQL database server.</span></span>

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

### <span data-ttu-id="3cb18-115">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="3cb18-115">-VirtualEndpointName</span></span>
<span data-ttu-id="3cb18-116">Specifica il nome del punto finale virtuale.</span><span class="sxs-lookup"><span data-stu-id="3cb18-116">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="3cb18-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3cb18-117">-Confirm</span></span>
<span data-ttu-id="3cb18-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cb18-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cb18-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cb18-119">-WhatIf</span></span>
<span data-ttu-id="3cb18-120">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3cb18-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cb18-121">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3cb18-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cb18-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb18-122">CommonParameters</span></span>
<span data-ttu-id="3cb18-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cb18-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb18-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3cb18-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb18-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3cb18-125">INPUTS</span></span>

### <span data-ttu-id="3cb18-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3cb18-126">System.String</span></span>

## <span data-ttu-id="3cb18-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3cb18-127">OUTPUTS</span></span>

### <span data-ttu-id="3cb18-128">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="3cb18-128">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="3cb18-129">Note</span><span class="sxs-lookup"><span data-stu-id="3cb18-129">NOTES</span></span>

## <span data-ttu-id="3cb18-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3cb18-130">RELATED LINKS</span></span>

[<span data-ttu-id="3cb18-131">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="3cb18-131">New-AzSqlServerDisasterRecoveryConfiguration</span></span>](./New-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="3cb18-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="3cb18-132">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="3cb18-133">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="3cb18-133">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="3cb18-134">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="3cb18-134">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

