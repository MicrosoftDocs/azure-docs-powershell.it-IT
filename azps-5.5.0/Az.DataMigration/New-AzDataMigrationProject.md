---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
ms.openlocfilehash: beed4ef06d567250fefa8cef86da133447a9f20c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200567"
---
# <span data-ttu-id="f9db3-101">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="f9db3-101">New-AzDataMigrationProject</span></span>

## <span data-ttu-id="f9db3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9db3-102">SYNOPSIS</span></span>
<span data-ttu-id="f9db3-103">Crea un nuovo progetto del servizio di migrazione dei database di Azure.</span><span class="sxs-lookup"><span data-stu-id="f9db3-103">Creates a new Azure Database Migration Service project.</span></span>

## <span data-ttu-id="f9db3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f9db3-104">SYNTAX</span></span>

### <span data-ttu-id="f9db3-105">ComponentNameParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f9db3-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9db3-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9db3-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9db3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9db3-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f9db3-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f9db3-108">DESCRIPTION</span></span>
<span data-ttu-id="f9db3-109">Il cmdlet New-AzDataMigrationProject crea un nuovo progetto del servizio di migrazione dei database di Azure.</span><span class="sxs-lookup"><span data-stu-id="f9db3-109">The New-AzDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="f9db3-110">Questo cmdlet accetta tutti i parametri necessari, ad esempio il nome del gruppo di risorse di Azure, il nome del servizio di migrazione dei dati di Azure in cui creare il nuovo progetto, l'area in cui deve essere creato il progetto, il nome univoco del nuovo progetto, gli oggetti di connessione di origine e di destinazione e l'oggetto tipo di destinazione, come input per l'elenco dei database di cui eseguire la migrazione.</span><span class="sxs-lookup"><span data-stu-id="f9db3-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="f9db3-111">Usare il cmdlet New-AzDataMigrationConnectionInfo per creare un nuovo oggetto ConnectionInfo per le connessioni di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f9db3-111">Use the New-AzDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="f9db3-112">Per i database selezionati è previsto l'elenco Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo. questo oggetto può essere creato con New-AzDataMigrationDatabaseInfo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9db3-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="f9db3-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f9db3-113">EXAMPLES</span></span>

### <span data-ttu-id="f9db3-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f9db3-114">Example 1</span></span>
```
PS C:\> New-AzDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="f9db3-115">L'esempio precedente mostra come creare un nuovo progetto denominato MyDMSProject situato nell'area centrale degli Stati Uniti nell'istanza del servizio di migrazione di database di Azure denominata TestService.</span><span class="sxs-lookup"><span data-stu-id="f9db3-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="f9db3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9db3-116">PARAMETERS</span></span>

### <span data-ttu-id="f9db3-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="f9db3-117">-DatabaseInfo</span></span>
<span data-ttu-id="f9db3-118">Informazioni sul database.</span><span class="sxs-lookup"><span data-stu-id="f9db3-118">Database Infos.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9db3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9db3-119">-DefaultProfile</span></span>
<span data-ttu-id="f9db3-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f9db3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9db3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9db3-121">-InputObject</span></span>
<span data-ttu-id="f9db3-122">Oggetto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="f9db3-122">PSDataMigrationService Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService
Parameter Sets: ComponentObjectParameterSet
Aliases: DataMigrationService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9db3-123">-Location</span><span class="sxs-lookup"><span data-stu-id="f9db3-123">-Location</span></span>
<span data-ttu-id="f9db3-124">Posizione dell'istanza del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="f9db3-124">The location of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="f9db3-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f9db3-125">-Name</span></span>
<span data-ttu-id="f9db3-126">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="f9db3-126">The name of the project.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProjectName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9db3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9db3-127">-ResourceGroupName</span></span>
<span data-ttu-id="f9db3-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f9db3-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9db3-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9db3-129">-ResourceId</span></span>
<span data-ttu-id="f9db3-130">ID risorsa DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="f9db3-130">DataMigrationService Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9db3-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f9db3-131">-ServiceName</span></span>
<span data-ttu-id="f9db3-132">Nome dell'istanza del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="f9db3-132">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9db3-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="f9db3-133">-SourceConnection</span></span>
<span data-ttu-id="f9db3-134">Informazioni sulla connessione di origine.</span><span class="sxs-lookup"><span data-stu-id="f9db3-134">Source Connection Info.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9db3-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="f9db3-135">-SourceType</span></span>
<span data-ttu-id="f9db3-136">Tipo di piattaforma di origine per il progetto.</span><span class="sxs-lookup"><span data-stu-id="f9db3-136">Source platform type for project.</span></span>

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

### <span data-ttu-id="f9db3-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="f9db3-137">-TargetConnection</span></span>
<span data-ttu-id="f9db3-138">Informazioni sulla connessione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f9db3-138">Target connection information.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9db3-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="f9db3-139">-TargetType</span></span>
<span data-ttu-id="f9db3-140">Tipo di piattaforma di destinazione per il progetto.</span><span class="sxs-lookup"><span data-stu-id="f9db3-140">Target platform type for project.</span></span>

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

### <span data-ttu-id="f9db3-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9db3-141">-Confirm</span></span>
<span data-ttu-id="f9db3-142">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9db3-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9db3-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9db3-143">-WhatIf</span></span>
<span data-ttu-id="f9db3-144">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9db3-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9db3-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f9db3-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9db3-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9db3-146">CommonParameters</span></span>
<span data-ttu-id="f9db3-147">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9db3-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9db3-148">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9db3-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9db3-149">INPUT</span><span class="sxs-lookup"><span data-stu-id="f9db3-149">INPUTS</span></span>

### <span data-ttu-id="f9db3-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="f9db3-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="f9db3-151">System.String</span><span class="sxs-lookup"><span data-stu-id="f9db3-151">System.String</span></span>

## <span data-ttu-id="f9db3-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f9db3-152">OUTPUTS</span></span>

### <span data-ttu-id="f9db3-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span><span class="sxs-lookup"><span data-stu-id="f9db3-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="f9db3-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="f9db3-154">NOTES</span></span>

## <span data-ttu-id="f9db3-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f9db3-155">RELATED LINKS</span></span>
