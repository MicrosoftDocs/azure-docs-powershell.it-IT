---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationProject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationProject.md
ms.openlocfilehash: d1f1ae44cf1b6d1b6d3afffa3e13ea34c1ffeb51
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674724"
---
# <span data-ttu-id="58f73-101">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="58f73-101">New-AzDataMigrationProject</span></span>

## <span data-ttu-id="58f73-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58f73-102">SYNOPSIS</span></span>
<span data-ttu-id="58f73-103">Crea un nuovo progetto di servizio di migrazione di database di Azure.</span><span class="sxs-lookup"><span data-stu-id="58f73-103">Creates a new Azure Database Migration Service project.</span></span>

## <span data-ttu-id="58f73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58f73-104">SYNTAX</span></span>

### <span data-ttu-id="58f73-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58f73-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f73-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58f73-106">ComponentObjectParameterSet</span></span>
```
New-AzDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <String> -TargetType <String> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58f73-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58f73-107">ResourceIdParameterSet</span></span>
```
New-AzDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String> -SourceType <String>
 -TargetType <String> [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>]
 [-DatabaseInfo <DatabaseInfo[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="58f73-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58f73-108">DESCRIPTION</span></span>
<span data-ttu-id="58f73-109">Il cmdlet New-AzDataMigrationProject crea un nuovo progetto di servizio di migrazione di database di Azure.</span><span class="sxs-lookup"><span data-stu-id="58f73-109">The New-AzDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="58f73-110">Questo cmdlet accetta tutti i parametri necessari, ad esempio il nome del gruppo di risorse di Azure, il nome del servizio di migrazione dei dati di Azure in cui deve essere creato il nuovo progetto, l'area geografica in cui deve essere creato il progetto, il nome univoco del nuovo progetto, gli oggetti di connessione di origine e di destinazione e l'oggetto tipo di destinazione, come input per l'elenco di database</span><span class="sxs-lookup"><span data-stu-id="58f73-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="58f73-111">Usa il cmdlet New-AzDataMigrationConnectionInfo per creare un nuovo oggetto ConnectionInfo per le connessioni di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="58f73-111">Use the New-AzDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="58f73-112">L'elenco di Microsoft. Azure. Management. DataMigration. Models. DatabaseInfo è previsto per i database selezionati. Questo oggetto può essere creato usando il cmdlet New-AzDataMigrationDatabaseInfo.</span><span class="sxs-lookup"><span data-stu-id="58f73-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="58f73-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58f73-113">EXAMPLES</span></span>

### <span data-ttu-id="58f73-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="58f73-114">Example 1</span></span>
```
PS C:\> New-AzDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="58f73-115">Nell'esempio precedente viene illustrato come creare un nuovo progetto denominato MyDMSProject situato nell'area centrale degli Stati Uniti nell'istanza del servizio di migrazione del database di Azure denominata TestService.</span><span class="sxs-lookup"><span data-stu-id="58f73-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>

## <span data-ttu-id="58f73-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58f73-116">PARAMETERS</span></span>

### <span data-ttu-id="58f73-117">-DatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="58f73-117">-DatabaseInfo</span></span>
<span data-ttu-id="58f73-118">Informazioni sul database.</span><span class="sxs-lookup"><span data-stu-id="58f73-118">Database Infos.</span></span>

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

### <span data-ttu-id="58f73-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58f73-119">-DefaultProfile</span></span>
<span data-ttu-id="58f73-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58f73-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58f73-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58f73-121">-InputObject</span></span>
<span data-ttu-id="58f73-122">Oggetto PSDataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="58f73-122">PSDataMigrationService Object.</span></span>

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

### <span data-ttu-id="58f73-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="58f73-123">-Location</span></span>
<span data-ttu-id="58f73-124">Posizione dell'istanza del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="58f73-124">The location of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="58f73-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="58f73-125">-Name</span></span>
<span data-ttu-id="58f73-126">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="58f73-126">The name of the project.</span></span>

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

### <span data-ttu-id="58f73-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58f73-127">-ResourceGroupName</span></span>
<span data-ttu-id="58f73-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="58f73-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="58f73-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58f73-129">-ResourceId</span></span>
<span data-ttu-id="58f73-130">ID risorsa DataMigrationService.</span><span class="sxs-lookup"><span data-stu-id="58f73-130">DataMigrationService Resource Id.</span></span>

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

### <span data-ttu-id="58f73-131">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="58f73-131">-ServiceName</span></span>
<span data-ttu-id="58f73-132">Nome dell'istanza del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="58f73-132">The name of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="58f73-133">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="58f73-133">-SourceConnection</span></span>
<span data-ttu-id="58f73-134">Informazioni sulla connessione di origine.</span><span class="sxs-lookup"><span data-stu-id="58f73-134">Source Connection Info.</span></span>

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

### <span data-ttu-id="58f73-135">-SourceType</span><span class="sxs-lookup"><span data-stu-id="58f73-135">-SourceType</span></span>
<span data-ttu-id="58f73-136">Tipo di piattaforma di origine per Project.</span><span class="sxs-lookup"><span data-stu-id="58f73-136">Source platform type for project.</span></span>

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

### <span data-ttu-id="58f73-137">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="58f73-137">-TargetConnection</span></span>
<span data-ttu-id="58f73-138">Informazioni sulla connessione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="58f73-138">Target connection information.</span></span>

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

### <span data-ttu-id="58f73-139">-TargetType</span><span class="sxs-lookup"><span data-stu-id="58f73-139">-TargetType</span></span>
<span data-ttu-id="58f73-140">Tipo di piattaforma di destinazione per Project.</span><span class="sxs-lookup"><span data-stu-id="58f73-140">Target platform type for project.</span></span>

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

### <span data-ttu-id="58f73-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="58f73-141">-Confirm</span></span>
<span data-ttu-id="58f73-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58f73-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58f73-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58f73-143">-WhatIf</span></span>
<span data-ttu-id="58f73-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58f73-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58f73-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="58f73-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58f73-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58f73-146">CommonParameters</span></span>
<span data-ttu-id="58f73-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58f73-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58f73-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58f73-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58f73-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58f73-149">INPUTS</span></span>

### <span data-ttu-id="58f73-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="58f73-150">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

### <span data-ttu-id="58f73-151">System. String</span><span class="sxs-lookup"><span data-stu-id="58f73-151">System.String</span></span>

## <span data-ttu-id="58f73-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58f73-152">OUTPUTS</span></span>

### <span data-ttu-id="58f73-153">Microsoft. Azure. Commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="58f73-153">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>

## <span data-ttu-id="58f73-154">Note</span><span class="sxs-lookup"><span data-stu-id="58f73-154">NOTES</span></span>

## <span data-ttu-id="58f73-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58f73-155">RELATED LINKS</span></span>