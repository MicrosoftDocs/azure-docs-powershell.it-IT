---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationProject.md
ms.openlocfilehash: 99884c23ff99287deb721e3cb76871766cdfa7a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521048"
---
# <span data-ttu-id="d8950-101">New-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="d8950-101">New-AzureRmDataMigrationProject</span></span>

## <span data-ttu-id="d8950-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d8950-102">SYNOPSIS</span></span>
<span data-ttu-id="d8950-103">Crea un nuovo progetto di servizio di migrazione di database di Azure.</span><span class="sxs-lookup"><span data-stu-id="d8950-103">Creates a new Azure Database Migration Service project.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8950-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8950-104">SYNTAX</span></span>

### <span data-ttu-id="d8950-105">ComponentNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d8950-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzureRmDataMigrationProject -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Name <String> -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform>
 [-SourceConnection <ConnectionInfo>] [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d8950-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8950-106">ComponentObjectParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-InputObject] <PSDataMigrationService> -Location <String> -Name <String>
 -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="d8950-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8950-107">ResourceIdParameterSet</span></span>
```
New-AzureRmDataMigrationProject [-ResourceId] <String> -Location <String> -Name <String>
 -SourceType <ProjectSourcePlatform> -TargetType <ProjectTargetPlatform> [-SourceConnection <ConnectionInfo>]
 [-TargetConnection <ConnectionInfo>] [-DatabaseInfo <DatabaseInfo[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="d8950-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8950-108">DESCRIPTION</span></span>
<span data-ttu-id="d8950-109">Il cmdlet New-AzureRmDataMigrationProject crea un nuovo progetto di servizio di migrazione di database di Azure.</span><span class="sxs-lookup"><span data-stu-id="d8950-109">The New-AzureRmDataMigrationProject cmdlet creates a new Azure Database Migration Service project.</span></span> <span data-ttu-id="d8950-110">Questo cmdlet accetta tutti i parametri necessari, ad esempio il nome del gruppo di risorse di Azure, il nome del servizio di migrazione dei dati di Azure in cui deve essere creato il nuovo progetto, l'area geografica in cui deve essere creato il progetto, il nome univoco del nuovo progetto, gli oggetti di connessione di origine e di destinazione e l'oggetto tipo di destinazione, come input per l'elenco di database</span><span class="sxs-lookup"><span data-stu-id="d8950-110">This cmdlet takes in all necessary parameters, such as the name of the Azure Resource Group, the name of Azure Data Migration Service in which new project is to be created, the region in which the project is to be created, the unique name of the new project, the source and target connection objects, and the target type object, as input for the list of databases to migrate.</span></span> <span data-ttu-id="d8950-111">Usa il cmdlet New-AzureRmDataMigrationConnectionInfo per creare un nuovo oggetto ConnectionInfo per le connessioni di origine e di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d8950-111">Use the New-AzureRmDataMigrationConnectionInfo cmdlet to create a new ConnectionInfo object for both the source and target connections.</span></span> <span data-ttu-id="d8950-112">L'elenco di Microsoft. Azure. Management. DataMigration. Models. DatabaseInfo è previsto per i database selezionati. Questo oggetto può essere creato usando il cmdlet New-AzureRmDataMigrationDatabaseInfo.</span><span class="sxs-lookup"><span data-stu-id="d8950-112">The list of Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo is expected for selected databases; this object can be created by using New-AzureRmDataMigrationDatabaseInfo cmdlet.</span></span> 

## <span data-ttu-id="d8950-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8950-113">EXAMPLES</span></span>

### <span data-ttu-id="d8950-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d8950-114">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationProject -ResourceGroupName MyResourceGroup -ServiceName TestService -ProjectName MyDMSProject -Location "central us"  -SourceType SQL -TargetType SQLDB -SourceConnection $sourceConnInfo -TargetConnection $targetConnInfo -DatabaseInfo $dbList
```

<span data-ttu-id="d8950-115">Nell'esempio precedente viene illustrato come creare un nuovo progetto denominato MyDMSProject situato nell'area centrale degli Stati Uniti nell'istanza del servizio di migrazione del database di Azure denominata TestService.</span><span class="sxs-lookup"><span data-stu-id="d8950-115">The above example shows how to create new project named MyDMSProject located in Central US region under the Azure Database Migration Service instance named TestService.</span></span>



## <span data-ttu-id="d8950-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8950-116">PARAMETERS</span></span>

### <span data-ttu-id="d8950-117">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d8950-117">-Confirm</span></span>
<span data-ttu-id="d8950-118">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8950-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8950-119">-DatabaseInfo[]</span><span class="sxs-lookup"><span data-stu-id="d8950-119">-DatabaseInfo[]</span></span>
<span data-ttu-id="d8950-120">Informazioni sul database</span><span class="sxs-lookup"><span data-stu-id="d8950-120">Database information</span></span>

```yaml
Type: DatabaseInfo[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8950-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8950-121">-DefaultProfile</span></span>
<span data-ttu-id="d8950-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d8950-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8950-123">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d8950-123">-Location</span></span>
<span data-ttu-id="d8950-124">Posizione dell'istanza del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="d8950-124">The location of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="d8950-125">-ProjectName</span><span class="sxs-lookup"><span data-stu-id="d8950-125">-ProjectName</span></span>
<span data-ttu-id="d8950-126">Nome del progetto.</span><span class="sxs-lookup"><span data-stu-id="d8950-126">The name of the project.</span></span>

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

### <span data-ttu-id="d8950-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8950-127">-ResourceGroupName</span></span>
<span data-ttu-id="d8950-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d8950-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="d8950-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="d8950-129">-ServiceName</span></span>
<span data-ttu-id="d8950-130">Nome dell'istanza del servizio di migrazione del database di Azure.</span><span class="sxs-lookup"><span data-stu-id="d8950-130">The name of the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="d8950-131">-SourceConnection</span><span class="sxs-lookup"><span data-stu-id="d8950-131">-SourceConnection</span></span>
<span data-ttu-id="d8950-132">Informazioni sulla connessione di origine.</span><span class="sxs-lookup"><span data-stu-id="d8950-132">Source Connection Info.</span></span>

```yaml
Type: ConnectionInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8950-133">-SourceType</span><span class="sxs-lookup"><span data-stu-id="d8950-133">-SourceType</span></span>
<span data-ttu-id="d8950-134">Tipo di piattaforma di origine per Project.</span><span class="sxs-lookup"><span data-stu-id="d8950-134">Source platform type for project.</span></span>

```yaml
Type: ProjectSourcePlatform
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8950-135">-TargetConnection</span><span class="sxs-lookup"><span data-stu-id="d8950-135">-TargetConnection</span></span>
<span data-ttu-id="d8950-136">Informazioni sulla connessione di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d8950-136">Target connection information.</span></span>

```yaml
Type: ConnectionInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8950-137">-TargetType</span><span class="sxs-lookup"><span data-stu-id="d8950-137">-TargetType</span></span>
<span data-ttu-id="d8950-138">Tipo di piattaforma di destinazione per Project.</span><span class="sxs-lookup"><span data-stu-id="d8950-138">Target platform type for project.</span></span>

```yaml
Type: ProjectTargetPlatform
Parameter Sets: (All)
Aliases: 
Accepted values: SQLDB

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```




## <span data-ttu-id="d8950-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8950-139">OUTPUTS</span></span>

### <span data-ttu-id="d8950-140">Microsoft. Azure. Commands. DataMigration. Models. PSProject</span><span class="sxs-lookup"><span data-stu-id="d8950-140">Microsoft.Azure.Commands.DataMigration.Models.PSProject</span></span>


## <span data-ttu-id="d8950-141">Note</span><span class="sxs-lookup"><span data-stu-id="d8950-141">NOTES</span></span>

## <span data-ttu-id="d8950-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8950-142">RELATED LINKS</span></span>

