---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: 8f1400ba07444a5fc14d2a3194edd9fe960aaccc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856834"
---
# <span data-ttu-id="15af9-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="15af9-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="15af9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="15af9-102">SYNOPSIS</span></span>
<span data-ttu-id="15af9-103">Crea una configurazione di ripristino di sistema del server di database.</span><span class="sxs-lookup"><span data-stu-id="15af9-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="15af9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15af9-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15af9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15af9-105">DESCRIPTION</span></span>
<span data-ttu-id="15af9-106">Il cmdlet **New-AzSqlServerDisasterRecoveryConfiguration** crea una configurazione di ripristino di sistema di database di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="15af9-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="15af9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15af9-107">EXAMPLES</span></span>

## <span data-ttu-id="15af9-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="15af9-108">PARAMETERS</span></span>

### <span data-ttu-id="15af9-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15af9-109">-AsJob</span></span>
<span data-ttu-id="15af9-110">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="15af9-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="15af9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15af9-111">-DefaultProfile</span></span>
<span data-ttu-id="15af9-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="15af9-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15af9-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="15af9-113">-FailoverPolicy</span></span>
<span data-ttu-id="15af9-114">Specifica i criteri di failover.</span><span class="sxs-lookup"><span data-stu-id="15af9-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="15af9-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15af9-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="15af9-116">Specifica il nome del gruppo di risorse partner.</span><span class="sxs-lookup"><span data-stu-id="15af9-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="15af9-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="15af9-117">-PartnerServerName</span></span>
<span data-ttu-id="15af9-118">Specifica il nome del server partner.</span><span class="sxs-lookup"><span data-stu-id="15af9-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="15af9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15af9-119">-ResourceGroupName</span></span>
<span data-ttu-id="15af9-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="15af9-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="15af9-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="15af9-121">-ServerName</span></span>
<span data-ttu-id="15af9-122">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="15af9-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="15af9-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="15af9-123">-VirtualEndpointName</span></span>
<span data-ttu-id="15af9-124">Specifica il nome del punto finale virtuale.</span><span class="sxs-lookup"><span data-stu-id="15af9-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="15af9-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="15af9-125">-Confirm</span></span>
<span data-ttu-id="15af9-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15af9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15af9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15af9-127">-WhatIf</span></span>
<span data-ttu-id="15af9-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15af9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15af9-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="15af9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15af9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15af9-130">CommonParameters</span></span>
<span data-ttu-id="15af9-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15af9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15af9-132">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15af9-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15af9-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="15af9-133">INPUTS</span></span>

### <span data-ttu-id="15af9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="15af9-134">System.String</span></span>

## <span data-ttu-id="15af9-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15af9-135">OUTPUTS</span></span>

### <span data-ttu-id="15af9-136">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="15af9-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="15af9-137">Note</span><span class="sxs-lookup"><span data-stu-id="15af9-137">NOTES</span></span>

## <span data-ttu-id="15af9-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15af9-138">RELATED LINKS</span></span>

[<span data-ttu-id="15af9-139">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="15af9-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="15af9-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="15af9-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="15af9-141">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="15af9-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="15af9-142">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="15af9-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
