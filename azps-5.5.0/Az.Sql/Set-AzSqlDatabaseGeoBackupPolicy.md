---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 5A2072B4-1533-46A2-9841-5509A44DE695
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasegeobackuppolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: 07836205ec7311eadf7e48dd79b322d00670f337
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190998"
---
# <span data-ttu-id="d5827-101">Set-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d5827-101">Set-AzSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="d5827-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5827-102">SYNOPSIS</span></span>
<span data-ttu-id="d5827-103">Imposta i criteri di backup geografici del database.</span><span class="sxs-lookup"><span data-stu-id="d5827-103">Sets a database geo backup policy.</span></span>

## <span data-ttu-id="d5827-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5827-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseGeoBackupPolicy -State <GeoBackupPolicyState> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d5827-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d5827-105">DESCRIPTION</span></span>
<span data-ttu-id="d5827-106">Il **cmdlet Set-AzSqlDatabaseGeoBackupPolicy** imposta il criterio di backup geografico registrato su un database.</span><span class="sxs-lookup"><span data-stu-id="d5827-106">The **Set-AzSqlDatabaseGeoBackupPolicy** cmdlet sets the geo backup policy registered to a database.</span></span>
<span data-ttu-id="d5827-107">Si tratta di una risorsa di backup di Azure usata per definire i criteri di archiviazione di backup.</span><span class="sxs-lookup"><span data-stu-id="d5827-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="d5827-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5827-108">EXAMPLES</span></span>

## <span data-ttu-id="d5827-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5827-109">PARAMETERS</span></span>

### <span data-ttu-id="d5827-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d5827-110">-DatabaseName</span></span>
<span data-ttu-id="d5827-111">Specifica il nome del database per cui questo cmdlet imposta i criteri di backup geografici.</span><span class="sxs-lookup"><span data-stu-id="d5827-111">Specifies the name of the database for which this cmdlet sets the geo backup policy.</span></span>

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

### <span data-ttu-id="d5827-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5827-112">-DefaultProfile</span></span>
<span data-ttu-id="d5827-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="d5827-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5827-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5827-114">-ResourceGroupName</span></span>
<span data-ttu-id="d5827-115">Specifica il nome del gruppo di risorse del server che contiene il database.</span><span class="sxs-lookup"><span data-stu-id="d5827-115">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="d5827-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d5827-116">-ServerName</span></span>
<span data-ttu-id="d5827-117">Specifica il nome del server che ospita il database.</span><span class="sxs-lookup"><span data-stu-id="d5827-117">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="d5827-118">-State</span><span class="sxs-lookup"><span data-stu-id="d5827-118">-State</span></span>
<span data-ttu-id="d5827-119">Specifica lo stato dei criteri di backup geografici.</span><span class="sxs-lookup"><span data-stu-id="d5827-119">Specifies the state of the geo backup policy.</span></span>
<span data-ttu-id="d5827-120">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="d5827-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d5827-121">Abilitato</span><span class="sxs-lookup"><span data-stu-id="d5827-121">Enabled</span></span> 
- <span data-ttu-id="d5827-122">Disabilitato</span><span class="sxs-lookup"><span data-stu-id="d5827-122">Disabled</span></span>

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

### <span data-ttu-id="d5827-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d5827-123">-Confirm</span></span>
<span data-ttu-id="d5827-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5827-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5827-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5827-125">-WhatIf</span></span>
<span data-ttu-id="d5827-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5827-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5827-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5827-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5827-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5827-128">CommonParameters</span></span>
<span data-ttu-id="d5827-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5827-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5827-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d5827-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5827-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="d5827-131">INPUTS</span></span>

### <span data-ttu-id="d5827-132">System.String</span><span class="sxs-lookup"><span data-stu-id="d5827-132">System.String</span></span>

## <span data-ttu-id="d5827-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5827-133">OUTPUTS</span></span>

### <span data-ttu-id="d5827-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d5827-134">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupPolicyModel</span></span>

## <span data-ttu-id="d5827-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="d5827-135">NOTES</span></span>

## <span data-ttu-id="d5827-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5827-136">RELATED LINKS</span></span>

[<span data-ttu-id="d5827-137">Get-AzSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="d5827-137">Get-AzSqlDatabaseGeoBackupPolicy</span></span>](./Get-AzSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="d5827-138">SQL documentazione del database</span><span class="sxs-lookup"><span data-stu-id="d5827-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

