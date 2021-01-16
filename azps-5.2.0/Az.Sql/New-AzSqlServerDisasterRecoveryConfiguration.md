---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1D8E8599-113C-4852-8416-1F3359071047
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverdisasterrecoveryconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDisasterRecoveryConfiguration.md
ms.openlocfilehash: a294fd3db4ded19dba2ebd55547ec1c6cbfa9c68
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336832"
---
# <span data-ttu-id="c7a4d-101">New-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7a4d-101">New-AzSqlServerDisasterRecoveryConfiguration</span></span>

## <span data-ttu-id="c7a4d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="c7a4d-103">Crea una configurazione di ripristino di sistema del server di database.</span><span class="sxs-lookup"><span data-stu-id="c7a4d-103">Creates a database server system recovery configuration.</span></span>

## <span data-ttu-id="c7a4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7a4d-104">SYNTAX</span></span>

```
New-AzSqlServerDisasterRecoveryConfiguration -VirtualEndpointName <String> -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-FailoverPolicy <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7a4d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7a4d-105">DESCRIPTION</span></span>
<span data-ttu-id="c7a4d-106">Il cmdlet **New-AzSqlServerDisasterRecoveryConfiguration** crea una configurazione di ripristino di sistema di database di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c7a4d-106">The **New-AzSqlServerDisasterRecoveryConfiguration** cmdlet creates a SQL database server system recovery configuration.</span></span>

## <span data-ttu-id="c7a4d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7a4d-107">EXAMPLES</span></span>

## <span data-ttu-id="c7a4d-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7a4d-108">PARAMETERS</span></span>

### <span data-ttu-id="c7a4d-109">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7a4d-109">-AsJob</span></span>
<span data-ttu-id="c7a4d-110">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="c7a4d-110">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c7a4d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7a4d-111">-DefaultProfile</span></span>
<span data-ttu-id="c7a4d-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c7a4d-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7a4d-113">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="c7a4d-113">-FailoverPolicy</span></span>
<span data-ttu-id="c7a4d-114">Specifica i criteri di failover.</span><span class="sxs-lookup"><span data-stu-id="c7a4d-114">Specifies the failover policy.</span></span>

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

### <span data-ttu-id="c7a4d-115">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7a4d-115">-PartnerResourceGroupName</span></span>
<span data-ttu-id="c7a4d-116">Specifica il nome del gruppo di risorse partner.</span><span class="sxs-lookup"><span data-stu-id="c7a4d-116">Specifies the name of the partner resource group.</span></span>

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

### <span data-ttu-id="c7a4d-117">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="c7a4d-117">-PartnerServerName</span></span>
<span data-ttu-id="c7a4d-118">Specifica il nome del server partner.</span><span class="sxs-lookup"><span data-stu-id="c7a4d-118">Specifies the name of the partner server.</span></span>

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

### <span data-ttu-id="c7a4d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7a4d-119">-ResourceGroupName</span></span>
<span data-ttu-id="c7a4d-120">Specifica il nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c7a4d-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="c7a4d-121">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="c7a4d-121">-ServerName</span></span>
<span data-ttu-id="c7a4d-122">Specifica il nome del server.</span><span class="sxs-lookup"><span data-stu-id="c7a4d-122">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="c7a4d-123">-VirtualEndpointName</span><span class="sxs-lookup"><span data-stu-id="c7a4d-123">-VirtualEndpointName</span></span>
<span data-ttu-id="c7a4d-124">Specifica il nome del punto finale virtuale.</span><span class="sxs-lookup"><span data-stu-id="c7a4d-124">Specifies the name of the virtual end point.</span></span>

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

### <span data-ttu-id="c7a4d-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c7a4d-125">-Confirm</span></span>
<span data-ttu-id="c7a4d-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7a4d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7a4d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7a4d-127">-WhatIf</span></span>
<span data-ttu-id="c7a4d-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7a4d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7a4d-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c7a4d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7a4d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7a4d-130">CommonParameters</span></span>
<span data-ttu-id="c7a4d-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7a4d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7a4d-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7a4d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7a4d-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7a4d-133">INPUTS</span></span>

### <span data-ttu-id="c7a4d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c7a4d-134">System.String</span></span>

## <span data-ttu-id="c7a4d-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7a4d-135">OUTPUTS</span></span>

### <span data-ttu-id="c7a4d-136">Microsoft. Azure. Commands. SQL. ServerDisasterRecoveryConfiguration. Model. AzureSqlServerDisasterRecoveryConfigurationModel</span><span class="sxs-lookup"><span data-stu-id="c7a4d-136">Microsoft.Azure.Commands.Sql.ServerDisasterRecoveryConfiguration.Model.AzureSqlServerDisasterRecoveryConfigurationModel</span></span>

## <span data-ttu-id="c7a4d-137">Note</span><span class="sxs-lookup"><span data-stu-id="c7a4d-137">NOTES</span></span>

## <span data-ttu-id="c7a4d-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7a4d-138">RELATED LINKS</span></span>

[<span data-ttu-id="c7a4d-139">Get-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7a4d-139">Get-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Get-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="c7a4d-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7a4d-140">Remove-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Remove-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="c7a4d-141">Set-AzSqlServerDisasterRecoveryConfiguration</span><span class="sxs-lookup"><span data-stu-id="c7a4d-141">Set-AzSqlServerDisasterRecoveryConfiguration</span></span>](./Set-AzSqlServerDisasterRecoveryConfiguration.md)

[<span data-ttu-id="c7a4d-142">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="c7a4d-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
