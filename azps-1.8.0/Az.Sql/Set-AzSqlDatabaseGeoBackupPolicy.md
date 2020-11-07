---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 6ac39ae2daba5f97b9046f3860eb34d3bb0f03ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676750"
---
# <span data-ttu-id="b55bf-101">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b55bf-101">Set-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="b55bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b55bf-102">SYNOPSIS</span></span>
<span data-ttu-id="b55bf-103">Imposta un criterio di Geo backup del database.</span><span class="sxs-lookup"><span data-stu-id="b55bf-103">Sets a database geo backup policy.</span></span>

## <span data-ttu-id="b55bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b55bf-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b55bf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b55bf-105">DESCRIPTION</span></span>
<span data-ttu-id="b55bf-106">Il cmdlet **set-AzSqlDatabaseGeoBackupPolicy** imposta i criteri di backup Geo registrati in un database.</span><span class="sxs-lookup"><span data-stu-id="b55bf-106">The **Set-AzSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="b55bf-107">Questa è una risorsa di backup di Azure usata per definire i criteri di archiviazione di backup.</span><span class="sxs-lookup"><span data-stu-id="b55bf-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="b55bf-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b55bf-108">EXAMPLES</span></span>

## <span data-ttu-id="b55bf-109">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b55bf-109">PARAMETERS</span></span>

### <span data-ttu-id="b55bf-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b55bf-110">-DatabaseName</span></span>
<span data-ttu-id="b55bf-111">Specifica il nome del database per cui questo cmdlet imposta i criteri di backup Geo.</span><span class="sxs-lookup"><span data-stu-id="b55bf-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="b55bf-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b55bf-112">-DefaultProfile</span></span>
<span data-ttu-id="b55bf-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b55bf-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b55bf-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b55bf-114">-ResourceGroupName</span></span>
<span data-ttu-id="b55bf-115">Specifica il nome del gruppo di risorse del server che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="b55bf-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="b55bf-116">-Nomeserver</span><span class="sxs-lookup"><span data-stu-id="b55bf-116">-ServerName</span></span>
<span data-ttu-id="b55bf-117">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="b55bf-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="b55bf-118">-Stato</span><span class="sxs-lookup"><span data-stu-id="b55bf-118">-State</span></span>
<span data-ttu-id="b55bf-119">Specifica lo stato dei criteri di backup Geo.</span><span class="sxs-lookup"><span data-stu-id="b55bf-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="b55bf-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="b55bf-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b55bf-121">Abilitato</span><span class="sxs-lookup"><span data-stu-id="b55bf-121">Enabled</span></span> 
- <span data-ttu-id="b55bf-122">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="b55bf-122">Disabled</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel+GeoBackupPolicyState
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, Enabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b55bf-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b55bf-123">-Confirm</span></span>
<span data-ttu-id="b55bf-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b55bf-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b55bf-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b55bf-125">-WhatIf</span></span>
<span data-ttu-id="b55bf-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b55bf-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b55bf-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b55bf-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b55bf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b55bf-128">CommonParameters</span></span>
<span data-ttu-id="b55bf-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b55bf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b55bf-130">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b55bf-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b55bf-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b55bf-131">INPUTS</span></span>

### <span data-ttu-id="b55bf-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b55bf-132">System.String</span></span>

## <span data-ttu-id="b55bf-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b55bf-133">OUTPUTS</span></span>

### <span data-ttu-id="b55bf-134">Microsoft. Azure. Commands. SQL. backup. Model. AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="b55bf-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="b55bf-135">Note</span><span class="sxs-lookup"><span data-stu-id="b55bf-135">NOTES</span></span>

## <span data-ttu-id="b55bf-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b55bf-136">RELATED LINKS</span></span>

[<span data-ttu-id="b55bf-137">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="b55bf-137">Get-AzSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="b55bf-138">Documentazione di database SQL</span><span class="sxs-lookup"><span data-stu-id="b55bf-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

